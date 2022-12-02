---
title: Kainos perrašymų įsigaliojimo data
description: Šiame straipsnyje aiškinama, kaip nustatyti tam tikrų kainoraštyje esančių kainų perrašymus.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446006"
---
# <a name="date-effective-price-overrides"></a>Kainos perrašymų įsigaliojimo data 

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

*Kainos perrašymų įsigaliojimo data* suteikia galimybę perrašyti arba pakeisti konkrečias kainoraštyje esančias kainas. Pavyzdžiui, turite standartinį kainoraštį, kuris galioja nuo 2022 m. sausio 1 d. iki 2022 m. gruodžio 31 d. Šiame kai kainų sąraše yra daugelio vaidmenų kainos. Vaidmens **Tinklo technikas** nustatyta kaina yra 100 JAV dolerių (USD) per valandą. Kai tinklo technikas registruoja laiką nuo 2022 m. sausio 1 d. iki 2022 m. gruodžio 31 d., laiko kaina yra 100 USD. 2022 m. spalio 1 d. turite pakoreguoti kainą *tik* vaidmeniui **Tinklo technikas**, iš 100 USD per valandą į 110 USD per valandą. Naudodami funkciją **Kainos perrašymų įsigaliojimo data** galite nustatyti šį pakeitimą kaip to konkretaus vaidmens kainos eilutės perrašymą. Todėl neturite kopijuoti viso kai kainoraščio, o keisti tik tos vienos eilutės kainą.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Darbo kainodaros datų nepaisymai, skirti darbų įkainiams

Projekto darbo laiko kainos perrašymų įsigaliojimo datos nustatymo procesas susideda iš dviejų pagrindinių žingsnių.

1. Įjunkite funkciją **Kainos perrašymų įsigaliojimo data**.
1. Nustatykite kainos perrašymų įsigaliojimo datą.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Funkcijos Kainos perrašymų įsigaliojimo data įjungimas

> [!NOTE]
> Įjungus funkciją **Kainos perrašymų įsigaliojimo data**, jos išjungti negalima.

Norėdami įjungti funkciją **Kainos perrašymų įsigaliojimo data**, atlikite toliau nurodytus veiksmus.

1. Eikite į **Parametrai** \> **Parametrai**.
1. Atidarykite įrašą **Parametrai**.
1. Veiksmų srities skirtuke **Funkcijos valdymas** pasirinkite **Įjungti kainos perrašymų įsigaliojimo datą**.
1. Patvirtinimo dialogo lange pasirinkite **Gerai**.
1. Po kelių sekundžių atnaujinkite naršyklę. Dabar kainos perrašymų įsigaliojimo datos galimybės turi būti pasiekiamos. Žinosite, kad šios galimybės įjungtos, jei veiksmų srityje nebebus rodomas mygtukas **Įjungti kainos perrašymų įsigaliojimo datą**.

### <a name="set-up-a-date-effective-price-override"></a>Kainos perrašymų įsigaliojimo datos nustatymas

Kainos perrašymų įsigaliojimo datą galima nustatyti kainoraščiams **Savikaina**, **Pardavimas** arba **Pirkimas**.

> [!NOTE]
>Funkcijos **Kainos perrašymų įsigaliojimo data** veikimo būdas šiuo metu turi šiuos apribojimus:
>
> - Tik vaidmenų kainos ir vaidmenų kainų antkainiai palaiko funkciją **Kainos perrašymų įsigaliojimo data** programoje „Project Operations“.
> - Kai naudodami veiksmą **Kopijuoti** kopijuojate kainoraštį puslapyje **Kainoraščio išsami informacija** ir kai kuriate projekto kainoraštį iš standartinio arba pasirinktinio kainoraščio sutarties kūrimo metu, kainos perrašymų įsigaliojimo data **nenukopijuojama** iš šaltinio kainoraščio.

Jei norite nustatyti vaidmens kainos arba vaidmens kainos antkainio kainos perrašymų įsigaliojimo datą, atlikite toliau nurodytus veiksmus.

