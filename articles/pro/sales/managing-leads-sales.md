---
title: Galimų klientų valdymas – „Lite“ versija
description: Šioje temoje pateikta informacija apie projektu pagrįstų galimų klientų valdymą (Pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 00fc16b0e723d4df88ceae961d9772e26dd1451e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180517"
---
# <a name="manage-leads---lite"></a>Galimų klientų valdymas – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projektu pagrįstus galimus klientus galima tvarkyti ir kvalifikuoti „Project Operations“. Galimų klientų valdymo procesas apima darbu pagrįstų galimų klientų kūrimą ir jų patvirtinimą. 

## <a name="list-of-project-sales-leads"></a>Projektu pagrįstų galimų klientų sąrašas

Skyrius **Pardavimas**, esantis kairiojoje naršymo srityje, atidaro sąrašo **Galimi klientai** puslapį, kur galima peržiūrėti visų sistemos galimų klientų įrašų sąrašą. Rodomą galimų klientų sąrašą sudaro darbu pagrįsti ir kitų tipų galimi klientai, kuriuos galima sukurti, jei turite „Dynamics 365 Sales“ arba „Dynamics 365 Field Service“ programą.

Galite sukurti filtruotą rodinį, kad matytumėte tik projektu pagrįstus galimus klientus, sukurdami filtrą reikšmėje **Tipas**. Pavyzdžiui, galite pasirinkti, kad būtų rodomi tik darbu pagrįsti galimi klientai.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Naujo galimo kliento, skirto projektu pagrįstam sandoriui, kūrimas

Kai projektu pagrįstas galimas klientas yra kvalifikuotas, sukuriama galimybė ir klientas. Projektu pagrįsta galimybė yra pradinis su pardavimu susijusios veiklos galimybių etape taškas. Projektu pagrįstos galimybės turi unikalių galimybių, reikalingų pardavimo projekto darbui. Šios galimybės apima:

- Laiko ir medžiagų bei fiksuotos kainos atsiskaitymo metodai
- Kelių datų efektyvūs kainoraščiai, skirti projekto žmogiškiesiems ištekliams, išlaidoms ir medžiagoms.

Kad tinkamas galimas klientas galėtų sukurti galimybę, kurdami galimą klientą nustatykite atributą **Tipas** į **Pagrįstas darbu**. Jei pasirinksite kitą tipą, galimas klientas nesukurs projektu pagrįstos galimybės. Jei projektu pagrįsta galimybė nesukuriama, projektui būdingų pajėgumų nebus tolesniuose pardavimo procesuose.

Šioje lentelėje yra svarbi galimo kliento lauko informacija ir šių laukų tolesnis poveikis.

| **Laukas** | **Vieta** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Tema | Bendros informacijos skirtukas | Šiame teksto lauke turi būti trumpas sandorio aprašas. | Galimo kliento tema bus numatytoji kaip galimybės ir pasiūlymo bei projekto sutarties pavadinimo tema. |
| Tipas | Bendros informacijos skirtukas | Šis parinkčių rinkinio laukas turi šias parinktis:</br>- Darbu pagrįsta (veikia tik kai įdiegta „Project Operations“)</br>- Elementu pagrįsta (yra tik jei turite įsidiegę „Project Operations“ ir „Sales")</br>- Pagrįstas aptarnavimo priežiūra (yra, kai įdiegta „Field Service“) | Kai šio lauko galimame kliente reikšmė nustatyta kaip **Darbu pagrįsta**, galimą klientą galima kvalifikuoti, kad būtų sukurta projektu pagrįsta galimybė. Galimybė turi būti pagrįsta projektu, kad būtų galima įjungti visus su projektu susijusius išplėtimus ir funkcijas tolesniuose šio sandorio procesuose. |
| Vardas | Bendros informacijos skirtukas | Potencialaus kliento vardas | Kai galimas klientas yra kvalifikuotas, sukuriamas klientas, kontaktas ir galimybė. Kontakto vardo reikšmė nustatyta čia. |
| Pavardė | Bendros informacijos skirtukas | Potencialaus kliento pavardė | Kai galimas klientas yra kvalifikuotas, sukuriamas klientas, kontaktas ir galimybė. Kontakto pavardės reikšmė nustatyta čia. |
| Įmonė | Bendros informacijos skirtukas | Potencialaus kliento įmonės pavadinimas | Kai galimas klientas yra kvalifikuotas, sukuriamas klientas, kontaktas ir galimybė. Sukurto kliento vardo reikšmė nustatyta čia. |
| Valiuta | Išsamios informacijos skirtukas | Potencialaus kliento valiuta | Kai galimas klientas yra kvalifikuotas, sukuriamas klientas, kontaktas ir galimybė. Sukurtos kliento valiutos reikšmė nustatyta čia. |

## <a name="qualify-a-new-project-based-lead"></a>Naujo projekto pagrįsto galimo kliento tinkamumo patvirtinimas

Galimi klientai, kurių reikšmė **Tipas** nustatyta kaip **Darbu pagrįsta**, vadinami projektu pagrįstais galimais klientais. Kai projektu pagrįstas galimas klientas yra patvirtintas kaip tinkamas, sukuriama:

- Klientas, kuris naudoja lauką **Įmonė** iš galimo kliento.
- Kontakto įrašas, susietas su klientu pagal galimo kliento laukų **Vardas** ir **Pavardė** reikšmes.
- Projektu pagrįsta galimybė, kurios laukas **Tipas** nustatytas į **Pagrįstas darbu**.

Išsamesnės informacijos apie galimų klientų tinkamumą žr. [Galimų klientų tinkamumo patvirtinimas arba konvertavimas](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Projektu pagrįstų sandorių veiklos procesų seka

„Project Operations“ palaikomos tokios projektu pagrįstų sandorių veiklos procesų sekos:

- Galimas klientas į galimybės veiklos procesą
- Galimybės pardavimo procesas

Galimas klientas į galimybės veiklos procesą palaiko šiuos etapus:

| Etapo pavadinimas | Susietas objektas | Funkcija |
| --- | --- | --- |
| Patvirtinti tinkamumą | Galimas klientas | Galimo kliento patvirtinimas, kad būtų sukurtas klientas, kontaktass ir galimybė. |
| Kurti | Galimybė | Sukurkite galimybę, kad būtų įtraukta daugiau informacijos apie susijusį darbą, svarbiausias suinteresuotąsias šalis ir konkurenciją. |
| Siūlyti | Galimybė | Sukurkite pasiūlymą ir gaukite vidinės peržiūros komandos patvirtinimą. |
| Uždaryti objektą  | Galimybė | Laimėkite galimybę, kad uždarytumėte sandorį. |
