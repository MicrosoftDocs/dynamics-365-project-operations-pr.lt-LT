---
title: Naujinti projektą
description: Šioje temoje pateikta informacija apie „Project Operations“ projektų naujinimą.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897822"
---
# <a name="update-a-project"></a>Naujinti projektą

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Toliau pateikiama laukų, kuriuos galima atnaujinti projekte po to, kai jis buvo sukurtas, suvestinė ir bet kokios galimos naujinimų pasekmės.

## <a name="project-detail-fields"></a>Projekto išsamios informacijos laukai

- **Pavadinimas**: projekto pavadinimas.
- **Aprašas**: projekto apžvalga.
- **Klientas**: įmonė, kuriai daromas projektas.
- **Kalendoriaus šablonas**: projekto darbo valandos. Kai laukas pakeičiamas, perskaičiuojamas visas grafikas.
- **Valiuta**: projekto valiuta. Šio lauko numatytosios reikšmės nustatomos pagal valiutą, apibrėžtą sutartį sudarančiame vienete. Atnaujinus sutartį sudarantį vienetą, laukas taip pat atnaujinamas.
- **Sutartį sudarantis vienetas**: organizacinis vienetas, atstovaujantis įmonių grupę arba padalinį, kuris yra atsakingas už laimėtą pardavimą ir darbo bei paslaugų pristatymą klientui. 
- **Projekto vadovas**: projekto komandos narys, turintis įgaliojimus peržiūrėti ir patvirtinti laiko įrašus ir išlaidas.

## <a name="estimate-fields"></a>Įvertinimo laukai

- **Numatoma pradžios data**: data, kada prasidės projektas. Atnaujinus šį lauką, bet kokios projekto užduotys bus proporcingai atnaujintos atsižvelgiant į naują pradžios datą.
- **Pabaigos data**: numatyta projekto pabaigos data.
- **Pastangos**: numatytos projekto pastangos. Kai užduotys įtraukiamos į projektą, šis laukas neberedaguojamas.
- **Įvertintos darbo sąnaudos**: įvertintos projekto darbo sąnaudos. Kai darbo sąnaudos įtraukiamos į projektą, šis laukas neberedaguojamas.
- **Numatomos išlaidos**: numatomos projekto išlaidos. Kai išlaidos įtraukiamos į projektą, šis laukas neberedaguojamas.

## <a name="project-actual-fields"></a>Projekto faktinių duomenų laukai
- **Faktinė pradžia**: data, kada prasidėjo projektas.
- **Faktinė pabaiga**: laukas atnaujinamas baigus projektą.

## <a name="project-status-fields"></a>Projekto būsenos laukai

- **Bendroji projekto būsena**: bendroji projekto būsena, kurią pateikia projekto vadovas.
- **Komentarai**: projekto vadovo pastabos apie esamą projekto būseną.

