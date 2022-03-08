---
title: Išankstinės projekto sąskaitos faktūros
description: Šioje temoje pateikiama informacija apie „Project Operations“ išankstines projektu pagrįstas sąskaitas faktūras.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3d02728ce682781eb8816e0c2239cf62f88adfa8c5d2a0aab280be053c2a5ae6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992936"
---
# <a name="proforma-project-pnvoices"></a>Išankstinės projekto sąskaitos faktūros

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projekto išankstinių sąskaitų faktūrų išrašymas suteikia projektų vadovams antrą patvirtinimo lygį prieš sukuriant klientų sąskaitas faktūras. Pirmasis patvirtinimo lygis baigiamas, kai patvirtinami laiko, išlaidų ir medžiagos įrašai, kuriuos pateikia projekto komandos nariai.

„Dynamics 365 Project Operations Lite“ visuotinis diegimas nėra sukurtas klientui prieinamoms sąskaitoms faktūroms generuoti. Toliau pateiktame sąraše nurodyta, kodėl negalima generuoti sąskaitų faktūrų.

- Programoje nėra mokesčių informacijos.
- Nėra galimybės konvertuoti kitų valiutų į sąskaitų faktūrų išrašymo valiutą.
- Nėra galimybės tinkamai suformatuoti sąskaitų faktūrų, kad būtų galima atsispausdinti.

Vietoje to galite naudoti finansų arba apskaitos sistemą, kad sukurtumėte klientui prieinamas sąskaitas faktūras, kuriose naudojama sugeneruotose sąskaitos faktūros pasiūlymuose naudojama informacija.

## <a name="creating-project-invoices"></a>Projekto sąskaitų faktūrų kūrimas

Projekto sąskaitas faktūras galima kurti po vieną arba dideliais kiekiais. Galite jas kurti rankiniu būdu arba sukonfigūruoti taip, kad jos būtų generuojamos automatiniais paleidimais.

### <a name="manually-create-project-invoices"></a>Projekto sąskaitų faktūrų kūrimas rankiniu būdu 

Sąrašo puslapyje **Projekto sutartys** galite sukurti projekto sąskaitas faktūras atskirai kiekvienai projekto sutarčiai arba dideliais kiekiais kelioms projekto sutartims.

   - Norėdami sukurti konkrečios projekto sutarties sąskaitą faktūrą, sąrašo puslapyje **Projekto sutartys** atidarykite projekto sutartį, tada pasirinkite **Kurti projekto sąskaitą faktūrą**.

   Sąskaita faktūra sugeneruojama visoms pasirinktos projekto sutarties operacijoms, kurių būsena yra **Parengta išrašyti sąskaitą faktūrą**. Į šias operacijas įtraukiamos laiko, išlaidų, medžiagų, etapų, produktu pagrįstos sutarties eilutės ir kitos pardavimo žurnalo eilutės, už kurias neišrašyta sąskaita ir kurias galima būti patvirtinti.

Norėdami sąskaitas faktūras sukurti dideliais kiekiais, atlikite toliau nurodytus veiksmus.

1. Sąrašo puslapyje **Projekto sutartys** pažymėkite vieną ar kelias projekto sutartis, kurioms norite sukurti sąskaitą faktūrą, tada pasirinkite **Kurti projekto sąskaitas faktūras**.
2. Įspėjamasis pranešimas informuoja, kad sąskaitų faktūrų sukūrimas gali užimti laiko. Taip pat rodomas procesas. Pasirinkite **Gerai**, kad uždarytumėte pranešimo langą.

   Sąskaita faktūra sugeneruojama visoms projekto eilutės operacijoms, kurių būsena yra **Parengta išrašyti sąskaitą faktūrą**. Į šias operacijas įtraukiamos laiko, išlaidų, medžiagų, etapų, produktu pagrįstos sutarties eilutės ir kitos pardavimo žurnalo eilutės, už kurias neišrašyta sąskaita ir kurias galima būti patvirtinti.

3. Sugeneruotas sąskaitas faktūras peržiūrėkite apsilankę **Pardavimai** \> **Atsiskaitymai** \> **Sąskaitos faktūros**. Kiekvienai projekto sutarčiai matysite po vieną sąskaitą faktūrą.

