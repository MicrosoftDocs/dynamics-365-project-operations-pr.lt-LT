---
title: SF išrašymo proceso apžvalga
description: Šioje temoje pateikiama SF išrašymo proceso apžvalga naudojant „Project Operations“, skirtą išteklių / nelaikomų medžiagų scenarijams.
author: sigitac
ms.date: 01/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 804d42f7e8bfd103b9143dc0f5c7ddecdee9e66e6072c3e7bf76b2a8c549cf55
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003781"
---
# <a name="invoicing-process-overview"></a>SF išrašymo proceso apžvalga

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

„Project Operations“, skirtas išteklių / nelaikomų medžiagų scenarijams, teikia išsamių galimybių, pritaikytų projekto vadovo ir gautinų sumų tarnautojo / projekto apskaitininko poreikiams. SF išrašymo proceso atveju projekto vadovas valdo projektų atsiskaitymo nebaigtas užduotis, o gautinų sumų tarnautojas / projekto apskaitininkas sukuria suderinamą ir tikslų kliento sąskaitų faktūrų dokumentą.

![SF išrašymo srauto diagrama.](./media/invoicing-flow.png)

Projekto sutarties eilutė apibrėžia susietų projekto operacijų sąskaitų išrašymo būdą. Kai projekto vadovas patvirtina laiko ir išlaidų operacijas, sistema įrašo operacijas objekte **Projekto faktiniai duomenys** ir siunčia informaciją į „Dynamics 365 Finance“ modulį **Projekto valdymas ir apskaita**. Tada projekto apskaitininkas peržiūri ir užregistruoja įrašus naudodamas [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md). Šiame žurnale pateikiama svarbi projekto faktinių duomenų apskaitos informacija, pvz., atsiskaitymas, PVM grupė, atsiskaitymo prekių PVM grupė ir finansinės dimensijos.

Projekto vadovas gali peržiūrėti pardavimų, už kuriuos neišrašyta sąskaita, operacijas naudodamas laiko ir medžiagų atsiskaitymo būdą nueidamas į [Laiko ir medžiagų atsiskaitymo nebaigtas užduotis](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) ir fiksuotos kainos atsiskaitymo būdą nueidamas į [Fiksuotos kainos etapus](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Šie rodiniai leidžia filtruoti ir pasirinkti operacijas, kurias reikia įtraukti į kitą atsiskaitymo ciklą, o tada pažymėti jas kaip **Parengta išrašyti sąskaitą faktūrą**.

Galite [rankiniu būdu sukurti išankstinę sąskaitą faktūrą](../proforma-invoicing/create-manual-proforma-invoice.md) arba naudoti [periodinį procesą](../proforma-invoicing/configure-automated-invoice-creation.md). Projekto vadovas gali prireikus [koreguoti juodraščio sąskaitos faktūros juodraštį](../proforma-invoicing/manage-proforma-invoice.md), o tada ją patvirtinti.

Patvirtinta išankstinė sąskaita faktūra nusiunčiama į „Finansų“ modulį **Projekto valdymas ir apskaita**. Projekto apskaitininkas formatuoja ir atnaujina projekto SF pasiūlymą, o tada užregistruoja ir spausdina dokumentą. Užregistruotos projekto sąskaitos faktūros įrašomos didžiojoje knygoje, taip pat papildomose klientų ir projektų knygose.


[!INCLUDE[footer-include](../includes/footer-banner.md)]