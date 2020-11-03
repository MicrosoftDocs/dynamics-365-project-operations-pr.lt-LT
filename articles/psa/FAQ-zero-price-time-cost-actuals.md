---
title: Kodėl numatytoji faktinių duomenų laiko savikaina nustatoma kaip nulis?
description: Trikčių šalinimas klausimu kodėl numatytoji faktinių duomenų laiko savikaina nustatoma kaip 0.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 44d4952b77ac0a541cdf8e3e55f202c9209efdf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080855"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Kodėl numatytoji faktinių duomenų laiko savikaina nustatoma kaip nulis?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Šie DUK taikomi faktiniams duomenims, kai nustatyta operacijos klasė „Laikas“, o operacijos tipas „Savikaina“. Šios trys patikros padės jums diagnozuoti triktis, susijusius su klausimu, kodėl faktinių duomenų laiko savikaina nustatoma kaip nulis.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>1 patikra: nustatykite projekto savikainos kainoraštį

Raskite projektą faktinių duomenų projekto lauke ir eikite į projekto puslapį. Lauke spustelėkite sutartį sudarančio vieneto nuorodą. Sutartį sudarančio vieneto puslapyje, savikainos kainoraščių tinklelyje patikrinkite, ar sutartį sudarantis vienetas turi kainoraštį.

Jei kainoraščių yra daugiau nei vienas, nustatėte problemą. „Project Service“ programoje palaikomas tik vienas kainoraštis vienam organizacijos vienetui. Šalinkite visus kainoraščius iš šio objekto tol, kol organizacijos vieneto savikainos kainoraščių tinklelyje liks tik vienas kainoraštis.

Jei prie organizacijos vieneto nėra prikabintų kainoraščių, pasižymėkite, kokia yra organizacijos vieneto valiuta. Eikite į „Project Service“, pasirinkite Parametrai ir atidarykite skirtuką „Projekto kainoraščiai“. Patikrinkite ar yra kainoraščių, kurių kontekstas yra „Kaina“, o valiuta sutampa su organizacijos vieneto valiuta.
 
Jei kriterijus atitinkančių kainoraščių nėra, nustatėte problemą. Įsitikinkite, kad yra bent vienas kainoraštis, kurio kontekstas nustatytas kaip „Kaina“, ir kurio valiuta sutampa su organizacijos vieneto valiuta.

Jei šiuos kriterijus atitinkančių kainoraščių yra daugiau, skaitykite toliau ir atlikite kitas patikras.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>2 patikra: ar anksčiau nurodyti kainoraščiai galioja konkrečiai faktinių duomenų laiko savikainos datai?

Tam, kad „Project Service“ programoje būtų atsižvelgiama į kainoraštį, kai nustatoma numatytoji kaina, šis kainoraštis turi būti taikytinas faktinės savikainos laiko datai. Tam, kad pamatytumėte, ar anksčiau nurodytas (-i) kainoraštis (-iai) yra taikytini, patikrinkite šiuos dalykus:

- Patikrinkite, ar pradžios ir pabaigos datos įvestos pridėtų kainoraščių skirtuke „Bendra“. Jei pradžios ir pabaigos datos anksčiau nurodytuose kainoraščiuose neįvestos, nustatėte problemą. 
- Užsirašykite pradžios datą, esančią faktinių savikainos laiko duomenų lauke ir patikrinkite, ar nors vienas nurodytų kainoraščių tinka šiai datai. Pavyzdžiui, faktinių savikainos laiko data turėtų atitikti laikotarpį nuo pradžios datos iki pabaigos datos, nurodytų kainoraštyje. 
    - Jei nėra kainoraščio, atitinkančio datą, nurodytą faktiniuose savikainos laiko duomenyse, nustatėte problemą. Pakeiskite kainoraščio pradžios ir pabaigos datas, užtikrindami, kad kainoraštis atitinka faktinių savikainos laiko duomenų datą. 
    - Jei yra daugiau nei vienas kainoraštis, atitinkantis faktinių savikainos laiko duomenų datą, nustatėte problemą. Galite ją išspręsti pakeitę kainoraščio (-ių) pradžios ir pabaigos datas, kad būtų tik vienas kainoraštis, atitinkantis faktinių savikainos laiko duomenų datą. 
    - Jei yra tik vienas kainoraštis, kuris apima faktinių savikainos laiko duomenų datą, pereikite prie kitos dokumento patikros.
Atlikę reikiamus taisymus, iš naujo sukurkite laiko įrašą, patvirtinkite jį ir patikrinkite, kad faktiniuose savikainos laiko duomenyse rodoma tinkama kaina.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>3 patikra: ar faktinių savikainos laiko duomenų kainodaros dimensijų kainoraštyje nurodyta kaina?

Jei sėkmingai atlikote 1 ir 2 patikras, dabar turite tik vieną kainoraštį, taikytiną faktinių savikainos laiko duomenų datai. Atidarykite šio projekto kainoraštį ir pereikite į skirtuką „Vaidmenų kainos“. Įsitikinkite, kad tinklelyje yra eilutė, skirta faktinių savikainos laiko duomenų kainodaros dimensijoms.

Jei faktinių savikainos laiko duomenų kainodaros dimensijų vaidmenų kainų tinklelyje nėra eilutės, nustatėte problemą. Sukurkite eilutę faktinių savikainos laiko duomenų kainodaros dimensijų vaidmenų kainų tinklelyje. Atlikę šį veiksmą, iš naujo sukurkite laiko įrašą, patvirtinkite jį ir patikrinkite, kad faktiniuose savikainos laiko duomenyse rodoma tinkama kaina.
 
Jei atlikote visas tris anksčiau minėtas patikras ir vis dar nematote tinkamos kainos faktiniuose savikainos laiko duomenyse, užregistruokite palaikymo kvitą.



