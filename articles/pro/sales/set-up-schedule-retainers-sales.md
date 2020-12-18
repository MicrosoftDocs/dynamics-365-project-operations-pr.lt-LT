---
title: Išankstinių apmokėjimų grafiko nustatymas
description: Šioje temoje pateikiama informacija apie tai, kaip nustatyti išankstinių apmokėjimų grafiką programoje „Project Operations”.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1c264b544660cf7a0b116f09b6bd7c94fcf0457e
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596382"
---
# <a name="set-up-a-retainer-schedule"></a>Išankstinių apmokėjimų grafiko nustatymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Išankstinių apmokėjimų grafikai nustatomi programos „Dynamics 365 Project Operations” puslapyje **Projekto sutartis**.

1. Puslapio **Projekto sutartis** skirtuke **Avansai ir išankstiniai apmokėjimai** pasirinkite **Išankstinių apmokėjimų grafiko nustatymas**.
2. Atsivėrusiame dialogo puslapyje rodomi laukai, išvardyti toliau pateikiamoje lentelėje. Lentelėje pateikiama idėja, kokį poveikį ar įtaką turės įvestos reikšmės išankstinių apmokėjimų grafikui, kuris bus sukurtas.

| Laukas | Aprašo | Tolesnis poveikis |
| --- | --- | --- |
| Projekto sutarties klientas | Sutarties klientas, kuriam bus išrašyta šių išankstinių apmokėjimų ar avanso sąskaita faktūra. | Jei sutartyje yra keli klientai ir reikia kiekvienam jų išrašyti konkrečių išankstinių apmokėjimų ar avanso sąskaitą faktūrą, rankiniu būdu sukurkite sąskaitą faktūrą kiekvienam klientui. |
| Išankstinio apmokėjimo grafiko pradžia | Įveskite išankstinių apmokėjimų grafiko pradžios datą. | Ši data gali būti ne ta data, kai buvo sukurti pirmi išankstiniai apmokėjimai ar avansas. Data, kai buvo sukurti pirmi išankstiniai apmokėjimas ar avansas, taip pat yra veikiama sąskaitos faktūros dažnumo. |
| Išankstinio apmokėjimo grafiko pabaiga | Įveskite išankstinių apmokėjimų grafiko pabaigos datą. | Ši data gali būti ne ta data, kai buvo sukurti paskutiniai išankstiniai apmokėjimai ar avansas. Data, kai buvo sukurti paskutiniai išankstiniai apmokėjimas ar avansas, taip pat yra veikiama sąskaitos faktūros dažnumo. |
| Kuriamų išankstinių apmokėjimų skaičius | Kai įvedate išankstinių apmokėjimų, kuriuos reikia sukurti, skaičių, sistema naudoja pradžios datą ir dažnumą, kad sukurtų skaičių šiame lauke. | Rankiniu būdu atnaujinus šį lauką, sistema nepaiso reikšmės, esančios lauke **Išankstinio apmokėjimo grafiko pabaiga**, ir vietoj to kuria konkretų išankstinių apmokėjimų arba avansų akaičių. |
| Sąskaitos faktūros dažnumas | Kaip dažnai programa kurs išankstinius apmokėjimus ir avansus. | Ši reikšmė turi tiesioginės įtakos išankstinių apmokėjimų ir avansų skaičiui bei sukūrimo datoms. |
| Bendra suma | Bendra suma yra suma, padalyta į atskirus išankstinius mokėjimus arba avansus, kurie bus sukurti. | Nėra jokio tolesnio šio lauko poveikio. |
