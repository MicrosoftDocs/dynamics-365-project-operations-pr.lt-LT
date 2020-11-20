---
title: Projektų pasiūlymų valdymas
description: Šioje temoje pateikta informacija apie projektų pasiūlymus.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177836"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="a58b3-103">Projektų pasiūlymų valdymas</span><span class="sxs-lookup"><span data-stu-id="a58b3-103">Manage project quotes</span></span>

<span data-ttu-id="a58b3-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="a58b3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a58b3-105">Programoje „Dynamics 365 Project Operations“ projekto pasiūlymai kuriami padėti projekto darbo pasiūlymams kurti.</span><span class="sxs-lookup"><span data-stu-id="a58b3-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="a58b3-106">Programoje „Project Operations” projekto pasiūlymo struktūra kuriama naudojant toliau pateikiamus komponentus.</span><span class="sxs-lookup"><span data-stu-id="a58b3-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="a58b3-107">Pasiūlymo eilutės, kuriose nustatomi diskretiški darbo komponentai, kurie bus pristatyti kaip aukšto lygio komponentai.</span><span class="sxs-lookup"><span data-stu-id="a58b3-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="a58b3-108">Pasiūlymo eilutės išsami informacija, kuria nustatomas ir įvertinamas kiekvieno aukšto lygio komponento arba pasiūlymo eilutės darbas.</span><span class="sxs-lookup"><span data-stu-id="a58b3-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="a58b3-109">Darbo grafiko arba datos sąmatos ir finansiniai aspektai susiejami su šia pasiūlymo eilute.</span><span class="sxs-lookup"><span data-stu-id="a58b3-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="a58b3-110">Sutarties sudarymo modeliai ir apmokestinami komponentai nustatomi kiekvienai pasiūlymo eilutei.</span><span class="sxs-lookup"><span data-stu-id="a58b3-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="a58b3-111">Šį sąranka padeda įvertinti kiekvienos pasiūlymo eilutės ir bendrą pasiūlymo pajamų, išlaidų ir pelningumo pasiskirstymą.</span><span class="sxs-lookup"><span data-stu-id="a58b3-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="a58b3-112">Visų projektu pagrįstų pasiūlymų peržiūra</span><span class="sxs-lookup"><span data-stu-id="a58b3-112">View all project-based quotes</span></span>

<span data-ttu-id="a58b3-113">Visų projekto pasiūlymų sąrašą galite matyti sąrašo puslapyje **Pasiūlymai**.</span><span class="sxs-lookup"><span data-stu-id="a58b3-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="a58b3-114">Eikite į **Pardavimas** > **Pasiūlymai**.</span><span class="sxs-lookup"><span data-stu-id="a58b3-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="a58b3-115">Rodomas visų sistemoje esančių jūsų projekto pasiūlymų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="a58b3-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="a58b3-116">Norėdami pasirinkti kitus pasiūlymų filtruotuosius rodinius, naudokite **Rodinio perjungiklį**.</span><span class="sxs-lookup"><span data-stu-id="a58b3-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="a58b3-117">Naudodami pasirinktinius filtro kriterijus, galite konfigūruoti savo rodinius ir naršymo galimybes.</span><span class="sxs-lookup"><span data-stu-id="a58b3-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="a58b3-118">Pasiūlymus galima kurti arba naikinti šiame sąrašo puslapyje arba išsamios informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a58b3-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
