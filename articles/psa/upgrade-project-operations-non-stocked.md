---
title: Naujinimas iš „Project Service Automation“ į „Project Operations“
description: Šiame straipsnyje apžvelgiamas procesas, nuo iki „Microsoft Dynamics 365 Project Service Automation“ ir „Dynamics 365 Project Operations“.
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736677"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Naujinimas iš „Project Service Automation“ į „Project Operations“

Džiaugiamės galėdami pranešti apie antrąjį iš trijų naujovinimo iš Microsoft Dynamics 365 Project Service Automation etapą į Microsoft Dynamics 365 Project Operations. Šiame straipsnyje apžvelgiami klientai, kurie šiuo įdomiu veiklos ciklu yra išsamūs. 

Naujinimo pristatymo programa bus padalyta į tris etapus.

| Naujinimo pristatymas | 1 etapas (2022 m. sausis) | 2 etapas (2022 m. lapkričio mėn.) | 3 etapas (2023 m. balandžio mėn.)  |
|------------------|------------------------|---------------------------|---------------------------|
| Projektų darbo struktūros (WBS) priklausomybė nuo darbo struktūros | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS pagal šiuo metu palaikomus projektų vykdymo „Project Operations“ | | :heavy_check_mark: | :heavy_check_mark: |
| WBS, esantis už šiuo metu palaikomų "Project Operations" apribojimų, įskaitant "Project Desktop Client" palaikymą | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Naujinimo proceso funkcijos 

Atnaujinę į svetainės struktūrą įtraukėme naujinimo žurnalų, kad administratoriai galėtų lengviau diagnozuoti triktis. Be naujos sąsajos, naujos tikrinimo taisyklės bus pridėtos siekiant užtikrinti duomenų vientisumą po atnaujinimo. Toliau nurodyti tikrinimas bus įtrauktas į naujinimo procesą.

