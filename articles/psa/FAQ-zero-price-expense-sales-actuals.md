---
title: Kodėl numatytoji faktinių duomenų pardavimo išlaidų kaina nustatoma kaip nulis?
description: Šios trys patikros padės jums diagnozuoti triktis, susijusias su klausimu, kodėl numatytoji faktinių duomenų pardavimo išlaidų kaina nustatoma kaip 0.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8c2270b07b6f8765a6ec1f506fe1767a1841950b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122083"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Kodėl numatytoji faktinių duomenų pardavimo išlaidų kaina nustatoma kaip nulis?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Šie DUK taikomi faktiniams išlaidų duomenims, kai nustatyta operacijos klasė „Išlaidos“, o operacijos tipas „Pardavimas, už kurį neišrašyta sąskaita“. Šios trys patikros padės jums diagnozuoti triktis, susijusius su klausimu, kodėl numatytoji faktinių duomenų pardavimo išlaidų kaina (sąskaitos tarifas) nustatoma kaip 0.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>1 patikra: nustatykite projekto pardavimo kainoraštį

Raskite projektą faktinių duomenų projekto lauke ir eikite į projekto puslapį. Tada eikite į skirtuką „Pardavimas“. Projekto sutarties eilučių tinklelyje spustelėkite saitą, esantį projekto sutarties lauke. Projekto sutarties puslapis bus atidarytas. Projekto sutarties puslapyje eikite į skirtuką „Projekto kainoraščiai“. Patikrinkite, ar čia pridėtas bent vienas kainoraštis.

Jeigu prie projekto sutarties projekto kainoraščio tinklelio nepridėta kainoraščių, atilkite šiuos veiksmus:

- Pridėkite kainoraštį prie projekto kainoraščių tinklelio. Kainoraščių, kuriuos galima pridėti čia, konteksto laukas turi būti nustatytas kaip „Pardavimas“, o valiutos laukas kainoraštyje turi atitikti valiutos lauką, esantį projekto sutartyje. Atlikę reikiamus taisymus, iš naujo sukurkite išlaidų įrašą, patvirtinkite jį ir patikrinkite, kad faktiniai pardavimo, už kurį neišrašyta sąskaita, duomenyse rodoma tinkama kaina.
- Jeigu prie projekto sutarties projekto kainoraščių tinklelio pridėtas vienas ar daugiau kainoraščių, atlikite 2 patikrą.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>2 patikra: ar anksčiau nurodyti kainoraščiai galioja konkrečiai faktinių išlaidų duomenų datai?

Tam, kad „Project Service“ atsižvelgtų į kainoraštį, kai nustatoma numatytoji kaina, šis kainoraštis turi būti taikytinas faktinių pardavimo išlaidų datai. Tam, kad pamatytumėte, ar anksčiau nurodytas (-i) kainoraštis (-iai) yra taikytini, patikrinkite šiuos dalykus:

- Pirma patikrinkite, ar pradžios ir pabaigos datos įvestos pridėtų kainoraščių skirtuke „Bendra“. Jei pradžios ir pabaigos datos anksčiau nurodytuose kainoraščiuose neįvestos, nustatėte problemą. 
- Užsirašykite pradžios datą, esančią faktinių išlaidų pardavimo duomenų lauke ir patikrinkite, ar nors vienas nurodytų kainoraščių tinka šiai datai. Pavyzdžiui, faktinių duomenų išlaidų data turėtų atitikti laikotarpį nuo pradžios datos iki pabaigos datos, nurodytų kainoraštyje. 
    - Jei nėra kainoraščio, atitinkančio datą, nurodytą faktiniuose pardavimo išlaidų duomenyse, nustatėte problemą. Pakeiskite kainoraščio pradžios ir pabaigos datas, užtikrindami, kad kainoraštis atitinka faktinių išlaidų duomenų datą. 
    - Jei yra daugiau nei vienas kainoraštis, atitinkantis išlaidų pardavimo faktinių duomenų datą, nustatėte problemą. Galite ją išspręsti pakeitę kainoraščio (-ių) pradžios ir pabaigos datas, kad būtų tik vienas kainoraštis, atitinkantis išlaidų faktinių duomenų datą. 
    - Jei yra tik vienas kainoraštis, atitinkantis faktinių išlaidų duomenų datą, atlikite 3 patikrą.
Atlikę reikiamus taisymus, iš naujo sukurkite išlaidų įrašą, patvirtinkite jį ir patikrinkite, kad faktiniuose pardavimo, už kurį neišrašyta sąskaita, duomenyse rodoma tinkama kaina.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>3 patikra: ar yra tinkama išlaidų kategorijos kaina taikytino projekto kainoraštyje? 

Jei sėkmingai atlikote 1 ir 2 patikras, dabar turite tik vieną projekto kainoraštį, taikytiną faktinių pardavimo išlaidų duomenų datai. Atidarykite šio projekto kainoraštį ir eikite į skirtuką „Kategorijos kainos“. Įsitikinkite, kad tinklelyje yra eilutė, skirta specialiai išlaidų kategorijai, esančiai faktiniuose išlaidų duomenyse.
 
- Jei eilutės nėra, nustatėte problemą. Sukurkite eilutę kategorijos kainų tinklelyje, skirtame faktinių išlaidų duomenų kategorijai. Atlikę šiuos veiksmus, iš naujo sukurkite išlaidų įrašą, patvirtinkite jį ir patikrinkite, kad faktiniuose pardavimo, už kurį neišrašyta sąskaita, duomenyse rodoma tinkama kaina. 
- Jei kategorijos kainų tinklelyje yra išlaidų kategorijos eilutė, patikrinkite, ar joje nurodyta tinkama kaina.

Tam, kad suprastumėte, kokia kaina yra tinkama, pasinaudokite šiais būdais:

- Jei kainodaros metodo laukas kategorijos kainų eilutėje nustatytas kaip „Savikaina“, vieneto tarifas faktiniuose pardavimo išlaidų duomenyse pagal numatytuosius duomenis bus nustatytas kaip vertė išlaidų įraše.
- Jei kainodaros metodo laukas kategorijos kainų eilutėje nustatytas kaip „Antkainio procentas“, patikrinkite, ar nustatyta tinkama procento lauko vertė. Faktinių pardavimo išlaidų duomenų vieneto tarifas pagal numatytuosius parametrus bus nustatytas taikant šį antkainio procentą išlaidų įrašo kainai.
- Jei kainodaros metodo laukas kategorijos kainų eilutėje nustatytas kaip „Vieneto kaina“, patikrinkite, ar nustatyta tinkama kainos lauko vertė. Vieneto tarifas faktiniuose pardavimo išlaidų duomenyse pagal numatytuosius parametrus bus nustatytas kaip valiutos suma, nurodyta kainos lauke.

Jeigu išlaidų kategorijos kaina yra netinkamai nustatyta, nustatėte problemą. Norėdami ją išspręsti, redaguokite kategorijos kainų eilutę, nurodydami tinkamą išlaidų kategorijos kainą pagal anksčiau pateiktas taisykles. Atlikę šiuos veiksmus, iš naujo sukurkite išlaidų įrašą, patvirtinkite jį ir patikrinkite, kad faktiniuose pardavimo, už kurį neišrašyta sąskaita, duomenyse rodoma tinkama kaina.

Jei atlikote visas tris anksčiau minėtas patikras ir vis dar nematote tinkamos kainos faktiniuose pardavimo išlaidų duomenyse, užregistruokite palaikymo kvitą.

