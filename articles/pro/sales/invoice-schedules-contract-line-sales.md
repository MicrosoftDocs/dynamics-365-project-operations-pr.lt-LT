---
title: Sąskaitos faktūros grafikų kūrimas projektu pagrįstoje sutarties eilutėje – „Lite“ versija
description: Šioje temoje pateikta informacija apie sąskaitų faktūrų grafikų ir etapų kūrimą.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 728a35b2b69fb63a2b20f218c250365c5068370f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180337"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Sąskaitos faktūros grafikų kūrimas projektu pagrįstoje sutarties eilutėje – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projektu pagrįstoje sutarties eilutėje galite pridėti sąskaitos faktūros grafiką. Sąskaitas faktūras išrašyti galima tik tada, kai laimėtas projekto sutarties kūrimo konkursas. Sąskaitų faktūrų grafikas leidžia automatiškai kurti projektu pagrįstos sutarties eilutės sąskaitų faktūrų juodraščius. Jei ketinate visada sąskaitas faktūras išrašyti neautomatiniu būdu, galite praleisti sąskaitų faktūrų grafikų kūrimo projektu pagrįstoje sutarties eilutėje ar įprastoje sutarties eilutėje etapą.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Laiko ir medžiagų sąskaitų faktūrų grafiko kūrimas projektu pagrįstai sutarties eilutei

Kai projektu pagrįstos sutarties eilutės atsiskaitymo būdas yra laikas ir medžiaga, galite kurti data pagrįstą sąskaitos faktūros grafiką. Norėdami automatiškai sugeneruoti data pagrįstą sąskaitos faktūros grafiką, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Parametrai** > **Sąskaitų faktūrų dažnis**, kad nustatytumėte sąskaitų faktūrų dažnį.
2. Atidarykite projekto sutartį ir skirtuke **Suvestinė** nustatykite pageidaujamą pristatymo datą.
3. Atidarykite laiko ir medžiagų sutarties eilutę, kuriai norite sukurti data pagrįstą sąskaitų faktūrų grafiką. 
4. Skirtuke **Sąskaitų faktūrų grafikas** pažymėkite sąskaitų išrašymo pradžios datą ir sąskaitų faktūrų dažnį. 
5. Papildomame tinklelyje pasirinkite **Generuoti sąskaitų faktūrų grafiką**.

    Sistema sąskaitų faktūrų grafiką sukuria su tolesne laukų informacija.

    - **Sąskaitos faktūros vykdymo data** nustatoma kaip data, parenkama pagal sąskaitų faktūrų dažnį.
    - **Operacijos galutinė data** nustatoma kaip diena prieš **sąskaitos faktūros vykdymo datą**.
    - **Vykdymo būsena** automatiškai nustatoma į **Nevykdoma**. Kai automatinio sąskaitos faktūros kūrimo užduotis paleidžiama tam tikrai **sąskaitos faktūros vykdymo datai**, ji atnaujins šį lauką į **Vykdymas sėkmingas** arba **Vykdymas nepavyko**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Fiksuotos kainos sąskaitų faktūrų grafiko kūrimas projektu pagrįstai sutarties eilutei

Kai projektu pagrįstai sutarties eilutei taikomas fiksuotos kainos atsiskaitymo metodas, galite sukurti etapinį sąskaitų faktūrų grafiką. Atlikite šiuos veiksmus, kad automatiškai būtų sukurtas etapinis sąskaitų faktūrų grafikas, pagal kurį nustatomas baigtinis etapų, tolygiai paskirstančių per kalendoriaus laikotarpį, rinkinys.

