---
title: Visiškai išrašytų sąskaitų faktūrų išrašymo etapų perkėlimas
description: Šiame straipsnyje paaiškinta, kaip perkelti fiksuotos kainos atsiskaitymo etapus, pagal kuriuos klientui buvo išrašytos sąskaitos faktūros pagal atviras projekto sutartis prieš įgyvendinimo pradžios datą.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Visiškai išrašytų sąskaitų faktūrų išrašymo etapų perkėlimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

## <a name="scenario"></a>Scenarijus

„Contoso“ paleidžiama naudojant „Microsoft Dynamics 365 Project Operations“, skirtą išteklių / nelaikomų medžiagų scenarijams. Diegimo komanda, atlikdama visišką perkėlimą,turi perkelti ir atviras projekto sutartis iš senos sistemos. Kai kurios projekto sutartys apima sutarties eilutes, kuriose naudojamas fiksuotos kainos atsiskaitymo metodas ir pagal kurias galutiniam klientui jau iš dalies išrašyta sąskaita faktūra. Diegimo komanda šiuos atsiskaitymo etapus turi perkelti kaip **Kliento sąskaita faktūra užregistruota**, nes juos reikia įtraukti į bendrą sutarties vertę pajamų pripažinimo tikslais. Tačiau klientų balansams, esantiems dalyse Gautinos sumos ir Bendra didžioji knyga, neturi būti daromas poveikis.

## <a name="solution"></a>Sprendimas

### <a name="prerequisites"></a>Būtinosios sąlygos

- Turi būti įdiegta „Dynamics 365 Finance 10.0.24“ arba naujesnė versija.
- Aplinka, kurioje bus atliekami perkėlimo veiksmai, turi veikti priežiūros režimu. Perkeliant etapus kitų veiklų atlikti negalima.
- Perkėlimo veiksmus reikia atlikti tiksliai taip, kaip aprašyta čia, ir juos galima naudoti tik visiško perkėlimo veiklai. „Microsoft“ nepalaiko jokio kito šios galimybės naudojimo.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>„Project Operations“ integravimo sutarties eilučių etapų dvigubo rašymo schemos visiško perkėlimo versijos kūrimas 

1. Įsitikinkite, kad objektas **„Project Operations“ integravimo sutarties eilučių etapai** tikslinis susiejimas yra atnaujintas. 

    1. Naudodami „Finance“ eikite į **Duomenų valdymas** \> **Duomenų objektai** ir pasirinkite objektą **„Project Operations“ integravimo sutarties eilučių etapai**. 
    2. Pasirinkite **Modifikuoti paskirties susiejimus**. 
    3. Puslapyje **Susieti išdėstymą su paskirties vieta** pasirinkite **Generuoti susiejimą**, tada patvirtinkite, kad norite generuoti susiejimą.

2. Sustabdykite ir atnaujinkite **„Project Operations“ integravimo sutarties eilučių etapai** (**msdyn\_contractlinescheduleofvalues**) dvigubo rašymo schemą. 

    1. Eikite į **Duomenų valdymas** \> **Dvigubas rašymas**, pasirinkite schemą ir atidarykite jos išsamią informaciją. 
    2. Pasirinkite **Stabdyti** ir palaukite, kol sistema sustabdys schemą. 
    3. Pasirinkite **Atnaujinti lenteles**.

3. Pridėkite operacijos būsenos susiejimą.

    1. Pasirinkite **Pridėti susiejimą**.
    2. Naujos eilutės stulpelyje **Finansų ir operacijų programos** pasirinkite lauką **TRANSSTATUS \[TRANSSTATUS\]**.
    3. Stulpelyje **Microsoft Dataverse** pasirinkite **msdyn\_invoicestatus \[Sąskaitos faktūros būsena\]**.
    4. Stulpelyje **Schemos tipas** pasirinkite rodyklę dešinėn (**\>**).
    5. Pasirodžiusiame dialogo lango lauke **Sinchronizavimo kryptis** pasirinkite **Iš „Dataverse“ į finansų ir operacijų programas**.
    6. Pasirinkite **Pridėti transformavimą**.
    7. Lauke **Transformavimo tipas** pasirinkite **ValueMap**.
    8. Pasirinkite **Įtraukti vertės susiejimą**.
    9. Kairiajame lauke įveskite **4**. Dešiniajame lauke įveskite **192350001**. 
    10. Pasirinkite **Įrašyti** ir uždarykite dialogo langą.

