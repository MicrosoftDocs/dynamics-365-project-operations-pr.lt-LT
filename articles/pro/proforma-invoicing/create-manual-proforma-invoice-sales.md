---
title: Neautomatinės išankstinės sąskaitos faktūros kūrimas
description: Šioje temoje pateikta informacija, kaip sukurti neautomatinę išankstinę sąskaitą faktūrą programoje „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081065"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="b2d05-103">Neautomatinės išankstinės sąskaitos faktūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="b2d05-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="b2d05-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="b2d05-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b2d05-105">„Dynamics 365 Project Operations“ išankstines sąskaita faktūras pagal poreikį galima kurti neautomatiškai.</span><span class="sxs-lookup"><span data-stu-id="b2d05-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="b2d05-106">Galite neautomatiškai sukurti išankstinę sąskaitą faktūrą sąrašo puslapyje **Projekto sutartys** arba informacijos puslapyje **Projekto sutartys**.</span><span class="sxs-lookup"><span data-stu-id="b2d05-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="b2d05-107">Sąrašo puslapis Projekto sutartys</span><span class="sxs-lookup"><span data-stu-id="b2d05-107">Project Contracts list page</span></span>

<span data-ttu-id="b2d05-108">Sąrašo puslapyje **Projektų sutartys** pasirinkite vieną arba kelias projekto sutartis ir sukurkite visų pasirinktų įrašų sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="b2d05-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="b2d05-109">Sistema tikrina, kurios iš pasirinktų projekto sutarčių nebaigta užduotis **Parengta išrašyti sąskaitą faktūrą** užregistruota prieš šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="b2d05-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="b2d05-110">Iš šių sutarčių sistema sukuria išankstinių sąskaitų faktūrų juodraščius.</span><span class="sxs-lookup"><span data-stu-id="b2d05-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="b2d05-111">Jei projekto sutartyje yra keli klientai, klientui gali būti sukurta viena sąskaita faktūra, o projekto sutarčiai – kelios sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="b2d05-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="b2d05-112">Visas sukurtas projekto sąskaitas faktūras galima rasti srities **Pardavimas** skilties **Atsiskaitymas** puslapyje **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="b2d05-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="b2d05-113">Projekto sutarties informacijos puslapis</span><span class="sxs-lookup"><span data-stu-id="b2d05-113">Project Contract details page</span></span>

<span data-ttu-id="b2d05-114">Išankstinę sąskaitą faktūrą taip pat galima sukurti naudojant informacijos puslapį **Projekto sutartis** , kuris sukuria tos konkrečios projekto sutarties sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="b2d05-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="b2d05-115">Sistema tikrina, ar projekto sutarties nebaigta užduotis **Parengta išrašyti sąskaitą faktūrą** užregistruota prieš šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="b2d05-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="b2d05-116">Iš šių sutarčių sistema sukuria išankstinių sąskaitų faktūrų juodraščius pagal kiekvienos sutarties eilutės klientų skaičių.</span><span class="sxs-lookup"><span data-stu-id="b2d05-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="b2d05-117">Kai sukuriama viena išankstinė sąskaita faktūra, atidaromas puslapis **sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="b2d05-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="b2d05-118">Jei sukuriamos kelios tos projekto sutarties sąskaitos faktūros, atidaromas puslapis **Sąskaitos faktūros** , kuriame rodomos visos sukurtos sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="b2d05-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
