---
title: Išteklių suderinimo apžvalga
description: Šioje temoje pateikiama informacija apie išteklių rezervavimų ir priskyrimų projektams sulygiavimo užtikrinimą.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1b60ed9d15f51ff01f27bcc231f5db27513a838f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897461"
---
# <a name="resource-reconciliation-overview"></a>Išteklių suderinimo apžvalga

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Komandos nariams rezervavimai ir priskyrimai yra laisvai susiję. Kitaip tariant, ištekliai gali turėti priskyrimų, bet ne rezervavimų, arba jie gali turėti rezervavimų, bet ne priskyrimų. Geriausiu atveju rezervavimai ir priskyrimai turėtų būti suderinti, kad ištekliai turėtų patvirtintą pajėgumą užduočių priskyrimams atlikti. Tačiau rezervavimai gali būti pagrįsti prieinamumu, o užduoties laikas gali keistis projektui tęsiantis. Todėl laisvas rezervavimų ir priskyrimų siejimas suteikia lankstumą.

Skirtuke **Derinimas**, esančiame formoje **Projektas**, projekto vadovai gali suderinti komandos narių rezervavimus ir jų priskyrimus prie projekto komandų.

Skirtuke **Derinimas** taip pat rodomi rezervavimai ir priskyrimai iki atskiro kiekvieno komandos nario užduoties priskyrimo lygio. Valandos rodomos langeliuose, kurie nurodo laikotarpius nuo mėnesių iki dienų.

Skirtuke taip pat rodoma bendra grynoji projekto suma kartu su stulpeliu **Iš viso**.

Kiekvienam ištekliui skirtukas apskaičiuoja skirtumą tarp komandos narių rezervavimų ir komandos nario užduočių priskyrimo apibendrinamosios reikšmės. Geriausiu atveju šis skirtumas turi būti 0 (nulis). Kitaip tariant, tarp rezervavimų ir priskyrimų neturėtų būti skirtumo. Skirtumai nuspalvinami ir nušešėliuojami, kad atkreiptų dėmesį į dvi sąlygas:

- **Rezervavimo trūkumas** – rezervavimo trūkumas atsiranda, kai išteklius turi daugiau priskyrimų nei rezervavimų. Kadangi šis pajėgumas nebuvo rezervuotas, projektų vadovas gali pataisyti šią sąlygą išplėsdamas ištekliaus rezervavimus, kad padengtų trūkumą.
- **Užsakymų perteklius** – užsakymų perteklius įvyksta, kai ištekliai buvo rezervuoti projektui, tačiau nebuvo priskirti užduotims. Ši sąlyga gali būti priimtina tais atvejais, kai išteklius buvo užrezervuotas projektui prieš užduoties priskyrimą. Tačiau kitais atvejais išteklius neplanuojamas priskirti užduotims. Tokiais atvejais projektų vadovas turėtų apsvarstyti išteklių rezervavimo atšaukimą, kad pajėgumą būtų galima naudoti kitam projektui.

Kai kuriais atvejais, peržiūrint laiką aukštesniame nei dienos lygyje (pavyzdžiui, mėnesio lygyje), galite matyti ištekliaus grynąjį nulio skirtumą (kitaip tariant, rezervavimai = priskyrimai). Tačiau, jei peržiūrite laiką savaitės lygyje, galite matyti nulio valandų priskyrimus ir 40 valandų rezervavimus pirmoje savaitėje, tačiau 40 valandų priskyrimus ir nulio valandų rezervavimus antroje savaitėje. Apskritai rezervavimai ir priskyrimai yra suderinami, tačiau kiekvieną savaitę jie skiriasi.

Peržiūrint laiką aukštesniuose lygiuose, langeliai, esantys skirtuke **Derinimas**, turi indikatorių, kuris praneša, kad žemesniuose lygiuose yra skirtumų. Dukart spustelėję langelį galite priartinti ir peržiūrėti skirtumą. Tada galite spustelėti dešiniuoju pelės mygtuku ir nutolinti. Pažymėdami išteklių, o tada naudodami valdiklį **Kitas skirtumas**, esantį tinklelio įrankių juostoje, galite eiti į kitą skirtumą tarp šio ištekliaus rezervavimų ir priskyrimų. Tada galite naudoti valdiklį **Ankstesnis skirtumas**, kad grįžtumėte atgal. Taip pat galite išjungti skirtumo indikatorių ir naršymą **Parametruose**.


Jei turite ištekliaus užduoties priskyrimus, bet ne rezervavimus, puslapio **Projektai** skirtuke **Derinimas** pažymėkite rezervavimo trūkumą, o tada pasirinkite **Išplėsti rezervavimą**. Atsiranda dialogo langas **Išplėsti rezervavimą** ir rodomas rezervavimas, reikalingas ištekliaus trūkumui spręsti. Jame taip pat nurodomi esami ištekliaus rezervavimai visuose projektuose arba kituose planiniuose objektuose. Jei pasirinksite **Gerai**, kad sukurtumėte ištekliaus rezervavimą, neatsižvelgiant į ištekliaus pasiekiamumą, galite viršyti rezervavimo limitą.

Projektų vadovas arba išteklių vadovas gali naudoti grafiko lentą, kad valdytų situacijas, kai išteklius rezervuojamas per daug nepaisant jo pajėgumo.

