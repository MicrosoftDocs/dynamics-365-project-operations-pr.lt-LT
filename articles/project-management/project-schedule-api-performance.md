---
title: Projekto grafiko API efektyvumas
description: Šiame straipsnyje pateikiama informacija apie projekto grafiko API efektyvumo sąlyginius etalonus ir nustatoma optimalaus naudojimo geriausia praktika.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911192"
---
# <a name="project-schedule-api-performance"></a>Projekto grafiko API efektyvumas

_**Taikoma:** „Project Operations“ ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, „Lite“ visuotinis diegimas – sąskaitų faktūrų išrašymo sandoris, „Project for the web“_

Šiame straipsnyje pateikiama informacija apie projekto grafiko programų kūrimo sąsajas (API) efektyvumo sąlyginius etalonus ir nustatoma optimalaus naudojimo geriausia praktika.

## <a name="project-scheduling-service"></a>Projektų planavimo tarnyba
Projektų planavimo tarnyba yra kelių nuomotojų aptarnavimas, vykdomas „Microsoft Azure”. Ji skirta sąveikai pagerinti, teikiant vartotojams greitas ir sklandžias darbo su projektais funkcijas. Šis patobulinimas pasiekiamas priimant keitimo užklausas, jas apdorojant ir nedelsiant pateikiant rezultatą. Aptarnavimas asinchroniškai išlieka „Dataverse” ir neblokuoja vartotojų leisdamas atlikti kitas operacijas.

Projekto grafiko API, vykdydamos užklausas, plačiau aprašytas tolesniuose šio straipsnio skyriuose, priklauso nuo projektų planavimo paslaugų.

Projekto grafiko API skirtos dirbti su toliau nurodytais darbo paskirstymo struktūros (WBS) objektais.

  - Project
  - Projekto užduotis
  - Projekto užduoties priklausomybė
  - Projekto komandos narys
  - Išteklių priskyrimas
  
Palaikomi ir parengti naudoti, ir pasirinktiniai laukai. Jei nenurodyta kitaip, palaikomos visos įprastos operacijos, pvz., kūrimas, naujinimas ir naikinimas. Daugiau informacijos žr. [Projekto grafiko API naudojimas operacijoms ir planavimo objektams atlikti](schedule-api-preview.md).

Darbo vieneto šablonas buvo įtrauktas kaip projekto grafiko API dalis. Šis šablonas yra žinomas kaip OperationSet, jį galima naudoti, kai atliekant vieną operaciją, reikia apdoroti kelias užklausas.

Tolesnėje iliustracijoje pavaizduotas srautas, pateikiamas partneriui, naudojant šią funkciją.

![„Dataverse” ir projektų planavimo tarnybos srautas.](./media/dataverse-project-scheduling-service-flow.png)

**1 veiksmas**. Programoje „Dataverse” klientas atlieka atviro duomenų protokolo (OData) galinio punkto API iškvietimą, kad sukurtų OperationSet.

**2 veiksmas**. Sukūrus OperationSet, pateikiama reikšmė **OperationSetId**.

**3 veiksmas**. Klientas naudoja reikšmę **OperationSetId**, kad pateiktų kitą projekto grafiko API užklausą. Rezultatas yra planavimo objekto kūrimo, naujinimo ar naikinimo užklausa. Pateikus šią užklausą, atliekamas metaduomenų tikrinimas. Jei patikrinti nepavyksta, užklausa nutraukiama ir pateikiama klaida.

**4a–4c veiksmai**. Šie veiksmai atitinka priėmimo (ACCEPT) etapą. Klientas iškviečia API **ExecuteOperationSetV1**, kuri visus pakeitimus viename pakete siunčia į projektų planavimo tarnybą. Projektų planavimo tarnyba vykdo savo pakete esančių užklausų tikrinimus. Bet kokios tikrinimo klaidos anuliuoja paketą ir skambintojui pateikia išimtį. Jei projektų planavimo tarnyba šį paketą sėkmingai priima, OperationSet būsena atnaujinama, siekiant parodyti, kad projektų planavimo tarnyba vykdo OperationSet.

**5 veiksmas**. Šis veiksmas atitinka išlaikymo (PERSIST) etapą. Operacijos metu projektų planavimo tarnyba asinchroniškai įrašo paketą į „Dataverse”. Jei įrašymo operacija sėkminga, OperationSet pažymima kaip **Atlikta**. Bet kokios klaidos atšaukia operaciją ir paketą, o OperationSet pažymima kaip **Nepavyko**.

## <a name="performance-methodology"></a>Efektyvumo metodologija
Vykdymo laikas apibrėžiamas kaip laikas nuo skambučio į **ExecuteOperationSetV1** API iki projekto planavimo tarnybos įrašymo į  „Dataverse” pabaigos. Visos operacijos vykdomos kombinuotus 2200 kartų ir pranešama apie P99 vykdymo laiko matavimus. Matuojamos vieno įrašo ir masinės operacijos.

