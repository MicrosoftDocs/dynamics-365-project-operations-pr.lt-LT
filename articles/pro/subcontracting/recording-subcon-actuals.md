---
title: Subrangos komponentų laiko, išlaidų ir medžiagų naudojimo fiksavimas
description: Šioje temoje paaiškinama, kaip laiką, išlaidas ir medžiagų naudojimą, įrašytus projektuose iš subrangos komponentų, seka Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903722"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Laiko, išlaidų ir medžiagų naudojimo subrangos komponentų projektuose fiksavimas

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šioje temoje paaiškinama, kaip laiką, išlaidas ir medžiagų naudojimą, įrašytus projektuose iš subrangos komponentų, seka Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Projektų subrangovo laiko įkainojimas
Projekto operacijose sutartininkai gali įrašyti laiką projektuose panašiai kaip ir darbuotojai. Įvesdamas projektų ir (arba) projekto užduočių laiką, sutartininkas gali pasirinkti konkrečią subrangos ir subrangos eilutę.

Kai patvirtinamas sutartininkų pateiktas laikas, projekto savikaina įrašoma naudojant vieneto savikainos normą, nustatytą tam sutartinės darbuotojo ištekliui **subrangos** pirkimo kaino dalies skyriuje Vaidmenų kainos.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Subrangos išlaidų projektams įkainojimas
Įvesdami projektų išlaidas, išlaidų įraše galite pasirinkti subrangos ir subrangos eilutę. 

Kai šis išlaidų įrašas pateikiamas ir patvirtinamas, išlaidų savikaina įrašoma į projektą pagal vieneto savikainą, nustatytą tai operacijos kategorijai **subrangos** pirkimo kaino dalies skyriuje Kategorijos kainos.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Subrangos medžiagų įkainojimas projektuose
Įvesdami medžiagų naudojimą projektuose, medžiagų naudojimo žurnale galite pasirinkti subrangos ir subrangos eilutę. Kai medžiagų naudojimo žurnalas pateikiamas ir patvirtinamas, medžiagų savikaina įrašoma į projektą pagal vieneto savikainą, nustatytą tam produktui **subrangos** kaino dalies straipsnių skyriuje.

Medžiagos naudojimas taip pat gali būti registruojamas rašymo produktams projektuose. Šio tipo medžiagų naudojimas taip pat gali būti susietas su subrangos ir subrangos linija. Įrašydami įrašymo produktų medžiagų naudojimą, turite įvesti įrašymo produkto vieneto savikainą. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
