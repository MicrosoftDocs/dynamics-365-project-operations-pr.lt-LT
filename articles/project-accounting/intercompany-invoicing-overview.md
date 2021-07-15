---
title: Vidinės įmonės sąskaitų faktūrų išrašymo apžvalga
description: Šioje temoje pateikiama informacijos ir pavyzdžių apie vidinės įmonės SF išrašymą už projektus.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c1dcf642f79ce64cb83285ac6dc6d7eaf815145c
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369386"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="9d06f-103">Vidinės įmonės sąskaitų faktūrų išrašymo apžvalga</span><span class="sxs-lookup"><span data-stu-id="9d06f-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="9d06f-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="9d06f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9d06f-105">Jūsų organizaciją gali sudaryti keli skyriai, filialai ir kiti juridiniai subjektai, kurie, vykdydami projektus, keičiasi produktais ir paslaugomis.</span><span class="sxs-lookup"><span data-stu-id="9d06f-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="9d06f-106">Juridinis subjektas, kuris teikia paslaugą arba produktą, vadinamas *skolinančiu juridiniu subjektu*.</span><span class="sxs-lookup"><span data-stu-id="9d06f-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="9d06f-107">Juridinis subjektas, kuris gauna paslaugą arba produktą, vadinamas *besiskolinančiu juridiniu subjektu*.</span><span class="sxs-lookup"><span data-stu-id="9d06f-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="9d06f-108">Šioje iliustracijoje pavaizduotas įprastas scenarijus, kai du juridiniai objektai Contoso Robotics USA (besiskolinantis juridinis subjektas) ir Contoso Robotics UK (skolinantis juridinis subjektas) bendrina išteklius, kad klientui „Adventure works“ būtų galima vykdyti projektą.</span><span class="sxs-lookup"><span data-stu-id="9d06f-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="9d06f-109">Pagal šį scenarijų Contoso Robotics USA sudarė sutartį teikti darbus „Adventure Works“.</span><span class="sxs-lookup"><span data-stu-id="9d06f-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Vidinės įmonės sąskaitų faktūrų išrašymas](./media/IntercompanyScenario.png) 

<span data-ttu-id="9d06f-111">„Dynamics 365 Project Operations“ naudoja toliau pateiktą srautą, kad apdorotų vidinės įmonės operacijas.</span><span class="sxs-lookup"><span data-stu-id="9d06f-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="9d06f-112">Skolinančio juridinio subjekto ištekliai įrašo vidinės įmonės laiko arba išlaidų operacijas rezervuodami laiką ir išlaidas besiskolinančio juridinio subjekto projektams.</span><span class="sxs-lookup"><span data-stu-id="9d06f-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="9d06f-113">Laiko ir išlaidų kaštai įrašomi skolinančioje įmonėje naudojant besiskolinančios įmonės vieneto savikainos kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="9d06f-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="9d06f-114">Vidinės įmonės pardavimo, už kurį neišrašyta sąskaita, operacijos įrašomos skolinančioje įmonėje naudojant besiskolinančios įmonės vieneto savikainos kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="9d06f-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="9d06f-115">Pajamos, už kurias neišrašyta sąskaita, įrašomos besiskolinančioje įmonėje naudojant projekto sutarties pardavimo kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="9d06f-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="9d06f-116">Klientui galima išrašyti sąskaitą, kai įrašomos pajamos, už kurias neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="9d06f-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="9d06f-117">Klientas neturi laukti, kol bus baigtas vidinės įmonės sąskaitos faktūros apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="9d06f-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="9d06f-118">Vidinės įmonės kliento sąskaitos faktūros sukuriamos periodiškai skolinančioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="9d06f-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="9d06f-119">Sąskaitos faktūros sukuriamos rankiniu būdu arba naudojant periodinį automatinį procesą.</span><span class="sxs-lookup"><span data-stu-id="9d06f-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="9d06f-120">Galima kurti vieną sąskaitą faktūrą kiekvienam besiskolinančiam juridiniam subjektui arba atskiras sąskaitas faktūras pagal projektą.</span><span class="sxs-lookup"><span data-stu-id="9d06f-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="9d06f-121">Kai vidinės įmonės kliento sąskaita faktūra užregistruojama skolinančiame juridiniame subjekte, atitinkama laukianti tiekėjo sąskaita faktūra sukuriama besiskolinančiame juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="9d06f-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="9d06f-122">Laukiančioje tiekėjo sąskaitoje faktūroje esančios išlaidos bus įrašytos į projekto papildomą knygą, kai bus užregistruota sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="9d06f-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="9d06f-123">Toliau pateiktoje diagramoje vaizduojamas vidinės įmonės sąskaitų faktūrų išrašymas, kaip jis susijęs su apskaitos įvykiais ir numatomais registravimais didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="9d06f-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Vidinės įmonės srautas](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="9d06f-125">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="9d06f-125">Additional resources</span></span>

- [<span data-ttu-id="9d06f-126">Vidinės įmonės SF išrašymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9d06f-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="9d06f-127">Vidinės įmonės operacijų įrašymas</span><span class="sxs-lookup"><span data-stu-id="9d06f-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="9d06f-128">Vidinės įmonės kliento ir tiekėjo sąskaitų faktūrų kūrimas</span><span class="sxs-lookup"><span data-stu-id="9d06f-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]