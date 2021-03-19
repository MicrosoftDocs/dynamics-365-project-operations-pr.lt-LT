---
title: Pajamų pripažinimo apžvalga
description: Šioje temoje pateikiama informacijos apie pajamų pripažinimą programoje „Project Operations”.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278878"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="bc85c-103">Pajamų pripažinimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="bc85c-103">Revenue recognition overview</span></span>

<span data-ttu-id="bc85c-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="bc85c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bc85c-105">Programoje „Dynamics 365 Project Operations“ pajamų pripažinimo principai skiriasi atsižvelgiant į pasirinktą atsiskaitymo metodą, taikomą projektui arba projekto daliai.</span><span class="sxs-lookup"><span data-stu-id="bc85c-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="bc85c-106">Šioje temoje pateikiama informacijos apie pajamų pripažinimą programoje „Project Operations”.</span><span class="sxs-lookup"><span data-stu-id="bc85c-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="bc85c-107">Operacijos, įtraukiamos naudojant atsiskaitymo už laiką ir medžiagas metodą</span><span class="sxs-lookup"><span data-stu-id="bc85c-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="bc85c-108">Išlaidų ir pajamų pripažinimas yra susiję tarpusavyje.</span><span class="sxs-lookup"><span data-stu-id="bc85c-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="bc85c-109">Operacijos išlaidos ir pardavimas, už kurį neišrašyta sąskaita, užregistruojami naudojant [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="bc85c-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="bc85c-110">Projekto išlaidų ir pajamų profilis nustato, ar pardavimo operacijos, už kurias neišrašyta sąskaita, registruojamos didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="bc85c-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="bc85c-111">Pasirinkus parinktį **Kaupti įplaukas**, sistema užregistruoja naudodama sąskaitas **NG – Pardavimo vertė** ir **Sukauptos įplaukos – Pardavimo vertė**.</span><span class="sxs-lookup"><span data-stu-id="bc85c-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="bc85c-112">Toliau pateikiamas šio metodo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="bc85c-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="bc85c-113">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="bc85c-113">Transaction type</span></span> | <span data-ttu-id="bc85c-114">Debetas / kreditas</span><span class="sxs-lookup"><span data-stu-id="bc85c-114">Debit/Credit</span></span> | <span data-ttu-id="bc85c-115">Suma</span><span class="sxs-lookup"><span data-stu-id="bc85c-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="bc85c-116">NG – Pardavimo vertė</span><span class="sxs-lookup"><span data-stu-id="bc85c-116">WIP Sales value</span></span> | <span data-ttu-id="bc85c-117">Debetas</span><span class="sxs-lookup"><span data-stu-id="bc85c-117">Debit</span></span> | <span data-ttu-id="bc85c-118">100</span><span class="sxs-lookup"><span data-stu-id="bc85c-118">100</span></span> |
  | <span data-ttu-id="bc85c-119">Sukauptos įplaukos – Pardavimo vertė</span><span class="sxs-lookup"><span data-stu-id="bc85c-119">Accrued revenue sales value</span></span> | <span data-ttu-id="bc85c-120">Kreditas</span><span class="sxs-lookup"><span data-stu-id="bc85c-120">Credit</span></span> | <span data-ttu-id="bc85c-121">100</span><span class="sxs-lookup"><span data-stu-id="bc85c-121">100</span></span> |

- <span data-ttu-id="bc85c-122">Pajamos pripažįstamos išrašant SF.</span><span class="sxs-lookup"><span data-stu-id="bc85c-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="bc85c-123">Sistema užregistruoja naudodama sąskaitą **įplaukos, kurioms išrašyta SF**.</span><span class="sxs-lookup"><span data-stu-id="bc85c-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="bc85c-124">Toliau pateikiamas šio metodo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="bc85c-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="bc85c-125">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="bc85c-125">Transaction type</span></span> | <span data-ttu-id="bc85c-126">Debetas / kreditas</span><span class="sxs-lookup"><span data-stu-id="bc85c-126">Debit/Credit</span></span> | <span data-ttu-id="bc85c-127">Suma</span><span class="sxs-lookup"><span data-stu-id="bc85c-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="bc85c-128">Kliento balansas</span><span class="sxs-lookup"><span data-stu-id="bc85c-128">Customer balance</span></span> | <span data-ttu-id="bc85c-129">Debetas</span><span class="sxs-lookup"><span data-stu-id="bc85c-129">Debit</span></span> | <span data-ttu-id="bc85c-130">120</span><span class="sxs-lookup"><span data-stu-id="bc85c-130">120</span></span> |
  | <span data-ttu-id="bc85c-131">Mokėtinas PVM</span><span class="sxs-lookup"><span data-stu-id="bc85c-131">Sales tax payable</span></span> | <span data-ttu-id="bc85c-132">Kreditas</span><span class="sxs-lookup"><span data-stu-id="bc85c-132">Credit</span></span> | <span data-ttu-id="bc85c-133">20</span><span class="sxs-lookup"><span data-stu-id="bc85c-133">20</span></span> |
  | <span data-ttu-id="bc85c-134">įplaukos, kurioms išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="bc85c-134">Invoiced Revenue</span></span> | <span data-ttu-id="bc85c-135">Kreditas</span><span class="sxs-lookup"><span data-stu-id="bc85c-135">Credit</span></span> | <span data-ttu-id="bc85c-136">100</span><span class="sxs-lookup"><span data-stu-id="bc85c-136">100</span></span> |

