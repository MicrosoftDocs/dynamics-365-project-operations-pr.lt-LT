---
title: Sukurti pasirinktinius sprendimus kainodaros dimensijoms
description: Šioje temoje aiškinama, kaip sukurti pasirinktinį sprendimą kuriant pasirinktines kainodaros dimensijas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080845"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Sukurti pasirinktinius sprendimus kainodaros dimensijoms

> [!IMPORTANT]
> Visi pasirinktinės kainodaros dimensijos pokyčiai turi būti atskirame sprendime. Ši svarbi geriausia praktika suteikia lankstumo ateityje siekiant tinkamai atnaujinti arba pašalinti pakeitimus ir padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių. Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus atvejus pakartotiniam kainodaros nustatymui.

1. Pasirinkite **Nustatymai** > **Sprendimai** ir spauskite **Naujas**. 
2. Pavadinkite sprendimą **\<your organization name>kainodaros dimensijos** , įveskite likusią reikiamą informaciją, tada spustelėkite **Įrašyti**.

> ![Pasirinktinio sprendimo kainodaros dimensijoms kūrimas](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Pridėkite visus reikalingus objektus ir susijusius komponentus į kainodaros dimensijos sprendimą
Į kainodaros sprendimą turėsite įtraukti toliau nurodytus „Project Service“ objektus. Užbaikite šioje procedūroje nurodytus veiksmus, kad atliktumėte svarbius kainodaros sprendimo schemos pakeitimus ir, kad objektai sužinotų apie naujas kainodaros dimensijas.

1. Pasirinkite **Parametrai** > **Sprendimai** , o tada dukart spustelėkite **\<your organization name> kainodaros dimensijas**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Pridėti esamus** > **Objektai**.
3. Dialogo lange **Sprendimo komponentas** pasirinkite toliau nurodytus objektus.

- Faktinis
- Rezervuojamas išteklius
- Įvertinimo eilutė
- Projekto užduotis
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

4. Paraginti įtraukti bet kokius priklausomus objektus iš pasirinktų objektų, spauskite **Ne**.

> ![Neįtraukite visų susijusių komponentų](media/Do-not-include-required.png)

