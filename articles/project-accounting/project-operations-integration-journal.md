---
title: Integravimo žurnalas programoje „Project Operations“
description: Šiame straipsnyje pateikiama informacija apie darbą su integravimo žurnalu programoje „Project Operations”.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541088"
---
# <a name="integration-journal-in-project-operations"></a>Integravimo žurnalas programoje „Project Operations“

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Laiko, išlaidų, mokesčių ir materialiniai įrašai sukuria **Faktines** operacijas, kurios nurodo pagal projektą užbaigto darbo veiklos rodinį. „Dynamics 365 Project Operations“ teikia apskaitininkams įrankį, skirtą operacijoms peržiūrėti ir apskaitos atributams koreguoti, kai reikia. Užbaigus peržiūrą ir koregavimus, operacijos skelbiamos projekto papildomoje knygoje ir didžiojoje knygoje. Buhalteris gali vykdyti šias veiklas naudodamas **„Project Operations“ integravimo** žurnalą (**„Dynamics 365 Finance“** > **Projektų valdymas ir apskaita** > **Žurnalai** > **„Project Operations“ integravimo** žurnalas.

![Integravimo žurnalo srautas.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Įrašų kūrimas „Project Operations“ integravimo žurnale

Įrašai „Project Operations“ integravimo žurnale įrašai kuriami naudojant periodinį procesą, **Importuoti iš paruošimo lentelės**. Šį procesą galite vykdyti eidami į **Dynamics 365 Finance** > **Projektų valdymas ir apskaita** > **Periodinis** > **„Project Operations“ integravimas** > **Importuoti iš paruošimo lentelės**. Jeigu reikia, galite vykdyti procesą interaktyviai arba sukonfigūruoti procesą, kad veiktų fone.

Vykdant periodinį procesą, randami visi faktiniai duomenys, kurie dar neįtraukti į „Project Operations“ integravimo žurnalą. Sukuriama kiekvienos faktinės operacijos žurnalo eilutė.
Sistema grupuoja žurnalo eilutes į atskirus žurnalus pagal reikšmę, pasirinktą lauke **Laiko vienetas „Project Operations“ integravimo žurnale** (**„Finansai”** > **Projektų valdymas ir apskaita** > **Sąranka** > **Projektų valdymo ir apskaitos parametrai**, **„Project Operations”, veikiančios „Dynamics 365 Customer Engagement”** skirtuke). Toliau pateikiamos galimos šio lauko reikšmės.

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
    - Jeigu **Operacijos kategorija** nenustatyta projekto faktiniuose duomenyse, sistema naudoja reikšmę, esančią **Projekto valdymo ir apskaitos parametrai** puslapio **„Project Operations” programoje „Project Operations on Dynamics 365 Customer Engagement”** skirtuko **Projektų kategorijos parametrai** laukelyje.
  - Laukas **Ištekliai** atitinka projekto išteklius, susijusius su šia operacija. Šie ištekliai naudojami kaip nuoroda projekto sąskaitų faktūrų pasiūlymuose klientams.
  - Laukelis **Valiutos kursas** nustatomas pagal **Valiutos keitimo kursą**, nustatytą „Dynamics 365 Finance”. Jeigu valiutos kurso sąrankos nėra, periodinis procesas **Importuoti iš paruošimo** neįtrauks įrašo į žurnalą ir klaidos pranešimas bus įtrauktas į užduoties vykdymo žurnalą.
  - Laukas **Eilutės ypatybės** atitinka atsiskaitymo tipą projekto faktiniuose duomenyse. Eilutės ypatybės ir atsiskaitymo tipo susiejimas apibrėžiami puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **„Project Operations“ programoje „Dynamics 365 Customer Engagement“**.

Tik toliau pateikiami apskaitos atributai gali būti atnaujinti „Project Operations” integravimo žurnalo eilutėse.

- **Atsiskaitymo PVM grupė** ir **Atsiskaitymo elemento PVM grupė**
- **Finansinės dimensijos** (naudojant veiksmą **Paskirstyti sumas**)

Integravimo žurnalo eilutes galima naikinti. Vis dėlto, iš naujo paleidus periodinį procesą **Importuoti iš paruošimo**, visos neužregistruotos eilutės bus vėl įterptos į žurnalą.

### <a name="post-the-project-operations-integration-journal"></a>Paskelbti „Project Operations“ integravimo žurnalą

Kai registruojate integravimo žurnalą, sukuriamos projekto antrinės knygos ir DK operacijos. Jos naudojamos toliau sąskaitas faktūras klientams teikti, pajamoms pripažinti ir finansinėms ataskaitoms teikti.

Parinktą "Project Operations" integravimo žurnalą galima paskelbti naudojant funkciją **Skelbti** „Project Operations“ integravimo žurnalo puslapyje. Visus žurnalus galima automatiškai skelbti vykdant procesą **Periodika** > **„Project Operations" integravimas** > **„Project Operations“ postintegravimo žurnalas**.

Paskelbimas gali būti vykdomas interaktyviai arba pakete. Atkreipkite dėmesį, kad visi žurnalai, turintys daugiau nei 100 eilučių, bus automatiškai paskelbti pakete. Kad procesas būtų efektyvesnis, kai pakete užregistruojami žurnalai, turintys daug eilučių, įgalinkite **„Project Operations" postintegravimo žurnalo, naudojant kelių paketų užduočių** funkciją **Funkcijų valdymo** darbo srityje. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Perkelti visas eilutes, kuriose yra paskelbimo klaidų, į naują žurnalą

> [!NOTE]
> Norėdami naudoti šią galimybę, įjunkite funkciją **Perkelti visas eilutes su registravimo klaidomis į naują „Project Operations" integravimo žurnalą** **Funkcijų valdymo** darbo srityje.

Ši funkcija padeda pagerinti "Project Operations" integravimo žurnalo naudojimo patirtį. Kai ši funkcija įjungta, dvigubo rašymo laiko problemos ir sąrankos problemos nebetrukdo galiojančių žurnalų paskelbimui. Skelbiant „Project Operations" integravimo žurnalą sistema patikrina kiekvieną žurnalo eilutę. Jame skelbiamos visos eilutės, kuriose nėra klaidų, ir sukuriamas naujas visų eilučių, kuriose yra registravimo klaidų, žurnalas.

Norėdami peržiūrėti registravimo klaidų turinčių eilučių žurnalą, eikite į **Projekto valdymas ir apskaita** \> **Žurnalai** \> **„Project Operations“ integravimo žurnalas** ir filtruokite žurnalų sąrašą naudodami laukelį **Originalus žurnalas**. Šioje iliustracijoje pateikiamas pavyzdys, kai žurnalai puslapyje **„Project Operations" integravimo žurnalas** filtruoti tokiu būdu.

![Orignalus žurnalas parodytas „Project Operations“ integravimo žurnalo puslapyje.](./media/transferLines-originalJournal.png)

Jei periodinis užduočių paketas sukonfigūruotas taip, kad būtų skelbiamas integravimo žurnalas, paskelbimas bus kartojamas ir žurnalai bus paskelbti, jei laiko problema bus išspręsta. Visus likusius žurnalus reikia ištirti rankiniu būdu peržiūrint žurnalus ir imantis bet kokių reikiamų veiksmų.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
