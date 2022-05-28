---
title: Projektų biudžetų perkėlimas finansinių metų pabaigoje
description: Šiame straipsnyje pateikiama informacija apie tai, kaip perkelti likusias biudžeto sumas į ateinančius metus ir sukurti išsamią biudžeto registro informaciją.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5b4e768cb78d6a6cb76b3c338fd76363d5290ebd
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684054"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Projektų biudžetų perkėlimas finansinių metų pabaigoje

[!include [banner](../includes/banner.md)]

Dirbdami su daugiamečiu projektu, finansinių metų pabaigoje galite turėti likusių biudžeto lėšų. Likusias biudžeto sumas galite perkelti į būsimus metus ir sukurti jų biudžeto registro duomenis susijusiose didžiosios knygos sąskaitose. Prieš perkeldami likusias biudžeto sumas peržiūrėkite jas ir išanalizuokite.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Likusių biudžeto sumų peržiūra ir analizė

Atlikite toliau nurodytus veiksmus norėdami peržiūrėti projektų metų pabaigos biudžeto sumas, bet sumų neperkelkite.

1. Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Biudžetai** > **Perkelti biudžetus**. 
2. Puslapio **Projekto biudžeto perkėlimo procesas** skirtuke **Metų pabaigos parinktys** patikrinkite, ar neįjungta **Perkelti likusias projekto biudžeto sumas**.
3. Skirtuko **Parametrai** lauke **Projekto biudžeto metai** pasirinkite finansinius metus, kurių likusią biudžeto sumą norite peržiūrėti. 
4. Lauke **Finansinių metų atidarymas** pasirinkite finansinius metus, kurių likusią biudžeto sumą norite peržiūrėti. 
5. Lauke **Iš prognozės modelio** pasirinkite **Likęs biudžetas**. 
6. Jei norite įtraukti projektus, atitinkančius jūsų pasirinktus kriterijus ir neturinčius likusio biudžeto, pasirinkite **Rodyti nulinį likutį**.  
7. Skirtuke **Pasirinkti biudžetus** pasirinkite **Nuskaityti visus biudžetus** norėdami įkelti visus biudžetus, kurie atitinka jūsų pasirinktus kriterijus, tada pasirinkite **Apdoroti**. 
8. Norėdami sukurti duomenų bazės užklausą, kuri į sritį įkelia tam tikrą biudžetų rinkinį, pasirinkite **Nuskaityti pasirinktus biudžetus**.

Norėdami gauti daugiau informacijos apie tam tikrą srities eilutę, ją pasirinkite ir pažymėkite **Peržiūrėti biudžeto informaciją** arba **Peržiūrėti sąskaitas**.

## <a name="carry-forward-remaining-budget-amounts"></a>Likusių biudžeto sumų perkėlimas 

