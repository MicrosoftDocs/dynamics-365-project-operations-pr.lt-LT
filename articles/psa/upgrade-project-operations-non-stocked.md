---
title: Atnaujinimas iš "Project Service Automation" į "Project Operations"
description: Šiame straipsnyje pateikiama proceso, kurį reikia atnaujinti iš Microsoft Dynamics 365 Project Service Automation į Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/13/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 30eb02240de6617d4c550ce59db2a454eee36f5b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912986"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Atnaujinimas iš "Project Service Automation" į "Project Operations"

Džiaugiamės galėdami pranešti apie pirmąjį iš trijų etapų, kuriuos reikia atnaujinti nuo Microsoft Dynamics 365 Project Service Automation iki Dynamics 365 Project Operations. Šiame straipsnyje pateikiama apžvalga klientams, kurie pradeda šią įdomią kelionę. Būsimuose straipsniuose bus įtraukti kūrėjų svarstymai ir išsami informacija apie funkcijų patobulinimus. Jie ne tik pateiks gaires, kurios padės jums pasiruošti "Project Operations" atnaujinimui, bet ir paaiškins, ko galite tikėtis atnaujinę.

Atnaujinimo pristatymo programa bus suskirstyta į tris etapus.

| Atnaujinti pristatymą | 1 etapas (2022 m. sausio mėn.) | 2 etapas (2022 m. Balandžio banga) | 3 etapas  |
|------------------|------------------------|---------------------------|---------------------------|
| Nėra priklausomybės nuo projektų darbo paskirstymo struktūros (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS neperžengia šiuo metu palaikomų projekto operacijų ribų | | :heavy_check_mark: | :heavy_check_mark: |
| WBS nepatenka į šiuo metu palaikomas "Project Operations" ribas, įskaitant "Project" darbalaukio kliento palaikymą | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Naujinimo proceso funkcijos 

Vykdydami atnaujinimo procesą, į svetainės struktūrą įtraukėme atnaujinimo žurnalus, kad administratoriai galėtų lengviau diagnozuoti gedimus. Be naujos sąsajos, bus pridėtos naujos patvirtinimo taisyklės, kad būtų užtikrintas duomenų vientisumas po atnaujinimo. Šie patvirtinimai bus įtraukti į atnaujinimo procesą.

| Tikrinimą | 1 etapas (2022 m. sausio mėn.) | 2 etapas (2022 m. Balandžio banga) | 3 etapas  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS bus patikrintas dėl bendrų duomenų vientisumo pažeidimų (pvz., išteklių priskyrimų, susietų su ta pačia pirmine užduotimi, bet turinčių skirtingus pirminius projektus). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bus patvirtintas pagal [žinomas žiniatinklio projekto ribas](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bus patvirtintas pagal žinomas "Project" darbalaukio kliento ribas. | |  | :heavy_check_mark: |
| Rezervuoti ištekliai ir projektų kalendoriai bus vertinami pagal bendras nesuderinamas kalendoriaus taisyklių išimtis. | | :heavy_check_mark: | :heavy_check_mark: |

2 etape klientai, kurie atnaujinami į "Project Operations", savo esamus projektus atnaujins į tik skaitomą projektų planavimo patirtį. Šioje tik skaityti skirtoje funkcijoje visas WBS bus matomas stebėjimo tinklelyje. Norėdami redaguoti WBS, projektų vadovai pagrindiniame **puslapyje Projektai** gali pasirinkti **Konvertuoti**. Tada foninis procesas atnaujins projektą, kad jis palaikytų naują projekto planavimo patirtį iš "Project for the Web". Šis etapas tinka klientams, turintiems projektų, atitinkančių [žinomas "Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries)" ribas.

3 etape bus pridėtas "Project" darbalaukio kliento palaikymas klientų, norinčių toliau redaguoti savo projektus iš tos programos, naudai. Tačiau, jei esami projektai konvertuojami į naują žiniatinklio patirties projektą, prieiga prie priedo bus išjungta kiekvienam konvertuotam projektui.

## <a name="prerequisites"></a>Būtinosios sąlygos

Kad galėtų gauti 1 etapo atnaujinimą, klientas turi atitikti šiuos kriterijus:

- Paskirties aplinkoje neturi būti jokių msdyn_projecttask **objekto** įrašų.
- Galiojančios "Project Operations" licencijos turi būti priskirtos visiems aktyviems kliento vartotojams. 
- Klientas turi patvirtinti atnaujinimo procesą bent vienoje negamybinėje aplinkoje, kurioje yra reprezentatyvus duomenų rinkinys, suderintas su gamybos duomenimis.
- Paskirties aplinka turi būti atnaujinta į "Project Service Automation Update Release" 41 (3.10.62.162) arba naujesnę versiją.

Artėjant bendroms prieinamumo datoms, 2 ir 3 etapų prielaidos bus atnaujintos.

## <a name="licensing"></a>Licencijavimas

Jei turite aktyvias "Project Service Automation" licencijas, galite įdiegti ir naudoti "Project Operations", kuri apima visas "Project Service Automation" galimybes ir dar daugiau. Tokiu būdu galite išbandyti "Project Operations" galimybes, kol gamyboje toliau naudojate "Project Service Automation". Pasibaigus "Project Service Automation" licencijų galiojimui, turėsite pereiti prie "Project Operations". Planuodami šį perėjimą turite atsižvelgti į tai, kad "Project Operations" licencijoje nėra "Project Service Automation" licencijos.

## <a name="testing-and-refactoring-customizations"></a>Tinkinimų testavimas ir pertvarkymas

Pirmiausia importuokite visus tinkinimus į švarią "Project Operations" (lite) aplinką, kad patvirtintumėte, jog importavimas yra sėkmingas ir kad verslo operacijos veikia taip, kaip tikėtasi.

Štai keletas dalykų, į kuriuos reikia atkreipti dėmesį:

- Importuoti gali nepavykti dėl trūkstamų priklausomybių. Kitaip tariant, tinkinimų nuorodų laukai ar kiti komponentai, kurie buvo pašalinti "Project Operations". Tokiu atveju pašalinkite šias priklausomybes iš vystymosi aplinkos.
- Jei nevaldomuosiuose ir valdomuose sprendimuose yra komponentų, kurie nėra tinkinti, pašalinkite šiuos komponentus iš sprendimo. Pavyzdžiui, kai tinkinate objektą **Projektas**, į savo sprendimą įtraukite tik objekto antraštę. Neįtraukite visų laukų. Jei anksčiau įtraukėte visus subkomponentus, gali tekti neautomatiniu būdu sukurti naują sprendimą ir į jį įtraukti atitinkamus komponentus.
- Formos ir rodiniai gali pasirodyti ne taip, kaip tikėtasi. Tam tikromis aplinkybėmis, jei tinkinote bet kurią iš "out-of-box" formų ar rodinių, tinkinimai gali neleisti įsigalioti naujiems "Project Operations" naujinimams. Norėdami nustatyti šias problemas, rekomenduojame atlikti švaraus "Project Operations" diegimo ir "Project Operations" diegimo, apimančio tinkinimus, peržiūrą. Palyginkite dažniausiai naudojamas formas savo įmonėje, kad patvirtintumėte, jog jūsų formos versija vis dar yra prasminga ir nieko netrūksta iš švarios formos versijos. Atlikite to paties tipo visų tinkintų rodinių peržiūrą.
- Verslo logika gali nepavykti vykdymo metu. Kadangi nuorodos į papildinių laukus importavimo metu nėra tikrinamos, verslo logika gali nepavykti dėl nuorodų į laukus, kurių nebėra, ir galite gauti klaidos pranešimą, panašų į šį pavyzdį: "Projekto" objekte nėra atributo, kurio pavadinimas = "msdyn_plannedhours" ir "NameMapping= "Loginis". Tokiu atveju modifikuokite tinkinimus, kad jie naudotų naujus laukus. Jei priedo logikoje naudojate automatiškai sugeneruotas tarpinio serverio klases ir stiprias tipo nuorodas, apsvarstykite galimybę regeneruoti šiuos tarpinius serverius iš švaraus diegimo. Tokiu būdu galite lengvai nustatyti visas vietas, kuriose jūsų papildiniai priklauso nuo nebenaudojamų laukų.

Atnaujinę tinkinimus, kad būtų galima švariai importuoti "Project Operations", pereikite prie kitų veiksmų.

## <a name="end-to-end-testing-in-development-environments"></a>"End-to-end" testavimas vystymosi aplinkoje

### <a name="initiate-upgrade"></a>Inicijuoti naujinimą 

1. Power Platform Administravimo centre raskite ir pasirinkite savo aplinką. Tada programose raskite ir pasirinkite **Dynamics 365 Project Operations**.
2. Norėdami pradėti naujinimą, pasirinkite **Diegti**. Administravimo Power Platform centras pristatys šį diegimą kaip naują diegimą. Tačiau bus aptikta ankstesnė "Project Service Automation" versija, o esamas diegimas bus atnaujintas.

    Baigus naujinti, aplinka turi rodyti, kad įdiegtos projekto operacijos ir kad "Project Service Automation" neįdiegta.

    > [!NOTE]
    > Atsižvelgiant į duomenų kiekį aplinkoje, atnaujinimas gali užtrukti kelias valandas. Pagrindinė komanda, valdanti atnaujinimą, turėtų atitinkamai planuoti ir vykdyti atnaujinimą ne darbo valandomis. Kai kuriais atvejais, jei duomenų apimtis yra didelė, atnaujinimas turėtų būti vykdomas savaitgalį. Sprendimas dėl tvarkaraščio turėtų būti grindžiamas bandymų rezultatais žemesnėje aplinkoje.

3. Jei reikia, atnaujinkite pasirinktinius sprendimus. Šiuo metu įdiekite visus tinkinimų pakeitimus [šio straipsnio skyriuje Tinkinimų](#testing-and-refactoring-customizations) testavimas ir pertvarkymas.
4. Eikite į **Parametrų** \> **sprendimai** ir pasirinkite, kad pašalintumėte **"Project Operations" nebenaudojamų komponentų** sprendimą.

    Šis sprendimas yra laikinas sprendimas, kuriame saugomas esamas duomenų modelis ir komponentai, esantys atnaujinimo metu. Pašalinę šį sprendimą, pašalinate visus nebenaudojamus laukus ir komponentus. Tokiu būdu padedate supaprastinti sąsają ir palengvinti integraciją bei išplėtimą.
    
### <a name="validate-common-scenarios"></a>Tikrinti bendruosius scenarijus

Kai patvirtinate konkrečius tinkinimus, rekomenduojame peržiūrėti ir verslo procesus, kurie palaikomi visose programose. Šie verslo procesai apima, bet neapsiriboja, pardavimo subjektų, pvz., pasiūlymų ir sutarčių, kūrimą ir projektų, apimančių PBS, kūrimą ir faktinių duomenų patvirtinimą.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Pagrindiniai pokyčiai tarp projekto paslaugų automatizavimo ir projekto operacijų

Šiame skyriuje pateikiama pagrindinių pakeitimų, kurių galite tikėtis tarp "Project Service Automation" ir "Project Operations", santrauka.

### <a name="project-planning"></a>Projekto planavimas

Projekto planavimo galimybės programoje "Project Operations" nebepriklauso nuo bendros kliento logikos ir serverio logikos. Vietoj to, "Project Operations" naudoja "Project" žiniatinklyje kaip planavimo variklį. Šis planavimo galimybių pakeitimas įgalina kelias naujas funkcijas, pvz., lentos ir Ganto rodinius, ištekliais pagrįstą planavimą, [užduočių kontrolinio sąrašo elementus](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) ir projektų planavimo režimus. Naujas planavimo galimybes taip pat palaiko turtingas naujų [programų programavimo sąsajų (API)](../project-management/schedule-api-preview.md) rinkinys. Šios API skirtos padėti užtikrinti, kad jokia programinė operacija, skirta WBS objektui kurti, naujinti ar naikinti, nesugadintų apskaičiuotųjų grafiko laukų.

## <a name="billing-and-pricing"></a>Sąskaitų siuntimas ir kainodara

Tęsiant investicijas į projektų operacijas, atsiskaitymo ir kainodaros srityje yra keletas naujų galimybių. Štai keli pavyzdžiai:

- [Medžiagos naudojimo registravimas projektuose ir projekto užduotyse](../material/material-usage-log.md)
- [Subrangos sutarčių valdymas](../pro/subcontracting/managing-subcontracts-overview.md)
- [Išankstinės arba išankstiniais apmokėjimais pagrįstos sutartys](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sutarties būsena ir patvirtinimai, kurių būsena neviršijama](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Užduotimis pagrįstas atsiskaitymas

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Kurie diegimo tipai šiuo metu palaikomi naujinant?

| Šaltinis                                                 | Vertimas                                                    | Būsena                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Projekto operacijos Lite diegimas                        | Palaikomas               |
| Dynamics 365 Finance projektų valdymas ir apskaita | Projekto operacijos Lite diegimas                        | Šiuo metu nepalaikomas |
| Finansų projektų valdymas ir apskaita              | „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams     | Šiuo metu nepalaikomas |
| Projekto paslaugų automatizavimas 3.x                         | „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams     | Šiuo metu nepalaikomas |
| Interneto projektas (speciali aplinka)            | Projekto operacijos Lite diegimas                        | Šiuo metu nepalaikomas |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kaip įdiegti "Project Operations" prieš pasiekiant naujinimo įrankį?

Yra dvi "Project Operations" diegimo parinktys prieš pasiekiant naujinimo įrankį:

- Sukurti naują aplinką.
- Diegti projekto operacijas atskirai bet kurioje pardavimo organizacijoje, kurioje nėra "Project Service Automation".

> [!NOTE]
> Jei organizacijoje įdiegtas "Project Service Automation", bet jis nebuvo naudojamas, jį galima pašalinti. Visiškai pašalinus "Project Service Automation", "Project Operations" galima įdiegti toje pačioje organizacijoje.
