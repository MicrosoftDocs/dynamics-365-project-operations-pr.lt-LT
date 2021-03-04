---
title: Įvardytų išteklių rezervavimas iš išteklių reikalavimų
description: Šioje temoje pateikiama informacija apie įvardytų išteklių rezervavimą bendrųjų išteklių reikalavimui.
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145109"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="cca45-103">Įvardytų išteklių rezervavimas iš išteklių reikalavimų</span><span class="sxs-lookup"><span data-stu-id="cca45-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cca45-104">Galite rezervuoti įvardytą išteklių, jei norite pakeisti bendrąjį išteklių, kuriam taikomas ištekliaus reikalavimas.</span><span class="sxs-lookup"><span data-stu-id="cca45-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="cca45-105">Programos „Project Service Automation“ (PSA) puslapyje **Projektai** spustelėkite skirtuką **Komanda**.</span><span class="sxs-lookup"><span data-stu-id="cca45-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="cca45-106">Sąraše pasirinkite bendrąjį išteklių, kuriam taikomas ištekliaus reikalavimas, ir spustelėkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="cca45-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="cca45-107">Arba atidarykite ištekliaus reikalavimą ir spustelėkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="cca45-107">Or, open the resource requirement and then click **Book**.</span></span>


![Bendrojo komandos nario rezervavimas](media/RM-how-to-14.png)


3. <span data-ttu-id="cca45-109">Puslapyje **Pagalbinė planavimo priemonė** pasirinkite įvardytą išteklių, kurį norite rezervuoti savo projekto komandoje, ir spustelėkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="cca45-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Bendrojo komandos nario rezervavimas naudojant pagalbinę planavimo priemonę](media/RM-how-to-15.png)

<span data-ttu-id="cca45-111">Atlikus rezervavimą ir įvardytam ištekliui jį įvykdžius, bendrasis išteklius pakeičiamas įvardytu ištekliumi.</span><span class="sxs-lookup"><span data-stu-id="cca45-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Įvardyto komandos nario pakeitimas bendruoju komandos nariu](media/RM-how-to-16.png)

<span data-ttu-id="cca45-113">Priskyrimus, nurodytus grafike, taip pat galima atnaujinti naudojant įvardytą išteklių.</span><span class="sxs-lookup"><span data-stu-id="cca45-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Įvardyto komandos nario priskyrimas projekto užduotims](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="cca45-115">Bendrojo ištekliaus reikalavimo įvykdymas naudojant kelis įvardytus išteklius</span><span class="sxs-lookup"><span data-stu-id="cca45-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="cca45-116">Bendrojo ištekliaus reikalavimas įvykdomas naudojant kelis įvardytus išteklius panašiai, kaip ir priskiriant vieną įvardytą išteklių.</span><span class="sxs-lookup"><span data-stu-id="cca45-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="cca45-117">Pavyzdžiui, turite penkių dienų trukmės užduotį, kuriai skirta 120 darbo valandų.</span><span class="sxs-lookup"><span data-stu-id="cca45-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="cca45-118">Šios užduoties per penkių dienų darbo savaitę negali atlikti vienas išteklius, dirbantis įprastą aštuonių valandų trukmės darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="cca45-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Užduotis, kurią reikia atlikti per penkias dienas, dirbant 120 valandų](media/RM-how-to-21.png)

<span data-ttu-id="cca45-120">120 valandų reikalavimas per penkias dienas skirtas robotų technikai, dirbančiai 24 valandas per parą.</span><span class="sxs-lookup"><span data-stu-id="cca45-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Dienos reikalavimas](media/RM-how-to-22.png)

<span data-ttu-id="cca45-122">Tai yra pavyzdys, kai norint įvykdyti bendrojo ištekliaus užklausą reikia kelių įvardytų išteklių.</span><span class="sxs-lookup"><span data-stu-id="cca45-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="cca45-123">Norint įvykdyti reikalavimą jums reikės rezervuoti kelis išteklius.</span><span class="sxs-lookup"><span data-stu-id="cca45-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Kelių išteklių rezervavimas siekiant įvykdyti reikalavimą](media/RM-how-to-23.png)

<span data-ttu-id="cca45-125">Šis scenarijus iš esmės skiriasi tuo, kad bendrasis išteklius lieka komandoje priskirtas užduočiai, o rezervuoti įvardytų išteklių komandos nariai nėra priskirti pareigų daliai.</span><span class="sxs-lookup"><span data-stu-id="cca45-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="cca45-126">Projekto vadovas gali atitinkamai priskirti darbą įvardytiems ištekliams.</span><span class="sxs-lookup"><span data-stu-id="cca45-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="cca45-127">Išskaidydamas kelis išteklių rezervavimus pagal užduočių priskyrimus, projektų vadovas gali naudotis rodiniu **Suderinimas**.</span><span class="sxs-lookup"><span data-stu-id="cca45-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="cca45-128">Šis procesas neatliekamas automatiškai, nes bet kokio sudėtingesnio scenarijaus atveju, nei aprašoma ankstesniame paprastame pavyzdyje, kaip antai, kai reikalavimą sudaro užduočių paketas, sistema turėtų numanyti, kaip projekto vadovas ketina priskirti.</span><span class="sxs-lookup"><span data-stu-id="cca45-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="cca45-129">Kadangi sistema negali suprasti ketinimų, yra tikimybė, kad ji numanys kitaip, nei ketinama, ir gautas rezultatas bus netinkamas arba nenuspėjamas.</span><span class="sxs-lookup"><span data-stu-id="cca45-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="cca45-130">Nuspėjami rezultatai gaunami, kai bendrieji ištekliai lieka priskirti tol, kol projekto vadovas sąmoningai sukuria priskyrimus naudodamasis rodiniu **Suderinimas**.</span><span class="sxs-lookup"><span data-stu-id="cca45-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


