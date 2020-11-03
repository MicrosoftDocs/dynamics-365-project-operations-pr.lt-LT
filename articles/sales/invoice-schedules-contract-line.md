---
title: Sąskaitos faktūros grafikų kūrimas projektais pagrįstoje sutarties eilutėje
description: Šioje temoje pateikta informacija apie sąskaitų faktūrų grafikų ir sutarties eilučių etapų kūrimą.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 23378b51c8324a60918ad494e7f659dbbc94e2a8
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081068"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Sąskaitos faktūros grafikų kūrimas projektais pagrįstoje sutarties eilutėje 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Sąskaitos faktūros grafikus galite kurti projektais pagrįstoje sutarties eilutėje. Sąskaita faktūras išrašyti leidžiama tik tada, kai laimėta sutartis ir kuriate projekto sutartį. Sąskaitos faktūros grafikas leidžia automatiškai sukurti projektais pagrįstos sutarties eilutės sąskaitų faktūrų juodraščius. Tačiau, jei galite tik neautomatiškai kurti sąskaitas faktūras, galite praleisti sutarties eilučių sąskaitų faktūrų grafikų kūrimą.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Sutarties eilutės laiko ir medžiagos sąskaitų faktūrų grafiko kūrimas

Kai projektu pagrįstos sutarties eilutės atsiskaitymo būdas yra laikas ir medžiaga, galite kurti data pagrįstą sąskaitos faktūros grafiką. Norėdami automatiškai sugeneruoti data pagrįstą sąskaitos faktūros grafiką, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Parametrai** > **Sąskaitos faktūros dažniai** ir nustatykite sąskaitos faktūros dažnumą.
2. Pereikite prie projekto sutarties įrašo skirtuke **Suvestinė** , lauke **Pageidaujama pristatymo data** pasirinkite datą.
3. Atidarykite **laiko ir medžiagos** pasiūlymo eilutę, kurią turite sukurti pagal data pagrįstą sąskaitos faktūros grafiką. 
4. Skirtuke **Sąskaitos faktūros** grafikas pasirinkite reikšmes atsiskaitymo pradžios datą ir sąskaitos faktūros dažnumą.
5. Papildomame tinklelyje pasirinkite **Generuoti sąskaitų faktūrų grafiką**. Sąskaitos faktūros grafikas sugeneruojamas su laukais **Sąskaitos faktūros vykdymo data** , **Operacijos galutinė data** ir **Vykdymo būsena** , kaip nurodyta toliau.

    - **Sąskaitos faktūros vykdymo data** : tai data, kurią diktuoja sąskaitos faktūros dažnumas.
    - **Operacijos galutinė data** : diena prieš sąskaitos faktūros vykdymo datą.
    - **Vykdymo būsena** : automatiškai nustatoma į **Nevykdoma**. Kai automatinio sąskaitos faktūros kūrimo užduotis paleidžiama tam tikrai sąskaitos faktūros vykdymo datai, ji atnaujins šį lauką į **Vykdymas sėkmingas** arba **Vykdymas nepavyko**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Sutarties eilutės fiksuotos kainos sąskaitų faktūrų grafiko kūrimas

Kai sutarties eilutėje yra fiksuotas atsiskaitymo būdas, galite kurti etapu pagrįstą sąskaitų faktūrų grafiką. 

> [!NOTE]
> Negalima kurti sutarties eilutės etapų, jei su sutarties eilute nebus susietas joks projektas.

Atlikite šiuos veiksmus, kad automatiškai generuotumėte etapais pagrįstą sąskaitų faktūrų grafiką, skirtą etapų, kurie vienodai paskirstyti kalendoriniam laikotarpiui, fiksuotam rinkiniui.

