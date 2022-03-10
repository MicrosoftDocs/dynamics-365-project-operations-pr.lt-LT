---
title: Projektu pagrįstų pasiūlymo eilučių sąskaitų faktūrų grafikai
description: Šioje temoje pateikta informacija apie sąskaitų faktūrų grafikų ir pasiūlymo eilučių etapų kūrimą.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0d07596b299d71b229487faf80a09e368059575ea37095d2c82d35561d009c96
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988616"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Projektu pagrįstų pasiūlymo eilučių sąskaitų faktūrų grafikai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projektu pagrįsta pasiūlymo eilutė suteikia galimybę išreikšti sąskaitos faktūros grafiką. Tai nebūtina pasiūlymo etape, nes programa nepalaiko projekto sąskaitos faktūros išrašymo, kai jis susiejamas su pasiūlymo eilute. Sąskaitų faktūrų išrašymas galimas tik gavus pasiūlymą. Vienintelis pasrovinis sąskaitų faktūrų grafiko kūrimo poveikis pasiūlymo etape yra tai, kad šis sąskaitų faktūrų grafikas kopijuojamas į projektu pagrįstą sutarties eilutę. Jei nesukursite sąskaitų faktūrų grafiko pasiūlymo etape, galėsite tai padaryti projektu pagrįstoje sutarties eilutėje.

Apskritai sąskaitų faktūrų grafikų paskirtis – leisti automatiškai kurti projektu pagrįstos sutarties eilutės juodraštines sąskaitas faktūras. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Projektu pagrįstos pasiūlymo eilutės laiko ir medžiagos sąskaitų faktūrų grafiko kūrimas

Kai projektu pagrįstos pasiūlymo eilutės atsiskaitymo būdas yra laikas ir medžiaga, sistema sugeneruoja data pagrįstą sąskaitos faktūros grafiką. Norėdami automatiškai sugeneruoti data pagrįstą sąskaitos faktūros grafiką, atlikite toliau nurodytus veiksmus.

1. Eikite į **Parametrai** > **Sąskaitos faktūros dažniai** ir nustatykite sąskaitos faktūros dažnumą.
2. Puslapyje **Pasiūlymai** atidarykite projekto pasiūlymą, o skirtuke **Suvestinė** nustatykite pristatymo datą.
3. Atidarykite laiko ir medžiagos pasiūlymo eilutę, kurią turite sukurti pagal data pagrįstą sąskaitos faktūros grafiką. 
4. Skirtuke **Sąskaitos faktūros grafikas** pažymėkite reikšmes laukuose **Atsiskaitymo pradžia** ir **Sąskaitos faktūros dažnumas**. 
5. Papildomame tinklelyje pasirinkite **Generuoti sąskaitų faktūrų grafiką**.
6. Programa sukuria sąskaitos faktūros grafiką su laukais **Sąskaitos faktūros vykdymo data**, **Operacijos galutinė data** ir **Vykdymo būsena** šiuo būdu:

    - **Sąskaitos faktūros vykdymo data** nustatoma į datą, kurią diktuoja sąskaitos faktūros dažnumas.
    - **Operacijos galutinė data** nustatoma į tą dieną prieš **Sąskaitos faktūros vykdymo datą**.
    - **Vykdymo būsena** automatiškai nustatoma į **Nevykdoma**. Kai automatinio sąskaitos faktūros kūrimo užduotis paleidžiama tam tikrai sąskaitos faktūros vykdymo datai, ji atnaujins šį lauką į **Vykdymas sėkmingas** arba **Vykdymas nepavyko**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Projektu pagrįstos pasiūlymo eilutės fiksuotos kainos sąskaitų faktūrų grafiko kūrimas

Kai projektu pagrįstoje pasiūlymo eilutėje yra **Fiksuotas** atsiskaitymo būdas, sistema sukuria etapu pagrįstą sąskaitų faktūrų grafiką. Atlikite šiuos veiksmus, kad automatiškai generuotumėte šį grafiką, skirtą etapų, kurie vienodai paskirstyti kalendoriniam laikotarpiui, fiksuotam rinkiniui.

