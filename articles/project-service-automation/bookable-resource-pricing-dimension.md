---
title: Rezervuojamų išteklių naudojimas kaip kainodaros dimensijos
description: Šioje temoje pateikiama informacijos apie rezervuojamų išteklių naudojimą kaip kainodaros dimensijos.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 1d147827-dc55-48a5-b3f6-d8b00bd1c7f7
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 999f7575d1777077376ba74933654b90fcc504c3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753705"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Rezervuojamų išteklių naudojimas kaip kainodaros dimensijos
Šioje temoje pateikiama informacijos apie rezervuojamų išteklių naudojimą kaip kainodaros dimensijos. Prieš pradėdami, jei dar nesukūrėte kainodaros dimensijos sprendimo, turėsite sukurti naują sprendimą. Jei jau turite kainodaros dimensijos sprendimą, galite atlikti šio sprendimo pakeitimus. Jei savo organizacijai nesukūrėte naujo kainodaros dimensijos sprendimo, atlikite procedūras, nurodytas temoje [Pasirinktinių laukų ir objektų kūrimas](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Rezervuojamų išteklių įtraukimas į formas ir rodinius
Norint, kad laukai būtų rodomi kainodaros dimensijos sprendimo UI, reikia peržiūrėti visų pagrindinių „Project Service“ objektų formas ir rodinius ir į juos įtraukti šiuos laukus.
Tolesnėje lentelėje pateikiamas išsamus parengtų naudoti formų ir rodinių, išvardytų pagal objektus, sąrašas, kurį reikės atnaujinti. Jei šių objektų tinkinimuose yra papildomų rodinių arba formų, įtraukite šiuos naujus laukus ir į juos.
Atidarykite kainodaros dimensijos sprendimo langą Sprendimų naršyklė ir spustelėkite **Publikuoti visus tinkinimus**.


|   Objektas        | Formos   |Rodiniai        |
| ------------------------------|---------------------------------|----------------------------------|
|  Vaidmens kaina|• Informacija |• Aktyviųjų išteklių kategorijų kainos<br> • Išteklių kategorijos kainos susietasis rodinys|
|  Vaidmens kainos antkainis|• Informacija|• Aktyviojo vaidmens kainos antkainis<br>• Vaidmens kainos antkainio susietasis rodinys|
|  Pasiūlymo eilutės informacija|• Projekto informacija<br>• Spartusis projekto kūrimas|• Aktyviojo pasiūlymo eilutės informacija<br>• Jungtinių pasiūlymo eilučių informacija<br>• Pasiūlymo eilutės informacijos susietasis rodinys|
|  • Projekto sutarties eilutės informacija|• Projekto informacija<br>• Spartusis projekto kūrimas|• Jungtinių sutarties eilučių informacija<br>• Aktyvios sutarties eilutės informacija<br>• Sutarties eilutės išsamios informacijos susietasis rodinys|
|  Projekto komandos narys|• Informacija<br>• Nauja forma|• Aktyvieji projekto komandos nariai<br>• Projekto komandos nariai<br>• Projekto komandos narių susietasis rodinys|
|  Laiko įrašas|• Informacija<br>• Laiko įrašo kūrimas|• Mano laiko įrašai pagal datą<br>• Mano laiko įrašai šią savaitę<br>• Laiko įrašai, skirti patvirtinti|
|  Žurnalo eilutė|• Informacija<br>• Spartusis kūrimas|• Aktyviojo žurnalo eilutės<br>• Žurnalo eilučių susietasis rodinys|
|  Sąskaitos faktūros eilutės informacija|• Informacija<br>• Spartusis kūrimas|• Aktyvioji sąskaitos faktūros eilutės išsami informacija<br>• Apmokestinamos sąskaitų faktūrų operacijos<br>• Nemokamos sąskaitos faktūros operacijos<br>• Sąskaitos faktūros eilutės informacijos susietasis rodinys<br>• Neapmokestinamos sąskaitos faktūros operacijos|
|  Faktinis|• Informacija<br>• Aktyvieji faktiniai duomenys|• Faktinis susietasis rodinys|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Rezervuojamų išteklių nustatymas kaip kainodaros dimensijos

1. Žiniatinklio sąsajoje eikite į **Project Service** > **Parametrai** > **Parametrai**. Puslapio **Parametrai** skirtuke **Kiekiu pagrįstos kainodaros dimensijos** atkreipkite dėmesį, kad tinklelyje rodomi kainodaros dimensijų objekto įrašai. 
2. Įtraukite **Rezervuojamą išteklių** į šį kainodaros dimensijų sąrašą kaip **msdyn_bookableresource**. 
3. Nurodykite kontekstą, kuriame rezervuojamas išteklius veiks kaip kainodaros dimensija, ir nustatykite reikšmes **Taikoma savikainai** ir **Taikoma pardavimui**.
4. Lauke **Dimensijos tipas** pažymėkite **Pagrįsta kiekiu**. 
5. Pasirinkite rezervuojamo ištekliaus savikainos ir pardavimo prioritetą. Paprastai, kai rezervuojamas išteklius įtraukiamas kaip kainodaros dimensija, jam suteikiamas didžiausias prioritetas, todėl nustatoma parinktis **1** (arba **0**, atsižvelgiant į tai, kaip skaičiuojate prioritetą), kad būtų užtikrintas toks veikimas.

## <a name="set-up-pricing-dimension-field-names"></a>Kainodaros dimensijų laukų pavadinimų nustatymas

Kai lentelėje **Vaidmens kaina** kainodaros dimensijos lauko pavadinimas skiriasi nuo tos dimensijos lauko pavadinimo bet kuriame kitame objekte, kuriame numatytosios kainos turi veikti, kainodaros dimensijos įraše būtina pranešti, kad pavadinimai skiriasi.    
Rezervuojamo ištekliaus lauko pavadinimas (**msdyn_bookableresourceid**), esantis objekte **Projekto komandos nariai**, nežymiai skiriasi nuo jo pavadinimo objekte **vaidmens kaina** (**msdyn_bookableresource**). Apie tai būtina pranešti kainodaros dimensijos įraše **msdyn_bookableresource**. 
1. Norėdami tai atlikti, dukart spustelėkite tinklelyje **Kainodaros dimensijos** esančią eilutę ir kad atidarykite dimensijos **msdyn_bookableresource** puslapį.
2. Dimensijos puslapio skirtuke**Susiję** spustelėkite **Kainodaros dimensijų laukų pavadinimai**.

 ![Skirtukas Kainodaros dimensijos laukų pavadinimai](media/PD-fieldname.png)

4. Atsidariusiame susietajame rodinyje spustelėkite **Įtraukti naują kainodaros dimensijos lauko pavadinimą**.

 ![Naujų kainodaros dimensijų laukų pavadinimį įtraukimas](media/Add-NewPD-fieldname.png)


Bus atidarytas dimensijos **msdyn_bookableresource** puslapis **Naujas kainodaros dimensijos lauko pavadinimas**. 

5. Į lauką **Objekto loginis pavadinimas** įtraukite **msdyn_projectteam**, o į lauką **Lauko pavadinimas** – **msdyn_bookableresourceid**. Įrašykite įrašą.

 ![Naujų kainodaros dimensijų laukų pavadinimų forma](media/PD-fieldname-Added.png)
