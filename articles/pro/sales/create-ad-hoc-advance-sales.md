---
title: Ad hoc avanso kūrimas sutartyje
description: Šiame straipsnyje pateikiama informacija apie sutarties avanso sukūrimą, jei reikia.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3e450a17990c6fc783ddffdb05e1ab5b9429a3c1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922186"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Ad hoc avanso kūrimas sutartyje

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]