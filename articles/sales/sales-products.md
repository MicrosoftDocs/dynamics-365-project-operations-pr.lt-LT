---
title: Produktai
description: Šioje temoje pateikta informacija apie produktų katalogą, kurį galite naudoti norėdami klientams pateikti informaciją apie produktus ir kainodarą jūsų organizacijoje.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 5c57b2596e1d480ff59591618f073ceb8f70a289
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574118"
---
# <a name="products"></a>Produktai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Produktai yra jūsų verslo pagrindas. Produktų katalogas programoje „Dynamics 365 Sales Professional“ yra produktų ir jų kainodaros informacijos rinkinys. Padėkite pardavimo atstovams padidinti jų pardavimo apimtį, sparčiai sukurdami produktų katalogą.

## <a name="add-a-product"></a>Produkto pridėjimas

1.  Įsitikinkite, kad turite „Sales Professional“ vadovo ar sistemos administratoriaus vaidmenį, kad galėtumėte įtraukti produktus į „Dynamics 365 Sales Professional“.
2.  Svetainės struktūros dalyje **Sąranka** pasirinkite **Produktai**.
3.  Pažymėkite **Įtraukti produktą** ir užpildykite šią informaciją:

    -  **Pavadinimas**
    -  **Produkto ID**
    -  **Pirminis**: pasirinkite produkto pirminę produktų šeimą. Jei kuriate antrinį produktą produktų šeimoje, čia įvedamas pirminės produktų šeimos pavadinimas. Įrašius įrašą pavadinimo keisti negalima.
    -  **Galioja nuo** / **Galioja iki**: nustatykite produkto galiojimo laikotarpį pasirinkdami datas laukuose **Galioja nuo** ir **Galioja iki**.
    -  **Vienetų grupė**: pasirinkite vienetų grupę. Vienetų grupė yra įvairių vienetų, kurie naudojami parduodant produktą, rinkinys ir ji nustato, kaip atskiri elementai yra grupuojami į didesnius kiekius. Pavyzdžiui, jeigu įtraukiate sėklas kaip produktą, galite sukurti vienetų grupę, pavadintą „Sėklos“, ir kaip pirminį vienetą nustatyti „pakelį“.
    -  **Numatytasis vienetas**: pasirinkite dažniausią vienetą, kuriuo gali būti parduodamas produktas. Vienetai yra kiekiai arba matavimų vienetai, kuriais skaičiuojami parduodami produktai. Pvz., jei sėklas pridedate kaip produktą, jas galite parduoti pakeliais, dėžėmis arba padėklais. Kiekvienas iš jų yra produkto vienetas. Jeigu sėklos yra dažniausiai parduodamos pakeliais, pasirinkite jį kaip vienetą.
    -  **Numatytasis kainoraštis**: jei tai naujas produktas, šis laukas bus skirtas tik skaityti. Kad galėtumėte pažymėti numatytąjį kainoraštį, turite užpildyti visus privalomuosius laukus, o tada įrašyti įrašą. Nors numatytasis kainoraštis nėra būtinas, įrašius produkto įrašą verta nustatyti numatytąjį kiekvieno produkto kainoraštį. Tada, jei kliento įraše nėra kainoraščio, „Sales“ gali naudoti numatytąjį kainoraštį pasiūlymams, užsakymams ir sąskaitoms faktūroms generuoti.
    -  **Palaikomos dešimtainės trupmenos**: įveskite sveikąjį skaičių nuo 0 iki 5. Jei produkto negalima padalyti į dalinius kiekius, įveskite 0. Jei su produktu nesusietas kainoraštis, pasiūlymo, užsakymo arba sąskaitos faktūros produkto įrašo lauke **Kiekis** įvestos reikšmės tikslumas tikrinamas pagal šiame lauke įvestą reikšmę.
    -  **Tema**: šį produktą susiekite su tema. Norėdami suskirstyti produktus į kategorijas ir filtruoti ataskaitas, galite naudoti temas.

