---
title: Versijos naujinimas iš projekto aptarnavimo automatizavimo į projekto operacijas
description: Šioje temoje pateikiama proceso, kurį reikia naujinti iš Microsoft Dynamics 365 Project Service Automation į Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954297"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Versijos naujinimas iš projekto aptarnavimo automatizavimo į projekto operacijas

Džiaugiamės galėdami pranešti apie pirmąjį iš trijų etapų atnaujinti iš Microsoft Dynamics 365 Project Service Automation į Dynamics 365 Project Operations. Ši tema suteikia apžvalgą klientams, kurie pradeda šią įdomią kelionę. Būsimos temos apims kūrėjų svarstymus ir išsamią informaciją apie funkcijų patobulinimus. Jie ne tik pateiks patarimų, padėsiančių pasiruošti atnaujinti projekto operacijas, bet ir paaiškins, ko galite tikėtis atnaujinę versiją.

Atnaujinimo pristatymo programa bus suskirstyta į tris etapus.

| Atnaujinti pristatymą | 1 etapas (2022 m. sausio mėn.) | 2 etapas (2022 m. balandžio banga) | 3 etapas (2022 m. balandžio banga) |
|------------------|------------------------|---------------------------|---------------------------|
| Nėra priklausomybės nuo projektų darbo paskirstymo struktūros (WBS) | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS šiuo metu palaikomose projekto operacijų ribose | | :heavy_check_mark: | :heavy_check_mark: |
| WBS už šiuo metu palaikomų projekto operacijų ribų, įskaitant projekto darbalaukio kliento palaikymą | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Atnaujinimo proceso funkcijos 

Kaip atnaujinimo proceso dalį, mes pridėjome atnaujinimo žurnalus į svetainės struktūrą, kad administratoriai galėtų lengviau diagnozuoti gedimus. Be naujos sąsajos, bus pridėtos naujos tikrinimo taisyklės, užtikrinančios duomenų vientisumą po atnaujinimo. Atnaujinimo procesas bus įtrauktas į šiuos patvirtinimus.

