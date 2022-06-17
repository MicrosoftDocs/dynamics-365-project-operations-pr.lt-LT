---
title: Sprendimo pasirinktinėms kainodaros dimensijoms kūrimas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip kurti pasirinktinių kainodaros dimensijų sprendimus.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cd7fedaa7bece16e99131bcc0faff3ce547580e8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915148"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Sprendimo pasirinktinėms kainodaros dimensijoms kūrimas

 _**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_ 

>[!IMPORTANT]
>Visi pasirinktinės kainodaros dimensijos pokyčiai turi būti atskirame sprendime. Ši svarbi geriausios praktikos procedūra suteikia galimybę lanksčiai atnaujinti arba pašalinti pakeitimus, padeda pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitus egzempliorius. Atlikę reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima naudoti pakartotinai.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Sprendimo pasirinktinėms kainodaros dimensijoms kūrimas

1.  Pasirinkite **Nustatymai** > **Sprendimai** ir spauskite **Naujas**.
2.  Sukurkite sprendimo pavadinimą: *\<your organization name\> kainodaros dimensijos*.
3. Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.

  ![Pasirinktinių kainodaros dimensijų sprendimo kūrimas.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Pridėkite visus reikalingus objektus ir susijusius komponentus į kainodaros dimensijos sprendimą

Pridėkite toliau nurodytus „Project Service“ objektus prie savo kainodaros sprendimo, kad atliktumėte svarbius schemos pakeitimus, susijusius su kainodaros sprendimu. Atlikus šią procedūrą, objektai atpažins naujas kainodaros dimensijas.

1.  Pasirinkite **Parametrai** > **Sprendimai**, tada dukart spustelėkite **<*jūsų organizacijos pavadinimas*> kainodaros dimensijos**.
2.  Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Pridėti esamus** > **Objektai**.
3.  Dialogo lange **Sprendimo komponentas** pasirinkite toliau nurodytus objektus.
 
   - **Faktinis**
   - **Rezervuojamas išteklius**
   - **Įvertinimo eilutė**
   - **Projekto užduotis**
   - **Sąskaitos faktūros eilutės informacija**
   - **Žurnalo eilutė**
   - **Projekto sutarties eilutės informacija**
   - **Projekto komandos narys**
   - **Pasiūlymo eilutės informacija**
   - **Vaidmens kainos antkainis**
   - **Vaidmens kaina**
   - **Laiko įrašas**
 
   ![Esamų objektų įtraukimas į pasirinktinių kainodaros dimensijų sprendimą.](./media/Existing-entities-to-PD-solution.png)
 
 4. Peržiūrėkite kiekvieno objekto pridedamus komponentus ir kiekvieno objekto galutinį objekto išteklių sąrašą. 

   >[!NOTE]
   > Įtraukite visas kiekvieno pasirinkto objekto formas ir rodinius.

  ![Pridėti objektai.](./media/solution-component-selection.png)


5.  Kai būsite paraginti įtraukti bet kokius pasirinktų objektų priklausomuosius objektus, pasirinkite **Ne, būtinųjų komponentų įtraukti nereikia.**

    ![Priklausomųjų objektų įtraukimas.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]