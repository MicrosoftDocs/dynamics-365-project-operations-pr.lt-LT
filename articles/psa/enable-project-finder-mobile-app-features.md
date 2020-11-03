---
title: „Project Finder Mobile“ programėlės funkcijų įjungimas
description: „Project Finder Mobile“ programėlės funkcijų įjungimas „Project Service“
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080843"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="1aa87-103">„Project Finder Mobile“ programėlės funkcijų įjungimas („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="1aa87-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1aa87-104">Jūsų ištekliai savo telefone gali naudoti „Project Finder Mobile“ ir „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“, kad rastų naujus projektus, kuriuos jie nori vykdyti, ir naujinti savo įgūdžių rinkinius.</span><span class="sxs-lookup"><span data-stu-id="1aa87-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="1aa87-105">Programėlę galima naudoti „[!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]“ ir „[!INCLUDE[tn_android](../includes/tn-android.md)]“ telefonuose bei „[!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]“.</span><span class="sxs-lookup"><span data-stu-id="1aa87-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="1aa87-106">Turite nustatyti kelias jūsų organizacijos vieneto parametrų sąrankos parinktis, kad vartotojai galėtų peržiūrėti projektų išteklių reikalavimus ir naujinti savo įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="1aa87-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="1aa87-107">„Project Finder Mobile“ programėlę galima naudoti tik su „[!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)]“ (ne su vietine versija).</span><span class="sxs-lookup"><span data-stu-id="1aa87-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="1aa87-108">Eikite į **Project Service > Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1aa87-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="1aa87-109">Spustelėkite parametrų nustatymą, kurį norite naudoti, kad įjungtumėte „Project Finder Mobile“ programėlės funkcijas.</span><span class="sxs-lookup"><span data-stu-id="1aa87-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="1aa87-110">Srityje **Bendra** parinktį **Išteklių reikalavimai matomi ištekliams** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1aa87-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="1aa87-111">Nustatykite **Leisti naujinti įgūdžius pagal išteklius** į parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1aa87-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="1aa87-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="1aa87-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="1aa87-113">Tai visuotinis parametras.</span><span class="sxs-lookup"><span data-stu-id="1aa87-113">This is a global setting.</span></span> <span data-ttu-id="1aa87-114">Projektų vadovai gali nustatyti, ar atskiras projektas bus matomas to projekto puslapyje **Projekto grupė**.</span><span class="sxs-lookup"><span data-stu-id="1aa87-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="1aa87-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="1aa87-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="1aa87-116">El. pašto pranešimai</span><span class="sxs-lookup"><span data-stu-id="1aa87-116">Email notifications</span></span>  
 <span data-ttu-id="1aa87-117">„[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ siunčia el. laiškus dėl išteklių užklausų toliau pateiktiems gavėjams nurodytu laiku.</span><span class="sxs-lookup"><span data-stu-id="1aa87-117">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="1aa87-118">Gavėjas</span><span class="sxs-lookup"><span data-stu-id="1aa87-118">Recipient</span></span>|<span data-ttu-id="1aa87-119">Įvykis</span><span class="sxs-lookup"><span data-stu-id="1aa87-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="1aa87-120">Projekto vadovas</span><span class="sxs-lookup"><span data-stu-id="1aa87-120">Project manager</span></span>|<span data-ttu-id="1aa87-121">- Kai išteklius užsiregistruoja vykdyti projektą naudodamas „Project Finder Mobile“ programėlę.</span><span class="sxs-lookup"><span data-stu-id="1aa87-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="1aa87-122">Ištekliai</span><span class="sxs-lookup"><span data-stu-id="1aa87-122">Resource</span></span>|<span data-ttu-id="1aa87-123">- Kai projekto darbą, kurį atlikti išteklius užsiregistravo, jau atliko kitas išteklius.</span><span class="sxs-lookup"><span data-stu-id="1aa87-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="1aa87-124">- Kada jų įgūdžių patvirtinimo užklausa patvirtinama arba atmetama.</span><span class="sxs-lookup"><span data-stu-id="1aa87-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="1aa87-125">- Kada jų registracijos vykdyti projektą užklausa patvirtinama arba atmetama.</span><span class="sxs-lookup"><span data-stu-id="1aa87-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="1aa87-126">Pastaba dėl privatumo</span><span class="sxs-lookup"><span data-stu-id="1aa87-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="1aa87-127">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="1aa87-127">See Also</span></span>  
 [<span data-ttu-id="1aa87-128">Rezervuojamų išteklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="1aa87-128">Set up resources</span></span>](../psa/set-up-resources.md)
