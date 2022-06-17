---
title: Kelių klientų tvarkymas projektu pagrįstose sutarties eilutėse – „Lite“ versija
description: Šiame straipsnyje pateikiama informacija apie kelių klientų valdymą pagal projektą pagrįstų sutarčių eilutėse.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f7648c7ef7ec6ffb68932552a0c25b79f1f93733
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922140"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Kelių klientų tvarkymas projektu pagrįstose sutarties eilutėse – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projektu pagrįstose sutarties eilutėse gali būti klientų, atsakingų už mokėjimą, sąrašas. Šis projektu pagrįstoje sutarties eilutėje esantis klientų sąrašas gali būti toks pats kaip sutartyje nurodytas klientų sąrašas, bet tai neprivaloma. Laimėjus projekto pasiūlymą ir sukūrus projekto sutartį, pasiūlymo eilutėje esantis klientų sąrašas nukopijuojamas į atitinkamą sutarties eilutę. Pasiūlyme nurodyti klientai nukopijuojami į sutartį.

Išrašant projekto sutarties sąskaitą faktūrą, projektu pagrįstoje sutarties eilutėje nurodytas klientų sąrašas turi viršenybę prieš sutarties klientų sąrašą. Klientų sąrašas, esantis projekto sutartyje, naudojamas tik numatytosioms naujoms sutarties eilutėms sukurti.

Visi sutarties klientai, esantys projekto sutarties skirtuke **Klientai**, nustatomi kaip numatytieji sutarties eilutės klientai visose naujose sukurtose projekto sutarties eilutėse. Jokios esamos sutarties eilutės nebus pakeistos naujais sutarties kliento įrašais, kurie sukurti po jų.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Sutarties eilutės kliento įrašo kūrimas, naujinimas arba panaikinimas

Galite kurti, atnaujinti arba panaikinti sutarties eilutės klientą skirtuke Sutarties eilutės klientai, esančiame puslapyje Projektu pagrįsta sutarties eilutė. Įtraukus naują klientą į projektu pagrįstą sutarties eilutę, jis taip pat bendrai įtraukiamas į sutartį kaip sutarties klientas ir nustatoma numatytoji nulinė atsiskaitymo išskaidymo procentinė vertė. Bendros sutarties atsiskaitymo išskaidymo procentinė vertė nukopijuojama į naujas sutarties eilutes ir paskui sukuriamą projekto sutartį. Tačiau išrašant sąskaitą faktūrą pagal sutartį, naudojama atsiskaitymo išskaidymo procentinė vertė sutarties eilutės lygiu, o ne atsiskaitymo išskaidymo procentinė vertė bendros sutarties lygiu.

Toliau pateikiami projektu pagrįstos sutarties eilutės **Sutartis** kliento įrašo laukai, į kuriuos reikia atsižvelgti.

| Laukas | Vieta | Aprašo | Tolesnis poveikis |
| --- | --- | --- | --- |
| **Klientas** | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties klientui. | Visi aktyvūs klientai. Šis laukas užrakinamas sukūrus įrašą. Naudojamas norint atnaujinti lauką, panaikinti įrašą ir sukurti naują įrašą. Jei įrašėte kokius nors faktinius duomenis, panaikinti įrašo negalima. Tačiau galite nurodyti nulinę to kliento atsiskaitymo išskaidymo procentinę vertę. Įraše nurodžius nulinę vertę, tai turi įtakos visoms būsimoms faktinėms išlaidoms ir įplaukoms, priskirtoms arba padalytoms šiam klientui. | Kai pasirenkate klientą iš pagrindinio klientų sąrašo norėdami jį įtraukti ir įrašyti, sutarties eilutės klientas taip pat įtraukiamas kaip sutarties klientas. Sutarties eilutės klientai naudojami išrašant sąskaitas faktūras. |
| **Atsiskaitymo išskaidymo procentas** | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties klientui. | Šis laukas nurodo kiekvienos pardavimo operacijos, už kurią neišrašyta sąskaita faktūra, procentinę dalį, kuri bus priskirta šios sutarties eilutės klientui. | Sutarties eilutės klientai ir atsiskaitymo išskaidymo procentinės vertės naudojami tada, kai patvirtinus sukuriami faktiniai duomenys ir sugeneruojama sąskaita faktūra. |
| **Limitas, kurio negalima viršyti** | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties klientui. | Nurodo, ar yra sutartinis limitas, ar viršutinė riba, taikoma bendrai sumai, kuri bus išrašyta šiam sutarties eilutės klientui. | Sutarties eilutės kliento limitas, kurio negalima viršyti, naudojamas tada, kai sukuriami faktiniai duomenys ir sugeneruojamos sąskaitos faktūros. |
| **Apvalinamas** | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties eilutės klientui. | Šis laukas nurodo, ar šis klientas yra numatytasis šios projektu pagrįstos sutarties eilutės apvalinimo klientas. | Kai generuojate faktinius duomenis pagal atsiskaitymo išskaidymo procentinę vertę, gali būti kai kurių apvalinimo paklaidų. Šiuo atveju šiam klientui taikoma apvalinimo paklaida. |

## <a name="edit-billing-split-percentages"></a>Atsiskaitymo išskaidytos procentinės dalies redagavimas

Atsiskaitymo išskaidymo procentines vertes galima redaguoti tinklelyje. Jei atsiskaitymo išskaidymo procentinės vertės nesudaro 100 procentų, pateikiama klaida. Pakoregavę atsiskaitymo išskaidymo procentines vertes, atnaujinkite puslapį, kad pašalintumėte klaidą.

Taip pat galite pasirinkti parinktį **Paskirstyti tolygiai** sutarties eilutės kliento papildomame tinklelyje. Tai pasirinkus atsiskaitymas išskaidomas tolygiai visiems sutarties eilutės klientams. Jei yra koks nors apvalinimo koeficientas, jis bus įtrauktas į apvalinimo klientą. Vienam sutarties eilutės klientui visada taikoma parinktis **Apvalinimas** ir žymė **Apvalinimas** nustatoma kaip **Taip**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]