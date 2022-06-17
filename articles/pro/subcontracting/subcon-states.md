---
title: Subrangos būsenos perėjimai
description: Šiame straipsnyje paaiškinami "Microsoft" Dynamics 365 Project Operations subrangos sutarties būsenos perėjimai, kai subrangos sutartis sukuriama, vykdoma ir uždaroma.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919748"
---
# <a name="state-transitions-on-a-subcontract"></a>Subrangos būsenos perėjimai 

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šiame straipsnyje paaiškinami "Microsoft" subrangos sutarties būsenos perėjimai Dynamics 365 Project Operations. Kiekviena valstybė pateikiama kaip projektas, patvirtintas, uždarytas arba atšauktas. Toliau pateiktas vaizdas atspindi valstybės perėjimus.

![Subrangos būsenos modelis](../media/SubconStates.png)  

Šioje lentelėje pateikiamas aprašymas, ką kiekviena valstybė atstovauja projekto operacijų subrangos sutarties gyvavimo cikle.

| Rajonas | Aprašą | Leidžiami perėjimai |
| --- | --- | --- |
| Juodraštis | Tai yra pradinė subrangos sutarties būsena. Šiuo metu vyksta derybos su pardavėju. Eilutės ir kainodara gali būti keičiamos. Subrangos sutartis šioje valstybėje gali būti naudojama įvertinti ir personalo projekto reikalavimus ištekliams ir medžiagoms. Jis taip pat gali būti nurodomas laiku, išlaidomis ir medžiagų naudojimu projekte. Šios būsenos subrangos sutartį galima redaguoti ir panaikinti. | Patvirtinta |
| Patvirtinta | Tai yra subrangos sutarties etapas po to, kai derybos su tiekėju dėl kainodaros ir perkamų eilutės prekių yra baigtos. Tačiau faktinis medžiagų tiekimas ir (arba) darbas subrangovų ištekliais vis dar vyksta. Subrangos sutartis šioje valstybėje gali būti naudojama įvertinti ir personalo projekto reikalavimus ištekliams ir medžiagoms. Jis taip pat gali būti nurodomas laiku, išlaidomis ir medžiagų naudojimu projekte. Šios būsenos subrangos sutarties redaguoti ar panaikinti negalima. Mygtukas **Atšaukti** leidžia atšaukti patvirtintą subrangos sutartį. Mygtukas **Iš naujo atidaryti** leidžia iš naujo atidaryti subrangos sutartį, kad ji vėl **taptų juodraščio** būsena. **Norėdami uždaryti patvirtintą subrangos sutartį, naudokite mygtuką Uždaryti**. | Uždaryta <br> Atšauktos <br> Juodraštis |
| Uždaryta | Tai yra subrangos sutarties etapas, kai faktinis medžiagų pristatymas ir (arba) darbas subrangos ištekliais yra baigtas. Subrangos sutartis šioje valstybėje nebegali būti naudojama išteklių ir medžiagų reikalavimų vertinimui ir personalo projektų reikalavimams įvertinti. Be to, jo nebegalima nurodyti laiku, išlaidomis ir medžiagų naudojimu projekte. Šios būsenos subrangos sutarties redaguoti ar panaikinti negalima. | Joks |
| Atšauktos | Tai yra subrangos sutarties etapas, kai faktinis medžiagų pristatymas ir (arba) darbas subrangos ištekliais nebereikalingas. Šios būsenos subrangos sutartis negali būti naudojama išteklių ir medžiagų reikalavimų įvertinimui ir personalo projekto reikalavimams įvertinti, taip pat negalima nurodyti projekto laiko, išlaidų ir medžiagų naudojimo. Šios būsenos subrangos sutarties redaguoti ar panaikinti negalima. | Joks |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
