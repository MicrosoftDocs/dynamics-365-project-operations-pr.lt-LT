---
title: Subrangos komponentų laiko, išlaidų ir medžiagų naudojimo registravimas
description: Šiame straipsnyje paaiškinta, kaip "Microsoft Dynamics 365 Project Operations“ sekamas įrašytas laiko, išlaidų ir medžiagų naudojimas projektuose pagal subrangos sutarties komponentus.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522524"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Subrangos komponentų laiko, išlaidų ir medžiagų naudojimo projektuose registravimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Šiame straipsnyje paaiškinta, kaip "Microsoft Dynamics 365 Project Operations“ sekamas įrašytas laiko, išlaidų ir medžiagų naudojimas projektuose pagal subrangos sutarties komponentus.

## <a name="costing-for-subcontractor-time-on-projects"></a>Projektų subrangos sutartčių laike įkainojimas
„Project Operations“ sutarties darbuotojai projektų laiką gali įrašyti panašiai kaip darbuotojai. Įrašydamas laiką projektui ir / ar projekto užduočiai, sutarties darbuotojas gali pasirinkti konkrečią subrangos sutartį ir subrangos sutarties eilutę.

Kai sutarties darbuotojų pateiktas laikas patvirtinamas, projekto išlaidos įrašomos naudojant to sutarties darbuotojo ištekliaus vieneto išlaidų koeficientą, nustatytą pirkimo kaininių sąrašo skyriuje **Vaidmens kainos**.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Projektų išlaidų įvertinimai subrangos sutartims
Įvesdami su projektais susijusias išlaidas, galite pažymėti išlaidų subrangos sutartį ir subrangos eilutę. 

Kai šis išlaidų įrašas pateikiamas ir patvirtinamas, projekto išlaidos įrašomos naudojant to sutarties darbuotojo ištekliaus vieneto išlaidų koeficientą, nustatytą pirkimo kaininių sąrašo skyriuje **Kategorijos kainos**.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Projektų medžiagų įvertinimai subrangos sutartims
Įvesdami su projektais susijusį medžiagų naudojimą, galite pažymėti subrangos sutartį ir subrangos eilutę medžiagų naudojimo žurnale. Kai medžiagų naudojimo žurnalas pateikiamas ir patvirtinamas, projekto medžiagų kaina įrašoma naudojant to sutarties darbuotojo ištekliaus vieneto išlaidų koeficientą, nustatytą pirkimo kaininių sąrašo skyriuje **Kategorijos kainos**.

Medžiagos naudojimą galima įrašyti ir projektų įrašams į produktus. Tokio tipo medžiagos naudojimas taip pat gali būti susietas su sąrangos sutartimi ir eilute. Įrašydami įvedamų produktų medžiagos naudojimą, turite įvesti į jį įvedamo produkto vieneto kainą. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
