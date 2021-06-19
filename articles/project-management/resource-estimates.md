---
title: Projektų išteklių laiko finansiniai įvertinimai
description: Šioje temoje pateikiama informacija apie tai, kaip apskaičiuojami finansiniai laiko įvertinimai.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e79e33da618c4ab32b1ba13f33e50f60a550ff0b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010796"
---
# <a name="financial-estimates-for-resource-time-on-projects"></a>Projektų išteklių laiko finansiniai įvertinimai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Finansiniai laiko įvertinimai apskaičiuojami remiantis trimis toliau nurodytais veiksniais. 

- Bendrojo arba įvardytojo komandos nario, priskirto kiekvienam projekto plano lapo mazgui, tipas. 
- Darbo tipas arba sudėtingumas.
- Užduoties išteklių priskyrimo pastangų paskirstymas. 

Nuo pirmųjų dviejų veiksnių priklauso vieneto savikaina arba ištekliaus priskyrimo sąskaitų tarifas. Išteklių priskyrimo vieneto savikaina arba sąskaitos tarifas nustatomas remiantis priskirtų išteklių atributais. Šie atributai apima organizacinį vienetą, kuriam išteklius priklauso, ir standartinį išteklių vaidmenį. Taip pat galite įtraukti pasirinktinių atributų, susijusių su jūsų verslu dėl išteklių, pvz., standartinį pavadinimą ar patirties lygį, ir nustatyti, kad jie darytų įtaką priskyrimo vieneto savikainai arba pardavimo tarifui.
Be išteklių atributų, darbo atributai, pvz., užduotis, taip pat gali turėti įtakos priskyrimo vieneto pardavimo tarifui arba savikainos tarifui. Pavyzdžiui, kai tam tikros užduotys yra sudėtingesnės, priskyrus išteklių prie konkrečių užduočių vieneto savikaina arba pardavimo tarifas tampa didesnis už ne tokių sudėtingų užduočių vieneto savikainą arba pardavimo tarifą.   

Trečias veiksnys susijęs su valandų pagal tam tikrą tarifą kiekiu. Tais atvejais, kai užduotis apima du kainų laikotarpius, greičiausiai bus įkainota pirma tos užduoties išteklių priskyrimo dalis, o jos kaina skirsis nuo antros užduoties dalies. Kiekvieno išteklių priskyrimo pastangų įvertinimas yra sudėtinė reikšmė, išsaugoma kartu su pastangų paskirstymo kiekvienai dienai rodikliu.

Išsamias instrukcijas, kaip pasirinktinius darbo ir išteklių atributus nustatyti kaip kainodaros ir įkainojimo dimensijas, žr. [Kainodaros dimensijų apžvalga](../pricing-costing/pricing-dimensions-overview.md).

Kiekvieno išteklių priskyrimo finansinis įvertinimas apskaičiuojamas kaip **tarifas/val., o priskyrimas padaugintas iš valandų skaičiaus.**  Nors ir panašus į pastangų įvertinimą, finansinis kiekvieno išteklių priskyrimo savikainos ir pajamų įvertinimas yra sudėtinė reikšmė, išsaugoma kartu su piniginės sumos paskirstymo kiekvienai dienai rodikliu. 

## <a name="summarizing-financial-estimates-for-time"></a>Laiko finansinių reikšmių apibendrinimas
Finansinis laiko įvertinimas lapo mazgo užduotyje – tai visų išteklių priskyrimų tai užduočiai finansinių įvertinimų suma.

Finansinis laiko įvertinimas apibendrinimo arba pirminėje užduotyje – tai visų antrinių užduočių finansinių įvertinimų suma. Tai numatoma projekto darbo savikaina. 

![Išteklių įvertinimai](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Numatytoji savikainos ir sąnaudų valiuta

Numatytoji savikaina gaunama iš kainoraščių, pridėtų prie projekto sutarties vieneto. Projekto savikainos valiuta visada yra projekto sutarties vieneto valiuta. Išteklių priskyrime savikainos finansinis įvertinimas išsaugomas projekto savikainos valiuta. Kartais valiuta, kuria kainoraštyje nustatytas savikainos tarifas, skiriasi nuo projekto savikainos valiutos. Tokiais atvejais programoje valiuta, kuria nustatyta savikaina, konvertuojama į projekto valiutą. Tinklelyje **Įvertinimai** visi išlaidų įvertinimai rodomi ir apibendrinami projekto savikainos valiuta. 

## <a name="default-bill-rate-and-sales-currency"></a>Numatytasis sąskaitų tarifas ir pardavimo valiuta

Numatytoji pardavimo kaina gaunama iš projekto kainoraščių, pridėtų prie susijusios projekto sutarties laimėjus sandorį, arba iš susijusio projekto pasiūlymo, jei sandoris vis dar yra etape prieš parduodant. Projekto pardavimo valiuta visada yra projekto pasiūlymo arba projekto sutarties valiuta. Išteklių priskyrime pardavimo finansinis įvertinimas išsaugomas projekto pardavimo valiuta. Skirtingai nei savikaina, kainoraštyje nustatyta pardavimo kaina niekada negali skirtis nuo projekto pardavimo valiutos. Nėra scenarijaus, kuriam esant valiutą reikėtų konvertuoti. Tinklelyje **Įvertinimai** visi pardavimo įvertinimai rodomi ir apibendrinami projekto pardavimo valiuta. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
