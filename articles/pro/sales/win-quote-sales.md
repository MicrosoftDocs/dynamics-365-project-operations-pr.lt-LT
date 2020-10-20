---
title: Pasiūlymų uždarymas
description: Šioje temoje pateikta informacija apie „Project Operations“ pasiūlymo uždarymą.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896201"
---
# <a name="close-quotes"></a><span data-ttu-id="e2a26-103">Pasiūlymų uždarymas</span><span class="sxs-lookup"><span data-stu-id="e2a26-103">Close quotes</span></span> 

<span data-ttu-id="e2a26-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="e2a26-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e2a26-105">Projekto pasiūlymą galima uždaryti kaip laimėtą arba pralaimėtą.</span><span class="sxs-lookup"><span data-stu-id="e2a26-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="e2a26-106">Pasiūlymų aktyvinimo ir peržiūros operacijos nepalaikomos „Microsoft Dynamics 365 Project Operations“, todėl juodraštinį pasiūlymą galima uždaryti.</span><span class="sxs-lookup"><span data-stu-id="e2a26-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="e2a26-107">Pasiūlymo uždarymas kaip laimėto</span><span class="sxs-lookup"><span data-stu-id="e2a26-107">Close a quote as Won</span></span>

<span data-ttu-id="e2a26-108">Uždarant projekto pasiūlymą kaip laimėtą, uždaromas pasiūlymas, kurio būsena yra Uždarytas, o būsenos tipas nustatytas kaip Laimėtas.</span><span class="sxs-lookup"><span data-stu-id="e2a26-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="e2a26-109">Uždarius pasiūlymą, projekto pasiūlymas pasidaro tik skaitomas ir sukuriamas projekto sutarties juodraštis, kuriame yra pasiūlymo informacija.</span><span class="sxs-lookup"><span data-stu-id="e2a26-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="e2a26-110">Kadangi uždaryto pasiūlymo atidaryti iš naujo negalima, prieš atliekant pakeitimus pateikiamas patvirtinimo dialogo langas, nes uždaryto pasiūlymo atidaryti iš naujo negalima ir pakeitimų atšaukti neįmanoma.</span><span class="sxs-lookup"><span data-stu-id="e2a26-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="e2a26-111">Jei pasiūlymas pridedamas prie galimybės, kiti projekto pasiūlymai dėl galimybės automatiškai uždaromi kaip pralaimėti.</span><span class="sxs-lookup"><span data-stu-id="e2a26-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="e2a26-112">Finansinis poveikis uždarius pasiūlymą kaip laimėtą</span><span class="sxs-lookup"><span data-stu-id="e2a26-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="e2a26-113">Jei yra įrašytų projekto laiko faktinių duomenų, kol jis dar pridėtas prie juodraštinio pasiūlymo, įrašomos tik laiko sąnaudos arba išlaidos.</span><span class="sxs-lookup"><span data-stu-id="e2a26-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="e2a26-114">Kai pasiūlymas uždaromas kaip laimėtas, programa restruktūrizuos išlaidas atšaukdama senesnius išlaidų faktinius duomenis ir iš naujo sukurdama naujus išlaidų faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="e2a26-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="e2a26-115">Programa apdoros šiuos išlaidų faktinius duomenis pagal susietos projekto sutarties eilutės atsiskaitymo metodą.</span><span class="sxs-lookup"><span data-stu-id="e2a26-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="e2a26-116">Jei išlaidų faktiniai duomenys nurodo laiko ir medžiagų sutarties eilutę, sistema automatiškai sukurs atitinkamus pardavimo faktinius duomenis, kuriems neišrašyta sąskaita faktūra, kai pasiūlymas uždaromas ir sukuriama projekto sutartis.</span><span class="sxs-lookup"><span data-stu-id="e2a26-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="e2a26-117">Jei išlaidų faktiniai duomenys nurodo fiksuotos kainos sutarties eilutę, programa sustabdys išlaidų faktinių duomenų apdorojimą pagal išskaidyto atsiskaitymo taisykles, taikomas projekto sutarties klientams.</span><span class="sxs-lookup"><span data-stu-id="e2a26-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="e2a26-118">Pasiūlymo uždarymas kaip pralaimėto:</span><span class="sxs-lookup"><span data-stu-id="e2a26-118">Closing a quote as lost:</span></span>

<span data-ttu-id="e2a26-119">Uždarant projekto pasiūlymą kaip pralaimėtą, bus nustatyta būsena Uždarytas ir nustatytas būsenos tipas Pralaimėtas.</span><span class="sxs-lookup"><span data-stu-id="e2a26-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="e2a26-120">Uždarius pasiūlymą projekto pasiūlymas yra tik skaitomas.</span><span class="sxs-lookup"><span data-stu-id="e2a26-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="e2a26-121">Kadangi uždaryto pasiūlymo atidaryti iš naujo negalima, prieš uždarant pasiūlymą pateikiamas patvirtinimo dialogo langas, kuriame reikės patvirtinti keitimus.</span><span class="sxs-lookup"><span data-stu-id="e2a26-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="e2a26-122">Jei projekto pasiūlymo, kuris uždarytas kaip pralaimėtas, bet kuri eilutė nurodo projektą, tas projektas taip pat pažymimas kaip uždarytas, o bet kokie išteklių rezervavimai nuo tos dienos atšaukiami.</span><span class="sxs-lookup"><span data-stu-id="e2a26-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="e2a26-123">„Project Operations“ uždarius pasiūlymą kaip laimėtą arba pralaimėtą galimybės būsena nebus paveikta – ji bus atidaryta tol, kol nebus uždaryta rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="e2a26-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
