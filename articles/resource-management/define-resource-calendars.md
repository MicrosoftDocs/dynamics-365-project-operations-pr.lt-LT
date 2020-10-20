---
title: Išteklių kalendorių apibrėžimas
description: Šioje temoje pateikta informacija apie tai, kaip apibrėžti darbo valandų kalendorius, skirtus „Project Operations“ ištekliams.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961908"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="ddfe6-103">Išteklių kalendorių apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="ddfe6-103">Define resource calendars</span></span>

<span data-ttu-id="ddfe6-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="ddfe6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ddfe6-105">Kiekvienas projekto rezervuojamasis išteklius turi turėti darbo valandų kalendorių, kad būtų galima apibrėžti jų pasiekiamumą.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="ddfe6-106">Išteklių darbo valandos gali būti apibrėžtos dviem būdais:</span><span class="sxs-lookup"><span data-stu-id="ddfe6-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="ddfe6-107">Išteklių individualaus kalendoriaus taisyklių apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="ddfe6-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="ddfe6-108">Ištekliaus esamo kalendoriaus šablono taikymas</span><span class="sxs-lookup"><span data-stu-id="ddfe6-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="ddfe6-109">Ištekliaus darbo valandų nustatymas</span><span class="sxs-lookup"><span data-stu-id="ddfe6-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="ddfe6-110">Meniu **Ištekliai** pažymėkite **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="ddfe6-111">Tinklelio rodinyje pažymėkite taikomą **Rezervuojamą išteklių**.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="ddfe6-112">Puslapyje **Išteklių išsami informacija** pažymėkite skirtuką **Darbo valandos**. Pagal numatytuosius nustatymus, rezervuojamų išteklių kalendorius nustato numatytojo darbo valandų šablono, apibrėžto organizacijoje, darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="ddfe6-113">Norėdami atnaujinti darbo valandas, dešiniuoju pelės mygtuku spustelėkite norimos apibrėžti kalendoriaus taisyklės pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="ddfe6-114">Pasinaudokite kalendoriaus taisyklės meniu, kad apibrėžtumėte tam tikros dienos, likusios sekos arba viso kalendoriaus, kalendoriaus taisyklę.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="ddfe6-115">Pažymėję parinktį, galite apibrėžti:</span><span class="sxs-lookup"><span data-stu-id="ddfe6-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="ddfe6-116">Savaitės dieną, kai taikomos darbo valandos.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="ddfe6-117">Darbo laiką kiekvieną dieną.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-117">The working times within each day.</span></span>
    - <span data-ttu-id="ddfe6-118">Kalendoriaus taisyklės laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="ddfe6-119">Jei taikoma, taisyklėje taip pat gali būti nurodytas ne darbo laikas.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="ddfe6-120">Kalendoriaus šablono taikymas ištekliui</span><span class="sxs-lookup"><span data-stu-id="ddfe6-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="ddfe6-121">Meniu **Ištekliai** pažymėkite **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="ddfe6-122">Tinklelio rodinyje pažymėkite iki 25 **Rezervuojamų išteklių**, kad juos atnaujintumėte.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="ddfe6-123">Pažymėkite **Nustatyti kalendorių** ir dialogo langas pasiūlys galimų darbo valandų šablonų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="ddfe6-124">Pasirinkite norimą naudoti šabloną ir pažymėkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="ddfe6-124">Select the template you want to use, and then select **Apply**.</span></span>
