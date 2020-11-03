---
title: Kas nauja arba pakeista „Project Service Automation“ V3 17 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 17 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 7ba685568692dafe117de42a71bb14d391cd7cc4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080792"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="e1993-103">„Project Service Automation“ V3 17 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="e1993-103">Project Service Automation Update Release 17, V3</span></span>

<span data-ttu-id="e1993-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="e1993-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e1993-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="e1993-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="e1993-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="e1993-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e1993-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="e1993-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="e1993-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e1993-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e1993-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti PSA V3 17 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="e1993-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="e1993-110">Ši versija turi naują komponavimo versijos numerį V3.10.6.34 ir ją galima pasiekti per 2020 m. kovo mėn. automatinį naujinimą.</span><span class="sxs-lookup"><span data-stu-id="e1993-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="e1993-111">17 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="e1993-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e1993-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="e1993-112">Bug fixes</span></span>

<span data-ttu-id="e1993-113">**Bendra**</span><span class="sxs-lookup"><span data-stu-id="e1993-113">**General**</span></span>

- <span data-ttu-id="e1993-114">Ištaisyta: atnaujinta „Project Service Automation“, kad būtų vykdomos komandos narių licencijos (projekto išteklių telkinys turės 3.x komandos narių tarnybos plano metaduomenis)</span><span class="sxs-lookup"><span data-stu-id="e1993-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="e1993-115">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="e1993-115">**Time and Expense**</span></span>

- <span data-ttu-id="e1993-116">Ištaisyta: neįmanoma pakeisti išlaidų sąmatos iš nenulinės kainos į nulinę (0).</span><span class="sxs-lookup"><span data-stu-id="e1993-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="e1993-117">Pakeitimas yra ignoruojamas.</span><span class="sxs-lookup"><span data-stu-id="e1993-117">The change is ignored.</span></span>

<span data-ttu-id="e1993-118">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="e1993-118">**Project Management**</span></span>

- <span data-ttu-id="e1993-119">Ištaisyta: nulinių reikšmių tikrinimas įtrauktas į komandos nario pareigų pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e1993-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="e1993-120">Ištaisyta: laukas **msdyn_userresourceid** objekte **msdyn_resourceassignment** nebenaudojamas.</span><span class="sxs-lookup"><span data-stu-id="e1993-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="e1993-121">Ištaisyta: naujinimas iš versijos 2.x į 3.x dabar tvarko tuščius pastangų kontūrus užduočių priskyrimuose.</span><span class="sxs-lookup"><span data-stu-id="e1993-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="e1993-122">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="e1993-122">**Sales**</span></span>

- <span data-ttu-id="e1993-123">Ištaisyta: **Invoice.PreValidateInvoiceUpdate** dabar tinkamai tvarko įrašų savininkų priskyrimo iš naujo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="e1993-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="e1993-124">Ištaisyta: kai operacijos klasė yra **Laikas** , visų objektų **UnitGroup** yra neredaguotina, įskaitant **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** ir **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="e1993-124">Fixed: When the transaction class is **Time** , **UnitGroup** is non-editable for all entities including, **QuoteLineDetails** , **JournalLine** , **InvoiceLineDetail** , and **ContractLineDetails**.</span></span> <span data-ttu-id="e1993-125">Tačiau **Vienetas** negalima redaguoti tik **JournalLine** ir **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="e1993-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


