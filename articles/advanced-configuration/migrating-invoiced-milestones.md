---
title: Perkelti visiškai išrašytus atsiskaitymo etapus, kuriems išrašyta SF
description: Šiame straipsnyje paaiškinama, kaip perkelti fiksuotos kainos atsiskaitymo etapus, kuriems klientui buvo išrašyta SF už atviras projekto sutartis iki įsigaliojimo datos.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d7bb3dbb5acd9be447c405ec17f18d00c500f655
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912250"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Perkelti visiškai išrašytus atsiskaitymo etapus, kuriems išrašyta SF

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

## <a name="scenario"></a>Scenarijus

Contoso tiesiogiai bendradarbiauja su "Microsoft" Dynamics 365 Project Operations dėl išteklių / ne atsargų scenarijų. Vykdydama mažinimo veiklą, įgyvendinimo grupė turi perkelti atviras projektų sutartis iš senosios sistemos. Kai kuriose projekto sutartyse yra sutarties eilučių, kuriose naudojamas fiksuotos kainos atsiskaitymo metodas ir kurioms galutiniam pirkėjui jau iš dalies išrašyta SF. Diegimo komanda turi perkelti šiuos atsiskaitymo etapus kaip **užregistruotą** kliento SF, nes jie turi būti įtraukti į bendrą sutarties vertę įplaukų pripažinimo tikslais. Tačiau klientų balansams gautinose sumose ir DK neturi būti daromas poveikis.

## <a name="solution"></a>Sprendimas

### <a name="prerequisites"></a>Būtinosios sąlygos

- Dynamics 365 Finance 10.0.24 ar naujesnė versija turi būti įrengti.
- Aplinka, kurioje bus atlikti perkėlimo etapai, turi būti techninės priežiūros režimu. Perkeliant etapus neturėtų būti vykdoma jokia kita veikla.
- Perkėlimo veiksmai turi būti atliekami tiksliai taip, kaip aprašyta čia, ir gali būti naudojami tik pjovimo veiklai. "Microsoft" nepalaiko jokio kito šios galimybės naudojimo.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Kurti "Project Operations" integravimo sutarties eilučių etapų dvigubo rašymo žemėlapio ribinę versiją 

1. Įsitikinkite, kad objekto **Projekto operacijos integravimo sutarties eilučių etapų tikslinis** susiejimas yra atnaujintas. 

    1. Programoje "Finance" eikite į **Duomenų valdymo** \> **duomenų objektus** ir pasirinkite objektą **"Project Operations" integravimo sutarties eilutės etapai.** 
    2. Pasirinkite **Modifikuoti tikslinius susiejimus**. 
    3. **Puslapyje Susieti išdėstymą pagal paskirtį** pasirinkite **Generuoti susiejimą**, tada patvirtinkite, kad norite generuoti susiejimą.

2. Sustabdyti ir atnaujinti **projekto operacijų integravimo sutarties eilučių etapų** (**msdyn\_ contractlineschedule ofvalues**) dvigubo rašymo žemėlapį. 

    1. Eikite į **Duomenų valdymas** \> **Dvigubas rašymas**, pasirinkite žemėlapį ir atidarykite išsamią jo informaciją. 
    2. Pasirinkite **Sustabdyti** ir palaukite, kol sistema sustabdys žemėlapį. 
    3. Pasirinkite **Atnaujinti lenteles**.

3. Įtraukite operacijos būsenos susiejimą.

    1. Pasirinkite **Įtraukti susiejimą**.
    2. Naujoje eilutėje, stulpelyje **Finansų ir operacijų programos**, pasirinkite **lauką TRANSSTATUS \[TRANSSTATUS\]**.
    3. Stulpelyje **Microsoft Dataverse** pasirinkite **msdyn\_ invoicestatus \[SF\]** būseną.
    4. Stulpelyje Žemėlapio **tipas** pasirinkite rodyklę dešinėn (**\>**).
    5. Pasirodžiusio dialogo lango lauke Sinchronizavimo kryptis **pasirinkite** į "Finance and Operations" programas **Dataverse.**
    6. Pasirinkite **Įtraukti transformaciją**.
    7. Lauke Transformuoti tipą **pasirinkite** **ValueMap**.
    8. Pasirinkite **Įtraukti vertės susiejimą**.
    9. Kairiajame lauke įveskite **4**. Dešiniajame lauke įveskite **192350001**. 
    10. Pasirinkite **Įrašyti**, tada uždarykite dialogo langą.

