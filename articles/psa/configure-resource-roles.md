---
title: Išteklių vaidmenų konfigūravimas
description: Išteklių vaidmenų konfigūravimas „Project Service“
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
ms.openlocfilehash: 5f899d17980df16602c964bab4bbab1e976b3ebf
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080834"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="3cf2d-103">Išteklių vaidmenų konfigūravimas („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="3cf2d-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3cf2d-104">Projektų planavime vaidmenims tenka svarbus vaidmuo nustatant reikalavimus ištekliams ar projekto savikainą.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="3cf2d-105">Kiekvienam vaidmeniui, kurio reikia projektui, turite sukurti išteklių vaidmenį ir susieti su tuo vaidmeniu įgūdžius bei kvalifikaciją.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="3cf2d-106">Pvz., galbūt norėsite sukurti programų kūrėjo, projektų vadovo ar žaidimų testuotojo vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="3cf2d-107">Taip pat nustatysite įgūdžių ir kvalifikacijos lygius, reikalingus šiam vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="3cf2d-108">Sukonfigūruodami išteklių vaidmenis, užtikrinsite veiksmingą projektų vertinimą organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="3cf2d-109">Taip pat įsitikinkite, kad tiksliai nustatėte atsiskaitymo tipą.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="3cf2d-110">Elementas, kurio atsiskaitymo tipas nustatytas kaip neapmokestinamas, sutarties ar pasiūlymo eilutėse nerodomas.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="3cf2d-111">Nustatę išteklių vaidmenis, naudodamiesi kainoraščiu galite nustatyti savikainą ir pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="3cf2d-112">Su kiekvienu norimu įtraukti vaidmeniu atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="3cf2d-113">Pasirinkite **Project Service > Išteklių vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="3cf2d-114">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="3cf2d-115">Srityje **Bendra** , lauke **Pavadinimas** įveskite vaidmens pavadinimą, o tada tinkamai užpildykite kitus laukus.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-115">In the **General** area, enter a name for the role in **Name** , and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="3cf2d-116">Spustelėkite **Įrašyti** , kad sukurtumėte įrašą, kurį vėliau galėsite redaguoti.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="3cf2d-117">Jei norite pridėti įgūdį, srityje **Įgūdžiai** spustelėkite **+**.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="3cf2d-118">Srityje **Vaidmens kompetencijos reikalavimai** spustelėkite lauke **Įgūdis** , spustelėkite mygtuką **Ieškoti** , o tada pasirinkite įgūdį.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="3cf2d-119">Pasirinkite to įgūdžiui kvalifikaciją, o tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="3cf2d-120">Tęskite pridėdami tiek įgūdžių, kiek reikia.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="3cf2d-121">Baigę spustelėkite mygtuką **Įrašyti** , esantį ekrano apatiniame dešiniame kampe.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="3cf2d-122">Kad šį išteklių vaidmenį būtų galima naudoti projektuose, spustelėkite **Aktyvinti**.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3cf2d-123">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="3cf2d-123">See Also</span></span>  
 [<span data-ttu-id="3cf2d-124">Rezervuojamų išteklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="3cf2d-124">Set up resources</span></span>](../psa/set-up-resources.md)
