---
title: Projektų sutarčių valdymas
description: Šioje temoje pateikta informacija apie projektu pagrįstų sutarčių peržiūrą.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177341"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="1c891-103">Projektų sutarčių valdymas</span><span class="sxs-lookup"><span data-stu-id="1c891-103">Manage project contracts</span></span>

<span data-ttu-id="1c891-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="1c891-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1c891-105">„Dynamics 365 Project Operations“ projektų sutartyse fiksuojami ir valdomi sutartyse numatyti įsipareigojimai bei išsami projekto informacija.</span><span class="sxs-lookup"><span data-stu-id="1c891-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="1c891-106">Programoje „Project Operations” projekto sutarties struktūra pritaikoma projektiniam darbui naudojant toliau pateikiamus komponentus.</span><span class="sxs-lookup"><span data-stu-id="1c891-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="1c891-107">Sutarties eilutės, kuriose nustatomi diskretiški darbo komponentai, kurie bus pristatyti kaip aukšto lygio komponentai projekto sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="1c891-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="1c891-108">Sutarties eilutės išsami informacija, kuria nustatomas ir įvertinamas kiekvieno aukšto lygio komponento arba sutarties eilutės darbas.</span><span class="sxs-lookup"><span data-stu-id="1c891-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="1c891-109">Sąmata apima darbo, susieto su sutarties eilute, grafiką ir finansinius aspektus.</span><span class="sxs-lookup"><span data-stu-id="1c891-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="1c891-110">Kiekvienai sutarties eilutei, kurioje pateikiama sąskaitų išrašymo tvarka kiekvienai sutarties eilutei ir bendrai sutarčiai, nustatomi sutarčių sudarymo modeliai ir apmokestinamieji komponentai.</span><span class="sxs-lookup"><span data-stu-id="1c891-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="1c891-111">Visų projektu pagrįstų sutarčių peržiūra</span><span class="sxs-lookup"><span data-stu-id="1c891-111">View all project-based contracts</span></span>

<span data-ttu-id="1c891-112">Visų projekto sutarčių sąrašą galite matyti sąrašo puslapyje **Sutartys**.</span><span class="sxs-lookup"><span data-stu-id="1c891-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="1c891-113">Eikite į **Pardavimas** > **Sutartys**.</span><span class="sxs-lookup"><span data-stu-id="1c891-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="1c891-114">Rodomas visų sistemoje esančių jūsų projekto sutarčių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="1c891-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="1c891-115">Norėdami pasirinkti kitus filtruotuosius rodinius, pasirinkite **rodinio perjungiklį** (šalia rodinio pavadinimo esančią išskleidžiamąją rodyklę).</span><span class="sxs-lookup"><span data-stu-id="1c891-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="1c891-116">Galite kurti savo rodinius su pasirinktiniais filtravimo kriterijais.</span><span class="sxs-lookup"><span data-stu-id="1c891-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="1c891-117">Sutartis galima kurti arba naikinti šiame sąrašo puslapyje arba išsamios informacijos puslapyje.</span><span class="sxs-lookup"><span data-stu-id="1c891-117">Contracts can be created or deleted from this list page or detail pages.</span></span>
