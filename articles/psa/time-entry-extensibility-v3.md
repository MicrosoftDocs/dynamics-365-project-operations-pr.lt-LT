---
title: Savaitės laiko įrašo tinkinimas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip įgyvendinti pasirinktines verslo taisykles, palaikančias organizacijos praktiką.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: bdc8df4050d895504fa126e2ee55fcd3b4de123f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918966"
---
# <a name="customize-weekly-time-entry"></a>Savaitės laiko įrašo tinkinimas 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Į „Microsoft Dynamics 365 Project Service Automation“ 3.3 versiją „Microsoft“ įtraukė naujovišką tinklelį, kurį naudodami projekto ištekliai gali greitai vienu metu įvesti ne daugiau kaip vienos savaitės laiką. Naujame savaitės laiko įrašo tinklelyje gali būti rodomos įrašų sumos pagal datą, eilutę arba savaitę. Ištekliai gali daryti savaitės laiko įrašų kopijas, taip pat masiškai kopijuoti iš ankstesnių savaičių. Sistemos tinkinimo specialistai gali tinkinti rodinį įtraukdami laukų, įtraukdami peržvalgų į kitus objektus ir diegdami pasirinktines verslo taisykles, kuriomis grindžiama organizacijos veikla.

Laiko įrašas ir naujas savaitės laiko tinklelis pasiekiami per svetainės struktūrą. Neišplėstinio pasirinktinio laiko įrašo funkcija, buvusi ankstesnėse PSA versijose, buvo pakeista išplėstiniu savaitės laiko įrašo tinkleliu ir kitokiu tik skaitomo tinklelio ir kalendoriaus naudojimu. Dėl šio pakeitimo vartotojai gali įvesti laiką savaitės sumomis.

## <a name="page-layout"></a>Puslapio maketas
Naujas savaitės laiko įrašo tinklelis yra pasirinktinis valdiklis su įrankių juosta ir dviem pagrindiniais skyriais – **Dimensijos** ir **Trukmė** Įrankių juostoje yra mygtukas, taikomas tik šiam laiko įrašo tinklelio pasirinktiniam valdikliui. Priešingai, puslapio viršuje esančios veiksmų srities mygtukai taikomi trijų tipų valdikliams, kurie palaikomi laiko įraše: savaitės laiko įrašo valdikliui, tik skaitomam valdikliui ir kalendoriaus valdikliui.

### <a name="dimensions"></a>Matmenys
Skyriuje **Dimensijos** kaip stulpelių antraštės rodomos visos dimensijos, prie kurių galima įvesti laiką. Toliau nurodytos dimensijos yra visiškai parengtos naudoti.

- Projektas
- Projekto užduotis
- Vaidmuo
- Tipas
- Įrašo būsena

Skyriuje **Dimensijos** negalima atlikti įdėtojo redagavimo. Šiame skyriuje palaikomas rodinys, leidžiantis į savaitės laiko įrašo tinklelį įtraukti pasirinktinių laukų. Informacijos apie tai, kaip įtraukti pasirinktinius laukus, ieškokite šio straipsnio skyriuje "Išplėtimas".

### <a name="duration"></a>Trukmė
Skyrius Trukmė rodo savaitės dienas kaip stulpelių antraštes. Šiame skyriuje leidžiamas įdėtasis redagavimas. Sukūrus laiko įrašo eilutę, kurioje yra atitinkamos dimensijos, vartotojai gali greitai eilutėje įvesti laiką, kurį skyrė šioms dimensijoms.

## <a name="create-a-new-time-entry"></a>Naujo laiko įrašo kūrimas
Norėdami sukurti naują laiko įrašą laiko įrašo tinklelyje, pasirinkite **Naujas**. Atidaromas dialogo langas **Laiko įrašo spartusis kūrimas**. Šiame dialogo lange vartotojai gali pasirinkti laiko įrašo datą, o tada įvesti dimensijų **Projektas**, **Projekto užduotis**, **Vaidmuo** ir **Trukmės** duomenis minutėmis, valandomis arba dienomis, įvesdami **h**, **m** arba **d** kartu su skaičiumi. Vartotojai taip pat gali įvesti laiko įrašo aprašą ir komentarus, kuriuos galima bendrinti išorėje. Kai vartotojai įrašo keitimus, prie dimensijų įvestos reikšmės rodomos skyriuje **Dimensijos**. Trukmės informacija, įvesta lauke **Trukmė**, rodoma tą dieną, kuriai buvo sukurtas laiko įrašas.

