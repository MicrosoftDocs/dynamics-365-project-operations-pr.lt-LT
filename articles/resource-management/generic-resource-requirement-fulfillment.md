---
title: Bendrųjų išteklių reikalavimų vykdymas
description: Šioje temoje pateikiama informacija apie įvardytų išteklių rezervavimą bendrųjų išteklių reikalavimui.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c4d02fd589d4a5d39380688852377f57fceb05b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130318"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="c6adc-103">Bendrųjų išteklių reikalavimų vykdymas</span><span class="sxs-lookup"><span data-stu-id="c6adc-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="c6adc-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="c6adc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c6adc-105">Galite rezervuoti įvardytą išteklių, jei norite pakeisti bendrąjį išteklių, kuriam taikomas ištekliaus reikalavimas.</span><span class="sxs-lookup"><span data-stu-id="c6adc-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="c6adc-106">Puslapyje **Projektai** pasirinkite skirtuką **Komanda**.</span><span class="sxs-lookup"><span data-stu-id="c6adc-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="c6adc-107">Sąraše pasirinkite bendrąjį išteklių, kuriam taikomas ištekliaus reikalavimas, ir spustelėkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="c6adc-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="c6adc-108">Arba atidarykite ištekliaus reikalavimą ir spustelėkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="c6adc-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="c6adc-109">Puslapyje **Pagalbinė planavimo priemonė** pasirinkite įvardytą išteklių, kurį norite rezervuoti savo projekto komandoje, ir spustelėkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="c6adc-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="c6adc-110">Atlikus rezervavimą ir įvardytam ištekliui jį įvykdžius, bendrasis išteklius pakeičiamas įvardytu ištekliumi.</span><span class="sxs-lookup"><span data-stu-id="c6adc-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="c6adc-111">Priskyrimus, nurodytus grafike, taip pat galima atnaujinti naudojant įvardytą išteklių.</span><span class="sxs-lookup"><span data-stu-id="c6adc-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="c6adc-112">Bendrojo ištekliaus reikalavimo įvykdymas naudojant kelis įvardytus išteklius</span><span class="sxs-lookup"><span data-stu-id="c6adc-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="c6adc-113">Bendrojo ištekliaus reikalavimas įvykdomas naudojant kelis įvardytus išteklius panašiai, kaip ir priskiriant vieną įvardytą išteklių.</span><span class="sxs-lookup"><span data-stu-id="c6adc-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="c6adc-114">Pavyzdžiui, turite penkių dienų trukmės užduotį, kuriai skirta 120 darbo valandų.</span><span class="sxs-lookup"><span data-stu-id="c6adc-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="c6adc-115">Šios užduoties per penkių dienų darbo savaitę negali atlikti vienas išteklius, dirbantis įprastą aštuonių valandų trukmės darbo dieną.</span><span class="sxs-lookup"><span data-stu-id="c6adc-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="c6adc-116">120 valandų reikalavimas per penkias dienas skirtas robotų technikai, dirbančiai 24 valandas per parą.</span><span class="sxs-lookup"><span data-stu-id="c6adc-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="c6adc-117">Tai yra pavyzdys, kai norint įvykdyti bendrojo ištekliaus užklausą reikia kelių įvardytų išteklių.</span><span class="sxs-lookup"><span data-stu-id="c6adc-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="c6adc-118">Norint įvykdyti reikalavimą jums reikės rezervuoti kelis išteklius.</span><span class="sxs-lookup"><span data-stu-id="c6adc-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="c6adc-119">Šis scenarijus iš esmės skiriasi tuo, kad bendrasis išteklius lieka komandoje priskirtas užduočiai, o rezervuoti įvardytų išteklių komandos nariai nėra priskirti pareigų daliai.</span><span class="sxs-lookup"><span data-stu-id="c6adc-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="c6adc-120">Projekto vadovas gali atitinkamai priskirti darbą įvardytiems ištekliams.</span><span class="sxs-lookup"><span data-stu-id="c6adc-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="c6adc-121">Išskaidydamas kelis išteklių rezervavimus pagal užduočių priskyrimus, projektų vadovas gali naudotis rodiniu **Suderinimas**.</span><span class="sxs-lookup"><span data-stu-id="c6adc-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="c6adc-122">Šis procesas neatliekamas automatiškai, nes bet kokio sudėtingesnio scenarijaus atveju, nei aprašoma ankstesniame paprastame pavyzdyje, kaip antai, kai reikalavimą sudaro užduočių paketas, sistema turėtų numanyti, kaip projekto vadovas ketina priskirti.</span><span class="sxs-lookup"><span data-stu-id="c6adc-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="c6adc-123">Kadangi sistema negali suprasti ketinimų, prielaidos gali būti kitokios, nei numatyta, ir gaunamas netinkamas arba nenuspėjamas rezultatas.</span><span class="sxs-lookup"><span data-stu-id="c6adc-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="c6adc-124">Nuspėjami rezultatai gaunami, kai bendrieji ištekliai lieka priskirti tol, kol projekto vadovas sąmoningai sukuria priskyrimus naudodamasis rodiniu **Suderinimas**.</span><span class="sxs-lookup"><span data-stu-id="c6adc-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