- <span data-ttu-id="bc85c-137">Jei įplaukos buvo sukauptos, kai yra užregistruojamas pardavimas, už kurį neišrašyta sąskaita, sistema atšauks sukauptas įplaukas išrašydama SF.</span><span class="sxs-lookup"><span data-stu-id="bc85c-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="bc85c-138">Operacijos tipas</span><span class="sxs-lookup"><span data-stu-id="bc85c-138">Transaction type</span></span> | <span data-ttu-id="bc85c-139">Debetas / kreditas</span><span class="sxs-lookup"><span data-stu-id="bc85c-139">Debit/Credit</span></span> | <span data-ttu-id="bc85c-140">Suma</span><span class="sxs-lookup"><span data-stu-id="bc85c-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="bc85c-141">NG – Pardavimo vertė</span><span class="sxs-lookup"><span data-stu-id="bc85c-141">WIP Sales value</span></span> | <span data-ttu-id="bc85c-142">Kreditas</span><span class="sxs-lookup"><span data-stu-id="bc85c-142">Credit</span></span> | <span data-ttu-id="bc85c-143">100</span><span class="sxs-lookup"><span data-stu-id="bc85c-143">100</span></span> |
  | <span data-ttu-id="bc85c-144">Sukauptos įplaukos – Pardavimo vertė</span><span class="sxs-lookup"><span data-stu-id="bc85c-144">Accrued revenue sales value</span></span> | <span data-ttu-id="bc85c-145">Debetas</span><span class="sxs-lookup"><span data-stu-id="bc85c-145">Debit</span></span> | <span data-ttu-id="bc85c-146">100</span><span class="sxs-lookup"><span data-stu-id="bc85c-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="bc85c-147">Operacijos, įtraukiamos naudojant fiksuotos kainos atsiskaitymo metodą</span><span class="sxs-lookup"><span data-stu-id="bc85c-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="bc85c-148">Išlaidų ir pajamų pripažinimas yra atskiri procesai.</span><span class="sxs-lookup"><span data-stu-id="bc85c-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="bc85c-149">Operacijos išlaidos užregistruojamos naudojant [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="bc85c-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="bc85c-150">Pardavimo, už kurį neišrašyta sąskaita, operacijos nesukuriamos.</span><span class="sxs-lookup"><span data-stu-id="bc85c-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="bc85c-151">Pajamas galima pripažinti išrašant SF, jei projekto išlaidų ir pajamų profilyje parinktis **Projekto atliko skaičiavimo principas** nustatyta kaip **NG nėra**.</span><span class="sxs-lookup"><span data-stu-id="bc85c-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="bc85c-152">Šį metodą taikykite tik trumpalaikiams, paprastiems projektams.</span><span class="sxs-lookup"><span data-stu-id="bc85c-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="bc85c-153">Pajamas galima pripažinti naudojant fiksuotos kainos pajamų įvertinimus, taikant pajamų pripažinimo metodą **Baigta sutartis** arba **Įvykdymo procentas**.</span><span class="sxs-lookup"><span data-stu-id="bc85c-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc85c-154">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="bc85c-154">Additional resources</span></span>
[<span data-ttu-id="bc85c-155">Apmokėtinų projektų apskaitos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="bc85c-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="bc85c-156">Fiksuotos kainos pajamų vertinimo projektai</span><span class="sxs-lookup"><span data-stu-id="bc85c-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="bc85c-157">Pajamų įvertinimų valdymas</span><span class="sxs-lookup"><span data-stu-id="bc85c-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="bc85c-158">Užbaigimo išlaidų apskaičiavimo metodai</span><span class="sxs-lookup"><span data-stu-id="bc85c-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]