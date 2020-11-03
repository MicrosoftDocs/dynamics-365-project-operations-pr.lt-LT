---
title: Projektu pagrįstų galimybių kopijavimas
description: Šioje temoje pateikta informacija apie tai, kaip kopijuoti projektu pagrįstas galimybes programoje „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080775"
---
# <a name="copy-project-based-opportunities"></a>Projektu pagrįstų galimybių kopijavimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_


Galite lengvai kopijuoti projekto galimybes, kad sukurtumėte naujas projekto galimybes. 

1. Prisijunkite prie sąrašo puslapio **Projekto galimybės** ir pasirinkite galimybę iš sąrašo. Arba atidarykite konkrečios galimybės informacijos puslapį. 
2. Bet kuriame puslapyje pasirinkite **Kopijuoti**. Atidaromas dialogo puslapis, kuriame yra ši lauko informacija. Atsižvelgiant į šiame dialogo lange pasirinktas reikšmes, kopijavimo procesas gali pasikeisti.

    | **Laukas** | **Atitiktis, tikslas ir gairės** | **Tolesnis poveikis** |
    | --- | --- | --- |
    | Tema | Įveskite tikslinės galimybės aktualią temą. Kai atidaromas dialogo langas, sistema nustatys šaltinio galimybės temą su pridėtu tekstu **kopija**. | Nėra jokio tolesnio šio lauko poveikio. |
    | Abonementas | Nurodo į kliento įmonę arba kliento įrašą. Kai atidaromas dialogo langas, sistema nustatys ją šaltinio galimybės abonemente. | Šis laukas yra pirminis klientas galimybėje. |
    | Sutartį sudarantis vienetas | Organizacijos vienetas, atsakingas už su šiuo sandoriu susijusių projektų pristatymą. Kai atidaromas dialogo langas, sistema nustatys ją šaltinio galimybės sutartį sudarančiu vienetu. | Sutartį sudarantis vienetas yra įmonės padalinys, kuris vykdys projektus po to, kai sandoris bus uždarytas. Kiekvienas sutartį sudarantis vienetas turi valiutą, o ši valiuta naudojama projekto metu padarytoms sąmatinėms ir faktinėms išlaidoms. |
    | Valiuta | Valiuta, kuria vykdoma operacija. Kai atidaromas dialogo lango puslapis, sistema nustatys ją į šaltinio galimybės valiutą. | Valiuta naudojama nustatant numatytąjį kainoraštį ir kuriant pasiūlymo finansinius įvertinimus. Galiausiai valiuta naudojama išrašas sąskaitas faktūras klientui, kai sandoris laimėtas. |
    | Kopijavimo įkainiai | Reikšmė Taip / Ne, nurodanti, ar galimybės kainodara turėtų būti kopijuojama iš šaltinio galimybės. | Jei pasirinkta **Taip** , kainoraščiai iš šaltinio kopijuojami į tikslinę galimybę. Jei pasirinkta **Ne** , kainoraščiai iš naujo nustatomi pagal naujausius nustatytus kainoraščius. |

3. Pasirinkite **Gerai**. Sistema sukuria projekto galimybės kopiją, pagrįstą pažymėtais parametrais, ir atidaroma nauja projekto galimybė.
