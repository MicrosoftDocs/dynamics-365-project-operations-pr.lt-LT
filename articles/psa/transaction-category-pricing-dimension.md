---
title: Operacijos kategorijos kaip kainodaros dimensijos naudojimas
description: Šioje temoje pateikta informacija apie operacijos kategorijos kaip kainodaros dimensijos naudojimą.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 776327ddca9b5013ca05eb4058145f4196e4143509098c82d0f452bc9709b673
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988878"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Operacijos kategorijos kaip kainodaros dimensijos naudojimas

[!include [banner](../includes/psa-now-project-operations.md)]

Šioje temoje parodyta, kaip naudoti operacijos kategoriją kaip kainodaros dimensiją. Prieš pradėdami, jei dar nesukūrėte kainodaros dimensijos sprendimo, turėsite sukurti naują sprendimą. Jei jau turite kainodaros dimensijos sprendimą, galite atlikti šio sprendimo pakeitimus. Jei savo organizacijai nesukūrėte naujo kainodaros dimensijos sprendimo, atlikite procedūras, nurodytas temoje [Pasirinktinių laukų ir objektų kūrimas](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Operacijos kategorijos įtraukimas į formas ir rodinius
Norint, kad operacijos kategorija būtų rodoma kainodaros dimensijos sprendimo UI, reikia peržiūrėti visų pagrindinių objektų formas ir rodinius ir į juos įtraukti šiuos laukus.
Tolesnėje lentelėje pateikiamas išsamus parengtų naudoti formų ir rodinių, išvardytų pagal objektus, kuriuos reikės atnaujinti įtraukiant naujų laukų, sąrašas. Jei šių objektų tinkinimuose yra papildomų rodinių arba formų, įtraukite šiuos naujus laukus ir į juos.

|  Objektas        | Formos     |Rodiniai        |
| ------------------------------|---------------------------------|----------------------------------|
|  Vaidmens kaina|• Informacija |• Aktyviųjų išteklių kategorijų kainos<br> • Išteklių kategorijos kainos susietasis rodinys|
|  Vaidmens kainos antkainis|• Informacija|• Aktyviojo vaidmens kainos antkainis<br>• Vaidmens kainos antkainio susietasis rodinys|
|  Pasiūlymo eilutės informacija|• Projekto informacija<br>• Spartusis projekto kūrimas|• Aktyviojo pasiūlymo eilutės informacija<br>• Jungtinių pasiūlymo eilučių informacija<br>• Pasiūlymo eilutės informacijos susietasis rodinys|
|  • Projekto sutarties eilutės informacija|• Projekto informacija<br>• Spartusis projekto kūrimas|• Jungtinių sutarties eilučių informacija<br>• Aktyvios sutarties eilutės informacija<br>• Sutarties eilutės išsamios informacijos susietasis rodinys|
|  Projekto užduotis|• Informacija<br>• Nauja forma||
|  Projekto komandos narys|• Informacija<br>• Nauja forma|• Aktyvieji projekto komandos nariai<br>• Projekto komandos nariai<br>• Projekto komandos narių susietasis rodinys|
|  Laiko įrašas|• Informacija<br>• Laiko įrašo kūrimas|• Mano laiko įrašai pagal datą<br>• Mano laiko įrašai šią savaitę<br>• Laiko įrašai, skirti patvirtinti|
|  Žurnalo eilutė|• Informacija<br>• Spartusis kūrimas|• Aktyviojo žurnalo eilutės<br>• Žurnalo eilučių susietasis rodinys|
|  Sąskaitos faktūros eilutės informacija|• Informacija<br>• Spartusis kūrimas|• Aktyvioji sąskaitos faktūros eilutės išsami informacija<br>• Apmokestinamos sąskaitų faktūrų operacijos<br>• Nemokamos sąskaitos faktūros operacijos<br>• Sąskaitos faktūros eilutės informacijos susietasis rodinys<br>• Neapmokestinamos sąskaitos faktūros operacijos|
|  Faktinis|• Informacija<br>• Aktyvieji faktiniai duomenys|• Faktinis susietasis rodinys|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Operacijos kategorijos kaip kainodaros dimensijos nustatymas

1. Žiniatinklio sąsajoje eikite į **Project Service** > **Parametrai** > **Parametrai**. 
2. Puslapio **Parametrai** skirtuke **Suma pagrįstos kainodaros dimensijos** pastebėkite, kad skirtuko tinklelis rodo objekte **Kainodaros dimensijos** esančius įrašus.
3. Į šį sąrašą įtraukite **Operacijos kategoriją** ir laukus **Taikoma savikainai** ir **Taikoma pardavimui** nustatykite į **Taip**.
4. Lauke **Dimensijos tipas** pasirinkite **Pagrįsta suma**, tada pasirinkite su savikaina ir pardavimu susijusios **Operacijos kategorijos** pirmenybę.


[!INCLUDE[footer-include](../includes/footer-banner.md)]