1. Nueikite į **Parametrai** > **Sąskaitų faktūrų dažnis**, kad nustatytumėte sąskaitų faktūrų dažnį.
2. Atidarykite projekto sutartį ir skirtuke **Suvestinė** nustatykite pageidaujamą pristatymo datą.
3. Atidarykite fiksuotos kainos sutarties eilutę, kuriai reikia sukurti etapų grafiką. 
4. Skirtuke **Sąskaitų faktūrų grafikas (atsiskaitymo etapai)** pažymėkite sąskaitų išrašymo pradžios datą ir sąskaitų faktūrų dažnį. 
5. Papildomame tinklelyje pasirinkite **Periodiški etapai**.

    Sistema sąskaitų faktūrų grafiką sukuria su tolesne etapų informacija.

    - **Etapo pavadinimas** nustatomas kaip data, parenkama pagal sąskaitų faktūrų dažnį.
    - **Etapo data** nustatoma kaip data, parenkama pagal sąskaitų faktūrų dažnį.
    - **Etapo suma** apskaičiuojama sutarties sumą projektu pagrįstoje sutarties eilutėje padalijant iš etapų skaičiaus, kaip tai nurodo dažnis, sąskaitų išrašymo pradžia ir pageidaujamos pristatymo datos.
    - Jei sutarties eilutės lauke **Įvertinta mokesčių suma** yra reikšmė, šis laukas taip pat proporcingai paskirstomas kiekvienam etapui, kai generuojami periodiniai etapai.

Atsiskaitymo etapai turi būti lygūs projektu pagrįstos sutarties eilutės vertei. Jei jie nėra lygūs, įvyksta klaida. Šią klaidą galite ištaisyti užtikrindami, kad bendroji atsiskaitymo etapų suma būtų lygi eilutės sutarties vertei, kurdami, redaguodami arba naikindami etapus. Atlikę pakeitimus atnaujinkite puslapį.

### <a name="manually-create-milestones"></a>Etapų kūrimas rankiniu būdu

Fiksuotos kainos etapus galima generuoti rankiniu būdu, kai jie nėra periodiškai išskaidomi. Norėdami sukurti etapą rankiniu būdu, atlikite toliau nurodytus veiksmus.

1. Atidarykite fiksuotos kainos sutarties eilutę, kurioje norite sukurti etapą. 
2. Skirtuko **Sąskaitų faktūrų grafikas** papildomame tinklelyje pasirinkite **+ Kurti naują sutarties eilutės etapą**.
3. Formoje **Etapo kūrimas** įveskite reikiamą informaciją pagal toliau pateiktą lentelę. 

| Laukas | Vieta | Aprašo | Tolesnis poveikis |
| --- | --- | --- | --- |
| Etapo pavadinimas | Spartusis kūrimas | Etapo pavadinimo teksto laukas. | Šis laukas įtrauktas į projekto sutarties eilutės etapą ir sąskaitą faktūrą. |
| Projekto užduotis | Spartusis kūrimas | Jei etapas yra susietas su projekto užduotimi, naudokite šią nuorodą ir įtraukite pasirinktinę logiką bei nustatykite etapo būseną pagal užduoties būseną. | Ši nuoroda vėliau užduočiai neturės jokios įtakos. |
| Etapo data | Spartusis kūrimas | Data, kai automatinio sąskaitų faktūrų kūrimo procesas turėtų ieškoti šio etapo būsenos, kad jį svarstytų dėl sąskaitų faktūrų išrašymo. | Tai įtraukta į projekto sutarties eilutės etapą ir sąskaitą faktūrą. |
| Sąskaitos faktūros būsena | Spartusis kūrimas | Sukūrus etapą, ši būsena visada nustatoma kaip **Neparengta išrašyti sąskaitos faktūros** arba **Nepradėta**. | Tai įtraukta į projekto sutarties eilutės etapą ir sąskaitą faktūrą. |
| Eilutės suma | Spartusis kūrimas | Etapo suma ar vertė, kuriai bus išrašyta klientui skirta sąskaita faktūra. | Šis laukas įtrauktas į projekto sutarties eilutės etapą ir sąskaitą faktūrą. |
| Mokesčiai | Spartusis kūrimas | Etapui taikoma mokesčių suma. | Tai įtraukta į projekto sutarties eilutės etapą ir sąskaitą faktūrą. |

4. Pasirinkite **Įrašyti ir uždaryti**.
