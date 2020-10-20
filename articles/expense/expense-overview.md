---
title: Išlaidų apžvalga
description: Šioje temoje pateikiama informacija apie išlaidų funkcijas programoje „Project Operations“.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 0874b3d89e1dc0e65a51cedb82bf8f80831ca0bb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967376"
---
# <a name="expense-home-page"></a><span data-ttu-id="240c5-103">Išlaidų pagrindinis puslapis</span><span class="sxs-lookup"><span data-stu-id="240c5-103">Expense home page</span></span>

<span data-ttu-id="240c5-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="240c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="240c5-105">„Dynamics 365 Project Operations“ palaiko galimybę apdoroti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="240c5-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="240c5-106">Išlaidų apdorojimas vykdomas su arba be projektų naudojant tinkinamą strategijų, operacijų kategorijų ir patvirtinimų darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="240c5-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="240c5-107">Programoje „Project Operations“, galimi du palaikomi išlaidų visuotinio diegimo modeliai:</span><span class="sxs-lookup"><span data-stu-id="240c5-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="240c5-108">**Pilnas**: pilnas visuotinis diegimas galimas **„Project Operations“, skirtam išteklių / atsargose nelaikomomis prekėmis pagrįstiems scenarijams** arba **„Project Operations“, skirtam gamybos užsakymu pagrįstiems scenarijams**.</span><span class="sxs-lookup"><span data-stu-id="240c5-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="240c5-109">**Pagrindinis**: pagrindinis visuotinis diegimas galimas **„Project Operations“, skirtam ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams** ir **„Lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros formą**.</span><span class="sxs-lookup"><span data-stu-id="240c5-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="240c5-110">Visas</span><span class="sxs-lookup"><span data-stu-id="240c5-110">Full</span></span> 
<span data-ttu-id="240c5-111">Pilnas išlaidų visuotinis diegimas užtikrina visišką strategijos vykdymą, įskaitant galimybę kurti strategijas, pvz.:</span><span class="sxs-lookup"><span data-stu-id="240c5-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="240c5-112">Išlaidų kategorijos limitai</span><span class="sxs-lookup"><span data-stu-id="240c5-112">Expense category limits</span></span>
  - <span data-ttu-id="240c5-113">Kelionė</span><span class="sxs-lookup"><span data-stu-id="240c5-113">Travel</span></span>
  - <span data-ttu-id="240c5-114">Dienpinigiai</span><span class="sxs-lookup"><span data-stu-id="240c5-114">Per diem</span></span>
  - <span data-ttu-id="240c5-115">Kredito kortelės importavimai</span><span class="sxs-lookup"><span data-stu-id="240c5-115">Credit card imports</span></span>
  - <span data-ttu-id="240c5-116">Kvito optinio simbolio atpažinimas</span><span class="sxs-lookup"><span data-stu-id="240c5-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="240c5-117">Bazinis</span><span class="sxs-lookup"><span data-stu-id="240c5-117">Basic</span></span> 
<span data-ttu-id="240c5-118">Pagrindinis išlaidų visuotinio diegimo scenarijus leidžia tik įrašyti pagrindines projekto išlaidas.</span><span class="sxs-lookup"><span data-stu-id="240c5-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="240c5-119">Daugiau informacijos ieškokite [Išlaidų įrašas („lite“)](basic-expense.md).</span><span class="sxs-lookup"><span data-stu-id="240c5-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="240c5-120">Išlaidų visuotinio diegimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="240c5-120">Determine your Expense deployment</span></span>
<span data-ttu-id="240c5-121">Norėdami nustatyti, ar naudojate pagrindinį išlaidų valdymo visuotinį diegimą, patikrinkite, ar adreso URL baigiasi **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="240c5-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
