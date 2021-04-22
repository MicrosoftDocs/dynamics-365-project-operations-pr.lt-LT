---
title: Įvardytų rezervuojamų išteklių rezervavimas projekto komandai ir užduočių priskyrimas
description: Šioje temoje pateikiama informacija apie įvardytų išteklių rezervavimą projektų komandoms ir jų priskyrimą užduotims.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6169f2bdc107e63d666fb32d34f531fd5d472c2f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291449"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="507b3-103">Įvardytų rezervuojamų išteklių rezervavimas projekto komandai ir užduočių priskyrimas</span><span class="sxs-lookup"><span data-stu-id="507b3-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="507b3-104">Galite įtraukti įvardytąjį išteklių į savo projekto komandą rezervuodami juos tiesiogiai komandoje.</span><span class="sxs-lookup"><span data-stu-id="507b3-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="507b3-105">Kad tai padarytumėte atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="507b3-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="507b3-106">Programoje „Project Service Automation“ eikite į sritį **Projektai** ir pasirinkite atidaryti projektą, kuriam rezervuojate.</span><span class="sxs-lookup"><span data-stu-id="507b3-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="507b3-107">Puslapio **Projektas** skirtuke **Komanda** spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="507b3-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Komandos nario įtraukimas naudojant komandos skirtuką](media/RM-how-to-1.png)

3. <span data-ttu-id="507b3-109">Dialogo lange **Spartusis projekto komandos nario kūrimas** pasirinkite rezervuojamą išteklių.</span><span class="sxs-lookup"><span data-stu-id="507b3-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="507b3-110">Jei ištekliui yra priskirtas numatytasis ištekliaus vaidmuo, jis bus automatiškai įvestas į lauką **Vaidmuo**.</span><span class="sxs-lookup"><span data-stu-id="507b3-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="507b3-111">Jei reikia, vaidmenį galite keisti.</span><span class="sxs-lookup"><span data-stu-id="507b3-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="507b3-112">Pasirinkite pradžios ir pabaigos datas, kada išteklius bus reikalingas, ir pasirinkite ištekliaus pajėgumo paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="507b3-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="507b3-113">Jei norite, kad komandos narys būtų projekto tvirtintojas, lauke **Projekto tvirtintojas** pasirinkite reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="507b3-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="507b3-114">Tai reikš, kad komandos narys galės tvirtinti pateiktus šio projekto laiko ir išlaidų įrašus.</span><span class="sxs-lookup"><span data-stu-id="507b3-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="507b3-115">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="507b3-115">Click **Save**.</span></span>

![Komandos nario įtraukimas į sparčiojo kūrimo formą](media/RM-how-to-2.png)


<span data-ttu-id="507b3-117">Dabar galite rezervuotą išteklių priskirti projekto užduotims.</span><span class="sxs-lookup"><span data-stu-id="507b3-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="507b3-118">Puslapyje **Projektas** spustelėkite skirtuką **Grafikas** ir priskirkite užduotis naujam ištekliui.</span><span class="sxs-lookup"><span data-stu-id="507b3-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="507b3-119">Išteklių parinkiklis, paleidžiamas naudojant užduočių tinklelio lauką **Ištekliai**, parodys komandos narius, kuriuos galite pasirinkti.</span><span class="sxs-lookup"><span data-stu-id="507b3-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Komandos nario priskyrimas užduočiai naudojant skirtuką Grafikas](media/RM-how-to-3.png)

<span data-ttu-id="507b3-121">Programos „Project Service Automation“ (PSA) 3 versijoje išteklių rezervavimas ir užduočių priskyrimai nėra tvirtai susieti.</span><span class="sxs-lookup"><span data-stu-id="507b3-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="507b3-122">Tai reiškia, kad naudodamiesi grafike esančiu išteklių parinkikliu komandos nariams galite priskirti daugiau užduočių valandų, nei jiems yra priskirta rezervuotų projekto valandų.</span><span class="sxs-lookup"><span data-stu-id="507b3-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="507b3-123">Skirtuke **Komanda** arba **Išteklių suderinimas** galite matyti skirtumus tarp komandos narių rezervavimų ir priskyrimų. Be to, išteklių rezervavimų ir priskyrimų skirtumus galite suderinti išsamesniu lygiu.</span><span class="sxs-lookup"><span data-stu-id="507b3-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Išteklių suderinimo skirtukas](media/RM-how-to-4.png)

<span data-ttu-id="507b3-125">Norėdami ieškoti rezervuojamų išteklių, kurie dar nėra įtraukti į jūsų projekto komandą, ir juos pasirinkti taip pat galite skirtuke **Grafikas** esantį išteklių parinkiklį.</span><span class="sxs-lookup"><span data-stu-id="507b3-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="507b3-126">Išteklių parinkiklyje jie yra rodomi kaip **Kiti ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="507b3-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Ne komandos nario ištekliaus priskyrimas užduočiai](media/RM-how-to-5.png)

<span data-ttu-id="507b3-128">Kai naudojate šį veiksmą, išteklius įtraukiamas į projekto komandą ir priskiriamas užduočiai, tačiau rezervavimas negeneruojamas.</span><span class="sxs-lookup"><span data-stu-id="507b3-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Priskyrimai komandos nariams nerezervuojant](media/RM-how-to-6.png)

<span data-ttu-id="507b3-130">Norėdami rezervuoti ištekliaus pajėgumą projektui galite naudoti skirtuko **Derinimas** rezervavimo išplėtimo pajėgumą arba **Grafiko lentą**.</span><span class="sxs-lookup"><span data-stu-id="507b3-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Komandos nario rezervavimų išplėtimas skirtuke Išteklių derinimas](media/RM-how-to-7.png)

<span data-ttu-id="507b3-132">Rezervavę komandos narį savo projektui, jo rezervavimus galite tvarkyti naudodami funkciją Prižiūrėti rezervavimus arba tiesiogiai naudodamiesi Grafiko lenta.</span><span class="sxs-lookup"><span data-stu-id="507b3-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]