1. Eikite į **Parametrai** > **Sąskaitos faktūros dažniai** ir nustatykite sąskaitos faktūros dažnumą.
2. Puslapyje **Pasiūlymai** atidarykite projekto pasiūlymą, o skirtuke **Suvestinė** nustatykite pristatymo datą.
3. Atidarykite fiksuotos kainos pasiūlymo eilutę, kuriai reikia sukurti etapo grafiką. 
4. Skirtuke **Sąskaitos faktūros grafikas** pažymėkite reikšmes laukuose **Atsiskaitymo pradžia** ir **Sąskaitos faktūros dažnumas**. 
5. Papildomame tinklelyje pasirinkite **Periodiški etapai**.
6. Programa sukuria sąskaitos faktūros grafiką su etapo pavadinimu, data ir suma.

    - Etapo pavadinimas nustatomas į datą, kurią diktuoja sąskaitos faktūros dažnumas.
    - Etapo data nustatomas į datą, kurią diktuoja sąskaitos faktūros dažnumas.
    - Etapų suma apskaičiuojama dalijant projektu pagrįstos pasiūlymo eilutės pasiūlymo sumą iš etapų skaičių, kuris priklauso nuo dažnumo ir atsiskaitymo pradžios ir pageidaujamų pristatymo datų.
    - Jei pasiūlymo eilutėje taip pat yra apskaičiuota mokesčių suma, ši reikšmė po lygiai padalinama kiekvienam etapui, kai generuojami periodiniai etapai.

### <a name="manually-create-milestones"></a>Etapų kūrimas rankiniu būdu

Fiksuotos kainos etapai taip pat gali būti generuojamos rankiniu būdu, kai jie nėra periodiškai padalijami. Norėdami sukurti etapą rankiniu būdu:

Atidarykite fiksuotos kainos pasiūlymo eilutę, kur norite sukurti etapą. Papildomo tinklelio skirtuke **Sąskaitų faktūrų grafikas** pasirinkite **+ Kurti naują pasiūlymo eilutės etapą** ir įveskite reikiamą informaciją pagal tolesnę lentelę.

| **Laukas** | **Vieta** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Etapo pavadinimas | Spartusis kūrimas | Etapo pavadinimas. | Tai platinama į projekto sutarties eilutės etapą ir į sąskaitą faktūrą |
| Projekto užduotis | Spartusis kūrimas | Jei etapas yra susietas su projekto užduotimi, galite naudoti šią nuorodą ir įtraukti pasirinktinę logiką, kuri nustatys etapo būseną pagal užduoties būseną. | Programa neturi jokio tolesnio šios nuorodos poveikio užduočiai. |
| Etapo data | Spartusis kūrimas | Nustatykite datą, kada automatinio sąskaitos faktūros kūrimo procesas turėtų ieškoti šio etapo būsenos, kad būtų galima ją išrašyti. | Tai platinama į projekto sutarties eilutės etapą ir į sąskaitą faktūrą. |
| Sąskaitos faktūros būsena | Spartusis kūrimas | Sukūrus etapą, ši būsena visada nustatoma į **Neparuošta išrašyti sąskaitos faktūros**. | Tai platinama į projekto sutarties eilutės etapą ir į sąskaitą faktūrą. |
| Eilutės suma | Spartusis kūrimas | Etapo, kuriam bus išrašyta sąskaita faktūra, suma arba reikšmė. | Tai platinama į projekto sutarties eilutės etapą ir į sąskaitą faktūrą. |
| Mokesčiai | Spartusis kūrimas | Mokesčių suma, kuri bus taikoma etapui. | Tai platinama į projekto sutarties eilutės etapą ir į sąskaitą faktūrą. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]