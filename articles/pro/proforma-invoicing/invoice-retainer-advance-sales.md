---
title: Avansinio arba išankstinio apmokėjimo sąskaitos faktūros išrašymas
description: Šioje temoje pateikta informacija apie išankstinio arba avansinio apmokėjimo sąskaitų faktūrų išrašymą naudojant „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 12bf3822227badcf8c83d84d6aef6c0fdc7a972a
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596202"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Išankstinio apmokėjimo arba išankstiniu mokėjimu pagrįsto mokėjimo sąskaita faktūra

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ palaiko išankstiniais apmokėjimais pagrįstas sutartis ir vienkartinius avansus. Projekto sutartyje galite įrašyti išankstinio apmokėjimo arba vienkartinio avanso grafiką. Tačiau, įrašant projekto sutarties lygyje, išankstinio arba avansinio mokėjimo negalima naudoti iš karto. Jei norite naudoti išankstinį arba avansinį apmokėjimą sąskaitoje faktūroje, kuria klientas faktiškai apmokestinamas, pirmiausia reikia išrašyti išankstinio arba avansinio apmokėjimo sąskaitą faktūrą.

Norėdami išrašyti išankstinio arba avansinio apmokėjimo sąskaitą faktūrą, atlikite šiuos veiksmus.

1. Pasirinkite **Pardavimas** > **Atsiskaitymas** > **Išankstinis ir avansinis apmokėjimas**. 
2. Puslapyje **Išankstiniai arba avansiniai apmokėjimai** naudokite filtrą, jei norite išrašyti konkretaus išankstinio arba avansinio apmokėjimo sąskaitą faktūrą, ir pažymėkite jį kaip **Parengta išrašyti sąskaitą faktūrą**.
3. Sukurkite sąskaitą faktūrą neautomatiškai iš sąrašo **Projekto sutartys** arba išsamios informacijos puslapio. Išankstinis arba avansinis apmokėjimas rodomas sąskaitos faktūros juodraštyje puslapio **Sąskaita faktūra** skiltyje **Avansiniai ir išankstiniai apmokėjimai**.
4. Patvirtinkite sąskaitą faktūrą. Tai suteiks galimybę naudoti išankstinį arba avansinį mokėjimą. Galite patvirtinti sąskaitą faktūrą sąrašo puslapyje **Išankstiniai ir avansiniai mokėjimai**. Jei avansinio arba išankstinio apmokėjimo sąskaita faktūra išrašyta, galima suma rodoma tinklelyje.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Avansinio arba išankstinio apmokėjimo kūrimas iš sąskaitos faktūros tinklelio

Išankstinį arba avansinį apmokėjimą galite tiesiogiai sukurti sąskaitoje faktūroje.

1. Sąskaitos faktūros juodraščio papildomame tinklelyje **Avansiniai ir išankstiniai apmokėjimai** pasirinkite **Naujas**, kad sukurtumėte naują išankstinį arba avansinį apmokėjimą. 
2. Puslapyje **Spartusis kūrimas** įtraukite būtiną informaciją ir pasirinkite **Įrašyti**. Išankstinis arba avansinis apmokėjimas sukuriamas projekto sutartyje, susijusioje su sąskaita faktūra. Išankstinis arba avansinis apmokėjimas automatiškai pažymimas kaip **Parengta išrašyti sąskaitą faktūrą** ir tada įtraukiamas į puslapio **Sąskaita faktūra** papildomą tinklelį **Avansiniai ir išankstiniai apmokėjimai**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Avansinio arba išankstinio apmokėjimo, už kurį išrašyta sąskaita faktūra, derinimas

Kai išankstinio arba avansinio apmokėjimo sąskaita faktūra išrašyta, juos galima naudoti arba suderinti sąskaitoje faktūroje su laiko, išlaidų, etapų arba kitomis projektais pagrįstomis išlaidomis. Klientas matys sąskaitos faktūros sumą, kurią sumažino išankstinio arba avansinio apmokėjimo suma, naudojama šioje sąskaitoje faktūroje.

Kiekvienoje sąskaitoje faktūroje, sugeneruojamoje projekto sutarčiai, kurioje yra apmokestintų išankstinių arba avansinių apmokėjimų, „Project Operation“ automatiškai taiko išankstinį arba avansinį apmokėjimą sąskaitai faktūrai.

Tai galima matyti puslapio **Sąskaita faktūra** tinklelyje **Taikomi išankstiniai ir avansiniai apmokėjimai**. Šioje lentelėje pateikiama informacija apie puslapyje **Projekto sąskaita faktūra** esančio tinklelio **Taikomi išankstiniai ir avansiniai apmokėjimai** laukus.

