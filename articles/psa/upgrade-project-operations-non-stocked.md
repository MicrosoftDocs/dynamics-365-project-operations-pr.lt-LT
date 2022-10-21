---
title: Naujinimas iš „Project Service Automation“ į „Project Operations“
description: Šiame straipsnyje apžvelgiamas versijos naujinimo iš Microsoft Dynamics 365 Project Service Automation į Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
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
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9686986"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Naujinimas iš „Project Service Automation“ į „Project Operations“

Džiaugiamės galėdami pranešti apie antrąjį iš trijų atnaujinimo iš Microsoft Dynamics 365 Project Service Automation "Microsoft" etapų Dynamics 365 Project Operations. Šiame straipsnyje pateikiama apžvalga klientams, kurie leidžiasi į šią įdomią kelionę. 

Atnaujinimo pristatymo programa bus padalinta į tris etapus.

| Versijos naujinimo pristatymas | 1 etapas (2022 m. sausio mėn.) | 2 etapas (2022 m. lapkričio mėn.) | 3 etapas (2023 m. balandžio banga)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nėra priklausomybės nuo projektų darbo paskirstymo struktūros (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| PBS pagal šiuo metu palaikomas "Project Operations" ribas | | :heavy_check_mark: | :heavy_check_mark: |
| WBS už šiuo metu palaikomų "Project Operations" ribų, įskaitant "Project" darbalaukio kliento palaikymą | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Atnaujinimo proceso funkcijos 

Vykdydami versijos naujinimo procesą, į svetainės schemą įtraukėme versijos naujinimo žurnalus, kad administratoriai galėtų lengviau diagnozuoti gedimus. Be naujos sąsajos, bus pridėtos naujos patvirtinimo taisyklės, kad būtų užtikrintas duomenų vientisumas po atnaujinimo. Toliau nurodyti patvirtinimai bus įtraukti į versijos naujinimo procesą.

| Tikrinimą | 1 etapas (2022 m. sausio mėn.) | 2 etapas (2022 m. lapkričio mėn.) | 3 fazė  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS bus tikrinama pagal įprastus duomenų vientisumo pažeidimus (pvz., išteklių priskyrimus, susietus su ta pačia pirmine užduotimi, bet turinčius skirtingus pirminius projektus). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bus patvirtintas pagal [žinomus "Project for the Web" apribojimus](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bus patikrintas pagal žinomus "Project" darbalaukio kliento apribojimus. | |  | :heavy_check_mark: |
| Rezervuojami ištekliai ir projektų kalendoriai bus vertinami pagal bendrąsias nesuderinamas kalendoriaus taisyklių išimtis. | | :heavy_check_mark: | :heavy_check_mark: |

2 etape klientai, kurie atnaujina į "Project Operations", atnaujins savo esamus projektus į tik skaitymo funkciją, skirtą projektų planavimui. Šioje tik skaitymo aplinkoje visas WBS bus matomas stebėjimo tinklelyje. Norėdami redaguoti WBS, projektų vadovai pagrindiniame projekto puslapyje gali pasirinkti [**Konvertuoti**](/PSA-Upgrade-Project-Conversion.md). Tada foninis procesas atnaujina projektą, kad jis palaikytų naują projekto planavimo patirtį iš "Project for the Web". Šis etapas tinka klientams, turintiems projektų, kurie atitinka [žinomas "Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries)" ribas.

3 etape bus pridėtas "Project" darbalaukio kliento palaikymas, kad būtų naudinga klientams, norintiems toliau redaguoti savo projektus iš tos programos. Tačiau jei esami projektai konvertuojami į naują žiniatinklio projektą, prieiga prie papildinio bus išjungta kiekvienam konvertuotam projektui.

## <a name="prerequisites"></a>Būtinosios sąlygos

Kad galėtumėte gauti 1 etapo versijos naujinimą, turite atitikti šiuos kriterijus:

- Paskirties aplinkoje neturi būti jokių įrašų **msdyn_projecttask** objekte.
- Galiojančios "Project Operations" licencijos turi būti priskirtos visiems aktyviems vartotojams. 
- Turite patikrinti versijos naujinimo procesą bent vienoje ne gamybos aplinkoje, kurioje yra reprezentatyvus duomenų rinkinys, suderintas su jūsų gamybos aplinka.
- Paskirties aplinka turi būti atnaujinta į "Project Service Automation Update Release 37" (V3.10.58.120) arba naujesnę versiją.

Kad galėtumėte gauti 2 etapo versijos naujinimą, turite atitikti šiuos kriterijus:

- Galiojančios "Project Operations" licencijos turi būti priskirtos visiems aktyviems vartotojams. 
- Turite patikrinti versijos naujinimo procesą bent vienoje ne gamybos aplinkoje, kurioje yra reprezentatyvus duomenų rinkinys, suderintas su jūsų gamybos aplinka.
- Paskirties aplinka turi būti atnaujinta į "Project Service Automation Update Release 37" (V3.10.58.120) arba naujesnę versiją.
- Aplinkos, kuriose yra užduočių (msdyn_projecttask), palaikomos tik tuo atveju, jei bendras vieno projekto užduočių skaičius yra 500 arba mažiau.

3 etapo būtinosios sąlygos bus atnaujintos artėjant bendrajai pasiekiamumo datai.

## <a name="licensing"></a>Licencijavimas

Jei turite aktyvias "Project Service Automation" licencijas, galite įdiegti ir naudoti "Project Operations", kuri apima visas "Project Service Automation" galimybes ir kt. Tada galite išbandyti "Project Operations" galimybes atskiroje aplinkoje, kol toliau naudojate "Project Service Automation" gamyboje. Pasibaigus "Project Service Automation" licencijų galiojimo laikui, turėsite pereiti prie "Project Operations". Planuodami šį perėjimą turite atsižvelgti į tai, kad "Project Operations" licencijoje nėra "Project Service Automation" licencijos.

## <a name="testing-and-refactoring-customizations"></a>Tinkinimų testavimas ir pertvarkymas

Pirmiausia importuokite visus tinkinimus į švarią "Project Operations" ("Lite") aplinką, kad patvirtintumėte, jog importavimas yra sėkmingas ir kad verslo operacijos veikia taip, kaip tikėtasi.

Štai keletas dalykų, į kuriuos reikia atkreipti dėmesį:

- Importuoti gali nepavykti, nes trūksta priklausomybių. Kitaip tariant, tinkinimų nuorodų laukai arba kiti komponentai, kurie buvo pašalinti iš "Project Operations". Tokiu atveju pašalinkite šias priklausomybes iš kūrimo aplinkos.
- Jei jūsų nevaldomuosiuose ir valdomuosiuose sprendimuose yra komponentų, kurie nėra tinkinami, pašalinkite tuos komponentus iš sprendimo. Pavyzdžiui, kai tinkinate **projekto** objektą, į sprendimą įtraukite tik objekto antraštę. Neįtraukite visų laukų. Jei anksčiau įtraukėte visus subkomponentus, gali tekti rankiniu būdu sukurti naują sprendimą ir į jį įtraukti atitinkamų komponentų.
- Formos ir rodiniai gali būti rodomi ne taip, kaip tikėtasi. Tam tikromis aplinkybėmis, jei tinkinote bet kurią iš anksto parengtų naudoti formų ar rodinių, tinkinimai gali neleisti įsigalioti naujiems "Project Operations" naujinimams. Jei norite nustatyti šias problemas, rekomenduojame kartu peržiūrėti švarų "Project Operations" diegimą ir "Project Operations" diegimą, kuris apima jūsų tinkinimus. Palyginkite dažniausiai įmonėje naudojamas formas, kad patvirtintumėte, jog jūsų formos versija vis dar yra prasminga ir jos netrūksta švarioje formos versijoje. Atlikite to paties tipo gretutines visų tinkintų rodinių peržiūras.
- Verslo logika vykdymo metu gali nepavykti. Kadangi nuorodos į papildinių laukus importavimo metu nėra tikrinamos, verslo logika gali nepavykti dėl nuorodų į nebeegzistuojančius laukus ir galite gauti klaidos pranešimą, panašų į šį pavyzdį: "'Project' objekte nėra atributo su Name = 'msdyn_plannedhours' ir NameMapping = 'Logical'." Tokiu atveju modifikuokite tinkinimus, kad jie naudotų naujus laukus. Jei papildinio logikoje naudojate automatiškai sugeneruotas tarpinio serverio klases ir stiprias tipo nuorodas, apsvarstykite galimybę atkurti tuos tarpinius serverius iš švaraus diegimo. Tokiu būdu galite lengvai nustatyti visas vietas, kuriose papildiniai priklauso nuo nebenaudojamų laukų.

Atnaujinę tinkinimus, kad būtų galima švariai importuoti "Project Operations", pereikite prie tolesnių veiksmų.

## <a name="end-to-end-testing-in-development-environments"></a>Ištisinis testavimas kūrimo aplinkose

### <a name="initiate-upgrade"></a>Versijos naujinimo inicijavimas 

1. Power Platform Administravimo centre raskite ir pasirinkite savo aplinką. Tada programose raskite ir pasirinkite **Dynamics 365 Project Operations**.
2. Pasirinkite **Įdiegti**, kad pradėtumėte naujinimą. Administravimo Power Platform centras pateiks šį diegimą kaip naują diegimą. Tačiau bus aptikta ankstesnė "Project Service Automation" versija, o esamas diegimas bus atnaujintas.

    Baigus naujinti versiją, aplinkoje turėtų būti rodoma, kad įdiegta "Project Operations" ir kad neįdiegta "Project Service Automation".

    Atsižvelgiant į duomenų kiekį aplinkoje, versijos naujinimas gali užtrukti kelias valandas. Pagrindinė komanda, valdanti naujinimą, turėtų atitinkamai planuoti ir vykdyti naujinimą ne darbo valandomis. Kai kuriais atvejais, jei duomenų kiekis yra didelis, atnaujinimas turėtų būti vykdomas savaitgalį. Sprendimas dėl planavimo turėtų būti pagrįstas bandymų rezultatais žemesnėse aplinkose.

3. Jei reikia, atnaujinkite pasirinktinius sprendimus. Šiuo metu visus atliktus tinkinimų [keitimus įdiekite šio straipsnio skyriuje Tinkinimų](#testing-and-refactoring-customizations) tikrinimas ir pertvarkymas.
4. Eikite į **Parametrų** \> **sprendimai** ir pasirinkite, kad pašalintumėte **"Project Operations" nebenaudojamų komponentų** sprendimą.

    Šis sprendimas yra laikinas sprendimas, kuriame saugomas esamas duomenų modelis ir komponentai, esantys naujinant versiją. Pašalindami šį sprendimą, pašalinate visus nebenaudojamus laukus ir komponentus. Tokiu būdu jūs padedate supaprastinti sąsają ir palengvinti integraciją bei plėtinį.
    
### <a name="upgrade-to-project-operations-lite"></a>Atnaujinimas į "Project Operations Lite"

Šie veiksmai apibūdina versijos naujinimo procesą ir susijusį klaidų registravimą:

1. **PSA versijos patikrinimas:** Norėdami įdiegti "Project Operations", turite turėti V3.10.58.120 arba naujesnę versiją.
1. **Išankstinis tikrinimas:** kai administratorius inicijuoja versijos naujinimą, sistema vykdo išankstinio tikrinimo operaciją su kiekvienu objektu, kuris yra pagrindinis projekto operacijų sprendimo elementas. Atliekant šį veiksmą patikrinama, ar visos objektų nuorodos yra galiojančios, ir užtikrinama, kad duomenys, susiję su WBS, neviršytų publikuotų "Project for the Web" ribų.
1. **Metaduomenų atnaujinimas:** po sėkmingo išankstinio patvirtinimo sistema inicijuoja schemos pakeitimus ir sukuria nebenaudojamų komponentų sprendimą. Šį nebenaudojamą sprendimą galite pašalinti atlikę visus reikiamus tinkinimų pertvarkymus. Šis veiksmas yra ilgiausia versijos naujinimo proceso dalis ir gali užtrukti iki keturių valandų.
1. **Duomenų atnaujinimas:** atlikus visus būtinus schemos pakeitimus metaduomenų atnaujinimo veiksme, jūsų duomenys perkeliami į naują schemą ir atliekami visi būtini numatytieji ir perskaičiavimai.
1. **Projekto grafiko modulio naujinimas:** sėkmingai atnaujinus duomenis, **pagrindinio puslapio skirtukas Tvarkaraštis** iš naujo **pažymimas kaip Užduotys**. Kai vartotojas pasirenka šį skirtuką po atnaujinimo, jam nurodoma pereiti į stebėjimo tinklelį, kad peržiūrėtų tik skaityti skirtą WBS versiją. Norėdami redaguoti WBS, jie turi pradėti tvarkaraščio [konvertavimo procesą](/PSA-Upgrade-Project-Conversion.md). Visi projektai, kuriuose nėra iš anksto nustatytos WBS, gali naudoti naują planavimo funkciją tiesiogiai, be konvertavimo.
 
### <a name="validate-common-scenarios"></a>Įprastų scenarijų tikrinimas

Kai tikrinate konkrečius tinkinimus, rekomenduojame taip pat peržiūrėti verslo procesus, kurie palaikomi visose programose. Šie verslo procesai apima (bet tuo neapsiribojama) pardavimo objektų, pvz., pasiūlymų ir sutarčių, kūrimą ir projektų, apimančių WBS ir faktinių duomenų patvirtinimą, kūrimą.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Pagrindiniai pakeitimai tarp "Project Service Automation" ir "Project Operations"

Šiame skyriuje pateikiama pagrindinių pakeitimų, kurių galite tikėtis tarp "Project Service Automation" ir "Project Operations", suvestinė.

### <a name="project-planning"></a>Projekto planavimas

"Project Operations" projekto planavimo galimybės nebepriklauso nuo kliento ir serverio logikos derinio. Vietoj to, "Project Operations" naudoja "Project for the Web" kaip planavimo modulį. Šis planavimo galimybių pakeitimas įgalina keletą naujų funkcijų, pvz., lentos ir Ganto rodinius, ištekliais pagrįstą planavimą, [užduočių kontrolinio sąrašo elementus](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) ir projektų planavimo režimus. Naujas planavimo galimybes taip pat palaiko gausus naujų [programų programavimo sąsajų (API)](../project-management/schedule-api-preview.md) rinkinys. Šios API skirtos padėti užtikrinti, kad jokia programinė WBS objekto kūrimo, naujinimo ar naikinimo operacija nesugadintų grafiko apskaičiuotųjų laukų.

### <a name="billing-and-pricing"></a>Sąskaitų siuntimas ir kainodara

Tęsiant investicijas į "Project Operations", yra keletas naujų atsiskaitymo ir kainodaros galimybių. Štai keli pavyzdžiai:

- [Medžiagos naudojimo įrašymas projektuose ir projekto užduotyse](../material/material-usage-log.md)
- [Subrangos sutarčių valdymas](../pro/subcontracting/managing-subcontracts-overview.md)
- [Išankstinės arba išankstiniais apmokėjimais pagrįstos sutartys](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sutarties neviršijimo statusas ir patvirtinimai](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Užduotimis pagrįstas atsiskaitymas

### <a name="resource-management"></a>Išteklių valdymas

"Project Operations" teikia pasirinktinį (URS) plokštės ir planavimo asistento Universal Resource Scheduling palaikymą. Ši nauja patirtis taps privaloma 2023 m. balandžio mėn.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Kokių tipų diegimai šiuo metu palaikomi naujinant versiją?

| Šaltinis                                                 | Vertimas                                                    | Būsena                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | "Project Operations Lite" diegimas                        | Palaikomas               |
| Dynamics 365 Finance Projektų valdymas ir apskaita | "Project Operations Lite" diegimas                        | Šiuo metu nepalaikoma |
| Finansų projektų valdymas ir apskaita              | „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams     | Šiuo metu nepalaikoma |
| "Project Service Automation" 3.x                         | „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams     | Šiuo metu nepalaikoma |
| "Project for the Web" (speciali aplinka)            | "Project Operations Lite" diegimas                        | Šiuo metu nepalaikoma |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kaip įdiegti "Project Operations", kol versijos naujinimo įrankiai dar neprieinami?

Yra dvi parinktys, kaip įdiegti "Project Operations" prieš pasiekiant naujinimo įrankius:

- Naujos aplinkos kūrimas.
- Įdiekite "Project Operations" atskirai bet kurioje pardavimo organizacijoje, kurioje nėra "Project Service Automation".

Jei "Project Service Automation" įdiegta organizacijoje, bet nebuvo naudojama, ją galima pašalinti. Visiškai pašalinus "Project Service Automation", "Project Operations" galima įdiegti toje pačioje organizacijoje.
