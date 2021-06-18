---
title: Komandos narių išlaikymas
description: Šioje temoje pateikiama informacija apie įvardytų išteklių rezervavimą projektų komandoms ir jų priskyrimą užduotims.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 00312c5a701768e0042e7e0236477c192690ded3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998646"
---
# <a name="maintain-team-members"></a><span data-ttu-id="81de9-103">Komandos narių išlaikymas</span><span class="sxs-lookup"><span data-stu-id="81de9-103">Maintain team members</span></span>

<span data-ttu-id="81de9-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="81de9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="81de9-105">Galite įtraukti įvardytąjį išteklių į savo projekto komandą rezervuodami juos tiesiogiai komandoje.</span><span class="sxs-lookup"><span data-stu-id="81de9-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="81de9-106">Programoje „Dynamics 365 Project Operations“ eikite į **Projektai** ir pasirinkite atidaryti projektą, kuriam rezervuojate.</span><span class="sxs-lookup"><span data-stu-id="81de9-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="81de9-107">Puslapyje **Projektas**, esančiame skirtuke **Komanda**, pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="81de9-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="81de9-108">Dialogo lange **Spartusis projekto komandos nario kūrimas** pasirinkite rezervuojamą išteklių.</span><span class="sxs-lookup"><span data-stu-id="81de9-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="81de9-109">Jei ištekliui yra priskirtas numatytasis ištekliaus vaidmuo, jis bus automatiškai įvestas į lauką **Vaidmuo**.</span><span class="sxs-lookup"><span data-stu-id="81de9-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="81de9-110">Galite keisti vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="81de9-110">You can change the role.</span></span> 
4. <span data-ttu-id="81de9-111">Pasirinkite pradžios ir pabaigos datas, kada išteklius bus reikalingas, o tada pasirinkite ištekliaus pajėgumo paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="81de9-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="81de9-112">Lauke **Projekto tvirtintojas** pasirinkite **Taip**, jei norite, kad komandos narys būtų projekto tvirtintoju.</span><span class="sxs-lookup"><span data-stu-id="81de9-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="81de9-113">Komandos narys galės tvirtinti pateiktus šio projekto laiko ir išlaidų įrašus.</span><span class="sxs-lookup"><span data-stu-id="81de9-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="81de9-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="81de9-114">Select **Save**.</span></span>

<span data-ttu-id="81de9-115">Dabar galite rezervuotą išteklių priskirti projekto užduotims.</span><span class="sxs-lookup"><span data-stu-id="81de9-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="81de9-116">Puslapyje **Projektas**, esančiame skirtuke **Grafikas**, priskirkite užduotis naujam ištekliui.</span><span class="sxs-lookup"><span data-stu-id="81de9-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="81de9-117">Išteklių parinkiklis, paleidžiamas naudojant užduočių tinklelio lauką **Ištekliai**, parodys komandos narius, kuriuos galite pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="81de9-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="81de9-118">Programoje „Project Operations“, išteklių rezervavimai ir užduočių priskyrimai nėra stipriai susieti.</span><span class="sxs-lookup"><span data-stu-id="81de9-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="81de9-119">Kai naudojate grafike esantį išteklių parinkiklį, galite priskirti komandos nariams daugiau užduočių valandų, nei apima jų projekto rezervavimai.</span><span class="sxs-lookup"><span data-stu-id="81de9-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="81de9-120">Skirtumai tarp komandos nario rezervavimų ir priskyrimų rodomi skirtukuose **Komanda** ir **Išteklių derinimas**.</span><span class="sxs-lookup"><span data-stu-id="81de9-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="81de9-121">Taip pat galite suderinti skirtumus tarp rezervavimų ir išteklių priskyrimų išsamesniu lygiu.</span><span class="sxs-lookup"><span data-stu-id="81de9-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="81de9-122">Naudokite išteklių parinkiklį, esantį skirtuke **Grafikas**, kad ieškotumėte ir pasirinktumėte rezervuojamus išteklius, kurie dar nėra projekto komandos dalimi.</span><span class="sxs-lookup"><span data-stu-id="81de9-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="81de9-123">Šie ištekliai išteklių parinkiklyje rodomi kaip **Kiti ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="81de9-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="81de9-124">Kai renkates, išteklius įtraukiamas į projekto komandą ir priskiriamas užduočiai, tačiau rezervavimas negeneruojamas.</span><span class="sxs-lookup"><span data-stu-id="81de9-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="81de9-125">Norėdami rezervuoti ištekliaus pajėgumą projektui galite naudoti skirtuko **Derinimas** rezervavimo išplėtimo pajėgumą arba **Grafiko lentą**.</span><span class="sxs-lookup"><span data-stu-id="81de9-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="81de9-126">Užrezervavę komandos narį projektui, galite naudotis parinktimis **Išlaikyti rezervavimus** arba **Grafiko lenta**, kad tiesiogiai valdytumėte jų rezervavimus.</span><span class="sxs-lookup"><span data-stu-id="81de9-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]