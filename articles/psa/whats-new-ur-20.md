---
title: Kas nauja arba pakeista „Project Service Automation“ V3 20 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 20 naujinimo leidime
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147123"
---
# <a name="project-service-automation-update-release-20-v3"></a>„Project Service Automation“ V3 20 naujinimo leidimas

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 20 atnaujintame leidime. Šios versijos komponavimo versijos numeris yra V 3.10.31.37 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. birželio mėn.

## <a name="update-release-20"></a>20 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Projektų valdymas**

Buvo pataisytos šios problemos:

- Projekto komandos narių importavimo metu naudojant paskirstymo metodą, kuriam reikalingos valandos, pateikiamas neaiškus klaidos pranešimas, jei nurodytos valandos yra nulis.
- Vartotojams nurodoma neteisinga klaida, kai projekto užduoties lauke **Aprašas** įvedamas didžiausias simbolių skaičius.
- Puslapyje **„Microsoft Dynamics 365 Project Service Automation” papildinio atsisiuntimas** nukreipiama į anglišką atsisiuntimo puslapį, kai vartotojo kalbos parametrai nustatyti kaip japonų kalba.
- Įvykus serverio klaidai, kartais lieka sinchronizavimo žyma skirtuke **Grafikas**, esančiame formoje **Projektai**.
- Kai užduotis modifikuojama, į serverį siunčiami nereikalingi užduočių naujinimai.

**„Sales“**

Buvo pataisytos šios problemos:

- Formoje **Sutartis** dukart spustelėjus **Kurti sąskaitą faktūrą** sukuriamos dvi vieno faktinių duomenų įrašo sąskaitos faktūros.
- Naršyklės „Internet Explorer 11” vartotojai negali kurti išlaidų įrašų.
- Išlaidų anuliavimas ir pardavimo faktinių duomenų, už kuriuos nebuvo išrašyta sąskaita, anuliavimas nesusieti.
- Mygtuku **Atnaujinti faktinius duomenis**, esančiu formoje **Projektas**, neatnaujinamos **Užduoties faktinės valandos**.
- Priedu **PreValidateProjectTeamMemberCreate** galima kurti pasikartojančių bendrųjų rezervuojamų išteklių, kai atributas **msdyn_isgenericresourceprojectscoped** nustatytas kaip **Klaidingas**.
- Parinktimi **Perskaičiuoti** išvalomos apmokestinamos produktu pagrįstos pasiūlymo eilutės išsamios informacijos ir sutarties eilutės išsamios informacijos išlaidos.
- Konkrečiose situacijose priede **PostEstimateLineUpdate** rodoma neapibrėžtos nuorodos išimties klaida.
- Laiko fazės trukmė, esanti **pelningumo analizės diagramoje**, nedera su fiksuotos kainos pasiūlymo eilutės išsamios informacijos apie pasiūlymą trukme.
- Vienetų ir vienetų grupių reikšmės išlaidų kategorijose, esančiose **Sutarties eilutės išsami informacija** ir **Pasiūlymo eilutės išsami informacija** formose, nurodomos neteisingai.
- Sąrašuose **Organizacijos vieneto savikaina** leidžiami datos efektyvumo persidengimai.
- Vartotojams neleidžiama keisti **OrgUnit**, kai užsakymo tipas nesusijęs su darbu, nes dėl jo bus pateikiama neapibrėžtos nuorodos išimties klaida.
- Bandant pereiti iš formos **Pasiūlymo eilutės išsami informacija**, atgal į skirtuką **Pasiūlymas**, forma atnaujinama ir rodomas skirtukas **Suvestinė**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]