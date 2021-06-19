---
title: Kopijuoti projektą
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Operations“ projektų kopijavimą.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091264"
---
# <a name="copy-a-project"></a>Projekto kopijavimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Naudodami „Dynamics 365 Project Operations“ galite greitai kurti naujus projektus formoje **Projektai** pasirinkdami **Kopijuoti projektą**. Jei norite kopijuoti projektą, atidarykite norimą kopijuoti projektą ir pasirinkite **Kopijuoti projektą**. Veiksmas nukopijuos šiuos duomenis:

- Projekto ypatybes 
- Darbo paskirstymo struktūra
- Projekto komandos nariai
- Projekto įvertinimai
- Projekto išlaidų įvertinimai
- Projekto medžiagų įvertinimai

## <a name="project-properties"></a>Projekto ypatybes

Kai projektas kopijuojamas, kopijuojamos šių laukų reikšmės:

- Pavadinimas / vardas, pavardė
- Aprašo
- Klientas
- Kalendoriaus šablonas
- Valiuta
- Sutartį sudarantis vienetas
- Projekto vadovas
- Būsena
- Bendroji projekto būsena
- Komentarai
- Įvertinimai
- Numatoma pradžios data: tai yra data, kai projektas kuriamas iš kopijos.
- Numatoma pabaigos data: ši data tikslinama pagal naujo projekto, sukurto iš kopijos, pradžios datą.
- Pastangos (valandos)
- Įvertintos darbo sąnaudos
- Įvertinta išlaidų savikaina
- Įvertinta medžiagos savikaina

> [!NOTE]
> Projekto kopijavimas yra ilgo veikimo operacija. Nukopijuojami projekto įrašai, jų atitinkami atributai ir daug susijusių objektų. Dėl ilgo operacijos veikimo pobūdžio, paleidus kopijavimą paskirties projekto puslapis užrakinamas ir jo redaguoti negalima, kol atliekama kopijavimo operacija.

## <a name="work-breakdown-structure"></a>Darbo paskirstymo struktūra

Kai projektas kopijuojamas, nukopijuojama visa išteklių įkelta darbo paskirtstymo struktūra. Įvardytieji ištekliai pakeičiami bendraisiais ištekliais. Jei įvardytieji ištekliai neturi tokių pačių darbo valandų kaip bendrasis išteklius, grafikas bus perskaičiuotas ir užduoties trukmė gali pasikeisti.

## <a name="project-team-members"></a>Projekto komandos nariai

Kai projekto komanda kopijuojama iš šaltinio projekto, kopijuojami bendrieji ištekliai. Bendrųjų išteklių priskyrimai tvarkomi taip pat kaip ir šaltinio projekte. Įvardytieji ištekliai bus konvertuoti į bendruosius komandos narius.

## <a name="estimates"></a>Įvertinimai

Nukopijavus projektą, iš šaltinio projekto kopijuojamos išteklių, išlaidų ir medžiagų sąmatos eilutės. 

Norėdami gauti informacijos apie tai, kaip programiškai pasiekti funkciją Kopijuoti projektą, žr. [Projektų šablonų kūrimas naudojant funkciją Kopijuoti projektą](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
