---
title: Kas nauja arba pakeista „Project Service Automation“ V3 34 atnaujintame leidime
description: Šiame straipsnyje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 34 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928672"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 34 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Ji suderinama su „Dynamics 365 9.x“. Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šiame straipsnyje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 34 atnaujintame leidime. Šios komponavimo versijos numeris yra V3.10.55.38 ir ji visuotinai pasiekiama naudojant savaimini naujinimą 2021 m. liepos mėn.

## <a name="update-release-34"></a>34 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos
Buvo pataisytos tolesnės problemos.

**Bendroji informacija**

- Leidėjo valdomi naujiniai neaktyvina naujos modernios patvirtinimo darbo eigos.
- Pagrindiniame puslapyje **Patvirtinimo rinkinys** nėra atributų **Tikslinė būsena** ir **Veiksmo tipas**.

**Laikas ir išlaidos**

- Nepavyksta patvirtinti atšaukimo užklausos naudojant modernią patvirtinimo eigą.
- Nepavyksta nukopijuoti įrašų savaičių laikų, kai kopijuojami įrašai, nesusiję su prisijungusiu vartotoju.

**Projekto planavimas**

- Išteklių priskyrimo kontūrai sugadinami, kai importuojama iš „Microsoft Project‟ darbalaukio priedo.

**Išteklių valdymas**

- Kai publikuojate projektą iš „Microsoft Project” darbalaukio kliento priedo, pasikeičia esamų reikalavimų pabaigos data.
- Rezervavimų išplėtimo patvirtinimo dialogo lange dešimtainių dalių tikslumas viršija du skaitmenis po kablelio.

**Pardavimas**

- Kai į projekto sutartį įtraukiate produktu pagrįstą eilutę su esamu produktu, rodoma išimtis **Raktas nerastas žodyne**.
- Nepavyksta patvirtinti galimų klientų, kai užsakymo tipas susietas iš galimo kliento į galimybę.
