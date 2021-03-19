---
title: Išteklių naudingumo apžvalga
description: Šioje temoje pateikiama informacija apie išteklių naudojimą „Project Operations”.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d66b5fc642ef53adf1169ce891a7a5fa26b07d6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279328"
---
# <a name="resource-utilization-overview"></a>Išteklių naudingumo apžvalga

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Ištekliai gali turėti tikslinį apmokėtiną naudojimą. Šis tikslinis naudojimas apibrėžiamas kaip atributas išteklių numatytame vaidmenyje arba nustatomas atskiro rezervuojamo ištekliaus įraše. Naudojimo skaičiavimai pagrįsti faktinėmis valandomis, apie kurias ištekliai pranešė naudodami patvirtintus laiko įrašus.

Naudojimo skaičiavimui naudojamos toliau nurodytos formulės.

  - Apmokėtinas naudojimas = apmokestinamos faktinės valandos ÷ išteklių pajėgumas
  - Neapmokėtinas naudojimas = faktinis laikas su apmokėtino tipo ID = neapmokestinamas, papildomas arba negalimas ÷ išteklių pajėgumas
  - Vidinis = faktinis laikas be pardavimo sutarties ÷ išteklių pajėgumas
  - Išteklių pajėgumas = išteklių darbo valandos – išvykęs – ne darbo dienos

Rodinį **Išteklių naudojimas** galite rasti skyde **Ištekliai**.

Kiekvienas tinklelio langelis nurodo išteklių apmokėtiną naudojimą pagal laiką, pavyzdžiui, dieną, savaitę arba mėnesį. Langeliams naudojamos toliau nurodytos spalvos.

  - **Žalia**: apmokėtinas naudojimas > = tikslinis išteklių naudojimas
  - **Geltona**: tikslinis naudojimas – 20 < = apmokėtinas naudojimas < tikslinis naudojimas
  - **Raudona**: apmokėtinas naudojimas < = tikslinis naudojimas – 20

Kadangi rodinys **Išteklių naudojimas** pagrįstas grafiko lenta, galite naudoti grafiko lentos filtravimo galimybes, kad filtruotumėte rezultatus.

Reikia, kad tinkleliui nustatytumėte tikslinį naudojimą arba pagal vaidmenį, arba individualų išteklių. Norėdami atlikti tokius nustatymus, eikite į **Ištekliai** > **Išteklių vaidmenys**.

Be to, kiekvienam rezervuojamam ištekliui reikia priskirti numatytąjį vaidmenį. Eikite į **Ištekliai** > **Ištekliai**. Skirtuke **„Project Service”** patikrinkite, kad nustatytas išteklių vaidmuo ir kad laukas **Yra numatytasis** nustatytas kaip **Taip**. Galite įtraukti papildomų vaidmenų, kai **Kaip numatytasis**  = **Ne**. Vaidmuo, kai **Yra numatytasis**  = **Taip**, naudojamas išteklių naudojimui įvertinti pagal to vaidmens tikslą.

Skirtuke **Project Service** taip pat galite ištekliui nustatyti individualų tikslinį naudojimą. Tada naudojimo skaičiavimui naudojamas šis tikslinis naudojamas, kad būtų įvertintas išteklių tikslas, o ne išteklių numatytojo vaidmens tikslas.

Išteklių naudojimas rodomas, tik jei šis išteklius turi patvirtintą ir apmokestinamą laiką periode, kuris rodomas tinklelyje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]