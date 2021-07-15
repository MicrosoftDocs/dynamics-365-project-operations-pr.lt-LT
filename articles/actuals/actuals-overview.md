---
title: Faktiniai duomenys
description: Šioje temoje pateikiama informacija apie tai, kaip dirbti su faktiniais duomenimis programoje „Microsoft Dynamics 365 Project Operations“.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368621"
---
# <a name="actuals"></a>Faktiniai duomenys 

_**Taikoma kam:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniam diegimui – išankstinėms sąskaitoms faktūroms išrašyti_

Faktinių duomenų srityje pateikiama projekto peržiūrėta ir patvirtinta finansinė bei grafiko eiga. Jie kuriami patvirtinus laiką, išlaidas, medžiagos naudojimo įrašus, žurnalų įrašus ir sąskaitas faktūras.

## <a name="journal-lines-and-time-submission"></a>Žurnalo eilutės ir laiko pateikimas

Daugiau informacijos apie laiko įrašą žr. [Laiko įrašo apžvalga](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Laikas ir medžiagos

Kai teikiamas laiko įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistema sukuria dvi žurnalo eilutes – vieną už sąnaudas, o kitą už pardavimą, už kurį neišrašyta sąskaita.

### <a name="fixed-price"></a>Fiksuota kaina

Kai teikiamas laiko įrašas susiejamas su projektu, kuris susietas su fiksuotos kainos sutarties eilute, sistema sukuria vieną žurnalo eilutę už sąnaudas.

### <a name="default-pricing"></a>Numatytoji kainodara

Numatytųjų kainų kūrimo logika yra žurnalo eilutėje. Laiko įrašo lauko reikšmės kopijuojamos į žurnalo eilutę. Šiose reikšmėse nurodoma operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta iš atitinkamo kainoraščio.

Laukai, turintys įtakos numatytajai kainodarai, pvz., **Vaidmuo** ir **Išteklių paskirstymo vienetas**, naudojami norint nustatyti atitinkamą kainą žurnalo eilutėje. Į laiko įrašą galite įtraukti pasirinktinį lauką. Jei norite, kad lauko reikšmė būtų užpildoma faktiniais duomenimis, sukurkite lauką lentelėse **Faktiniai duomenys** ir **Žurnalo eilutė**. Naudokite pasirinktinį kodą ir užpildykite pasirinktą faktinių duomenų laiko įrašą per žurnalo eilutę naudodami operacijos kilmę. Norėdami gauti daugiau informacijos apie operacijų kilmę ir ryšius, žr. [Faktinių duomenų susiejimas su pradiniais įrašais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Žurnalo eilutės ir pagrindinių išlaidų pateikimas

Daugiau informacijos apie išlaidų įrašą žr. [Išlaidų apžvalga](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Laikas ir medžiagos

Kai teikiamas pagrindinių išlaidų įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistema sukuria dvi žurnalo eilutes – vieną už sąnaudas, o kitą už pardavimą, už kurį neišrašyta sąskaita.

### <a name="fixed-price"></a>Fiksuota kaina

Kai pateiktas pagrindinis išlaidų įrašas susiejamas su projektu, susietu su fiksuotos kainos sutarties eilute, sistemoje sukuriama viena žurnalo eilutė išlaidoms.

### <a name="default-pricing"></a>Numatytoji kainodara

Numatytųjų išlaidų kainų įvedimo logika priklauso nuo išlaidų kategorijos. Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami norint nustatyti atitinkamą kainoraštį. Laukai, turintys įtakos numatytajai kainodarai, pvz., **Operacijos kategorija** ir **Vienetas**, naudojami norint nustatyti atitinkamą kainą žurnalo eilutėje. Tačiau tai pasitarnauja tik tada, kai kainodaros būdas kainoraštyje yra **Vieneto kaina**. Jei kainodaros būdas yra **Savikaina** arba **Antkainis prie savikainos**, kaina, įvedama sukūrus išlaidų įrašą, naudojama savikainai, o kaina pardavimo žurnalo eilutėje apskaičiuojama pagal kainodaros būdą. 

Išlaidų įrašo dalyje galite įtraukti pasirinktinį lauką. Jei norite, kad lauko reikšmė būtų užpildoma faktiniais duomenimis, sukurkite lauką lentelėse **Faktiniai duomenys** ir **Žurnalo eilutė**. Naudokite pasirinktinį kodą ir užpildykite pasirinktą faktinių duomenų laiko įrašą per žurnalo eilutę naudodami operacijos kilmę. Norėdami gauti daugiau informacijos apie operacijų kilmę ir ryšius, žr. [Faktinių duomenų susiejimas su pradiniais įrašais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Žurnalo eilutės ir medžiagos naudojimo žurnalo pateikimas

Daugiau informacijos apie išlaidų įrašą žr. [Medžiagos naudojimo žurnalas](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Laikas ir medžiagos

Kai pateiktas medžiagos naudojimo žurnalo įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistemoje sukuriamos dvi žurnalo eilutės – viena išlaidoms, o kita – pardavimui, už kurį neišrašyta sąskaita.

### <a name="fixed-price"></a>Fiksuota kaina

Kai pateiktas medžiagos naudojimo žurnalo įrašas susiejamas su projektu, susietu su fiksuotos kainos sutarties eilute, sistemoje sukuriama viena žurnalo eilutė išlaidoms.

### <a name="default-pricing"></a>Numatytoji kainodara

Medžiagos numatytųjų kainų įvedimo logika pagrįsta produkto ir vieneto deriniu. Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami norint nustatyti atitinkamą kainoraštį. Laukai, turintys įtakos numatytajai kainodarai, pvz., **Produkto ID** ir **Vienetas**, naudojami norint nustatyti atitinkamą kainą žurnalo eilutėje. Tačiau tai pasitarnauja tik katalogo produktų atveju. Įtraukiamųjų produktų atveju, kaina, įvesta sukūrus medžiagos naudojimo žurnalo įrašą, naudojama išlaidoms ir pardavimo kainai žurnalo eilutėse įvesti. 

Išlaidų įrašo dalyje **Medžiagos naudojimo žurnalas** galite įtraukti pasirinktinį lauką. Jei norite, kad lauko reikšmė būtų užpildoma faktiniais duomenimis, sukurkite lauką lentelėse **Faktiniai duomenys** ir **Žurnalo eilutė**. Naudokite pasirinktinį kodą ir užpildykite pasirinktą faktinių duomenų laiko įrašą per žurnalo eilutę naudodami operacijos kilmę. Norėdami gauti daugiau informacijos apie operacijų kilmę ir ryšius, žr. [Faktinių duomenų susiejimas su pradiniais įrašais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Įrašų žurnalų naudojimas išlaidoms įrašyti

Galite naudoti įrašų žurnalus, kad įrašytumėte savikainą ar pajamas medžiagos, mokesčio, laiko, išlaidų ar mokesčių operacijų klasėms. Žurnalus galima naudoti šiems tikslams:

- Operacijų faktinius duomenis perkelkite iš kitos sistemos į „Microsoft Dynamics 365 Project Operations“.
- Įrašyti išlaidas, atsiradusias kitoje sistemoje. Šios išlaidos gali apimti viešuosius pirkimus arba subrangos išlaidas.

> [!IMPORTANT]
> Programa nepatvirtina žurnalo eilutės tipo arba susijusios kainos, įvestos žurnalo eilutėje. Todėl tik vartotojas, gerai žinantis kokį apskaitos poveikį faktiniai duomenys turi projektui, gali naudoti įrašų žurnalus faktiniams duomenis kurti. Dėl šio žurnalo tipo poveikio reikia atidžiai pasirinkti, kas turi prieigą prie įrašų žurnalų kūrimo.

## <a name="record-actuals-based-on-project-events"></a>Faktinių duomenų įrašymas pagal projekto įvykius

„Project Operations“ įrašo projekto metu vykdomas finansines operacijas. Šios operacijos įrašomos kaip faktiniai duomenys. Toliau pateikiamose lentelėse rodomi skirtingi faktinių duomenų tipai, kurie sukuriami, atsižvelgiant į tai, ar projektas yra laiko ir medžiagų, ar fiksuotos kainos projektas, yra paruošiamųjų darbų prieš parduodant etape, arba yra vidinis projektas.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Ištekliai priklauso tam pačiam organizaciniam vienetui kaip ir projekto sutarties vienetas

<table>
<thead>
<tr>
<th rowspan="3">Įvykis</th>
<th colspan="4">Apmokėtinas arba parduotas projektas</th>
<th rowspan="3">Projektas paruošiamųjų darbų etape prieš parduodant</th>
<th rowspan="3">Vidinis projektas</th>
</tr>
<tr>
<th colspan="2">Laikas ir medžiagos</th>
<th colspan="2">Fiksuota kaina</th>
</tr>
<tr>
<th>Faktinės</th>
<th>Operacijos valiuta</th>
<th>Fiksuota kaina</th>
<th>Operacijos valiuta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sukurtas laiko įrašas.</td>
<td colspan="6">Nėra veiksmų faktinių duomenų objekte</td>
</tr>
<tr>
<td>Sukurtas laiko įrašas.</td>
<td colspan="6">Nėra veiksmų faktinių duomenų objekte</td>
</tr>
<tr>
<td rowspan="2">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</td>
<td>Faktinės išlaidos</td>
<td>Sutarties vieneto valiuta</td>
<td rowspan="2">Faktinės išlaidos</td>
<td rowspan="2">Sutarties vieneto valiuta
<td rowspan="2">Faktinės išlaidos</td>
<td rowspan="2">Faktinės išlaidos</td>
</tr>
<tr>
<td>Neišrašyta pardavimo suma - Apmokestinama</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td rowspan="3">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</td>
<td>Faktinės išlaidos</td>
<td>Sutarties vieneto valiuta</td>
<td rowspan="3">Faktinės išlaidos</td>
<td rowspan="3">Sutarties vieneto valiuta</td>
<td rowspan="3">Faktinės išlaidos</td>
<td rowspan="3">Faktinės išlaidos</td>
</tr>
<tr>
<td>Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td>Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td rowspan="2">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</td>
<td>Neišrašyto pardavimo atšaukimas</td>
<td>Projekto sutarties valiuta.</td>
<td rowspan="2">Išrašytas pardavimas už etapą</td>
<td rowspan="2">Projekto sutarties valiuta.</td>
<td rowspan="2">Netaikoma</td>
<td rowspan="2">Netaikoma</td>
</tr>
<tr>
<td>Išrašytas pardavimas</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td rowspan="3">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</td>
<td>Neišrašyto pardavimo atšaukimas</td>
<td>Projekto sutarties valiuta.</td>
<td rowspan="3">Netaikoma</td>
<td rowspan="3">Netaikoma</td>
<td rowspan="3">Netaikoma</td>
<td rowspan="3">Netaikoma</td>
</tr>
<tr>
<td>Išrašytas pardavimas - Apmokestinamas už naują kiekį</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td>Išrašytas pardavimas - Neapmokestinamas už skirtumą</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td rowspan="2">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</td>
<td>Neišrašytas pardavimas - Atšaukimas</td>
<td>Projekto sutarties valiuta.</td>
<td rowspan="5">
<ul>
<li>Išrašyto pardavimo atšaukimas už etapą</li>
<li>Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></li>
</ul>
</td>
<td rowspan="5">Projekto sutarties valiuta.</td>
<td rowspan="5">Netaikoma</td>
<td rowspan="5">Netaikoma</td>
</tr>
<tr>
<td>Išrašytas pardavimas</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td rowspan="3">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</td>
<td>Neišrašytas pardavimas - Atšaukimas</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td>Išrašytas pardavimas už naują kiekį</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td>Neišrašytas pardavimas - apmokestinamas už skirtumą</td>
<td>Projekto sutarties valiuta.</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Ištekliai priklauso skirtingam organizaciniam vienetui nei projekto sutarties vienetas

<table>
<thead>
<tr>
<th rowspan="3">Įvykis</th>
<th colspan="4">Apmokėtinas arba parduotas projektas</th>
<th rowspan="3">Projektas paruošiamųjų darbų etape prieš parduodant</th>
<th rowspan="3">Vidinis projektas</th>
</tr>
<tr>
<th colspan="2">Laikas ir medžiagos</th>
<th colspan="2">Fiksuota kaina</th>
</tr>
<tr>
<th>Faktinės</th>
<th>Operacijos valiuta</th>
<th>Fiksuota kaina</th>
<th>Operacijos valiuta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Sukurtas laiko įrašas.</td>
<td colspan="6">Nėra veiksmų faktinių duomenų objekte</td>
</tr>
<tr>
<td>Sukurtas laiko įrašas.</td>
<td colspan="6">Nėra veiksmų faktinių duomenų objekte</td>
</tr>
<tr>
<td rowspan="4">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</td>
<td>Faktinės išlaidos</td>
<td>Sutarties vieneto valiuta</td>
<td rowspan="4">Faktinės išlaidos</td>
<td rowspan="4">Sutarties vieneto valiuta</td>
<td rowspan="4">Faktinės išlaidos</td>
<td rowspan="4">Faktinės išlaidos</td>
</tr>
<tr>
<td>Neišrašyta pardavimo suma - Apmokestinama</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td>Išteklių paskirstymo vieneto savikaina</td>
<td>Išteklių vieneto valiuta</td>
</tr>
<tr>
<td>Tarp organizacijų vykdomas pardavimas</td>
<td>Sutarties vieneto valiuta</td>
</tr>
<tr>
<td rowspan="5">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</td>
<td>Faktinės išlaidos</td>
<td>Sutarties vieneto valiuta</td>
<td rowspan="5">Faktinės išlaidos</td>
<td rowspan="5">Sutarties vieneto valiuta</td>
<td rowspan="5">Faktinės išlaidos</td>
<td rowspan="5">Faktinės išlaidos</td>
</tr>
<tr>
<td>Išteklių paskirstymo vieneto savikaina</td>
<td>Išteklių vieneto valiuta</td>
</tr>
<tr>
<td>Tarp organizacijų vykdomas pardavimas</td>
<td>Sutarties vieneto valiuta</td>
</tr>
<tr>
<td>Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td>Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td rowspan="2">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</td>
<td>Neišrašyto pardavimo atšaukimas</td>
<td>Projekto sutarties valiuta.</td>
<td rowspan="2">Išrašytas pardavimas už etapą</td>
<td rowspan="2">Projekto sutarties valiuta.</td>
<td rowspan="2">Netaikoma</td>
<td rowspan="2">Netaikoma</td>
</tr>
<tr>
<td>Išrašytas pardavimas</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td rowspan="3">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</td>
<td>Neišrašyto pardavimo atšaukimas</td>
<td>Projekto sutarties valiuta.</td>
<td rowspan="3">Netaikoma</td>
<td rowspan="3">Netaikoma</td>
<td rowspan="3">Netaikoma</td>
<td rowspan="3">Netaikoma</td>
</tr>
<tr>
<td>Išrašytas pardavimas - Apmokestinamas už naują kiekį</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td>Išrašytas pardavimas - Neapmokestinamas už skirtumą</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td rowspan="2">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</td>
<td>Neišrašytas pardavimas - Atšaukimas</td>
<td>Projekto sutarties valiuta.</td>
<td rowspan="5">
<ul>
<li>Išrašyto pardavimo atšaukimas už etapą</li>
<li>Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></li>
</ul>
</td>
<td rowspan="5">Projekto sutarties valiuta.</td>
<td rowspan="5">Netaikoma</td>
<td rowspan="5">Netaikoma</td>
</tr>
<tr>
<td>Išrašytas pardavimas</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td rowspan="3">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</td>
<td>Neišrašytas pardavimas - Atšaukimas</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td>Išrašytas pardavimas už naują kiekį</td>
<td>Projekto sutarties valiuta.</td>
</tr>
<tr>
<td>Neišrašytas pardavimas - apmokestinamas už skirtumą</td>
<td>Projekto sutarties valiuta.</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
