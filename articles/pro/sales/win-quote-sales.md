---
title: Pasiūlymo uždarymas – „Lite“ versija
description: Šioje temoje pateikta informacija apie „Project Operations“ pasiūlymo uždarymą.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ae5e14220ffecab5bcfa016d8d18e6ccfbc5b04be9a4e66cee26f8885125d31
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994331"
---
# <a name="close-a-quote---lite"></a>Pasiūlymo uždarymas – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projekto pasiūlymą galima uždaryti kaip laimėtą arba pralaimėtą. Pasiūlymo juodraštį galima uždaryti, nes „Microsoft Dynamics 365 Project Operations“ pasiūlymuose nepalaiko aktyvavimo ir peržiūrėjimo operacijų.

## <a name="close-a-quote-as-won"></a>Pasiūlymo uždarymas kaip laimėto

Kai uždarote projekto pasiūlymą kaip laimėtą, būsena nustatoma į uždarytą, o būsenos tipas yra laimėtas. Uždarius pasiūlymą, projekto pasiūlymas pasidaro tik skaitomas ir sukuriamas projekto sutarties juodraštis, kuriame yra pasiūlymo informacija. Kadangi uždaryto pasiūlymo negalima atidaryti iš naujo, patvirtinimo dialogas patvirtins jūsų pakeitimus.

Jei pasiūlymas pridedamas prie galimybės, kiti projekto pasiūlymai dėl galimybės automatiškai uždaromi kaip pralaimėti.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finansinis poveikis uždarius pasiūlymą kaip laimėtą

Jei prie pasiūlymo juodraščio projekto faktinių duomenų projekto metu yra faktinių duomenų, įrašoma tik laiko arba išlaidų kaina. Kai pasiūlymas uždaromas kaip laimėtas, programa restruktūrizuos išlaidas atšaukdama senesnius išlaidų faktinius duomenis ir iš naujo sukurdama naujus išlaidų faktinius duomenis. Programa apdoros šiuos išlaidų faktinius duomenis pagal susietos projekto sutarties eilutės atsiskaitymo metodą. Jei išlaidų faktiniai duomenys nurodo laiką ir medžiagos sutarties eilutę, uždarius pasiūlymą ir sukūrus projekto sutartį sukuriami atitinkami pardavimo, už kurį neišrašyta SF, faktiniai duomenys. Jei išlaidų faktiniai duomenys nuoro fiksuotos kainos sutarties eilutę, programa sustabdys išlaidų faktinių duomenų, pagrįstų projekto sutarties klientų atsiskaitymo taisyklėmis, apdorojimą.

## <a name="closing-a-quote-as-lost"></a>Pasiūlymo uždarymas kaip pralaimėto:

Kai uždarote projekto pasiūlymą kaip pralaimėtą, būsena nustatoma į uždarytą, o būsenos tipas yra pralaimėtas. Uždarius pasiūlymą projekto pasiūlymas yra tik skaitomas. Kadangi uždaryto pasiūlymo atidaryti iš naujo negalima, prieš uždarant pasiūlymą pateikiamas patvirtinimo dialogo langas, kuriame reikės patvirtinti keitimus.

Jei projekto pasiūlymas, uždarytas kaip pralaimėtas, nurodo projektą bet kurioje iš jo eilučių, tas projektas taip pat pažymimas kaip uždarytas. Nuo tos dienos atšaukiami visi išteklių rezervavimai.

> [!NOTE]
> „Project Operations“ uždarius pasiūlymą kaip laimėtą arba pralaimėtą galimybės būsena nebus paveikta – ji bus atidaryta tol, kol nebus uždaryta rankiniu būdu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]