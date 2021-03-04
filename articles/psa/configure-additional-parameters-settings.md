---
title: Papildomų parametrų nuostatų konfigūravimas
description: Papildomų parametrų nuostatų konfigūravimas „Project Service“
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 73264845808e12950a48eea2b79e54c393d9c024
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151578"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="3a82d-103">Papildomų parametrų nuostatų konfigūravimas („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="3a82d-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3a82d-104">Kai sukonfigūruosite ankstesnių temų elementus, jums reikės nustatyti papildomus projekto parametrus, naudotinus jūsų projektuose.</span><span class="sxs-lookup"><span data-stu-id="3a82d-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="3a82d-105">Kai pirmą kartą įdiegėte „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“, sukūrėte parametrų nustatymą pirmiausia kurti visus įrašus, reikalingus „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“.</span><span class="sxs-lookup"><span data-stu-id="3a82d-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="3a82d-106">Dabar laikas grįžti atgal ir konfigūruoti papildomus šių parametrų nustatymo laukus.</span><span class="sxs-lookup"><span data-stu-id="3a82d-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="3a82d-107">Turite būti sukonfigūravę tolesnius parametrus.</span><span class="sxs-lookup"><span data-stu-id="3a82d-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="3a82d-108">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="3a82d-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="3a82d-109">SF išrašymo dažnis</span><span class="sxs-lookup"><span data-stu-id="3a82d-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="3a82d-110">Darbo valandų šablonas</span><span class="sxs-lookup"><span data-stu-id="3a82d-110">Work hours template</span></span>  
  
-   <span data-ttu-id="3a82d-111">Kainoraštis</span><span class="sxs-lookup"><span data-stu-id="3a82d-111">Price list</span></span>  
 
<span data-ttu-id="3a82d-112">Atlikdami šį veiksmą, taip pat nurodykite, kokio tipo išteklių paskirstymą norite taikyti.</span><span class="sxs-lookup"><span data-stu-id="3a82d-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="3a82d-113">**Centrinis**.</span><span class="sxs-lookup"><span data-stu-id="3a82d-113">**Central**.</span></span> <span data-ttu-id="3a82d-114">Tik išteklių vadovai gali paskirstyti išteklius projektams.</span><span class="sxs-lookup"><span data-stu-id="3a82d-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="3a82d-115">**Hibridinis**.</span><span class="sxs-lookup"><span data-stu-id="3a82d-115">**Hybrid**.</span></span> <span data-ttu-id="3a82d-116">Išteklių vadovai, projektų vadovai ir klientų vadybininkai gali paskirstyti išteklius projektams.</span><span class="sxs-lookup"><span data-stu-id="3a82d-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="3a82d-117">Norėdami nustatyti projekto parametrus, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3a82d-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="3a82d-118">Eikite į **Project Service > Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="3a82d-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="3a82d-119">Spustelėkite parametrų nustatymą, kurį norite konfigūruoti (tas, kurį sukūrėte, kai pirmą kartą įdiegėte „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“), arba spustelėkite **Naujas**, kad sukurtumėte naują.</span><span class="sxs-lookup"><span data-stu-id="3a82d-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="3a82d-120">Srityje **Bendra** nustatykite visas savo projekto parametrų parinktis.</span><span class="sxs-lookup"><span data-stu-id="3a82d-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="3a82d-121">Srityje **Kainoraštis** spustelėkite **+**, kad įtrauktumėte kainoraštį, pasirinkite kainoraštį išplečiamajame sąraše **Projekto parametrų kainoraštis**, o tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3a82d-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="3a82d-122">Viršutiniame dešiniajame ekrano kampe spustelėkite mygtuką **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3a82d-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="3a82d-123">Reikia išlaikyti projekto parametro įrašą, kad „Project Service“ tinkamai veiktų.</span><span class="sxs-lookup"><span data-stu-id="3a82d-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="3a82d-124">Šis įrašas neturėtų būti panaikintas.</span><span class="sxs-lookup"><span data-stu-id="3a82d-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="3a82d-125">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="3a82d-125">See Also</span></span>  
 [<span data-ttu-id="3a82d-126">Rezervuojamų išteklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="3a82d-126">Set up resources</span></span>](../psa/set-up-resources.md)
