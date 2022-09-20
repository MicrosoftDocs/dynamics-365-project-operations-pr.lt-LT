---
title: Faktinės datos kaina nepaiso
description: Šiame straipsnyje paaiškinama, kaip kainoraštyje nustatyti kainų nepaisymus konkrečioms kainoms.
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
# <a name="date-effective-price-overrides"></a>Faktinės datos kaina nepaiso 

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

*Datos įsigaliojimo kainų nepaisymas* suteikia galimybę nepaisyti arba pakeisti konkrečias kainas kainoraštyje. Pavyzdžiui, turite standartinį kainoraštį, kuris galioja nuo 2022 m. sausio 1 d. iki 2022 m. gruodžio 31 d. Šiame kainoraštyje yra daugelio vaidmenų kainos. Tinklo techniko **vaidmeniui** nustatyta kaina yra 100 JAV dolerių (USD) už valandą. Kai tinklo technikas registruoja laiką nuo 2022 m. sausio 1 d. iki 2022 m. gruodžio 31 d., laikas įkainojamas 100 USD. 1 m. spalio 2022 d. turite koreguoti tik *tinklo* techniko **vaidmens kainą**– nuo 100 USD per valandą iki 110 USD per valandą. Funkcija Datos **efektyvios kainos nepaisymo** leidžia nustatyti šį pakeitimą kaip eilutės nepaisymą tos konkrečios vaidmens kainos eilutei. Todėl jums nereikia kopijuoti viso kainoraščio ir keisti tik tos vienos eilutės kainos.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Darbo kainodarai taikoma galiojanti data

Datos efektyvios kainos nustatymo procesas, viršijantis darbo laiką projekte, susideda iš dviejų pagrindinių etapų.

1. Įgalinti **datos įsigaliojimo kainos nepaisymo** funkciją.
1. Nustatykite datos įsigaliojimo kainos nepaisymą.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Įgalinkite funkciją Data įsigaliojimo kaina nepaiso

> [!NOTE]
> **Įjungus funkciją "Date effective price overrides**", jos išjungti negalima.

Norėdami įjungti **efektyvios datos kainos nepaisymo** funkciją, atlikite šiuos veiksmus.

1. Eikite į **"Settings Parameters"** \> **·**.
1. Atidarykite parametrų **įrašą**.
1. Veiksmų srities skirtuke Funkcijų **valdymas** pasirinkite **Įgalinti datos efektyvios kainos nepaisymą**.
1. Patvirtinimo dialogo lange pasirinkite **Gerai**.
1. Po kelių akimirkų atnaujinkite naršyklę. Dabar turėtų būti prieinamos datos įsigaliojimo kainos nepaisymo galimybės. Žinosite, kad šios galimybės buvo įjungtos, jei **veiksmų srityje nebepasirodomi įgalinti datos efektyvios kainos nepaisymus**.

### <a name="set-up-a-date-effective-price-override"></a>Faktinės datos kainos nepaisymo nustatymas

Datos įsigaliojimo kainos perrašymus galima nustatyti **savikainos**, **pardavimo** arba **pirkimo** kainoraščiuose.

> [!NOTE]
>Įsigaliojimo datos kainos nepaisymo elgsena **šiuo** metu turi šiuos apribojimus:
>
> - Tik vaidmenų kainos ir vaidmenų kainų antkainiai palaiko **"Project Operations" funkciją Efektyvios kainos nepaisymo** data.
> - Kai kopijuojate kainoraštį naudodami veiksmą Kopijuoti, esantį **puslapyje Kainoraščių informacija**, ir kai kuriate projekto kainoraštį iš standartinio arba pasirinktinio kainoraščio kurdami sutartį, datos įsigaliojimo kainų perrašymai iš šaltinio kainoraščio **nekopijuojami**.**·**

Norėdami nustatyti datos efektyvios kainos nepaisymą vaidmens kainai arba vaidmens kainos antkainiui, atlikite šiuos veiksmus.

