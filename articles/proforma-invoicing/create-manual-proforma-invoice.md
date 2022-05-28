---
title: Išankstinės sąskaitos faktūros
description: Šioje temoje pateikiama informacija apie išankstines sąskaitas faktūras „Project Operations“.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e20ea17691c592493a790fb38451b35db03416be
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600062"
---
# <a name="proforma-invoices"></a>Išankstinės sąskaitos faktūros

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Išankstinių sąskaitų faktūrų išrašymas suteikia projektų vadovams antrą patvirtinimo lygį prieš sukuriant klientų sąskaitas faktūras. Pirmasis patvirtinimo lygis baigiamas, kai patvirtinami laiko, išlaidų ir medžiagos įrašai, kuriuos pateikia projekto komandos nariai. Patvirtintas išankstines sąskaitas faktūras galima rasti „Project Operations“ projekto apskaitos modulyje. Projekto buhalteriai gali atlikti papildomų naujinimų, pvz., PVM, apskaitai ir sąskaitos faktūros maketui.


## <a name="creating-project-invoices"></a>Projekto sąskaitų faktūrų kūrimas

Projekto sąskaitas faktūras galima kurti po vieną arba dideliais kiekiais. Galite jas kurti rankiniu būdu arba sukonfigūruoti taip, kad jos būtų generuojamos automatiniais paleidimais.

### <a name="manually-create-project-invoices"></a>Projekto sąskaitų faktūrų kūrimas rankiniu būdu 

**Projekto sutarčių** sąrašo puslapyje projekto sąskaitas faktūras galite kurti atskirai kiekvienai projekto sutarčiai arba dideliais kiekiais kelioms projekto sutartims.

Atlikite šį žingsnį, kad sukurtumėte konkrečios projekto sutarties sąskaitą faktūrą.

- **Projekto sutarčių** sąrašo puslapyje atidarykite projekto sutartį ir pažymėkite **Kurti sąskaitą faktūrą**.

    Sąskaita faktūra sugeneruojama visoms pasirinktos projekto sutarties operacijoms, kurių būsena yra **Parengta išrašyti sąskaitą faktūrą**. Šios operacijos apima laiką, išlaidas, medžiagą, etapus ir kitas pardavimo, už kurį neišrašyta sąskaita faktūra, žurnalo eilutes.

Atlikite šiuos veiksmus, kad sukurtumėte sąskaitas faktūras dideliais kiekiais.

1. **Projekto sutarčių** sąrašo puslapyje pažymėkite vieną ar kelias projekto sutartis, kurioms turite sukurti sąskaitą faktūrą, o tada pažymėkite **Kurti projekto sąskaitas faktūras**.

    Įspėjamasis pranešimas informuoja, kad sąskaitų faktūrų sukūrimas gali užimti laiko. Taip pat rodomas procesas.

2. Pasirinkite **Gerai**, kad uždarytumėte pranešimo langą.

    Sąskaita faktūra sugeneruojama visoms projekto eilutės operacijoms, kurių būsena yra **Parengta išrašyti sąskaitą faktūrą**. Šios operacijos apima laiką, išlaidas, medžiagą, etapus ir kitas pardavimo, už kurį neišrašyta sąskaita faktūra, žurnalo eilutes.

3. Norėdami peržiūrėti sugeneruotas sąskaitas faktūras, nueikite į **Pardavimai** \> **Atsiskaitymai** \> **Sąskaitos faktūros.** Kiekvienai projekto sutarčiai matysite po vieną sąskaitą faktūrą.

### <a name="set-up-automated-creation-of-project-invoices"></a>Automatinio projekto sąskaitų faktūrų kūrimo nustatymas 

Norėdami konfigūruoti automatinį sąskaitos faktūros vykdymą, atlikite šiuos veiksmus.

1. Pasirinkite **Parametrai** \> **Paketinės užduotys**.
2. Sukurkite paketinę užduotį ir pavadinkite ją **„Project Operations“ sąskaitų faktūrų kūrimas**. Paketinės užduoties pavadinime turi būti terminas „Kurti sąskaitas faktūras“.
3. Lauke **Užduoties tipas** pažymėkite **Nėra**. Pagal numatytuosius nustatymus, parinktys **Dažnumas: kasdien** ir **Aktyvus** nustatytos į **Taip**.
4. Pasirinkite **Vykdyti darbo eigą**. Dialogo lange **ieškoti įrašo** matysite tris darbo eigas:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Pasirinkite **ProcessRunCaller**, o tada pažymėkite **Įtraukti**.
6. Kitame dialogo lange pasirinkite **Gerai**. Po darbo eigos **Miego režimas** seka darbo eiga **Procesas**.

    Taip pat galite pasirinkti **ProcessRunner** 5 veiksme. Pažymėję **Gerai**, po darbo eigos **Procesas** seka darbo eiga **Miego režimas**.

Darbo eigos **ProcessRunCaller** ir **ProcessRunner** sukuria sąskaitas faktūras. **ProcessRunCaller** iškviečia **ProcessRunner**. **ProcessRunner** yra darbo eiga, kuri iš tikrųjų sukuria sąskaitas faktūras. Ji taikoma visoms sutarties eilutėms, kurioms reikia sukurti SF, ir sukuria tų eilučių sąskaitas faktūras. Norint nustatyti sutarties eilutes, kurioms reikia sukurti SF, užduotis atsižvelgia į projekto eilutėms skirtos sąskaitos faktūros vykdymo datas. Jei vienam projektui priklausančių projekto eilučių sąskaitos faktūros buvo vykdytos tuo pačiu metu, operacijos įtraukiamos į vieną sąskaitą faktūrą, kurioje yra dvi sąskaitos faktūros eilutės. Jei nėra operacijų, skirtų išrašyti sąskaitas faktūras, užduotis nesukuria sąskaitos faktūros.

