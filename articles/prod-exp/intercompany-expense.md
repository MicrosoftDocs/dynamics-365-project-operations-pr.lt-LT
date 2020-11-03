---
title: Vidinės įmonės išlaidos
description: Darbuotojas, įdarbintas vieno organizacijos juridinio subjekto, gali atlikti darbą, skirtą kitam tos pačios organizacijos juridiniam subjektui. Esant tokiai situacijai, galite naudoti vidinės įmonės išlaidų funkciją, kad priskirtumėte darbuotojo išlaidas juridiniam subjektui, kuriam buvo skirtas atliktas darbas.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080987"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="50f61-104">Vidinės įmonės išlaidos</span><span class="sxs-lookup"><span data-stu-id="50f61-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50f61-105">Darbuotojas, įdarbintas vieno organizacijos juridinio subjekto, gali atlikti darbą, skirtą kitam tos pačios organizacijos juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="50f61-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="50f61-106">Esant tokiai situacijai, galite naudoti vidinės įmonės išlaidų funkciją, kad priskirtumėte darbuotojo išlaidas juridiniam subjektui, kuriam buvo skirtas atliktas darbas.</span><span class="sxs-lookup"><span data-stu-id="50f61-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="50f61-107">Juridinis subjektas, įdarbinantis darbuotoją, vadinamas skolinančiu juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="50f61-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="50f61-108">Juridinis subjektas, kuris už darbuotojo atliktą darbą patiria išlaidų, vadinamas pasiskolinančiu juridiniu subjektu.</span><span class="sxs-lookup"><span data-stu-id="50f61-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="50f61-109">Kad darbuotojas galėtų kurti ir pateikti kitame juridiniame subjekte atlikto darbo išlaidas, skolinančio juridinio subjekto puslapyje **Išlaidų valdymo parametrai** pasirinkite parinktį **Leisti vidinės įmonės išlaidų eilutes**.</span><span class="sxs-lookup"><span data-stu-id="50f61-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="50f61-110">Vidinės įmonės išlaidų mokesčių registravimas</span><span class="sxs-lookup"><span data-stu-id="50f61-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50f61-111">Jei savo išlaidų ataskaitoje norite naudoti mokesčių grupes, susietas su skolinančiu (šaltinio) juridiniu subjektu, o ne pasiskolinančiu (paskirties) juridiniu subjektu, turėsite tai sukonfigūruoti DK PVM rinkinyje.</span><span class="sxs-lookup"><span data-stu-id="50f61-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="50f61-112">Kai DK parametras **Vidinės įmonės mokesčių registravimo juridinis subjektas** nustatomas į parinktį **Šaltinis** , o parametras **Taikyti PVM apmokestinimo taisykles** nustatytas į parinktį **Ne** , bus naudojamas skolinančio juridinio subjekto mokesčių derinys.</span><span class="sxs-lookup"><span data-stu-id="50f61-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="50f61-113">Kai tas pats parametras nustatytas į parinktį **Paskirtis** , bus naudojamas pasiskolinančio juridinio subjekto mokesčių derinys.</span><span class="sxs-lookup"><span data-stu-id="50f61-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="50f61-114">Jei juridiniai subjektai Jungtinėse Valstijose, kai parametras nustatytas į parinktį **Šaltinis** , laukas **Gaunamas PVM** turi būti sukonfigūruotas laukas naujame puslapyje **DK registravimo grupės**.</span><span class="sxs-lookup"><span data-stu-id="50f61-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="50f61-115">Apskaitos sistema naudos šiame lauke esančią informaciją rašydama su mokesčiais susijusį apskaitos įrašą.</span><span class="sxs-lookup"><span data-stu-id="50f61-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="50f61-116">Veikimas atitinka išlaidų eilutes, užregistruotas su projektu ar be jo.</span><span class="sxs-lookup"><span data-stu-id="50f61-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