1. Atidarykite kainoraščio, kuriam norite nustatyti datos įsigaliojimo kainos perrašymą, puslapį.
1. Pasirinkite skirtuką **Vaidmenų kainos** . Šiame skirtuke pateikiami visi **kainoraštyje esantys vaidmenų kainoraščio** įrašai.
1. **Pasirinkite vaidmens kainos** įrašą, kurio kainą norite nustatyti kaip naują galiojančią datą, tada dukart bakstelėkite (arba dukart spustelėkite) **Vaidmens kaina**, kad atidarytumėte **puslapį Išsami** vaidmens informacija.
1. Pasirinkite skirtuką Data, **kada galioja, nepaiso** . Šiame skirtuke esančiame tinklelyje pateikiami visi pasirinktos **vaidmens kainos** įrašo efektyvios kainos perrašymai.
1. Virš tinklelio esančioje įrankių juostoje pasirinkite **Naujo vaidmens kainos nepaisymas**. Atidaromas slankiklis **Naujo vaidmens kainos nepaisymo** slankiklis.
1. Nurodykite įsigaliojimo datą, vienetą ir naują kainos nepaisymo kainą. Tada pasirinkite **Įrašyti** ir uždarykite formą.

> [!NOTE]
> - Faktinės datos kainos nepaisymas vaidmens kainai arba vaidmens kainos antkainiui taikomas tam pačiam kainodaros dimensijos reikšmių deriniui, esančiam pirminėje **vaidmens kainos** arba **vaidmens kainos žymėjimo** eilutėje.
> - Lauke Efektyvus iš **pasirinkta** data turi būti pirminio kainoraščio įsigaliojimo datose. Kainų nepaisymas įsigalios lauke Galioja nuo **pasirinktos** datos ir bus taikomas iki pirminio kainoraščio pabaigos datos pabaigos datos. Jei nustatysite kitą datos efektyvios kainos nepaisymą tai pačiai vaidmens kainai, pirmasis kainos nepaisymas įsigalios tą dieną, kuri bus pasirinkta **lauke Efektyvus nuo ir** bus taikomas iki antrojo perrašymo pradžios.

## <a name="examples"></a>Pavyzdžiai

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>1 pavyzdys: vaidmens kainos, kurios vaidmens kaina yra nepaisoma, datos efektingumo nustatymas

Toliau pateiktame pavyzdyje parodyta, kaip nustatomas konkrečios vaidmens kainos, kuriai nustatyti vaidmens kainos nepaisymo, datos veiksmingumas.

**Kainoraštis A: nuo sausio 1 d. iki birželio 30 d.**

*Vaidmens kaina*

| Vaidmens kaina | Vienetas | Kainos | Poveikis gaunamų sandorių kainodarai |
|---|---|---|---|
| Tinklo technikas | Valanda | 100 | Ši kaina bus naudojama visiems sandoriams, kai sandorio data yra nuo sausio 1 d. iki kovo 14 d. |

*Vaidmens kainos nepaisymas*

| Efektyvus nuo | Vienetas | Kainos | Poveikis gaunamų sandorių kainodarai |
|---|---|---|---|
| 15 m. kovo mėn. | Valanda | 110 | Ši kaina bus naudojama visiems sandoriams, kai sandorio data yra nuo kovo 15 d. iki kovo 30 d. |
| 1 balandžio mėn. | Valanda | 120 | Ši kaina bus naudojama visiems sandoriams, kai sandorio data yra nuo balandžio 1 d. iki birželio 30 d. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>2 pavyzdys: vaidmens kainos žymėjimo, kurio vaidmens kainos žymėjimas nepaiso, datos efektingumo nustatymas

Toliau pateiktame pavyzdyje parodyta, kaip nustatomas konkretaus vaidmens kainos žymėjimo, kuriam nustatyti vaidmens kainos žymėjimo nepaisymai, datos veiksmingumas.

**Kainoraštis A: nuo sausio 1 d. iki birželio 30 d.**

*Vaidmens kaina*

| Vaidmens kaina | Darbo valandos | Vienetas | Kainos | Poveikis gaunamų sandorių kainodarai |
|---|---|---|---|---|
| Tinklo technikas | Taisyklingas | Valanda | 100 | Ši kaina bus naudojama visiems sandoriams, kai sandorio data yra nuo sausio 1 d. iki kovo 14 d. |

*Vaidmens kainos žymėjimas*

| Organizacijos padalinys | Darbo valandos | Antkainis % |
|---|---|---|
| „Danys“, JAV | Viršvalandžiai | 10 % |

*Vaidmens kainos žymėjimo nepaisymas*

| Efektyvus nuo | Kainos | Poveikis gaunamų sandorių kainodarai |
|---|---|---|
| 15 m. kovo mėn. | 20 % | Šis antkainio procentas bus naudojamas visoms operacijoms, kai operacijos data yra nuo kovo 15 d. iki kovo 30 d. |
| 1 balandžio mėn. | 25 % | Šis žymėjimas bus naudojamas visoms operacijoms, kai operacijos data yra nuo balandžio 1 d. iki birželio 30 d. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