1. Atidarykite kainoraščio, kurio kainos perrašymų įsigaliojimo datą norite nustatyti, puslapį.
1. Pasirinkite skirtuką **Vaidmenų kainos**. Šiame skirtuke išvardyti visi kainoraštyje esantys įrašai **Vaidmens kaina**.
1. Pasirinkite įrašą **Vaidmens kaina**, kuriam norite nustatyti naują kainos perrašymų įsigaliojimo datą, tada dukart bakstelėkite (arba dukart spustelėkite) **Vaidmens kaina**, kad atidarytumėte puslapį **Vaidmens kainos išsami informacija**.
1. Pasirinkite skirtuką **Perrašymų įsigaliojimo data**. Šio skirtuko tinklelyje išvardytos visos pasirinkto įrašo **Vaidmens kaina** kainos perrašymų įsigaliojimo datos.
1. Virš tinklelio esančioje įrankių juostoje pasirinkite **Naujas vaidmens kainos nepaisymas**. Atidaromas slankiklis **Naujas vaidmens kainos perrašymas**.
1. Nurodykite šio kainos perrašymo galiojimo pradžios datą, vienetą ir naują kainą. Tada pasirinkite **Įrašyti** ir uždarykite formą.

> [!NOTE]
> - Vaidmens kainos arba vaidmens kainos antkainio kainos perrašymų įsigaliojimo data taikoma tam pačiam įkainių dimensijos reikšmių deriniui, kuris egzistuoja pirminėje eilutėje **Vaidmens kaina** arba **Vaidmens kainos antkainis**.
> - Data, pasirinkta lauke **Galioja nuo**, turi būti pirminio kainoraščio sąrašo galiojimo datų ribose. Kainos perrašymas įsigalios lauke **Galioja nuo** pasirinktą dieną ir bus taikomas iki pirminio kainoraščio pabaigos datos. Jei nustatote kitą to paties vaidmens kainos perrašymo įsigaliojimo datą, pirmasis kainos perrašymas įsigalios lauke **Galioja nuo** pasirinktą dieną ir bus taikomas iki antrojo perrašymo pradžios.

## <a name="examples"></a>Pavyzdžiai

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>1 pavyzdys: vaidmens kainos, turinčios vaidmens kainos perrašymų, galiojimo datos nustatymas

Toliau pateiktame pavyzdyje parodyta, kaip nustatoma konkrečios vaidmens kainos, kuriai nustatyta kainos perrašymų, galiojimo data.

**Kainoraštis A: nuo sausio 1 iki kovo 30 d.**

*Vaidmens kaina*

| Vaidmens kaina | Vienetas | Kainos | Poveikis gaunamų operacijų įkainiams |
|---|---|---|---|
| Tinklo technikas | Valanda | 100 | Ši kaina bus naudojama visoms operacijoms, kurių operacijos data bus nuo sausio 1 iki kovo 14 d. |

*Vaidmens kainos perrašymas*

| Galioja nuo | Vienetas | Kainos | Poveikis gaunamų operacijų įkainiams |
|---|---|---|---|
| 15 m. kovo mėn. | Valanda | 110 | Ši kaina bus naudojama visoms operacijoms, kurių operacijos data bus nuo kovo 15 iki kovo 30 d. |
| 1 balandžio mėn. | Valanda | 120 | Ši kaina bus naudojama visoms operacijoms, kurių operacijos data bus nuo balandžio 1 iki birželio 30 d. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>2 pavyzdys: vaidmens kainos antkainio, turinčios vaidmens kainos antkainio perrašymų, galiojimo datos nustatymas

Toliau pateiktame pavyzdyje parodyta, kaip nustatoma konkrečios vaidmens kainos antkainio, kuriam nustatyta kainos antkainio perrašymų, galiojimo data.

**Kainoraštis A: nuo sausio 1 iki kovo 30 d.**

*Vaidmens kaina*

| Vaidmens kaina | Darbo valandos | Vienetas | Kainos | Poveikis gaunamų operacijų įkainiams |
|---|---|---|---|---|
| Tinklo technikas | Reguliarus | Valanda | 100 | Ši kaina bus naudojama visoms operacijoms, kurių operacijos data bus nuo sausio 1 iki kovo 14 d. |

*Vaidmens kainos antkainis*

| Organizacijos vienetas | Darbo valandos | Antkainis % |
|---|---|---|
| „Danys“, JAV | Viršvalandžiai | 10 % |

*Vaidmens kainos antkainio perrašymas*

| Galioja nuo | Kainos | Poveikis gaunamų operacijų įkainiams |
|---|---|---|
| 15 m. kovo mėn. | 20 % | Šis kainos antkainis bus naudojamas visoms operacijoms, kurių operacijos data bus nuo kovo 15 iki kovo 30 d. |
| 1 balandžio mėn. | 25 % | Šis kainos antkainis bus naudojama visoms operacijoms, kurių operacijos data bus nuo balandžio 1 iki birželio 30 d. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
