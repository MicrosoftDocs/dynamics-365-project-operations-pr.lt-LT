---
title: Kas nauja arba pakeista „Project Service Automation“ V3 23 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 23 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150048"
---
# <a name="project-service-automation-update-release-23-v3"></a>„Project Service Automation“ V3 23 naujinimo leidimas

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 23 atnaujintame leidime. Ši versija turi naują komponavimo versijos numerį V 3.10.34.30 ir ją galima pasiekti per 2020 m. rugpjūčio mėn. automatinį naujinimą.

## <a name="update-release-23"></a>23 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

Buvo pataisytos šios problemos:
- Tvarkykite kraštutinį atvejį **Projekto komandos nario ištrynimo** lauke, norėdami pateikti prasmingą išimtį.
- Importavimo rezultatų priskyrimas tuščiame pašalinimo ekrane.

**Išteklių valdymas**

Buvo pataisytos šios problemos:

- **Ištekliaus panaudojimo tinklelio ištekliaus kortelė** rodo neteisingus duomenis, kai laiko mastelis yra didesnis nei penkios dienos.
- Kai klientai sukuria rezervuojamą išteklių, priedas negali automatiškai su pertraukomis pridėti ištekliaus prie „Microsoft Office 365“ grupės.
- **Susitaikymo** rodinys neteisingai pateikia rankinį kontūrą **savaitės** arba **mėnesio** rodinyje.

**Projektų valdymas**

Buvo pataisytos šios problemos:

- Pernelyg didelis **RetrieveMultiple for usersettings** objektų skaičius blogina projektų patvirtinimo ir kitų operacijų atlikimo rezultatus.
- **Užduočių planavimo** tinklelio ištekliaus peržiūra yra ribojama iki penkių komandos narių iš projekto komandos. 
- **Užduočių planavimo** tinklelio ištekliaus peržiūra nefiltruoja neaktyvių išteklių.
- Rankinis režimas neveikia kaip numatyta projekto planavimo darbo paskirstymo struktūroje.
- **Užduočių planavimo** tinklelis rodo **neaktyvias transakcijų kategorijas**.
- **Išteklių priskyrimo** tinklelis apvalina neteisingai, kai užduotis turi kelis priskyrimus.
- Reikšmių apvalinimas skiriasi tarp suplanuotų išlaidų ir tikrosios vienos užduoties kainos.

**„Sales“**

Buvo pataisytos šios problemos:

- Dukart paspaudus **Sukelti visas transakcijų kategorijas**, sukuriamos kelios eilutės.


[!INCLUDE[footer-include](../includes/footer-banner.md)]