---
title: Operacijos kategorijos kaip kainodaros dimensijos naudojimas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip naudoti lauką Operacijos kategorija kaip kainodaros dimensiją.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 648933299616a683b19bbe2f1231caac779bd1f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911704"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Operacijos kategorijos kaip kainodaros dimensijos naudojimas


_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


Šiame straipsnyje paaiškinama, kaip naudoti **lauką Operacijos kategorija** kaip kainodaros dimensiją. 

## <a name="prerequisites"></a>Būtinosios sąlygos
Prieš atlikdami šiame straipsnyje pateiktas procedūras, turite turėti naują savo organizacijos kainodaros dimensijos sprendimą. Jei dar jo nesukūrėte, žr. [Pasirinktinių laukų ir objektų kaip kainodaros dimensijų kūrimas](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Operacijos kategorijos lauko įtraukimas į formas ir rodinius
Jei norite, kad laukas **Operacijos kategorija** būtų rodomas kainodaros dimensijos sprendime, reikia pridėti lauką prie visų formų ir rodinių kaip objektą.

Toliau esančioje lentelėje pateiktos visos paruoštos naudoti formos ir rodiniai pagal objektą. Taip pat turėsite pridėti naują lauką prie bet kokių papildomų formų ar rodinių, esančių jūsų tinkintuose objektuose.

|  Entity        | Formos     |Peržiūros        |
| ------------------------------|---------------------------------|----------------------------------|
|  Vaidmens kaina| Informacija |- Aktyvių išteklių kategorijų kainos<br> - Išteklių kategorijos kainos susietasis rodinys |
|  Vaidmens kainos antkainis| Informacija|- Aktyvaus vaidmens kainos antkainis<br>- Vaidmens kainos antkainio susietasis rodinys |
|  Pasiūlymo eilutės informacija|- Projekto informacija<br>- Spartusis projekto kūrimas| - Aktyvaus pasiūlymo eilutės informacija<br>- Jungtinių pasiūlymo eilučių informacija<br>- Pasiūlymo eilutės informacijos susietasis rodinys |
|  Projekto sutarties eilutės informacija|- Projekto informacija<br>- Spartusis projekto kūrimas|- Jungtinių sutarties eilučių informacija<br>- Aktyvios sutarties eilutės informacija<br>- Sutarties eilutės informacijos susietasis rodinys |
|  Projekto užduotis|- Informacija<br>- Nauja forma| &nbsp; |
|  Projekto komandos narys|- Informacija<br>- Nauja forma|- Aktyvūs projekto komandos nariai<br>- Projekto komandos nariai<br>- Projekto komandos narių susietasis rodinys |
|  Laiko įrašas|- Informacija<br>- Kurti laiko įrašą|- Mano laiko įrašai pagal datą<br>- Mano laiko įrašai šią savaitę<br>- Laiko įrašai, skirti patvirtinti|
|  Žurnalo eilutė|- Informacija<br>- Spartusis kūrimas|- Aktyvaus žurnalo eilutės<br>- Žurnalo eilučių susietasis rodinys|
|  Sąskaitos faktūros eilutės informacija|- Informacija<br>- Spartusis kūrimas|- Aktyvios sąskaitos faktūros eilutės informacija<br>- Apmokestinamos sąskaitos faktūros operacijos<br>- Nemokamos sąskaitos faktūros operacijos<br>- Sąskaitos faktūros eilutės informacijos susietasis rodinys <br>- Neapmokestinamos sąskaitos faktūros operacijos|
|  Faktinis|- Informacija<br>- Aktyvūs faktiniai duomenys| Faktinis susietasis rodinys |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Operacijos kategorijos lauko kaip kainodaros dimensijos nustatymas

1. Eikite į **Parametrai** > **Parametrai**. 
2. Puslapio **Parametrai** skirtuke **Suma pagrįstos kainodaros dimensijos** įsitikinkite, kad tinklelyje rodomi objekto **Kainodaros dimensijos** įrašai.
3. Prie šio sąrašo pridėkite **Operacijos kategorija** ir nustatykite laukus **Taikoma savikainai** ir **Taikoma pardavimui** kaip **Taip**.
4. Lauke **Dimensijos tipas** pasirinkite **Pagrįsta suma**, tada pasirinkite lauko **Operacijos kategorija** prioritetą, nes jis susijęs su savikaina ir pardavimu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]