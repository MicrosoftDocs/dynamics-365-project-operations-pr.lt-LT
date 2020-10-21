---
title: Neautomatinės „Proforma“ sąskaitos faktūros kūrimas
description: Šioje temoje pateikta informacija, kaip sukurti „Proforma“ sąskaitą faktūrą.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ad85262482f782391eca85f46ca0e63a887c89f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896120"
---
# <a name="create-a-manual-proforma-invoice"></a>Neautomatinės „Proforma“ sąskaitos faktūros kūrimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Sąskaitų faktūrų išrašymas suteikia projektų vadovams antrą patvirtinimo lygį prieš sukuriant klientų sąskaitas faktūras. Pirmasis patvirtinimo lygis baigiamas, kai patvirtinami laiko ir išlaidų įrašai, kuriuos pateikia projekto komandos nariai.

„Dynamics 365 Project Operations“ nėra sukurta norint generuoti klientui prieinamas sąskaitas faktūras dėl šių priežasčių:

- Joje nėra mokesčių informacijos.
- Ji negali konvertuoti kitų valiutų į sąskaitų faktūrų išrašymo valiutą naudojant tinkamai sukonfigūruotus valiutos kursus.
- Joje negalima tinkamai formatuoti sąskaitų faktūrų, kad jas būtų galima išspausdinti.

Vietoje to galite naudoti finansų arba apskaitos sistemą, kad sukurtumėte klientui prieinamas sąskaitas faktūras, kuriose naudojama sugeneruotū sąskaitos faktūros pasiūlymų informacija.

## <a name="creating-project-invoices"></a>Projekto sąskaitų faktūrų kūrimas

Projekto sąskaitas faktūras galima kurti po vieną arba dideliais kiekiais. Galite jas kurti rankiniu būdu arba sukonfigūruoti taip, kad jos būtų generuojamos automatiniais paleidimais.

### <a name="manually-create-project-invoices"></a>Projekto sąskaitų faktūrų kūrimas rankiniu būdu 

**Projekto sutarčių** sąrašo puslapyje projekto sąskaitas faktūras galite kurti atskirai kiekvienai projekto sutarčiai arba dideliais kiekiais kelioms projekto sutartims.

Atlikite šį žingsnį, kad sukurtumėte konkrečios projekto sutarties sąskaitą faktūrą.

- **Projekto sutarčių** sąrašo puslapyje atidarykite projekto sutartį ir pažymėkite **Kurti sąskaitą faktūrą**.

    Sąskaita faktūra sugeneruojama visoms pasirinktos projekto sutarties operacijoms, kurių būsena yra **Parengta išrašyti sąskaitą faktūrą**. Į šias operacijas įtrauktos laiko, išlaidų, etapų ir produktu pagrįstos sutarties eilutės.

Atlikite šiuos veiksmus, kad sukurtumėte sąskaitas faktūras dideliais kiekiais.

1. **Projekto sutarčių** sąrašo puslapyje pažymėkite vieną ar kelias projekto sutartis, kurioms turite sukurti sąskaitą faktūrą, o tada pažymėkite **Kurti projekto sąskaitas faktūras**.

    Įspėjamasis pranešimas informuoja, kad sąskaitų faktūrų sukūrimas gali užimti laiko. Taip pat rodomas procesas.

2. Pasirinkite **Gerai**, kad uždarytumėte pranešimo langą.

    Sąskaita faktūra sugeneruojama visoms projekto eilutės operacijoms, kurių būsena yra **Parengta išrašyti sąskaitą faktūrą**. Į šias operacijas įtrauktos laiko, išlaidų, etapų ir produktu pagrįstos sutarties eilutės.

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
6. Kitame dialogo lange pasirinkite **Gerai**. Po darbo eigos **Miego režimas**seka darbo eiga **Procesas**.

    Taip pat galite pasirinkti **ProcessRunner** 5 veiksme. Pažymėję **Gerai**, po darbo eigos **Procesas** seka darbo eiga **Miego režimas**.

Darbo eigos **ProcessRunCaller** ir **ProcessRunner** sukuria sąskaitas faktūras. **ProcessRunCaller** iškviečia **ProcessRunner**. **ProcessRunner** yra darbo eiga, kuri iš tikrųjų sukuria sąskaitas faktūras. Ji taikoma visoms sutarties eilutėms, kurioms reikia sukurti SF, ir sukuria tų eilučių sąskaitas faktūras. Norint nustatyti sutarties eilutes, kurioms reikia sukurti SF, užduotis atsižvelgia į projekto eilutėms skirtos sąskaitos faktūros vykdymo datas. Jei vienam projektui priklausančių projekto eilučių sąskaitos faktūros buvo vykdytos tuo pačiu metu, operacijos įtraukiamos į vieną sąskaitą faktūrą, kurioje yra dvi sąskaitos faktūros eilutės. Jei nėra operacijų, skirtų išrašyti sąskaitas faktūras, užduotis nesukuria sąskaitos faktūros.

Kai **ProcessRunner** baigia vykdymą, iškviečiamas **ProcessRunCaller**, pateikiamas pabaigos laikas ir yra uždaromas. Tada **ProcessRunCaller** paleidžia laikmatį, kuris trunka 24 valandas nuo nurodyto pabaigos laiko. Baigiantis laikmačio laikui, **ProcessRunCaller** uždaromas.

