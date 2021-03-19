---
title: Išlaidų valdymo darbo eiga
description: Šioje temoje aiškinama, kaip „Microsoft Dynamics 365 Finance“ galima naudoti darbo eigos sistemą, norint nustatyti išlaidų valdymo išlaidų ataskaitų peržiūros procesą.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271678"
---
# <a name="expense-management-workflow"></a>Išlaidų valdymo darbo eiga

Galite naudoti darbo eigos sistemą, norėdami nustatyti išlaidų valdymo išlaidų ataskaitų peržiūros procesą. Galite nustatyti darbo eigą, kuri naudoja šiuos kriterijus, kad nustatytų, kas patvirtina išlaidų ataskaitas.

- Darbuotojų ataskaitų hierarchija ir iš anksto nustatyti patvirtinimo apribojimai
- Daugiapakopis patvirtinimas, palaikantis laikinuosius tvirtintojus ir galutinį tvirtintoją
- Finansinės dimensijos ir projektų vykdymo atsakomybė
- Priskyrimas konkretiems vartotojams arba vartotojų grupėms

Galima kurti išlaidų ataskaitų, kelionių paraiškų, avansinių mokėjimų ir pridėtinės vertės mokesčio (PVM) susigrąžinimo darbo eigos patvirtinimus.

**Pavyzdžiui**

Toliau pateikiamas išlaidų ataskaitos išlaidų valdymo darbo eigos pavyzdys.

1. Darbuotojas sukuria ir išsaugo išlaidų ataskaitą.
2. Darbuotojas pateikia išlaidų ataskaitą patvirtinti. Tvirtintojas identifikuojamas pagal taisykles, apibrėžtas nustatant darbo eigą.
3. Tvirtintojas gauna pranešimą, kad išlaidų ataskaita paruošta patvirtinti. Tvirtintojas patikrina išlaidų ataskaitą ir patvirtina, kad tenkinamos toliau nurodytos sąlygos.

    - Išlaidos nepažeidžia jokios išlaidų strategijos. Jei išlaidos pažeidžia strategiją, tvirtintojas patikrina, ar išlaidų ataskaitoje yra galiojantis įmonės pagrindimas.
    - Elektroniniai kvitai pridėti prie išlaidų ataskaitos.

4. Tvirtintojas patvirtina išlaidų ataskaitą.
5. Išlaidų ataskaita priskirta mokėtinų sumų koordinatoriui užregistruoti.
6. Atliekamas vienas iš toliau nurodytų veiksmų, atsižvelgiant į tai, ar sukonfigūruotas automatinis registravimas.

    - Jei automatinis registravimas sukonfigūruotas, išlaidų ataskaita apdorojama ir vykdomas mokėjimas, o išlaidų ataskaitos būsena atnaujinama.
    - Jei automatinis registravimas nesukonfigūruotas, mokėtinos sumos koordinatorius patikrina, ar yra pateikti visi pradiniai kvitai ir kad kvitai suderinti su išlaidų ataskaitos išlaidomis. Visi mokesčių kodai, įvesti išlaidų ataskaitoje, taip pat turi būti patvirtinti kaip teisingi.

Kai šie reikalavimai patvirtinti, užregistruojama išlaidų ataskaita.

Užregistravus išlaidų ataskaitą, leidžiama atlikti išlaidų ataskaitos mokėjimą ir kompensuoti darbuotojo išlaidas.


[!INCLUDE[footer-include](../includes/footer-banner.md)]