Peržvalgos laukus teikia sistemos rodiniai. Pavyzdžiui, kai vartotojas įveda projektą, laukas **Projekto užduotis** pagal numatytuosius nustatymus nustatomas į rodinį **Kopijuoti**. Norėdami kurti užduočių, kurios nepriskirtos vartotojui, laiko įrašus, peržvalgos dialogo lange pasirinkite **Keisti rodinį**, tada pasirinkite rodinį **Visos aktyvios projekto užduotys**.

## <a name="edit-a-time-entry"></a>Laiko įrašo redagavimas
Kai kurių laukų laiko įrašų puslapyje išsami informacija, pvz., **Aprašas** ir **Išoriniai komentarai** savaitės laiko įrašo tinklelyje nerodoma. Vietoje to, trukmės langeliuose, kuriuose yra ši papildoma išsami informacija, bus rodomas nedidelis trikampis indikatorius. Pasirinkite langelį, tada pasirinkite **Redaguoti išsamią informaciją**, kad peržiūrėtumėte duomenis srityje **Spartusis redagavimas**. Norėdami redaguoti arba atnaujinti tam tikro laiko įrašo, kuris nepriklauso savaitės laiko įrašo tinkleliui, išsamią informaciją, vartotojai turi atidaryti sritį **Spartusis redagavimas**.

## <a name="copy-a-time-entry-row"></a>Laiko įrašo eilutės kopijavimas
Sukūrus pirmą laiko įrašo eilutę, vartotojai gali pasirinkti **Kopijuoti eilutę** ir nukopijuoti visą eilutę į naują eilutę. Tokiu būdu nukopijavus eilutę, taip pat nukopijuojamos dimensijos ir trukmė. Be to, vartotojai gali pasirinkti **Redaguoti eilutę**, kad skyriuje **Trukmė** eilutėje atnaujintų dimensijos reikšmes ir trukmę.

## <a name="open-a-time-entry"></a>Laiko įrašo atidarymas
Kad būtų galima optimaliai ir greitai įvesti į svarbiausius laukus, savaitės laiko įrašo tinklelyje rodomas pasirinktų dimensijų ir laiko trukmės subrinkinys. Norėdami peržiūrėti visą išsamią vieno laiko įrašo informaciją, srityje **Redaguoti įrašą** pasirinkite **Atidaryti**.

## <a name="submit-a-time-entry"></a>Laiko įrašo pateikimas
Vartotojai gali pateikti vieną laiko įrašą arba laiko įrašų grupę, pažymėdami langelių bloką arba visą laiko įrašo eilutę, o tada pasirinkdami **Pateikti**. Pateikti laiko įrašai rodomi kaip įrašai, laukiantys patvirtinimo tvirtintojo puslapyje **Tvirtinimas**. Sėkmingai pateikus laiko įrašus jų redaguoti negalima.

## <a name="recall-a-time-entry"></a>Laiko įrašo atšaukimas
Galite atšaukti laiko įrašus, kuriuos pateikėte. Galite atšaukti vieną laiko įrašą, laiko įrašų bloką arba visą laiko įrašų eilutę. Atšauktus laiko įrašus ištekliai gali redaguoti.

## <a name="time-entry-status"></a>Laiko įrašo būsena
Naujiems laiko įrašams automatiškai priskiriama būsena **Juodraštis**. Pateikus laiko įrašą jo būsena atnaujinama į **Pateiktas**. Kai pateiktas laiko įrašas patvirtinamas, jo būsena atnaujinama į **Patvirtintas**. Jei laiko įrašas atmetamas, būsena atnaujinama į **Grąžintas**, o įrašą galima pataisyti ir pateikti iš naujo. Galima naikinti tik laiko įrašus, kurių būsena yra **Juodraštis**.

