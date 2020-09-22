---
title: Pasirinktinių laukų ir objektų kūrimas
description: Šioje temoje paaiškinama, kaip kurti parinkčių rinkinius ir objektus naudojant asmeninį sprendimą Power Apps platformoje.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753761"
---
# <a name="create-custom-fields-and-entities"></a>Pasirinktinių laukų ir objektų kūrimas 

Atlikite toliau nurodytus veiksmus bet kuriuo metu, kai norite sukurti pasirinktinį parinkčių rinkinį arba objektą „Power Apps“ platformoje.  
Šioje temoje nurodytas procedūras reikia atlikti naudojant „Project Service Automation“ (PSA) internetinę sąsają.

> [!IMPORTANT]
> Rekomenduojame visus pasirinktinio kainodaros dimensijų pakeitimus atlikti naudojant atskirą sprendimą. Ši svarbi geriausia praktika suteikia lankstumo ateityje siekiant tinkamai atnaujinti arba pašalinti pakeitimus ir padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių. Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima pakartotinai naudoti kainodaros nustatymus.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Pasirinktinio sprendimo kainodaros dimensijoms kūrimas
1. Naudodami PSA spustelėkite **Parametrai** > **Sprendimai**, tada spustelėkite **Naujas** ir sukurkite naują sprendimą. 
2. Pavadinkite sprendimą (**\<organizacijos pavadinimas > kainodaros dimensijos**), įveskite likusią reikiamą informaciją, tada spustelėkite **Įrašyti**.

> ![Pasirinktinio sprendimo kainodaros dimensijoms kūrimas](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Pasirinktinių laukų ir parinkčių rinkinių kūrimas kainodaros dimensijos sprendime

Kainodaros dimensija gali būti parinkčių rinkinys arba objektas. Abu turi būti sukurti jūsų kainodaros sprendime. Šioje procedūroje nurodytuose veiksmuose paaiškinta, kaip kurti objekto dimensijas ir parinkčių rinkinio dimensijas.

### <a name="entity-based-dimensions"></a>Objekto dimensijos

1. (PSA) spustelėkite **„Parametrai“** > **„Sprendimai“**, tada dukart spustelėkite **\<organizacijos pavadinimas > kainų dimensijos**.
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Objektai**.
3. Spustelėkite **Naujas**, kad sukurtumėte naują objektą pavadinimu **Standartinis pavadinimas**. Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.

> ![Standartinio pavadinimo objekto apibrėžtis](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Parinkčių rinkinio matmenys 
Galite sukurti du parinkčių rinkinio matmenis. Pasinaudokite lauku **Išteklių darbo vieta** ir sekite darbą **namų** vietoje bei **darbo vietoje**, o pasinaudodami lauku **Išteklių darbo valandos**, su vertėmis **Įprastos** ir **Viršvalandžiai**, pritaikykite antkainį darbui pasibaigus.


1. Apsilankę PSA spustelėkite **Parametrai** > **Sprendimai**, tada dukart spustelėkite **\<organizacijos pavadinimas > kainų dimensijos**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Parinkčių rinkiniai**. 
3. Spustelėkite **Naujas**, kad sukurtumėte naują parinkčių rinkinį, įveskite trūkstamą būtiną informaciją, tada spustelėkite **Įrašyti**.

> ![Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo vieta“ ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo valandos“ ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Objekto dimensijų duomenų kūrimas

Objektų dimensijų duomenis galite kurti rankiniu būdu arba naudodami „Microsoft Excel“ importavimo ar aptarnavimo komandų iškvietimą. Atlikite šioje procedūroje nurodytus veiksmus, kad du standartinius pavadinimus – **Sistemų inžinierius** ir **Vyresnysis sistemų inžinierius** – sukurtumėte pagal objekto dimensijos **standartinį pavadinimą**. Jei duomenys, kuriuos norite sukurti, yra maži, kaip toliau pateiktame pavyzdyje, galite naudoti standartinę formą.

1. Apsilankę PSA spustelėkite **Išplėstinė ieška**. Pasirinkite objektą **Standartinis pavadinimas**, tada spustelėkite **Rezultatai**. Bus rodomos visos objekto **Standartinis pavadinimas** eilutės.
2. Spustelėkite **Naujas**. Lauke **Pavadinimas** įveskite „Sistemų inžinierius“, tada spustelėkite **Įrašyti**.
3. Uždarykite formą. 
4. Pakartokite 1–3 veiksmus, kad sukurtumėte kitą standartinį vyresniojo sistemų inžinieriaus pavadinimą.

> ![Standartinio pavadinimo objekto duomenų pavyzdžiai ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Visų reikiamų PSA objektų ir susijusių komponentų įtraukimas į kainodaros dimensijos sprendimą
Į kainodaros sprendimą turėsite įtraukti toliau nurodytus „Project Service“ objektus. Atlikite šioje procedūroje nurodytus veiksmus, kad atliktumėte svarbių kainodaros sprendimo schemos pakeitimų ir objektai žinotų apie naujas kainodaros dimensijas.

1. (PSA) spustelėkite **„Parametrai“** > **„Sprendimai“**, tada dukart spustelėkite **\<organizacijos pavadinimas > kainų dimensijos**. 
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

> ![Esamų objektų įtraukimas į kainodaros dimensijų sprendimą](media/Existing-entities-to-PD-solution.png)

> ![Sprendimo komponentų pasirinkimas](media/Dimension-Components.png)

> [!NOTE]
> Būtinai įtraukite visas kiekvieno pasirinkto objekto formas ir rodinius.

4. Paraginti įtraukti priklausomus objektus iš pirmiau pasirinktų objektų, spustelėkite **Ne**.

> ![Neįtraukite visų susijusių komponentų](media/Do-not-include-required.png)


