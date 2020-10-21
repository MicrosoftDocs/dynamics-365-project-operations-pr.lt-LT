---
title: Išlaidų valdymo darbo eigų nustatymas
description: Galite nustatyti darbo eigos procesą, naudojamą kelionių ir išlaidų dokumentų peržiūrai ir tvirtinimui.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dfc5945f32bb8d4073fc31499979ba279fef66a4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896561"
---
# <a name="set-up-workflows-for-expense-management"></a>Išlaidų valdymo darbo eigų nustatymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Galite nustatyti darbo eigos procesą kelionių ir išlaidų dokumentų peržiūrai ir tvirtinimui. Galite apibrėžti išlaidų ataskaitų, kelionių paraiškų ir grynųjų pinigų išankstinių užklausų darbo eigas.

Darbo eiga yra verslo procesų ir apibrėžia, kaip dokumentas teka sistema. Darbo eiga taip pat nurodo, kas turi atlikti užduotį arba patvirtinti dokumentą. Jūsų organizacijoje yra keli darbo eigos sistemos naudojimo pranašumai:

- **Nuoseklūs procesai** – galite apibrėžti tam tikrų dokumentų, pvz., pirkimo paraiškų ir išlaidų ataskaitų, patvirtinimo procesą. Darbo eigos sistemos naudojimas padeda užtikrinti, kad dokumentai būtų apdorojami ir tvirtinami nuosekliai bei efektyviai.
- **Proceso matomumas** – galite sekti tam tikro darbo eigos egzemplioriaus būseną, retrospektyvą ir našumą. Taip galėsite nustatyti, ar darbo eiga turi būti keičiama efektyvumui padidinti.
- **Centralizuotas darbo sąrašas** – vartotojai gali peržiūrėti centralizuotą darbo sąrašą, kad galėtų peržiūrėti jiems priskirtas darbo eigos užduotis ir patvirtinimus. 

## <a name="workflow-types"></a>Darbo eigos tipai

Šioje lentelėje išvardyti darbo eigų tipai, kuriuos galite sukurti **Išlaidų valdyme**.


|              <strong>Tipas</strong>              |                   <strong>Naudokite šį tipą, kad</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Išlaidų ataskaitos automatinis patvirtinimas</strong> |            Kurti išlaidų ataskaitų patvirtinimo darbo eigas.             |
|  <strong>Išlaidų ataskaitų automatinis publikavimas</strong>   |        Kurti išlaidų ataskaitų automatinio publikavimo darbo eigas.        |
|       <strong>Išlaidų eilutės elementas</strong>        |     Kurti išlaidų ataskaitų eilučių elementų patvirtinimo darbo eigas.      |
| <strong>Išlaidų eilutės elemento automatinis publikavimas</strong> | Kurti išlaidų ataskaitų eilučių elementų automatinio publikavimo darbo eigas. |
|       <strong>Kelionės paraiška</strong>       |          Kurkite kelionių paraiškų patvirtinimo darbo eigas.           |
|      <strong>Avansinis mokėjimo užklausa</strong>      |         Grynųjų pinigų avanso užklausų patvirtinimo darbo eigų kūrimas.          |
|        <strong>PVM mokesčių grąžinimas</strong>        | Kurti pridėtinės vertės mokesčio (PVM) susigrąžinimo darbo eigas.  |
