---
title: Išlaidų ataskaitų publikavimas
description: Šiame straipsnyje aiškinama, kaip skelbti išlaidų ataskaitas.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524880"
---
# <a name="post-expense-reports"></a>Išlaidų ataskaitų publikavimas

Kai išlaidų ataskaita buvo patvirtinta ir perkelta į bendrąjį žurnalą, ją galima paskelbti. Kai registruojate išlaidų ataskaitą, nustatomos išlaidos, atitinkančios pridėtinės vertės mokesčio (PVM) susigrąžinimo reikalavimus. PVM mokėjimų tikrinimo ir susigrąžinimo užduotis priskiriama darbuotojui, atsakingam už išlaidų ataskaitos tikrinimą.

Jei išlaidų ataskaitoje išlaidos priskirtos kitai įmonei, o ne darbuotoją įdarbinusiai įmonei, turite patikrinti ir įmonę, kuriai reikia sumokėti išlaidas, ir įmonę, iš kurios jos turi būti sumokėtos. Pavyzdžiui, darbuotojas, kuris pateikė išlaidų ataskaitą, dirba DAT bendrovėje, bet išlaidos skirtos DIR bendrovei. Tokiu atveju DAT yra įmonė, kuriai reikia sumokėti išlaidas, o DIR yra įmonė, iš kurios reikia sumokėti. Patvirtinę šias žurnalo eilutes, galite užregistruoti išlaidų eilutes didžiojoje knygoje.

Norėdami užregistruoti išlaidų ataskaitą puslapyje **Patvirtintos išlaidų ataskaitos** pažymėkite išlaidų ataskaitą, tada veiksmų srityje pasirinkite **Paskelbti**.

Tuo pačiu metu galite paskelbti visas sąrašo išlaidų ataskaitas. Pažymėkite visas išlaidų ataskaitas, tada pasirinkite **Paskelbti**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Funkcijos Galimybė skelbti išlaidų įsipareigojimus tiekėjo valiuta naudojant mokėjimo grynaisiais pinigais būdą įjungimas

Funkcija **Galimybė skelbti išlaidų įsipareigojimus tiekėjo valiuta naudojant mokėjimo grynaisiais pinigais būdą** leidžia išlaidų ataskaitas skelbti tiekėjo valiuta, kai naudojamas mokėjimo grynaisiais pinigais būdas.

Dabar, kai pateikiate grynųjų pinigų išlaidas, išlaidų ataskaitos skelbiamos apskaitos valiuta. Dėl sumos konvertavimo, naudojant operacijos valiutą, apskaitos valiutą ir tiekėjo valiutą, tiekėjams sumokama neteisinga suma, jei išlaidų operacijos dieną ir faktinio mokėjimo dieną būna skirtingi valiutų kursai.

Ši funkcija užtikrins, kad skelbiant išlaidų ataskaitą tiekėjo balansas būtų įrašytas tiekėjo valiuta.

1. Eikite į **Darbo sritys**\>**Funkcijų tvarkymas**.
2. Sąraše raskite ir pasirinkite **Galimybė skelbti išlaidų įsipareigojimus tiekėjo valiuta naudojant mokėjimo grynaisiais pinigais būdą**, tada pasirinkite **Įjungti dabar**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
