---
title: Subrangos komponentų laiko, išlaidų ir medžiagų naudojimo registravimas
description: Šiame straipsnyje paaiškinama, kaip "Microsoft" seka laiką, išlaidas ir medžiagų naudojimą, įrašytą projektuose iš subrangos komponentų Dynamics 365 Project Operations.
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
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Laiko, išlaidų ir medžiagų naudojimo registravimas subrangovų komponentų projektuose

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Šiame straipsnyje paaiškinama, kaip "Microsoft" seka laiką, išlaidas ir medžiagų naudojimą, įrašytą projektuose iš subrangos komponentų Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Subrangovų laiko įkainojimas projektuose
Programoje "Project Operations" pagal sutartis dirbantys darbuotojai gali įrašyti projektų laiką panašiai kaip darbuotojai. Nustatydamas laiką projektams ir (arba) projekto užduotims atlikti, pagal sutartį dirbantis darbuotojas gali pasirinkti konkrečią subrangos ir subrangos liniją.

Patvirtinus sutartininkų pateiktą laiką, projekto išlaidos įrašomos naudojant vieneto savikainos tarifą, nustatytą tam sutartinio darbuotojo ištekliui subrangos **sutarties pirkimo kainoraščio dalyje Vaidmenų kainos**.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Subrangos sutartimi atliekamų projektų išlaidų įkainojimas
Įvesdami projektų patirtas išlaidas, išlaidų įraše galite pasirinkti subrangos ir subrangos liniją. 

Kai šis išlaidų įrašas pateikiamas ir patvirtinamas, išlaidų savikaina įrašoma į projektą pagal vieneto kainą, nustatytą tai sandorių kategorijai **subrangos sutarties pirkimo kainoraščio skyriuje Kategorijos kainos**.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Subrangos pagrindu pagamintų medžiagų, susijusių su projektais, įkainojimas
Įvesdami medžiagų naudojimą projektuose, medžiagų naudojimo žurnale galite pasirinkti subrangos ir subrangos liniją. Kai medžiagos naudojimo žurnalas pateikiamas ir patvirtinamas, materialinė projekto savikaina įrašoma pagal vieneto kainą, nustatytą tam produktui **subrangos kainoraščio skiltyje Kainoraštis**.

Medžiagos panaudojimas taip pat gali būti registruojamas projektams. Šio tipo medžiagų naudojimą taip pat galima susieti su subrangos ir subrangos linija. Įrašydami medžiagos naudojimą įrašymo gaminiams, turite įvesti įrašymo produkto vieneto kainą. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
