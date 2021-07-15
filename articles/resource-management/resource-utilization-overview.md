---
title: Išteklių naudingumo apžvalga
description: Šioje temoje pateikiama informacija apie išteklių naudojimą „Project Operations”.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367946"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="77ba7-103">Išteklių naudingumo apžvalga</span><span class="sxs-lookup"><span data-stu-id="77ba7-103">Resource utilization overview</span></span>

<span data-ttu-id="77ba7-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="77ba7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="77ba7-105">Ištekliai gali turėti tikslinį apmokėtiną naudojimą.</span><span class="sxs-lookup"><span data-stu-id="77ba7-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="77ba7-106">Šis tikslinis naudojimas apibrėžiamas kaip atributas išteklių numatytame vaidmenyje arba nustatomas atskiro rezervuojamo ištekliaus įraše.</span><span class="sxs-lookup"><span data-stu-id="77ba7-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="77ba7-107">Naudojimo skaičiavimai pagrįsti faktinėmis valandomis, apie kurias ištekliai pranešė naudodami patvirtintus laiko įrašus.</span><span class="sxs-lookup"><span data-stu-id="77ba7-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="77ba7-108">Naudojimo skaičiavimui naudojamos toliau nurodytos formulės.</span><span class="sxs-lookup"><span data-stu-id="77ba7-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="77ba7-109">Apmokėtinas naudojimas = apmokestinamos faktinės valandos ÷ išteklių pajėgumas</span><span class="sxs-lookup"><span data-stu-id="77ba7-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="77ba7-110">Neapmokėtinas naudojimas = faktinis laikas su apmokėtino tipo ID = neapmokestinamas, papildomas arba negalimas ÷ išteklių pajėgumas</span><span class="sxs-lookup"><span data-stu-id="77ba7-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="77ba7-111">Vidinis = faktinis laikas be pardavimo sutarties ÷ išteklių pajėgumas</span><span class="sxs-lookup"><span data-stu-id="77ba7-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="77ba7-112">Išteklių pajėgumas = išteklių darbo valandos – išvykęs – ne darbo dienos</span><span class="sxs-lookup"><span data-stu-id="77ba7-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="77ba7-113">Rodinį **Išteklių naudojimas** galite rasti skyde **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="77ba7-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="77ba7-114">Kiekvienas tinklelio langelis nurodo išteklių apmokėtiną naudojimą pagal laiką, pavyzdžiui, dieną, savaitę arba mėnesį.</span><span class="sxs-lookup"><span data-stu-id="77ba7-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="77ba7-115">Langeliams naudojamos toliau nurodytos spalvos.</span><span class="sxs-lookup"><span data-stu-id="77ba7-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="77ba7-116">**Žalia**: apmokėtinas naudojimas > = tikslinis išteklių naudojimas</span><span class="sxs-lookup"><span data-stu-id="77ba7-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="77ba7-117">**Geltona**: tikslinis naudojimas – 20 < = apmokėtinas naudojimas < tikslinis naudojimas</span><span class="sxs-lookup"><span data-stu-id="77ba7-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="77ba7-118">**Raudona**: apmokėtinas naudojimas < = tikslinis naudojimas – 20</span><span class="sxs-lookup"><span data-stu-id="77ba7-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="77ba7-119">Kadangi rodinys **Išteklių naudojimas** pagrįstas grafiko lenta, galite naudoti grafiko lentos filtravimo galimybes, kad filtruotumėte rezultatus.</span><span class="sxs-lookup"><span data-stu-id="77ba7-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="77ba7-120">Reikia, kad tinkleliui nustatytumėte tikslinį naudojimą arba pagal vaidmenį, arba individualų išteklių.</span><span class="sxs-lookup"><span data-stu-id="77ba7-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="77ba7-121">Norėdami atlikti tokius nustatymus, eikite į **Ištekliai** > **Išteklių vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="77ba7-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="77ba7-122">Be to, kiekvienam rezervuojamam ištekliui reikia priskirti numatytąjį vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="77ba7-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="77ba7-123">Eikite į **Ištekliai** > **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="77ba7-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="77ba7-124">Skirtuke **„Project Service”** patikrinkite, kad nustatytas išteklių vaidmuo ir kad laukas **Yra numatytasis** nustatytas kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="77ba7-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="77ba7-125">Galite įtraukti papildomų vaidmenų, kai **Kaip numatytasis**  = **Ne**.</span><span class="sxs-lookup"><span data-stu-id="77ba7-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="77ba7-126">Vaidmuo, kai **Yra numatytasis**  = **Taip**, naudojamas išteklių naudojimui įvertinti pagal to vaidmens tikslą.</span><span class="sxs-lookup"><span data-stu-id="77ba7-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="77ba7-127">Skirtuke **Project Service** taip pat galite ištekliui nustatyti individualų tikslinį naudojimą.</span><span class="sxs-lookup"><span data-stu-id="77ba7-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="77ba7-128">Tada naudojimo skaičiavimui naudojamas šis tikslinis naudojamas, kad būtų įvertintas išteklių tikslas, o ne išteklių numatytojo vaidmens tikslas.</span><span class="sxs-lookup"><span data-stu-id="77ba7-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="77ba7-129">Išteklių naudojimas rodomas, tik jei šis išteklius turi patvirtintą ir apmokestinamą laiką periode, kuris rodomas tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="77ba7-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]