---
title: Bendrųjų rezervuojamų išteklių priskyrimas užduočiai ir projekto komandai
description: Šioje temoje pateikiama informacija apie bendrųjų išteklių rezervavimą užduotims ir projekto komandoms.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145413"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="da04b-103">Bendrųjų rezervuojamų išteklių priskyrimas užduočiai ir išteklių reikalavimų generavimas</span><span class="sxs-lookup"><span data-stu-id="da04b-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="da04b-104">Savo projektui galite ne tik rezervuoti ir priskirti įvardytus arba realius išteklius, bet ir priskirti bendruosius išteklius projekto užduotims.</span><span class="sxs-lookup"><span data-stu-id="da04b-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="da04b-105">Šiuos išteklius galima naudoti kaip įvardytų išteklių vietos rezervavimo ženklus, kol būsite pasirengę juos pakeisti įvardytais projekto ištekliais.</span><span class="sxs-lookup"><span data-stu-id="da04b-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="da04b-106">Naudodami „Project Service Automation“ (PSA), atidarykite puslapį **Projektas** ir skirtuko **Grafikas** grafiko langelyje **Išteklius** įveskite bendrojo ištekliaus padėties pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="da04b-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="da04b-107">Arba spustelėkite langelyje esančią piktogramą **Išteklius** ir atidarykite išteklių parinkiklį, tada įveskite bendrojo ištekliaus, kurį norite sukurti, pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="da04b-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Bendrojo komandos nario sukūrimas ir priskyrimas](media/RM-how-to-9.png)

<span data-ttu-id="da04b-109">Atsidarys sritis **Spartusis kūrimas: projekto komandos narys**.</span><span class="sxs-lookup"><span data-stu-id="da04b-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="da04b-110">Įveskite bendrojo išteklių komandos nario vaidmenį ir organizacijos vienetą, tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="da04b-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Spartusis bendrojo komandos nario kūrimas](media/RM-how-to-10.png)

3. <span data-ttu-id="da04b-112">Sukūrus naują bendrąjį išteklių komandos narį, jis priskiriamas užduočiai.</span><span class="sxs-lookup"><span data-stu-id="da04b-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="da04b-113">Galite tęsti ir priskirti tą bendrąjį išteklių kitoms užduočių grafiko užduotims.</span><span class="sxs-lookup"><span data-stu-id="da04b-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Esamo bendrojo komandos nario priskyrimas užduotims](media/RM-how-to-11.png)

4. <span data-ttu-id="da04b-115">Priskyrę bendrąjį išteklių, galite generuoti ištekliaus reikalavimą ir jį įvykdyti tiesiogiai rezervuodami arba pateikdami ištekliaus užklausą išteklių vadovui.</span><span class="sxs-lookup"><span data-stu-id="da04b-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Bendrojo komandos nario reikalavimo generavimas](media/RM-how-to-12.png)

<span data-ttu-id="da04b-117">Komandos narių tinklelyje galite naudoti ne tik išteklių parinkiklį, kaip paminėta pirmiau, bet ir tiesiogiai įtraukti bendruosius išteklius.</span><span class="sxs-lookup"><span data-stu-id="da04b-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="da04b-118">Ištekliai įtraukiami nurodant išteklių reikalavimą, pagrįstą pradžios / pabaigos datomis ir paskirstymo metodu, nurodytu srityje **Spartusis kūrimas: projekto komandos narys**.</span><span class="sxs-lookup"><span data-stu-id="da04b-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="da04b-119">Skirtumą galite pamatyti tiesiogiai įtraukę bendrąjį komandos narį ir tada bendrajam ištekliui priskyrę daugiau užduočių, nei yra būtinų valandų, kurias jis turi apimti.</span><span class="sxs-lookup"><span data-stu-id="da04b-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="da04b-120">Norėdami iš naujo sugeneruoti reikalavimą, atitinkantį reikiamas valandas pagal priskyrimus spustelėkite **Generuoti reikalavimą**.</span><span class="sxs-lookup"><span data-stu-id="da04b-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="da04b-121">Taip pat galite spustelėti komandos tinklelyje esantį saitą **Išteklių reikalavimas**, kad atidarytumėte reikalavimą, įtrauktumėte įgūdžių, pageidaujamų išteklių ir pan.</span><span class="sxs-lookup"><span data-stu-id="da04b-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Išteklių reikalavimas](media/RM-how-to-13.png)

