---
title: Perkelkite visiškai sąskaitoje faktūroje numatytus atsiskaitymo etapus per supaprastintą laikotarpį
description: Šiame straipsnyje paaiškinama, kaip perkelti fiksuotos kainos atsiskaitymo etapus, kuriems klientui buvo išrašytos sąskaitos už atidarytas projekto sutartis iki paleidimo datos.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028712"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Perkelkite visiškai sąskaitoje faktūroje numatytus atsiskaitymo etapus per supaprastintą laikotarpį

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

## <a name="scenario"></a>Scenarijus

Contoso veikia su "Microsoft" Dynamics 365 Project Operations dėl išteklių / ne atsargų scenarijų. Vykdydama mažinimo veiklą, įgyvendinimo komanda turi perkelti atviras projekto sutartis iš senosios sistemos. Kai kurios projekto sutartys apima sutarčių eilutes, kuriose naudojamas fiksuotos kainos atsiskaitymo metodas ir už kurias jau buvo išrašytos iš dalies sąskaitos faktūros galutiniam klientui. Diegimo komanda turi perkelti šiuos atsiskaitymo etapus kaip **užregistruotą** kliento sf, nes pajamų atpažinimo tikslais jie turi būti įtraukti į bendrą sutarties vertę. Tačiau klientų balansams gautinose sumose ir Didžiojoje knygoje neturi būti daromas poveikis.

## <a name="solution"></a>Sprendimas

### <a name="prerequisites"></a>Būtinosios sąlygos

- Dynamics 365 Finance 10.0.24 ar naujesnė versija turi būti įdiegta.
- Aplinka, kurioje bus atlikti perkėlimo veiksmai, turi veikti priežiūros režimu. Perkeliant orientyrus, neturėtų būti vykdoma jokia kita veikla.
- Perkėlimo veiksmai turi būti atliekami tiksliai taip, kaip aprašyta čia, ir gali būti naudojami tik apkarpymo veiklai. "Microsoft" nepalaiko jokio kito šios galimybės naudojimo.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Sukurkite "Project Operations" integravimo sutarties eilutės etapų dvigubo rašymo žemėlapio iškirptę versiją 

1. Įsitikinkite, kad objekto **"Project Operations" integravimo sutarties eilutės orientyrų tikslinis susiejimas** yra atnaujintas. 

    1. Dalyje "Finance" eikite į **Duomenų valdymo** \> **duomenų objektus** ir pasirinkite objektą **Projekto operacijų integravimo sutarties eilutės orientyrai.** 
    2. Pasirinkite **Keisti paskirties susiejimą**. 
    3. **Puslapyje Žemėlapio skirstymas į paskirties vietą** pasirinkite **Generuoti susiejimą**, tada patvirtinkite, kad norite generuoti susiejimą.

2. Sustabdykite ir atnaujinkite **"Project Operations" integravimo sutarties eilutės etapus** (**msdyn\_ contractlinescheduleofvalues**) dvigubo rašymo žemėlapį. 

    1. Eikite į **Duomenų valdymas** \> **Du kartus rašykite**, pasirinkite žemėlapį ir atidarykite išsamią jo informaciją. 
    2. Pasirinkite **Stabdyti** ir palaukite, kol sistema sustabdys žemėlapį. 
    3. Pasirinkite **Atnaujinti lenteles**.

3. Įtraukite operacijos būsenos susiejimą.

    1. Pasirinkite **Įtraukti susiejimą**.
    2. Naujos eilutės stulpelyje **Finansai ir operacijų programėlės** pasirinkite lauką **TRANSSTATUS \[TRANSSTATUS\]**.
    3. Stulpelyje **Microsoft Dataverse** pasirinkite **msdyn\_ invoicestatus \[Invoice būseną\]**.
    4. Stulpelyje Žemėlapio **tipas** pasirinkite rodyklę dešinėn (**\>**).
    5. Pasirodžiusio dialogo lango lauke Sinchronizavimo **kryptis** pasirinkite **Dataverse programėlės** Finansai ir operacijos.
    6. Pasirinkite **Pridėti transformaciją**.
    7. **Lauke Transformuoti tipą** pasirinkite **ValueMap**.
    8. Pasirinkite **Pridėti vertės susiejimą**.
    9. Kairiajame lauke įveskite **4**. Dešiniajame lauke įveskite **192350001**. 
    10. Pasirinkite **Įrašyti**, tada uždarykite dialogo langą.

