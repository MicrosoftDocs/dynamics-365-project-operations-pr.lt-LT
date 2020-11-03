---
title: Kopijuoti projektą
description: Šioje temoje pateikiama informacija apie projektų kopijavimą programoje „Dynamics 365 Project Operations“.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: cf80f2a1cd27aae33d123e45dee70d94ea4d01a9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080777"
---
# <a name="copy-a-project"></a>Kopijuoti projektą

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Naudodami „Dynamics 365 Project Operations“ galite greitai kurti naujus projektus pasirinkdami **Kopijuoti projektą** , esantį formoje **Projektai**. Jei norite kopijuoti projektą, atidarykite norimą kopijuoti projektą ir pasirinkite **Kopijuoti projektą**. Veiksmas kopijuos:

- Projekto ypatybes
- Darbo paskirstymo struktūrą
- Projekto komandos nariai
- Projekto įvertinimai
- Projekto išlaidų įvertinimai

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
- Numatoma pradžios data
- Pabaigos data
- Pastangos (valandos)
- Įvertintos darbo sąnaudos
- Įvertinta išlaidų savikaina

## <a name="work-breakdown-structure"></a>Darbo paskirstymo struktūra

Kai projektas kopijuojamas, nukopijuojama visa išteklių įkelta darbo paskirtstymo struktūra. Įvardytieji ištekliai pakeičiami bendraisiais ištekliais. Jei įvardytieji ištekliai neturi tokių pačių darbo valandų kaip bendrasis išteklius, grafikas bus perskaičiuotas ir užduoties trukmė gali pasikeisti.

## <a name="project-team-members"></a>Projekto komandos nariai

Kai projekto komanda kopijuojama iš šaltinio projekto, kopijuojami bendrieji ištekliai. Bendrųjų išteklių priskyrimai tvarkomi taip pat kaip ir šaltinio projekte. Įvardytieji ištekliai bus konvertuoti į bendruosius komandos narius.

## <a name="estimates"></a>Įvertinimai

Kai projektas kopijuojamas, iš šaltinio projekto kopijuojamos ir išteklių, ir išlaidų įvertinimo eilutės. 

Norėdami gauti informacijos apie tai, kaip programiškai pasiekti funkciją Kopijuoti projektą, žr. [Projektų šablonų kūrimas naudojant funkciją Kopijuoti projektą](dev-copy-project.md).
