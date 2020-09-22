---
title: Laiko ir medžiagų projektų pardavimo užsakymai
description: Šioje temoje paaiškinama, kaip kurti laiko ir medžiagų projektų projektu pagrįstus pardavimo užsakymus.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753650"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="e0640-103">Laiko ir medžiagų projektų pardavimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="e0640-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="e0640-104">Šioje temoje aprašoma, kaip sukurti projekto pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="e0640-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="e0640-105">Pardavimo užsakymus galima kurti tik projektuose, kurių tipas yra **laikas ir medžiagos**.</span><span class="sxs-lookup"><span data-stu-id="e0640-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="e0640-106">Jei su laiko ir medžiagų projektu susijusioje projekto sutartyje yra keli finansavimo šaltiniai, turite įjungti parametrą **Leisti pardavimo užsakymus projektuose su keliais finansavimo šaltiniais** puslapyje **Projektų valdymas ir apskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e0640-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="e0640-107">Galima naudoti projektų pardavimo užsakymų su keliais finansavimo šaltiniais palaikymą pradedant nuo 10.0.2 programos leidimo ir naujesnių versijų.</span><span class="sxs-lookup"><span data-stu-id="e0640-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="e0640-108">Parametras, kuriuo įgalinamas projektų pardavimo užsakymų su keliais finansavimo šaltiniais palaikymas, bus pašalintas 2020 m. balandžio mėn. leidimo bangos metu, po kurios ši funkcija bus įgalinta visada.</span><span class="sxs-lookup"><span data-stu-id="e0640-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="e0640-109">Projektu pagrįstus pardavimo užsakymus galite kurti toliau pateikiamais dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="e0640-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="e0640-110">Pereikite prie paties projekto.</span><span class="sxs-lookup"><span data-stu-id="e0640-110">Go to the project itself.</span></span> <span data-ttu-id="e0640-111">Veiksmų srityje pasirinkite **Valdyti > Elementų užduotys > Pardavimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="e0640-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="e0640-112">Projekto informacija pagal numatytuosius parametrus bus nustatyta pagal projekto pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="e0640-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="e0640-113">Jei projekto sutartyje yra daugiau nei vienas finansavimo šaltinis, turėsite pasirinkti finansavimo šaltinį, kad nustatytumėte pardavimo užsakymo klientą.</span><span class="sxs-lookup"><span data-stu-id="e0640-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="e0640-114">Jei projekte yra tik vienas finansavimo šaltinis, klientas bus nustatytas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="e0640-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="e0640-115">Įeikite į sąrašo puslapį **Visi pardavimo užsakymai** ir sukurkite naują pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="e0640-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="e0640-116">Turėsite pasirinkti pardavimo užsakymo projektą.</span><span class="sxs-lookup"><span data-stu-id="e0640-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="e0640-117">Pasirinkus projektą, klientas bus nustatomas pagal finansavimo šaltinį, arba reikės pasirinkti finansavimo šaltinį, jei projekto sutartyje nurodyti keli finansavimo šaltiniai.</span><span class="sxs-lookup"><span data-stu-id="e0640-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

