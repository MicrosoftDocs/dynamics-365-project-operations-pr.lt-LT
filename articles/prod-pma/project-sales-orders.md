---
title: Laiko ir medžiagų projektų pardavimo užsakymai
description: Šioje temoje paaiškinama, kaip kurti laiko ir medžiagų projektų projektu pagrįstus pardavimo užsakymus.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009671"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="3099f-103">Laiko ir medžiagų projektų pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="3099f-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3099f-104">Šioje temoje aprašoma, kaip sukurti projekto pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3099f-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="3099f-105">Pardavimo užsakymus galima kurti tik projektuose, kurių tipas yra **laikas ir medžiagos**.</span><span class="sxs-lookup"><span data-stu-id="3099f-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="3099f-106">Jei su laiko ir medžiagų projektu susijusioje projekto sutartyje yra keli finansavimo šaltiniai, turite įjungti parametrą **Leisti pardavimo užsakymus projektuose su keliais finansavimo šaltiniais** puslapyje **Projektų valdymas ir apskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="3099f-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="3099f-107">Galima naudoti projektų pardavimo užsakymų su keliais finansavimo šaltiniais palaikymą pradedant nuo 10.0.2 programos leidimo ir naujesnių versijų.</span><span class="sxs-lookup"><span data-stu-id="3099f-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="3099f-108">Parametras, kuriuo įgalinamas projektų pardavimo užsakymų su keliais finansavimo šaltiniais palaikymas, bus pašalintas 2020 m. balandžio mėn. leidimo bangos metu, po kurios ši funkcija bus įgalinta visada.</span><span class="sxs-lookup"><span data-stu-id="3099f-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="3099f-109">Projektu pagrįstus pardavimo užsakymus galite kurti toliau pateikiamais dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="3099f-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="3099f-110">Pereikite prie paties projekto.</span><span class="sxs-lookup"><span data-stu-id="3099f-110">Go to the project itself.</span></span> <span data-ttu-id="3099f-111">Veiksmų srityje pasirinkite **Valdyti > Elementų užduotys > Pardavimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="3099f-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="3099f-112">Projekto informacija pagal numatytuosius parametrus bus nustatyta pagal projekto pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3099f-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="3099f-113">Jei projekto sutartyje yra daugiau nei vienas finansavimo šaltinis, turėsite pasirinkti finansavimo šaltinį, kad nustatytumėte pardavimo užsakymo klientą.</span><span class="sxs-lookup"><span data-stu-id="3099f-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="3099f-114">Jei projekte yra tik vienas finansavimo šaltinis, klientas bus nustatytas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="3099f-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="3099f-115">Įeikite į sąrašo puslapį **Visi pardavimo užsakymai** ir sukurkite naują pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="3099f-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="3099f-116">Turėsite pasirinkti pardavimo užsakymo projektą.</span><span class="sxs-lookup"><span data-stu-id="3099f-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="3099f-117">Pasirinkus projektą, klientas bus nustatomas pagal finansavimo šaltinį, arba reikės pasirinkti finansavimo šaltinį, jei projekto sutartyje nurodyti keli finansavimo šaltiniai.</span><span class="sxs-lookup"><span data-stu-id="3099f-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]