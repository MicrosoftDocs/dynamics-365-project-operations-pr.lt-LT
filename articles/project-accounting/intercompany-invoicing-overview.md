---
title: Vidinės įmonės sąskaitų faktūrų išrašymo apžvalga
description: Šioje temoje pateikiama informacijos ir pavyzdžių apie vidinės įmonės SF išrašymą už projektus.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287338"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="b494e-103">Vidinės įmonės sąskaitų faktūrų išrašymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="b494e-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="b494e-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="b494e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b494e-105">Jūsų organizaciją gali sudaryti keli skyriai, filialai ir kiti juridiniai subjektai, kurie, vykdydami projektus, keičiasi produktais ir paslaugomis.</span><span class="sxs-lookup"><span data-stu-id="b494e-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="b494e-106">Juridinis subjektas, kuris teikia paslaugą arba produktą, vadinamas *skolinančiu juridiniu subjektu*.</span><span class="sxs-lookup"><span data-stu-id="b494e-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="b494e-107">Juridinis subjektas, kuris gauna paslaugą arba produktą, vadinamas *besiskolinančiu juridiniu subjektu*.</span><span class="sxs-lookup"><span data-stu-id="b494e-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="b494e-108">Toliau pateikiamas tipiško scenarijaus pavyzdys: du juridiniai subjektai „Contoso Robotics USA“ (besiskolinantis juridinis subjektas) ir „Contoso Robotics UK“ (skolinantis juridinis subjektas) dalijasi ištekliais, kad pateiktų projektą klientui „Adventure Works“.</span><span class="sxs-lookup"><span data-stu-id="b494e-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="b494e-109">Šiuo atveju su „Contoso Robotics USA“ sudaryta sutartis, pagal kurią ji turi pateikti darbą įmonei „Adventure Works“.</span><span class="sxs-lookup"><span data-stu-id="b494e-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Vidinės įmonės sąskaitų faktūrų išrašymas](./media/IntercompanyScenario.png) 

<span data-ttu-id="b494e-111">„Dynamics 365 Project Operations“ naudoja toliau pateiktą srautą, kad apdorotų vidinės įmonės operacijas.</span><span class="sxs-lookup"><span data-stu-id="b494e-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="b494e-112">Skolinančio juridinio subjekto ištekliai įrašo vidinės įmonės laiko arba išlaidų operacijas rezervuodami laiką ir išlaidas besiskolinančio juridinio subjekto projektams.</span><span class="sxs-lookup"><span data-stu-id="b494e-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="b494e-113">Laiko ir išlaidų kaštai įrašomi skolinančioje įmonėje naudojant besiskolinančios įmonės vieneto savikainos kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="b494e-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="b494e-114">Vidinės įmonės pardavimo, už kurį neišrašyta sąskaita, operacijos įrašomos skolinančioje įmonėje naudojant besiskolinančios įmonės vieneto savikainos kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="b494e-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="b494e-115">Pajamos, už kurias neišrašyta sąskaita, įrašomos besiskolinančioje įmonėje naudojant projekto sutarties pardavimo kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="b494e-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="b494e-116">Klientui galima išrašyti sąskaitą, kai įrašomos pajamos, už kurias neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="b494e-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="b494e-117">Klientas neturi laukti, kol bus baigtas vidinės įmonės sąskaitos faktūros apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="b494e-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="b494e-118">Vidinės įmonės kliento sąskaitos faktūros sukuriamos periodiškai skolinančioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="b494e-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="b494e-119">Sąskaitos faktūros sukuriamos rankiniu būdu arba naudojant periodinį automatinį procesą.</span><span class="sxs-lookup"><span data-stu-id="b494e-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="b494e-120">Galima kurti vieną sąskaitą faktūrą kiekvienam besiskolinančiam juridiniam subjektui arba atskiras sąskaitas faktūras pagal projektą.</span><span class="sxs-lookup"><span data-stu-id="b494e-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="b494e-121">Kai vidinės įmonės kliento sąskaita faktūra užregistruojama skolinančiame juridiniame subjekte, atitinkama laukianti tiekėjo sąskaita faktūra sukuriama besiskolinančiame juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="b494e-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="b494e-122">Laukiančioje tiekėjo sąskaitoje faktūroje esančios išlaidos bus įrašytos į projekto papildomą knygą, kai bus užregistruota sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="b494e-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="b494e-123">Toliau pateiktoje diagramoje vaizduojamas vidinės įmonės sąskaitų faktūrų išrašymas, kaip jis susijęs su apskaitos įvykiais ir numatomais registravimais didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="b494e-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Vidinės įmonės srautas](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="b494e-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="b494e-125">Additional resources</span></span>

- [<span data-ttu-id="b494e-126">Vidinės įmonės SF išrašymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b494e-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="b494e-127">Vidinės įmonės operacijų įrašymas</span><span class="sxs-lookup"><span data-stu-id="b494e-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="b494e-128">Vidinės įmonės kliento ir tiekėjo sąskaitų faktūrų kūrimas</span><span class="sxs-lookup"><span data-stu-id="b494e-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]