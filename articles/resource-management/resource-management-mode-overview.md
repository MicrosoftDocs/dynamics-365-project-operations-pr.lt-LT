---
title: Išteklių valdymo režimų apžvalga
description: Šioje temoje pateikiama informacija apie išteklių valdymo funkciją programoje „Dynamics 365 Project Operations“.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 5c0f98a6f08129ebef9b6d3fed1cc85969aa347c815a643d3c8dd639b42c0e8c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008236"
---
# <a name="resource-management-modes-overview"></a>Išteklių valdymo režimų apžvalga

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


„Dynamics 365 Project Operations“ palaiko du režimus, kad galėtumėte vykdyti bendrą rezervavimo srautą. Valdymo režimas apibrėžiamas kaip projekto parametras ir jį galima keisti, jei pasikeičia jūsų verslo poreikiai.    

## <a name="central-mode"></a>Centralizuotas režimas
Organizacijoms, kuriose išteklių priskyrimas projektams yra centralizuotas, centralizuotas režimas suteikia galimybę užtikrinti, kad projektų vadovai galėtų apibrėžti išteklių reikalavimus projekto lygiu. Išteklių reikalavimų vykdymas deleguojamas išteklių vadovui. Projektų vadovai gali priimti arba atmesti išteklių vadovo siūlomus išteklius.

![Centralizuotas režimas.](./media/resource-management-central.png)

Jei norite valdyti išteklius naudodami centralizuotą režimą, žr.:

- [Bendrųjų rezervuojamų išteklių priskyrimas užduočiai ir išteklių reikalavimų generavimas](/dynamics365/project-service/assign-generic-bookable-resource)
- [Įvardytų išteklių rezervavimas iš išteklių reikalavimų](/dynamics365/project-service/book-named-resource)
- [Išteklių užklausos pateikimas](/dynamics365/project-service/submit-resource-request)
- [Išteklių užklausos vykdymas](/dynamics365/project-service/resource-management-fulfill-requests)
- [Pasiūlyto projekto ištekliaus iš ištekliaus užklausos priėmimas arba atmetimas](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Hibridinis režimas
Organizacijoms, kurioms reikia lankstumo priskiriant išteklius, hibridinis režimas suteikia projektų vadovams ir išteklių vadovams galimybę rezervuoti išteklius.

![Hibridinis režimas.](./media/resource-management-hybrid.png)

Be palaikomo centralizuoto režimo proceso, peržiūrėkite toliau pateiktas temas, kad galėtumėte valdyti visas kitas palaikomas hibridinio režimo rezervavimo eigas:

Tiesioginis ištekliaus rezervavimas projekte:
- [Įvardytų rezervuojamų išteklių rezervavimas projekto komandai ir užduočių priskyrimas](/dynamics365/project-service/assign-named-bookable-resource)

Ištekliaus rezervavimas iš ištekliaus reikalavimo:
- [Bendrųjų rezervuojamų išteklių priskyrimas užduočiai ir išteklių reikalavimų generavimas](/dynamics365/project-service/assign-generic-bookable-resource)
- [Įvardytų išteklių rezervavimas iš išteklių reikalavimų](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]