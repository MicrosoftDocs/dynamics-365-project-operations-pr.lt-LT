---
title: Laiko įrašo vartotojo sąsajos veikimas
description: Šioje temoje pateikiama informacija apie laiko įrašo vartotojo sąsajos veikimą.
author: stsporen
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 86f805cd33f81e70bf9ae3c1fb20a1c310473604
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961729"
---
# <a name="time-entry-ui-behavior"></a>Laiko įrašo vartotojo sąsajos veikimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


Tinklelis **Savaitės laiko įrašas** yra pasirinktinis valdiklis, kuriame yra du skyriai: **Dimensijos** ir **Trukmė**.

## <a name="dimensions"></a>Dimensijos
Skyriuje **Dimensijos** rodomos visos dimensijos, prie kurių galima įvesti laiką. Toliau nurodytos dimensijos yra visiškai parengtos naudoti.

  - Project
  - Projekto užduotis
  - Vaidmuo
  - Tipas
  - Įrašo būsena

Skyriuje **Dimensijos** negalima atlikti įdėtojo redagavimo. Šiame skyriuje palaikomas rodinys, leidžiantis į savaitės laiko įrašo tinklelį įtraukti pasirinktinių laukų.

## <a name="duration"></a>Trukmė
Skyrius Trukmė rodo savaitės dienas kaip stulpelių antraštes. Šiame skyriuje leidžiamas įdėtasis redagavimas. Sukūrus laiko įrašo eilutę, kurioje yra atitinkamos dimensijos, vartotojai gali greitai eilutėje įvesti laiką, kurį skyrė šioms dimensijoms.

## <a name="create-a-new-time-entry"></a>Naujo laiko įrašo kūrimas

1. Laiko įrašo tinklelyje pasirinkite **Naujas**. 
2. Dialogo lange **Laiko įrašo spartusis kūrimas** pasirinkite laiko įrašo datą.
3. Įveskite duomenis dimensijose **Projektas**, **Projekto užduotis**, **Vaidmuo** ir **Trukmė**. Reikia nurodyti minutes, valandas arba dienas įvedant **h**, **min** arba **d** kartu su skaičiumi. 
4. Įveskite įrašo aprašą ir bet kokius laiko įrašo komentarus, kuriuos galima bendrinti išoriškai. 

Įrašius įrašą, įvestos reikšmės bus rodomos skyriuje **Dimensijos**. Informacija, įvesta lauke **Trukmė**, rodoma tą dieną, kuriai buvo sukurtas laiko įrašas.

Peržvalgos laukus teikia sistemos rodiniai. Pavyzdžiui, kai vartotojas įveda projektą, laukas **Projekto užduotis** pagal numatytuosius nustatymus nustatomas į rodinį **Kopijuoti**. Norėdami kurti užduočių, kurios nepriskirtos vartotojui, laiko įrašus, peržvalgos dialogo lange pasirinkite **Keisti rodinį**, tada pasirinkite rodinį **Visos aktyvios projekto užduotys**.

## <a name="edit-a-time-entry"></a>Laiko įrašo redagavimas 
Kai kurių laukų laiko įrašų puslapyje išsami informacija, pvz., **Aprašas** ir **Išoriniai komentarai** savaitės laiko įrašo tinklelyje nerodoma. Vietoj to, langeliuose **Trukmė**, kuriuose yra ši papildoma išsami informacija, bus rodomas nedidelis trikampis indikatorius. 

1. Norėdami redaguoti laiko įrašą, pasirinkite laiko įrašo langelį, kurį norite atnaujinti.
2. Pasirinkite **Redaguoti išsamią informaciją**, kad atnaujintumėte duomenis srityje **Laiko įrašo pagrindinė forma**. 

## <a name="copy-a-time-entry-row"></a>Laiko įrašo eilutės kopijavimas
Sukūrę eilutę, galite pasirinkti **Kopijuoti eilutę** ir nukopijuoti visą eilutę į naują eilutę. Tokiu būdu nukopijavus eilutę, taip pat nukopijuojamos dimensijos ir trukmė. Taip pat galite pasirinkti **Redaguoti eilutę**, kad skyriuje **Trukmė** eilutėje atnaujintumėte dimensijos reikšmes ir trukmę.

