---
title: Išankstinių apmokėjimų grafiko nustatymas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip nustatyti išankstinių apmokėjimų grafiką programoje „Project Operations”.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 077961d2f649754149315438252970609c246555
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927752"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]