4.  Pasirinkite **Įrašyti**.
5.  Skirtuke **Papildoma informacija**, esančiame skiltyje **Kainoraščio elementai** pasirinkite **Daugiau komandų**, o tada pasirinkite **Įtraukti naują kainoraščio elementą**.
7.  Skirtuke **Papildoma informacija**, esančiame skiltyje **Produkto ryšys** pasirinkite piktogramą **Daugiau komandų**, o tada pasirinkite **Įtraukti naują produkto ryšį**.
8.  Formoje **Naujas produkto ryšys** įveskite toliau nurodytą informaciją ir komandų juostoje pasirinkite **Įrašyti ir uždaryti**.

    -   **Susijęs produktas** – pasirinkite produktą, kurį norite įtraukti kaip susijusį produktą į esamo produkto įrašą, su kuriuo dirbate.
    -   **Pardavimų ryšio tipas** – pasirinkite, ar norite įtraukti produktą kaip papildomą pardavimą, kaip kryžminį pardavimą, kaip priedą, ar kaip pakaitinį produktą.
    -   **Kryptis** – pasirinkite, ar ryšys tarp produktų bus vienakryptis ar dvikryptis. Kai pasirenkate Vienakryptis, produktas, kurį pasirenkate dalyje **Susijęs produktas**, bus rodomas kaip esamo produkto rekomendacija (bet ne atvirkščiai).

9.  Produkto formoje pasirinkite **Įrašyti**.

## <a name="import-products"></a>Produktų importavimas

Galite naudoti importavimo šablonus ir masiškai įtraukti produktų duomenis į „Dynamics 365 Sales“.

## <a name="revise-a-product"></a>Produkto peržiūra

Siekdami rodyti naujausią produktų atsargų informaciją, greitai peržiūrėkite reikiamų produktų ypatybes ir pakartotinai paskelbkite informaciją, kad pardavimo agentai galėtų matyti vėliausius atsargų pasikeitimus.

1.  Įsitikinkite, kad turite vieną iš toliau nurodytų saugos vaidmenų arba atitinkamų teisų: sistemos administratoriaus, sistemos pritaikymo specialisto, pardavimo vadybininko, pardavimo skyriaus vadovo pavaduotojo, rinkodaros skyriaus vadovo pavaduotojo arba įmonės vadovo.
2.  Svetainės struktūroje pasirinkite **Produktai**.
3.  Atidarykite aktyvų produktą, kurį norite keisti, ir komandų juostoje pasirinkite **Peržiūrėti**.
4.  Dialogo lange **Patvirtinti keitimą** pasirinkite **Patvirtinti**. Produkto būsena pasikeis į **Peržiūrimas**.
5.  Atlikę keitimus, komandų juostoje pasirinkite **Publikuoti**.

    > [!TIP]
    > Norėdami atmesti keitimus ir tęsti naudodami vėliausią aktyvią produkto versiją, pasirinkite **Atmesti keitimus**. Sugrąžinama produkto būsena **Aktyvus**.

## <a name="clone-a-product"></a>Produkto klonavimas 

Norėdami sukurti naują produktą, galite sutaupyti laiko klonuodami esamą. Taip sukuriama originalaus įrašo kopija su tokia pačia informacija; skiriasi tik pavadinimas ir ID.

1.  Įsitikinkite, kad turite vieną iš toliau nurodytų saugos vaidmenų arba atitinkamų teisų: sistemos administratoriaus, sistemos pritaikymo specialisto, pardavimo vadybininko, pardavimo skyriaus vadovo pavaduotojo, rinkodaros skyriaus vadovo pavaduotojo arba įmonės vadovo.
2.  Svetainės struktūroje pasirinkite **Produktai**.
3.  Pasirinkite produktą, kurį norite klonuoti, ir komandų juostoje pasirinkite **Klonuoti**. Rodomos patvirtinimo dialogo langas.
4.  Spustelėkite **Patvirtinti**.

