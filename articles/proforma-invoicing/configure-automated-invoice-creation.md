---
title: Automatizuotų sąskaitų faktūrų kūrimo konfigūravimas
description: Šioje temoje pateikta informacija apie tai, kaip konfigūruojant sistemą automatiškai generuoti sąskaitas faktūras.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 295c3b099c9670c930fb2ba2fd208be63a77217f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122443"
---
# <a name="configure-automatic-invoice-creation"></a>Automatizuotų sąskaitų faktūrų kūrimo konfigūravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_


Atlikite šiuos veiksmus, kad konfigūruotumėte automatinę sąskaitą faktūrą „Dynamics 365 Project Operations“.

1. Pasirinkite **Parametrai** > **Paketinės užduotys**.
2. Sukurkite paketinę užduotį ir pavadinkite ją **„Project Operations“ sąskaitų faktūrų kūrimas**. Paketinės užduoties pavadinime turi būti terminas „Kurti sąskaitas faktūras“.
3. Lauke **Užduoties tipas** pasirinkite **Nėra**. Pagal numatytuosius nustatymus, parinktys **Dažnumas: kasdien** ir **Aktyvus** nustatytos į **Taip**.
4. Pasirinkite **Vykdyti darbo eigą**. Dialogo lange **ieškoti įrašo** matysite tris darbo eigas:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Pasirinkite **ProcessRunCaller**, o tada pažymėkite **Įtraukti**.
6. Kitame dialogo lange pasirinkite **Gerai**. Po darbo eigos **Miego režimas** seka darbo eiga **Procesas**.

  > [!NOTE]
  > Taip pat galite pasirinkti **ProcessRunner** 5 veiksme. Pažymėję **Gerai**, po darbo eigos **Procesas** seka darbo eiga **Miego režimas**.

Darbo eigos **ProcessRunCaller** ir **ProcessRunner** sukuria sąskaitas faktūras. **ProcessRunCaller** iškviečia **ProcessRunner**. **ProcessRunner** yra darbo eiga, kuri iš tikrųjų sukuria sąskaitas faktūras. Ji taikoma visoms sutarties eilutėms, kurioms reikia sukurti SF, ir sukuria tų eilučių sąskaitas faktūras. Norint nustatyti sutarties eilutes, kurioms reikia sukurti SF, užduotis atsižvelgia į projekto eilutėms skirtos sąskaitos faktūros vykdymo datas. Jei vienam projektui priklausančių projekto eilučių sąskaitos faktūros buvo vykdytos tuo pačiu metu, operacijos įtraukiamos į vieną sąskaitą faktūrą, kurioje yra dvi sąskaitos faktūros eilutės. Jei nėra operacijų, skirtų išrašyti sąskaitas faktūras, užduotis nesukuria sąskaitos faktūros.

Kai **ProcessRunner** baigia vykdymą, iškviečiamas **ProcessRunCaller**, pateikiamas pabaigos laikas ir yra uždaromas. Tada **ProcessRunCaller** paleidžia laikmatį, kuris trunka 24 valandas nuo nurodyto pabaigos laiko. Baigiantis laikmačio laikui, **ProcessRunCaller** uždaromas.

Paketinė proceso užduotis, skirta sąskaitoms faktūroms kurti, yra pasikartojanti užduotis. Jei šis paketinis procesas vykdomas daug kartų, sukuriami keli užduoties egzemplioriai ir sukeliamos klaidos. Todėl paketinį procesą reikia pradėti tik vieną kartą, o jį paleisti iš naujo reikia tik tuo atveju, jei jis sustos.

> [!NOTE]
> Paketinių sąskaitų faktūrų išrašymas vykdomas tik projekto sutarties eilutėse, sukonfigūruotose sąskaitų faktūrų grafike. Sutarties eilutė su fiksuotos kainos atsiskaitymų metodu turi turėti sukonfigūruotus etapus. Norint naudoti projekto sutarties eilutę su laiko ir medžiagų atsiskaitymo metodu, reikės nustatyti data pagrįstą sąskaitos faktūros grafiką. Tokia pati tvarka galioja ir projektu pagrįstai sutarties eilutei.     