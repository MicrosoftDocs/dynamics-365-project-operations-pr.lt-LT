---
title: Pasirinktinių laukų ir objektų kūrimas kaip kainodaros dimensijų
description: Šioje temoje pateikta informacija apie tai, kaip kurti pasirinktinių parinkčių rinkinius arba objektus.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080874"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Pasirinktinių laukų ir objektų kūrimas kaip kainodaros dimensijų

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Atlikite toliau nurodytus veiksmus bet kuriuo metu, kai norite sukurti pasirinktinį parinkčių rinkinį arba objektą.

> [!IMPORTANT]
> Rekomenduojame visus pasirinktinio kainodaros dimensijų pakeitimus atlikti naudojant atskirą sprendimą. Ši svarbi geriausia praktika suteikia lankstumo ateityje siekiant tinkamai atnaujinti arba pašalinti pakeitimus ir padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių. Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima pakartotinai naudoti kainodaros nustatymus.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Pasirinktinio sprendimo kainodaros dimensijoms kūrimas
1. Eikite į **Parametrai** > **Sprendimai** , o tada pasirinkite **Naujas** ir sukurkite naują sprendimą. 
2. Pavadinkite sprendimą **\<your organization name>kainodaros dimensijos** , įveskite likusią reikiamą informaciją, tada spustelėkite **Įrašyti**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Pasirinktinių laukų ir parinkčių rinkinių kūrimas kainodaros dimensijos sprendime

Kainodaros dimensija gali būti parinkčių rinkinys arba objektas. Abu turi būti sukurti jūsų kainodaros sprendime. Šioje procedūroje nurodytuose veiksmuose paaiškinta, kaip kurti objekto dimensijas ir parinkčių rinkinio dimensijas.

### <a name="entity-based-dimensions"></a>Objekto dimensijos

1. Eikite į **Parametrai** > **Sprendimai** , o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Objektai**.
3. Pasirinkite **Naujas** , kad sukurtumėte naują objektą pavadinimu **Standartinis pavadinimas**. 
4. Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.


### <a name="option-set-based-dimensions"></a>Parinkčių rinkinio matmenys 
Galite sukurti du parinkčių rinkinio matmenis. Pasinaudokite lauku **Išteklių darbo vieta** ir sekite darbą **namų** vietoje bei **darbo vietoje** , o pasinaudodami lauku **Išteklių darbo valandos** , su vertėmis **Įprastos** ir **Viršvalandžiai** , pritaikykite antkainį darbui pasibaigus.


1. Eikite į **Parametrai** > **Sprendimai** , o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Parinkčių rinkiniai**. 
3. Pasirinkite **Naujas** , kad sukurtumėte naują parinkčių rinkinį, įveskite trūkstamą būtiną informaciją, tada pasirinkite **Įrašyti**.

## <a name="create-data-for-entity-based-dimensions"></a>Objekto dimensijų duomenų kūrimas

Objektų dimensijų duomenis galite kurti rankiniu būdu arba naudodami „Microsoft Excel“ importavimo ar aptarnavimo komandų iškvietimą. Atlikite šioje procedūroje nurodytus veiksmus, kad du standartinius pavadinimus – **Sistemų inžinierius** ir **Vyresnysis sistemų inžinierius** – sukurtumėte pagal objekto dimensijos **standartinį pavadinimą**. Jei duomenys, kuriuos norite sukurti, yra maži, kaip toliau pateiktame pavyzdyje, galite naudoti standartinę formą.

1. Pažymėkite **Išplėstinė ieška** , pažymėkite objekto **standartinį pavadinimą** ir pasirinkite **Rezultatai**. Bus rodomos visos objekto **Standartinis pavadinimas** eilutės.
2. Pasirinkite **Naujas** ir lauke **Pavadinimas** įveskite „Sistemos inžinierius“ ir pasirinkite **Įrašyti**.
3. Uždarykite formą. 
4. Pakartokite 1–3 veiksmus, kad sukurtumėte kitą standartinį vyresniojo sistemų inžinieriaus pavadinimą.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Visų reikiamų objektų ir susijusių komponentų įtraukimas į kainodaros dimensijos sprendimą
Į kainodaros sprendimą turėsite įtraukti toliau nurodytus objektus. Atlikite šioje procedūroje nurodytus veiksmus, kad atliktumėte svarbių kainodaros sprendimo schemos pakeitimų ir objektai žinotų apie naujas kainodaros dimensijas.

1. Pasirinkite **Parametrai** > **Sprendimai** , o tada dukart spustelėkite **\<your organization name> kainodaros dimensijas**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Pridėti esamus** > **Objektai**.
3. Dialogo lange **Sprendimo komponentas** pasirinkite toliau nurodytus objektus.

  - Faktinis
  - Rezervuojami ištekliai
  - Įvertinimo eilutė
  - Sąskaitos faktūros eilutės informacija
  - Žurnalo eilutė
  - Projekto sutarties eilutės informacija
  - Projekto komandos narys
  - Pasiūlymo eilutės informacija
  - Vaidmens kainos antkainis
  - Vaidmens kaina 
  - Laiko įrašas 


> [!NOTE]
> Būtinai įtraukite visas kiekvieno pasirinkto objekto formas ir rodinius.

4. Paraginti įtraukti priklausomus objektus iš pirmiau pasirinktų objektų, spustelėkite **Ne**.

