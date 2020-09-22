---
title: Kainoraščio kūrimas
description: Kainoraščio kūrimas „Project Service“
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: bdd05aea-27a3-431d-9a80-2e220fb25e53
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 756af2fe3bc73d478b0355493aae6f0e49ac5835
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753785"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="415f2-103">Kainoraščio kūrimas („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="415f2-103">Create a price list (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="415f2-104">Kainoraščiai pateikia šabloną, kurį naudodami jūsų klientų vadybininkai gali kurti pasiūlymus bei projektus ir įvertinti projektų savikainą.</span><span class="sxs-lookup"><span data-stu-id="415f2-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="415f2-105">Kainoraščiuose eilutės elementų sąrašo formatu išvardijami vaidmenys bei išlaidos ir kaina, mokėtina už kiekvieną iš jų.</span><span class="sxs-lookup"><span data-stu-id="415f2-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="415f2-106">Galite sukurti kelis kainoraščius ir atskirai tvarkyti skirtingų regionų, kuriuose parduodate savo produktus, arba skirtingų pardavimo kanalų kainas.</span><span class="sxs-lookup"><span data-stu-id="415f2-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="415f2-107">Pravartu sukurti bent vieną kainoraštį kiekviena valiuta, kuria planuojate išrašyti sąskaitas savo klientams.</span><span class="sxs-lookup"><span data-stu-id="415f2-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="415f2-108">Norėdami sukurti sąmatas už darbą, kuris bus atliekamas, įsitikinkite, kad yra sudaryta kiekvieno projekto pagrįsta savikaina ir pardavimo kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="415f2-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="415f2-109">Sudarykite numatytąją savikainą ir pardavimo kainoraštį, kuris bus taikomas visiems jūsų organizacijoje sukurtiems projektams.</span><span class="sxs-lookup"><span data-stu-id="415f2-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="415f2-110">Kainoraščiai grindžiami vaidmenų ir išlaidų kategorijomis, todėl prieš kurdami kainoraštį įsitikinkite, kad jau esate sukonfigūravę vaidmenų ir išlaidų kategorijas, kurias norite naudoti kurdami kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="415f2-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="415f2-111">Pasirinkite **Project Service > Kainoraščiai**.</span><span class="sxs-lookup"><span data-stu-id="415f2-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="415f2-112">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="415f2-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="415f2-113">Parinktyje **Kontekstas** pasirinkite, ar šis kainoraštis skiriamas kategorijai **Savikaina**, **Pirkimas** ar **Sales**.</span><span class="sxs-lookup"><span data-stu-id="415f2-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="415f2-114">Lauke **Pavadinimas** įveskite kainoraščio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="415f2-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="415f2-115">Lauke **Valiuta** pasirinkite valiutą, kurią planuojate naudoti išrašydami sąskaitas ar įvertindami savikainą.</span><span class="sxs-lookup"><span data-stu-id="415f2-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="415f2-116">Lauke **Laiko vienetas** nurodykite laikotarpį, kuriuo bus taikoma ta kaina, pvz., dieną ar valandą.</span><span class="sxs-lookup"><span data-stu-id="415f2-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="415f2-117">Užpildykite laukus **Pradžios data**, **Pabaigos data** ir **Aprašas** reikiama informacija.</span><span class="sxs-lookup"><span data-stu-id="415f2-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="415f2-118">Spustelėkite **Įrašyti**, kad sukurtumėte įrašą, kurį vėliau galėsite redaguoti.</span><span class="sxs-lookup"><span data-stu-id="415f2-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="415f2-119">Norėdami į kainoraštį įtraukti vaidmens kainą, spustelėkite **+**, esantį prie parinkties **Vaidmenų kainos**.</span><span class="sxs-lookup"><span data-stu-id="415f2-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="415f2-120">Srityje **Vaidmens kaina** įveskite išsamią informaciją, o tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="415f2-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="415f2-121">Tęskite pridėdami tiek vaidmenų kainų, kiek reikia.</span><span class="sxs-lookup"><span data-stu-id="415f2-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="415f2-122">Baigę spustelėkite mygtuką **Įrašyti**, esantį ekrano apatiniame dešiniame kampe.</span><span class="sxs-lookup"><span data-stu-id="415f2-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="415f2-123">Norėdami į kainoraštį įtraukti išlaidų kategorijos kainą, spustelėkite **+**, esantį prie parinkties **Kategorijų kainos**.</span><span class="sxs-lookup"><span data-stu-id="415f2-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="415f2-124">Srityje **Operacijos kategorijos kaina** įveskite išsamią informaciją, o tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="415f2-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="415f2-125">Tęskite pridėdami tiek kategorijų kainų, kiek reikia.</span><span class="sxs-lookup"><span data-stu-id="415f2-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="415f2-126">Baigę spustelėkite mygtuką **Įrašyti**, esantį ekrano apatiniame dešiniame kampe.</span><span class="sxs-lookup"><span data-stu-id="415f2-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="415f2-127">Norėdami kainoraštį papildyti kainoraščio elementais, spustelėkite **+**, esantį prie parinkties **Kainoraščio elementai**.</span><span class="sxs-lookup"><span data-stu-id="415f2-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="415f2-128">Srityje **Kainoraščio elementas** įveskite išsamią informaciją, o tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="415f2-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="415f2-129">Tęskite pridėdami tiek kainoraščio elementų, kiek reikia.</span><span class="sxs-lookup"><span data-stu-id="415f2-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="415f2-130">Baigę spustelėkite mygtuką **Įrašyti**, esantį ekrano apatiniame dešiniame kampe.</span><span class="sxs-lookup"><span data-stu-id="415f2-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="415f2-131">Norėdami į kainoraštį įtraukti teritorijos ryšius, spustelėkite **+**, esantį prie parinkties **Teritorijos ryšiai**.</span><span class="sxs-lookup"><span data-stu-id="415f2-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="415f2-132">Lange **Naujas ryšys** įveskite išsamią informaciją, o tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="415f2-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="415f2-133">Tęskite pridėdami tiek teritorijos ryšių, kiek reikia.</span><span class="sxs-lookup"><span data-stu-id="415f2-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="415f2-134">Baigę spustelėkite mygtuką **Įrašyti**, esantį ekrano apatiniame dešiniame kampe.</span><span class="sxs-lookup"><span data-stu-id="415f2-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="415f2-135">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="415f2-135">See Also</span></span>  
 [<span data-ttu-id="415f2-136">„Project Service Automation“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="415f2-136">Configure Project Service Automation</span></span>](../project-service/configure.md)
