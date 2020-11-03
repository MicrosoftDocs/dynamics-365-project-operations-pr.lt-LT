---
title: Išteklių valdymas DUK
description: Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie išteklių valdymą.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081047"
---
# <a name="resource-management-faq"></a>Išteklių valdymas DUK

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Koks skirtumas tarp komandos nario ir ištekliaus reikalavimo?

Projekto komandos narys gali būti priskirtas užduotims, rezervuotas arba rezervuotas daugiau kartų ir nustatytas kaip tvirtintojas. Ištekliaus reikalavimas gali egzistuoti be projekto komandos nario, kaip poreikio juodraščio pastaba. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Kuo skiriasi pasiūlytos ir preliminariai rezervuotos valandos?

Skiriasi pasiūlytų valandų ir preliminariai rezervuotų valandų matomumas. Pasiūlytos valandos matomos tik išteklių valdytojui ir projektų vadovui, kuris inicijavo poreikį naudodamas išteklių užklausą. Preliminariai rezervuotos valandos matomos visiems, kurie turi prieigą prie grafiko lentos.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Kaip galiu matyti išteklių komandai preliminariai rezervuotas valandas?

Preliminarios rezervacijos gali būti atliekamos, kai rezervuojate išteklių reikalavimą. Ištekliai, kurie projekto komandai rezervuojami preliminariai, rodomi kaip komandos nariai, kuriems rezervuotos preliminarios valandos. Ši informacija taip pat rodoma grafiko lentoje.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Kaip pakeisti išteklių (bendrųjų arba turinčių pavadinimą), kuriuos rezervavau, būtinas valandas?

Rezervavę išteklius, pasirinkite **Tvarkyti rezervacijas** , kad atliktumėte visus reikiamus pakeitimus.

## <a name="what-resources-types-does-project-service-automation-support"></a>Kokius išteklių tipus palaiko „Project Service Automation“?

**Naudotojas** ir **Kontaktas** yra vieninteliai išteklių tipai, palaikomi Dynamics 365 Project Service Automation. Nors galite kurti kitų tipų išteklius (pavyzdžiui, **Įranga** ir **Grupė** ), jų galutinis naudojimas nepalaikomas.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Koks skirtumas tarp priskyrimo ir rezervacijos?

Priskyrimai yra išteklių projekto užduotims priskyrimas projekto grafike. Ištekliai gali būti faktiniai arba bendrieji. Rezervacijos yra galutinis arba preliminarus išteklių paskirstymas projektui. Galutinės rezervacijos naudoja išteklių pajėgumus. Idealiu atveju faktinių išteklių rezervacijos ir priskyrimai turėtų sutapti, nes jie nesiskiria. Tačiau PSA neįgyvendina šio sutapimo. Derinimo rodinyje rodomos projektų vadovo vietos, kuriose išteklių rezervacijos ir priskyrimai nesutampa.