Vieno įrašo operacijos OperationSet yra viena užklausa. Atliekant masines operacijas, joje yra 20, 50 arba 100 užklausų. Apie kiekvienos masinės operacijos dydį pranešama atskirai.

Šiaurės Amerikoje šios operacijos vykdomos UR 15 „Project Operations Lite” diegime.

## <a name="results"></a>Rezultatai
### <a name="create-operations"></a>Operacijų kūrimas
#### <a name="single-record-create-operations"></a>Vieno įrašo kūrimo operacijos
Šioje lentelėje parodytas vieno įrašo kūrimo vykdymo laikas. Laikas nurodomas sekundėmis.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Įrašo&nbsp;&nbsp;&nbsp;tipas</th>
    <th class="tg-0lax" colspan="2">Laikas</th>
  </tr>
  <tr>
    <th class="tg-0lax">Būtini laukai</th>
    <th class="tg-0lax">Visi palaikomi laukai</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Užduotis</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Priskyrimas</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Komandos narys</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Priklausomybė</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Masinio kūrimo operacijos
Šioje lentelėje parodytas masinio įrašų kūrimo vykdymo laikas. „Microsoft” išmatavo 20, 50 ir 100 įrašų kūrimo vykdymo laiką per vieną OperationSet. Laikas nurodomas sekundėmis.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Įrašo&nbsp;&nbsp;&nbsp;tipas</th>
    <th class="tg-0lax" colspan="6">Laikas</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 įrašų</th>
    <th class="tg-0lax" colspan="2">50 įrašų</th>
    <th class="tg-0lax" colspan="2">100 įrašų</th>
  </tr>
  <tr>
    <th class="tg-0lax">Būtini laukai</th>
    <th class="tg-0lax">Visi palaikomi laukai</th>
    <th class="tg-0lax">Būtini laukai</th>
    <th class="tg-0lax">Visi palaikomi laukai</th>
    <th class="tg-0lax">Būtini laukai</th>
    <th class="tg-0lax">Visi palaikomi laukai</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Užduotis</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Priskyrimas</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Priklausomybė</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Į šią lentelę neįtrauktos masinio kūrimo operacijos objektuose **Projektas** ir **Komandos narys**, nes šių operacijų vykdymo laikas yra panašus į vykdymo laiką, kai vieno įrašo kūrimo API iškviečiama keletą kartų. Šios API vykdomos iš karto „Dataverse”.

Tolesnėje iliustracijoje pavaizduota objektų **Užduotis**, **Priskyrimas** ir **Priklausomybė** vykdymo laiko diagrama, kai sukuriama 20, 50 ir 100 įrašų ir naudojami visi palaikomi laukai.

