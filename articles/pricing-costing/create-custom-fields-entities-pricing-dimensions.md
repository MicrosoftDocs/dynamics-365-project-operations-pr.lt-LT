---
title: Pasirinktinių laukų ir objektų kūrimas kaip kainodaros dimensijų
description: Šioje temoje pateikta informacija apie tai, kaip kurti pasirinktinių parinkčių rinkinius arba objektus.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642823"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Pasirinktinių laukų ir objektų kūrimas kaip kainodaros dimensijų

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Atlikite toliau nurodytus veiksmus, kai norite sukurti pasirinktinį parinkčių rinkinį arba objektą, skirtą naudoti kaip kainodaros dimensija. Norėdami gauti daugiau informacijos, žr. [Kainodaros dimensijų apžvalga](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Rekomenduojame visus pasirinktinio kainodaros dimensijų pakeitimus atlikti naudojant atskirą sprendimą. Ši svarbi geriausia praktika suteikia lankstumo ateityje, prireikus atnaujinti arba pašalinti pakeitimus. Tai padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima pakartotinai naudoti kainodaros nustatymus.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Pasirinktinių laukų ir parinkčių rinkinių kūrimas kainodaros dimensijos sprendime

Kainodaros dimensija gali būti parinkčių rinkinys arba objektas. Abu turi būti sukurti jūsų kainodaros sprendime. Šioje procedūroje nurodytuose veiksmuose paaiškinta, kaip kurti objekto dimensijas ir parinkčių rinkinio dimensijas.

### <a name="entity-based-dimensions"></a>Objekto dimensijos
Jei norite kurti objekto dimensijas, atlikite toliau nurodytus veiksmus:

1. Eikite į **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Objektai**.
3. Pasirinkite **Naujas**, kad sukurtumėte naują objektą pavadinimu **Standartinis pavadinimas**. 
4. Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.

> ![Standartinio pavadinimo objekto apibrėžtis](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Parinkčių rinkinio matmenys 
Galite sukurti du parinkčių rinkinio matmenis. 

- Pasinaudokite lauku **Išteklių darbo vieta** ir sekite darbą **namų** vietoje bei **darbo vietoje**. 
- Pasinaudodami lauku **Išteklių darbo valandos**, su reikšmėmis **Įprastos** ir **Viršvalandžiai**, pritaikykite antkainį darbui pasibaigus.

Toliau esančiame grafiniame vaizde pateikiamas **išteklių darbo vietos** dimensijos rodinys. 

> ![Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo vieta“](media/Option-set-PD-called-Resource-Work-Location.png)

Toliau esančiame grafiniame vaizde pateikiamas **išteklių darbo valandų** dimensijos rodinys. 

> ![Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo valandos“](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Eikite į **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Parinkčių rinkiniai**. 
3. Pasirinkite **Naujas**, kad sukurtumėte naują parinkčių rinkinį, įveskite trūkstamą būtiną informaciją, tada pasirinkite **Įrašyti**.

## <a name="create-data-for-entity-based-dimensions"></a>Objekto dimensijų duomenų kūrimas

Objektų dimensijų duomenis galite kurti rankiniu būdu arba naudodami „Microsoft Excel“ importavimo ar aptarnavimo komandų iškvietimą. Atlikite šioje procedūroje nurodytus veiksmus, kad du standartinius pavadinimus – **Sistemų inžinierius** ir **Vyresnysis sistemų inžinierius** – sukurtumėte pagal objekto dimensijos **standartinį pavadinimą**. Jei duomenys, kuriuos norite sukurti, yra maži, kaip toliau pateiktame pavyzdyje, galite naudoti standartinę formą.

1. Pasirinkite **Išplėstinė ieška**.
2. Pasirinkite objektą **Standartinis pavadinimas**, o tada pasirinkite **Rezultatai**. Bus rodomos visos objekto **Standartinis pavadinimas** eilutės.
3. Pasirinkite **Naujas** ir lauke **Pavadinimas** įveskite „Sistemos inžinierius“ ir pasirinkite **Įrašyti**.
4. Uždarykite puslapį. 
5. Pakartokite 1–3 veiksmus, kad sukurtumėte kitą standartinį vyresniojo sistemų inžinieriaus pavadinimą.

> ![Standartinio pavadinimo objekto duomenų pavyzdžiai](media/ST-data.png)
