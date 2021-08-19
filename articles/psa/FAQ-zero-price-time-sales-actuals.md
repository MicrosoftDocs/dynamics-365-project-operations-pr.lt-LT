---
title: Kodėl numatytoji faktinių pardavimo laiko duomenų kaina nustatoma kaip nulis?
description: Trikčių šalinimas klausimu kodėl numatytoji faktinių pardavimo laiko duomenų kaina nustatoma kaip 0.
author: rumant
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
ms.openlocfilehash: 2df4ce2d6391e70fea8e8f15c1b5774c9a9bfbe5f5ef2e6d8da8668afd34d4c9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992576"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Kodėl numatytoji faktinių pardavimo laiko duomenų kaina nustatoma kaip nulis?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Šie DUK taikomi faktiniams duomenims, kai nustatyta operacijos klasė „Laikas“, o operacijos tipas „Pardavimas, už kurį neišrašyta sąskaita“. Šios trys patikros padės jums diagnozuoti triktis, susijusius su klausimu, kodėl faktinių pardavimo laiko duomenų kaina (sąskaitos tarifas) nustatoma kaip nulis.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>1 patikra: nustatykite projekto pardavimo kainoraštį

Raskite projektą faktinių duomenų projekto lauke ir eikite į projekto puslapį. Tada eikite į skirtuką „Pardavimas“ ir projekto sutarties eilučių tinklelyje spustelėkite saitą, esantį projekto sutarties lauke. Projekto sutarties puslapis bus atidarytas. Projekto sutarties puslapyje eikite į skirtuką „Projekto kainoraščiai“. Patikrinkite, ar čia pridėtas bent vienas kainoraštis. Jeigu prie projekto sutarties projekto kainoraščio tinklelio nepridėta kainoraščių, nustatėte problemą: Pridėkite kainoraštį prie projekto kainoraščių tinklelio. Kainoraščių, kuriuos galima pridėti čia, konteksto laukas turi būti nustatytas kaip „Pardavimas“, o valiutos laukas kainoraštyje turi atitikti valiutos lauką, esantį projekto sutartyje. Atlikę reikiamus taisymus, iš naujo sukurkite laiko įrašą, patvirtinkite jį ir patikrinkite, kad faktiniuose pardavimo, už kurį neišrašyta sąskaita, duomenyse rodoma tinkama kaina. 

Jeigu prie projekto sutarties projekto kainoraščių tinklelio pridėtas vienas ar daugiau kainoraščių, atlikite kitą dokumento patikrą.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>2 patikra: ar anksčiau nurodyti kainoraščiai galioja konkrečiai faktinių pardavimo laiko duomenų datai?

Tam, kad „Project Service“ atsižvelgtų į kainoraštį, kai nustatoma numatytoji kaina, šis kainoraštis turi būti taikytinas faktinių pardavimo laiko datai. Tam, kad pamatytumėte, ar anksčiau nurodytas (-i) kainoraštis (-iai) yra taikytini, patikrinkite šiuos dalykus:
- Patikrinkite, ar pradžios ir pabaigos datos įvestos pridėtų kainoraščių skirtuke „Bendra“. Jei pradžios ir pabaigos datos anksčiau nurodytuose kainoraščiuose neįvestos, nustatėte problemą. 
- Užsirašykite pradžios datą, esančią faktinių pardavimo laiko duomenų lauke ir patikrinkite, ar nors vienas nurodytų kainoraščių tinka šiai datai. Pavyzdžiui, faktinių pardavimo laiko duomenų data turėtų atitikti laikotarpį nuo pradžios datos iki pabaigos datos, nurodytų kainoraštyje. 
    - Jei nėra kainoraščio, atitinkančio datą, nurodytą faktiniuose pardavimo laiko duomenyse, nustatėte problemą. Pakeiskite kainoraščio pradžios ir pabaigos datas, užtikrindami, kad kainoraštis atitinka faktinių pardavimo laiko duomenų datą. 
    - Jei yra daugiau nei vienas kainoraštis, atitinkantis faktinių pardavimo laiko duomenų datą, nustatėte problemą. Galite ją išspręsti pakeitę kainoraščio (-ių) pradžios ir pabaigos datas, kad būtų tik vienas kainoraštis, atitinkantis faktinių pardavimo laiko duomenų datą. 
    - Jei yra tik vienas kainoraštis, atitinkantis faktinių pardavimo laiko duomenų datą, atlikite 3 patikrą.
Atlikę reikiamus taisymus, iš naujo sukurkite laiko įrašą, patvirtinkite jį ir patikrinkite, kad faktiniuose pardavimo laiko duomenyse rodoma tinkama kaina.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>3 patikra: ar faktinių pardavimo laiko duomenų kainodaros dimensijų kainoraštyje nurodyta kaina?

Jei sėkmingai atlikote 1 ir 2 patikras, dabar turite tik vieną kainoraštį, taikytiną faktinių pardavimo laiko duomenų datai. Atidarykite šio projekto kainoraštį ir pereikite į skirtuką „Vaidmenų kainos“. Įsitikinkite, kad tinklelyje yra eilutė, skirta faktinių pradavimo laiko duomenų kainodaros dimensijoms.

Jei faktinių pardavimo laiko duomenų kainodaros dimensijų vaidmenų kainų tinklelyje nėra eilutės, nustatėte problemą. Sukurkite eilutę faktinių pardavimo laiko duomenų kainodaros dimensijų vaidmenų kainų tinklelyje. Atlikę šį veiksmą, iš naujo sukurkite laiko įrašą, patvirtinkite jį ir patikrinkite, kad faktiniuose pardavimo laiko duomenyse rodoma tinkama kaina.

Jei atlikote visas tris anksčiau minėtas patikras ir vis dar nematote tinkamos kainos faktiniuose pardavimo laiko duomenyse, užregistruokite palaikymo kvitą. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]