| Tikrinimai | 1 etapas (2022 m. sausis) | 2 etapas (2022 m. lapkričio mėn.) | 3 etapas  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS bus tikrinama pagal bendrą duomenų vientisumo vientisumą (pvz., išteklių priskyrimai, susieti su ta pačia pirmine užduotimi, bet turi skirtingus pirminius projektus). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bus tikrinamas pagal žinomas [Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS bus tikrinamas pagal žinomas žiniatinklio "Project desktop client" ribas . | |  | :heavy_check_mark: |
| Rezervuotini ištekliai ir projektų kalendoriai bus įvertinti atsižvelgiant į įprastas kalendoriaus taisyklių išimtis. | | :heavy_check_mark: | :heavy_check_mark: |

2 etape klientai, kurie atnaujins į "Project Operations", esamų projektų bus atnaujinti ir projektai bus planuojami tik skaityti. Naudojant šį tik skaitomą rodinį visas WBS bus matomas sekimo tinklelyje. Norėdami redaguoti WBS, projektų vadovai [**projekto**](/PSA-Upgrade-Project-Conversion.md) pagrindiniame puslapyje gali pažymėti Konvertuoti. Tada foninis procesas atnaujina projektą, kad jį naudojant būtų palaikoma nauja „Project for the Web“ planavimo iš žiniatinklio funkcija. Šis etapas tinka klientams, kurie turi projektus, kurie atitinka [žinomas „Project for the Web“](/project-for-the-web/project-for-the-web-limits-and-boundaries).

3 etape bus įtrauktas „Project Desktop client" palaikymas, naudingas klientams, kurie nori toliau redaguoti savo projektus iš tos programos. Tačiau, jei esami projektai konvertuojami į naują „Project for the Web" patirtį, prieiga prie papildinyje bus išjungta kiekvienam konvertuotam projektui.

## <a name="prerequisites"></a>Būtinosios sąlygos

Norėdami, kad būtų galima atnaujinti 1 etapą, turite atitikti šiuos kriterijus:

- Paskirties aplinkoje neturi būti jokių objekto **msdyn_projecttask** įrašų.
- Tinkamas "Project Operations" licencijas reikia priskirti visiems aktyviems vartotojams. 
- Turite patikrinti naujinimo procesą bent vienoje ne gamybos aplinkoje, kurioje yra jūsų gamybos aplinką sutapęs atstovas duomenų rinkinys.
- Paskirties aplinka turi būti atnaujinta į "Project Service Automation" 37 naujinimo leidimą (V3.10.58.120) arba naujesnę versiją.

Norėdami, kad būtų galima atnaujinti 2 etapą, turite atitikti šiuos kriterijus:

- Tinkamas "Project Operations" licencijas reikia priskirti visiems aktyviems vartotojams. 
- Turite patikrinti naujinimo procesą bent vienoje ne gamybos aplinkoje, kurioje yra jūsų gamybos aplinką sutapęs atstovas duomenų rinkinys.
- Paskirties aplinka turi būti atnaujinta į "Project Service Automation" 37 naujinimo leidimą (V3.10.58.120) arba naujesnę versiją.
- Aplinkos, kuriose yra užduočių (msdyn_projecttask) yra palaikomos tik jei bendras projekto užduočių skaičius yra 500 ar mažiau.

Būtinosios 3 etapo sąlygos bus atnaujintos kaip bendrosios prieinamumo datos.

## <a name="licensing"></a>Licencijavimas

Jei turite aktyvias "Project Service Automation" licencijas, galite įdiegti ir naudoti „Project Operations", į kurią įtrauktos visos „Project Service Automation" galimybės ir kt. Tokiu būdu galite patikrinti "Project Operations" galimybes ir toliau naudoti "Project Service Automation" gamybai. Pasibaigus "Project Service Automation" licencijų galiojimui turėsite pereiti prie "Project Operations". Planuokite šį perėjimą, turite atsižvelgti į tai, kad "Project Operations" licencijoje nėra "Project Service Automation" licencijos. Klientai, kurie turi scenarijų, kai jie dislokavo "Project Service Automation" ir turi toliau naudoti arba padidinti PSA licencijas, kol ketina pereiti prie "Project Operations", gali prašyti laikinųjų PSA licencijų pagal įsigytas "Project Operations" licencijas. Viena "Project Service Automation" licencija bus viena "Project Operations" licencija. Laikinųjų PSA licencijų gali būti paprašyta naudojant šį saitą: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Tinkinimų tikrinimas ir pergaminimas

Pradinis taškas – visus tinkinimus importuokite į švarią "Project Operations" (Lite) aplinką, kad įsitikintų, jog importas sėkmingas ir kad verslo operacijos veikia taip, kaip tikėjotės.

Toliau pateikiami keli dalykai, kurių reikia norint sužinoti:

- Importuoti gali nepavykti, nes trūksta priklausomybių. Kitaip tariant, tinkinimų nuorodos laukai arba kiti komponentai, pašalinti "Project Operations". Tokiu atveju pašalinkite šias priklausomybes iš programavimo aplinkos.
- Jei jūsų nevaldomasis ir valdomasis sprendimai apima netinkintus komponentus, pašalinkite šiuos komponentus iš sprendimo. Pavyzdžiui, kai tinkinate projekto **objektą**, į savo sprendimą įtraukite tik objekto antraštę. Neį įtraukite ne visus laukus. Jei anksčiau įtraukėte visus antrinius komponentus, gali tekti rankiniu būdu sukurti naują sprendimą ir į jį įtraukti aktualių komponentų.
- Formos ir rodiniai gali būti rodomi ne taip, kaip tikėjotės. Kai kuriais atvejais, jei tinkinote kurią nors iš anksto nustatyta formas arba rodinius, tinkinimai gali neleisti pritaikyti naujų "Project Operations" naujinimų. Kad būtų nustatytos šios problemos, rekomenduojame greta peržiūrėti švarų "Project Operations" diegimą ir "Project Operations" diegimą, kuriame yra jūsų tinkinimai. Palyginkite dažniausiai naudojamas verslo formas ir patvirtinkite, kad jūsų formos versija vis dar prasminga ir kad švarioje formos versijoje kažko nėra. Atlikite to paties tipo tinkintų rodinių peržiūrą greta.
- Pa vykdymo metu gali nepavykti verslo logika. Kadangi nuorodos į laukus jūsų papilduose importavimo metu nėra tikrintos, verslo logika gali nepavykti dėl nuorodų į laukus, kurių nebėra, ir galite gauti klaidos pranešimą, kuriame pateikiamas toks pavyzdys: "Projektui" nėra atributo, kurio pavadinimas = "msdyn_plannedhours" ir "NameMapping " = "Loginis". Tokiu atveju modifikuokite tinkinimus, kad jie galėtų naudoti naujus laukus. Jei savo papildinio logioje naudojate automatiškai sugeneruotas "susietos" ir "susiakime" tipo nuorodas, apsvarstykite galimybę išvalyti tuos iš švarios įdiegties serverius. Tokiu būdu galite lengvai identifikuoti visas vietas, kur jūsų priedai priklauso nuo nebenaudojami laukai.

Atnaujinę tinkinimus, kad būtų galima švariai importuoti "Project Operations", pereikite prie kitų veiksmų.

## <a name="end-to-end-testing-in-development-environments"></a>Tikrinimas nuo pabaigos programavimo aplinkose

### <a name="initiate-upgrade"></a>Inicijuoti atnaujinimą 

1. Nueikite į Power Platform administravimo centrą adresu, ir suraskite bei pasirinkite savo aplinką. Tada programose suraskite ir rinkitės **Dynamics 365 Project Operations**.
2. Rinkitės **Diegti** jei norite pradėti naujinti. Administravimo Power Platform centras pateiks šį diegimą kaip naują diegimą. Tačiau bus aptikta senesnė „Project Service Automation" versija ir bus atnaujinta esama įdiegtis.

    Kai naujinimas bus baigtas, aplinkoje turi būti rodoma, kad įdiegta „Project Operations" ir neįdiegta „Project Service Automation".

    Priklausomai nuo duomenų sumos aplinkoje, naujinimas gali užtrukti kelias valandas. Pagrindinė komanda, valdanti atnaujinimą, turi atitinkamai planuoti ir vykdyti atnaujinimą ne darbo valandomis. Kai kuriais atvejais, jei duomenų apimtis yra didelė, plėtotė turi būti vykdoma naudojant ne darbo laiką. Sprendimas dėl planavimo turėtų būti pagrįstas bandymų rezultatais apatinėje aplinkoje.

3. Atitinkamai atnaujinkite pasirinktinius sprendimus. Šiuo metu šio straipsnio skyriuje [Tikrinimas ir pertvarkymai](#testing-and-refactoring-customizations) įdiekite visus tinkinimų pakeitimus.
4. Eikite į **make.powerapps.com**, rinkitės savo aplinką iš iškritusio meniu dešinėje viršuje portalo, rinkitės **Sprendimai** kairiajame meniu, rinkitės **Project Operations nerekomenduojami komponentai** sprendimą ir **Išdiegti**.

    Šis sprendimas yra laikinas sprendimas, kuriame yra esamas duomenų modelis ir komponentai, pateikiami naujinant. Pašalindami šį sprendimą pašalinsite visus nebenaudojami laukus ir komponentus. Tokiu būdu galite supaprastinti sąsają ir palengvinti integravimą bei plėtinius.
    
### <a name="upgrade-to-project-operations-lite"></a>Naujinti į „Project Operations Lite“

Toliau aprašyti naujinimo procesas ir susietas klaidų registravimas:

1. **PSA versijos tikrinimas:** norint įdiegti "Project Operations", reikia turėti V3.10.58.120 aukštesnę versiją.
1. **Išankstinis tikrinimas:** kai administratorius inicijuoja atnaujinimą, sistema vykdo kiekvieno objekto, kuris yra pagrindinis „Project Operations“ sprendimo objektas, išankstinio tikrinimo operaciją. Šis veiksmas patikrina, ar visos objektų nuorodos yra tinkamos ir užtikrina, kad su WBS susiję duomenys yra paskelbti „Project for the Web“ limituose.
1. **Metaduomenų naujinimas.** Sėkmingai atlikusi išankstinio patikrinimo procesą sistema iniciuoja schemos pakeitimus ir sukuria nebenaudojamų komponentų sprendimą. Baigę atlikti visus reikiamus tinkinimų veiksmus, galite pašalinti šį nebenaudojamą sprendimą. Šis veiksmas yra ilgiausią naujinimo proceso dalį ir gali užtrukti iki keturių valandų.
1. **Duomenų naujinimas:** atlikus visus reikiamus schemos pakeitimus metaduomenų naujinimo žingsnyje jūsų duomenys perkeliami į naują schemą ir atliekami visi būtini numatytieji ir perskaičiavimai.
1. **Projekto grafiko modulio naujinimas:** sėkmingai atnaujinus duomenis **pagrindiniame** puslapyje skirtukas Grafikas yra iš naujo ženkluotos **užduotys**. Kai vartotojas pasirenka šį skirtuką po atnaujinimo, jis nukreipiamas į stebėjimo tinklelį ir peržiūrėti WBS versiją, tik skaitomą. Norėdami redaguoti WBS, jie turi pradėti grafiko [konvertavimo procesą](/PSA-Upgrade-Project-Conversion.md). Visi projektai, neturintys iš anksto esamo WBS, gali tiesiogiai naudoti naują planavimo funkciją be konvertavimo.
 
### <a name="validate-common-scenarios"></a>Patvirtinti bendrus scenarijus

Kai patikrinate konkrečius tinkinimus, rekomenduojame peržiūrėti ir visose programose palaikomus veiklos procesus. Šie verslo procesai apima, bet tuo neapsiribojant, pardavimo objektų, pvz., pasiūlymų ir sutarčių, kūrimą ir projektų, kuriuose yra WBS, kūrimą ir faktinių duomenų patvirtinimą.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Pagrindiniai pokyčiai lyginant „Project Service Automation“ ir „Project Operations“

Šiame skyriuje pateikiama pagrindinių pakeitimų, kuriuos galite tikėtis tarp "Project Service Automation" ir "Project Operations", suvestinė.

### <a name="project-planning"></a>Projekto planavimas

Projektų planavimo galimybės "Project Operations" nebenaudojamos kartu su kliento logika ir serverio logika. Vietoj to "Project Operations" naudoja "Project for the Web" kaip planavimo modulio funkciją. Šis planavimo galimybių keitimas leidžia naudoti kelias naujas funkcijas, pvz., [rodinius Lenta ir I. G. G](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). I. G. G. O. O. Naujas planavimo galimybes taip pat palaiko gausus naujų programų [programavimo sąsajų (API) rinkinys](../project-management/schedule-api-preview.md). Šios API skirtos padėti užtikrinti, kad jokia programinė objekto kūrimo, naujinimo ar naikinimo operacija WBS sugadins tvarkaraščio apskaičiuotus laukus.

### <a name="billing-and-pricing"></a>Sąskaitų siuntimas ir kainodara

"Project Operations" yra vienas iš indingų ir nauji atsiskaitymo ir kainodaros galimybių. Štai keli pavyzdžiai:

- [Medžiagų naudojimo projektuose ir projekto užduotyse įrašymas](../material/material-usage-log.md)
- [Subrangos sutarties valdymas](../pro/subcontracting/managing-subcontracts-overview.md)
- [Išankstinės arba išankstiniais apmokėjimais pagrįstos sutartys](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Neviršijimo būsenos ir tikrinimų sutartis](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Užduotimis pagrįstas atsiskaitymas

### <a name="resource-management"></a>Išteklių valdymas

"Project Operations" teikia pasirenkamą Universal Resource Scheduling (URS) lentos ir planavimo asistento palaikymą. Ši nauja patirtis taps privaloma 2023 m. balandžio mėn.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Kurie visuotinio diegimo tipai yra kol kas palaikomi naujinti?

| Šaltinis                                                 | Vertimas                                                    | Būsena                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | „Project Operations Lite visuotinis diegimas“                        | Palaikomas               |
| Projektų valdymas ir apskaita „Dynamics 365 Finance” | „Project Operations Lite visuotinis diegimas“                        | Šiuo metu nepalaikoma |
| „Finance“ projekto valdymas ir apskaita              | „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams     | Šiuo metu nepalaikoma |
| „Project Service Automation“ 3.x                         | „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams     | Šiuo metu nepalaikoma |
| „Project for the Web“ (paskirtosios aplinkos)            | „Project Operations Lite visuotinis diegimas“                        | Šiuo metu nepalaikoma |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kaip įdiegti "Project Operations" prieš įdiegiant naujinimo įrankį?

Yra dvi "Project Operations" diegimo parinktys, kad būtų galima naudotis naujinimo įrankiais:

- Naujos aplinkos parengimas.
- „Project Operations" įdiekite atskirai bet kurioje pardavimo organizacijoje, kurioje nėra "Project Service Automation".

Jei organizacijoje įdiegtas „Project Service Automation", tačiau jis nenaudotas, jį galima pašalinti. Kai visiškai pašalinsite „Project Service Automation", "Project Operations" bus galima įdiegti toje pačioje organizacijoje.