| Laukas | Vieta | Aprašo | Tolesnis poveikis |
| --- | --- | --- | --- |
| Aprašo | Puslapio **Projekto sąskaita faktūra** tinklelis **Taikomi išankstiniai ir avansiniai apmokėjimai** |Šiame tik skaitomame lauke pateikiamas išankstinio ir avansinio apmokėjimo, panaudoto šioje sąskaitoje faktūroje, aprašymas. Šios reikšmės sąskaitoje faktūroje pakeisti negalima. Šią reikšmę galima atnaujinti puslapio **Projekto sutartis** papildomame tinklelyje. | Šį lauką galima rodyti išspausdintoje sąskaitoje faktūroje klientui, kad būtų nurodyta, kuris išankstinis ir avansinis apmokėjimas taikomas sąskaitoje faktūroje. |
| Kada pristatyta | Puslapio **Projekto sąskaita faktūra** tinklelis **Taikomi išankstiniai ir avansiniai apmokėjimai**  | Šiame tik skaitomame lauke pateikiama išankstinio ir avansinio apmokėjimo, panaudoto šioje sąskaitoje faktūroje, sąskaitos faktūros data. Šios reikšmės sąskaitoje faktūroje pakeisti negalima. Šią reikšmę galima atnaujinti puslapio **Projekto sutartis** papildomame tinklelyje. | Šį lauką galima rodyti išspausdintoje sąskaitoje faktūroje klientui, kad būtų nurodyta data, kai išankstinio ir avansinio apmokėjimo sąskaita faktūra buvo pirmą kartą išrašyta klientui. |
| Suma | Puslapio **Projekto sąskaita faktūra** tinklelis **Taikomi išankstiniai ir avansiniai apmokėjimai**  | Šiame tik skaitomame lauke pateikiama išankstinio ir avansinio apmokėjimo, panaudoto šioje sąskaitoje faktūroje, suma. Šios reikšmės sąskaitoje faktūroje pakeisti negalima. Šią reikšmę galima atnaujinti puslapio **Projekto sutartis** papildomame tinklelyje. | Šį lauką galima rodyti išspausdintoje sąskaitoje faktūroje klientui, kad būtų nurodyta pradinė išankstinio ir avansinio apmokėjimo suma, sumokėta kliento. |
| Panaudota suma | Puslapio **Projekto sąskaita faktūra** tinklelis **Taikomi išankstiniai ir avansiniai apmokėjimai**  | Šiame tik skaitomame lauke pateikiama apskaičiuota reikšmė, kuri apibendrina, kiek išankstinio ir avansinio apmokėjimo sumos panaudota. | Šį lauką galima rodyti išspausdintoje sąskaitoje faktūroje klientui, kad būtų nurodyta anksčiau panaudota išankstinio ir avansinio apmokėjimo suma. |
| Išplėstinė suma | Puslapio **Projekto sąskaita faktūra** tinklelis **Taikomi išankstiniai ir avansiniai apmokėjimai**  | Šiame redaguojamame lauke pateikiama išankstinio ir avansinio apmokėjimo, naudojamo šioje projekto sąskaitoje faktūroje, suma. Ši suma negali būti didesnė už galimą avansinio mokėjimo sumą. Sistema ją automatiškai apskaičiuoja kaip skirtumą tarp tinklelio laukų **Suma** ir **Panaudota suma** reikšmių. Galite sumažinti šią sumą, kad būtų naudojama mažesnė suma, tačiau negalima padidinti sumos ir naudoti daugiau pinigų, nei yra. | Šį lauką galima rodyti išspausdintoje sąskaitoje faktūroje klientui, kad būtų nurodyta sąskaitoje faktūroje naudojama išankstinio ir avansinio apmokėjimo suma. |
| Balanso išankstinio apmokėjimo suma. | Puslapio **Projekto sąskaita faktūra** tinklelis **Taikomi išankstiniai ir avansiniai apmokėjimai**  | Šis tik skaitomas laukas pateikia reikšmę, kaip ilgai išankstinis ir avansinis apmokėjimas bus paliktas, kai patvirtinama sąskaita faktūra. | Šį lauką galima rodyti išspausdintoje sąskaitoje faktūroje klientui, kad būtų nurodyta suma, kuri liks atlikus išankstinį arba avansinį apmokėjimą, kai sąskaita faktūra bus patvirtinta ir apmokėta. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]