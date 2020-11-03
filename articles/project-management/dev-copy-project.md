---
title: Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą
description: Šioje temoje pateikta informacija apie tai, kaip kurti projektų šablonus naudojant pasirinktinį veiksmą Kopijuoti projektą.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080776"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="221bb-103">Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą</span><span class="sxs-lookup"><span data-stu-id="221bb-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="221bb-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="221bb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="221bb-105">„Dynamics 365 Project Operations“ palaiko galimybę kopijuoti projektą ir atkurti bet kokius priskyrimus į bendruosius išteklius, nurodančius vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="221bb-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="221bb-106">Naudodami šią funkciją klientai gali kurti pagrindinių projektų šablonus.</span><span class="sxs-lookup"><span data-stu-id="221bb-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="221bb-107">Pasirinkus **Kopijuoti projektą** , tikslinio projekto būsena atnaujinama.</span><span class="sxs-lookup"><span data-stu-id="221bb-107">When you select **Copy Project** , the status of the target project is updated.</span></span> <span data-ttu-id="221bb-108">Naudokite **būsenos tipą** , kad nustatytumėte, kada kopijavimo veiksmas yra baigtas.</span><span class="sxs-lookup"><span data-stu-id="221bb-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="221bb-109">Pasirinkus **Kopijuoti projektą** taip pat projekto pradžios data atnaujinama į dabartinę pradžios datą, jei tikslinio projekto objekte neaptikta tikslinė data.</span><span class="sxs-lookup"><span data-stu-id="221bb-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="221bb-110">Pasirinktinis veiksmas Kopijuoti projektą</span><span class="sxs-lookup"><span data-stu-id="221bb-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="221bb-111">Pavadinimas / vardas, pavardė</span><span class="sxs-lookup"><span data-stu-id="221bb-111">Name</span></span> 

<span data-ttu-id="221bb-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="221bb-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="221bb-113">Įvesties parametrai</span><span class="sxs-lookup"><span data-stu-id="221bb-113">Input parameters</span></span>
<span data-ttu-id="221bb-114">Yra trys įvesties parametrai.</span><span class="sxs-lookup"><span data-stu-id="221bb-114">There are three input parameters:</span></span>

| <span data-ttu-id="221bb-115">Parametras</span><span class="sxs-lookup"><span data-stu-id="221bb-115">Parameter</span></span>          | <span data-ttu-id="221bb-116">Tipas</span><span class="sxs-lookup"><span data-stu-id="221bb-116">Type</span></span>   | <span data-ttu-id="221bb-117">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="221bb-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="221bb-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="221bb-118">ProjectCopyOption</span></span>  | <span data-ttu-id="221bb-119">String</span><span class="sxs-lookup"><span data-stu-id="221bb-119">String</span></span> | <span data-ttu-id="221bb-120">**{"removeNamedResources":true}** arba **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="221bb-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="221bb-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="221bb-121">SourceProject</span></span>      | <span data-ttu-id="221bb-122">Objekto nuoroda</span><span class="sxs-lookup"><span data-stu-id="221bb-122">Entity Reference</span></span> | <span data-ttu-id="221bb-123">Šaltinio projektas</span><span class="sxs-lookup"><span data-stu-id="221bb-123">Source Project</span></span> |
| <span data-ttu-id="221bb-124">Tikslinis objektas</span><span class="sxs-lookup"><span data-stu-id="221bb-124">Target</span></span>             | <span data-ttu-id="221bb-125">Objekto nuoroda</span><span class="sxs-lookup"><span data-stu-id="221bb-125">Entity Reference</span></span> | <span data-ttu-id="221bb-126">Tikslinis projektas</span><span class="sxs-lookup"><span data-stu-id="221bb-126">Target Project</span></span> |


- <span data-ttu-id="221bb-127">**{"clearTeamsAndAssignments":true}** : numatytas „Project“, skirto žiniatinkliui, veikimas, bus pašalinti visi priskyrimai ir komandos nariai.</span><span class="sxs-lookup"><span data-stu-id="221bb-127">**{"clearTeamsAndAssignments":true}** : Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="221bb-128">**{"removeNamedResources":true}** : numatytasis „Project Operations“ veikimas, priskyrimai bus atkurti į bendruosius išteklius.</span><span class="sxs-lookup"><span data-stu-id="221bb-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="221bb-129">Daugiau informacijos apie veiksmus žr. [Žiniatinklio API veiksmai](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions).</span><span class="sxs-lookup"><span data-stu-id="221bb-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="221bb-130">Kopijuotinų laukų nurodymas</span><span class="sxs-lookup"><span data-stu-id="221bb-130">Specify fields to copy</span></span> 
<span data-ttu-id="221bb-131">Kai veiksmas iškviečiamas, funkcija **Kopijuoti projektą** ieškos projekto rodinyje **Kopijuoti projekto stulpelius** ir nustatys, kuriuos laukus kopijuoti, kai projektas kopijuojamas.</span><span class="sxs-lookup"><span data-stu-id="221bb-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