Kai **ProcessRunner** baigia vykdymą, iškviečiamas **ProcessRunCaller**, pateikiamas pabaigos laikas ir yra uždaromas. Tada **ProcessRunCaller** paleidžia laikmatį, kuris trunka 24 valandas nuo nurodyto pabaigos laiko. Baigiantis laikmačio laikui, **ProcessRunCaller** uždaromas.

Paketinė proceso užduotis, skirta sąskaitoms faktūroms kurti, yra pasikartojanti užduotis. Jei šis paketinis procesas vykdomas daug kartų, sukuriami keli užduoties egzemplioriai ir sukeliamos klaidos. Todėl paketinį procesą reikia pradėti tik vieną kartą, o jį paleisti iš naujo reikia tik tuo atveju, jei jis sustos.

> [!NOTE]
> Paketinių sąskaitų faktūrų išrašymas vykdomas tik projekto sutarties eilutėse, sukonfigūruotose sąskaitų faktūrų grafike. Sutarties eilutė su fiksuotos kainos atsiskaitymų metodu turi turėti sukonfigūruotus etapus. Norint naudoti projekto sutarties eilutę su laiko ir medžiagų atsiskaitymo metodu, reikės nustatyti data pagrįstą sąskaitos faktūros grafiką. Tokia pati tvarka galioja ir projektu pagrįstai sutarties eilutei.      
 
### <a name="edit-a-draft-invoice"></a>Sąskaitos faktūros juodraščio redagavimas

Sukūrus juodraštinę projekto sąskaitą faktūrą, visos pardavimo operacijos, už kurias neišrašyta sąskaita, sukurtos, kai laiko, išlaidų ir medžiagų naudojimo įrašai buvo patvirtinti, yra įtraukiamos į sąskaitą faktūrą. Galite atlikti šiuos koregavimus, kai sąskaita faktūra vis dar yra juodraščio etape:

- Naikinti arba redaguoti sąskaitos faktūros eilutės išsamią informaciją.
- Redaguoti ir koreguoti kiekį ir atsiskaitymo tipą.

Pažymėkite **Patvirtinti**, kad patvirtintumėte sąskaitą faktūrą. Patvirtinimo veiksmas yra vienpusis veiksmas. Pasirinkus **Patvirtinti**, sąskaita faktūra sistemoje tampa tik skaitoma ir sukuriami faktiniai pardavimai, už kuriuos išrašyta sąskaita, iš kiekvienos sąskaitos faktūros eilutės išsamios informacijos kiekvienai sąskaitos faktūros eilutei. Jei sąskaitos faktūros eilutėje nurodomas faktinis pardavimas, už kurį neišrašyta sąskaita, sistema taip pat atšaukia faktinį pardavimą, už kurį neišrašyta sąskaita. (Bet kuri sąskaitos faktūros eilutės išsami informacija, sukurta naudojant laiko ar išlaidų įrašą, nurodo faktinį pardavimą, už kurį neišrašyta sąskaita). Didžiosios knygos integravimo sistemos gali naudoti šį atšaukimą, kad atšauktų projekto nebaigtą gamybą (NG) apskaitos tikslais.

> [!NOTE]
> Patvirtintų proformos SF ir susijusių įrašų, pvz., SF eilučių ir SF eilutės informacijos, redaguoti arba panaikinti negalima. 

### <a name="correct-a-confirmed-invoice"></a>Patvirtintos sąskaitos faktūros taisymas

Patvirtintas sąskaitas faktūras galima redaguoti (taisyti). Pataisius patvirtintą sąskaitą faktūrą, sukuriama nauja juodraštinė koreguojamoji sąskaita faktūra. Kadangi daroma prielaida, kad norite atšaukti visas operacijas ir kiekius iš pradinės sąskaitos faktūros, į šią koreguojamąją sąskaitą faktūrą įeina visos operacijos iš pradinės sąskaitos faktūros, o visi joje esantys kiekiai yra 0 (nulis).

Jei tam tikrų operacijų taisyti nereikia, galite jas pašalinti iš juodraštinės koreguojamosios sąskaitos faktūros. Jei norite atšaukti arba grąžinti tik dalinį kiekį, galite redaguoti eilutės informacijos lauką **Kiekis**. Jei atidarote sąskaitos faktūros eilutės išsamią informaciją, galite peržiūrėti pradines sąskaitos faktūros kiekį. Tada galite redaguoti dabartinės sąskaitos faktūros kiekį, kad jis būtų mažesnis arba didesnis nei pradinės sąskaitos faktūros kiekis.

Patvirtinus koreguojamąją sąskaitą faktūrą, pradinis faktinis pardavimas, už kurį išrašyta sąskaita, yra atšaukiamas ir sukuriamas naujas faktinis pardavimas, už kurį išrašyta sąskaita. Jei kiekis sumažintas, dėl skirtumo taip pat bus sukuriamas naujas faktinis pardavimas, už kurį neišrašyta sąskaita. Pavyzdžiui, jei pradinio pardavimo, už kurį išrašyta sąskaita, kiekis yra aštuonios valandos, o koreguojamosios sąskaitos faktūros eilutės išsamioje informacijoje nurodomas sumažintas šešių valandų kiekis, pradinio pardavimo, už kurį išrašyta sąskaita faktūra, eilutė atšaukiama ir sukuriami du nauji faktiniai duomenys:

- Šešių valandų faktinis pardavimas, už kurį išrašyta sąskaita.
- Likusių dviejų valandų faktinis pardavimas, už kurį neišrašyta sąskaita. Šiai operacijai vėliau galima išrašyti sąskaitą arba pažymėti ją kaip neapmokestinamąją, atsižvelgiant į derybas su klientu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
