---
title: Versijos naujinimas iš "Project Service Automation" į "Project Operations"
description: Šiame straipsnyje apžvelgiamas atnaujinimo iš Microsoft Dynamics 365 Project Service Automation į Dynamics 365 Project Operations.
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
ms.openlocfilehash: 43ea29aeafb62f3ecd69b316f2c0a5b791707da5
ms.sourcegitcommit: bc21fbe8547534d2644269f873eb05d509840f23
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446046"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Versijos naujinimas iš "Project Service Automation" į "Project Operations"

Džiaugiamės galėdami pranešti apie pirmąjį iš trijų atnaujinimo etapų nuo Microsoft Dynamics 365 Project Service Automation iki Dynamics 365 Project Operations. Šiame straipsnyje pateikiama apžvalga klientams, kurie leidžiasi į šią įdomią kelionę. Būsimi straipsniai apims kūrėjų svarstymus ir išsamią informaciją apie funkcijų patobulinimus. Jie ne tik pateiks patarimų, padėsiančių pasiruošti naujinti versiją į "Project Operations", bet ir paaiškins, ko galite tikėtis atnaujinę versiją.

Atnaujinimo pristatymo programa bus padalinta į tris etapus.

| Atnaujinimo pristatymas | 1 etapas (2022 m. sausio mėn.) | 2 etapas (2022 m. lapkričio mėn.) | 3 etapas (2023 m. balandžio banga)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nėra priklausomybės nuo projektų darbo paskirstymo struktūros (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS šiuo metu palaikomose "Project Operations" ribose | | :heavy_check_mark: | :heavy_check_mark: |
| WBS viršija šiuo metu palaikomus "Project Operations" apribojimus, įskaitant "Project" kompiuterio kliento palaikymą | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Atnaujinimo proceso funkcijos 

Atnaujindami versiją, į svetainės žemėlapį įtraukėme atnaujinimo žurnalus, kad administratoriai galėtų lengviau diagnozuoti gedimus. Be naujos sąsajos, bus įtrauktos naujos tikrinimo taisyklės, kad būtų užtikrintas duomenų vientisumas po atnaujinimo. Toliau nurodyti tikrinimai bus įtraukti į versijos naujinimo procesą.

| Tikrinimą | 1 etapas (2022 m. sausio mėn.) | 2 etapas (2022 m. lapkričio mėn.) | 3 fazė  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS bus patikrintas pagal įprastus duomenų vientisumo pažeidimus (pvz., išteklių priskyrimus, susietus su ta pačia pirmine užduotimi, bet turinčius skirtingus pirminius projektus). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bus patvirtintas pagal [žinomas "Project for the Web" ribas](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bus patvirtintas pagal žinomas "Project" darbalaukio kliento ribas. | |  | :heavy_check_mark: |
| Rezervuojami ištekliai ir projektų kalendoriai bus vertinami pagal įprastas nesuderinamas kalendoriaus taisyklių išimtis. | | :heavy_check_mark: | :heavy_check_mark: |

2 etape klientai, kurie atnaujina į "Project Operations", turės savo esamus projektus atnaujinti į tik skaityti skirtas projektų planavimo funkcijas. Šioje tik skaitomoje aplinkoje visas WBS bus matomas stebėjimo tinklelyje. Norėdami redaguoti WBS, projektų vadovai pagrindiniame **puslapyje Projektai** gali pasirinkti **Konvertuoti**. Tada foninis procesas atnaujins projektą, kad jis palaikytų naujas projekto planavimo funkcijas iš "Project for the Web". Šis etapas tinka klientams, turintiems projektų, kurie atitinka [žinomas "Project for the Web"](/project-for-the-web/project-for-the-web-limits-and-boundaries) ribas.

3 etape bus pridėtas "Project" darbalaukio kliento palaikymas klientų, norinčių toliau redaguoti savo projektus iš tos programos, naudai. Tačiau jei esami projektai konvertuojami į naują žiniatinklio naudojimo projektą, prieiga prie papildinio bus išjungta kiekvienam konvertuotam projektui.

## <a name="prerequisites"></a>Būtinosios sąlygos

Kad atitiktų 1 etapo versijos naujinimą, klientas turi atitikti šiuos kriterijus:

- Tikslinėje aplinkoje neturi būti jokių msdyn_projecttask objekto **įrašų**.
- Galiojančios "Project Operations" licencijos turi būti priskirtos visiems aktyviems kliento vartotojams. 
- Klientas turi patvirtinti versijos naujinimo procesą bent vienoje negamybinėje aplinkoje, kurioje yra tipinis duomenų rinkinys, sulygiuotas su gamybos duomenimis.
- Tikslinė aplinka turi būti atnaujinta į "Project Service Automation Update Release" 41 (3.10.62.162) arba naujesnę versiją.

2 ir 3 etapų būtinosios sąlygos bus atnaujintos artėjant bendrosioms prieinamumo datoms.

## <a name="licensing"></a>Licencijavimas

Jei turite aktyvias "Project Service Automation" licencijas, galite įdiegti ir naudoti "Project Operations", kuri apima visas "Project Service Automation" galimybes ir kt. Tokiu būdu galite išbandyti "Project Operations" galimybes ir toliau naudoti "Project Service Automation" gamyboje. Pasibaigus "Project Service Automation" licencijų galiojimo laikui, turėsite pereiti prie "Project Operations". Planuodami šį perėjimą turite atsižvelgti į tai, kad "Project Operations" licencijoje nėra "Project Service Automation" licencijos.

## <a name="testing-and-refactoring-customizations"></a>Tinkinimų testavimas ir pertvarkymas

Pirmiausia importuokite visus tinkinimus į švarią projekto operacijų (Lite) aplinką, kad patvirtintumėte, jog importavimas sėkmingas ir kad verslo operacijos veikia taip, kaip tikėtasi.

Štai keletas dalykų, į kuriuos reikia atkreipti dėmesį:

- Importuoti gali nepavykti dėl trūkstamų priklausomybių. Kitaip tariant, tinkinimai nurodo laukus arba kitus komponentus, kurie buvo pašalinti iš "Project Operations". Tokiu atveju pašalinkite šias priklausomybes iš vystymosi aplinkos.
- Jei jūsų nevaldomuose ir valdomuose sprendimuose yra komponentų, kurie nėra tinkinti, pašalinkite tuos komponentus iš sprendimo. Pavyzdžiui, kai tinkinate objektą **Projektas**, į sprendimą įtraukite tik objekto antraštę. Nepridėkite visų laukų. Jei anksčiau pridėjote visus subkomponentus, gali tekti rankiniu būdu sukurti naują sprendimą ir pridėti prie jo atitinkamus komponentus.
- Formos ir rodiniai gali būti rodomi ne taip, kaip tikėtasi. Tam tikromis aplinkybėmis, jei tinkinote kurią nors iš paruoštų naudoti formų arba rodinių, tinkinimai gali neleisti įsigalioti naujiems "Project Operations" naujinimams. Norėdami nustatyti šias problemas, rekomenduojame atlikti vieną šalia kito pateiktą švaraus "Project Operations" diegimo ir "Project Operations" diegimo, apimančio tinkinimus, peržiūrą. Palyginkite dažniausiai įmonėje naudojamas formas, kad patvirtintumėte, jog formos versija vis dar yra prasminga ir kad švarioje formos versijoje jos kažko netrūksta. Atlikite to paties tipo vieną šalia kito atliekamą visų tinkintų rodinių peržiūrą.
- Verslo logika vykdymo metu gali nepavykti. Kadangi nuorodos į papildinių laukus importavimo metu nėra tikrinamos, verslo logika gali nepavykti dėl nuorodų į laukus, kurių nebėra, ir galite gauti klaidos pranešimą, panašų į šį pavyzdį: "Projekto" objekte nėra atributo su Name = 'msdyn_plannedhours' ir NameMapping = 'Logical'." Tokiu atveju modifikuokite tinkinimus, kad jie naudotų naujus laukus. Jei papildinio logikoje naudojate automatiškai sugeneruotas tarpinio serverio klases ir stipriojo tipo nuorodas, apsvarstykite galimybę atkurti tuos tarpinius serverius iš švaraus diegimo. Tokiu būdu galite lengvai nustatyti visas vietas, kuriose jūsų papildiniai priklauso nuo nebenaudojamų laukų.

Atnaujinę tinkinimus, kad jie švariai importuotų "Project Operations", pereikite prie tolesnių veiksmų.

## <a name="end-to-end-testing-in-development-environments"></a>Testavimas nuo galo iki galo kūrimo aplinkoje

### <a name="initiate-upgrade"></a>Inicijuokite versijos naujinimą 

1. Power Platform Administravimo centre raskite ir pasirinkite savo aplinką. Tada programose raskite ir pasirinkite **Dynamics 365 Project Operations**.
2. Pasirinkite **Diegti**, kad pradėtumėte naujinimą. Administravimo Power Platform centras pateiks šį diegimą kaip naują diegimą. Tačiau ankstesnės "Project Service Automation" versijos buvimas bus aptiktas ir esamas diegimas bus atnaujintas.

    Baigus naujinti versiją, aplinka turėtų parodyti, kad įdiegtos "Project Operations" ir kad "Project Service Automation" neįdiegta.

    > [!NOTE]
    > Atsižvelgiant į duomenų kiekį aplinkoje, versijos naujinimas gali užtrukti kelias valandas. Pagrindinė komanda, valdanti naujinimą, turėtų atitinkamai planuoti ir paleisti naujinimą ne darbo valandomis. Kai kuriais atvejais, jei duomenų kiekis yra didelis, atnaujinimas turėtų būti vykdomas savaitgalį. Sprendimas dėl planavimo turėtų būti grindžiamas bandymų rezultatais žemesnėse aplinkose.

3. Jei reikia, atnaujinkite pasirinktinius sprendimus. Šiuo metu įdiekite visus tinkinimų pakeitimus [šio straipsnio skyriuje Testavimas ir pertvarkymas tinkinimai](#testing-and-refactoring-customizations).
4. Eikite į **"Settings Solutions"** \> **ir** pasirinkite, kad pašalintumėte **"Project Operations" nebenaudojamų komponentų** sprendimą.

    Šis sprendimas yra laikinas sprendimas, kuriame yra esamas duomenų modelis ir komponentai, esantys naujinant versiją. Pašalindami šį sprendimą, pašalinate visus nebenaudojamus laukus ir komponentus. Tokiu būdu padedate supaprastinti sąsają ir palengvinti integraciją bei išplėtimą.
    
### <a name="validate-common-scenarios"></a>Dažnai pasitaikančių scenarijų tikrinimas

Kai patvirtinate konkrečius tinkinimus, rekomenduojame peržiūrėti ir verslo procesus, kurie palaikomi visose programose. Šie verslo procesai apima, bet tuo neapsiriboja, pardavimo objektų, pvz., pasiūlymų ir sutarčių, kūrimą ir projektų, apimančių PBS ir faktinių duomenų patvirtinimą, kūrimą.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Pagrindiniai "Project Service Automation" ir "Project Operations" pakeitimai

Šiame skyriuje pateikiama pagrindinių pakeitimų, kurių galite tikėtis tarp "Project Service Automation" ir "Project Operations", suvestinė.

### <a name="project-planning"></a>Projekto planavimas

Projekto planavimo galimybės "Project Operations" nebepasiremia kombinuota kliento logika ir serverio logika. Vietoj to, "Project Operations" naudoja "Project for the Web" kaip planavimo variklį. Šis planavimo galimybių pakeitimas įgalina keletą naujų funkcijų, pvz., lentos ir Ganto rodinius, ištekliais pagrįstą planavimą, [užduočių kontrolinio sąrašo elementus](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) ir projekto planavimo režimus. Naujas planavimo galimybes taip pat palaiko gausus naujų [programų programavimo sąsajų (API)](../project-management/schedule-api-preview.md) rinkinys. Šios API skirtos užtikrinti, kad jokia programinė operacija, skirta WBS objektui kurti, naujinti ar naikinti, nesugadintų apskaičiuotųjų grafiko laukų.

## <a name="billing-and-pricing"></a>Sąskaitų siuntimas ir kainodara

Tęsiant investicijas į "Project Operations", yra keletas naujų atsiskaitymo ir kainodaros galimybių. Štai keli pavyzdžiai:

- [Medžiagos naudojimo projektams ir projekto užduotims įrašyti įrašymas](../material/material-usage-log.md)
- [Subrangos valdymas](../pro/subcontracting/managing-subcontracts-overview.md)
- [Išankstinės arba išankstiniais apmokėjimais pagrįstos sutartys](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sutarties, kuri neviršija statuso, ir patvirtinimai](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Užduotimis pagrįstas atsiskaitymas

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Kuriuos diegimo tipus šiuo metu galima naujinti?

| Šaltinis                                                 | Vertimas                                                    | Būsena                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | "Project Operations Lite" diegimas                        | Palaikomas               |
| Dynamics 365 Finance Projektų valdymas ir apskaita | "Project Operations Lite" diegimas                        | Šiuo metu nepalaikoma |
| Finansų projektų valdymas ir apskaita              | „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams     | Šiuo metu nepalaikoma |
| "Project Service Automation 3.x"                         | „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams     | Šiuo metu nepalaikoma |
| Projektas žiniatinkliui (speciali aplinka)            | "Project Operations Lite" diegimas                        | Šiuo metu nepalaikoma |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kaip įdiegti "Project Operations" prieš pradedant naudoti naujinimo įrankius?

Yra dvi "Project Operations" diegimo parinktys prieš pradedant naudoti naujinimo įrankius:

- Sukurkite naują aplinką.
- Įdiekite "Project Operations" atskirai bet kurioje pardavimo organizacijoje, kurioje nėra "Project Service Automation".

> [!NOTE]
> Jei "Project Service Automation" įdiegta organizacijoje, bet ji nebuvo naudojama, ją galima pašalinti. Visiškai pašalinus "Project Service Automation", "Project Operations" galima įdiegti toje pačioje organizacijoje.
