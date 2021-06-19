---
title: Vidinės įmonės operacijų kūrimas
description: Šioje temoje pateikiama informacijos, kaip kurti vidinės įmonės operacijas.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0e396f0d08fd166e7acd6f8ec8f32353a7679dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013361"
---
# <a name="create-intercompany-transactions"></a>Vidinės įmonės operacijų kūrimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Vidinės įmonės operacijos yra laiko ir išlaidų operacijos iš projekto sutarties, priklausančios vienai įmonei arba organizaciniam vienetui, kai projekto sutarties ištekliai priklauso kitai įmonei arba organizaciniam vienetui.

Patvirtinus vidinės įmonės operaciją, sukuriamos toliau nurodytos faktinės operacijos

| **Operacijos tipas** | **Taikomas kainoraštis** | **Operacijos valiuta** |
| --- | --- | --- |
| Savikaina | Sutartį sudarančio vieneto savikainos kainoraštis | Valiuta kainos eilutėje |
| Pardavimas, už kurį neišrašyta sąskaita. Sukuriama tik faktiniams duomenims, susietiems su sutarties eilute, turinčia atsiskaitymo tipą, laiką ir medžiagas. | Sutarties projekto pardavimo kainoraštis | Sutarties valiuta |
| Išteklių paskirstymo vieneto savikaina | Išteklių paskirstymo vieneto savikainos kainoraštis | Valiuta kainos eilutėje |
| Tarp organizacijų vykdomas pardavimas | Sutartį sudarančio vieneto savikainos kainoraštis | Valiuta kainos eilutėje |

Savikainą, išteklių paskirstymo vieneto savikainą ir tarp organizacijų vykdomo pardavimo operacijos kainą ir valiutą valdo **organizacinis vienetas**. Tai svarbu prisiminti priimant sprendimą, kaip diegimo aplinkoje struktūrizuoti įmones ir organizacinius vienetus.

Kai kuriate galimybę, pasiūlymą, projekto sutartį ir projekto įrašus, sistema patikrina, ar sutartį sudarančio vieneto valiuta atitinka sutartį sudarančios įmonės apskaitos valiutą. Jei jos nesutampa, šių įrašo sukurti nepavyks. Organizacinio vieneto valiutą galima apibrėžti „Dynamics 365 Project Operations“ dalyje **„Dataverse“** > **Parametrai** > **Organizaciniai vienetai**. Įmonės apskaitos valiutą galima nurodyti „Dynamics 365 Finance“ dalyje **Didžioji knyga** > **DK nustatymas** > **Didžioji knyga**. Valiuta sinchronizuojama su jūsų „Dataverse“ aplinka naudojant didžiųjų knygų dvigubo rašymo struktūrą.

Sistema sukuria išteklių paskirstymo vieneto savikainą ir tarp organizacijų vykdomo pardavimo faktinius duomenis toliau nurodytais atvejais.

  - Kai išteklių paskirstymo vienetas skiriasi nuo sutartį sudarančio vieneto
  - Kai išteklių paskirstymo įmonė skiriasi nuo sutartį sudarančios įmonės

Tačiau tik operacijos, kurių išteklių paskirstymo įmonė skiriasi nuo sutartį sudarančios įmonės, bus perkeltos į „Dynamics 365 Finance“ aplinką papildomos apskaitos tikslais.

Projekto faktinių duomenų apskaita įrašoma į „Project Operations“integravimo žurnalą dalyje „Finance“. Sistema sukuria toliau nurodytas žurnalo eilutes.

| **Operacijos tipas** | **Juridinis subjektas** | **Sukuria projekto operaciją registruojant** | **Numatytosios finansinių dimensijų reikšmės gaunamos iš** | **Numatytoji atsiskaitymo PVM grupė ir atsiskaitymo elemento PVM grupė** |
| --- | --- | --- | --- | --- |
| Savikaina | Nepridedama prie integravimo žurnalo | Nėra | Nėra | Nėra |
| Neišrašytas pardavimas | Besiskolinančio juridinio subjekto integravimo žurnalas | Taip | Project | **Atsiskaitymo PVM grupė**: remiantis **sutarties klientu** <br/> **Atsiskaitymo elemento PVM grupė**: iš esamo juridinio subjekto projekto kategorijos žurnalo eilutėje |
| Išteklių paskirstymo vieneto savikaina | Skolinančio juridinio subjekto integravimo žurnalas | No | Vidinės įmonės klientas | **Atsiskaitymo PVM grupė**: remiantis **vidinės įmonės klientu** <br/> **Atsiskaitymo elemento PVM grupė**: iš esamo juridinio subjekto projekto kategorijos žurnalo eilutėje |
| Tarp organizacijų vykdomas pardavimas | Skolinančio juridinio subjekto integravimo žurnalas | No | Vidinės įmonės klientas | **Atsiskaitymo PVM grupė**: remiantis **vidinės įmonės klientu** <br/> **Atsiskaitymo elemento PVM grupė**: iš esamo juridinio subjekto projekto kategorijos žurnalo eilutėje |

### <a name="example-intercompany-transactions"></a>Pavyzdys: vidinės įmonės operacijos

Simona Terentjeva, GBPM dirbanti kūrėja, užregistravo, kad dirbo 10 darbo valandų su „USPM Adventure Works“ projektu, kurį patvirtino projekto vadovas. Kūrėjo valandinis įkainis įmonėje GBPM yra 88 GBP. GBPM įmonei USPM pateiks sąskaitą, kurioje nurodytas 120 USD valandinis kūrėjo įkainis. USPM pateiks klientui „Adventure Works“ sąskaitą, kurioje nurodytas 200 USD įkainis už GBPM ištekliaus darbą. Norėdami gauti daugiau informacijos žr. [Vidinės įmonės SF išrašymo konfigūravimas](configure-intercompany-invoicing.md).

