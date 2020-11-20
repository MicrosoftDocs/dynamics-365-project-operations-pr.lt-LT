---
title: Projekto kalendorių apibrėžimas
description: Šioje temoje pateikta informacija apie projekto kalendoriaus naudojimą projekto grafike sekti.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131668"
---
# <a name="define-project-calendars"></a><span data-ttu-id="45cac-103">Projekto kalendorių apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="45cac-103">Define project calendars</span></span>

<span data-ttu-id="45cac-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="45cac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="45cac-105">Norėdami sukurti projekto grafiką, sukuriate projekto kalendoriaus šabloną, nurodydami dienos darbo valandų skaičių ir kada įmonės nedirba.</span><span class="sxs-lookup"><span data-stu-id="45cac-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="45cac-106">Norėdami sukurti projekto kalendoriaus šabloną, susiejate darbo šabloną su projekto **Kalendoriaus šablonas** lauku.</span><span class="sxs-lookup"><span data-stu-id="45cac-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="45cac-107">Norėdami sukurti darbo šabloną, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="45cac-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="45cac-108">Kairėje naršymo srityje pasirinkite **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="45cac-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="45cac-109">Sąrašo puslapyje **Ištekliai** atidarykite vartotojo įrašą, tada pažymėkite **Rodyti darbo valandas**.</span><span class="sxs-lookup"><span data-stu-id="45cac-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="45cac-110">Įsitikinkite, kad naršyklėje leidžiami iššokantieji langai.</span><span class="sxs-lookup"><span data-stu-id="45cac-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="45cac-111">Taip galėsite matyti ištekliui nustatytas darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="45cac-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="45cac-112">Skirtuke **Mėnesio rodinys** spustelėkite **Nustatyti**.</span><span class="sxs-lookup"><span data-stu-id="45cac-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="45cac-113">Bus rodomas trijų parinkčių sąrašas:</span><span class="sxs-lookup"><span data-stu-id="45cac-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="45cac-114">Naujas savaitės grafikas</span><span class="sxs-lookup"><span data-stu-id="45cac-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="45cac-115">Vienos dienos darbo grafikas</span><span class="sxs-lookup"><span data-stu-id="45cac-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="45cac-116">Ne darbo laikas</span><span class="sxs-lookup"><span data-stu-id="45cac-116">Time Off</span></span>

4. <span data-ttu-id="45cac-117">Pažymėkite **Naujas savaitės grafikas** ir nustatykite šio išteklių grafiko parinktis.</span><span class="sxs-lookup"><span data-stu-id="45cac-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="45cac-118">Galite nustatyti pasikartojantį savaitinį grafiką, dienos darbo valandų parametrus, įmonės ne darbo laiką ir kt.</span><span class="sxs-lookup"><span data-stu-id="45cac-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="45cac-119">Nustatykite datų intervalą pasirinkdami **Įrašyti**, tada spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="45cac-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="45cac-120">Grįžkite į sąrašo puslapį **Ištekliai** ir pažymėkite išteklių, kuriam nustatėte darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="45cac-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="45cac-121">Pažymėkite **Nustatyti kalendorių kaip** nustatyti darbo šabloną.</span><span class="sxs-lookup"><span data-stu-id="45cac-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="45cac-122">Dialogo lange **Darbo šablonas** įveskite darbo šablono pavadinimą, tada pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="45cac-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="45cac-123">Dabar galite susieti darbo šabloną su projekto kalendoriaus šablonu.</span><span class="sxs-lookup"><span data-stu-id="45cac-123">You can now associate the work template with a project calendar template.</span></span>
