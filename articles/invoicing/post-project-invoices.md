---
title: SF išrašymo proceso apžvalga
description: Šioje temoje pateikiama SF išrašymo proceso apžvalga naudojant „Project Operations“, skirtą išteklių / nelaikomų medžiagų scenarijams.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9dc424cf69abfccc10bf551272a14e5cefb3dff0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275817"
---
# <a name="invoicing-process-overview"></a>SF išrašymo proceso apžvalga

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

„Project Operations“, skirtas išteklių / nelaikomų medžiagų scenarijams, teikia išsamių galimybių, pritaikytų projekto vadovo ir gautinų sumų tarnautojo / projekto apskaitininko poreikiams. SF išrašymo proceso atveju projekto vadovas valdo projektų atsiskaitymo nebaigtas užduotis, o gautinų sumų tarnautojas / projekto apskaitininkas sukuria suderinamą ir tikslų kliento sąskaitų faktūrų dokumentą.

![SF išrašymo srauto diagrama](./media/invoicing-flow.png)

Projekto sutarties eilutė apibrėžia susietų projekto operacijų sąskaitų išrašymo būdą. Kai projekto vadovas patvirtina laiko ir išlaidų operacijas, sistema įrašo operacijas objekte **Projekto faktiniai duomenys** ir siunčia informaciją į „Dynamics 365 Finance“ modulį **Projekto valdymas ir apskaita**. Tada projekto apskaitininkas peržiūri ir užregistruoja įrašus naudodamas [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md). Šiame žurnale pateikiama svarbi projekto faktinių duomenų apskaitos informacija, pvz., atsiskaitymas, PVM grupė, atsiskaitymo prekių PVM grupė ir finansinės dimensijos.

Projekto vadovas gali peržiūrėti pardavimų, už kuriuos neišrašyta sąskaita, operacijas naudodamas laiko ir medžiagų atsiskaitymo būdą nueidamas į [Laiko ir medžiagų atsiskaitymo nebaigtas užduotis](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) ir fiksuotos kainos atsiskaitymo būdą nueidamas į [Fiksuotos kainos etapus](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Šie rodiniai leidžia filtruoti ir pasirinkti operacijas, kurias reikia įtraukti į kitą atsiskaitymo ciklą, o tada pažymėti jas kaip **Parengta išrašyti sąskaitą faktūrą**.

Galite [rankiniu būdu sukurti išankstinę sąskaitą faktūrą](../proforma-invoicing/create-manual-proforma-invoice.md) arba naudoti [periodinį procesą](../proforma-invoicing/configure-automated-invoice-creation.md). Projekto vadovas gali prireikus [koreguoti juodraščio sąskaitos faktūros juodraštį](../proforma-invoicing/manage-proforma-invoice.md), o tada ją patvirtinti.

Patvirtinta išankstinė sąskaita faktūra nusiunčiama į „Finansų“ modulį **Projekto valdymas ir apskaita**. Projekto apskaitininkas formatuoja ir atnaujina projekto SF pasiūlymą, o tada užregistruoja ir spausdina dokumentą. Užregistruotos projekto sąskaitos faktūros įrašomos didžiojoje knygoje, taip pat papildomose klientų ir projektų knygose.


[!INCLUDE[footer-include](../includes/footer-banner.md)]