---
title: Išteklių naudingumo apžvalga
description: Šioje temoje pateikiama informacija apie išteklių naudojimą „Project Operations”.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d66b5fc642ef53adf1169ce891a7a5fa26b07d6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279328"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="3739f-103">Išteklių naudingumo apžvalga</span><span class="sxs-lookup"><span data-stu-id="3739f-103">Resource utilization overview</span></span>

<span data-ttu-id="3739f-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="3739f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3739f-105">Ištekliai gali turėti tikslinį apmokėtiną naudojimą.</span><span class="sxs-lookup"><span data-stu-id="3739f-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="3739f-106">Šis tikslinis naudojimas apibrėžiamas kaip atributas išteklių numatytame vaidmenyje arba nustatomas atskiro rezervuojamo ištekliaus įraše.</span><span class="sxs-lookup"><span data-stu-id="3739f-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="3739f-107">Naudojimo skaičiavimai pagrįsti faktinėmis valandomis, apie kurias ištekliai pranešė naudodami patvirtintus laiko įrašus.</span><span class="sxs-lookup"><span data-stu-id="3739f-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="3739f-108">Naudojimo skaičiavimui naudojamos toliau nurodytos formulės.</span><span class="sxs-lookup"><span data-stu-id="3739f-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="3739f-109">Apmokėtinas naudojimas = apmokestinamos faktinės valandos ÷ išteklių pajėgumas</span><span class="sxs-lookup"><span data-stu-id="3739f-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="3739f-110">Neapmokėtinas naudojimas = faktinis laikas su apmokėtino tipo ID = neapmokestinamas, papildomas arba negalimas ÷ išteklių pajėgumas</span><span class="sxs-lookup"><span data-stu-id="3739f-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="3739f-111">Vidinis = faktinis laikas be pardavimo sutarties ÷ išteklių pajėgumas</span><span class="sxs-lookup"><span data-stu-id="3739f-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="3739f-112">Išteklių pajėgumas = išteklių darbo valandos – išvykęs – ne darbo dienos</span><span class="sxs-lookup"><span data-stu-id="3739f-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="3739f-113">Rodinį **Išteklių naudojimas** galite rasti skyde **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="3739f-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="3739f-114">Kiekvienas tinklelio langelis nurodo išteklių apmokėtiną naudojimą pagal laiką, pavyzdžiui, dieną, savaitę arba mėnesį.</span><span class="sxs-lookup"><span data-stu-id="3739f-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="3739f-115">Langeliams naudojamos toliau nurodytos spalvos.</span><span class="sxs-lookup"><span data-stu-id="3739f-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="3739f-116">**Žalia**: apmokėtinas naudojimas > = tikslinis išteklių naudojimas</span><span class="sxs-lookup"><span data-stu-id="3739f-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="3739f-117">**Geltona**: tikslinis naudojimas – 20 < = apmokėtinas naudojimas < tikslinis naudojimas</span><span class="sxs-lookup"><span data-stu-id="3739f-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="3739f-118">**Raudona**: apmokėtinas naudojimas < = tikslinis naudojimas – 20</span><span class="sxs-lookup"><span data-stu-id="3739f-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="3739f-119">Kadangi rodinys **Išteklių naudojimas** pagrįstas grafiko lenta, galite naudoti grafiko lentos filtravimo galimybes, kad filtruotumėte rezultatus.</span><span class="sxs-lookup"><span data-stu-id="3739f-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="3739f-120">Reikia, kad tinkleliui nustatytumėte tikslinį naudojimą arba pagal vaidmenį, arba individualų išteklių.</span><span class="sxs-lookup"><span data-stu-id="3739f-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="3739f-121">Norėdami atlikti tokius nustatymus, eikite į **Ištekliai** > **Išteklių vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="3739f-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="3739f-122">Be to, kiekvienam rezervuojamam ištekliui reikia priskirti numatytąjį vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="3739f-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="3739f-123">Eikite į **Ištekliai** > **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="3739f-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="3739f-124">Skirtuke **„Project Service”** patikrinkite, kad nustatytas išteklių vaidmuo ir kad laukas **Yra numatytasis** nustatytas kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="3739f-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="3739f-125">Galite įtraukti papildomų vaidmenų, kai **Kaip numatytasis**  = **Ne**.</span><span class="sxs-lookup"><span data-stu-id="3739f-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="3739f-126">Vaidmuo, kai **Yra numatytasis**  = **Taip**, naudojamas išteklių naudojimui įvertinti pagal to vaidmens tikslą.</span><span class="sxs-lookup"><span data-stu-id="3739f-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="3739f-127">Skirtuke **Project Service** taip pat galite ištekliui nustatyti individualų tikslinį naudojimą.</span><span class="sxs-lookup"><span data-stu-id="3739f-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="3739f-128">Tada naudojimo skaičiavimui naudojamas šis tikslinis naudojamas, kad būtų įvertintas išteklių tikslas, o ne išteklių numatytojo vaidmens tikslas.</span><span class="sxs-lookup"><span data-stu-id="3739f-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="3739f-129">Išteklių naudojimas rodomas, tik jei šis išteklius turi patvirtintą ir apmokestinamą laiką periode, kuris rodomas tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="3739f-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]