4. Pasirinkite **Įrašyti, kad** įrašytumėte dvigubo rašymo žemėlapio versiją. 
5. Srities **Įtraukti lentelę** lauke Publisher **pasirinkite** **Numatytasis leidėjas**.
6. Lauke **Versija** įveskite versiją.
7. Lauke **Aprašas** įveskite pastabą apie šią iškirptąją žemėlapio versiją. 
8. Pasirinkite **Įrašyti**.
9. Pradėkite žemėlapį.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Perkelti etapus, kuriems išrašyta SF, Dataverse į aplinką

1. Aplinkoje Projekto operacijos Dataverse sukurkite etapus, kurių SF būsena yra **Paruošta sf išrašymui**. Šiuo metu nekelkite jokių etapų, kuriems nebuvo išrašyta SF.

    > [!NOTE]
    > Prieš perkeldami atsiskaitymo etapus, įsitikinkite, kad su projekto sutarties eilute susijusios finansinės dimensijos nustatytos taip, kaip tikėtasi. Pasibaigus perkėlimui, finansinių dimensijų redaguoti negalima.

2. Perkėlę visus etapus, sustabdykite šiuos dvigubo rašymo žemėlapius:

    - Projekto operacijų integravimo sutarčių eilučių orientyrai (msdyn\_ sutarčių eilutės, apimančios vertes)
    - „Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)
    - Projekto sąskaitų faktūrų pasiūlymų V2 (SF)

    Norėdami sustabdyti žemėlapius, atlikite šiuos veiksmus:

    1. Programoje "Finance" eikite į **Duomenų valdymas** \> **Dvigubas rašymas**, pasirinkite žemėlapį ir atidarykite išsamią jo informaciją.
    2. Pasirinkite **Sustabdyti** ir palaukite, kol sistema sustabdys žemėlapį.

3. Aplinkoje Projekto operacijos Dataverse kurkite ir patvirtinkite atsiskaitymo etapų pro forma SF. 

    1. Svetainės struktūroje eikite į projekto sutartis, pasirinkite sutartis, tada pasirinkite **Kurti SF**.
    2. Sukūrę sąskaitas faktūras, atidarykite jas **svetainės struktūros meniu Sąskaitos** faktūros, tada pasirinkite **Patvirtinti**.

    Šis veiksmas sukuria reikiamus įrašus Dataverse aplinkoje. Tačiau tai neturi įtakos finansams ir gautinoms sumoms, nes anksčiau išvardyti dvigubo rašymo žemėlapiai buvo sustabdyti.

4. Patvirtinus visas pro forma sąskaitas faktūras, grąžinkite visus dvigubo rašymo žemėlapius į pradinę būseną.

    1. Atnaujinkite projekto operacijų integravimo sutarties eilučių etapų **(** msdyn **contractlineschedule ofvalues\_) dvigubo rašymo žemėlapio versiją** atgal į originalą. 
    2. Žemėlapių sąraše pasirinkite dvigubo rašymo žemėlapį, pasirinkite **Lentelės schemos versiją**, tada pasirinkite pradinę lentelės schemos versiją.
    3. Pasirinkite **Įrašyti**.
    4. Iš naujo paleiskite šiuos dvigubo rašymo žemėlapius:

        - Projekto operacijų integravimo sutarčių eilučių orientyrai (msdyn\_ sutarčių eilutės, apimančios vertes)
        - „Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)
        - Projekto sąskaitų faktūrų pasiūlymų V2 (SF)

Etapai dabar perkelti, o sistema yra pasirengusi tolesniems pjovimo veiklos etapams.