## <a name="view-rejection-comments"></a>Atmetimo komentarų peržiūra
Kai tvirtintojas atmeta laiko įrašą, jis gali įtraukti atmetimo komentarų, kad išteklius galėtų sužinoti atmetimo priežastį. Norėdami peržiūrėti laiko įrašo atmetimo komentarus, pasirinkite **Atidaryti įrašą**. Atmetimo komentarai bus rodomi laiko planavimo juostoje. Laiko planavimo juostoje išteklius gali atsakyti į atmetimo komentarus prieš pateikdamas įrašą iš naujo.

## <a name="copy-week"></a>Kopijuoti savaitę
Sukūrus kelis laiko įrašus, vartotojai gali pasirinkti **Kopijuoti savaitę**, kad būtų masiškai sukurti papildomi laiko įrašai. Rodomas dialogo langas **Kopijuoti**. Skyriuje **Laikotarpio pradžia** naudokite laukus **Pradžios data** ir **Pabaigos data**, kad nustatytumėte datos intervalą, iš kurio kopijuoti laiko įrašus. Skyriuje **Laikotarpio pabaiga**, lauke **Pradžios data** nurodykite datą, kuriai norite kurti laiko įrašus. Tada pasirinkite **Kopijuoti**. Datai, nurodytai kaip „Laikotarpio pabaiga“, sukuriama savaitės, nurodytos kaip „Laikotarpio pradžia“ atitinkamos dienos laiko įrašų kopija. Pavyzdžiui, praėjusios savaitės pirmadienio laiko įrašas nukopijuojamas į savaitės, nurodytos kaip „Laikotarpio pabaiga“, pirmadienį.

## <a name="import"></a>Importuoti
Tas pats pagrindinis procesas naudojamas importuojant iš rezervavimų, užduočių ir keitimų. Vartotojai gali nurodyti datų intervalą, iš kurio importuojami rezervavimai. Tada jie turi pasirinkti konkrečius rezervavimus, kuriuos reikia kopijuoti į laiko įrašų juodraščius. Ankstesniame leidime siūlomi laiko įrašų buvo rodomi tinklelyje ir kalendoriuje, o atnaujinus seansą būdavo prarandami.

## <a name="extensibility"></a>Išplečiamumas
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Pasirinktinių laukų su peržvalgomis įtraukimas į kitus objektus
Yra trys pagrindiniai veiksmai, kaip į savaitės laiko įrašo tinklelį įtraukti pasirinktinį lauką.

1.  Įtraukite pasirinktinį lauką į sparčiojo kūrimo dialogo langą.
2.  Sukonfigūruokite tinklelį, kad būtų rodomas pasirinktinis laukas.
3.  Įtraukite pasirinktinį lauką atitinkamai į eilutės redagavimo užduočių srautą arba langelio redagavimo užduočių srautą.

Be to, reikia įsitikinti, ar naujas laukas turi reikiamus tikrinimus eilutės arba langelio redagavimo užduočių sraute. Atlikdami šį žingsnį, turite užrakinti lauką pagal laiko įrašo būseną.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pasirinktinio lauko įtraukimas į sparčiojo kūrimo dialogo langą
Į dialogo langą „Laiko įrašo spartusis kūrimas“ reikia įtraukti pasirinktinį lauką. kad vartotojai galėtų įvesti reikšmę, kai jie įtraukia laiko įrašus naudodami mygtuką **Naujas**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Sukonfigūruokite tinklelį, kad būtų rodomas pasirinktinis laukas
Įtraukti pasirinktinį lauką į savaitės laiko įrašo tinklelį galima dviem būdais. Pirma parinktis yra tinkinti rodinį **Mano savaitės laiko įrašai** ir į jį įtraukti pasirinktinį lauką. Galite pasirinkti pasirinktinio lauko padėtį ir dydį tinklelyje redaguodami šias ypatybes rodinyje.

