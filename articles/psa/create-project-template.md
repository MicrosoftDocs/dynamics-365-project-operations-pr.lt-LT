---
title: Projekto šablono kūrimas
description: Projekto šablono kūrimas „Project Service“
author: ruhercul
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
ms.openlocfilehash: 78d25183aad8d86593d3f2582295db59eb84cf14
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133198"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="cfcb0-103">Projekto šablono kūrimas („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="cfcb0-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="cfcb0-104">Naudojant Projektų šablonus galima sutaupyti laiko, jei jūsų įmonė reguliariai teikia pasiūlymus dėl panašių tipų projektų.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="cfcb0-105">Juose pateikiamas standartinis tam tikto tipo projekto vaidmenų ir numatomų valandų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="cfcb0-106">Klientų vadovai ir projektų vadovai gali kurti projektus pagal projekto šabloną arba kopijuoti šabloną ir susikurti savąjį.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="cfcb0-107">Projekto šablono komponentai</span><span class="sxs-lookup"><span data-stu-id="cfcb0-107">Components of project template</span></span>
 <span data-ttu-id="cfcb0-108">Projekto šabloną sudaro trys toliau nurodyti komponentai.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="cfcb0-109">**Darbo paskirstymo struktūra**: darbo paskirstymo struktūrą projekto šablone sudaro tie patys elementai kaip ir projekte.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="cfcb0-110">Galite kurti užduočių hierarchiją, susieti vaidmenis su užduotimis, nustatyti grafiko atributus, nustatyti priklausomybes ir peržiūrėti visus Ganto diagramos duomenis.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="cfcb0-111">Projekto šablonų darbo paskirstymo struktūra taip pat palaiko visų užduočių režimus.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="cfcb0-112">Kuriant darbo grafiką, skirtumų tarp projekto šablono ir projekto nėra.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="cfcb0-113">**Projekto sąmatos**: projekto šablonų ir projektų sąmatos sudaromos pagal tokį patį principą, išskyrus tai, kad numatytųjų išlaidų kainoraščiai ir pardavimo kainos visada yra numatytosios išlaidos ir pardavimo kainų sąrašai, nustatyti „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ parametruose.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="cfcb0-114">Kitos funkcijos yra tokios pat kaip projekte.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="cfcb0-115">**Projekto komandos formavimas**: formuojant projekto komandą projekto šablone, jame negalima užsisakyti pavadino ištekliaus.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="cfcb0-116">Galite naudoti parinktį **Generuoti projekto komandą** darbo paskirstymo struktūroje, kad sukurtumėte bendrųjų išteklių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="cfcb0-117">Taip pat galite nurodyti reikiamus bendrųjų išteklių įgūdžius ir kvalifikaciją.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="cfcb0-118">Projekto šablonuose bendrojo ištekliaus negalima pakeisti rezervuojamu ištekliumi.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="cfcb0-119">Projekto kūrimas pagal šabloną</span><span class="sxs-lookup"><span data-stu-id="cfcb0-119">Create a project from a template</span></span>  
 <span data-ttu-id="cfcb0-120">Projektą kurti šabloną galima toliau nurodytais būdais.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="cfcb0-121">Kurdami projektą pagal pasiūlymą, projekto šabloną galite pasirinkti projekto sparčiojo kūrimo formoje.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="cfcb0-122">Kai projektą kuriate spustelėję **Naujas projektas**, prieš įrašant įrašą rodoma projekto forma.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="cfcb0-123">Joje galite spustelėti lauką **Pasirinkti šabloną** ir pasirinkti iš jūsų organizacijoje iš anksto nustatytų šablonų sąrašo.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="cfcb0-124">Spustelėkite **Kurti projektą pagal šabloną** puslapyje **Projekto šablonas**, kad sukurtumėte projektą pagal šabloną.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="cfcb0-125">Šablono komponentų kopijavimas į projektą</span><span class="sxs-lookup"><span data-stu-id="cfcb0-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="cfcb0-126">Jei kopijuojate šablono komponentus į projektą, įsidėmėkite kelis dalykus.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="cfcb0-127">**Darbo paskirstymo struktūros kopijavimas**: kai iš projekto šablono kopijuojate darbo paskirstymo struktūrą, jei projekto kalendorius skiriasi nuo šablono kalendoriaus, užduočių grafike bus taikomos projekto kalendoriaus darbo valandos.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="cfcb0-128">Tokiu būdu grafikas yra pakoreguojamas pagal atsarginį projekto kalendorių.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="cfcb0-129">Panašiai pirmoji darbo paskirstymo struktūros užduotis perima projekto pradžios datą, todėl likęs užduočių hierarchijos grafikas yra atnaujinamas pagal trukmę ir priklausomybes, nurodytas šablono darbo paskirstymo struktūroje.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="cfcb0-130">**Projekto sąmatos kopijavimas**: kai kopijuojate keliose projekto sąmatų eilutėse, kainoraščiai atnaujinami pagal projekto valdančio vieneto savikainų sąrašą ir kliento pardavimo kainų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="cfcb0-131">Pagal šiuos sąrašus nustatomos vieneto savikainos ir pardavimo kainos projektuose, susijusiuose su pardavimo objektu.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="cfcb0-132">**Projekto komandos kopijavimas**: kopijuojant projekto komandą iš šablono į projektą, nukopijuojami visi bendrieji resursai ir jų įgūdžiai bei kvalifikacija, nurodyti šablone.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="cfcb0-133">Bendrųjų išteklių priskyrimai taip pat tvarkomi kaip ir projekto šablone.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="cfcb0-134">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="cfcb0-134">See Also</span></span>  
 [<span data-ttu-id="cfcb0-135">Projekto vadovo vadovas</span><span class="sxs-lookup"><span data-stu-id="cfcb0-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
