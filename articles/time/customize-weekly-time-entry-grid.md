---
title: Laiko įrašų išplėtimas
description: Šioje temoje pateikta informacija apie tai, kaip kūrėjai gali išplėsti laiko įrašų valdiklį.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930890"
---
# <a name="extending-time-entries"></a>Laiko įrašų išplėtimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ yra išskleidžiamas laiko įrašo pasirinktinis valdiklis. Šiame valdiklyje yra tokių funkcijų:

- Įveskite laiką horizontaliai per savaitę
- Bendrosios sumos pagal dieną, eilutę arba savaitę
- Kopijuoti eilutes ar savaites
- Laiko įvestis per VV:mm arba VV.vv (automatiškai konvertuojama į VV.vv)
- Importavimas iš užduočių, užsakymų arba paskyrų

Laiko įrašų išplėtimas galimas dviejose srityse:
- [Pasirinktinių laiko įrašų įtraukimas asmeniniam naudojimui](#add)
- [Savaitės laiko įrašo valdiklio tinkinimas](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Pasirinktinių laiko įrašų įtraukimas asmeniniam naudojimui.

Laiko įrašai yra pagrindinis objektas, skirtas naudoti keliems scenarijams. 2020 m. balandžio mėn. 1 leidimo bangoje buvo pristatytas TESA pagrindinis sprendimas, kuriame yra objektas **Parametrai** ir naujas **Laiko įrašų vartotojo** saugos vaidmuo. Tai pat įtraukti nauji laukai **msdyn_start** ir **msdyn_end**, kurie yra tiesiogiai susiję su **msdyn_duration**. Naujas objektas, saugos vaidmuo ir laukai leidžia vieningesnį požiūrį į laiką keliuose produktuose.


### <a name="time-source-entity"></a>Laiko šaltinio objektas
| Laukas | Aprašo | 
|-------|------------|
| Pavadinimas / vardas, pavardė  | Laiko šaltinio įrašo, naudojamo kaip pasirinkimo reikšmė, kai kuriamas laiko įrašas, pavadinimas. |
| Numatytasis laiko šaltinis [laiko šaltinis: isdefault] | Pagal numatytuosius nustatymus tik vienas laiko šaltinis gali būti pažymėtas numatytuoju laiko šaltiniu. Ši galimybė leidžia priskirti įrašų numatytuosius nustatymus laiko šaltiniui, jei jis nenurodytas. |
|Laiko šaltinio tipas [laiko šaltinis: sourcetype] | Šaltinio tipas yra parinktis (laiko įrašo šaltinio tipas), leidžianti susieti laiko šaltinį su programa. į šį parinkčių rinkinį papildomos reikšmės bus įtrauktos kaip įtraukiamos papildomos programos. Atminkite, kad „Microsoft“ rezervuoja didesnes nei 190,000,000 reikšmes.|


### <a name="time-entries-and-the-time-source-entity"></a>Laiko įrašai ir laiko šaltinio objektas
Kiekvieną kartą laiko įrašas susiejamas su laiko šaltinio įrašu. Šis įrašas nustato, kaip ir kokios programos turėtų apdoroti laiko įrašą.

Laiko įrašai visada yra vienas nepertraukiamo laiko blokas, susijęs su pradžia, pabaiga ir trukme.

Logika automatiškai atnaujins laiko įrašo įrašą šiose situacijose:

- Jei pateikiami du iš trijų nurodytų laukų, trečiasis apskaičiuojamas automatiškai 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Laukuose **msdyn_start** ir **msdyn_end** paisoma laiko juosta.
- Laiko įrašai, sukurti naudojant tik **msdyn_date** ir **msdyn_duration** prasidės nuo vidurnakčio, o **msdyn_start** ir **msdyn_end** bus atitinkamai atnaujinti.

#### <a name="time-entry-types"></a>Laiko įrašo tipai

Laiko įrašų įrašuose yra susietas tipas, apibrėžiantis elgesį susietos programos pateikimo sraute.

|Žyma | Reikšmė|
|-----|-----|
|Pertrauka   |192,355,000|
|Kelionė | 192,355,001|
|Viršvalandžiai   | 192,354,320|
|Darbas   | 192,350,000|
|Nebuvimas darbe    | 192,350,001|
|Atostogos   | 192,350,002|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Savaitės laiko įrašo valdiklio tinkinimas
Kūrėjai gali įtraukti papildomų laukų ir peržvalgų į kitus objektus bei diegti pasirinktines veiklos taisykles savo verslo scenarijams palaikyti.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Pasirinktinių laukų su peržvalgomis įtraukimas į kitus objektus
Yra trys pagrindiniai veiksmai, kaip į savaitės laiko įrašo tinklelį įtraukti pasirinktinį lauką.

- Įtraukite pasirinktinį lauką į sparčiojo kūrimo dialogo langą.
- Sukonfigūruokite tinklelį, kad būtų rodomas pasirinktinis laukas.
- Įtraukite pasirinktinį lauką į eilutės redagavimo užduočių srautą arba langelio redagavimo užduočių srautą.

Be to, reikia įsitikinti, ar naujas laukas turi reikiamus tikrinimus eilutės arba langelio redagavimo užduočių sraute. Atlikdami šį žingsnį, turite užrakinti lauką pagal laiko įrašo būseną.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pasirinktinio lauko įtraukimas į sparčiojo kūrimo dialogo langą
Į dialogo langą **Laiko įrašo spartusis kūrimas** reikia įtraukti pasirinktinį lauką. Vartotojai gali įvesti reikšmę įtraukdami laiko įrašus pasirinkdami **Naujas**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Sukonfigūruokite tinklelį, kad būtų rodomas pasirinktinis laukas
Įtraukti pasirinktinį lauką į savaitės laiko įrašo tinklelį galima dviem būdais:

  - Rodinio tinkinimas ir pasirinktinio lauko įtraukimas
  - Naujo numatytojo pasirinktinio laiko įrašo kūrimas 


**Rodinio tinkinimas ir pasirinktinio lauko įtraukimas**

Galite tinkinti rodinį **Mano savaitės laiko įrašai** ir įtraukti į jį pasirinktinį lauką. Galite pasirinkti pasirinktinio lauko padėtį ir dydį tinklelyje redaguodami šias ypatybes rodinyje.

**Naujo numatytojo pasirinktinio laiko įrašo kūrimas** 

Šiame rodinyje turėtų būti laukai **Aprašas** ir **Išoriniai komentarai**, taip pat stulpeliai, kurie turėtų būti tinklelyje. 

1. Pasirinkite tinklelio padėtį, dydį ir numatytąją rikiavimo tvarką redaguodami šias ypatybes rodinyje. 
2. Sukonfigūruokite pasirinktinį šio rodinio valdiklį, kad jis būtų **Laiko įrašo tinklelis** valdikliu. 
3. Įtraukite šį valdiklį į rodinį ir pasirinkite jį žiniatinklyje, telefone ir planšetiniame kompiuteryje. 
4. Sukonfigūruokite savaitės laiko įrašo tinklelio parametrus. Lauką **Pradžios data** nustatykite kaip **msdyn_date**, lauką **Trukmė** nustatykite kaip **msdyn_duration**, o lauką **Būsena** nustatykite kaip **msdyn_entrystatus**. 
5. Naudojant numatytąjį rodinį laukas **Tik skaitymo būsenos sąrašas** nustatytas kaip **192350002,192350003,192350004**, laukas **Eilutės redagavimo užduočių srautas**nustatytas kaip **msdyn_timeentryrowedit**, o laukas **Langelio redagavimo užduočių srautas** nustatytas kaip **msdyn_timeentryedit**. 
6. Galite tinkinti šiuos laukus, jei norite įtraukti arba pašalinti tik skaitymo būseną arba naudoti kitą užduotimi pagrįstą funkciją (TBX) eilutėms arba langeliams redaguoti. Šie laukai turi būti susieti su pastovia reikšme.


> [!NOTE] 
> Abi parinktys pašalins kai kuriuos parengtus naudoti objektų **Projektas** ir **Projekto užduotis** filtrus, todėl bus rodomi visi objektų peržvalgos rodiniai. Iš anksto nustatytose funkcijose matomi tik susiję peržvalgos rodiniai.
Turite nustatyti tinkamą pasirinktinio lauko užduočių srautą. Tikriausiai, jei įtraukėte lauką į tinklelį, jis turėtų patekti į eilutės redagavimo užduočių srautą, naudojamą laukuose, kurie taikomi visai laiko įrašų eilutei. Jei pasirinktinis lauką kiekvieną dieną turi skirtingą reikšmę, pvz., **Pabaigos laiko** pasirinktinis laukas, jis turėtų patekti į langelio redagavimo užduočių srautą.

Norėdami į užduočių srautą įtraukti pasirinktinį lauką, nuvilkite elementą **Laukas** į reikiamą vietą puslapyje ir nustatykite lauko ypatybes. Ypatybę **Šaltinis** nustatykite kaip **Laiko įrašas**, o ypatybę **Duomenų laukas** nustatykite kaip pasirinktinį lauką. Ypatybė **Laukas** nurodo rodomą pavadinimą TBX puslapyje. Pasirinkite **Taikyti**, kad įrašytumėte keitimus lauke, o tada pasirinkite **Atnaujinti**, kad įrašytumėte pakeitimus puslapyje.

Jei norite naudoti naują pasirinktinį TBX puslapį, sukurkite naują procesą. Nustatykite kategoriją kaip **Veiklos procesų seka**, nustatykite objektą kaip **Laiko įrašas**, o veiklos proceso tipą nustatykite kaip **Vykdyti procesą kaip užduočių srautą**. Srityje **Ypatybės** ypatybė **Puslapio pavadinimas** turi būti nustatyta kaip puslapio rodomas pavadinimas. Visus reikiamus laukus įtraukite į TBX puslapį. Įrašykite ir suaktyvinkite procesą, tada atnaujinkite atitinkamo užduočių srauto pasirinktinio valdiklio ypatybę į reikšmę **Pavadinimas** procese.

### <a name="add-new-option-set-values"></a>Naujų parinkčių rinkinio reikšmių įtraukimas
Norėdami įtraukti parinkčių rinkinio reikšmių į numatytąjį lauką, atidarykite lauko redagavimo puslapį, tada srityje **Tipas** šalia parinkčių rinkinio pasirinkite **Redaguoti**. Tada įtraukite naują parinktį, turinčią pasirinktinę žymą ir spalvą. Jei norite įtraukti naują laiko įrašo būseną, numatytojo lauko pavadinimas yra **Įrašo būsena**, o ne **Būsena**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Naujos laiko įrašo būsenos nustatymas kaip skirtos tik skaityti
Norėdami nustatyti naują laiko įrašo būseną kaip skirtą tik skaityti, įtraukite naują laiko įrašo reikšmę į ypatybę **Tik skaitymo būsenos sąrašas**. Eilučių, kurios turi naują būseną, laiko įrašo tinklelio redaguojama dalis bus užrakinta.
Tada įtraukite veiklos taisyklių, kad užrakintumėte visus laukus TBX puslapiuose **Laiko įrašo eilutės redagavimas** ir **Laiko įrašo redagavimas**. Galite pasiekti šių puslapių veiklos taisykles atidarę puslapio veiklos procesų sekos rengyklę ir pasirinkę **Veiklos taisyklės**. Naują būseną galite įtraukti į esamų veiklos taisyklių sąlygą arba galite įtraukti naują naujos būsenos veiklos taisyklę.

### <a name="add-custom-validation-rules"></a>Pasirinktinių tikrinimo taisyklių įtraukimas
Yra dviejų tipų tikrinimo taisyklių, kurias galite įtraukti į savaitės laiko įrašo tinklelio patirtį:

- Kliento veiklos taisyklės, kurios veikia sparčiojo kūrimo dialogo languose ir TBX puslapiuose.
- Serverio priedo patikros, kurios taikomos visiems laiko įrašų atnaujinimams.

#### <a name="business-rules"></a>Verslo taisyklės
Naudodami veiklos taisykles, galite užrakinti ir atrakinti laukus, laukuose įvesti numatytąsias reikšmes ir nustatyti tikrinimus, kuriems reikia informacijos tik iš esamo laiko įrašo įrašo. Galite pasiekti TBX puslapio veiklos taisykles atidarę puslapio veiklos procesų sekos rengyklę ir pasirinkę **Veiklos taisyklės**. Tada galite redaguoti esamas veiklos taisykles arba įtraukti naują veiklos taisyklę. Jei norite dar labiau tinkintų tikrinimų, galite naudoti veiklos taisyklę, kad paleistumėte „JavaScript“.

#### <a name="plug-in-validations"></a>Priedo tikrinimai
Norėdami atlikti bet kokius tikrinimus, kuriems reikia daugiau konteksto, nei yra viename laiko įrašo įraše, arba bet kokius norimus eilutės atnaujinimų tinklelyje tikrinimus, turėtumėte naudoti priedo tikrinimus. Norėdami baigti tikrinimą, sukurkite pasirinktinį priedą įraše **Laiko įrašas**.