### <a name="set-up-automated-creation-of-project-invoices"></a>Automatinio projekto sąskaitų faktūrų kūrimo nustatymas 

Norėdami konfigūruoti automatinį sąskaitos faktūros vykdymą, atlikite šiuos veiksmus.

1. Pasirinkite **Parametrai** \> **Paketinės užduotys**.
2. Sukurkite paketinę užduotį ir pavadinkite ją **„Project Operations“ sąskaitų faktūrų kūrimas**. Paketinės užduoties pavadinime turi būti terminas „Kurti sąskaitas faktūras“.
3. Lauke **Užduoties tipas** pažymėkite **Nėra**. Pagal numatytuosius nustatymus, parinktys **Dažnumas: kasdien** ir **Aktyvus** nustatytos į **Taip**.
4. Pasirinkite **Vykdyti darbo eigą**. Dialogo lange **Ieškoti įrašo** matysite tris toliau nurodytas darbo eigas.

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Pasirinkite **ProcessRunCaller**, o tada pažymėkite **Įtraukti**.
6. Kitame dialogo lange pasirinkite **Gerai**. Po darbo eigos **Miego režimas** seka darbo eiga **Procesas**.

    Taip pat galite pasirinkti **ProcessRunner** 5 veiksme. Pažymėję **Gerai**, po darbo eigos **Procesas** seka darbo eiga **Miego režimas**.

Darbo eigos **ProcessRunCaller** ir **ProcessRunner** sukuria sąskaitas faktūras. **ProcessRunCaller** iškviečia **ProcessRunner**. **ProcessRunner** yra darbo eiga, kurią naudojant sukuriamos sąskaitos faktūros. Ši darbo eiga taikoma visoms sutarties eilutėms, kurioms reikia sukurti SF, ir sukuria sąskaitas faktūras. Norint nustatyti sutarties eilutes, kurioms reikia sukurti SF, darbo eiga atsižvelgia į projekto eilutėms skirtos sąskaitos faktūros vykdymo datas. Jei vienam projektui priklausančių projekto eilučių sąskaitos faktūros buvo vykdytos tuo pačiu metu, operacijos įtraukiamos į vieną sąskaitą faktūrą, kurioje yra dvi sąskaitos faktūros eilutės. Jei nėra operacijų, skirtų išrašyti sąskaitas faktūras, sąskaitos faktūros nesukuriamos.

Kai **ProcessRunner** baigia vykdymą, iškviečiamas **ProcessRunCaller**, pateikiamas pabaigos laikas ir yra uždaromas. Tada **ProcessRunCaller** paleidžia laikmatį, kuris trunka 24 valandas nuo nurodyto pabaigos laiko. Baigiantis laikmačio laikui, **ProcessRunCaller** uždaromas.

Paketinė proceso užduotis, skirta sąskaitoms faktūroms kurti, yra pasikartojanti užduotis. Jei šis paketinis procesas vykdomas daug kartų, sukuriami keli užduoties egzemplioriai ir gali būti sukeltos klaidos. Norėdami šios problemos išvengti, paketinį procesą pradėkite tik vieną kartą, o jį iš naujo paleiskite tik tuo atveju, jei jis sustos.

> [!NOTE]
> Paketinių sąskaitų faktūrų išrašymas vykdomas tik projekto sutarties eilutėse, sukonfigūruotose sąskaitų faktūrų grafike. Sutarties eilutė su fiksuotos kainos atsiskaitymų metodu turi turėti sukonfigūruotus etapus. Norint naudoti projekto sutarties eilutę su laiko ir medžiagų atsiskaitymo metodu, reikės nustatyti data pagrįstą sąskaitos faktūros grafiką. Tokia pati tvarka galioja ir projektu pagrįstai sutarties eilutei.      
 
### <a name="edit-a-draft-invoice"></a>Sąskaitos faktūros juodraščio redagavimas

