---
title: Laiko įrašų išplėtimas
description: Šioje temoje pateikta informacija apie tai, kaip kūrėjai gali išplėsti laiko įrašų valdiklį.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582996"
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
Kiekvieną kartą laiko įrašas susiejamas su laiko šaltinio įrašu. Šis įrašas nustato, kurios paraiškos turėtų apdoroti laiko įrašą ir kaip.

Laiko įrašai visada yra vienas nepertraukiamo laiko blokas, susijęs su pradžia, pabaiga ir trukme.

Logika automatiškai atnaujins laiko įrašo įrašą šiose situacijose:

- Jei pateikiami du iš trijų nurodytų laukų, trečiasis apskaičiuojamas automatiškai. 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- msdyn_start **ir** **msdyn_end** laukai žino laiko juostą.
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

1. Įtraukite pasirinktinį lauką į dialogo langą **Spartus kūrimas**.
2. Sukonfigūruokite tinklelį, kad būtų rodomas pasirinktinis laukas.
3. Jei reikia, įtraukite pasirinktinį lauką į **puslapį Eilutės redagavimas** arba **Laiko įrašo redagavimas**.

Įsitikinkite, kad naujame lauke yra reikiamas tikrinimas puslapyje Eilutės redagavimas **arba** **Laiko įrašo redagavimas**. Atlikdami šią užduotį užrakinkite lauką pagal laiko įrašo būseną.

Kai į **tinklelį Laiko įrašas** įtraukiate pasirinktinį lauką ir sukuriate laiko įrašus tiesiai tinklelyje, šių įrašų pasirinktinis laukas automatiškai nustatomas taip, kad jis atitiktų eilutę. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Pasirinktinio lauko įtraukimas į dialogo langą Spartus kūrimas
Įtraukite pasirinktinį lauką į dialogo langą **Greitas kūrimas: kurti laiko įrašą**. Vartotojai gali įvesti reikšmę įtraukdami laiko įrašus pasirinkdami **Naujas**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Sukonfigūruokite tinklelį, kad būtų rodomas pasirinktinis laukas
Yra du būdai įtraukti pasirinktinį lauką į savaitės laiko įvedimo **tinklelį**.

- Tinkinkite **rodinį Mano savaitės laiko įrašai** ir įtraukite į jį pasirinktinį lauką. Redaguodami rodinio ypatybes galite nurodyti pasirinktinio lauko vietą ir dydį tinklelyje.
- Sukurkite naują pasirinktinio laiko įrašo rodinį ir nustatykite jį kaip numatytąjį rodinį. Šiame rodinyje, be stulpelių **, kuriuos norite įtraukti tinklelyje, turėtų būti laukai Aprašas** ir **Išoriniai komentarai**. Redaguodami rodinio ypatybes galite nurodyti tinklelio padėtį, dydį ir numatytąją rūšiavimo tvarką. Tada sukonfigūruokite pasirinktinį šio rodinio valdiklį, kad jis būtų valdiklis **Laiko įrašo tinklelis**. Įtraukite valdiklį į rodinį ir pasirinkite jį **žiniatinklyje**, **telefone** ir **planšetiniame kompiuteryje**. Tada konfigūruokite savaitės laiko įvedimo **tinklelio** parametrus. **Nustatykite lauką Pradžios data** į **Msdyn\_ datą**, nustatykite **lauką Trukmė** į **msdyn\_ trukmę** ir nustatykite **lauką Būsena** į **msdyn\_ entrystatus**. Laukas Tik **skaitomas būsenų sąrašas** nustatytas kaip **192350002 (patvirtinta)**, **192350003 (pateikta)**, arba **192350004 (atšaukta prašoma)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Pasirinktinio lauko įtraukimas į atitinkamą redagavimo puslapį
Puslapius, naudojamus laiko įrašui arba laiko įrašų eilutei redaguoti, galima rasti dalyje **Formos**. Tinklelio mygtukas **Redaguoti įrašą** atidaro **puslapį Redaguoti įrašą**, o mygtukas **Redaguoti eilutę** atidaro puslapį Eilutės **redagavimas**. Galite redaguoti šiuos puslapius, kad juose būtų pasirinktiniai laukai.

Abi parinktys pašalina kai kuriuos "Project" ir **"** Project Task **" objektų filtravimą** lauke, kad būtų matomi visi objektų peržvalgos rodiniai. Pirmą kartą paleidus matomi tik susiję peržvalgos rodiniai.

