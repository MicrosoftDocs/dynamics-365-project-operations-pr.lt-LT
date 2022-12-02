---
title: Projektų prognozės ir biudžetai
description: „Microsoft Dynamics 365 Finance” teikia projektų prognozes ir projektų biudžetus, kad galėtumėte tvarkyti ir valdyti savo projektus.
author: Yowelle
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15731010877b5d62329867e878f624149e74f761
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684560"
---
# <a name="project-forecasts-and-budgets"></a>Projektų prognozės ir biudžetai

[!include [banner](../includes/banner.md)]

Yra du projektų valdymo ir kontrolės būdai: projektų prognozės ir projektų biudžetai. 

Naudokite projektų prognozavimą, jei jūsų organizacija turi veiklos perspektyvą ir orientuojasi į pajamas ir išlaidas, gaunamas iš konkrečių operacijų. Naudokite projektų biudžeto sudarymo paslaugą, jei jūsų organizacija daugiau dėmesio skiria finansinėms sumoms. 

Sudarant tiek projektų prognozes, tiek biudžetus, naudojami prognozavimo modeliai, skirti suplanuotoms operacijų sumoms gauti. 

Kiekvienas metodas turi savo privalumų. Prieš pasirinkdami metodą, kurį naudosite savo organizacijoje, turėtumėte apsvarstyti toliau pateikiamus punktus.

|   Paskirstymo metodas       |           Projektų prognozavimas            |        Projektų biudžeto sudarymas                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Laikotarpio skyrimas**     | Negalite skirti operacijų ataskaitiniam laikotarpiui. Prognozės ir prognozių valdymas yra pagrįsti projekto vykdymo trukme. Kadangi prognozės pagrįstos konkrečia data, turite nustatyti laikotarpį remdamiesi data. | Galite skirti operacijas visam projektui arba ataskaitiniam laikotarpiui. Jeigu skiriate laikotarpiui, galite perkelti nepanaudotas sumas į kitą ataskaitinį laikotarpį. |
| **Operacijų peržiūra**  | Galite peržiūrėti operacijas prognozės formose, kuriose matysite visos įmonės ir visų projektų prognozes, neatsižvelgiant į hierarchiją. Norėdami peržiūrėti konkretų projektą, turite filtruoti duomenis.                                       | Galite peržiūrėti vieno projekto hierarchijos operacijas, kurioms yra skirtas biudžetas. Todėl galite peržiūrėti pirminio projekto arba jo subprojektų operacijų išsamią informaciją.                 |
| **Operacijų kintamieji** | Įvesdami prognozės operacijas, galite naudoti visus esamus faktinės operacijos atributus. Taip galima tiksliau prognozuoti. Pavyzdžiui, galite įvesti kiekių, darbuotojų, elementų arba eilutės ypatybių išsamią informaciją.         | Įvesdami biudžeto išsamią informaciją, galite naudoti tik sumas, kategorijas ir veiklas.                    |
| **Sauga**              | Prognozės grindžiamos operacijomis, kurias įvedėte prognozės formose – nenaudojamas joks proceso valdymo mechanizmas. Bet kuris darbuotojas, turintis teises naudotis prognozės formą, gali be patvirtinimo peržiūrėti informaciją.                                        | Sudarant biudžetą, naudojama darbo eigos sistema, kuri leidžia keisti valdymą ir turėti peržiūrų retrospektyvą.         |
| **Įrašų tipai**           | Prognozės operacijų įrašai grindžiami vienetų skaičiumi bei išlaidų ir pardavimo vienetų kainomis.  | Biudžeto duomenys grindžiami sumomis, kurios padalijamos į išlaidas ir pajamas.                                          |
| **Prognozių modeliai**       | Kadangi kiekviena prognozė turi būti susieta su modeliu, galite sukurti kelis prognozių modelius, taip pat nustatyti submodelius.           | Sudarant projekto biudžetą, ribojamas prognozių modelių, naudojamų biudžetui sudaryti, skaičius. Naudojant mažiau prognozių modelių, didinamas planavimo nuoseklumas.                           |
| **Viršytos išlaidos**         | Galite tik leisti arba neleisti įrašyti operacijas, dėl kurių bus viršytos išlaidos.   | Sudarant projekto biudžetą, naudotojams suteikiamos papildomos valdymo parinktys. Galite leisti įspėjimus ir išlaidų viršijimus.                    |
| **Valdiklis**               | Prognozės valdomos naudojant prognozės sumažinimą. Faktinės sumos atimamos iš prognozės operacijų balansų nenaudojant jokio įrašo sekimo. Taip gali būti sunkiau nustatyti, kur įvyko faktinė operacija.                   | Valdant projekto biudžetą, faktinės sumos atimamos iš likusio biudžeto sumų. Taip galima tiksliau sekti įrašą.                                   |

## <a name="project-forecasts"></a>Projektų prognozės
Prognozuodami biudžetą, galite įvesti prognozės operacijas į kiekvieno operacijų tipo prognozės formas. Visi atributai, kurie gali būti naudojami faktinei operacijai atlikti, gali būti naudojami ir prognozės operacijai atlikti, pvz., eilutės pelningumas, eilutės atributai, darbuotojai arba aprašymai. Taip pat patyrę išlaidų, galite planuoti, po kiek laiko išrašysite klientui sąskaitą faktūrą. 

