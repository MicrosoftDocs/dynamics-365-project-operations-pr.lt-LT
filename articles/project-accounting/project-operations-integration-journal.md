---
title: Integravimo žurnalas programoje „Project Operations“
description: Šioje temoje pateikiama informacija apie darbą su integravimo žurnalu programoje „Project Operations”.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ffe3373184c8cd776bf3705fd674bedf221d9b77
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133396"
---
# <a name="integration-journal-in-project-operations"></a>Integravimo žurnalas programoje „Project Operations“

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Laiko ir išlaidų įrašai sukuria operacijas **Faktinės**, kurios atitinka pagal projektą užbaigto darbo veiklos rodinį. „Dynamics 365 Project Operations” teikia buhalterius, turinčius įrankį, skirtą operacijoms peržiūrėti ir apskaitos atributams koreguoti, kai reikia. Užbaigus peržiūrą ir koregavimus, operacijos skelbiamos projekto papildomoje knygoje ir didžiojoje knygoje. Buhalteris gali vykdyti šias veiklas naudodamas **„Project Operations“ integravimo** žurnalą (**„Dynamics 365 Finance”** > **Projektų valdymas ir apskaita** > **Žurnalai** > **„Project Operations“ integravimo** žurnalas.

![Integravimo žurnalo srautas](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Įrašų kūrimas „Project Operations“ integravimo žurnale

Įrašai „Project Operations“ integravimo žurnale įrašai kuriami naudojant periodinį procesą, **Importuoti iš paruošimo lentelės**. Šį procesą galite vykdyti eidami į **„Dynamics 365 Finance”** > **Projektų valdymas ir apskaita** > **Periodinis** > **„Project Operations“ integravimas** > **Importuoti iš paruošimo lentelės**. Jeigu reikia, galite vykdyti procesą interaktyviai arba sukonfigūruoti procesą, kad veiktų fone.

Vykdant periodinį procesą, randami visi faktiniai duomenys, kurie dar neįtraukti į „Project Operations“ integravimo žurnalą. Sukuriama kiekvienos faktinės operacijos žurnalo eilutė.
Sistema grupuoja žurnalo eilutes į atskirus žurnalus pagal vertę, pažymėtą lauke **Laiko vienetas „Project Operations“ integravimo žurnale** (**„Finance”** > **Projektų valdymas ir apskaita** > **Sąranka** > **Projektų valdymo ir apskaitos parametrai**, **„Project Operations”, veikiančios „Dynamics 365 Customer Engagement”** _ skirtukas). Toliau pateikiamos galimos šio lauko reikšmės.

  - _*Dienos**: faktiniai duomenys grupuojami pagal operacijos datą. Sukuriamas atskiras kiekvienos dienos žurnalas.
  - **Mėnesiai**: faktiniai duomenys grupuojami pagal kalendorinį mėnesį. Sukuriamas atskiras kiekvieno mėnesio žurnalas.
  - **Metai**: faktiniai duomenys grupuojami pagal kalendorinius metus. Sukuriamas atskiras kiekvienų metų žurnalas.
  - **Visi**: visos faktinės operacijos įtraukiamos į tą patį integravimo žurnalą. Jei vykdant periodinį procesą, žurnalas nepasiekiamas, pvz., jei žurnale vykdomas operacijų skelbimo procesas, sukuriamas naujas žurnalas.

Žurnalo eilutės kuriamos pagal projekto faktinius duomenis. Toliau pateiktame sąraše nurodytos kelios svarbios numatytųjų nustatymų ir transformacijos taisyklės.

  - Kiekvieno projekto faktinė operacija turi eilutę „Project Operations“ integravimo žurnale. Išlaidų operacijos ir pardavimo operacijos, kurioms neišrašyta sąskaita, priklausančios laiko ir medžiagų atsiskaitymo tipui, rodomos atskirose eilutėse.
  - Lauke **Data** nurodoma operacijos data. Lauke **Apskaitos data** nurodoma data, kai operacija buvo įrašyta į knygą. Jei apskaitos data yra [uždarytame finansiniame laikotarpyje](https://docs.microsoft.com/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), o parametras **Automatiškai nustatyti apskaitos datą, siekiant atidaryti knygos laikotarpį** nustatytas skirtuke **Finansų**, esančiame puslapyje **Projektų valdymo ir apskaitos parametrai**, sistema koreguos operacijos apskaitos datą į pirmą kito atidaryto knygos laikotarpio datą.
  - Lauke **Kvitas** rodomas kiekvienos faktinės operacijos kvito numeris. Kvitų numerių seka yra nurodyta puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **Numerių sekos**. Kiekvienai eilutei priskiriamas naujas numeris. Paskelbę kvitą, galite peržiūrėti, kaip yra susijusios išlaidų operacijos ir pardavimo operacijos, kurioms neišrašyta sąskaita, pasirinkdami **Susiję kvitai** puslapyje **Kvito operacija**.
  - Laukas **Kategorija** atitinka projekto operaciją ir numatytąsias reikšmes pagal susijusio projekto faktinių duomenų operacijos kategoriją.
    - Jei **Operacijos kategorija** nustatyta projekto faktiniuose duomenyse, o susijusi **Projekto kategorija** yra nurodytame juridiniame subjekte, pagal numatytuosius nustatymus kategorija priskiriama šiai projekto kategorijai.
    - Jeigu **Operacijos kategorija** nenustatyta projekto faktiniuose duomenyse, sistema naudoja reikšmę, esančią puslapio **Projektų valdymo ir apskaitos parametrai** skirtuko **„Project Operations” programoje „Dynamics 365 Customer Engagement”** lauke **Projekto kategorijos numatytieji nustatymai**.
  - Laukas **Ištekliai** atitinka projekto išteklius, susijusius su šia operacija. Šie ištekliai naudojami kaip nuoroda projekto sąskaitų faktūrų pasiūlymuose klientams.
  - Laukas **Valiutos kursas** nustatomas pagal numatytuosius nustatymus iš **Valiutos kurso**, nustatyto „Dynamics 365 Finance”. Jeigu valiutos kurso sąrankos nėra, periodinis procesas **Importuoti iš paruošimo** neįtrauks įrašo į žurnalą ir klaidos pranešimas bus įtrauktas į užduoties vykdymo žurnalą.
  - Laukas **Eilutės ypatybės** atitinka atsiskaitymo tipą projekto faktiniuose duomenyse. Eilutės ypatybės ir atsiskaitymo tipo susiejimas apibrėžiami puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **„Project Operations” programoje „Dynamics 365 Customer Engagement”**.

Tik toliau pateikiami apskaitos atributai gali būti atnaujinti „Project Operations” integravimo žurnalo eilutėse.

- **Atsiskaitymo PVM grupė** ir **Atsiskaitymo elemento PVM grupė**
- **Finansinės dimensijos** (naudojant veiksmą **Paskirstyti sumas**)

Integravimo žurnalo eilutes galima panaikinti, tačiau iš naujo paleidus periodinį procesą **Importuoti iš paruošimo**, visos neužregistruotos eilutės bus vėl įterptos į žurnalą.

Kai registruojate integravimo žurnalą, sukuriamos projekto antrinės knygos ir DK operacijos. Jos naudojamos toliau sąskaitas faktūras klientams teikti, pajamoms pripažinti ir finansinėms ataskaitoms teikti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]