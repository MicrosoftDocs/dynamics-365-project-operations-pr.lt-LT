---
title: Kopijuoti projektą
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Operations“ projektų kopijavimą.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574440"
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
- Projektų kontroliniai sąrašai
- Projekto kaušai

## <a name="project-properties"></a>Projekto ypatybes

Kopijuojant projektą, kopijuojamos šių laukų vertės.

| Laukas | Projekto operacijos nekaupiamos medžiagos | Projekto operacijos Lite | Žiniatinklio projektas |
|-------|------------------------------------------|-------------------------|---------------------|
| Pavadinimą | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Aprašą | :heavy_check_mark: | :heavy_check_mark: | |
| kliente | :heavy_check_mark: | :heavy_check_mark: | |
| Kalendoriaus šablonas | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Valiuta | :heavy_check_mark: | :heavy_check_mark: | |
| Sutartį sudarantis vienetas | :heavy_check_mark: | :heavy_check_mark: | |
| Įmonė, kuriai priklauso | :heavy_check_mark: | | |
| Projekto vadovas | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Būsena | :heavy_check_mark: | :heavy_check_mark: | |
| Bendroji projekto būsena | :heavy_check_mark: | :heavy_check_mark: | |
| Komentarai | :heavy_check_mark: | :heavy_check_mark: | |
| Įvertinimai | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Numatoma pradžios data</p><p><strong>Pastaba:</strong> Šiame lauke nurodoma projekto sukūrimo iš kopijos data. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Numatoma pabaigos data</p><p><strong>Pastaba:</strong> Data šiame lauke koreguojama pagal naujo projekto, kuris buvo atliktas iš kopijos, pradžios datą.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Pastangos (valandos) | :heavy_check_mark: | :heavy_check_mark: | |
| Įvertintos darbo sąnaudos | :heavy_check_mark: | :heavy_check_mark: | |
| Įvertinta išlaidų savikaina | :heavy_check_mark: | :heavy_check_mark: | |
| Įvertinta medžiagos savikaina | | :heavy_check_mark: | |

> [!NOTE]
> Projekto kopijavimas yra ilgo veikimo operacija. Nukopijuojami projekto įrašai, jų atitinkami atributai ir daug susijusių objektų. Dėl ilgo operacijos veikimo pobūdžio, paleidus kopijavimą paskirties projekto puslapis užrakinamas ir jo redaguoti negalima, kol atliekama kopijavimo operacija.

## <a name="work-breakdown-structure"></a>Darbo paskirstymo struktūra

Kai projektas kopijuojamas, nukopijuojama visa išteklių įkelta darbo paskirtstymo struktūra. Įvardytieji ištekliai pakeičiami bendraisiais ištekliais. Jei įvardytų išteklių darbo valandos nesutampa su bendruoju ištekliumi, tvarkaraštis bus perskaičiuotas, o užduoties trukmė gali keistis.

## <a name="project-team-members"></a>Projekto komandos nariai

Kai projekto komanda kopijuojama iš šaltinio projekto, kopijuojami bendrieji ištekliai. Bendrųjų išteklių priskyrimai tvarkomi taip pat kaip ir šaltinio projekte. Įvardytieji ištekliai bus konvertuoti į bendruosius komandos narius.

> [!NOTE]
> Komandos nariai ir priskyrimai nekopijuojami programoje "Project for the Web".

## <a name="estimates"></a>Įvertinimai

Nukopijavus projektą, iš šaltinio projekto kopijuojamos išteklių, išlaidų ir medžiagų sąmatos eilutės. 

Norėdami gauti informacijos apie tai, kaip programiškai pasiekti funkciją Kopijuoti projektą, žr. [Projektų šablonų kūrimas naudojant funkciją Kopijuoti projektą](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Pasiūlymai ir sutartys

Pasiūlymai ir sutartys nėra susieti su paskirties projektu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
