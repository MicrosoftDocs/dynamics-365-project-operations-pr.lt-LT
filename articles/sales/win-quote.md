---
title: Pasiūlymo uždarymas
description: Šioje temoje pateikta informacija apie „Project Operations“ pasiūlymų uždarymą.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2314444dfdbd4d1a2f38c7de55e2070011e51a86f1e074dd6667d54393c641fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993431"
---
# <a name="close-a-quote"></a>Pasiūlymo uždarymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projekto pasiūlymą galima uždaryti kaip laimėtą arba pralaimėtą. Kadangi funkcijos „Aktyvinti“ ir „Peržiūrėti“ nepalaikomi „Microsoft Dynamics 365 Project Operations“ pasiūlymuose, galite uždaryti juodraštinį pasiūlymą.

## <a name="close-a-quote-as-won"></a>Pasiūlymo uždarymas kaip laimėto

Uždarant projekto pasiūlymą kaip laimėtą, nustatoma pasiūlymo būsena **Uždarytas**, o būsenos tipas nustatomas kaip **Laimėtas**. Uždarius pasiūlymą, jis pasidaro tik skaitomas ir sukuriamas projekto sutarties juodraštis su visa pasiūlymo informacija. Kadangi uždaryto pasiūlymo atidaryti iš naujo negalima, prieš uždarant pasiūlymą pateikiamas patvirtinimo dialogo langas, kuriame reikės patvirtinti keitimus.

Projekto sutartis, sukurta pagal projekto pasiūlymą, taip pat pateikiama „Project Operations“ modulyje Projektų valdymas ir apskaita. Jei projekto sutartis nesusieta su jokiomis projekto eilutėmis, ši projekto sutartis nustatoma kaip neaktyvi projekto sutartis ir ji pasidaro aktyvi iš karto, kai tik projektas susiejamas su bent viena iš sutarties eilučių.

Jei pasiūlymas pridedamas prie galimybės, kiti projekto pasiūlymai dėl galimybės automatiškai uždaromi kaip pralaimėti.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finansinis poveikis uždarius pasiūlymą kaip laimėtą

Jei yra įrašytų projekto laiko faktinių duomenų, kol jis dar pridėtas prie juodraštinio pasiūlymo, įrašomos tik laiko sąnaudos arba išlaidos. Kai pasiūlymas uždaromas kaip laimėtas, programa restruktūrizuos išlaidas atšaukdama senesnius išlaidų faktinius duomenis ir iš naujo sukurdama naujus išlaidų faktinius duomenis. Programa apdoros šiuos išlaidų faktinius duomenis pagal susietos projekto sutarties eilutės atsiskaitymo metodą. Jei išlaidų faktiniai duomenys nurodo laiko ir medžiagų sutarties eilutę, sistema automatiškai sukurs atitinkamus pardavimo faktinius duomenis, kuriems neišrašyta sąskaita faktūra, kai pasiūlymas uždaromas ir sukuriama projekto sutartis. Jei išlaidų faktiniai duomenys nurodo fiksuotos kainos sutarties eilutę, programa sustabdys išlaidų faktinių duomenų apdorojimą pagal išskaidyto atsiskaitymo taisykles, taikomas projekto sutarties klientams.

Visus iš naujo apdorotus faktinius duomenis projekto apskaitininkas gali rasti modulyje Projektų valdymas ir apskaita, kad galėtų juos peržiūrėti, atnaujinti ir užregistruoti didžiojoje knygoje. 

## <a name="close-a-quote-as-lost"></a>Pasiūlymo uždarymas kaip pralaimėto

Uždarant projekto pasiūlymą kaip pralaimėtą, bus nustatyta būsena **Uždarytas** ir nustatytas būsenos tipas **Pralaimėtas**. Uždarius pasiūlymą, jį galima tik skaityti. Kadangi uždaryto pasiūlymo atidaryti iš naujo negalima, prieš uždarant pasiūlymą pateikiamas patvirtinimo dialogo langas, kuriame reikės patvirtinti keitimus.

Jei projekto pasiūlymo, kuris uždarytas kaip pralaimėtas, bet kuri eilutė nurodo projektą, tas projektas taip pat pažymimas kaip uždarytas, o bet kokie išteklių rezervavimai nuo tos dienos atšaukiami.

> [!NOTE]
> „Project Operations“ uždarius pasiūlymą kaip laimėtą arba pralaimėtą galimybės būsena nebus paveikta – ji bus atidaryta tol, kol nebus uždaryta rankiniu būdu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]