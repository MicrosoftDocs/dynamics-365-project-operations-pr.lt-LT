---
title: Pasiūlymų uždarymas
description: Šioje temoje pateikta informacija apie „Project Operations“ pasiūlymo uždarymą.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080757"
---
# <a name="close-quotes"></a>Pasiūlymų uždarymas 

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projekto pasiūlymą galima uždaryti kaip laimėtą arba pralaimėtą. Pasiūlymų aktyvinimo ir peržiūros operacijos nepalaikomos „Microsoft Dynamics 365 Project Operations“, todėl juodraštinį pasiūlymą galima uždaryti.

## <a name="close-a-quote-as-won"></a>Pasiūlymo uždarymas kaip laimėto

Uždarant projekto pasiūlymą kaip laimėtą, uždaromas pasiūlymas, kurio būsena yra Uždarytas, o būsenos tipas nustatytas kaip Laimėtas. Uždarius pasiūlymą, projekto pasiūlymas pasidaro tik skaitomas ir sukuriamas projekto sutarties juodraštis, kuriame yra pasiūlymo informacija. Kadangi uždaryto pasiūlymo atidaryti iš naujo negalima, prieš atliekant pakeitimus pateikiamas patvirtinimo dialogo langas, nes uždaryto pasiūlymo atidaryti iš naujo negalima ir pakeitimų atšaukti neįmanoma.

Jei pasiūlymas pridedamas prie galimybės, kiti projekto pasiūlymai dėl galimybės automatiškai uždaromi kaip pralaimėti.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finansinis poveikis uždarius pasiūlymą kaip laimėtą

Jei yra įrašytų projekto laiko faktinių duomenų, kol jis dar pridėtas prie juodraštinio pasiūlymo, įrašomos tik laiko sąnaudos arba išlaidos. Kai pasiūlymas uždaromas kaip laimėtas, programa restruktūrizuos išlaidas atšaukdama senesnius išlaidų faktinius duomenis ir iš naujo sukurdama naujus išlaidų faktinius duomenis. Programa apdoros šiuos išlaidų faktinius duomenis pagal susietos projekto sutarties eilutės atsiskaitymo metodą. Jei išlaidų faktiniai duomenys nurodo laiko ir medžiagų sutarties eilutę, sistema automatiškai sukurs atitinkamus pardavimo faktinius duomenis, kuriems neišrašyta sąskaita faktūra, kai pasiūlymas uždaromas ir sukuriama projekto sutartis. Jei išlaidų faktiniai duomenys nurodo fiksuotos kainos sutarties eilutę, programa sustabdys išlaidų faktinių duomenų apdorojimą pagal išskaidyto atsiskaitymo taisykles, taikomas projekto sutarties klientams.

## <a name="closing-a-quote-as-lost"></a>Pasiūlymo uždarymas kaip pralaimėto:

Uždarant projekto pasiūlymą kaip pralaimėtą, bus nustatyta būsena Uždarytas ir nustatytas būsenos tipas Pralaimėtas. Uždarius pasiūlymą projekto pasiūlymas yra tik skaitomas. Kadangi uždaryto pasiūlymo atidaryti iš naujo negalima, prieš uždarant pasiūlymą pateikiamas patvirtinimo dialogo langas, kuriame reikės patvirtinti keitimus.

Jei projekto pasiūlymo, kuris uždarytas kaip pralaimėtas, bet kuri eilutė nurodo projektą, tas projektas taip pat pažymimas kaip uždarytas, o bet kokie išteklių rezervavimai nuo tos dienos atšaukiami.

> [!NOTE]
> „Project Operations“ uždarius pasiūlymą kaip laimėtą arba pralaimėtą galimybės būsena nebus paveikta – ji bus atidaryta tol, kol nebus uždaryta rankiniu būdu.
