---
title: Laiko įrašų išplėtimas
description: Šiame straipsnyje pateikta informacija apie tai, kaip kūrėjai gali išplėsti laiko įrašų valdiklį.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914780"
---
# <a name="extending-time-entries"></a>Laiko įrašų išplėtimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ turi išplečiamąjį laiko įrašo pasirinktinį valdiklį. Šiame valdiklyje yra tokių funkcijų:

- Įveskite laiką horizontaliai per savaitę
- Bendrosios sumos pagal dieną, eilutę arba savaitę
- Kopijuoti eilutes ar savaites
- Laiko įvestis per VV:mm arba VV.vv (automatiškai konvertuojama į VV.vv)
- Importavimas iš užduočių, užsakymų arba paskyrų

Laiko įrašų išplėtimas galimas dviejose srityse:
- [Pasirinktinių laiko įrašų įtraukimas asmeniniam naudojimui](#add)
- [Savaitės laiko įrašo valdiklio tinkinimas](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Pasirinktinių laiko įrašų įtraukimas asmeniniam naudojimui

Laiko įrašai yra pagrindinis objektas, naudojamas keliuose scenarijuose. 2020 m. balandžio 1 bangos leidime pristatytas TESA pagrindinis sprendimas. TESA teikia objektą **Parametrai** ir naują saugos vaidmenį **Laiko įrašo vartotojas**. Tai pat įtraukti nauji laukai **msdyn_start** ir **msdyn_end**, kurie yra tiesiogiai susiję su **msdyn_duration**. Naujas objektas, saugos vaidmuo ir laukai leidžia vieningesnį požiūrį į laiką keliuose produktuose.


### <a name="time-source-entity"></a>Laiko šaltinio objektas
| Laukas | Aprašo | 
|-------|------------|
| Pavadinimas / vardas, pavardė  | Laiko šaltinio įrašo, naudojamo kaip pasirinkimo reikšmė, kai kuriamas laiko įrašas, pavadinimas. |
| Numatytasis laiko šaltinis [laiko šaltinis: isdefault] | Pagal numatytuosius nustatymus tik vienas laiko šaltinis gali būti pažymėtas numatytuoju. Ši galimybė leidžia priskirti įrašų numatytuosius nustatymus laiko šaltiniui, jei jis nenurodytas. |
|Laiko šaltinio tipas [laiko šaltinis: sourcetype] | Šaltinio tipas yra parinktis (laiko įrašo šaltinio tipas), leidžianti susieti laiko šaltinį su programa. „Microsoft“ rezervuoja didesnes nei 190,000,000 reikšmes.|


### <a name="time-entries-and-the-time-source-entity"></a>Laiko įrašai ir laiko šaltinio objektas
Kiekvieną kartą laiko įrašas susiejamas su laiko šaltinio įrašu. Šis įrašas nustato, kaip ir kokios programos turėtų apdoroti laiko įrašą.

Laiko įrašai visada yra vienas nepertraukiamo laiko blokas, susijęs su pradžia, pabaiga ir trukme.

Logika automatiškai atnaujins laiko įrašo įrašą šiose situacijose:

- Jei pateikiami du iš trijų nurodytų laukų, trečiasis apskaičiuojamas automatiškai. 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Laukuose **msdyn_start** ir **msdyn_end** paisoma laiko juostos.
- Laiko įrašai, sukurti naudojant tik **msdyn_date** ir **msdyn_duration**, prasidės vidurnaktį. Laukai **msdyn_start** ir **msdyn_end** bus atitinkamai atnaujinti.

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

1. Įtraukite pasirinktinį lauką į dialogo langą **Spartusis kūrimas**.
2. Sukonfigūruokite tinklelį, kad būtų rodomas pasirinktinis laukas.
3. Įtraukite pasirinktinį lauką atitinkamai į puslapį **Eilutės redagavimas** arba **Laiko įrašas**.

Įsitikinkite, kad naujas laukas turi reikiamus tikrinimus puslapyje **Eilutės redagavimas** arba **Laiko įrašas**. Atlikdami šią užduotį, užrakinkite lauką pagal laiko įrašo būseną.

Kai įtraukiate pasirinktinį lauką į tinklelį **Laiko įrašas**, tada sukuriate laiko įrašus tiesiogiai tinklelyje, šių įrašų pasirinktinis laukas nustatomas automatiškai, kad atitiktų eilutę. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pasirinktinio lauko įtraukimas į sparčiojo kūrimo dialogo langą
Į dialogo langą **Spartusis kūrimas: laiko įrašo kūrimas** įtraukite pasirinktinį lauką. Vartotojai gali įvesti reikšmę įtraukdami laiko įrašus pasirinkdami **Naujas**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Sukonfigūruokite tinklelį, kad būtų rodomas pasirinktinis laukas
Įtraukti pasirinktinį lauką į tinklelį **Savaitės laiko įrašas** galima dviem būdais.

- Tinkinkite rodinį **Mano savaitės laiko įrašai** ir įtraukite į jį pasirinktinį lauką. Galite nurodyti pasirinktinio lauko padėtį ir dydį tinklelyje redaguodami šias ypatybes rodinyje.
- Sukurkite naują pasirinktinį laiko įrašo rodinį ir nustatykite jį kaip numatytąjį rodinį. Šiame rodinyje turėtų būti laukai **Aprašas** ir **Išoriniai komentarai**, taip pat stulpeliai, kurie turėtų būti tinklelyje. Galite nurodyti tinklelio padėtį, dydį ir numatytąją rikiavimo tvarką redaguodami šias ypatybes rodinyje. Tada sukonfigūruokite pasirinktinį šio rodinio valdiklį, kad jis būtų valdiklis **Laiko įrašo tinklelis**. Įtraukite šį valdiklį į rodinį ir pasirinkite jį naudoti **Žiniatinklyje**, **Telefone** ir **Planšetiniame kompiuteryje**. Tada sukonfigūruokite tinklelio **Savaitės laiko įrašas** parametrus. Lauką **Pradžios data** nustatykite kaip **msdyn\_date**, lauką **Trukmė** nustatykite kaip **msdyn\_duration**, o lauką **Būsena** nustatykite kaip **msdyn\_entrystatus**. Laukas **Tik skaitymo būsenos sąrašas** nustatomas kaip **192350002 (Patvirtinta)**, **192350003 (Pateikta)** arba **192350004 (Pateikta atšaukimo užklausa)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Pasirinktinio lauko įtraukimas į atitinkamą redagavimo puslapį
Puslapius, naudojamus laiko įrašui arba laiko įrašų eilutei redaguoti, galima rasti dalyje **Formos**. Tinklelio mygtukas **Redaguoti įrašą** atidaro puslapį **Įrašo redagavimas**, o mygtukas **Redaguoti eilutę** atidaro puslapį **Eilutės redagavimas**. Galite redaguoti šiuos puslapius, kad juose būtų pasirinktinių laukų.

Abi parinktys pašalina kai kuriuos parengtus naudoti objektų **Projektas** ir **Projekto užduotis** filtrus, todėl rodomi visi objektų peržvalgos rodiniai. Pirmą kartą paleidus matomi tik susiję peržvalgos rodiniai.

Turite nustatyti tinkamą pasirinktinio lauko puslapį. Tikriausiai, jei įtraukėte lauką į tinklelį, jis turėtų patekti į puslapį **Eilutės redagavimas**, naudojamą laukams, kurie taikomi visai laiko įrašų eilutei. Jei pasirinktinis laukas eilutėje kiekvieną dieną turi skirtingą reikšmę (pvz., pabaigos laiko pasirinktinis laukas), jis turėtų patekti į puslapį **Laiko įrašo redagavimas**.

Norėdami į puslapį įtraukti pasirinktinį lauką, nuvilkite elementą **Laukas** į reikiamą vietą puslapyje ir nustatykite jo ypatybes.

### <a name="add-new-option-set-values"></a>Naujų parinkčių rinkinio reikšmių įtraukimas
Norėdami parinkčių rinkinio reikšmes įtraukti į parengtą naudoti lauką, atlikite toliau nurodytus veiksmus.

1. Atidarykite lauko redagavimo puslapį, tada srityje **Tipas** šalia parinkčių rinkinio pasirinkite **Redaguoti**.
2. Įtraukite naują parinktį, turinčią pasirinktinę žymą ir spalvą. Jei norite įtraukti naują laiko įrašo būseną, parengto naudoti lauko pavadinimas yra **Įrašo būsena**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Naujos laiko įrašo būsenos nustatymas kaip skirtos tik skaityti
Norėdami nustatyti naują laiko įrašo būseną kaip skirtą tik skaityti, įtraukite naują laiko įrašo reikšmę į ypatybę **Tik skaitymo būsenos sąrašas**. Įsitikinkite, kad pridedate skaičių, o ne etiketę. Dabar eilučių, kurios turi naują būseną, laiko įrašo tinklelio redaguojama dalis bus užrakinta. Jei ypatybę **Tik skaitymo būsenos sąrašas** norite skirtingai nustatyti skirtingiems rodiniams **Laiko įrašas**, įtraukite tinklelį **Laiko įrašas** į rodinio skyrių **Pasirinktiniai valdikliai** ir atitinkamai sukonfigūruokite parametrus.

Tada įtraukite veiklos taisyklių, kad užrakintumėte visus laukus puslapiuose **Eilutės redagavimas** ir **Laiko įrašo redagavimas**. Norėdami pasiekti šių puslapių veiklos taisykles, atidarykite kiekvieno puslapio formų rengyklę, tada pasirinkite **Veiklos taisyklės**. Naują būseną galite įtraukti į esamų veiklos taisyklių sąlygą arba galite įtraukti naują naujos būsenos veiklos taisyklę.

### <a name="add-custom-validation-rules"></a>Pasirinktinių tikrinimo taisyklių įtraukimas
Galite pridėti dviejų tipų tikrinimo taisyklių, skirtų **Savaitės laiko įrašas** tinkleliui:

- Puslapiuose taikomos kliento verslo taisyklės
- Serverio priedo tikrinimai, kurie taikomi visiems laiko įrašų atnaujinimams

#### <a name="client-side-business-rules"></a>Kliento verslo taisyklės
Naudodami veiklos taisykles, galite užrakinti ir atrakinti laukus, laukuose įvesti numatytąsias reikšmes ir nustatyti tikrinimus, kuriems reikia informacijos tik iš esamo laiko įrašo įrašo. Norėdami pasiekti puslapio veiklos taisykles, atidarykite formų rengyklę, tada pasirinkite **Veiklos taisyklės**. Tada galite redaguoti esamas veiklos taisykles arba įtraukti naują veiklos taisyklę.

#### <a name="server-side-plug-in-validations"></a>Serverio priedų tikrinimai
Norėdami atlikti bet kokius tikrinimus, kuriems reikia daugiau konteksto, nei yra viename laiko įrašo įraše, turite naudoti priedo tikrinimus. Taip pat juos turėtumėte naudoti visiems tikrinimams, kuriuos tinklelyje norite taikyti įdėtiesiems naujinimams. Norėdami atlikti tikrinimus, sukurkite pasirinktinį priedą objekte **Laiko įrašas**.

### <a name="limits"></a>Apribojimai
Šiuo metu tinkleliui **Laiko įrašas** taikomas dydžio apribojimas iki 500 eilučių. Jei yra daugiau nei 500 eilučių, tos eilutės nebus rodomos. Nėra jokios galimybės padidinti šį dydžio apribojimą.

### <a name="copying-time-entries"></a>Laiko įrašų kopijavimas
Norėdami apibrėžti laukų, kuriuos reikia kopijuoti įrašant laiką, sąrašą, naudokite rodinį **Kopijuoti laiko įrašo stulpelius**. **Data** ir **Trukmė** yra būtini laukai, todėl jų negalima pašalinti iš rodinio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
