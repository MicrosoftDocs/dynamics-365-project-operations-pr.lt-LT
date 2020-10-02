---
title: Automatizuotų sąskaitų faktūrų kūrimo konfigūravimas
description: Šioje temoje pateikta informacija apie tai, kaip konfigūruojant sistemą automatiškai generuoti sąskaitas faktūras.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898136"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="a501d-103">Automatizuotų sąskaitų faktūrų kūrimo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a501d-103">Configure automated invoice creation</span></span>

<span data-ttu-id="a501d-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="a501d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a501d-105">Atlikite šiuos veiksmus, kad konfigūruotumėte automatinę sąskaitą faktūrą vykdyti projekto operacijose.</span><span class="sxs-lookup"><span data-stu-id="a501d-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="a501d-106">Pasirinkite **Parametrai** \> **Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="a501d-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="a501d-107">Sukurkite paketinę užduotį ir pavadinkite ją **„Project Operations“ sąskaitų faktūrų kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="a501d-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="a501d-108">Paketinės užduoties pavadinime turi būti terminas „Kurti sąskaitas faktūras“.</span><span class="sxs-lookup"><span data-stu-id="a501d-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="a501d-109">Lauke **Užduoties tipas** pažymėkite **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="a501d-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="a501d-110">Pagal numatytuosius nustatymus, parinktys **Dažnumas: kasdien** ir **Aktyvus** nustatytos į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a501d-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="a501d-111">Pasirinkite **Vykdyti darbo eigą**.</span><span class="sxs-lookup"><span data-stu-id="a501d-111">Select **Run Workflow**.</span></span> <span data-ttu-id="a501d-112">Dialogo lange **ieškoti įrašo** matysite tris darbo eigas:</span><span class="sxs-lookup"><span data-stu-id="a501d-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="a501d-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="a501d-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="a501d-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="a501d-114">ProcessRunner</span></span>
    - <span data-ttu-id="a501d-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="a501d-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="a501d-116">Pasirinkite **ProcessRunCaller**, o tada pažymėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="a501d-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="a501d-117">Kitame dialogo lange pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a501d-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="a501d-118">Po darbo eigos **Miego režimas**seka darbo eiga **Procesas**.</span><span class="sxs-lookup"><span data-stu-id="a501d-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="a501d-119">Taip pat galite pasirinkti **ProcessRunner** 5 veiksme.</span><span class="sxs-lookup"><span data-stu-id="a501d-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="a501d-120">Pažymėję **Gerai**, po darbo eigos **Procesas** seka darbo eiga **Miego režimas**.</span><span class="sxs-lookup"><span data-stu-id="a501d-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="a501d-121">Darbo eigos **ProcessRunCaller** ir **ProcessRunner** sukuria sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="a501d-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="a501d-122">**ProcessRunCaller** iškviečia **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="a501d-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="a501d-123">**ProcessRunner** yra darbo eiga, kuri iš tikrųjų sukuria sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="a501d-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="a501d-124">Ji taikoma visoms sutarties eilutėms, kurioms reikia sukurti SF, ir sukuria tų eilučių sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="a501d-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="a501d-125">Norint nustatyti sutarties eilutes, kurioms reikia sukurti SF, užduotis atsižvelgia į projekto eilutėms skirtos sąskaitos faktūros vykdymo datas.</span><span class="sxs-lookup"><span data-stu-id="a501d-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="a501d-126">Jei vienam projektui priklausančių projekto eilučių sąskaitos faktūros buvo vykdytos tuo pačiu metu, operacijos įtraukiamos į vieną sąskaitą faktūrą, kurioje yra dvi sąskaitos faktūros eilutės.</span><span class="sxs-lookup"><span data-stu-id="a501d-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="a501d-127">Jei nėra operacijų, skirtų išrašyti sąskaitas faktūras, užduotis nesukuria sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="a501d-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="a501d-128">Kai **ProcessRunner** baigia vykdymą, iškviečiamas **ProcessRunCaller**, pateikiamas pabaigos laikas ir yra uždaromas.</span><span class="sxs-lookup"><span data-stu-id="a501d-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="a501d-129">Tada **ProcessRunCaller** paleidžia laikmatį, kuris trunka 24 valandas nuo nurodyto pabaigos laiko.</span><span class="sxs-lookup"><span data-stu-id="a501d-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="a501d-130">Baigiantis laikmačio laikui, **ProcessRunCaller** uždaromas.</span><span class="sxs-lookup"><span data-stu-id="a501d-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="a501d-131">Paketinė proceso užduotis, skirta sąskaitoms faktūroms kurti, yra pasikartojanti užduotis.</span><span class="sxs-lookup"><span data-stu-id="a501d-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="a501d-132">Jei šis paketinis procesas vykdomas daug kartų, sukuriami keli užduoties egzemplioriai ir sukeliamos klaidos.</span><span class="sxs-lookup"><span data-stu-id="a501d-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="a501d-133">Todėl paketinį procesą reikia pradėti tik vieną kartą, o jį paleisti iš naujo reikia tik tuo atveju, jei jis sustos.</span><span class="sxs-lookup"><span data-stu-id="a501d-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="a501d-134">Paketinių sąskaitų faktūrų išrašymas vykdomas tik projekto sutarties eilutėse, sukonfigūruotose sąskaitų faktūrų grafike.</span><span class="sxs-lookup"><span data-stu-id="a501d-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="a501d-135">Sutarties eilutė su fiksuotos kainos atsiskaitymų metodu turi turėti sukonfigūruotus etapus.</span><span class="sxs-lookup"><span data-stu-id="a501d-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="a501d-136">Norint naudoti projekto sutarties eilutę su laiko ir medžiagų atsiskaitymo metodu, reikės nustatyti data pagrįstą sąskaitos faktūros grafiką.</span><span class="sxs-lookup"><span data-stu-id="a501d-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="a501d-137">Tokia pati tvarka galioja ir projektu pagrįstai sutarties eilutei.</span><span class="sxs-lookup"><span data-stu-id="a501d-137">The same applies to a project-based contract line.</span></span>     
