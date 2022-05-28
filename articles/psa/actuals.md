---
title: Faktinių duomenų apžvalga
description: Šioje temoje pateikta informacija apie projekto faktinius duomenis.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
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
ms.openlocfilehash: 7ab2638d82eb5ba928d95ca6a524a1566f21e1ba
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587596"
---
# <a name="actuals-overview"></a>Faktinių duomenų apžvalga

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Faktiniai duomenys yra projekto užbaigto darbo kiekis. Projekto faktinius duomenis galima atsekti jų pirminiuose dokumentuose. Šie pirminiai dokumentai apima laiko, išlaidų ir žurnalo įrašus, taip pat sąskaitas faktūras.

![Kaip projekto faktinius duomenis galima atsekti pirminiuose dokumentuose.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Laiko įrašo pateikimas

Naudojant PSA, kai laiko įrašas pateikiamas projektui, susietam su laiko ir medžiagų sutarties eilute, sukuriamos dvi žurnalo eilutės. Viena eilutė skirta išlaidoms, o kita eilutė skirta neįvardintiems pardavimams. Kai laiko įrašas pateikiamas projektui, susietam su nustatytos kainos sutarties eilute, sukuriama žurnalo eilutė tik išlaidoms. 

Numatytųjų kainų įvedimo logika yra žurnalo eilutėje Visos laiko įrašo lauko reikšmės kopijuojamos į žurnalo eilutę. Šiuose laukuose nurodoma operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta iš atitinkamo kainoraščio. 

Dėl laukų, turinčių įtakos numatytosioms kainoms, pvz., **Vaidmuo** ir **Org vienetas**, pagal numatytuosius nustatymus įvedama atitinkama kaina į žurnalo eilutę. Jei į laiko įrašą įtrauksite pasirinktinį lauką ir norite, kad lauko reikšmė būtų dauginama į faktinius duomenis, sukurkite lauką faktinių duomenų objekto lauke ir naudokite lauko susiejimo funkciją, kad nukopijuotumėte lauką iš laiko įrašo į faktinius duomenis.

## <a name="submitting-an-expense-entry"></a>Išlaidų įrašo pateikimas

Naudojant PSA, kai išlaidų įrašas pateikiamas projektui, susietam su laiko ir medžiagų sutarties eilute, sukuriamos dvi žurnalo eilutės. Viena eilutė skirta išlaidoms, o kita eilutė skirta neįvardintiems pardavimams. Kai išlaidų įrašas pateikiamas projektui, susietam su fiksuotos kainos sutarties eilute, sukuriama žurnalo eilutė tik išlaidoms.

Išlaidų numatytųjų kainų įvedimo logika grindžiama išlaidų kategorija, kuri pasirenkama **Išlaidų įvedimas** puslapyje. Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami, kad nustatyti atitinkamą kainoraštį. Tačiau pačioje kainoje suma, kurią vartotojas įvedė, pagal nutylėjimą yra tiesiogiai nukreipiama atitinkamų išlaidų žurnalų kaštų ir pardavimų eilutėse.

Dabartinėje PSA versijoje kategorija paremti numatytųjų vieneto kainų įrašai išlaidų įrašuose negalimi.

## <a name="using-entry-journals-to-record-costs"></a>Įrašų žurnalų naudojimas išlaidoms įrašyti

PSA programoje įrašų žurnalai leidžia įrašyti išlaidas arba pajamas medžiagos, mokesčio, laiko, išlaidų arba mokesčių operacijų klasėse. Žurnale yra antraštė, eilutės ir **Patvirtinti** veiksmas. Štai keletas scenarijų, kai galite naudoti žurnalą:

- Turite įrašyti medžiagos projekto faktines išlaidas ir pardavimą.
- Transakcijų faktinius duomenis turite perkelti iš kitos sistemos į PSA.
- Reikia įrašyti išlaidas, patirtas kitoje sistemoje, pvz., pirkimų arba subrangos išlaidos.

> [!IMPORTANT]
> Faktinių duomenų kūrimas naudojant įrašų žurnalus turėtų būti atliekamas tik vartotojo, kuris supranta, kaip faktiniai duomenys paveikia apskaitą. Taip yra todėl, kad programa nepatvirtina žurnalo eilutės tipo arba susijusių kainų, kurios įvedamos į žurnalo eilutę. Dėl šio žurnalo tipo svarbos atsargiai pasirinkite asmenis, kuriems suteikiama prieiga kurti įrašų žurnalus.     


## <a name="recording-actuals-based-on-project-events"></a>Faktinių duomenų įrašymas pagal projekto įvykius

PSA registruoja projekto metu vykdomas finansines operacijas. Šios operacijos įrašomos kaip **faktiniai duomenys**. Toliau pateikiamose lentelėse rodomi skirtingi faktinių duomenų tipai, kurie sukuriami, atsižvelgiant į tai, ar projektas yra laiko ir medžiagų, ar fiksuotos kainos projektas, yra paruošiamųjų darbų prieš parduodant etape, arba yra vidinis projektas.

**Ištekliai priklauso tam pačiam organizaciniam vienetui kaip ir projekto sutarties vienetas**

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

**Ištekliai priklauso skirtingam organizaciniam vienetui nei projekto sutarties vienetas**

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
