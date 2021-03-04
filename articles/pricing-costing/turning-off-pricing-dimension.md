---
title: Kainodaros dimensijos išjungimas
description: Šioje temoje pateikiama informacija apie tai, kaip išjungti kainodaros dimensijas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650059"
---
# <a name="turning-off-a-pricing-dimension"></a>Kainodaros dimensijos išjungimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Kas kelerius metus gali reikėti peržiūrėti ir atnaujinti savo kainodaros strategiją. Dėl bet kokių atliktų atnaujinimų gali reikėti išjungti esamą kainodaros dimensiją ir sukurti naują. Pavyzdžiui, galbūt anksčiau kainą nustatėte pagal **Vaidmenį**, tačiau dabar nusprendėte kainą nustatyti pagal **Darbo patirtį**. Tam gali reikėti išjungti **Vaidmenį** kaip kainodaros dimensiją ir sukurti **Darbo patirtį** kaip naują kainodaros dimensiją. 

Kainodaros dimensiją, neatsižvelgiant į tai, ar ji yra iš anksto nustatyta, ar pasirinktinė, galima išjungti kainodaros dimensijos laukus **Taikomai savikainai** ir **Taikoma pardavimui** nustačius kaip **Ne**.

Tačiau, kai tai padarysite, gali būti parodytas klaidos pranešimas **Kainodaros dimensija negalima atnaujinti arba panaikinti, jei yra susietųjų kainų įrašai.**

![Išjungus kainodaros dimensiją gali įvykti veiklos proceso klaida](media/Business-Process-Error.png)

Šis klaidos pranešimas rodo, kad yra kainų įrašų, kurie prieš tai buvo nustatyti dimensijai, kuri išjungiama. Reikia panaikinti visus dimensiją nurodančius įrašus **Vaidmens kaina** ir **Vaidmens kainos antkainis**, o tik tada dimensijos taikymą galima nustatyti kaip **Ne**. Ši taisyklė taikoma ir iš anksto nustatytoms kainodaros dimensijoms, ir bet kurioms jūsų sukurtoms pasirinktinėms kainodaros dimensijoms. Šio tikrinimo priežastis yra ta, kad kiekvienas įrašas **Vaidmens kaina** turi turėti unikalų dimensijų derinį. Pavyzdžiui, kainų sąraše, pavadintame **JAV išlaidų tarifai 2018**, yra šios **Vaidmens kainos** eilutės. 

| Standartinis pavadinimas         | Org. vienetas    |Vienetas   |Kaina  |Valiuta  |
| -----------------------|-------------|-------|-------|----------|
| Sistemos inžinierius|„Danys“, JAV|Hour| 100|USD|
| Vyresnysis sistemos inžinierius|„Danys“, JAV|Hour| 150| USD|


Kai **Standartinį pavadinimą** išjungsite kaip kainodaros dimensiją, o kainodaros modulis ieškos kainos, iš įvesties konteksto ji naudos tik reikšmę **Org. vienetas**. Jei įvesties konteksto **Org. vienetas** yra „Danys JAV“, rezultatas bus nedeterminuotas, nes abi eilutės sutaps. Kad būtų išvengta tokio scenarijaus, kai kuriate įrašus **Vaidmens kaina** sistema tikrina, ar dimensijų derinys yra unikalus. Jei sukūrus **Vaidmens kainos** įrašus dimensija išjungiama, šis apribojimas gali būti pažeistas. Todėl prieš išjungiant dimensiją reikia panaikinti visas **Vaidmens kainos** ir **Vaidmens kainos antkainio** eilutes, kuriose yra ta dimensijos reikšmė.


[!INCLUDE[footer-include](../includes/footer-banner.md)]