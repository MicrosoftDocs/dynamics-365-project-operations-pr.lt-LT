---
title: Kas nauja arba pakeista „Project Service Automation“ V3 15 atnaujintame leidime
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 15 atnaujintame leidime V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 2112e70d7359e7f30725ef3069a18570da651c06
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119923"
---
# <a name="project-service-automation-update-release-15-v3"></a>„Project Service Automation“ V3 15 naujinimo leidimas

Džiaugiamės galėdami pranešti apie naujausią Dynamics 365 Project Service Automation (PSA) programos naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti PSA V3 15 atnaujintame leidime. Ši versija turi naują komponavimo versijos numerį V3.10.5.28 ir ją galima pasiekti per 2020 m. sausio mėn. automatinį naujinimą.

## <a name="update-release-15"></a>15 atnaujintas leidimas 

### <a name="enhancements"></a>Patobulinimai

- Projektų valdymas

### <a name="bug-fixes"></a>Ištaisytos klaidos

- Laikas ir išlaidos

  - Sutaisyta: pridėtas įkėlimo klaidos tvarkymas suderinimo rodinyje.
  - Sutaisyta: projekto išteklių priegloba: pervadinta **Suma**, siekiant sumažinti neaiškumą.
  - Sutaisyta: pakoreguotas rodinys **Kopijuoti laiko įrašo stulpelius**, kad būtų įtrauktas tipas.
  - Sutaisyta: laiko įrašo trukmės redagavimas tinklelio rodinyje naudojant dešimtainius skaičius sukelia kai kurių skaičių nežinomas klaidas.

- Projektų valdymas

  - Sutaisyta: išskleidžiamasis **Naudoti sekimo rodinyje** dabar išplečiamas pagal parinkčių plotį.
  - Sutaisyta: tvarkant projektus +13 laiko juostose, užduočių skaičiavimuose gali būti netikslių rezultatų.
  - Sutaisyta: **Komandos nario pabaigos laikas** pakoreguotas naudojant 24 val. kalendorių.
  - Sutaisyta: iš naujo suaktyvintas **BPF** **msdyn_project** pagrindinėje formoje.
  - Sutaisyta: skaičiuojant priskyrimus daugiau neignoruojama viena diena.
  - Sutaisyta: nauja pranešimų juosta pridėta prie projekto formos, kai laiko zona skiriasi nuo vartotojo ir projekto.

- Sales

  - Sutaisyta: išlaidų skaičiavimo kategorijos apžvalgą galima naudoti norint filtruoti dublikatus.
  - Sutaisyta: kode **PluginDomain.ExecuteInTryCatchBlock(..)** daugiau neslepiama išimties kilmė.
  - Sutaisyta: daugiau negaunamas klaidos pranešimas **Projekto apžvalgos** **Pasiūlymo eilutės** formoje, kai yra daugiau nei 1000 projektų.
  - Sutaisyta: **Skaičiavimų** tinklelyje, skirtame darbo įverčiams ir išlaidų sąmatoms, dabar rodomas teisingas valiutos simbolis.
  - Sutaisyta: kai organizacija atnaujina PSA iš 14 atnaujinto leidimo į 15 atnaujintą leidimą, skirtukas **Grafikas** formoje **Projektas** daugiau nerodomas kaip tuščias.