Atidaromas naujas produkto įrašas, kuriame pateikiama tokia pati pradinio įrašo informacija; skiriasi tik pavadinimas ir ID.

## <a name="retire-a-product"></a>Produkto nurašymas 

Jei jūsų organizacija nebeprekiauja produktu, nurašykite jį, kad produkto nebegalėtų pasirinkti jūsų prekybos agentai.

1.  Įsitikinkite, kad turite sistemos administratoriaus ar „Sales Professional“ vadovo vaidmenį arba lygiavertes teises.
2.  Svetainės struktūroje pasirinkite **Produktai**.
3.  Atidarykite aktyvų produktą, kurį norite nurašyti, ir komandų juostoje pasirinkite **Nurašyti**.
4.  Dialogo lange **Patvirtinti nurašymą** pasirinkite **Patvirtinti**.


## <a name="delete-a-product"></a>Produkto naikinimas

Jei norite nustoti prekiauti produktu, panaikinkite jį.

> [!IMPORTANT]
> Panaikinto įrašo atkurti negalima.

1.  Įsitikinkite, kad turite sistemos administratoriaus ar „Sales Professional“ vadovo vaidmenį arba lygiavertes teises.
2.  Svetainės struktūroje pasirinkite **Produktai**.
3.  Pasirinkite produktą, kurį norite naikinti, ir komandų juostoje pasirinkite **Naikinti**.
4.  Dialogo lange **Naikinimo patvirtinimas** pasirinkite **Tęsti**.
 
 ## <a name="quantity-factors-for-products"></a>Produktų kiekio koeficientai

Kiekio koeficientai, kad būtų palaikomas prenumerata pagrįstų produktų pardavimas. Prenumerata pagrįstiems produktams pasiūlymo arba projekto sutarties eilutėje kiekis išreiškiamas kaip vartotojo mėnesių skaičius.

Paprastai prenumeratos programinės įrangos kaina kataloge yra kaina vienam vartotojui per mėnesį. Tačiau vietoje to galite naudoti kitus laiko aprašus. Per pardavimo procesą pasiūlymo eilutėje nurodyta kaina paprastai yra vienam vartotojui per mėnesį, dėl kurios susitarė ir nuolaidą pritaikė IT pardavimo agentas. Kiekvienas sandoris turi skirtingą vartotojų skaičių ir skirtingą prenumeratos mėnesių skaičių. Kiekis, naudojamas pasiūlymo eilutės sumai apskaičiuoti, yra vartotojų skaičiaus ir prenumeratos mėnesių skaičiaus produktas.

Kiekio koeficientai priklauso nuo produkto atributų. Konfigūruojant konkrečias produkto ypatybes, galite žymėti tų ypatybių pogrupį arba visas ypatybes kaip kiekio koeficientus.

Sistema tikrina, kad tik skaitinės ypatybės arba produkto, turinčio skaitinių duomenų tipą, ypatybės būtų žymimos kaip kiekio koeficientai. Kai produktas, kuriam sukonfigūruoti kiekio koeficientai, yra įtraukiamas į pasiūlymo eilutę, pasiūlymo eilutėje esantis laukas **Kiekis** tampa tik skaitomu lauku. Įvedus produktų ypatybių reikšmes, kurios yra kiekio koeficientai, apskaičiuojamas pasiūlymo eilutės kiekis.

Pavyzdžiui, jei yra šios ypatybės: 

- **Vartotojų skaičius** – vartotojų skaičius 
- **Mėnesių skaičius** – prenumeratos mėnesių skaičius
- **Produkto SKU** 

Ypatybės **Vartotojų skaičius** ir **Mėnesių skaičius** gali būti pažymėtos kaip kiekio koeficientai redaguojant produkto eilutės ypatybes. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]