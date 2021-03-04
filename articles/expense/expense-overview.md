---
title: Išlaidų apžvalga
description: Šioje temoje pateikiama informacija apie išlaidų funkcijas programoje „Project Operations“.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d946a8dcbf3b2369631d83e80788eed4904be95d
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764919"
---
# <a name="expense-home-page"></a><span data-ttu-id="32552-103">Išlaidų pagrindinis puslapis</span><span class="sxs-lookup"><span data-stu-id="32552-103">Expense home page</span></span>

<span data-ttu-id="32552-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="32552-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="32552-105">„Dynamics 365 Project Operations“ palaiko galimybę apdoroti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="32552-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="32552-106">Išlaidų apdorojimas vykdomas su arba be projektų naudojant tinkinamą strategijų, operacijų kategorijų ir patvirtinimų darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="32552-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="32552-107">Programoje „Project Operations“, galimi du palaikomi išlaidų visuotinio diegimo modeliai:</span><span class="sxs-lookup"><span data-stu-id="32552-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="32552-108">**Pilnas**: pilnas visuotinis diegimas galimas **„Project Operations“, skirtam išteklių / nelaikomų medžiagų scenarijams** arba **„Project Operations“, skirtam gamybos užsakymu pagrįstiems scenarijams**.</span><span class="sxs-lookup"><span data-stu-id="32552-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="32552-109">**Pagrindinis**: pagrindinis visuotinis diegimas galimas **„Project Operations“, skirtam ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams** ir **„Lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros formą**.</span><span class="sxs-lookup"><span data-stu-id="32552-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="32552-110">Visas</span><span class="sxs-lookup"><span data-stu-id="32552-110">Full</span></span> 
<span data-ttu-id="32552-111">Pilnas visuotinis išlaidų diegimas suteikia išsamų strategijos vykdymą, kuris apima galimybę kurti strategijas, pvz.:</span><span class="sxs-lookup"><span data-stu-id="32552-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="32552-112">Išlaidų kategorijos limitai</span><span class="sxs-lookup"><span data-stu-id="32552-112">Expense category limits</span></span>
  - <span data-ttu-id="32552-113">Kelionė</span><span class="sxs-lookup"><span data-stu-id="32552-113">Travel</span></span>
  - <span data-ttu-id="32552-114">Dienpinigiai</span><span class="sxs-lookup"><span data-stu-id="32552-114">Per diem</span></span>
  - <span data-ttu-id="32552-115">Kredito kortelės importavimai</span><span class="sxs-lookup"><span data-stu-id="32552-115">Credit card imports</span></span>
  - <span data-ttu-id="32552-116">Kvito optinio simbolio atpažinimas</span><span class="sxs-lookup"><span data-stu-id="32552-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="32552-117">Bazinis</span><span class="sxs-lookup"><span data-stu-id="32552-117">Basic</span></span> 
<span data-ttu-id="32552-118">Pagrindinis išlaidų visuotinio diegimo scenarijus leidžia tik įrašyti pagrindines projekto išlaidas.</span><span class="sxs-lookup"><span data-stu-id="32552-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="32552-119">Daugiau informacijos ieškokite [Išlaidų įrašas („lite“)](basic-expense.md).</span><span class="sxs-lookup"><span data-stu-id="32552-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="32552-120">Išlaidų visuotinio diegimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="32552-120">Determine your Expense deployment</span></span>
<span data-ttu-id="32552-121">Norėdami nustatyti, ar naudojate pagrindinį išlaidų valdymo visuotinį diegimą, patikrinkite, ar adreso URL baigiasi **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="32552-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
