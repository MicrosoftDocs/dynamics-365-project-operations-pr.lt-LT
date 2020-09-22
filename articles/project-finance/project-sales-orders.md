---
title: Laiko ir medžiagų projektų pardavimo užsakymai
description: Šioje temoje paaiškinama, kaip kurti laiko ir medžiagų projektų projektu pagrįstus pardavimo užsakymus.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753650"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Laiko ir medžiagų projektų pardavimo užsakymai

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Šioje temoje aprašoma, kaip sukurti projekto pardavimo užsakymą. Pardavimo užsakymus galima kurti tik projektuose, kurių tipas yra **laikas ir medžiagos**.

Jei su laiko ir medžiagų projektu susijusioje projekto sutartyje yra keli finansavimo šaltiniai, turite įjungti parametrą **Leisti pardavimo užsakymus projektuose su keliais finansavimo šaltiniais** puslapyje **Projektų valdymas ir apskaitos parametrai**. 

> [!NOTE]
> - Galima naudoti projektų pardavimo užsakymų su keliais finansavimo šaltiniais palaikymą pradedant nuo 10.0.2 programos leidimo ir naujesnių versijų.
> - Parametras, kuriuo įgalinamas projektų pardavimo užsakymų su keliais finansavimo šaltiniais palaikymas, bus pašalintas 2020 m. balandžio mėn. leidimo bangos metu, po kurios ši funkcija bus įgalinta visada.

Projektu pagrįstus pardavimo užsakymus galite kurti toliau pateikiamais dviem būdais.

- Pereikite prie paties projekto. Veiksmų srityje pasirinkite **Valdyti > Elementų užduotys > Pardavimo užsakymas**. Projekto informacija pagal numatytuosius parametrus bus nustatyta pagal projekto pardavimo užsakymą. Jei projekto sutartyje yra daugiau nei vienas finansavimo šaltinis, turėsite pasirinkti finansavimo šaltinį, kad nustatytumėte pardavimo užsakymo klientą. Jei projekte yra tik vienas finansavimo šaltinis, klientas bus nustatytas automatiškai.
- Įeikite į sąrašo puslapį **Visi pardavimo užsakymai** ir sukurkite naują pardavimo užsakymą. Turėsite pasirinkti pardavimo užsakymo projektą. Pasirinkus projektą, klientas bus nustatomas pagal finansavimo šaltinį, arba reikės pasirinkti finansavimo šaltinį, jei projekto sutartyje nurodyti keli finansavimo šaltiniai.

