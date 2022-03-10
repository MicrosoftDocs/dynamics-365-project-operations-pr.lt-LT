---
title: Kas nauja arba pakeista „Project Service Automation“ V3 29 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 29 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 87f10d793f9edc055444a3cecea9ea709c1fd7ff7213d6cfaf6b3cbe83a6a5a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6985106"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 29 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 29 atnaujintame leidime. Šios versijos numeris yra V3.10.47.7 ir ji visuotinai pasiekiama įdiegiant savaiminį 2021 m. vasario mėn. naujinimą.

## <a name="update-release-29"></a>29 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

Buvo pataisytos šios problemos:

- Vartotojams laiko įvedimo tinklelyje nemato darbo valandų, kai jie prisijungia ne darbo dienomis.
- Patvirtintus išlaidų įrašus tinklelyje galima redaguoti.

**Projektų valdymas**

Buvo pataisytos šios problemos:

- Trūksta tikrinimo logikos, užtikrinančios, kad išteklių priskyrimo pastangų valandos negali būti neigiamos.
- Pasirinktinis veiksmas **AssignResourcesForTask** atnaujina visus laukus, o ne tik pakeistus laukus.
- Kopijuojant projektą aplinkoje su priedais arba darbo eigomis, kurios yra užregistruotos įvykyje **CreateProject**, atributas **msdyn_bulkgenerationstatus** neatnaujinamas, jei **CopyWBSToProject** veiksmas nepavyks.
- Kai išplečiate projekto kalendorių, darbo dienos nerūšiuojamos didėjimo tvarka, todėl nepavyksta atnaujinti kai kurių projekto užduočių.
- Keičiant esamo projekto projekto vadovą paleidžiama numatytoji organizacijos vieneto logika.

**Pardavimas**

Buvo pataisytos šios problemos:

- Puslapio **Sutartis** skirtuko **Sutaties efektyvumas** veiksmas nepavyksta inicijavimo metu, kai nėra sutarties eilučių.