Turite nustatyti atitinkamą pasirinktinio lauko puslapį. Labiausiai tikėtina, kad jei įtraukėte lauką į tinklelį, jis turėtų eiti į **puslapį Eilutės redagavimas**, kuris naudojamas laukams, taikomiems visai laiko įrašų eilutei. Jei pasirinktinis laukas kiekvieną dieną eilutėje turi unikalią reikšmę (pvz., jei tai pasirinktinis pabaigos laiko laukas), jis turėtų būti rodomas **puslapyje Laiko įrašo redagavimas**.

Norėdami įtraukti pasirinktinį lauką į puslapį, vilkite lauko **elementą** į atitinkamą puslapio vietą ir nustatykite jo ypatybes.

### <a name="add-new-option-set-values"></a>Naujų parinkčių rinkinio reikšmių įtraukimas
Norėdami įtraukti parinkčių rinkinys reikšmes į lauką lauke, kuriame nėra langelio, atlikite šiuos veiksmus.

1. Atidarykite lauko redagavimo puslapį, tada dalyje **Tipas** šalia parinkčių rinkinys pasirinkite **Redaguoti**.
2. Įtraukite naują parinktį, turinčią pasirinktinę žymą ir spalvą. Jei norite įtraukti naują laiko įrašo būseną, laukas lauke Lauke Yra įrašo **būsena**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Naujos laiko įrašo būsenos nustatymas kaip skirtos tik skaityti
Norėdami nustatyti naują laiko įrašo būseną kaip skirtą tik skaityti, įtraukite naują laiko įrašo reikšmę į ypatybę **Tik skaitymo būsenos sąrašas**. Būtinai pridėkite numerį, o ne etiketę. Redaguojama laiko įvedimo tinklelio dalis dabar bus užrakinta eilutėms, turinčioms naują būseną. Norėdami skirtingai nustatyti **ypatybę Tik skaityti skirtas būsenų sąrašas** skirtingiems **laiko įrašo** rodiniams, įtraukite **laiko įrašo** tinklelį į rodinio pasirinktinių **valdiklių** sekciją ir atitinkamai konfigūruokite parametrus.

Tada įtraukite verslo taisykles, kad užrakintumėte visus laukus, esančius puslapiuose Eilutės redagavimas **ir** **Laiko įrašo redagavimas**. Norėdami pasiekti šių puslapių verslo taisykles, atidarykite kiekvieno puslapio formų rengyklė, tada pasirinkite **Verslo taisyklės**. Naują būseną galite įtraukti į esamų veiklos taisyklių sąlygą arba galite įtraukti naują naujos būsenos veiklos taisyklę.

### <a name="add-custom-validation-rules"></a>Pasirinktinių tikrinimo taisyklių įtraukimas
Savaitės laiko įvedimo **tinklelio patirtį galite įtraukti dviejų tipų tikrinimo taisykles**:

- Kliento verslo taisyklės, veikiančios puslapiuose
- Serverio priedo patvirtinimai, taikomi visų laikų įrašų naujinimams

#### <a name="client-side-business-rules"></a>Kliento verslo taisyklės
Naudodami veiklos taisykles, galite užrakinti ir atrakinti laukus, laukuose įvesti numatytąsias reikšmes ir nustatyti tikrinimus, kuriems reikia informacijos tik iš esamo laiko įrašo įrašo. Norėdami pasiekti puslapio verslo taisykles, atidarykite formų rengyklė, tada pasirinkite **Verslo taisyklės**. Tada galite redaguoti esamas veiklos taisykles arba įtraukti naują veiklos taisyklę.

#### <a name="server-side-plug-in-validations"></a>Serverio papildinio tikrinimas
Priedų patvirtinimus turėtumėte naudoti bet kokiems patvirtinimams, kuriems reikia daugiau konteksto, nei galima pasiekti vieno laiko įrašo įraše. Taip pat turėtumėte juos naudoti bet kokiems patvirtinimams, kuriuos norite vykdyti įdėtuosiuose naujiniuose tinklelyje. Norėdami užbaigti tikrinimą, objekte Laiko įrašas **sukurkite** pasirinktinį priedą.

### <a name="limits"></a>Apribojimai
Šiuo metu laiko įvedimo **tinklelyje** yra 500 eilučių dydžio riba. Jei yra daugiau nei 500 eilučių, perteklinės eilutės nebus rodomos. Nėra jokio būdo padidinti šią dydžio ribą.

### <a name="copying-time-entries"></a>Laiko įrašų kopijavimas
Norėdami apibrėžti laukų, kuriuos reikia kopijuoti įrašant laiką, sąrašą, naudokite rodinį **Kopijuoti laiko įrašo stulpelius**. **Data** ir **Trukmė** yra būtini laukai, todėl jų negalima pašalinti iš rodinio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