1. Pasirinkite **Parametrai** > **Sąskaitos faktūros dažniai** ir nustatykite sąskaitos faktūros dažnumą.
2. Pereikite prie projekto sutarties įrašo skirtuke **Suvestinė** , lauke **Pageidaujama pristatymo data** pasirinkite datą.
3. Atidarykite **fiksuotos kainos** pasiūlymo eilutę, kuriai reikia sukurti etapo grafiką. Skirtuke **Atsiskaitymo etapai** pasirinkite reikšmes atsiskaitymo pradžios datą ir sąskaitos faktūros dažnumą. 
4. Papildomame tinklelyje pasirinkite **Periodiški etapai**. Sąskaitų faktūrų grafikas generuojamas naudojant laukus **Etapo pavadinimas** , **Etapo data** ir **Etapo suma** , kaip nurodyta toliau.

    - **Etapo pavadinimas** : tai data, kurią diktuoja sąskaitos faktūros dažnumas.
    - **Etapo data** : tai data, kurią diktuoja sąskaitos faktūros dažnumas.
    - **Etapų suma** : ši suma apskaičiuojama dalijant sutarties eilutės sutarties sumą iš etapų skaičių, kuris priklauso nuo dažnumo ir atsiskaitymo pradžios ir pageidaujamų pristatymo datų.

    Jei sutarties eilutė turi reikšmę lauke **Apskaičiuota mokesčių suma** , šis laukas taip pat paskirstomas kiekvienam etapui vienodai, kai generuojami periodiniai etapai.

Atsiskaitymo etapai turi būti lygūs sutarties eilutės sutartyje nustatytai vertei. Jei taip nėra, puslapyje **Sutarties eilutė** įvyks klaida. Klaidą galite ištaisyti patvirtindami, kad atsiskaitymo etapų suma atitinka sutartyje nustatytą eilutės reikšmę, kurdami, redaguodami arba naikindami etapus. Atlikę pakeitimus atnaujinkite puslapį, kad būtų pašalinta klaida.

### <a name="manually-create-milestones"></a>Etapų kūrimas rankiniu būdu

Fiksuotos kainos etapai gali būti generuojamos neautomatiškai, kai jie nėra periodiškai padalijami. Atlikite šiuos veiksmus, kad neautomatiškai sukurtumėte etapą.

1. Atidarykite fiksuotos kainos sutarties eilutę, kuriai kuriate etapą, ir papildomame tinklelyje esančiame skirtuke **Sąskaitų faktūrų grafikas** pasirinkite **+ Kurti naują sutarties eilutės etapą**. 
2. Puslapyje **Etapo kūrimas** įveskite reikiamą informaciją pagal toliau pateiktą lentelę.

| Laukas | Vieta | Atitiktis, tikslas ir gairės | Tolesnis poveikis |
| --- | --- | --- | --- |
| Etapo pavadinimas | Spartusis kūrimas | Etapo pavadinimo teksto laukas. | Tai perkeliama į projekto sutarties eilutės etapą ir į sąskaitą faktūrą. |
| Projekto užduotis | Spartusis kūrimas | Jei etapas yra susietas su projekto užduotimi, galite naudoti šią nuorodą ir įtraukti pasirinktinę logiką, kuri nustatys etapo būseną pagal užduoties būseną. | Programa neturi jokio tolesnio šios nuorodos poveikio užduočiai. |
| Etapo data | Spartusis kūrimas | Nustatykite datą, kada automatinio sąskaitos faktūros kūrimo procesas turėtų ieškoti šio etapo būsenos, kad būtų galima ją išrašyti. | Tai perkeliama į projekto sutarties eilutės etapą ir į sąskaitą faktūrą. |
| Sąskaitos faktūros būsena | Spartusis kūrimas | Sukūrus etapą, ši būsena visada nustatoma į **Neparengta išrašyti sąskaitos faktūros** arba **Nepradėta**. | Tai perkeliama į projekto sutarties eilutės etapą ir į sąskaitą faktūrą. |
| Eilutės suma | Spartusis kūrimas | Etapo, kuriam bus išrašyta sąskaita faktūra, suma arba reikšmė. | Tai perkeliama į projekto sutarties eilutės etapą ir į sąskaitą faktūrą. |
| Mokesčiai | Spartusis kūrimas | Etapui taikoma mokesčių suma. | Tai perkeliama į projekto sutarties eilutės etapą ir į sąskaitą faktūrą. |

3. Pasirinkite **Įrašyti ir uždaryti**.
