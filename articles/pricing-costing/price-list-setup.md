---
title: Kainoraščių nustatymas
description: Šioje temoje pateikta informacija, kaip nustatyti savikainos ir pardavimo kainoraščius.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 578f5641659a5d05785781afe7055fe4449cf799
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088021"
---
# <a name="set-up-price-lists"></a>Kainoraščių nustatymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ esantys kainoraščiai yra tarifų katalogas. Tarifai rodo savikainos, pardavimo ir sąskaitų tarifus. Atsižvelgiant į tai, ar kainoraštis nurodo savikainos tarifus, ar pardavimo ir sąskaitų tarifus, kainoraščio kontekstas yra **Pardavimas** arba **Savikaina**.

Šie plėtiniai yra būdingi „Project Operations“ ir taikomi kainoraščiams iš „Dynamics 365 Sales“.

- **Kontekstas** : šiame lauke yra palaikomos reikšmės **Savikaina** ir **Pardavimas**. Reikšmė **Pirkinys** nepalaikoma. Nustatykite kontekstą į **Savikaina** norėdami sudaryti savikainų sąrašą arba nustatykite kontekstą į **Pardavimas** norėdami pardavimo kainoraščio. Savikainų kainoraščiai nustato savikainos tipo kainą numatomuose ir faktiniuose įrašuose. Pardavimo kainoraščiai nustato kainą pardavimo tipų, kuriems sąskaita neišrašyta ir išrašyta, numatomuose bei faktiniuose įrašuose.
- **Laiko vienetas** : tai yra numatytasis laiko vienetas, kurio kaina nustatyta susijusioje šio kainoraščio **Vaidmens kainos** lentelėje.
- **Kainoraščio objektas** : šis paslėptas laukas priklauso „Project Operations“, kad būtų atskirti kainoraščiai, kurie yra būdingi pasiūlymui arba sutarčiai, nuo standartinių ir visuotinai priimtinų.

## <a name="price-list-header"></a>Kainoraščio antraštė

Šioje lentelėje yra laukai, esantys kainoraščio skirtuke **Bendra** , kurie yra unikalūs „Project Operations“ arba turi reikšmingų veikimo pokyčių, palyginti su „Sales“ kainoraščiais.

| Laukas | Vieta | Atitiktis, tikslas ir gairės | Tolesnis poveikis |
| --- | --- | --- | --- |
| Pavadinimas / vardas, pavardė | Skirtukas **Bendra** ir **Sparčiojo kūrimo** formos | Kainoraščio tapatybė. | Kainoraštis rodomas su šia reikšme visuose sąrašo puslapiuose ir išplečiamosiose parinktyse.|
| Kontekstas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** formos | Šį lauką galima nustatyti į **Savikaina** arba **Pardavimas**. | Kainoraštis, nustatytas į **Savikaina** , naudojamas norint ieškoti numatomos savikainos ir faktinės savikainos. Kainoraštis, nustatytas į **Pardavimas** , naudojamas norint ieškoti numatomos pardavimo kainos ir faktinės pardavimo kainos. Prie klientų, projektų pasiūlymų ir projektų sutarčių kainoraščių galima pridėti tik kainoraščius, kurių kontekstas nustatytas į **Pardavimas**. |
| Pradžios data | Skirtukas **Bendra** ir **Sparčiojo kūrimo** formos | Kainoraščio galiojimo laikotarpio pradžios data. | Naudojant lauką **Pabaigos data** , šis laukas naudojamas norint nustatyti, kuris kainoraštis taikomas tam tikrai numatomai arba faktinei eilutei. |
| Pabaigos data | Skirtukas **Bendra** ir **Sparčiojo kūrimo** formos | Kainoraščio galiojimo laikotarpio pabaigos data. | Naudojant lauką **Pradžios data** , šis laukas naudojamas norint nustatyti, kuris kainoraštis taikomas tam tikrai numatomai arba faktinei eilutei. |
| Valiuta | Skirtukas **Bendra** ir **Sparčiojo kūrimo** formos | Šis laukas naudojamas nustatyti numatytąją valiutą kiekvienoje vaidmens, kategorijos arba kainoraščio elemento eilutėje, susijusioje su šiuo kainoraščiu. | **Pardavimo** kainoraščių, vaidmenų, kategorijų arba kainoraščio elementų eilutes galima sukurti tik šia valiuta. **Savikainos** kainoraščiuose galite sukurti vaidmens kainos eilutę bet kuria valiuta. Čia apibrėžta valiuta naudojama kaip numatytoji. Naudotojo sąranka, kur yra susijusios vaidmens kainos, gali perrašyti šią reikšmę, kad būtų galima nustatyti darbo sąnaudų tarifą bet kuria valiuta. Kategorijos savikainos tarifus ir kainoraščio elemento savikainą galima nustatyti tik čia apibrėžta valiuta. |
| Laiko vienetas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** formos | Šis laukas naudojamas norint nustatyti numatytąjį laiko vienetą kiekvienoje vaidmens eilutėje, susijusioje su šiuo kainoraščiu. | Ši lauko reikšmė naudojama tik susijusiame vaidmens kainos nustatyme. **Savikainos** ir **Pardavimo** kainoraščiuose galite sukurti vaidmens kainos eilutę naudodami bet kokį laiko vienetą. Čia apibrėžtas laiko vienetas naudojamas kaip numatytasis. Su naudotojo sąranka susijusios vaidmens kainos gali perrašyti šią reikšmę, kad būtų galima nustatyti darbo sąnaudų ir sąskaitos tarifą naudojant bet kokį laiko vienetą. |
| Aprašo | Skirtukas **Bendra** ir **Sparčiojo kūrimo** formos | Šiame teksto lauke galite nurodyti keleto eilučių kainoraščio aprašą. | Šis laukas rodomas įvairių objektų, kurie turi susietų kainoraščių, kainoraščių **susietuose** rodiniuose. |
