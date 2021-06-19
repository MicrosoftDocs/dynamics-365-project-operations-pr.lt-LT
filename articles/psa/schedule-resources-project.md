---
title: Projekto išteklių planavimas
description: Projekto išteklių planavimas „Project Service“
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: c67633960bb448d2190ec1bfde4e964f4fcb7969
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008501"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="a18fd-103">Projekto išteklių planavimas („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="a18fd-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a18fd-104">Galite patikrinti išteklių užimtumą, kad turėtumėte apie jį bendrą vaizdą, arba galite rodinį filtruoti pagal įgūdžius, komandą, vietą ir kitas parinktis.</span><span class="sxs-lookup"><span data-stu-id="a18fd-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="a18fd-105">Grafiko lentoje rodomas išteklių sąrašas ir jų pasiekiamumas.</span><span class="sxs-lookup"><span data-stu-id="a18fd-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="a18fd-106">Pasirinkite peržiūros režimą, kas būtų rodomas pasiekiamumas pagal **Valandas**, **Dieną**, **Savaitę** arba **Mėnesį**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="a18fd-107">Prieš pradedant naudotis grafiko lenta, svarbu ją nustatyti.</span><span class="sxs-lookup"><span data-stu-id="a18fd-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="a18fd-108">Daugiau informacijos žr. [Grafiko lentos konfigūravimas („Field Service” arba „Project Service Automation”)](/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="a18fd-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="a18fd-109">Jei jūs naudojate senesnę versiją, dėl išteklių pasiekiamumo, žr. [Išteklių pasiekiamumo peržiūra](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="a18fd-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="a18fd-110">Norint naudoti grafiko lentos rezervacijos funkcines galimybes, geokodavimo ir vietos nustatymo paslaugas, jums reikia įjungti žemėlapius.</span><span class="sxs-lookup"><span data-stu-id="a18fd-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="a18fd-111">Pagrindiniame meniu pasirinkite **Išteklių planavimas** > **Administravimas**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="a18fd-112">Spustelėkite **Planavimo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="a18fd-113">Atidarykite įrašą ir slinkite žemyn iki srities **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="a18fd-114">Lauke **Prisijungimas prie žemėlapių** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="a18fd-115">Sutikite su sąlygomis ir įrašykite įrašą.</span><span class="sxs-lookup"><span data-stu-id="a18fd-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="a18fd-116">Pagrindiniame meniu pasirinkite **Project Service** > **Grafiko lenta**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="a18fd-117">Tada suplanuoti rezervacijos reikalavimą neautomatiniu būdu galima keliais būdais.</span><span class="sxs-lookup"><span data-stu-id="a18fd-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="a18fd-118">Pasirinkite jums tinkantį būdą.</span><span class="sxs-lookup"><span data-stu-id="a18fd-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="a18fd-119">Pasiekiamų išteklių radimas</span><span class="sxs-lookup"><span data-stu-id="a18fd-119">Find available resources</span></span>

1.  <span data-ttu-id="a18fd-120">Sąraše **Rezervacijos reikalavimas** dešiniuoju pelės klavišu spustelėkite ant nesuplanuotos rezervacijos ir pasirinkite vieną iš tolesnių parinkčių.</span><span class="sxs-lookup"><span data-stu-id="a18fd-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="a18fd-121">Pasirinkite **Rasti pasiekiamus – dabartiniai ištekliai**, kad rastumėte pasiekiamų išteklių iš grafiko lentoje pateikto sąrašo.</span><span class="sxs-lookup"><span data-stu-id="a18fd-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="a18fd-122">Pasirinkite **Rasti pasiekiamus – visi ištekliai**, kad rastumėte pasiekiamų išteklių sistemos šaltiniuose</span><span class="sxs-lookup"><span data-stu-id="a18fd-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="a18fd-123">Tai atlikus, filtrai parodys pasirinkto rezervacijos reikalavimo parinktis.</span><span class="sxs-lookup"><span data-stu-id="a18fd-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="a18fd-124">Kai pamatysite laisvą atkarpą, dešiniuoju pelės klavišu spustelėkite ant laisvos atkarpos grafiko lentoje ir pasirinkite **Rezervuoti čia**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="a18fd-125">Arba nuvilkite rezervacijos reikalavimą į laisvą laiko tarpą.</span><span class="sxs-lookup"><span data-stu-id="a18fd-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="a18fd-126">Rezervuokite išteklių dienos rodinyje ir raskite, kas nėra rezervuotas</span><span class="sxs-lookup"><span data-stu-id="a18fd-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="a18fd-127">Grafiko lentoje pasirinkite **Peržiūros režimas** ir pasirinkite **Dienos**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="a18fd-128">Rodomas tinklelio rodinys, kiek ištekliaus valandų yra rezervuota per dieną ir kokiomis dienomis jie laisvi.</span><span class="sxs-lookup"><span data-stu-id="a18fd-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="a18fd-129">Spustelėkite ištekliaus, kurį norite rezervuoti, vardą, tada pasirinkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="a18fd-130">Dialogo lange **Išteklių rezervavimas (sukurti)** pasirinkite projektą, kuriam norite rezervuoti išteklių, taip pat rezervavimo būdą, pradžios ir pabaigos laiką.</span><span class="sxs-lookup"><span data-stu-id="a18fd-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="a18fd-131">Baigę pasirinkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="a18fd-132">Grafiko lentos peržiūra</span><span class="sxs-lookup"><span data-stu-id="a18fd-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="a18fd-133">Pasirinkite nesuplanuotą rezervacijos reikalavimą iš sąrašo apačioje.</span><span class="sxs-lookup"><span data-stu-id="a18fd-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="a18fd-134">Nuvilkite rezervacijos reikalavimą į laisvų išteklių / laiko atkarpą grafiko lentoje.</span><span class="sxs-lookup"><span data-stu-id="a18fd-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="a18fd-135">Baigę pasirinkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="a18fd-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="a18fd-136">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a18fd-136">Additional resources</span></span>  
 [<span data-ttu-id="a18fd-137">Išteklių vadovo vadovas</span><span class="sxs-lookup"><span data-stu-id="a18fd-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]