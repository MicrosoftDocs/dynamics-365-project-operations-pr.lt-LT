---
title: Išteklių valdymo režimų apžvalga
description: Šioje temoje pateikiama informacija apie išteklių valdymo funkciją programoje „Dynamics 365 Project Operations“.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279463"
---
# <a name="resource-management-modes-overview"></a>Išteklių valdymo režimų apžvalga

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


„Dynamics 365 Project Operations“ palaiko du režimus, kad galėtumėte vykdyti bendrą rezervavimo srautą. Valdymo režimas apibrėžiamas kaip projekto parametras ir jį galima keisti, jei pasikeičia jūsų verslo poreikiai.    

## <a name="central-mode"></a>Centralizuotas režimas
Organizacijoms, kuriose išteklių priskyrimas projektams yra centralizuotas, centralizuotas režimas suteikia galimybę užtikrinti, kad projektų vadovai galėtų apibrėžti išteklių reikalavimus projekto lygiu. Išteklių reikalavimų vykdymas deleguojamas išteklių vadovui. Projektų vadovai gali priimti arba atmesti išteklių vadovo siūlomus išteklius.

![Centralizuotas režimas](./media/resource-management-central.png)

Jei norite valdyti išteklius naudodami centralizuotą režimą, žr.:

- [Bendrųjų rezervuojamų išteklių priskyrimas užduočiai ir išteklių reikalavimų generavimas](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Įvardytų išteklių rezervavimas iš išteklių reikalavimų](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Išteklių užklausos pateikimas](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Išteklių užklausos vykdymas](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Pasiūlyto projekto ištekliaus iš ištekliaus užklausos priėmimas arba atmetimas](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibridinis režimas
Organizacijoms, kurioms reikia lankstumo priskiriant išteklius, hibridinis režimas suteikia projektų vadovams ir išteklių vadovams galimybę rezervuoti išteklius.

![Hibridinis režimas](./media/resource-management-hybrid.png)

Be palaikomo centralizuoto režimo proceso, peržiūrėkite toliau pateiktas temas, kad galėtumėte valdyti visas kitas palaikomas hibridinio režimo rezervavimo eigas:

Tiesioginis ištekliaus rezervavimas projekte:
- [Įvardytų rezervuojamų išteklių rezervavimas projekto komandai ir užduočių priskyrimas](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Ištekliaus rezervavimas iš ištekliaus reikalavimo:
- [Bendrųjų rezervuojamų išteklių priskyrimas užduočiai ir išteklių reikalavimų generavimas](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Įvardytų išteklių rezervavimas iš išteklių reikalavimų](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]