4. Pasirinkite **Įrašyti kaip**, kad įrašytumėte dvigubo rašymo schemos versiją. 
5. Srities **Įtraukti lentelę** lauke **Leidėjas** pasirinkite **Numatytasis leidėjas**.
6. Lauke **Versija** įveskite versiją.
7. Lauke **Aprašas** įveskite pastabą apie šią schemos visiško perkėlimo versiją. 
8. Pasirinkite **Įrašyti**.
9. Paleiskite schemą.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Etapų, kuriems išrašyta sąskaita faktūra, perkėlimas į „Dataverse“ aplinką

1. „Project Operations“ aplinkoje „Dataverse“ sukurkite etapus, kurių sąskaitų faktūrų išrašymo būsena yra **Parengta išrašyti sąskaitą faktūrą**. Šiuo metu neperkelkite jokių etapų, už kuriuos nebuvo išrašyta sąskaita faktūra.

    > [!NOTE]
    > Prieš perkeldami atsiskaitymo etapus įsitikinkite, kad finansinės dimensijos, susijusios su projekto sutarties eilute, yra nustatytos taip, kaip numatyta. Baigus perkėlimą finansinių dimensijų redaguoti negalima.

2. Kai bus perkelti visi etapai, sustabdykite šias dvigubas rašymo schemas:

    - „Project Operations“ integravimo sutarties eilučių etapai (msdyn\_contractlinescheduleofvalues)
    - „Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)
    - Projekto sąskaitų faktūrų pasiūlymų V2 (SF)

    Norėdami sustabdyti schemas, atlikite šiuos veiksmus:

    1. Naudodami „Finance“, eikite į **Duomenų valdymas** \> **Dvigubas rašymas**, pasirinkite schemą ir atidarykite jos išsamią informaciją.
    2. Pasirinkite **Stabdyti** ir palaukite, kol sistema sustabdys schemą.

3. „Project Operations“ aplinkoje „Dataverse“ kurkite ir patvirtinkite išankstines atsiskaitymo etapų sąskaitas faktūras. 

    1. Svetainės struktūroje eikite į projekto sutartis, pasirinkite sutartis, tada pasirinkite **Kurti sąskaitas faktūras**.
    2. Sukūrę sąskaitas faktūras, jas atidarykite svetainės struktūros meniu **Sąskaitos faktūros**, tada pasirinkite **Patvirtinti**.

    Šiuo veiksmu sukuriami reikiami aplinkos „Dataverse“ įrašai. Tačiau tai neturi įtakos finansams ir gautinoms sumoms, nes anksčiau išvardytos dvigubo rašymo schemos buvo sustabdytos.

4. Kai visos išankstinės sąskaitos faktūros bus patvirtintos, grąžinkite visas dvigubo rašymo schemas į pradinę būseną.

    1. Atnaujinkite **„„Project Operations“ integravimo sutarties eilučių etapai** (**msdyn\_contractlinescheduleofvalues**) dvigubo rašymo schemos versiją, kad ji vėl būtų pradinė. 
    2. Schemų sąraše pasirinkite dvigubo rašymo schemą, pasirinkite **Lentelės schemos versija**, tada pasirinkite pradinę lentelės schemos versiją.
    3. Pasirinkite **Įrašyti**.
    4. Iš naujo paleiskite šias dvigubo rašymo schemas:

        - „Project Operations“ integravimo sutarties eilučių etapai (msdyn\_contractlinescheduleofvalues)
        - „Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)
        - Projekto sąskaitų faktūrų pasiūlymų V2 (SF)

Dabar etapai yra perkelti, o sistema parengta atlikti kitus visiško perkėlimo veiklos veiksmus.