Antroji parinktis yra sukurti naują pasirinktinį laiko įrašo rodinį ir nustatyti jį kaip numatytąjį rodinį. Šiame rodinyje turėtų būti laukai **Aprašas** ir **Išoriniai komentarai**, taip pat stulpeliai, kurie turėtų būti tinklelyje. Galite pasirinkti tinklelio padėtį, dydį ir numatytąją rikiavimo tvarką redaguodami šias ypatybes rodinyje. Tada sukonfigūruokite pasirinktinį šio rodinio valdiklį, kad jis būtų valdiklis **Laiko įrašo tinklelis**. Įtraukite šį valdiklį į rodinį ir pasirinkite jį žiniatinklyje, telefone ir planšetiniame kompiuteryje. Tada sukonfigūruokite savaitės laiko įrašo tinklelio parametrus. Lauką **Pradžios data** nustatykite kaip **msdyn_date**, lauką **Trukmė** nustatykite kaip **msdyn_duration**, o lauką **Būsena** nustatykite kaip **msdyn_entrystatus**. Naudojant numatytąjį rodinį laukas **Tik skaitymo būsenos sąrašas** nustatytas kaip **192350002,192350003,192350004**, laukas **Eilutės redagavimo užduočių srautas** nustatytas kaip **msdyn_timeentryrowedit**, o laukas **Langelio redagavimo užduočių srautas** nustatytas kaip **msdyn_timeentryedit**. Galite tinkinti šiuos laukus, jei norite įtraukti arba pašalinti tik skaitymo būseną arba naudoti kitą užduotimi pagrįstą funkciją (TBX) eilutėms arba langeliams redaguoti. Šie laukai turi būti susieti su pastovia reikšme.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Pasirinktinio lauko įtraukimas į reikiamą redagavimo užduočių srautą
TBX puslapius, naudojamus redagavimui, galima rasti srityje **Procesai**. Numatytieji puslapiai yra **„Project Service“ - Laiko įrašo eilutės redagavimas** ir **„Project Service“ - Laiko įrašo redagavimas**. Galite redaguoti šiuos numatytuosius puslapius arba kurti naujus pasirinktinius TBX puslapius.

> [!NOTE] 
> Abi parinktys pašalins kai kuriuos parengtus naudoti objektų **Projektas** ir **Projekto užduotis** filtrus, todėl bus rodomi visi objektų peržvalgos rodiniai. Pirmą kartą paleidus matomi tik susiję peržvalgos rodiniai.

Turite nustatyti tinkamą pasirinktinio lauko užduočių srautą. Tikriausiai, jei įtraukėte lauką į tinklelį, jis turėtų patekti į eilutės redagavimo užduočių srautą, naudojamą laukuose, kurie taikomi visai laiko įrašų eilutei. Jei pasirinktinis lauką kiekvieną dieną turi skirtingą reikšmę, pvz., **Pabaigos laiko** pasirinktinis laukas, jis turėtų patekti į langelio redagavimo užduočių srautą.

Norėdami į užduočių srautą įtraukti pasirinktinį lauką, nuvilkite elementą **Laukas** į reikiamą vietą puslapyje ir nustatykite jo ypatybes. Ypatybę **Šaltinis** nustatykite kaip **Laiko įrašas**, o ypatybę **Duomenų laukas** nustatykite kaip pasirinktinį lauką. Ypatybė **Laukas** nurodo rodomą pavadinimą TBX puslapyje. Pasirinkite **Taikyti**, kad įrašytumėte lauko keitimus. Tada pasirinkite **Naujinti**, kad įrašytumėte puslapio keitimus.

