---
title: Neautomatinės „proforma“ sąskaitos faktūros kūrimas – „Lite“ versija
description: Šioje temoje pateikta informacija, kaip sukurti neautomatinę išankstinę sąskaitą faktūrą programoje „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87ef090454b2a7ab997e7c21d8d10badc31c8235
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176396"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="063b4-103">Neautomatinės „proforma“ sąskaitos faktūros kūrimas – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="063b4-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="063b4-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="063b4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="063b4-105">„Dynamics 365 Project Operations“ išankstines sąskaita faktūras pagal poreikį galima kurti neautomatiškai.</span><span class="sxs-lookup"><span data-stu-id="063b4-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="063b4-106">Galite neautomatiškai sukurti išankstinę sąskaitą faktūrą sąrašo puslapyje **Projekto sutartys** arba informacijos puslapyje **Projekto sutartys**.</span><span class="sxs-lookup"><span data-stu-id="063b4-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="063b4-107">Sąrašo puslapis Projekto sutartys</span><span class="sxs-lookup"><span data-stu-id="063b4-107">Project Contracts list page</span></span>

<span data-ttu-id="063b4-108">Sąrašo puslapyje **Projektų sutartys** pasirinkite vieną arba kelias projekto sutartis ir sukurkite visų pasirinktų įrašų sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="063b4-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="063b4-109">Sistema tikrina, kurios iš pasirinktų projekto sutarčių nebaigta užduotis **Parengta išrašyti sąskaitą faktūrą** užregistruota prieš šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="063b4-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="063b4-110">Iš šių sutarčių sistema sukuria išankstinių sąskaitų faktūrų juodraščius.</span><span class="sxs-lookup"><span data-stu-id="063b4-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="063b4-111">Jei projekto sutartyje yra keli klientai, klientui gali būti sukurta viena sąskaita faktūra, o projekto sutarčiai – kelios sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="063b4-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="063b4-112">Visas sukurtas projekto sąskaitas faktūras galima rasti srities **Pardavimas** skilties **Atsiskaitymas** puslapyje **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="063b4-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="063b4-113">Projekto sutarties informacijos puslapis</span><span class="sxs-lookup"><span data-stu-id="063b4-113">Project Contract details page</span></span>

<span data-ttu-id="063b4-114">Išankstinę sąskaitą faktūrą taip pat galima sukurti naudojant informacijos puslapį **Projekto sutartis**, kuris sukuria tos konkrečios projekto sutarties sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="063b4-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="063b4-115">Sistema tikrina, ar projekto sutarties nebaigta užduotis **Parengta išrašyti sąskaitą faktūrą** užregistruota prieš šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="063b4-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="063b4-116">Iš šių sutarčių sistema sukuria išankstinių sąskaitų faktūrų juodraščius pagal kiekvienos sutarties eilutės klientų skaičių.</span><span class="sxs-lookup"><span data-stu-id="063b4-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="063b4-117">Kai sukuriama viena išankstinė sąskaita faktūra, atidaromas puslapis **sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="063b4-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="063b4-118">Jei sukuriamos kelios tos projekto sutarties sąskaitos faktūros, atidaromas puslapis **Sąskaitos faktūros**, kuriame rodomos visos sukurtos sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="063b4-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
