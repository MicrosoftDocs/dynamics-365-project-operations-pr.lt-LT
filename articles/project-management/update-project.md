---
title: Projekto kūrimas ir naujinimas
description: Šioje temoje pateikta informacija apie „Project Operations“ projektų naujinimą.
author: ruhercul
ms.date: 10/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 07f96973a1341e65e648f126a931d72454334e9c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8592518"
---
# <a name="create-and-update-a-project"></a>Projekto kūrimas ir naujinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Toliau pateikiama laukų, kuriuos galima atnaujinti projekte po to, kai jis buvo sukurtas, suvestinė. Be to, joje pateikiamos visos taikytinos pasekmės, susijusios su šiais naujinimais.

## <a name="project-detail-fields"></a>Projekto išsamios informacijos laukai

- **Pavadinimas**: projekto pavadinimas.
- **Aprašas**: projekto apžvalga.
- **Klientas**: įmonė, kuriai daromas projektas.
- **Kalendoriaus šablonas**: projekto darbo valandos. Kai laukas pakeičiamas, perskaičiuojamas visas grafikas.
- **Valiuta**: projekto valiuta. Numatytoji šio lauko reikšmė priklauso nuo valiutos, apibrėžtos sutartį sudarančiame vienete. Atnaujinus sutartį sudarantį vienetą, laukas taip pat atnaujinamas.
- **Sutartį sudarantis vienetas**: organizacinis vienetas, atstovaujantis įmonių grupę arba padalinį, kuris yra atsakingas už laimėtą pardavimą ir darbo bei paslaugų pristatymą klientui.  Nustačius projekto vadovo organizacijos vienetą, nustatoma šio lauko numatytoji reikšmė, apibrėžta projekto parametruose.
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



[!INCLUDE[footer-include](../includes/footer-banner.md)]
