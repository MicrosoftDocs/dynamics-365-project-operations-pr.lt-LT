---
title: SF išrašymo proceso apžvalga
description: Šiame straipsnyje pateikiama sf išrašymo projekto operacijose, skirta iš išteklių / nekauptų scenarijų, proceso apžvalga.
author: sigitac
ms.date: 01/29/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6b285a88be14a5972e9a4604713d7d35a3a442b6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923106"
---
# <a name="invoicing-process-overview"></a>SF išrašymo proceso apžvalga

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

„Project Operations“, skirtas išteklių / nelaikomų medžiagų scenarijams, teikia išsamių galimybių, pritaikytų projekto vadovo ir gautinų sumų tarnautojo / projekto apskaitininko poreikiams. SF išrašymo proceso atveju projekto vadovas valdo projektų atsiskaitymo nebaigtas užduotis, o gautinų sumų tarnautojas / projekto apskaitininkas sukuria suderinamą ir tikslų kliento sąskaitų faktūrų dokumentą.

![SF išrašymo srauto diagrama.](./media/invoicing-flow.png)

Projekto sutarties eilutė apibrėžia susietų projekto operacijų sąskaitų išrašymo būdą. Kai projekto vadovas patvirtina laiko ir išlaidų operacijas, sistema įrašo operacijas objekte **Projekto faktinės** aplinkybės ir siunčia informaciją į **Dynamics 365 Finance projektų valdymo ir apskaitos** modulį. Tada projekto apskaitininkas peržiūri ir užregistruoja įrašus naudodamas [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md). Šiame žurnale pateikiama svarbi projekto faktinių duomenų apskaitos informacija, pvz., atsiskaitymas, PVM grupė, atsiskaitymo prekių PVM grupė ir finansinės dimensijos.

Projekto vadovas gali peržiūrėti pardavimų, už kuriuos neišrašyta sąskaita, operacijas naudodamas laiko ir medžiagų atsiskaitymo būdą nueidamas į [Laiko ir medžiagų atsiskaitymo nebaigtas užduotis](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) ir fiksuotos kainos atsiskaitymo būdą nueidamas į [Fiksuotos kainos etapus](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Šie rodiniai leidžia filtruoti ir pasirinkti operacijas, kurias reikia įtraukti į kitą atsiskaitymo ciklą, o tada pažymėti jas kaip **Parengta išrašyti sąskaitą faktūrą**.

Galite [rankiniu būdu sukurti išankstinę sąskaitą faktūrą](../proforma-invoicing/create-manual-proforma-invoice.md) arba naudoti [periodinį procesą](../proforma-invoicing/configure-automated-invoice-creation.md). Projekto vadovas gali prireikus [koreguoti juodraščio sąskaitos faktūros juodraštį](../proforma-invoicing/manage-proforma-invoice.md), o tada ją patvirtinti.

Patvirtinta išankstinė sąskaita faktūra nusiunčiama į „Finansų“ modulį **Projekto valdymas ir apskaita**. Projekto apskaitininkas formatuoja ir atnaujina projekto SF pasiūlymą, o tada užregistruoja ir spausdina dokumentą. Užregistruotos projekto sąskaitos faktūros įrašomos didžiojoje knygoje, taip pat papildomose klientų ir projektų knygose.


[!INCLUDE[footer-include](../includes/footer-banner.md)]