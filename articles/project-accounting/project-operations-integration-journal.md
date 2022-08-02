---
title: Integravimo žurnalas programoje „Project Operations“
description: Šiame straipsnyje pateikiama informacija apie darbą su "Project Operations" žurnalu Integravimas.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106285"
---
# <a name="integration-journal-in-project-operations"></a>Integravimo žurnalas programoje „Project Operations“

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Laikas, išlaidos, mokestis ir reikšmingi įrašai sukuria **faktines operacijas**, kurios atspindi pagal projektą atlikto darbo veiklos rodinį. „Dynamics 365 Project Operations“ teikia apskaitininkams įrankį, skirtą operacijoms peržiūrėti ir apskaitos atributams koreguoti, kai reikia. Užbaigus peržiūrą ir koregavimus, operacijos skelbiamos projekto papildomoje knygoje ir didžiojoje knygoje. Buhalteris gali atlikti šią veiklą naudodamas žurnalą **"Project Operations Integration**" (**Dynamics 365 Finance** > **projektų valdymo ir apskaitos** > **žurnalų** > **"Project Operations Integration**".

![Integravimo žurnalo srautas.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Įrašų kūrimas „Project Operations“ integravimo žurnale

Įrašai „Project Operations“ integravimo žurnale įrašai kuriami naudojant periodinį procesą, **Importuoti iš paruošimo lentelės**. Šį procesą galite vykdyti nuėję į **Dynamics 365 Finance** > **Projekto valdymas ir apskaita** > **Periodinių** > **projektų operacijų integravimas** > **Importavimas iš išdėstymo lentelės**. Jeigu reikia, galite vykdyti procesą interaktyviai arba sukonfigūruoti procesą, kad veiktų fone.

Vykdant periodinį procesą, randami visi faktiniai duomenys, kurie dar neįtraukti į „Project Operations“ integravimo žurnalą. Sukuriama kiekvienos faktinės operacijos žurnalo eilutė.
Sistema sugrupuoja žurnalo eilutes į atskirus žurnalus pagal reikšmę, pasirinktą lauke Laikotarpio vienetas, esančiame projekto operacijų integravimo žurnale ("Finance **Project management and accounting Setup Project management and accounting** Setup **Project management and accounting parameters** > **",** > **"Project Operations on Dynamics 365 Customer Engagement** > **" skirtuke).** **·** Toliau pateikiamos galimos šio lauko reikšmės.

  - **Dienos**: faktiniai duomenys grupuojami pagal operacijos datą. Sukuriamas atskiras kiekvienos dienos žurnalas.
  - **Mėnesiai**: faktiniai duomenys grupuojami pagal kalendorinį mėnesį. Sukuriamas atskiras kiekvieno mėnesio žurnalas.
  - **Metai**: faktiniai duomenys grupuojami pagal kalendorinius metus. Sukuriamas atskiras kiekvienų metų žurnalas.
  - **Visi**: visos faktinės operacijos įtraukiamos į tą patį integravimo žurnalą. Jei vykdant periodinį procesą, žurnalas nepasiekiamas, pvz., jei žurnale vykdomas operacijų skelbimo procesas, sukuriamas naujas žurnalas.

Žurnalo eilutės kuriamos pagal projekto faktinius duomenis. Toliau pateiktame sąraše nurodytos kelios svarbios numatytųjų nustatymų ir transformacijos taisyklės.

  - Kiekvieno projekto faktinė operacija turi eilutę „Project Operations“ integravimo žurnale. Išlaidų operacijos ir pardavimo operacijos, kurioms neišrašyta sąskaita, priklausančios laiko ir medžiagų atsiskaitymo tipui, rodomos atskirose eilutėse.
  - Lauke **Data** nurodoma operacijos data. Lauke **Apskaitos data** nurodoma data, kai operacija buvo įrašyta į knygą. Jei apskaitos data yra [uždarytame finansiniame laikotarpyje](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), o parametras **Automatiškai nustatyti apskaitos datą, siekiant atidaryti knygos laikotarpį** nustatytas skirtuke **Finansų**, esančiame puslapyje **Projektų valdymo ir apskaitos parametrai**, sistema koreguos operacijos apskaitos datą į pirmą kito atidaryto knygos laikotarpio datą.
  - Lauke **Kvitas** rodomas kiekvienos faktinės operacijos kvito numeris. Kvitų numerių seka yra nurodyta puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **Numerių sekos**. Kiekvienai eilutei priskiriamas naujas numeris. Paskelbę kvitą, galite peržiūrėti, kaip yra susijusios išlaidų operacijos ir pardavimo operacijos, kurioms neišrašyta sąskaita, pasirinkdami **Susiję kvitai** puslapyje **Kvito operacija**.
  - Laukas **Kategorija** atitinka projekto operaciją ir numatytąsias reikšmes pagal susijusio projekto faktinių duomenų operacijos kategoriją.
    - Jei **Operacijos kategorija** nustatyta projekto faktiniuose duomenyse, o susijusi **Projekto kategorija** yra nurodytame juridiniame subjekte, pagal numatytuosius nustatymus kategorija priskiriama šiai projekto kategorijai.
    - Jei **kategorija Operacija nenustatyta faktiniame projekte, sistema naudoja reikšmę, esančią lauke Projekto kategorijos numatytieji nustatymai**, esančiame **puslapio** Projekto valdymo ir apskaitos parametrai **skirtuke** Projekto operacijos Dynamics 365 Customer **Engagement**.
  - Laukas **Ištekliai** atitinka projekto išteklius, susijusius su šia operacija. Šie ištekliai naudojami kaip nuoroda projekto sąskaitų faktūrų pasiūlymuose klientams.
  - Laukas **Valiutos kursas** pagal numatytuosius parametrus pagal **valiutos keitimo kursą**, nustatytą Dynamics 365 Finance. Jeigu valiutos kurso sąrankos nėra, periodinis procesas **Importuoti iš paruošimo** neįtrauks įrašo į žurnalą ir klaidos pranešimas bus įtrauktas į užduoties vykdymo žurnalą.
  - Laukas **Eilutės ypatybės** atitinka atsiskaitymo tipą projekto faktiniuose duomenyse. Eilutės ypatybė ir atsiskaitymo tipo susiejimas apibrėžiami **puslapio Projektų valdymas ir apskaitos parametrai** skirtuke **Projekto operacijos Dynamics 365 Customer Engagement**.

Tik toliau pateikiami apskaitos atributai gali būti atnaujinti „Project Operations” integravimo žurnalo eilutėse.

- **Atsiskaitymo PVM grupė** ir **Atsiskaitymo elemento PVM grupė**
- **Finansinės dimensijos** (naudojant veiksmą **Paskirstyti sumas**)

Integravimo žurnalo eilutes galima panaikinti. Tačiau visos neskelbtos eilutės vėl bus įterptos į žurnalą, kai iš naujo paleisite **periodinio proceso importavimo iš inscenizavimo** procesą.

### <a name="post-the-project-operations-integration-journal"></a>Žurnalo "Project Operations" integravimo registravimas

Kai registruojate integravimo žurnalą, sukuriamos projekto antrinės knygos ir DK operacijos. Jos naudojamos toliau sąskaitas faktūras klientams teikti, pajamoms pripažinti ir finansinėms ataskaitoms teikti.

Pasirinktą "Project Operations" integravimo žurnalą galima registruoti naudojant **įrašą** puslapyje "Project Operations" integravimo žurnalas. Visus žurnalus galima automatiškai paskelbti vykdant procesą žurnale **Periodinių** > **projektų operacijų integravimas** > **Po projekto operacijų integravimo**.

Registravimas gali būti atliekamas interaktyviai arba pakete. Atminkite, kad visi žurnalai, kuriuose yra daugiau nei 100 eilučių, bus automatiškai paskelbti pakete. Norėdami pagerinti našumą, kai žurnalai, kuriuose yra daug eilučių, skelbiami pakete, įgalinkite integravimo žurnalą **"Post Project Operations" naudodami kelių paketinių užduočių** funkciją **funkcijų valdymo** srityje. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Perkelkite visas eilutes, kuriose yra registravimo klaidų, į naują žurnalą

> [!NOTE]
> Norėdami naudoti šią galimybę, įgalinkite **funkciją Perkelti visas eilutes su registravimo klaidomis į naują "Project Operations" integravimo žurnalą**, esančią **darbo srityje Funkcijų valdymas**.

Skelbiant žurnale "Project Operations" integravimas, sistema patvirtina kiekvieną žurnalo eilutę. Sistema skelbia visas eilutes, kuriose nėra klaidų, ir sukuria naują žurnalą visoms eilutėms, kuriose yra registravimo klaidų. Norėdami peržiūrėti žurnalus, kuriuose yra registravimo klaidų eilučių, eikite į žurnalą **Projektų valdymas ir apskaitos** > **žurnalai** > **Projekto operacijų integravimo žurnalas** ir filtruokite žurnalus naudodami lauką **Pradinis žurnalas**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
