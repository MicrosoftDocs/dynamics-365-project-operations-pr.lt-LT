---
title: Projekto pirkimo užsakymai
description: Šiame straipsnyje aprašomi įvairūs būdai, kuriuos galite naudoti, kad sukurtumėte projekto pirkimo užsakymus. Naudojamas būdas priklauso nuo pirkimo užsakymo tikslo ir nuo to, kada nupirktos prekės yra panaudojamos ir priskirtos projektui.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5de28f3844b802a980c811411cae75549c697538f89e8c3d2495ea171a188524
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009001"
---
# <a name="purchase-orders-for-a-project"></a>Projekto pirkimo užsakymai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi įvairūs būdai, kuriuos galite naudoti, kad sukurtumėte projekto pirkimo užsakymus. Naudojamas būdas priklauso nuo pirkimo užsakymo tikslo ir nuo to, kada nupirktos prekės yra panaudojamos ir priskirtos projektui.

### <a name="methods-for-creating-a-purchase-order"></a>Pirkimo užsakymo kūrimo būdai

Galite naudoti vieną iš toliau pateikiamų būdų, kad sukurtumėte pirkimo užsakymą projekto valdymo ir apskaitos srityje. Pirkimo užsakymo tikslas lemia, kada pirkimo užsakymas bus panaudotas, o elementai priskirti projektui.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metodas</th>
<th>Tikslas</th>
<th>Prekių sunaudojimas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sukurkite pirkimo užsakymą tiesiogiai projekte.</td>
<td>Naudokite šį būdą, jei norite iš išorinio tiekėjo įsigyti prekių, kurias naudosite projekte. Pirkimo užsakymą galite sukurti dviem būdais.
<ul>
<li>Iš paties projekto. Šiuo atveju pirkimo užsakymo projektas jau yra nustatytas.</li>
<li>Pereidami į projekto pirkimo užsakymą. Turite pasirinkti ir tiekėją, ir projektą, kuriems kursite pirkimo užsakymą.</li>
</ul></td>
<td>Prekės yra sunaudojamos, kai atnaujinama tiekėjo SF.</td>
</tr>
<tr class="even">
<td>Sukurkite pirkimo užsakymą iš pardavimo užsakymo.</td>
<td>Naudokite šį būdą, pirkdami prekes, kai kuriate pardavimo užsakymą projekte.</td>
<td>Prekės yra sunaudojamos, kai klientui išrašoma SF už pardavimo užsakymą.</td>
</tr>
<tr class="odd">
<td>Sukurkite pirkimo užsakymą iš prekės poreikio.</td>
<td>Naudokite šį būdą, pirkdami prekes, kai kuriate elemento reikalavimą projekte.</td>
<td>Prekės ura sunaudojamos, kai atnaujinamas prekės poreikio važtaraštis.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Kai atnaujinsite tiekėjo sąskaitą faktūrą arba važtaraštį, būsite paraginti atnaujinti elemento reikalavimo važtaraštį.

Norėdami gauti daugiau informacijos žr. [Pirkimo užsakymo elementų gavimas iš elementų reikalavimo](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]