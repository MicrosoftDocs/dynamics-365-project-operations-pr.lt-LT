---
title: Tvirtinimų apžvalga
description: Šioje temoje pateikta informacija, kaip dirbti su patvirtinimais programoje „Project Operations“.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961176"
---
# <a name="approvals-overview"></a><span data-ttu-id="a7f8a-103">Tvirtinimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="a7f8a-103">Approvals overview</span></span>

<span data-ttu-id="a7f8a-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="a7f8a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a7f8a-105">Laiko ir išlaidų pateikimai vyksta per patvirtinimo darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="a7f8a-106">Patvirtinus įrašus, operacijos įrašomos faktiniuose duomenyse arba laikas rezervuojamas grafike.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="a7f8a-107">Patvirtinimų darbo eiga</span><span class="sxs-lookup"><span data-stu-id="a7f8a-107">Approvals workflow</span></span>
<span data-ttu-id="a7f8a-108">Kai kuriate ir pateikiate laiko arba išlaidų įrašą, sukuriamas patvirtinimo įrašas.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="a7f8a-109">Projekto tvirtintojas arba jūsų vadovas peržiūri ir patvirtina įrašą.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="a7f8a-110">Jei įrašas yra susijęs su projektu, jį patvirtinus, bus sukurti faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="a7f8a-111">Tai leidžia sekti išlaidas ir sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="a7f8a-112">Įrašo patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="a7f8a-112">Approve an entry</span></span>
<span data-ttu-id="a7f8a-113">**Patvirtinimo** forma leidžia persijungti iš skirtingų rodinių, kad galėtumėte peržiūrėti skirtingų tipų patvirtinimus.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="a7f8a-114">Eikite į **Patvirtinimų** formą ir pasirinkite **Išlaidos**, **Laikas**arba **Atšaukimai**.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-114">Go to the **Approvals** form and select **Expenses**, **Time**, or **Recalls**.</span></span>
2. <span data-ttu-id="a7f8a-115">Peržiūrėkite kiekvieną patvirtinimą ir pažymėkite tuos, kuriuos norite patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="a7f8a-116">Pažymėkite **Patvirtinti**, kad patvirtintumėte pažymėtus įrašus.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="a7f8a-117">Sistema apdoros šiuos įrašus ir sukurs faktinius duomenis arba užsakymą.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="a7f8a-118">Įrašo atmetimas</span><span class="sxs-lookup"><span data-stu-id="a7f8a-118">Reject an entry</span></span>
<span data-ttu-id="a7f8a-119">Kaip projektų tvirtintojui, jums gali tekti nusiųsti įrašą atgal vartotojui pataisymui.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="a7f8a-120">Eikite į formą **Patvirtinimai** ir pasirinkite įrašą, kurį norite atmesti.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="a7f8a-121">Pasirinkite **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-121">Select **Reject**.</span></span>
3. <span data-ttu-id="a7f8a-122">Pasirinktinai – dialogo lange **Atmetimo komentarai** įtraukite komentarą, kad informuotumėte vartotoją, kodėl įrašas yra atmetamas.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="a7f8a-123">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-123">Select **OK**.</span></span> <span data-ttu-id="a7f8a-124">Įrašas bus grąžintas vartotojui.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="a7f8a-125">Įrašų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="a7f8a-125">Recall entries</span></span>
<span data-ttu-id="a7f8a-126">Tam tikru momentu gali prireikti atšaukti pateiktą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="a7f8a-127">Jei įrašas nebuvo patvirtintas, jis bus nedelsiant grąžintas.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="a7f8a-128">Tačiau patvirtintas įrašas gali turėti reikšmingą poveikį.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="a7f8a-129">Projektų tvirtintojas privalo patvirtinti atšaukimą tam, kad pakeisti operaciją faktiniuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="a7f8a-130">Projekto tvirtintojų nurodymas</span><span class="sxs-lookup"><span data-stu-id="a7f8a-130">Specify Project approvers</span></span>
<span data-ttu-id="a7f8a-131">Kiekvienas projektas turi keletą projekto komandos narių.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-131">Each project has a number of project team members.</span></span> <span data-ttu-id="a7f8a-132">Galite nurodyti, kurie komandos nariai taip pat yra projektų tvirtintojai.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="a7f8a-133">Eikite į formą **Projektai** ir atidarykite projektą iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="a7f8a-134">Skirtuke **Komanda** pasirinkite komandos narį, kuris bus projekto tvirtintojas ir pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="a7f8a-135">Nustatykite lauką **Projekto tvirtintojas** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="a7f8a-136">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-136">Select **Save**.</span></span>
5. <span data-ttu-id="a7f8a-137">Pakartokite 2–4 veiksmus, jei norite įtraukti papildomų projekto tvirtintojų.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="a7f8a-138">Vartotojo vadovo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="a7f8a-138">Configure the user's manager</span></span>

1. <span data-ttu-id="a7f8a-139">Pasirinkite **Parametrai** > **Sauga** > **Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="a7f8a-140">Pažymėkite vartotoją, kuriam priskiriate vadovą ir srityje **Organizacijos informacija** sąraše pasirinkite vadovą.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="a7f8a-141">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="a7f8a-141">Select **Save**.</span></span>


