---
title: Laiko ir medžiagų projektų pardavimo užsakymai
description: Šioje temoje paaiškinama, kaip kurti laiko ir medžiagų projektų projektu pagrįstus pardavimo užsakymus.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080821"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Laiko ir medžiagų projektų pardavimo užsakymai

[!include[banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti projekto pardavimo užsakymą. Pardavimo užsakymus galima kurti tik projektuose, kurių tipas yra **laikas ir medžiagos**.

Jei su laiko ir medžiagų projektu susijusioje projekto sutartyje yra keli finansavimo šaltiniai, turite įjungti parametrą **Leisti pardavimo užsakymus projektuose su keliais finansavimo šaltiniais** puslapyje **Projektų valdymas ir apskaitos parametrai**. 

> [!NOTE]
> - Galima naudoti projektų pardavimo užsakymų su keliais finansavimo šaltiniais palaikymą pradedant nuo 10.0.2 programos leidimo ir naujesnių versijų.
> - Parametras, kuriuo įgalinamas projektų pardavimo užsakymų su keliais finansavimo šaltiniais palaikymas, bus pašalintas 2020 m. balandžio mėn. leidimo bangos metu, po kurios ši funkcija bus įgalinta visada.

Projektu pagrįstus pardavimo užsakymus galite kurti toliau pateikiamais dviem būdais.

- Pereikite prie paties projekto. Veiksmų srityje pasirinkite **Valdyti > Elementų užduotys > Pardavimo užsakymas**. Projekto informacija pagal numatytuosius parametrus bus nustatyta pagal projekto pardavimo užsakymą. Jei projekto sutartyje yra daugiau nei vienas finansavimo šaltinis, turėsite pasirinkti finansavimo šaltinį, kad nustatytumėte pardavimo užsakymo klientą. Jei projekte yra tik vienas finansavimo šaltinis, klientas bus nustatytas automatiškai.
- Įeikite į sąrašo puslapį **Visi pardavimo užsakymai** ir sukurkite naują pardavimo užsakymą. Turėsite pasirinkti pardavimo užsakymo projektą. Pasirinkus projektą, klientas bus nustatomas pagal finansavimo šaltinį, arba reikės pasirinkti finansavimo šaltinį, jei projekto sutartyje nurodyti keli finansavimo šaltiniai.

