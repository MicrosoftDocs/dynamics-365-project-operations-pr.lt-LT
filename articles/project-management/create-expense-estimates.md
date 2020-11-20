---
title: Išlaidų sąmatos
description: Šioje temoje pateikta informacija apie projektu pagrįstų išlaidų nustatymą arba vertinimą.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131713"
---
# <a name="expense-estimates"></a><span data-ttu-id="6a14e-103">Išlaidų sąmatos</span><span class="sxs-lookup"><span data-stu-id="6a14e-103">Expense estimates</span></span>
<span data-ttu-id="6a14e-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="6a14e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6a14e-105">Kartu su ištekliais pagrįstais įvertinimais, „Dynamics 365 Project Operations“ leidžia projektų vadovams apibrėžti kiekvieno projekto projektu pagrįstas išlaidas.</span><span class="sxs-lookup"><span data-stu-id="6a14e-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="6a14e-106">Kiekvienas išlaidų elementas gali būti susietas su konkrečia projekto užduotimi arba išlaidų kategorija.</span><span class="sxs-lookup"><span data-stu-id="6a14e-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="6a14e-107">Išlaidų kategorijos paprastai apibrėžiamos organizaciniu lygiu.</span><span class="sxs-lookup"><span data-stu-id="6a14e-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="6a14e-108">Kiekvienos išlaidų kategorijos kainodara paprastai apibrėžiama šioje hierarchijoje:</span><span class="sxs-lookup"><span data-stu-id="6a14e-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="6a14e-109">Organizacija</span><span class="sxs-lookup"><span data-stu-id="6a14e-109">Organization</span></span>
- <span data-ttu-id="6a14e-110">Klientas</span><span class="sxs-lookup"><span data-stu-id="6a14e-110">Customer</span></span>
- <span data-ttu-id="6a14e-111">Pasiūlymas / sutartis</span><span class="sxs-lookup"><span data-stu-id="6a14e-111">Quote/contract</span></span>

<span data-ttu-id="6a14e-112">Atlikite šiuos veiksmus norėdami peržiūrėti, įtraukti arba panaikinti projekto išlaidas.</span><span class="sxs-lookup"><span data-stu-id="6a14e-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="6a14e-113">Eikite į **Projektai** ir pažymėkite projektą, ties kuriuo norite dirbti.</span><span class="sxs-lookup"><span data-stu-id="6a14e-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="6a14e-114">Pažymėkite skirtuką **Projektų sąmatos** ir peržiūrėkite projekto išlaidų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="6a14e-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="6a14e-115">Pažymėkite **Naujos išlaidos** ir įtraukite išlaidas.</span><span class="sxs-lookup"><span data-stu-id="6a14e-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="6a14e-116">Arba pažymėkite išlaidas, kurias norite panaikinti, o tada pasirinkite **Naikinti išlaidas**.</span><span class="sxs-lookup"><span data-stu-id="6a14e-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="6a14e-117">Kiekvienam išlaidų eilutės elementui nustatomi šie atributai:</span><span class="sxs-lookup"><span data-stu-id="6a14e-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="6a14e-118">**Kategorija**: bendrosios grupės, naudojamos visoms išlaidoms, patirtoms projekto metu, aprašyti.</span><span class="sxs-lookup"><span data-stu-id="6a14e-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="6a14e-119">**Pradžios data**: data, kada išlaidas numatoma patirti.</span><span class="sxs-lookup"><span data-stu-id="6a14e-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="6a14e-120">**Kiekis**: numatomas tam tikros kategorijos išlaidų elementų skaičius.</span><span class="sxs-lookup"><span data-stu-id="6a14e-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="6a14e-121">**Vieneto savikaina**: vieneto kaina, naudojama išlaidų kainai apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="6a14e-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="6a14e-122">**Vieneto pardavimų kaina**: vieneto kaina, naudojama išlaidų pardavimų kainoms apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="6a14e-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

