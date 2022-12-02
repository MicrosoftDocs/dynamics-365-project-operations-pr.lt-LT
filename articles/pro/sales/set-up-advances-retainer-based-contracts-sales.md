---
title: Išankstinės arba išankstiniais apmokėjimais pagrįstos sutartys
description: Šiame straipsnyje pateikta informacija apie išankstiniais apmokėjimais pagrįstų sutarčių modelius ir avansus naudojant „Project Operations“.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 201dd1651b12614930f6a2c294156b31deceab0b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932490"
---
# <a name="advances-and-retainer-based-contracts"></a>Išankstinės arba išankstiniais apmokėjimais pagrįstos sutartys


_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ palaiko išankstiniais apmokėjimais pagrįstas sutartis. Išankstiniais apmokėjimais pagrįsta sutartis yra sutartas lygiai paskirstytų mokėjimų, kuriuos klientas turės mokėti tęsiantis projektui, rinkinys. Šio tipo sutartis paprastai naudojama laiku ir medžiagomis arba sąnaudomis pagrįsto atsiskaitymo modeliuose, kai klientui reikia pateikti prognozuojamą sąskaitą faktūrą ir mokėjimo grafiką. Kiekvieną laikotarpį sukauptos faktinės pajamos suderinamos su laikotarpio pradžioje iš kliento gautu mokėjimu. Remiantis atsiskaitymo už laiką ir medžiagas modeliu, kiekvieną laikotarpį sukauptos pajamos gali skirtis atsižvelgiant į patirtas išlaidas. Jei sukauptos pajamos viršija laikotarpio pradžioje gautą sumą, projekto pristatymo įmonė gali:

- Klientui sąskaita faktūra išrašoma tik už perteklių 
- Atidėkite pajamų suderinimą su kitu sąskaitų išrašymo laikotarpiu ir išrašykite vieną galutinę sąskaitą projekto pabaigoje likusioms nesuderintoms pajamoms

Pagrindinis išankstiniais apmokėjimais pagrįstų sutarčių modelio ir pastovios kainos sutarties modelio skirtumas naudojant „Project Operations“ yra tas, kad pastovios kainos sutarties modelyje sąskaitos faktūros suma nėra susieta su patirtomis išlaidomis. Sąskaitos faktūros išrašomos etapais, atsižvelgiant į patirtas to laikotarpio išlaidas. Išankstiniais apmokėjimais pagrįstoje sutartyje pajamos, kurioms galima išrašyti sąskaitą faktūrą, registruojamos remiantis sutarties eilutėje nurodytu atsiskaitymo metodu. Kai atsiskaitymo metodas yra laikas ir medžiaga, pajamos, kurioms išrašomos sąskaitos faktūros, yra susijusios su išlaidomis, patirtomis bet kurį pateiktą laikotarpį; jos skirtingais laikotarpiais gali skirtis. Tačiau klientui sąskaita faktūra išrašoma tik periodinei išankstinio apmokėjimo sumai. Laikotarpio pabaigoje sistema naudoja kitą sąskaitą faktūrą, kad suderintų laikotarpio metu užregistruotas pajamas, kurioms reikia išrašyti sąskaitą faktūrą, su suma, kuriai laikotarpio pradžioje klientui buvo išrašyta sąskaita faktūra.

Šio metodo privalumas yra tas, kad kliento išlaidos tampa nuspėjamos naudojant išankstinio apmokėjimo grafiką, skirtingai nei naudojant įprastą laiko ir medžiagų modelį. Projektą pristatanti organizacija taip pat turi šiek tiek erdvės padengti išlaidų susigrąžinimo riziką, kai padidėja aprėptis, skirtingai nei naudojant pastovios kainos modelį.

Neskaitant periodiniais išankstiniais apmokėjimais pagrįsto grafiko, „Project Operations“ gali registruoti vienkartinį iš kliento gautą avansą ir suderinti su skirtingais projekto išlaidų komponentais.

„Project Operations“ išankstinį apmokėjimą galima naudoti tik tada, kai klientui išrašoma sąskaita faktūra. Tai nurodo toliau papildomame tinklelyje pateikti laukai, skirti avansams ir išankstiniams mokėjimams.

| Laukas | Aprašo | Tolesnis poveikis |
| --- | --- | --- |
| Galima suma | Suma, kurią galima naudoti išankstinio mokėjimo arba avanso įrašui. | Kol neišrašoma avanso arba išankstinio apmokėjimo sąskaita faktūra, jų negalima naudoti; tai reiškia, kad suma yra nulis. |
| Panaudota suma | Suma, kuri jau naudojama išankstiniam mokėjimui arba avansui. | Avansą arba išankstinį mokėjimą sąskaitoje faktūroje galima iš dalies suderinti su faktinėmis išlaidomis, kurios bus pažymėtos, kaip panaudotos. Likusi avanso arba išankstinio mokėjimo suma galės būti suderinta su faktinėmis išlaidomis būsimoje sąskaitoje faktūroje. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]