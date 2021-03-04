---
title: Mobilioji darbo sritis Projekto laiko įvedimas
description: Šioje temoje pateikiama informacija apie mobiliąją darbo sritį Projekto laiko įvedimas. Šioje darbo srityje vartotojai gali įvesti ir sutaupyti projekto laiko, naudodami mobiliuosius įrenginius.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 23a5a9f25cfdd6df74257b3500c7a035d711b5f6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080817"
---
# <a name="project-time-entry-mobile-workspace"></a>Mobilioji darbo sritis Projekto laiko įvedimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie mobiliąją darbo sritį **Projekto laiko įvedimas**. Šioje darbo srityje vartotojai gali įvesti ir sutaupyti projekto laiko, naudodami mobiliuosius įrenginius.

Ši mobilioji darbo sritis skirta naudoti su „Dynamics 365“ bendrųjų operacijų mobiliųjų įrenginių programėle. 

## <a name="overview"></a>Apžvalga
Vykdydami kasdienes užduotis, projekto ištekliai dažnai yra vietoje arba keliauja. Mobilioji darbo sritis **Projekto laiko įvedimas** suteikia vartotojams galimybę įvesti apmokėtiną arba neapmokėtiną projekto laiką jų pasirinktuose mobiliuosiuose įrenginiuose. Todėl projekto ištekliai gali bet kada ir bet kur įrašyti laiką. Taip pat jie gali peržiūrėti jau sukurtus laiko įrašus. 

Tiksliau sakant, mobiliojoje darbo srityje **Projekto laiko įvedimas** vartotojai gali atlikti toliau pateikiamas užduotis.

-   Bet kurią pasirinktą dieną įvesti valandų, praleistų atliekant tam tikrą užduotį, skaičių.
-   Ieškoti pagal projekto pavadinimą arba klientą ir rasti projektą, kurio laiką norimą įvesti.
-   Nurodyti praleisto laiko kategoriją ir veiklą.
-   Įrašyti apmokėtiną arba neapmokėtiną projekto laiką.
-   Pasirinktinai įvesti komentarus, skirtus naudoti įmonėje ar už jos ribų.

## <a name="prerequisites"></a>Būtinosios sąlygos
Būtinosios sąlygos skiriasi atsižvelgiant į „Microsoft Dynamics 365“ versiją, įdiegtą organizacijoje.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Būtinosios sąlygos, jei naudojama „Dynamics 365 Finance“
Jei organizacijoje įdiegta „Finance“, sistemos administratorius turi publikuoti mobiliąją darbo sritį **Projekto laiko įvedimas**. Instrukcijų ieškokite skyriuje [Mobiliosios darbo srities publikavimas](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Būtinosios sąlygos, jei naudojama 1611 versija su 3 arba naujesnės versijos platforma
Jei organizacijoje įdiegta 1611 versija su 3 arba naujesnės versijos platforma, sistemos administratorius turi įvykdyti toliau pateikiamas būtinąsias sąlygas. 

<table>
<thead>
<tr class="header">
<th>Būtinoji sąlyga</th>
<th>Vaidmuo</th>
<th>Aprašas</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Įdiegti KB 4018050.</td>
<td>Sistemos administratorius</td>
<td>KB 4018050 yra X++ naujinimas arba metaduomenų karštosios pataisos, kuriose yra mobilioji darbo sritis <strong>Projekto laiko įvedimas</strong>. Norėdamas įdiegti KB 4018050, sistemos administratorius turi atlikti toliau pateikiamus veiksmus.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Atsisiųsti metaduomenų karštąsias pataisas iš „Microsoft Dynamics“ „Lifecycle Services“ (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Įdiegti metaduomenų karštąsias pataisas</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Sukurti įdiegiamą paketą,</a> kuriame yra modeliai <strong>„ApplicationSuite“</strong> ir <strong>„ProjectMobile“</strong>, ir įkelti įdiegiamą paketą į LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Pritaikyti įdiegiamą paketą</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publikuoti mobiliąją darbo sritį <strong>Projekto laiko įvedimas</strong>.</td>
<td>Sistemos administratorius</td>
<td>Žr. <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiliosios darbo srities publikavimas</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiliųjų įrenginių programėlės atsisiuntimas ir įdiegimas

Mobiliųjų įrenginių programėlės „Finance and Operations“ atsisiuntimas ir įdiegimas.

-   [Skirta telefonams „Android“](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Skirta telefonams „iPhone“](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prisijungimas prie mobiliųjų įrenginių programėlės
1.  Mobiliajame įrenginyje paleiskite mobiliųjų įrenginių programėlę.
2.  Įveskite savo „Dynamics 365“ URL.
3.  Pirmą kartą prisijungdami, būsite paraginti įvesti vartotojo vardą ir slaptažodį. Įveskite savo kredencialus.
4.  Kai prisijungsite, bus rodomos galimos jūsų įmonės darbo sritys. Atminkite, kad jei jūsų sistemos administratorius vėliau publikuos naują darbo sritį, turėsite atnaujinti mobiliųjų darbo sričių sąrašą.

[![Atnaujinimas patempiant žemyn](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Laiko įvedimas, naudojant mobiliąją darbo sritį Projekto laiko įvedimas
1.  Mobiliajame įrenginyje pasirinkite darbo sritį **Projekto laiko įvedimas**.
2.  Pasirinkite **Laiko įvedimas**. Rodomos dabartinės savaitės kalendoriaus datos.
3.  Pažymėkite pasirinktos datos parinktis **Veiksmai** &gt; **Naujas įrašas**.
4.  Įveskite įrašytinų valandų skaičių.
5.  Pasirinkite laiko įrašo projektą. Sąraše pateikiami į programą įkelti projektai, skirti naudoti neprisijungus. Pagal numatytuosius parametrus įkeliama 50 elementų, bet kūrėjas gali šį skaičių pakeisti. Daugiau informacijos žr. skyriuje [Mobilioji platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Jei jūsų projekto sąraše nėra, pasirinkite **Ieškoti**. Ieškokite pagal pavadinimą arba pereikite prie ieškos pagal projekto pavadinimą arba klientą.
7.  Pasirinkite kategoriją.  Sąraše pateikiamos į programą įkeltos kategorijos, skirtos naudoti neprisijungus. Pagal numatytuosius parametrus įkeliama 50 elementų, bet kūrėjas gali šį skaičių pakeisti. Daugiau informacijos žr. skyriuje [Mobilioji platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Jei jūsų kategorijos sąraše nėra, pasirinkite **Ieškoti**. Ieškokite pagal kategoriją arba pereikite prie ieškos pagal kategorijos pavadinimą.
9.  Pasirinkite veiklą. Sąraše pateikiamos į programą įkeltos veiklos, skirtos naudoti neprisijungus. Pagal numatytuosius parametrus įkeliama 50 elementų, bet kūrėjas gali šį skaičių pakeisti. Daugiau informacijos žr. skyriuje [Mobilioji platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Jei jūsų veiklos sąraše nėra, pasirinkite **Ieškoti**. Ieškokite pagal veiklos numerį arba pereikite prie ieškos pagal paskirtį.

11. Pažymėkite eilutės ypatybę.
12. Pasirinktinai įveskite komentarų, skirtų naudoti įmonėje ir už jos ribų.
13. Pasirinkite **Atlikta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]