## <a name="open-a-time-entry-behavior"></a>Laiko įrašo atidarymas
Kad būtų galima optimaliai ir greitai įvesti duomenis svarbiausiuose laukuose, savaitės laiko įrašo tinklelyje rodomas pasirinktų dimensijų ir laiko trukmės pogrupis. Norėdami peržiūrėti visą išsamią vieno laiko įrašo informaciją, srityje **Redaguoti įrašą** pasirinkite **Atidaryti**.

## <a name="submit-a-time-entry"></a>Laiko įrašo pateikimas
Galite pateikti vieną laiko įrašą arba laiko įrašų grupę, pasirinkdami langelių bloką arba visą laiko įrašo eilutę, o tada pasirinkdami **Pateikti**. Pateikti laiko įrašai rodomi kaip įrašai, laukiantys patvirtinimo tvirtintojo puslapyje **Tvirtinimas**. Sėkmingai pateikus laiko įrašus jų redaguoti negalima.

## <a name="recall-a-time-entry"></a>Laiko įrašo atšaukimas
Galite atšaukti laiko įrašus, kuriuos pateikėte. Galite atšaukti vieną laiko įrašą, laiko įrašų bloką arba visą laiko įrašų eilutę. Atšauktus laiko įrašus galima redaguoti.

## <a name="time-entry-status"></a>Laiko įrašo būsena

- **Juodraštis**: naujiems laiko įrašams automatiškai priskiriama būsena **Juodraštis**. Galima naikinti tik laiko įrašus, kurių būsena yra **Juodraštis**.
- **Pateiktas**: pateikus laiko įrašą jo būsena atnaujinama į **Pateiktas**. 
- **Patvirtintas**: kai pateiktas laiko įrašas patvirtinamas, jo būsena atnaujinama į **Patvirtintas**. 
- **Grąžintas**: jei laiko įrašas atmetamas, būsena atnaujinama į **Grąžintas** ir įrašą galima koreguoti ir pateikti iš naujo. 

## <a name="view-rejection-comments"></a>Atmetimo komentarų peržiūra
Kai tvirtintojas atmeta laiko įrašą, jis gali įtraukti komentarų, kad išteklius galėtų sužinoti atmetimo priežastį. Norėdami peržiūrėti laiko įrašo atmetimo komentarus, pasirinkite **Atidaryti įrašą**. Atmetimo komentarai bus rodomi laiko planavimo juostoje. Prieš pakartotinai pateikdamas įrašą vartotojas gali atsakyti į atmetimo komentarus.

## <a name="copy-week"></a>Kopijuoti savaitę
Sukūrę kelis laiko įrašus, vartotojai tuo pačiu metu gali sukurti kelis laiko įrašus.

1. Formoje **Laiko įrašai** pasirinkite **Kopijuoti savaitę**, kad masiškai sukurtumėte papildomus laiko įrašus. 
2. Dialogo lango **Kopijavimas** skyriuje **Iš laikotarpio** naudokite laukus **Pradžios data** ir **Pabaigos data**, kad nurodytumėte datos diapazoną, kurio laiko įrašus kopijuoti. 
3. Skyriuje **Laikotarpio pabaiga**, lauke **Pradžios data** nurodykite datą, kuriai norite kurti laiko įrašus. 
4. Pasirinkite **kopijuoti**. Į datą, nurodytą dalyje **Iki laikotarpio**, nukopijuojami atitinkamos savaitės dienos, nurodytos dalyje **Nuo laikotarpio**, laiko įrašai. Pavyzdžiui, praėjusios savaitės pirmadienio laiko įrašas nukopijuojamas į savaitės, nurodytos kaip **Iki laikotarpio**, pirmadienį.

## <a name="import"></a>Importuoti
Tas pats pagrindinis procesas naudojamas importuojant iš rezervavimų, užduočių ir keitimų. Galite nurodyti datos diapazoną, iš kurio importuojami rezervavimai, tada konkrečiai pasirinkti rezervavimus, kuriuos reikia nukopijuoti kaip laiko įrašų juodraščius. 