![Įrašo sukūrimo vykdymo laiko diagrama.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Naujinimo operacijos
#### <a name="single-record-update-operations"></a>Vieno įrašo naujinimo operacijos
Šioje lentelėje parodytas vieno įrašo atnaujinimo vykdymo laikas. Laikas nurodomas sekundėmis.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Įrašo&nbsp;&nbsp;&nbsp;tipas</th>
    <th class="tg-0lax" colspan="2">Laikas</th>
  </tr>
  <tr>
    <th class="tg-0lax">Būtini laukai </th>
    <th class="tg-0lax">Visi palaikomi laukai</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Užduotis</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Komandos narys</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Naujinimo operacijos nepalaikomos objektuose **Išteklių priskyrimai** ir **Projekto užduoties priklausomybė**.

#### <a name="bulk-update-operations"></a>Masinio naujinimo operacijos
Šioje lentelėje parodytas masinio įrašų naujinimo vykdymo laikas. „Microsoft” išmatavo 20, 50 ir 100 įrašų naujinimo vykdymo laiką per vieną OperationSet. Laikas nurodomas sekundėmis.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Įrašo&nbsp;&nbsp;&nbsp;tipas</th>
    <th class="tg-0lax" colspan="6">Laikas</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 įrašų</th>
    <th class="tg-0lax" colspan="2">50 įrašų</th>
    <th class="tg-0lax" colspan="2">100 įrašų</th>
  </tr>
  <tr>
    <th class="tg-0lax">Būtini laukai</th>
    <th class="tg-0lax">Visi palaikomi laukai</th>
    <th class="tg-0lax">Būtini laukai</th>
    <th class="tg-0lax">Visi palaikomi laukai</th>
    <th class="tg-0lax">Būtini laukai</th>
    <th class="tg-0lax">Visi palaikomi laukai</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Užduotis</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Komandos narys</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Naujinimo operacijos nepalaikomos objektuose **Išteklių priskyrimai** ir **Projekto užduoties priklausomybė**.

Tolesnėje iliustracijoje pavaizduota objektų „Užduotis”, „Komandos narys” ir „Priklausomybė” vykdymo laiko diagrama, kai naujinama 20, 50 ir 100 įrašų ir naudojami visi palaikomi laukai.

![Įrašo naujinimo vykdymo laiko diagrama.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Naikinimo operacijos
#### <a name="single-record-delete-operations"></a>Vieno įrašo naikinimo operacijos
Šioje lentelėje parodytas vieno įrašo naikinimo vykdymo laikas. Laikas nurodomas sekundėmis.

| Įrašo tipas | Laikas  |
|-------------|-------|
| Užduotis        | 20.12 |
| Priskyrimas  | 10.86 |
| Komandos narys | 12.52 |
| Priklausomybė  | 20.89 |

> [!NOTE]
> Naikinimo operacijos objekte **Projektas** nepalaikomos.

#### <a name="bulk-delete-operations"></a>Masinio naikinimo operacijos
Šioje lentelėje parodytas masinio įrašų naikinimo vykdymo laikas. „Microsoft” išmatavo 20, 50 ir 100 įrašų naikinimo vykdymo laiką per vieną OperationSet. Laikas nurodomas sekundėmis.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Įrašo&nbsp;&nbsp;&nbsp;tipas</th>
    <th class="tg-0lax" colspan="3">Laikas</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 įrašų</th>
    <th class="tg-0lax">50 įrašų</th>
    <th class="tg-0lax">100 įrašų</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Užduotis</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Priskyrimas</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Komandos narys</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Priklausomybė</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Naikinimo operacijos objekte **Projektas** nepalaikomos.

Tolesnėje iliustracijoje pavaizduota objektų **Užduotis**, **Priskyrimas**, **Komandos narys** ir **Priklausomybė** vykdymo laiko diagrama, kai naikinama 20, 50 ir 100 įrašų ir naudojami visi palaikomi laukai.

![Įrašo naikinimo vykdymo laiko diagrama.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Pastabos
Atliekant kiekvieną įrašo operaciją, API **ExecuteOperationSet** užtrunka maždaug 800 milisekundžių, kad nusiųstų užklausą projektų planavimo tarnybai. Tada projektų planavimo tarnyba užtrunka maždaug penkias sekundes, kad apdorotų apkrovą ir iškviestų „Dataverse”. Likusį vykdymo laiką vykdoma verslo logika ir duomenys įrašomi į duomenų bazę „Dataverse”.

Kuriant, naujinant arba naikinant 100 įrašų, API **ExecuteOperationSet** užtrunka maždaug 3 sekundes, kad nusiųstų užklausą projektų planavimo tarnybai. Tada projektų planavimo tarnyba užtrunka maždaug penkias sekundes, kad apdorotų užklausas ir iškviestų „Dataverse”. Už visus OperationSet esančius įrašus masinės operacijos turi vieną kartą sumokėti **projektų planavimo tarnybos mokestį**. Todėl masinių operacijų vidutinis vykdymo laikas yra gerokai mažesnis nei vieno įrašo operacijos vykdymo laikas.

## <a name="scenarios"></a>Scenarijai
Tolesnėje lentelėje rodomas vykdymo laikas, kai projekto grafiko API naudojamos konkretiems scenarijams vykdyti. Laikas nurodomas sekundėmis.

| Scenarijus                                                                   | Laikas  |
|----------------------------------------------------------------------------|-------|
| Sukurkite projektą, kuriame yra 40 užduočių.                                      | 36.01 |
| Sukurkite projektą, kuriame yra 40 užduočių ir 20 priklausomybių.                  | 38.11 |
| Sukurkite projektą, kuriame yra 40 užduočių ir 30 priskyrimų.                   | 60.17 |
| Sukurkite projektą, kuriame yra 40 užduočių, 20 priklausomybių ir 30 priskyrimų. | 60.27 |

## <a name="best-practices"></a>Geriausia praktika
Pagal ankstesnius scenarijaus rezultatus API yra efektyvesnė toliau nurodytomis sąlygomis.

  - Grupuokite kuo daugiau operacijų. Vidutinė masinių operacijų vykdymo trukmė yra geresnė nei vidutinė vieno įrašo operacijų vykdymo trukmė. Kuo mažesnis naudojamų OperationSets skaičius, tuo trumpesnis bus vidutinis vykdymo laikas.
  - Nustatykite tik minimalius atributus, kurių reikia scenarijui įvykdyti. Atidžiai rinkitės nebūtinų laukų, kurie bus įtraukti į OperationSet užklausą, tipus. Laukai, kuriuose yra išorinių raktų arba apibendrinimo laukų, turės neigiamos įtakos efektyvumui.
