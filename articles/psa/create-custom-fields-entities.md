---
title: Pasirinktinių laukų ir objektų kūrimas
description: Šioje temoje paaiškinama, kaip kurti parinkčių rinkinius ir objektus naudojant asmeninį sprendimą Power Apps platformoje.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d2fbe6a4061a93ac3186bbc8624bf5d16209cdf9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574394"
---
# <a name="create-custom-fields-and-entities"></a>Pasirinktinių laukų ir objektų kūrimas 

[!include [banner](../includes/psa-now-project-operations.md)]

Atlikite toliau nurodytus veiksmus bet kuriuo metu, kai norite sukurti pasirinktinį parinkčių rinkinį arba objektą „Power Apps“ platformoje.  
Šioje temoje nurodytas procedūras reikia atlikti naudojant „Project Service Automation“ (PSA) internetinę sąsają.

> [!IMPORTANT]
> Rekomenduojame visus pasirinktinio kainodaros dimensijų pakeitimus atlikti naudojant atskirą sprendimą. Ši svarbi geriausia praktika suteikia lankstumo ateityje siekiant tinkamai atnaujinti arba pašalinti pakeitimus ir padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių. Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima pakartotinai naudoti kainodaros nustatymus.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Pasirinktinių laukų ir parinkčių rinkinių kūrimas kainodaros dimensijos sprendime

Kainodaros dimensija gali būti parinkčių rinkinys arba objektas. Abu turi būti sukurti jūsų kainodaros sprendime. Šioje procedūroje nurodytuose veiksmuose paaiškinta, kaip kurti objekto dimensijas ir parinkčių rinkinio dimensijas.

### <a name="entity-based-dimensions"></a>Objekto dimensijos

1. PSA pasirinkite **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Objektai**.
3. Spustelėkite **Naujas**, kad sukurtumėte naują objektą pavadinimu **Standartinis pavadinimas**. Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.

> ![Standartinio pavadinimo objekto apibrėžtis.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Parinkčių rinkinio matmenys 
Galite sukurti du parinkčių rinkinio matmenis. Pasinaudokite lauku **Išteklių darbo vieta** ir sekite darbą **namų** vietoje bei **darbo vietoje**, o pasinaudodami lauku **Išteklių darbo valandos**, su vertėmis **Įprastos** ir **Viršvalandžiai**, pritaikykite antkainį darbui pasibaigus.


1. PSA pasirinkite **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Parinkčių rinkiniai**. 
3. Spustelėkite **Naujas**, kad sukurtumėte naują parinkčių rinkinį, įveskite trūkstamą būtiną informaciją, tada spustelėkite **Įrašyti**.

> ![Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo vieta“.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo valandos“.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Objekto dimensijų duomenų kūrimas

Objektų dimensijų duomenis galite kurti rankiniu būdu arba naudodami „Microsoft Excel“ importavimo ar aptarnavimo komandų iškvietimą. Atlikite šioje procedūroje nurodytus veiksmus, kad du standartinius pavadinimus – **Sistemų inžinierius** ir **Vyresnysis sistemų inžinierius** – sukurtumėte pagal objekto dimensijos **standartinį pavadinimą**. Jei duomenys, kuriuos norite sukurti, yra maži, kaip toliau pateiktame pavyzdyje, galite naudoti standartinę formą.

1. Apsilankę PSA spustelėkite **Išplėstinė ieška**. Pasirinkite objektą **Standartinis pavadinimas**, tada spustelėkite **Rezultatai**. Bus rodomos visos objekto **Standartinis pavadinimas** eilutės.
2. Spustelėkite **Naujas**. Lauke **Pavadinimas** įveskite „Sistemų inžinierius“, tada spustelėkite **Įrašyti**.
3. Uždarykite formą. 
4. Pakartokite 1–3 veiksmus, kad sukurtumėte kitą standartinį vyresniojo sistemų inžinieriaus pavadinimą.

> ![Standartinio pavadinimo objekto duomenų pavyzdžiai.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