Sukūrus juodraštinę projekto sąskaitą faktūrą, visos pardavimo operacijos, už kurias neišrašyta sąskaita, sukurtos, kai laiko ir išlaidų įrašai buvo patvirtinti, yra įtraukiamos į sąskaitą faktūrą. Galite atlikti šiuos koregavimus, kai sąskaita faktūra vis dar yra juodraščio etape:

- Naikinti arba redaguoti sąskaitos faktūros eilutės išsamią informaciją.
- Redaguoti ir koreguoti kiekį ir atsiskaitymo tipą.
- Į sąskaitą faktūrą tiesiogiai įtraukti laiko, medžiagos ir išlaidų mokesčių operacijas. Galite naudoti šią funkciją, jei sąskaitos faktūros eilutė susieta su sutarties eilute, kurioje leidžiama atlikti šias operacijų klases.

Pažymėkite **Patvirtinti**, kad patvirtintumėte sąskaitą faktūrą. Šis veiksmas yra vienpusis veiksmas. Pasirinkus **Patvirtinti**, sąskaita faktūra tampa tik skaitoma ir sukuriami faktiniai pardavimai, už kuriuos išrašyta sąskaita, iš kiekvienos sąskaitos faktūros eilutės išsamios informacijos kiekvienai sąskaitos faktūros eilutei. Jei sąskaitos faktūros eilutėje nurodomas faktinis pardavimas, už kurį neišrašyta sąskaita, faktinis pardavimas, už kurį neišrašyta sąskaita, atšaukiamas. Sąskaitos faktūros eilutės išsami informacija, kuri buvo sukurta pagal laiko, išlaidų arba medžiagos naudojimo įrašą, nurodys faktinį pardavimą, už kurį neišrašyta sąskaita. Didžiosios knygos integravimo sistemose šis atšaukimas gali būti naudojamas norint atšaukti projekto nebaigtą gamybą (NG) apskaitos tikslais.

### <a name="correct-a-confirmed-invoice"></a>Patvirtintos sąskaitos faktūros taisymas

Patvirtintas sąskaitas faktūras galima redaguoti. Pataisius patvirtintą sąskaitą faktūrą, sukuriama nauja juodraštinė koreguojamoji sąskaita faktūra. Kadangi daroma prielaida, kad norite atšaukti visas operacijas ir kiekius iš pradinės sąskaitos faktūros, į šią koreguojamąją sąskaitą faktūrą įeina visos operacijos iš pradinės sąskaitos faktūros, o visi joje esantys kiekiai yra nuliniai.

Jei yra operacijų, kurių taisyti nereikia, galite jas pašalinti iš juodraštinės koreguojamosios sąskaitos faktūros. Jei norite atšaukti arba grąžinti tik dalinį kiekį, galite redaguoti eilutės informacijos lauką **Kiekis**. Jei atidarote sąskaitos faktūros eilutės išsamią informaciją, galite peržiūrėti pradines sąskaitos faktūros kiekį. Tada galite redaguoti dabartinės sąskaitos faktūros kiekį, kad jis būtų mažesnis arba didesnis nei pradinės sąskaitos faktūros kiekis.

Patvirtinus koreguojamąją sąskaitą faktūrą, pradinis faktinis pardavimas, už kurį išrašyta sąskaita, yra atšaukiamas ir sukuriamas naujas faktinis pardavimas, už kurį išrašyta sąskaita. Jei kiekis sumažintas, dėl skirtumo bus sukuriamas naujas faktinis pardavimas, už kurį neišrašyta sąskaita. Pavyzdžiui, jei pradinio pardavimo, už kurį išrašyta sąskaita, kiekis yra aštuonios valandos, o koreguojamosios sąskaitos faktūros eilutės išsamioje informacijoje nurodomas sumažintas šešių valandų kiekis, pradinio pardavimo, už kurį išrašyta sąskaita faktūra, eilutė atšaukiama ir sukuriami du nauji toliau nurodyti faktiniai duomenys.

- Šešių valandų faktinis pardavimas, už kurį išrašyta sąskaita.
- Likusių dviejų valandų faktinis pardavimas, už kurį neišrašyta sąskaita. Šiai operacijai vėliau galima išrašyti sąskaitą arba pažymėti ją kaip neapmokestinamąją, atsižvelgiant į derybas su klientu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
