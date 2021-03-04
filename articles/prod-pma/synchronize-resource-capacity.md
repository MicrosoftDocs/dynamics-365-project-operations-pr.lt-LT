---
title: Išteklių pajėgumo sinchronizavimas
description: Šioje temoje pateikta informacija, kaip sinchronizuoti ištekliaus pajėgumą kalendoriuose ir projektuose.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080814"
---
# <a name="synchronize-resource-capacity"></a>Išteklių pajėgumo sinchronizavimas

[!include [banner](../includes/banner.md)]

Išteklių sinchronizavimo procesai padeda užtikrinti, kad kalendoriaus ir pagrindinio kalendoriaus informacija naudojama planuojant projekto išteklius. Jei pakeičiamas kalendorius, procesai atlieka reikiamus projekto išteklių planavimo atnaujinimus. Procesai taip pat padeda gerinti efektyvumą, nes kalendoriaus išteklių informacija sinchronizuojama iš anksto. Todėl išteklių planavimo informacija atnaujinama greičiau. Rekomenduojame planuoti procesus kaip paketą, o ne po vieną. Priešingu atveju kyla pavojus, kad kas nors pamirš įtraukti paskutinį kartą sinchronizuotos informacijos datas. Jei paskutinį kartą nurodytos datos nebus naudojamos, sinchronizuojant datas gali atsirasti tarpų.

![Kalendoriaus sinchronizavimas](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Išteklių pajėgumų sumavimų sinchronizavimas

Sinchronizavimo procesas skirtas visai išteklių kalendoriaus informacijai sinchronizuoti. Į šią informacija įtraukta pagrindinio kalendoriaus informacija apie visus projekto išteklių kalendoriaus pajėgumo lentelės pakeitimus. Jei į projektą įtraukiami nauji ištekliai, sinchronizavimas padeda užtikrinti, kad atnaujinta kalendoriaus informacija yra pasiekiama. Šis sinchronizavimas gali būti atliktas bet kuriuo metu.

Rekomenduojame naudoti paketą. Šios parinktys yra pasiekiamos pajėgumų rezervavimų sinchronizavimo metu.

1. Pasirinkite **Projektų valdymas ir apskaita** &gt; **Periodinis** &gt; **Pajėgumų sinchronizavimas** &gt; **Išteklių pajėgumų sumavimų sinchronizavimas**.
2. Nustatykite parinktis toliau pateiktoje lentelėje.

    | Parinktis      | Aprašo |
    |-------------|-------------|
    | Laikotarpio kodas | Arba pasirinkite didžiosios knygos datų intervalo kodą, kad nustatytumėte išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios ir pabaigos datas. |
    | Pradžios data  | Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios datą. |
    | Pabaigos data    | Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pabaigos datą. |

[![Sinchronizavimo procesas](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]