---
title: Kas nauja arba pakeista „Project Service Automation“ V3 20 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 20 naujinimo leidime
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080785"
---
# <a name="project-service-automation-update-release-20-v3"></a>„Project Service Automation“ V3 20 naujinimo leidimas

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 20 atnaujintame leidime. Šios versijos komponavimo versijos numeris yra V 3.10.31.37 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. birželio mėn.

## <a name="update-release-20"></a>20 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Projektų valdymas**

Buvo pataisytos šios problemos:

- Projekto komandos narių importavimo metu naudojant paskirstymo metodą, kuriam reikalingos valandos, pateikiamas neaiškus klaidos pranešimas, jei nurodytos valandos yra nulis.
- Vartotojams nurodoma neteisinga klaida, kai projekto užduoties lauke **Aprašas** įvedamas didžiausias simbolių skaičius.
- Puslapyje **„Microsoft Dynamics 365 Project Service Automation” papildinio atsisiuntimas** nukreipiama į anglišką atsisiuntimo puslapį, kai vartotojo kalbos parametrai nustatyti kaip japonų kalba.
- Įvykus serverio klaidai, kartais lieka sinchronizavimo žyma skirtuke **Grafikas** , esančiame formoje **Projektai**.
- Kai užduotis modifikuojama, į serverį siunčiami nereikalingi užduočių naujinimai.

**„Sales“**

Buvo pataisytos šios problemos:

- Formoje **Sutartis** dukart spustelėjus **Kurti sąskaitą faktūrą** sukuriamos dvi vieno faktinių duomenų įrašo sąskaitos faktūros.
- Naršyklės „Internet Explorer 11” vartotojai negali kurti išlaidų įrašų.
- Išlaidų anuliavimas ir pardavimo faktinių duomenų, už kuriuos nebuvo išrašyta sąskaita, anuliavimas nesusieti.
- Mygtuku **Atnaujinti faktinius duomenis** , esančiu formoje **Projektas** , neatnaujinamos **Užduoties faktinės valandos**.
- Priedu **PreValidateProjectTeamMemberCreate** galima kurti pasikartojančių bendrųjų rezervuojamų išteklių, kai atributas **msdyn_isgenericresourceprojectscoped** nustatytas kaip **Klaidingas**.
- Parinktimi **Perskaičiuoti** išvalomos apmokestinamos produktu pagrįstos pasiūlymo eilutės išsamios informacijos ir sutarties eilutės išsamios informacijos išlaidos.
- Konkrečiose situacijose priede **PostEstimateLineUpdate** rodoma neapibrėžtos nuorodos išimties klaida.
- Laiko fazės trukmė, esanti **pelningumo analizės diagramoje** , nedera su fiksuotos kainos pasiūlymo eilutės išsamios informacijos apie pasiūlymą trukme.
- Vienetų ir vienetų grupių reikšmės išlaidų kategorijose, esančiose **Sutarties eilutės išsami informacija** ir **Pasiūlymo eilutės išsami informacija** formose, nurodomos neteisingai.
- Sąrašuose **Organizacijos vieneto savikaina** leidžiami datos efektyvumo persidengimai.
- Vartotojams neleidžiama keisti **OrgUnit** , kai užsakymo tipas nesusijęs su darbu, nes dėl jo bus pateikiama neapibrėžtos nuorodos išimties klaida.
- Bandant pereiti iš formos **Pasiūlymo eilutės išsami informacija** , atgal į skirtuką **Pasiūlymas** , forma atnaujinama ir rodomas skirtukas **Suvestinė**.