| Tikrinimą | 1 etapas (2022 m. sausio mėn.) | 2 etapas (2022 m. balandžio banga) | 3 etapas (2022 m. balandžio banga) |
|-------------|------------------------|---------------------------|---------------------------|
| WBS bus patvirtinta pagal bendrus duomenų vientisumo pažeidimus (pvz., išteklių priskyrimus, kurie yra susieti su ta pačia pirmine užduotimi, bet turi skirtingus pirminius projektus). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bus patvirtintas pagal [žinomas žiniatinklio projekto ribas](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bus patvirtintas pagal žinomas projekto darbalaukio kliento ribas. | | :heavy_check_mark: | :heavy_check_mark: |
| Rezervuojami ištekliai ir projektų kalendoriai bus vertinami pagal įprastas nesuderinamų kalendoriaus taisyklių išimtis. | | :heavy_check_mark: | :heavy_check_mark: |

2 etape klientai, kurie atnaujins į projekto operacijas, esamus projektus atnaujins į tik skaitomą projektų planavimo patirtį. Šioje tik skaitomoje patirtyje visas WBS bus matomas stebėjimo tinklelyje. Norėdami redaguoti WBS, projektų vadovai pagrindiniame projektų puslapyje gali **pasirinkti** **Konvertuoti**. Tada foninis procesas atnaujins projektą taip, kad jis palaikytų naują projekto planavimo patirtį iš "Project for the Web". Šis etapas tinka klientams, kurių projektai atitinka [žinomas žiniatinklio projekto](/project-for-the-web/project-for-the-web-limits-and-boundaries) ribas.

3 etape bus pridėta parama projekto darbalaukio klientui, skirta klientams, norintiems toliau redaguoti savo projektus iš tos programos. Tačiau, jei esami projektai konvertuojami į naują žiniatinklio patirties projektą, prieiga prie priedo bus išjungta kiekvienam konvertuotam projektui.

## <a name="prerequisites"></a>Būtinosios sąlygos

Kad galėtų atnaujinti 1 etapo atnaujinimą, klientas turi atitikti šiuos kriterijus:

- Paskirties aplinkoje neturi būti jokių **msdyn_projecttask objekto įrašų.**
- Galiojančios projekto operacijų licencijos turi būti priskirtos visiems aktyviems kliento vartotojams. 
- Klientas turi patvirtinti atnaujinimo procesą bent vienoje ne gamybos aplinkoje, kurioje yra reprezentatyvus duomenų rinkinys, suderintas su gamybos duomenimis.
- Paskirties aplinka turi būti atnaujinta į 38 arba naujesnės versijos naujinimo leidimą.

Artėjant bendroms prieinamumo datoms, bus atnaujintos 2 ir 3 etapo prielaidos.

## <a name="licensing"></a>Licencijavimas

Jei turite aktyvių "Project Service Automation" licencijų, galite įdiegti ir naudoti "Project Operations", kuri apima visas "Project Service Automation" galimybes ir kt. Tokiu būdu galite išbandyti projekto operacijų galimybes, kol toliau naudojate "Project Service Automation" gamyboje. Pasibaigus "Project Service Automation" licencijų galiojimui, turėsite pereiti prie "Project Operations". Planuodami šį perėjimą, turite atsižvelgti į tai, kad projekto operacijų licencijoje nėra projekto paslaugų automatizavimo licencijos.

## <a name="testing-and-refactoring-customizations"></a>Tinkinimo testavimas ir pertvarkymas

Pradinis taškas importuokite visus tinkinimus į švarią projekto operacijų (lite) aplinką, kad patvirtintumėte, jog importavimas sėkmingas ir kad verslo operacijos veikia taip, kaip tikėtasi.

Štai keletas dalykų, į kuriuos reikia atkreipti dėmesį:

- Importavimas gali nepavykti dėl trūkstamų priklausomybių. Kitaip tariant, tinkinimo nuorodos laukai arba kiti komponentai, pašalinti projekto operacijose. Tokiu atveju pašalinkite šias priklausomybes nuo vystymosi aplinkos.
- Jei nevaldomi ir valdomi sprendimai apima ne tinkintų komponentų, pašalinkite šiuos komponentus iš sprendimo. Pavyzdžiui, kai tinkinate **projekto** objektą, į sprendimą įtraukite tik objekto antraštę. Nedėkite visų laukų. Jei anksčiau įtraukėte visus subkomponentus, gali tekti rankiniu būdu sukurti naują sprendimą ir pridėti prie jo atitinkamus komponentus.
- Formos ir rodiniai gali neatrodyti netikėti. Tam tikromis aplinkybėmis, jei pritaikėte bet kurią iš "out-of-box" formų ar rodinių, tinkinimai gali užkirsti kelią naujiems projekto operacijų naujinimams įsigalioti. Norėdami nustatyti šias problemas, rekomenduojame atlikti švarios projekto operacijų diegimo ir projekto operacijų diegimo, apimančio jūsų tinkinimus, peržiūrą. Palyginkite dažniausiai naudojamas formas savo versle, kad patvirtintumėte, jog jūsų formos versija vis dar yra prasminga ir trūksta kažko iš švarios formos versijos. Atlikite to paties tipo peržiūrą vienas šalia kito, kad peržiūrėtumėte bet kokius pritaikytus rodinius.
- Verslo logika gali nepavykti vykdymo metu. Kadangi nuorodos į papildinių laukus importavimo metu nėra patvirtintos, verslo logika gali nepavykti dėl nuorodų į laukus, kurių nebėra, ir galite gauti klaidos pranešimą, panašų į šį pavyzdį: "Projekto" objekte nėra atributo, kurio pavadinimas = "msdyn_plannedhours" ir Vardų naudojimas = "Loginis". Tokiu atveju modifikuokite tinkinimus taip, kad jie naudotų naujus laukus. Jei naudojate automatiškai sugeneruotas tarpinių serverių klases ir stiprias tipo nuorodas savo priedo logikoje, apsvarstykite galimybę atkurti tuos tarpinius serverius iš švaraus diegimo. Tokiu būdu galite lengvai nustatyti visas vietas, kuriose jūsų papildiniai priklauso nuo pasenusių laukų.

Atnaujinę tinkinimus, kad švariai importuotumėte projekto operacijas, pereikite prie tolesnių veiksmų.

## <a name="end-to-end-testing-in-lower-environments"></a>Išsakęs testavimas žemesnėje aplinkoje

### <a name="run-the-upgrade-in-production"></a>Vykdyti gamybos naujinimą

1. Administravimo Power Platform centre raskite ir pasirinkite aplinką. Tada programose raskite ir pasirinkite **Dynamics 365 Project Operations**.
2. Norėdami **pradėti naujinimą, pasirinkite** Diegti. Power Platform Administravimo centras pristatys šį diegimą kaip naują diegimą. Tačiau bus aptikta ankstesnė "Project Service Automation" versija, o esamas diegimas bus atnaujintas.

    Baigus naujinimą, aplinka turėtų parodyti, kad įdiegtos projekto operacijos ir kad projekto aptarnavimo automatizavimas neįdiegtas.

    > [!NOTE]
    > Priklausomai nuo duomenų kiekio aplinkoje, atnaujinimas gali užtrukti kelias valandas. Pagrindinė komanda, valdanti atnaujinimą, turėtų atitinkamai planuoti ir paleisti atnaujinimą ne darbo valandomis. Kai kuriais atvejais, jei duomenų apimtis yra didelė, atnaujinimas turėtų būti vykdomas savaitgalį. Sprendimas dėl planavimo turėtų būti grindžiamas bandymų rezultatais žemesnėje aplinkoje.

3. Jei reikia, atnaujinkite pasirinktinius sprendimus. Šiuo metu įdiekite visus tinkinimo keitimus [šios temos skyriuje Testavimas ir](#testing-and-refactoring-customizations) tinkinimas.
4. Eikite **į** \> **Parametrų sprendimai** ir pasirinkite, kad pašalintumėte **sprendimo Projekto operacijos nebenaudojami** komponentai.

    Šis sprendimas yra laikinas sprendimas, kuriame yra esamas duomenų modelis ir komponentai, esantys atnaujinimo metu. Pašalinę šį sprendimą, pašalinkite visus nebenaudojamų laukų ir komponentų. Tokiu būdu padėsite supaprastinti sąsają ir palengvinti integraciją bei plėtinį.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Esminiai pokyčiai tarp projektų paslaugų automatizavimo ir projekto operacijų

Šiame skyriuje pateikiama pagrindinių pakeitimų, kurių galite tikėtis tarp "Project Service Automation" ir "Project Operations", santrauka.

### <a name="project-planning"></a>Projekto planavimas

Projekto operacijų projekto planavimo galimybės nebepasiremia kombinuota kliento logika ir serverio logika. Vietoj to, projekto operacijos naudoja projektą žiniatinklyje kaip planavimo variklį. Šis planavimo galimybių pakeitimas įgalina kelias naujas funkcijas, pvz., valdybos ir Ganto rodinius, ištekliais pagrįstą planavimą, [užduočių kontrolinio sąrašo elementus](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) ir projektų planavimo režimus. Naujas planavimo galimybes taip pat palaiko turtingas naujų [programų programavimo sąsajų (API) rinkinys](../project-management/schedule-api-preview.md). Šiomis API siekiama užtikrinti, kad jokia programinė operacija objektui WBS kurti, atnaujinti ar naikinti nesugadintų grafiko apskaičiuotų laukų.

## <a name="billing-and-pricing"></a>Sąskaitų siuntimas ir kainodara

Tęsiant investicijas į projekto operacijas, yra keletas naujų atsiskaitymo ir kainodaros galimybių. Štai keli pavyzdžiai:

- [Medžiagų naudojimo įrašant projektus ir projekto užduotis](../material/material-usage-log.md)
- [Subrangos valdymas](../pro/subcontracting/managing-subcontracts-overview.md)
- [Išankstinės arba išankstiniais apmokėjimais pagrįstos sutartys](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sutarties neviršijimas būsena ir patvirtinimai](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Užduotimis pagrįstas atsiskaitymas

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Kokius diegimo tipus šiuo metu palaiko naujinti?

| Šaltinis                                                 | Vertimas                                                    | Būsena                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Projekto operacijų lite diegimas                        | Palaikomas               |
| Dynamics 365 Finance Projektų valdymas ir apskaita | Projekto operacijų lite diegimas                        | Šiuo metu nepalaikoma |
| Finansai Projektų valdymas ir apskaita              | „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams     | Šiuo metu nepalaikoma |
| Finansai Projektų valdymas ir apskaita              | „Project Operations“, skirta laikomų medžiagų / gamybos užsakymo scenarijams | Šiuo metu nepalaikoma |
| Projekto paslaugų automatizavimas 3.x                         | „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams     | Šiuo metu nepalaikoma |
| Interneto projektas (skirta aplinka)            | Projekto operacijų lite diegimas                        | Šiuo metu nepalaikoma |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kaip įdiegti projekto operacijas prieš pasiekiant naujinimo įrankius?

Yra dvi projekto operacijų diegimo parinktys prieš pasiekiant naujinimo įrankį:

- Sukurti naują aplinką.
- Projekto operacijas įdiekite atskirai bet kurioje pardavimo organizacijoje, kurioje nėra "Project Service Automation".

> [!NOTE]
> Jei "Project Service Automation" įdiegta organizacijoje, bet ji nebuvo naudojama, ją galima pašalinti. Visiškai pašalinus "Project Service Automation", "Project Operations" galima įdiegti toje pačioje organizacijoje.
