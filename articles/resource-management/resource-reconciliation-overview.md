---
title: Išteklių suderinimo apžvalga
description: Šioje temoje pateikiama informacija, kuri padės užtikrinti, kad projektų išteklių rezervavimai ir priskyrimai būtų suderinti.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 5c48589e745dbf6e3a51ae749b9b45491d26406e
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368216"
---
# <a name="resource-reconciliation-overview"></a>Išteklių suderinimo apžvalga

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Komandos nariams rezervavimai ir priskyrimai yra laisvai susiję. Kitaip tariant, ištekliai gali turėti priskyrimų ir neturėti rezervavimų, arba jie gali turėti rezervavimų ir neturėti priskyrimų. Geriausiu atveju rezervavimai ir priskyrimai turėtų būti suderinti, kad ištekliai turėtų patvirtintą pajėgumą užduočių priskyrimams atlikti. Tačiau rezervavimai gali būti pagrįsti prieinamumu, o užduoties laikas gali keistis projektui tęsiantis. Todėl laisvas rezervavimų ir priskyrimų siejimas suteikia lankstumą.

Puslapio **Projektai** skirtuke **Derinimas** projekto vadovai gali derinti komandos narių rezervavimus ir jų priskyrimus projekto komandoms.

Skirtuke **Derinimas** rodomi rezervavimai ir priskyrimai iki atskiro kiekvieno komandos nario užduoties priskyrimo lygio. Jame rodomos valandos langeliuose, kurie gali nurodyti laikotarpius nuo mėnesių iki dienų. Skirtuke taip pat rodoma bendra grynoji projekto suma kartu su stulpeliu **Iš viso**.

Kiekvienam ištekliui skirtukas **Derinimas** apskaičiuoja skirtumą tarp komandos narių rezervavimų ir tos komandos nario užduočių priskyrimo apibendrinamosios reikšmės. Geriausiu atveju šis skirtumas turi būti 0 (nulis). Kitaip tariant, tarp rezervavimų ir priskyrimų neturėtų būti skirtumo. Skirtumai nuspalvinami ir nušešėliuojami, kad atkreiptų dėmesį į dvi sąlygas:

- **Rezervavimo trūkumas** – rezervavimo trūkumas atsiranda, kai išteklius turi daugiau priskyrimų nei rezervavimų. Kadangi šis pajėgumas nebuvo rezervuotas, projektų vadovas gali pataisyti šią sąlygą išplėsdamas ištekliaus rezervavimus, kad padengtų trūkumą.
- **Užsakymų perteklius** – užsakymų perteklius įvyksta, kai ištekliai buvo rezervuoti projektui, tačiau nebuvo priskirti užduotims. Ši sąlyga gali būti priimtina tais atvejais, kai išteklius buvo užrezervuotas projektui prieš užduoties priskyrimą. Tačiau kitais atvejais, kai ištekliaus neplanuojama priskirti užduotims, projekto vadovas turėtų nuspręsti atšaukti ištekliaus rezervavimus. Tokiu būdu pajėgumą galima naudoti kitam projektui.

Kai kuriais atvejais, peržiūrint laiką aukštesniame nei dienos lygyje (pavyzdžiui, mėnesio lygyje), galite matyti ištekliaus grynąjį nulio skirtumą (kitaip tariant, rezervavimai yra lygus priskyrimams). Tačiau, jei peržiūrite laiką savaitės lygyje, galite matyti nulio valandų priskyrimus ir 40 valandų rezervavimus pirmoje savaitėje, tačiau 40 valandų priskyrimus ir nulio valandų rezervavimus antroje savaitėje. Apskritai rezervavimai ir priskyrimai yra suderinami, tačiau kiekvieną savaitę jie skiriasi.

Peržiūrint laiką aukštesniuose lygiuose, langeliai, esantys skirtuke **Derinimas**, turi indikatorių, kuris praneša, kad žemesniuose lygiuose yra skirtumų. Dukart bakstelėję ar spustelėję langelį galite priartinti ir peržiūrėti skirtumą. Tada galite pasirinkti ir laikydami nuspaudus (arba spustelėjus dešiniuoju pelės mygtuku) nutolinti. Pažymėdami išteklių, o tada naudodami valdiklį **Kitas skirtumas**, esantį tinklelio įrankių juostoje, galite eiti į kitą skirtumą tarp šio ištekliaus rezervavimų ir priskyrimų. Tada galite naudoti valdiklį **Ankstesnis skirtumas**, kad grįžtumėte atgal. Taip pat galite išjungti skirtumo indikatorių ir naršymą **Parametruose**.

Jei turite ištekliaus užduoties priskyrimus, bet ne rezervavimus, puslapio **Projektai** skirtuke **Derinimas** pasirinkite rezervavimo trukūmą, o tada pasirinkite **Išplėsti rezervavimą**. Atsiranda dialogo langas **Išplėsti rezervavimą** ir rodomas rezervavimas, reikalingas ištekliaus trūkumui spręsti. Dialogo lange taip pat nurodomi esami ištekliaus rezervavimai visuose projektuose arba kituose planiniuose objektuose. Jei pasirinksite **Gerai**, kad sukurtumėte ištekliaus rezervavimą, neatsižvelgiant į ištekliaus pasiekiamumą, galite viršyti rezervavimo limitą.

Rezervavimai, sukurti vykdant **Išplėsti rezervavimą** veiksmą, yra susieti su pirminiu projekto reikalavimu. Kai plėtinys inicijuojamas, konkretaus reikalavimo, kurį reikia išplėsti, nustatyti negalima, nes ištekliai gali būti susieti su daugiau nei vienu projekto reikalavimu.

Projekto vadovas arba išteklių vadovas gali naudoti grafiko lentą, kad valdytų situacijas, kai išteklius rezervuojamas per daug nepaisant jo pajėgumo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]