Projekto prognozės operacijos grindžiamos vienetais ir sumomis. 

Kiekvieną projekto prognozę turite susieti su prognozės modeliu. Kai įvedate prognozės operaciją, automatiškai siūlomas prognozės modelis. Prognozės modelis veikia kaip prognozės operacijų saugojimo vieta. 

Galite priskirti prognozės modelius kaip modelio submodelius. Taip galėsite prognozuoti pagal regioną, laikotarpį arba skyrių. Galite kopijuoti prognozės operacijas į modelį, kad sukurtumėte naują modelį, taip pat galite perkelti operacijas į didžiąją knygą. Kadangi tarp prognozės ir modelio yra ryšys „vienas su vienu“, kiekvienas prognozės modelis sudaro atskirą projekto biudžetą. 

Prognozės modeliai gali naudoti prognozės sumažinimą kaip projektų valdymo mechanizmą. Mažinant prognozę, faktinės operacijos sumažina prognozės operacijų balansus. Tačiau kadangi prognozės sumažinimas taikomas aukščiausiai hierarchijos struktūroje esančiam projektui, teikiamas ribotas prognozės pokyčių rodinys. Pavyzdžiui, jei darbuotojas susietas su subprojektu, faktinės šio darbuotojo operacijos registruojamos pirminiame projekte. Dėl to gali būti sunku sekti pokyčius, nes sunku nustatyti, kuri operacija kuriame projekte lėmė prognozės sumos sumažėjimą. Todėl verta sukurti prognozės modelio kopiją, skirtą naudoti prognozės sumažėjimo atveju. Tada galite naudoti ataskaitas, kad peržiūrėtumėte, kas buvo prognozuojama iš pradžių. 

Galite peržiūrėti, kopijuoti, naikinti arba perkelti projekto prognozes į didžiosios knygos biudžetą. Tačiau procesas nėra valdomas. Bet kuris darbuotojas, turintis teisę naudotis prognozės formą, gali be patvirtinimo peržiūrėti informaciją.

-   **Peržiūra** – galite peržiūrėti prognozės operaciją tose pačiose formose, kuriose buvo atlikti pradiniai įrašai.
-   **Kopijavimas arba naikinimas** – kai kopijuojate prognozės operacijas, kopijuojate vieno prognozės modelio operacijos eilutes į kitą prognozės modelį. Kai naikinate prognozę, naikinate prognozės operacijas iš prognozės modelio. Norėdami riboti kopijuojamų arba naikinamų prognozės operacijų skaičių, pažymėkite konkrečius operacijų tipus ir datas. Taip galėsite kopijuoti arba naikinti tik konkrečias prognozės dalis.
-   **Perkėlimas** – kai projekto prognozę perkeliate į didžiosios knygos biudžetą, perkeliate prognozės modelio prognozės operacijas į didžiąją knygą. Galite perrašyti bet kurias anksčiau perkeltas operacijas didžiosios knygos biudžete, į kurį perkeliate savo projekto prognozę.

## <a name="project-budgets"></a>Projekto biudžetai
Projekto biudžeto sudarymas yra paprastesnis metodas negu prognozavimas, nors jis yra integruojamas su prognozės modeliais. Jam naudojama viena įrašo forma, skirta pradinio biudžeto išsamiai informacijai ir tikslinimams, ir leidžiama planuoti remiantis tik suma, kategorija arba veikla. 

Sudarant projekto biudžetą, visi pradiniai biudžetai ir tikslinimai turi būti siunčiami į projekto darbo eigą patvirtinti. Naudojant darbo eigas, galima geriau valdyti procesą ir kurti pakeistą retrospektyvos įrašą. 

Projekto biudžeto sudarymas yra panašus į didžiosios knygos biudžeto sudarymą, tačiau jis yra greitesnis ir lengviau nustatomas. Daugelio didžiosios knygos biudžeto sudarymo parinkčių, pvz., numerių sekų arba valiutos, projektams nereikia nustatyti atskirai.

Projekto biudžetai automatiškai siejami su dviem prognozės modeliais, vienu, skirtu pradiniam biudžetui, ir vienu, skirtu likusiam biudžetui. Todėl prognozės modeliais paremtose ataskaitose gali būti naudojami biudžeto duomenys. Patvirtinus biudžetą, sistema kuria prognozės operacijas pagal susietus modelius, naudojamus ataskaitų kūrimo ir valdymo tikslais.

## <a name="forecast-models"></a>Prognozės modeliai
Prognozės modeliai turi vieno sluoksnio hierarchiją. Tai reiškia, kad viena projekto prognozė turi būti susieta su vienu prognozės modeliu.

Jei naudojate projekto prognozavimo funkciją, galite nustatyti modelius kaip submodelius. Tada galėsite kurti prognozes pagal skyrių, laikotarpį arba regioną. Pavyzdžiui, galite sukurti prognozės modelį metams, tada sukurti submodelius, skirtus šiaurės rytų, pietryčių, šiaurės vakarų ir pietvakarių regionų prognozėms, kurias teikia regionų vadovai. Pasirinkdami skirtingas galimų ataskaitų parinktis, galite peržiūrėti informaciją pagal bendrą prognozę arba pagal submodelį.





[!INCLUDE[footer-include](../includes/footer-banner.md)]