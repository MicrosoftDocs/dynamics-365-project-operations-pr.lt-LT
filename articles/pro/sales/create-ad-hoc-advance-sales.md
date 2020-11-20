---
title: Ad hoc avanso sukūrimas sutartyje – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip prireikus sutartyje sukurti avansą.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181372"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Ad hoc avanso sukūrimas sutartyje – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

„Microsoft Dynamics 365 Project Operations“ palaiko sąskaitų faktūrų išrašymo scenarijus, kurie apima išankstinius mokėjimus ir avansus. Programoje **„Project Operations“** **avansai** naudojami panašiai kaip **išankstinių apmokėjimų** sutartys. 

Norėdami klientui išrašyti sąskaitą faktūrą už avansą, atlikite tolesnius veiksmus.

1. Nueikite į puslapį **Projekto sutartis**, tada pasirinkite skirtuką **Avansai ir išankstiniai apmokėjimai**.
2. Papildomame tinklelyje, kuriame išvardyti visi anksčiau nurodyti avansai ir išankstiniai apmokėjimai, pasirinkite **+ Naujas projekto sutarties išankstinis apmokėjimas**. 

    Atidaroma **sparčiojo kūrimo** forma, skirta išankstiniam mokėjimui arba avansui įrašyti.
    
3. Toliau pateiktoje lentelėje išvardyti laukai, pagal kuriuos reikia įrašyti avansą, ir aspektai, kurių reikia nepamiršti kuriant naujus avansus.

    | Laukas | Aprašo | Tolesnis poveikis |
    | --- | --- | --- |
    | **Projekto sutarties klientas** | Šis laukas nurodo, kuriam sutarties klientui bus išrašyta sąskaita faktūra už šį avansą. | Jei sutartyje yra keli klientai ir norite kiekvienam iš jų išrašyti konkrečių išankstinių apmokėjimų ar avanso sąskaitą faktūrą, atskirai sukurkite avansą kiekvienam klientui. |
    | **Aprašas** | Avanso paskirties ar laiko aprašas, siekiant padėti nustatyti šį avansą. | Šis aprašas rodomas šio avanso sąskaitos faktūros eilutėje. |
    | **Suma** | Išankstinio mokėjimo arba avanso suma. | Ši suma rodoma šio avanso sąskaitos faktūros eilutėje. |
    | **Sąskaitos faktūros data** | Šio avanso sąskaitos faktūros išrašymo klientui data. | Tai yra data automatiniam sąskaitos faktūros kūrimo procesui, kad būtų galima sukurti šio avanso sąskaitos faktūros eilutę. |
    | **Sąskaitos faktūros būsena** | Tai yra parinkčių parametras, nurodantis, ar šis avansas įtraukiamas į šio kliento sąskaitos faktūros juodraštį. Galimos tolesnės reikšmės.</br>- **Neparengta išrašyti sąskaitos faktūros**</br>- **Parengta išrašyti sąskaitą faktūrą** | Kai avansas arba išankstinis mokėjimas pažymimas kaip **Parengta išrašyti sąskaitą faktūrą**, jis kaip eilutės laikas įtraukiamas į sąskaitos faktūros juodraštį. Tik toks avansas, kuriam visam išrašyta sąskaita faktūra, gali būti naudojamas norint derinti projekto kaštus kitam sąskaitos faktūros laikotarpiui. |

4. Norėdami įrašyti avansą arba išankstinį mokėjimą, sparčiojo kūrimo dialogo lange pasirinkite **Įrašyti ir uždaryti**.
