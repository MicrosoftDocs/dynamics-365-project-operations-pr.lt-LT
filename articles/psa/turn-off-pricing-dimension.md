---
title: Kainodaros dimensijos išjungimas
description: Šioje temoje aprašyta, kaip nustatyti kainodaros dimensijas naudojant sprendimą „Project Service“.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080921"
---
# <a name="turn-off-a-pricing-dimension"></a>Kainodaros dimensijos išjungimas

Kas kelerius metus gali reikėti peržiūrėti ir atnaujinti savo kainodaros strategiją. Dėl bet kokių atliktų atnaujinimų gali reikėti išjungti esamą kainodaros dimensiją ir sukurti naują. Pavyzdžiui, galbūt anksčiau kainą nustatėte pagal **Vaidmenį** , tačiau dabar nusprendėte kainą nustatyti pagal **Darbo patirtį**. Tam gali reikėti išjungti **Vaidmenį** kaip kainodaros dimensiją ir sukurti **Darbo patirtį** kaip naują kainodaros dimensiją. 

Kainodaros dimensiją, neatsižvelgiant į tai, ar ji yra iš anksto nustatyta, ar pasirinktinė, galima išjungti kainodaros dimensijos laukus **Taikomai savikainai** ir **Taikoma pardavimui** nustačius kaip **Ne**.

Tačiau tai padarius gali būti parodytas toliau pateiktas klaidos pranešimas.

![Išjungus kainodaros dimensiją gali įvykti veiklos proceso klaida](media/Business-Process-Error.png)


Šis klaidos pranešimas rodo, kad yra kainų įrašų, kurie prieš tai buvo nustatyti dimensijai, kuri išjungiama. Reikia panaikinti visus dimensiją nurodančius įrašus **Vaidmens kaina** ir **Vaidmens kainos antkainis** , o tik tada dimensijos taikymą galima nustatyti kaip **Ne**. Ši taisyklė taikoma ir iš anksto nustatytoms kainodaros dimensijoms, ir bet kurioms jūsų sukurtoms pasirinktinėms kainodaros dimensijoms. Šio tikrinimo priežastis yra ta, kad „Project Service“ taikomas apribojimas, kad kiekvienas įrašas **Vaidmens kaina** turi turėti unikalų dimensijų derinį. Pavyzdžiui, kainų sąraše, pavadintame **JAV išlaidų tarifai 2018** , yra šios **Vaidmens kainos** eilutės. 

| Standartinis pavadinimas         | Org. vienetas    |Vienetas   |Kaina  |Valiuta  |
| -----------------------|-------------|-------|-------|----------|
| Sistemos inžinierius|„Danys“, JAV|Hour| 100|USD|
| Vyresnysis sistemos inžinierius|„Danys“, JAV|Hour| 150| USD|


Kai **Standartinį pavadinimą** išjungsite kaip kainodaros dimensiją, o „Project Service“ kainodaros sistema ieškos kainos, iš įvesties konteksto ji naudos tik reikšmę **Org. vienetas**. Jei įvesties konteksto **Org. vienetas** yra „Danys JAV“, rezultatas bus nedeterminuotas, nes abi eilutės sutaps. Kad būtų išvengta tokio scenarijaus, kai kuriate įrašus **Vaidmens kaina** „Project Service“ patikrina, ar dimensijų derinys yra unikalus. Jei sukūrus **Vaidmens kainos** įrašus dimensija išjungiama, šis apribojimas gali būti pažeistas. Todėl prieš išjungiant dimensiją reikia panaikinti visas **Vaidmens kainos** ir **Vaidmens kainos antkainio** eilutes, kuriose yra ta dimensijos reikšmė.
