---
title: Pasiūlymo uždarymas – „Lite“ versija
description: Šioje temoje pateikta informacija apie „Project Operations“ pasiūlymo uždarymą.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994146"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="548e8-103">Pasiūlymo uždarymas – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="548e8-103">Close a quote - lite</span></span>

<span data-ttu-id="548e8-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="548e8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="548e8-105">Projekto pasiūlymą galima uždaryti kaip laimėtą arba pralaimėtą.</span><span class="sxs-lookup"><span data-stu-id="548e8-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="548e8-106">Pasiūlymo juodraštį galima uždaryti, nes „Microsoft Dynamics 365 Project Operations“ pasiūlymuose nepalaiko aktyvavimo ir peržiūrėjimo operacijų.</span><span class="sxs-lookup"><span data-stu-id="548e8-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="548e8-107">Pasiūlymo uždarymas kaip laimėto</span><span class="sxs-lookup"><span data-stu-id="548e8-107">Close a quote as Won</span></span>

<span data-ttu-id="548e8-108">Kai uždarote projekto pasiūlymą kaip laimėtą, būsena nustatoma į uždarytą, o būsenos tipas yra laimėtas.</span><span class="sxs-lookup"><span data-stu-id="548e8-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="548e8-109">Uždarius pasiūlymą, projekto pasiūlymas pasidaro tik skaitomas ir sukuriamas projekto sutarties juodraštis, kuriame yra pasiūlymo informacija.</span><span class="sxs-lookup"><span data-stu-id="548e8-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="548e8-110">Kadangi uždaryto pasiūlymo negalima atidaryti iš naujo, patvirtinimo dialogas patvirtins jūsų pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="548e8-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="548e8-111">Jei pasiūlymas pridedamas prie galimybės, kiti projekto pasiūlymai dėl galimybės automatiškai uždaromi kaip pralaimėti.</span><span class="sxs-lookup"><span data-stu-id="548e8-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="548e8-112">Finansinis poveikis uždarius pasiūlymą kaip laimėtą</span><span class="sxs-lookup"><span data-stu-id="548e8-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="548e8-113">Jei prie pasiūlymo juodraščio projekto faktinių duomenų projekto metu yra faktinių duomenų, įrašoma tik laiko arba išlaidų kaina.</span><span class="sxs-lookup"><span data-stu-id="548e8-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="548e8-114">Kai pasiūlymas uždaromas kaip laimėtas, programa restruktūrizuos išlaidas atšaukdama senesnius išlaidų faktinius duomenis ir iš naujo sukurdama naujus išlaidų faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="548e8-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="548e8-115">Programa apdoros šiuos išlaidų faktinius duomenis pagal susietos projekto sutarties eilutės atsiskaitymo metodą.</span><span class="sxs-lookup"><span data-stu-id="548e8-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="548e8-116">Jei išlaidų faktiniai duomenys nurodo laiką ir medžiagos sutarties eilutę, uždarius pasiūlymą ir sukūrus projekto sutartį sukuriami atitinkami pardavimo, už kurį neišrašyta SF, faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="548e8-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="548e8-117">Jei išlaidų faktiniai duomenys nuoro fiksuotos kainos sutarties eilutę, programa sustabdys išlaidų faktinių duomenų, pagrįstų projekto sutarties klientų atsiskaitymo taisyklėmis, apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="548e8-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="548e8-118">Pasiūlymo uždarymas kaip pralaimėto:</span><span class="sxs-lookup"><span data-stu-id="548e8-118">Closing a quote as lost:</span></span>

<span data-ttu-id="548e8-119">Kai uždarote projekto pasiūlymą kaip pralaimėtą, būsena nustatoma į uždarytą, o būsenos tipas yra pralaimėtas.</span><span class="sxs-lookup"><span data-stu-id="548e8-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="548e8-120">Uždarius pasiūlymą projekto pasiūlymas yra tik skaitomas.</span><span class="sxs-lookup"><span data-stu-id="548e8-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="548e8-121">Kadangi uždaryto pasiūlymo atidaryti iš naujo negalima, prieš uždarant pasiūlymą pateikiamas patvirtinimo dialogo langas, kuriame reikės patvirtinti keitimus.</span><span class="sxs-lookup"><span data-stu-id="548e8-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="548e8-122">Jei projekto pasiūlymas, uždarytas kaip pralaimėtas, nurodo projektą bet kurioje iš jo eilučių, tas projektas taip pat pažymimas kaip uždarytas.</span><span class="sxs-lookup"><span data-stu-id="548e8-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="548e8-123">Nuo tos dienos atšaukiami visi išteklių rezervavimai.</span><span class="sxs-lookup"><span data-stu-id="548e8-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="548e8-124">„Project Operations“ uždarius pasiūlymą kaip laimėtą arba pralaimėtą galimybės būsena nebus paveikta – ji bus atidaryta tol, kol nebus uždaryta rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="548e8-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]