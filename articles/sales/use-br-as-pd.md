---
title: Rezervuojamų išteklių kaip kainodaros dimensijos naudojimas
description: Šioje temoje pateikiama informacijos, kaip naudoti rezervuojamus išteklius kaip kainodaros dimensiją.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d46d4659a5f60226f80b29f3dd8607249cb91ac2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011201"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Rezervuojamų išteklių kaip kainodaros dimensijos naudojimas

 _**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_ 

Šioje temoje pateikiama informacijos, kaip naudoti rezervuojamus išteklius kaip kainodaros dimensiją. Jei jūsų kainodaros strategijoje nustatyta, kad kiekvienas rezervuojamas išteklius turi turėti konkrečią kainą ar įkainį, naudokite rezervuojamus išteklius kaip kainodaros dimensiją.

## <a name="prerequisites"></a>Būtinosios sąlygos
Kad galėtumėte atlikti šioje temoje nurodytus veiksmus, turite turėti naują savo organizacijos kainodaros dimensijos sprendimą. Jei dar jo nesukūrėte, žr. [Pasirinktinių laukų ir objektų kūrimas](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Rezervuojamų išteklių lauko įtraukimas į formas ir rodinius
Jei norite, kad laukas **Rezervuojami ištekliai** būtų rodomas kainodaros dimensijos sprendime, reikia pridėti lauką prie visų formų ir rodinių kaip objektą.

Toliau esančioje lentelėje pateiktos visos paruoštos naudoti formos ir rodiniai pagal objektą. Taip pat turėsite pridėti naują lauką prie bet kokių papildomų formų ar rodinių, esančių jūsų tinkintuose objektuose.

|   Entity        | Formos   |Peržiūros        |
| ------------------------------|---------------------------------|----------------------------------|
|  Vaidmens kaina| Informacija | - Aktyvių išteklių kategorijų kainos<br> - Išteklių kategorijos kainos susietasis rodinys |
|  Vaidmens kainos antkainis| Informacija| - Aktyvaus vaidmens kainos antkainis<br>- Vaidmens kainos antkainio susietasis rodinys |
|  Pasiūlymo eilutės informacija| - Projekto informacija<br>- Spartusis projekto kūrimas| - Aktyvaus pasiūlymo eilutės informacija<br>- Jungtinių pasiūlymo eilučių informacija<br>- Pasiūlymo eilutės informacijos susietasis rodinys |
|  • Projekto sutarties eilutės informacija| - Projekto informacija<br>- Spartusis projekto kūrimas| - Jungtinių sutarties eilučių informacija<br>- Aktyvios sutarties eilutės informacija<br>- Sutarties eilutės informacijos susietasis rodinys |
|  Projekto užduotis| - Informacija<br>- Nauja forma| &nbsp; |
|  Projekto komandos narys| - Informacija<br>- Nauja forma| - Aktyvūs projekto komandos nariai<br>- Projekto komandos nariai<br>- Projekto komandos narių susietasis rodinys |
|  Laiko įrašas| - Informacija<br>- Kurti laiko įrašą| - Mano laiko įrašai pagal datą<br>- Mano laiko įrašai šią savaitę<br>- Laiko įrašai, skirti patvirtinti|
|  Žurnalo eilutė| - Informacija<br>- Spartusis kūrimas| - Aktyvaus žurnalo eilutės<br>- Žurnalo eilučių susietasis rodinys |
|  Sąskaitos faktūros eilutės informacija| - Informacija<br>- Spartusis kūrimas| - Aktyvios sąskaitos faktūros eilutės informacija<br>- Apmokestinamos sąskaitos faktūros operacijos<br>- Nemokamos sąskaitos faktūros operacijos<br>- Sąskaitos faktūros eilutės informacijos susietasis rodinys <br>- Neapmokestinamos sąskaitos faktūros operacijos|
|  Faktinis| - Informacija<br>- Aktyvūs faktiniai duomenys| Faktinis susietasis rodinys |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Rezervuojamų išteklių kaip kainodaros dimensijos nustatymas
Norėdami nustatyti rezervuojamus išteklius kaip kainodaros dimensiją, atlikite toliau nurodytus veiksmus.

1. Eikite į **Parametrai** > **Parametrai**. 
2. Puslapio **Parametras** skirtuke **Suma pagrįstos kainodaros dimensijos** įsitikinkite, kad tinklelyje rodomi objekto **Kainodaros dimensijos** įrašai. 
2. Įtraukite **Rezervuojamą išteklių** į šį kainodaros dimensijų sąrašą kaip **msdyn_bookableresource**. 
3. Dalyse **Taikoma savikainai** ir **Taikoma pardavimui** pasirinkite reikšmę.
4. Dalyje **Dimensijos tipas** pasirinkite **Pagrįsta suma**. 
5. Pasirinkite rezervuojamo ištekliaus savikainos ir pardavimo prioritetą. Paprastai rezervuojamiems ištekliams taikomas didžiausias prioritetas, kai jie įtraukiami kaip kainodaros dimensija. Nustatykite prioriteto reikšmę **1** (arba **0**, atsižvelgiant į tai, kaip taikote prioritetus), kad užtikrintumėte šį veikimo principą.

## <a name="set-up-pricing-dimension-field-names"></a>Kainodaros dimensijų laukų pavadinimų nustatymas

Kai lentelėje **Vaidmens kaina** kainodaros dimensijos lauko pavadinimas skiriasi nuo tos dimensijos lauko pavadinimo bet kuriame kitame objekte, kuriame naudojama numatytoji kaina, kainodaros dimensijos įraše būtina nurodyti, kad pavadinimai skiriasi.  

Objekto **Projekto komandos nariai** rezervuojamų išteklių lauko pavadinimas šiek tiek skiriasi nuo pavadinimo objekte **Vaidmens kaina**: 

 - Objektas **Projekto komandos nariai** = **msdyn_bookableresourceid**
 - Objektas **Vaidmens kaina** = **msdyn_bookableresource**

Šį skirtumą būtina nurodyti **msydn_bookableresource** kainodaros dimensijos įraše.

1. Dukart spustelėkite eilutę tinklelyje **Kainodaros dimensijos**, kad atidarytumėte dimensijos puslapį **msdyn_bookableresource**.
2. Dimensijos puslapio skirtuke **Susiję** pasirinkite **Kainodaros dimensijų laukų pavadinimai**.

  ![Skirtukas Kainodaros dimensijos laukų pavadinimai](media/PD-fieldname.png)

3. Atsidariusiame susietajame rodinyje pasirinkite **Įtraukti naują kainodaros dimensijos lauko pavadinimą**.

  ![Naujų kainodaros dimensijų laukų pavadinimį įtraukimas](media/Add-NewPD-fieldname.png)

  Bus atidarytas dimensijos **msdyn_bookableresource** puslapis **Naujas kainodaros dimensijos lauko pavadinimas**. 

4. Puslapyje **Naujų kainodaros dimensijų laukų pavadinimų forma** pridėkite **msdyn_projectteam** prie **Objekto loginis pavadinimas**.
5. Pridėkite **msdyn_bookableresourceid** prie **Lauko pavadinimas**.

 ![Naujų kainodaros dimensijų laukų pavadinimų forma](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]