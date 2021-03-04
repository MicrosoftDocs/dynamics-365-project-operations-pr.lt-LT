---
title: Įmonės vidaus išlaidos
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti vidinės įmonės išlaidas darbuotojo išlaidoms priskirti juridiniam subjektui, kuriam buvo atliktas darbas.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960842"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="12f80-103">Vidinės įmonės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12f80-103">Intercompany expenses</span></span>

<span data-ttu-id="12f80-104">Darbuotojas, įdarbintas vieno organizacijos juridinio subjekto, gali atlikti darbą, skirtą kitam tos pačios organizacijos juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="12f80-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="12f80-105">Galite naudoti vidinės įmonės išlaidas darbuotojo išlaidoms priskirti juridiniam subjektui, kuriam buvo atliktas darbas.</span><span class="sxs-lookup"><span data-stu-id="12f80-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="12f80-106">Juridinis subjektas, įdarbinantis darbuotoją, vadinamas skolinančiu juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="12f80-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="12f80-107">Juridinis subjektas, kuris už darbuotojo atliktą darbą patiria išlaidų, vadinamas pasiskolinančiu juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="12f80-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="12f80-108">Kad darbuotojas galėtų kurti ir pateikti vidinės įmonės išlaidas, turite įjungti vidinės įmonės išlaidų eilutes.</span><span class="sxs-lookup"><span data-stu-id="12f80-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="12f80-109">Skolinančiajame juridiniame subjekte, puslapyje **Išlaidų valdymo parametrai**, pasirinkite **Leisti vidinės įmonės išlaidų eilutes**.</span><span class="sxs-lookup"><span data-stu-id="12f80-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="12f80-110">Vidinės įmonės išlaidų mokesčių registravimas</span><span class="sxs-lookup"><span data-stu-id="12f80-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12f80-111">Kad savo išlaidų ataskaitoje galėtumėte naudoti mokesčių grupes, susietas su skolinančiuoju (šaltinio) juridiniu subjektu, o ne su besiskolinančiu (paskirties) juridiniu subjektu, turite įjungti šią funkciją didžiosios knygos PVM sąrankoje.</span><span class="sxs-lookup"><span data-stu-id="12f80-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="12f80-112">Kai parametras **Juridinis subjektas mokesčių registracijai tarp įmonių** nustatytas į **Šaltinio**, o **Taikyti PVM apmokestinimo taisykles** nustatytas į **Ne**, naudojamas skolinančiojo juridinio subjekto mokesčių derinys.</span><span class="sxs-lookup"><span data-stu-id="12f80-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="12f80-113">Kai tas pats parametras nustatytas į parinktį **Paskirtis**, bus naudojamas pasiskolinančio juridinio subjekto mokesčių derinys.</span><span class="sxs-lookup"><span data-stu-id="12f80-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="12f80-114">Jei juridiniai subjektai Jungtinėse Valstijose, kai parametras nustatytas į parinktį **Šaltinis**, laukas **Gaunamas PVM** turi būti sukonfigūruotas laukas naujame puslapyje **DK registravimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="12f80-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="12f80-115">Apskaitos modulis naudos šiame lauke esančią informaciją su mokesčiais susijusiam apskaitos įrašui.</span><span class="sxs-lookup"><span data-stu-id="12f80-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="12f80-116">Veikimas atitinka išlaidų eilutes, užregistruotas su projektu ar be jo.</span><span class="sxs-lookup"><span data-stu-id="12f80-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
