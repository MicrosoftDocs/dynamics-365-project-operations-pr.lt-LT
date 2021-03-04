---
title: Operacijos kategorijos kaip kainodaros dimensijos naudojimas
description: Šioje temoje pateikiama informacijos, kaip operacijos kategorijos lauką naudoti kaip kainodaros dimensiją.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514006"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Operacijos kategorijos kaip kainodaros dimensijos naudojimas


_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


Šioje temoje paaiškinta, kaip naudoti lauką **Operacijos kategorija** kaip kainodaros dimensiją. 

## <a name="prerequisites"></a>Būtinosios sąlygos
Kad galėtumėte atlikti šioje temoje nurodytus veiksmus, turite turėti naują savo organizacijos kainodaros dimensijos sprendimą. Jei dar jo nesukūrėte, žr. [Pasirinktinių laukų ir objektų kaip kainodaros dimensijų kūrimas](create-custom-fields-entities-pricing-dimensions.md).

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