4. Pasirinkite **Išsaugoti kaip**, kad išsaugotumėte dvigubo rašymo žemėlapio versiją. 
5. **Srities Įtraukti lentelę** lauke **Leidėjas** pasirinkite **Numatytasis leidėjas**.
6. **Lauke Versija** įveskite versiją.
7. **Lauke Aprašas** įveskite pastabą apie šią iškirptą žemėlapio versiją. 
8. Pasirinkite **Įrašyti**.
9. Paleiskite žemėlapį.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Sąskaitose faktūrose nurodytų orientyrų perkėlimas į Dataverse aplinką

1. "Project Operations" Dataverse aplinkoje kurkite gaires, kurių sąskaitos faktūros būsena **yra Paruošta sf išrašymui**. Šiuo metu neperkelkite jokių etapų, kuriems nebuvo išrašyta sąskaita faktūra.

    > [!NOTE]
    > Prieš perkeldami atsiskaitymo tarpinius įvykius, įsitikinkite, kad finansinės dimensijos, susijusios su projekto sutarties eilute, nustatytos taip, kaip tikėtasi. Baigus perkėlimą, finansinių dimensijų redaguoti negalima.

2. Perkėlę visus etapus, sustabdykite šiuos dvigubo rašymo žemėlapius:

    - "Project Operations" integravimo sutarties linijos etapai (msdyn\_ contractlineschedule ofvalues)
    - „Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)
    - Projekto sąskaitų faktūrų pasiūlymų V2 (SF)

    Norėdami sustabdyti žemėlapius, atlikite šiuos veiksmus:

    1. Programoje "Finance" eikite į **Duomenų valdymas** \> **Dvigubas rašymas**, pasirinkite žemėlapį ir atidarykite jo informaciją.
    2. Pasirinkite **Stabdyti** ir palaukite, kol sistema sustabdys žemėlapį.

3. Projekto operacijų Dataverse aplinkoje kurkite ir patvirtinkite išankstines atsiskaitymo etapų sąskaitas faktūras. 

    1. Svetainės schemoje eikite į projekto sutartis, pasirinkite sutartis, tada pasirinkite **Kurti sąskaitas faktūras**.
    2. Sukūrę sąskaitas faktūras, atidarykite jas svetainės žemėlapio **meniu Sąskaitos faktūros**, tada pasirinkite **Patvirtinti**.

    Šis veiksmas sukuria reikiamus įrašus Dataverse aplinkoje. Tačiau tai neturi įtakos finansams ir gautinoms sumoms, nes anksčiau išvardyti dvigubo rašymo žemėlapiai buvo sustabdyti.

4. Patvirtinę visas formalias sąskaitas faktūras, grąžinkite visus dvigubo rašymo žemėlapius į pradinę būseną.

    1. Atnaujinkite "Project Operations" integravimo sutarties eilutės etapų versiją **(** msdyn **contractlinescheduleofvalues\_) dvigubo rašymo žemėlapį atgal** į pradinį. 
    2. Žemėlapių sąraše pasirinkite dvigubo rašymo žemėlapį, pasirinkite **Lentelės žemėlapio versija**, tada pasirinkite pradinę lentelės žemėlapio versiją.
    3. Pasirinkite **Įrašyti**.
    4. Iš naujo paleiskite šiuos dvigubo rašymo žemėlapius:

        - "Project Operations" integravimo sutarties linijos etapai (msdyn\_ contractlineschedule ofvalues)
        - „Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)
        - Projekto sąskaitų faktūrų pasiūlymų V2 (SF)

Orientyrai dabar perkeliami, o sistema yra pasirengusi tolesniems mažinimo veiklos veiksmams.
