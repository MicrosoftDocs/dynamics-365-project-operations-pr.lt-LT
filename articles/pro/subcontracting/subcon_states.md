---
title: Valstybės perėjimai į subrangos sutartis projekto operacijose
description: Šioje temoje paaiškinami "Microsoft" subrangos būsenos Dynamics 365 Project Operations perėjimai, kai subranga sukuriama, vykdoma ir uždaroma.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4ca658440c7a9b29a927098f24c092d72d9eb0c9
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903057"
---
# <a name="state-transitions-on-a-subcontract-in-project-operations"></a>Valstybės perėjimai į subrangos sutartis projekto operacijose

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šioje temoje paaiškinami "Microsoft" subrangos būsenos perėjimai Dynamics 365 Project Operations. Kiekviena būsena pateikiama kaip juodraštis, patvirtintas, uždarytas arba atšauktas. Toliau pateiktas vaizdas atspindi valstybės perėjimus.

![Subrangos būsenos modelis](../media/SubconStates.png)  

Šioje lentelėje pateikiamas aprašymas, ką kiekviena būsena nurodo projekto operacijų subrangos gyvavimo cikle.

| Rajonas | Aprašą | Leidžiami perėjimai |
| --- | --- | --- |
| Juodraštis | Tai yra pradinė subrangos būsena. Vyksta derybos su pardavėju. Linijos ir kainodara gali būti keičiamos. Subrangos sutartis šioje valstybėje gali būti naudojama įvertinti ir personalo projekto reikalavimus ištekliams ir medžiagoms. Jis taip pat gali būti nurodytas apie projekto laiką, išlaidas ir medžiagų naudojimą. Subrangos sutartis šioje būsenoje gali būti redaguojama ir panaikinta. | Patvirtinta |
| Patvirtinta | Tai yra subrangos etapas po to, kai bus baigtos derybos su tiekėju dėl kainos ir perkamų linijinių prekių. Tačiau faktinis medžiagų tiekimas ir (arba) darbas subrangos ištekliais vis dar vyksta. Subrangos sutartis šioje valstybėje gali būti naudojama įvertinti ir personalo projekto reikalavimus ištekliams ir medžiagoms. Jis taip pat gali būti nurodytas apie projekto laiką, išlaidas ir medžiagų naudojimą. Šios būsenos subrangos negalima redaguoti ar panaikinti. **Mygtukas Atšaukti** leidžia atšaukti patvirtintą subrangovą. **Mygtukas Iš naujo atidaryti** leidžia iš naujo atidaryti subrangą, kad ji vėl būtų grąžinta į **juodraščio** būseną. Norėdami **uždaryti** patvirtintą subrangovą, naudokite mygtuką Uždaryti. | Uždaryta <br> Atšauktos <br> Juodraštis |
| Uždaryta | Tai yra subrangos etapas, kai baigiamas faktinis medžiagų pristatymas ir (arba) darbas subrangos ištekliais. Subrangos sutartis šioje valstybėje nebegali būti naudojama įvertinti ir personalo projekto reikalavimus ištekliams ir medžiagoms. Be to, jo nebegalima nurodyti apie projekto laiką, išlaidas ir medžiagų naudojimą. Šios būsenos subrangos negalima redaguoti ar panaikinti. | Joks |
| Atšauktos | Tai yra subrangos etapas, kai nebereikia faktinio medžiagų pristatymo ir (arba) darbo subrangos ištekliais. Šios būsenos subrangos sutartis negali būti naudojama įvertinti ir personalo projekto poreikiams ištekliams ir medžiagoms įvertinti, taip pat negalima nurodyti projekto laiko, išlaidų ir medžiagų naudojimo. Šios būsenos subrangos negalima redaguoti ar panaikinti. | Joks |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