1. „Project Operations“ eikite į **Ištekliai** ir sąraše pasirinkite **Simona Terentjeva**. Skirtuko **Planavimas** lauke **Įmonė** pasirinkite **GBPM**.
2. Eikite į **Pardavimas** > **Klientai** ir pasirinkite **Naujas**, kad  to create sukurtumėte naują kliento įrašą, skirtą „Adventure Works“.
    1. Nustatykite įmonę **USPM**.
    2. Nustatykite **Ryšio tipas** parinktį **Klientas**.
    3. Pasirinkite **10 klientų grupė – vietinis**.
    4. Nustatykite valiutą **USD**.
    5. Įrašykite įrašą.
3. Eikite į **Pardavimas** > **Projekto sutartys** ir sukurkite naują projekto sutartį, skirtą „Adventure Works“.
    1. Valdančią įmonę nustatykite kaip **USPM**, o sutartį sudarantį vienetą – kaip **„Contoso Robotics US“**.
    2. Pasirinkite „Adventure Works“ kaip klientą.
    3. Pasirinkite produkto kainoraštį ir įrašykite įrašą.
    4. Skirtuke **Sutarties eilutės** sukurkite naują sutarties eilutę. Nustatykite bet kokį pavadinimą ir pasirinkite **Laikas ir medžiagos** kaip atsiskaitymo metodą.
    5. Sukurkite naują projektą ir susiekite jį su šia sutarties eilute.
4. Prisijunkite kaip išteklius **Simona Terentjeva**. Eikite į **Projektai** > **Laiko įrašai** ir sukurkite laiko įrašą, skirtą „Adventure Works“ projektui.
5. Prisijunkite kaip projekto vadovas. Eikite į **Projektai** > **Patvirtinimai** ir patvirtinkite laiko įrašo operaciją, kurią užregistravo Simona Terentjeva.
6. Eikite į „Adventure Works“ projektą ir pasirinkite **Susiję** > **Faktiniai duomenys**. Sukuriamos toliau nurodytos faktinių operacijų operacijos.

| **Operacijos tipas** | **Kainos** | **Operacijos valiuta** | **Suma** |
| --- | --- | --- | --- |
| Savikaina | 120 | USD | 1200 |
| Neišrašytas pardavimas | Virš 200 | USD | 2000 |
| Išteklių paskirstymo vieneto savikaina | 88 | GBP | 880 |
| Tarp organizacijų vykdomas pardavimas | 120 | USD | 1200 |

7. Prisijunkite kaip USPM buhalteris. Atidarykite „Project Operations“ egzempliorių „Finance“ ir pasirinkite įmonę **USPM**. 
8. Eikite į **Projektų valdymas ir apskaita** > **Periodiniai** > **„Project Operations“ ir „Customer Engagement“** > **Importuoti iš paruošimo** ir pasirinkite vykdyti periodinį procesą. Šis periodinis procesas užpildys „Project Operations“ integravimo žurnalą.
9. Eikite į **Projektų valdymas ir apskaita** > **Žurnalai** > **„Project Operations“ integravimo žurnalas** ir peržiūrėkite žurnalo eilutes. Sistema sukuria toliau nurodytą eilutę.

    | **Operacijos tipas** | **Kainos** | **Operacijos valiuta** | **Suma** |
    | --- | --- | --- | --- |
    | Neišrašytas pardavimas | Virš 200 | USD | 2000 |

    Jei sistema yra nustatyta kaupti šio projekto įplaukas, užregistruojami toliau nurodyti duomenys.

    - Debetas: projektas – NG pardavimo vertė 200 USD
    - Kreditas: projektas – sukauptos įplaukos 200 USD

    Šis pardavimas, už kurį neišrašyta sąskaita, jau paruoštas SF išrašyti. Prireikus galima finansiškai užregistruoti klientui „Adventure Works“ skirtą sąskaitą faktūrą.

10. Prisijunkite kaip **GBPM** buhalteris. Atidarykite „Project Operations“ egzempliorių „Finance“ ir atidarykite įmonę **GBPM**. 
11. Nueikite į **Projektų tvarkymas ir apskaita** > **Periodinis** > **„Project Operations“ integravimas** > **Importuoti iš eilučių paruošimo lentelės** ir vykdykite procesą, kad užpildytumėte „Project Operations“ integravimo žurnalą.
12. Eikite į **Projektų valdymas ir apskaita** > **Žurnalai** > **„Project Operations“ integravimo žurnalas** ir peržiūrėkite eilutes. Sistema sukuria toliau nurodytas eilutes.

    | **Operacijos tipas** | **Kainos** | **Operacijos valiuta** | **Suma** |
    | --- | --- | --- | --- |
    | Išteklių paskirstymo vieneto savikaina | 88 | GBP | 880 |
    | Tarp organizacijų vykdomas pardavimas | 120 | USD | 1200 |

    Užregistravus šiuos įrašus sukuriamos toliau nurodytos kvito operacijos.

    - Debetas: projekto savikaina 88 GBP
    - Kreditas: Atlyginimo paskirstymas 88 GBP

    Jei sistema yra nustatyta kaupti vidinės įmonės įplaukas, užregistruojami toliau nurodyti duomenys.

    - Debetas: projektas – NG pardavimo vertė 120 USD
    - Kreditas: projektas – sukauptos įplaukos 120 USD

    Sistema jau paruošta kurti vidinės įmonės kliento sąskaitą faktūrą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