Jei norite naudoti naują pasirinktinį TBX puslapį, sukurkite naują procesą. Nustatykite kategoriją kaip **Veiklos procesų seka**, nustatykite objektą kaip **Laiko įrašas**, o veiklos proceso tipą nustatykite kaip **Vykdyti procesą kaip užduočių srautą**. Srityje **Ypatybės** ypatybė **Puslapio pavadinimas** turi būti nustatyta kaip puslapio rodomas pavadinimas. Visus reikiamus laukus įtraukite į TBX puslapį. Įrašykite ir suaktyvinkite procesą, tada atnaujinkite atitinkamo užduočių srauto pasirinktinio valdiklio ypatybę į reikšmę **Pavadinimas** procese.

### <a name="add-new-option-set-values"></a>Naujų parinkčių rinkinio reikšmių įtraukimas
Norėdami įtraukti parinkčių rinkinio reikšmių į numatytąjį lauką, atidarykite lauko redagavimo puslapį, tada srityje **Tipas** šalia parinkčių rinkinio pasirinkite **Redaguoti**. Tada įtraukite naują parinktį, turinčią pasirinktinę žymą ir spalvą. Jei norite įtraukti naują laiko įrašo būseną, numatytojo lauko pavadinimas yra **Įrašo būsena**, o ne **Būsena**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Naujos laiko įrašo būsenos nustatymas kaip skirtos tik skaityti
Norėdami nustatyti naują laiko įrašo būseną kaip skirtą tik skaityti, įtraukite naują laiko įrašo reikšmę (numerį, o ne žymą) į ypatybę **Tik skaitymo būsenos sąrašas**. Eilučių, kurios turi naują būseną, laiko įrašo tinklelio redaguojama dalis bus užrakinta.
Tada įtraukite veiklos taisyklių, kad užrakintumėte visus laukus TBX puslapiuose **Laiko įrašo eilutės redagavimas** ir **Laiko įrašo redagavimas**. Galite pasiekti šių puslapių veiklos taisykles atidarę puslapio veiklos procesų sekos rengyklę ir pasirinkę **Veiklos taisyklės**. Naują būseną galite įtraukti į esamų veiklos taisyklių sąlygą arba galite įtraukti naują naujos būsenos veiklos taisyklę.

### <a name="add-custom-validation-rules"></a>Pasirinktinių tikrinimo taisyklių įtraukimas
Yra dviejų tipų tikrinimo taisyklės, kurias galite įtraukti į savaitės laiko įrašo tinklelio patirtį: • kliento veiklos taisyklės, kurios veikia sparčiojo kūrimo dialogo languose ir TBX puslapiuose • serverio priedo tikrinimai, taikomi visiems laiko įrašų naujinimams

#### <a name="business-rules"></a>Veiklos taisyklės
Naudodami veiklos taisykles, galite užrakinti ir atrakinti laukus, laukuose įvesti numatytąsias reikšmes ir nustatyti tikrinimus, kuriems reikia informacijos tik iš esamo laiko įrašo įrašo. Galite pasiekti TBX puslapio veiklos taisykles atidarę puslapio veiklos procesų sekos rengyklę ir pasirinkę **Veiklos taisyklės**. Tada galite redaguoti esamas veiklos taisykles arba įtraukti naują veiklos taisyklę. Jei norite dar labiau tinkintų tikrinimų, galite naudoti veiklos taisyklę, kad paleistumėte „JavaScript“.

#### <a name="plug-in-validations"></a>Priedo tikrinimai
Norėdami atlikti bet kokius tikrinimus, kuriems reikia daugiau konteksto, nei yra viename laiko įrašo įraše, arba bet kokius norimus eilutės atnaujinimų tinklelyje tikrinimus, turėtumėte naudoti priedo tikrinimus. Norėdami baigti tikrinimą, sukurkite pasirinktinį priedą įraše **Laiko įrašas**.

> [!IMPORTANT] 
> Šiuo metu žinoma problema, esanti TBX puslapiuose, neleidžia vartotojams taisyti informacijos ir iš naujo pasirinkti Atlikta, kai naujinimo priedo tikrinimas nesėkmingas. Kaip problemos sprendimą nustatykite veiklos taisyklės tikrinimus, kad, kiek įmanoma, būtų išvengta šios situacijos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
