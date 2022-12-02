---
title: Projektų žaliavų finansiniai įvertinimai
description: Šiame straipsnyje pateikiama informacija apie tai, kaip apibrėžti arba įvertinti projektu pagrįstas medžiagas.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eb33c8e2ead2a558bf53256095645011212ff343
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925712"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Projektų žaliavų finansiniai įvertinimai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Programoje „Dynamics 365 Project Operations“ projektų vadovai kiekvienam projektui arba užduočiai gali nustatyti projektu pagrįstas medžiagos savikainas. Kiekvieną medžiagų įvertinimą galima susieti su konkrečia projekto užduotimi. Projektuose naudojamos medžiagos gali būti įtraukiamieji produktai arba produktai iš produktų katalogo. Kiekvieno produkto ir vieneto derinio kainą galima apibrėžti projekto pardavimo kainoraščiuose ir projekto savikainos kainoraščiuose.  

Norėdami peržiūrėti, įtraukti arba panaikinti projekto medžiagos įvertinimą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Projektai** ir pasirinkite projektą, kurį norite atnaujinti.
2. Skirtuke **Medžiagų įvertinimai** peržiūrėkite projekto medžiagos įvertinimų sąrašą.
3. Pasirinkite **Naujas medžiagos įvertinimas**, kad sukurtumėte naują medžiagos įvertinimą. Arba pasirinkite naikintiną medžiagų įvertinimą, tada pasirinkite **Naikinti medžiagos įvertinimą**.

Šioje lentelėje pateikiama informacija apie projekto laukus dalyje **Medžiagos įvertinimo eilutė**. 

| **Laukas** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- |
| Užduotis | Projekto užduočių sąrašas. Pateikiama suvestinė ir lapo mazgo užduotys. | Pasirinkus medžiagos įvertinimo eilutės užduotį, bus paveikta užduoties įvertinta medžiagos savikaina ir įvertintas medžiagos pardavimas. Jei šis laukas bus paliktas tuščias, medžiagos įvertinimas bus sekamas ir apibendrinamas tik projekto lygiu. |
| Pasirinkti produktą |  Galite nurodyti, ar ši įvertinimo eilutė yra skirta esamam (kataloge nurodytam) arba įtraukiamajam produktui. | Šiame lauke apibrėžiama, ar pasirenkate produktą iš katalogo, ar įtraukiamąjį produktą. |
| Produktas | Produkto iš produktų katalogo ID. Pasirinkus produkto ID, reikšmė lauke **Pasirinkti produktą** automatiškai atnaujinama į **Esamas produktas**. ID naudojamas norint gauti kainoraščio savikainą ir pardavimo kainas. | Nėra jokio tolesnio šio lauko poveikio. |
| Įtraukiamojo produkto aprašas | Teksto laukas, kuriame reikia įrašyti produkto pavadinimą. Šį lauką reikia naudoti pasirinkus **Įtraukiamasis** lauke **Pasirinkti produktą**.| Nėra jokio tolesnio šio lauko poveikio. |
| Pradžios data | Prognozuojama medžiagų naudojimo data. | Nėra jokio tolesnio šio lauko poveikio. |
| Vienetų grupė | Numatytoji šio lauko reikšmė gaunama iš numatytosios katalogo produktų vienetų grupės. Šį lauką galite atnaujinti, kad būtų galima pasirinkti kitą vienetų grupę. | Nėra jokio tolesnio šio lauko poveikio. |
| Vienetas | Šio lauko reikšmė gaunama iš numatytojo pasirinkto produkto vieneto. Šį lauką galite atnaujinti, kad būtų galima pasirinkti kitą vienetą. | Pakeitus vienetą, nustatoma kita numatytoji vieneto kaina ir savikaina. |
| Kiekis | Įvertintas produkto, kuris bus naudojamas projekte, kiekis. | Nėra jokio tolesnio šio lauko poveikio. |
| Vieneto savikaina | Pasirinkto produkto vieneto savikainos ir vieneto derinys, nustatytas taikomame savikainos kainoraštyje. | Vieneto savikaina visada rodoma projekto savikainos valiuta. Jei kainoraštyje nėra produkto ir vieneto sąrankos deriniui nustatyto vieneto savikainos, vieneto savikainai bus nustatyta numatytoji reikšmė – 0,00. |
| Vieneto kaina | Pasirinkto produkto kainos ir vieneto derinys, nustatytas taikomame pardavimo kainoraštyje. | Vieneto kaina visada rodoma projekto pardavimo valiuta. Jei kainoraštyje nėra produkto ir vieneto sąrankos deriniui nustatytos vieneto kainos, tada vieneto kainai bus nustatyta numatytoji reikšmė – 0,00.|
| Bendroji savikaina | Savikainos suma, apskaičiuojama kaip vieneto \* kiekio savikaina.| Savikainos suma visada rodoma projekto savikainos valiuta. |
| Bendrasis pardavimas | Pardavimo suma, apskaičiuojama kaip vieneto \* kiekio kaina. | Pardavimo suma visada rodoma projekto pardavimo valiuta. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