Kai apdorojate likusias biudžeto sumas, galite sukurti perkeliamų sumų operacijas didžiojoje knygoje. Norėdami sukurti didžiosios knygos operacijas, atlikite veiksmus, nurodytus skyriuje [Biudžeto sumų perkėlimas ir didžiosios knygos operacijų kūrimas](#carry-forward). 

> [!NOTE]
> Perkeltos biudžeto sumos perkeliamos į prognozės modelį, kuris puslapyje **Prognozės modeliai** yra pasirinktas kaip perkėlimo prognozės modelis.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Biudžeto sumų perkėlimas ir didžiosios knygos operacijų kūrimas

1.  Pasirinkite **Projektų valdymas ir apskaita** > **Periodinis** > **Biudžetai** > **Perkelti biudžetus**. 
2. Puslapyje **Projekto biudžeto perkėlimo procesas** pasirinkite **Metų pabaiga**, tada įjunkite **Perkelti likusias projekto biudžeto sumas** ir **Sukurti biudžeto registro įrašus didžiojoje knygoje**. 
3. Skirtuke **Parametrai**, laukų grupėje **Projekto parametrai**, pasirinkite tai:

   - **Projekto biudžeto metai**: pasirinkite finansinių metų, kurių likusias biudžeto sumas norite peržiūrėti, pradžią. 
   - **Pelnas ir nuostolis**: sukurkite pelno ir nuostolio operacijas didžiojoje knygoje. 
   -  **NG**: sukurkite nebaigtos gamybos (NG) operacijas didžiojoje knygoje.
   -  **Algalapis**: sukurkite algalapio paskirstymo operacijas didžiojoje knygoje. 

5. Laukų grupėje **Didžioji knyga** pateikite nurodytą informaciją: 

   - Lauke **Finansinių metų atidarymas** pasirinkite finansinius metus, kurių likusias projektų biudžetų sumas norite perkelti. Numatytoji reikšmė yra vieneri metai po lauke **Projekto biudžeto metai** nurodytos reikšmės.
   -  Lauke **Perkėlimo laikotarpis** pasirinkite laikotarpį, kurio biudžeto registro duomenis norite sukurti didžiojoje knygoje. Paprastai tai yra pirmasis atidarytų finansinių metų laikotarpis.

6. Laukų grupėje **Kopijuoti iš / į** pateikite nurodytą informaciją:

   - Lauke **Iš prognozės modelio** pasirinkite projekto biudžeto prognozės modelį, susietą su likusiomis projektų biudžetų sumomis, kurias norite perkelti. 
   - Lauke **Į didžiosios knygos biudžeto modelį** pasirinkite didžiosios knygos biudžeto modelį, susietą su biudžetų sumomis, kurias norite perkelti į didžiąją knygą. 
   -  Pasirinkite **Perkelti pardavimo valiutą** norėdami naudoti didžiosios knygos operacijų, sukuriamų perkeliant projektų biudžetų sumas, projekto pardavimo valiutą. Kai parinktis nepažymėta, operacijose naudojama apskaitos valiuta. 
   -  Pasirinkite **Rodyti likutinį nulį**, kad būtų įtraukti projektai, kuriuose nėra likusių biudžeto sumų, bet atitinka kitus kriterijus, kuriuos pasirinkote apatinėje srityje rodomuose projektuose.

7. Skirtuke **Pasirinkti biudžetus** pasirinkite **Nuskaityti visus biudžetus** norėdami įkelti visus biudžetus, kurie atitinka jūsų pasirinktus kriterijus. Norėdami sukurti duomenų bazės užklausą, kuri į sritį įkelia tam tikrą projektų biudžetų rinkinį, pasirinkite **Nuskaityti pasirinktus biudžetus**.
8. Pasirinkite kiekvieno projekto, kurį norite apdoroti, parinktį, esančią projekto eilutės pradžioje.

    > [!TIP]
    > Jei norite pasirinkti visus arba daugelį projektų, pažymėkite varnelę viršutiniame kairiajame kampe. Jei kurio nors projekto apdoroti nenorite, pašalinkite jo varnelę.

9. Jei norite perkelti likusias pasirinktų projektų biudžetų sumas į pasirinktus finansinius metus ir sukurti biudžeto registro duomenis didžiojoje knygoje, pažymėkite **Apdoroti**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Biudžeto sumų perkėlimas nekuriant didžiosios knygos operacijų

1. Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Biudžetai** > **Perkelti biudžetus**.
2. Puslapio **Projekto biudžeto perkėlimo procesas** lauke **Metų pabaigos parinktys** pasirinkite **Perkelti likusias projekto biudžeto sumas**.
3. Grupės **Parametrai** lauke **Projekto biudžeto metai** pasirinkite finansinius metus, kurių likusias biudžeto sumas norite peržiūrėti.
4. Grupėje **Kopijuoti iš / į** pateikite nurodytą informaciją:

   - Lauke **Iš prognozės modelio** pasirinkite projekto biudžeto prognozės modelį, susietą su likusiomis projektų biudžetų sumomis, kurias norite perkelti. 
   - Pasirinkite **Rodyti nulinį likutį**, jei norite įtraukti projektus, neturinčius likusių biudžeto sumų, bet atitinkančius kitus jūsų pasirinktus kriterijus.
   - Grupėje **Pasirinkti biudžetus** pasirinkite **Nuskaityti visus biudžetus** norėdami įkelti visus biudžetus, kurie atitinka jūsų pasirinktus kriterijus. Norėdami sukurti duomenų bazės užklausą, kuri į sritį įkelia tam tikrą projektų biudžetų rinkinį, pasirinkite **Nuskaityti pasirinktus biudžetus**.

5. Pasirinkite kiekvieno projekto, kurį norite apdoroti, parinktį, esančią projekto eilutės pradžioje. 
6. Pasirinkite **Apdoroti**, jei norite perkelti likusias pasirinktų projektų biudžetų sumas į pasirinktus finansinius metus.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
