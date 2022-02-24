---
title: Kopijuoti projektą
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Operations“ projektų kopijavimą.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479529"
---
# <a name="copy-a-project"></a>Projekto kopijavimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Naudodami „Dynamics 365 Project Operations“ galite greitai kurti naujus projektus formoje **Projektai** pasirinkdami **Kopijuoti projektą**. Jei norite kopijuoti projektą, atidarykite norimą kopijuoti projektą ir pasirinkite **Kopijuoti projektą**. Veiksmas kopijuos:

- Projekto ypatybės (numatoma pradžios data kopijuojama iš šaltinio projekto)
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
