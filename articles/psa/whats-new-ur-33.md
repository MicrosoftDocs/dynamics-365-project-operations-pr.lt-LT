---
title: Kas nauja arba pakeista „Project Service Automation“ V3 33 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 33 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334572"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 33 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Ji suderinama su „Dynamics 365 9.x“. Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 33 atnaujintame leidime. Šios komponavimo versijos numeris yra V3.10.54.98 ir ji visuotinai pasiekiama naudojant savaimini naujinimą 2021 m. liepos mėn.

## <a name="update-release-33"></a>33 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

Buvo pataisytos šios problemos:

- Pateikus galima redaguoti du užrakintus laukus – **msdyn_description** ir **msdyn_externaldescription**.
- Jei sukuriamos išlaidos, kurios nėra susijusios su projektu, pateikiamas klaidos pranešimas.
- Sukūrus laiko įrašą, išteklių vaidmuo pagal numatytuosius parametrus nustatomas kaip neaktyvus.
- Su atšauktomis ir panaikintomis išlaidomis susietos žurnalo eilutės nėra panaikinamos.
- **Laiko įrašo sparčiojo kūrimo formoje** atnaujinkite rodinį **Projekto užduočių sąrašas**, kad pagal numatytuosius parametrus rodomą datą pakeistumėte į užduoties pradžios datą.
- Kai sukuriate laiko įrašą rezervuojamojo ištekliaus skirtuke **Susiję**, netinkamai sukuriamas prisijungusio vartotojo, o ne pirminio rezervuojamojo ištekliaus laiko įrašas.
- Nauji laukai įtraukiami į dialogo langą **Masinio patvirtinimo MDD**.

**Projekto planavimas**

Buvo pataisytos šios problemos:
- Kai darbo valandų šablonai taikomi su sudėtingais kalendoriais, sulėtėja projektų kūrimo našumas.
- Kai pradžios data yra vėlesnė nei pabaigos data, kopijavimo projekto šablone rodoma klaida dėl kiekvieno lauko laiko komponento skirtumų.

**Išteklių valdymas**

Buvo pataisytos šios problemos:
- Išteklių naudojimo užklausoje naudojamas netinkamas parametras, o dėl XML tinklelyje **Išteklių naudojimas** gaunami neteisingi rezultatai.
- Patvirtinimo lange **Rezervacijų pratęsimas** rodoma neteisinga rezervacijų pabaigos data.

**Pardavimas**

Buvo pataisytos šios problemos:
- Jei sukuriama kategorijos kaina su trūkstamomis reikšmėmis, pateikiamas klaidos pranešimas.
- Jei sutarties eilutės etapas sukuriamas be užsakymo eilutės, pateikiamas klaidos pranešimas.
