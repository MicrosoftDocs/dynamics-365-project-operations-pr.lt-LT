---
title: Subrangos būsenos perėjimai
description: Šiame straipsnyje paaiškinami būsenos perėjimai pagal subrangos sutartį programoje "Microsoft" Dynamics 365 Project Operations, kai sukuriama, vykdoma ir uždaroma subrangos sutartis.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522941"
---
# <a name="state-transitions-on-a-subcontract"></a>Subrangos būsenos perėjimai 

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Šiame straipsnyje paaiškinami būsenos perėjimai subrangoje programoje "Microsoft" Dynamics 365 Project Operations. Kiekviena valstija pateikiama kaip juodraštis, patvirtinama, uždaroma arba atšaukiama. Šis vaizdas atspindi būsenos perėjimus.

![Subrangos būsenos modelis](../media/SubconStates.png)  

Šioje lentelėje pateikiamas aprašymas, ką kiekviena būsena reiškia subrangos ciklo programoje "Project Operations".

| Rajonas | Aprašą | Leidžiami perėjimai |
| --- | --- | --- |
| Juodraštis | Tai rodo pradinę subrangos sutarties būseną. Vyksta derybos su pardavėju. Linijos ir kainodara gali būti keičiamos. Šios būklės subrangos sutartis gali būti naudojama išteklių ir medžiagų projekto poreikiams įvertinti ir darbuotojų projektams. Jis taip pat gali būti nurodytas pagal laiką, išlaidas ir medžiagų naudojimą projekte. Šios būsenos subrangos sutartis gali būti redaguojama ir ištrinama. | Patvirtinta |
| Patvirtinta | Tai yra subrangos etapas po to, kai derybos su pardavėju dėl kainų nustatymo ir perkamų prekių linijų kainos yra baigtos. Tačiau faktinis medžiagų pristatymas ir (arba) darbas pagal subrangos sutartis sudarytais ištekliais vis dar vyksta. Šios būklės subrangos sutartis gali būti naudojama išteklių ir medžiagų projekto poreikiams įvertinti ir darbuotojų projektams. Jis taip pat gali būti nurodytas pagal laiką, išlaidas ir medžiagų naudojimą projekte. Šios būsenos subrangos sutartis negali būti redaguojama ar ištrinama. Mygtukas **Atšaukti** leidžia atšaukti patvirtintą subrangos sutartį. Mygtukas **Iš naujo atidaryti** leidžia iš naujo atidaryti subrangos sutartį, kad ji vėl būtų įtraukta į **juodraščio** būseną. Naudokite mygtuką **Uždaryti**, kad uždarytumėte patvirtintą subrangos sutartį. | Uždaryta <br> Atšauktos <br> Juodraštis |
| Uždaryta | Tai yra subrangos etapas, kai baigiamas faktinis medžiagų pristatymas ir (arba) darbas subrangos būdu iš subrangovų išteklių. Subrangos sutartis šioje būsenoje nebegali būti naudojama išteklių ir medžiagų išteklių ir medžiagų projektų reikalavimams įvertinti ir darbuotojų projektams. Be to, jo nebegalima nurodyti laiku, išlaidomis ir medžiagų naudojimu projekte. Šios būsenos subrangos sutartis negali būti redaguojama ar ištrinama. | Joks |
| Atšauktos | Tai yra subrangos etapas, kai nebereikia faktinio medžiagų pristatymo ir (arba) darbo naudojant subrangos išteklius. Šios būsenos subrangos sutartis negali būti naudojama išteklių ir medžiagų projekto poreikiams įvertinti ir darbuotojų projektams, taip pat negalima nurodyti laiko, išlaidų ir medžiagų panaudojimo projekte. Šios būsenos subrangos sutartis negali būti redaguojama ar ištrinama. | Joks |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
