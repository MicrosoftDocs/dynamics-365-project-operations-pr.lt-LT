---
title: Subrangos komponentų laiko, išlaidų ir medžiagų naudojimo registravimas
description: Šiame straipsnyje paaiškinama, kaip "Microsoft" stebi laiką, išlaidas ir medžiagų naudojimą, įrašytą projektuose iš subrangos komponentų Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927660"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Pagal subrangos sutartis sudarytų komponentų projektų laiko, išlaidų ir medžiagų naudojimo registravimas

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šiame straipsnyje paaiškinama, kaip "Microsoft" stebi laiką, išlaidas ir medžiagų naudojimą, įrašytą projektuose iš subrangos komponentų Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Subrangovo laiko sąnaudos projektuose
Programoje "Project Operations" sutartininkai gali įrašyti laiką projektuose taip pat, kaip ir darbuotojai. Įvesdamas laiką su projektais ir (arba) projekto užduotimis, sutartininkas gali pasirinkti konkrečią subrangos ir subrangos eilutę.

Patvirtinus sutartininkų pateiktą laiką, projekto savikaina įrašoma naudojant vieneto savikainos tarifą, nustatytą tam sutartininko ištekliui **subrangos pirkimo kainoraščio skyriuje Vaidmenų kainos**.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Subrangos išlaidų projektų įkainojimas
Įvesdami su projektais patirtas išlaidas, išlaidų įraše galite pasirinkti subrangos ir subrangos eilutę. 

Kai šis išlaidų įrašas pateikiamas ir patvirtinamas, išlaidų savikaina įrašoma projekte pagal vieneto savikainą, nustatytą tai operacijų kategorijai **subrangos pirkimo kainoraščio skyriuje Kategorijos kainos**.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Subrangos medžiagų, susijusių su projektais, įkainojimas
Įvesdami medžiagų naudojimą projektuose, medžiagų naudojimo žurnale galite pasirinkti subrangos ir subrangos eilutę. Kai medžiagų naudojimo žurnalas pateikiamas ir patvirtinamas, medžiagų savikaina įrašoma į projektą pagal vieneto savikainą, nustatytą tam produktui **subrangos kainoraščio kainoraščio skyriuje Kainoraščio prekės**.

Medžiagų naudojimas taip pat gali būti įrašomas į projektus įtrauktiems produktams. Šio tipo medžiagų naudojimas taip pat gali būti susietas su subrangos ir subrangos eilute. Fiksuodami įrašymo produktų medžiagų naudojimą, turite įvesti įrašymo produkto vieneto kainą. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