Paketinė proceso užduotis, skirta sąskaitoms faktūroms kurti, yra pasikartojanti užduotis. Jei šis paketinis procesas vykdomas daug kartų, sukuriami keli užduoties egzemplioriai ir sukeliamos klaidos. Todėl paketinį procesą reikia pradėti tik vieną kartą, o jį paleisti iš naujo reikia tik tuo atveju, jei jis sustos.

> [!NOTE]
> Paketinių sąskaitų faktūrų išrašymas vykdomas tik projekto sutarties eilutėse, sukonfigūruotose sąskaitų faktūrų grafike. Sutarties eilutė su fiksuotos kainos atsiskaitymų metodu turi turėti sukonfigūruotus etapus. Norint naudoti projekto sutarties eilutę su laiko ir medžiagų atsiskaitymo metodu, reikės nustatyti data pagrįstą sąskaitos faktūros grafiką. Tokia pati tvarka galioja ir projektu pagrįstai sutarties eilutei.      
 
### <a name="edit-a-draft-invoice"></a>Sąskaitos faktūros juodraščio redagavimas

Sukūrus juodraštinę projekto sąskaitą faktūrą, visos pardavimo operacijos, už kurias neišrašyta sąskaita, sukurtos, kai laiko ir išlaidų įrašai buvo patvirtinti, yra įtraukiamos į sąskaitą faktūrą. Galite atlikti šiuos koregavimus, kai sąskaita faktūra vis dar yra juodraščio etape:

- Naikinti arba redaguoti sąskaitos faktūros eilutės išsamią informaciją.
- Redaguoti ir koreguoti kiekį ir atsiskaitymo tipą.
- Į sąskaitą faktūrą tiesiogiai įtraukti laiko, išlaidų ir mokesčių operacijas. Galite naudoti šią funkciją, jei sąskaitos faktūros eilutė susieta su sutarties eilute, kurioje leidžiama atlikti šias operacijų klases.

Pažymėkite **Patvirtinti**, kad patvirtintumėte sąskaitą faktūrą. Patvirtinimo veiksmas yra vienpusis veiksmas. Pasirinkus **Patvirtinti**, sąskaita faktūra sistemoje tampa tik skaitoma ir sukuriami faktiniai pardavimai, už kuriuos išrašyta sąskaita, iš kiekvienos sąskaitos faktūros eilutės išsamios informacijos kiekvienai sąskaitos faktūros eilutei. Jei sąskaitos faktūros eilutėje nurodomas faktinis pardavimas, už kurį neišrašyta sąskaita, sistema taip pat atšaukia faktinį pardavimą, už kurį neišrašyta sąskaita. (Bet kuri sąskaitos faktūros eilutės išsami informacija, sukurta naudojant laiko ar išlaidų įrašą, nurodo faktinį pardavimą, už kurį neišrašyta sąskaita). Didžiosios knygos integravimo sistemos gali naudoti šį atšaukimą, kad atšauktų projekto nebaigtą gamybą (NG) apskaitos tikslais.

### <a name="correct-a-confirmed-invoice"></a>Patvirtintos sąskaitos faktūros taisymas

Patvirtintas sąskaitas faktūras galima redaguoti (taisyti). Pataisius patvirtintą sąskaitą faktūrą, sukuriama nauja juodraštinė koreguojamoji sąskaita faktūra. Kadangi daroma prielaida, kad norite atšaukti visas operacijas ir kiekius iš pradinės sąskaitos faktūros, į šią koreguojamąją sąskaitą faktūrą įeina visos operacijos iš pradinės sąskaitos faktūros, o visi joje esantys kiekiai yra 0 (nulis).

Jei tam tikrų operacijų taisyti nereikia, galite jas pašalinti iš juodraštinės koreguojamosios sąskaitos faktūros. Jei norite atšaukti arba grąžinti tik dalinį kiekį, galite redaguoti eilutės informacijos lauką **Kiekis**. Jei atidarote sąskaitos faktūros eilutės išsamią informaciją, galite peržiūrėti pradines sąskaitos faktūros kiekį. Tada galite redaguoti dabartinės sąskaitos faktūros kiekį, kad jis būtų mažesnis arba didesnis nei pradinės sąskaitos faktūros kiekis.

Patvirtinus koreguojamąją sąskaitą faktūrą, pradinis faktinis pardavimas, už kurį išrašyta sąskaita, yra atšaukiamas ir sukuriamas naujas faktinis pardavimas, už kurį išrašyta sąskaita. Jei kiekis sumažintas, dėl skirtumo taip pat bus sukuriamas naujas faktinis pardavimas, už kurį neišrašyta sąskaita. Pavyzdžiui, jei pradinio pardavimo, už kurį išrašyta sąskaita, kiekis yra aštuonios valandos, o koreguojamosios sąskaitos faktūros eilutės išsamioje informacijoje nurodomas sumažintas šešių valandų kiekis, pradinio pardavimo, už kurį išrašyta sąskaita faktūra, eilutė atšaukiama ir sukuriami du nauji faktiniai duomenys:

- Šešių valandų faktinis pardavimas, už kurį išrašyta sąskaita.
- Likusių dviejų valandų faktinis pardavimas, už kurį neišrašyta sąskaita. Šiai operacijai vėliau galima išrašyti sąskaitą arba pažymėti ją kaip neapmokestinamąją, atsižvelgiant į derybas su klientu.
