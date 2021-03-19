---
title: Vidinių projektų apskaitos konfigūravimas
description: Šioje temoje pateikta informacija, kaip nustatyti vidinių projektų apskaitos praktikas naudojant „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287608"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="0e020-103">Vidinių projektų apskaitos konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="0e020-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="0e020-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="0e020-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0e020-105">Vidiniai projektai įmonėms suteikia galimybę sekti išlaidas, susijusias su veiklomis, už kurias klientui negalima išrašyti sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="0e020-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="0e020-106">Vidinių projektų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="0e020-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="0e020-107">Produkto kūrimas, pvz., mobiliųjų įrenginių programėlės, ir su kūrimu susijusių išlaidų sekimas.</span><span class="sxs-lookup"><span data-stu-id="0e020-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="0e020-108">Laiko ir išlaidų valdymas iki pardavimo.</span><span class="sxs-lookup"><span data-stu-id="0e020-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="0e020-109">Šį vidinį projektą iki pardavimo galima konvertuoti vėliau į apmokestinamą projektą, jei pasiūlymas laimėtas.</span><span class="sxs-lookup"><span data-stu-id="0e020-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="0e020-110">Bet kuris su „Dynamics 365 Project Operations“ sutartimi nesusietas projektas laikomas vidiniu.</span><span class="sxs-lookup"><span data-stu-id="0e020-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="0e020-111">Projekto išlaidų ir pajamų profiliai nėra naudojami nustatant projekto apskaitos taisykles.</span><span class="sxs-lookup"><span data-stu-id="0e020-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="0e020-112">Vidinio projekto savikaina visada registruojama naudojant pelno ir nuostolio principus.</span><span class="sxs-lookup"><span data-stu-id="0e020-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="0e020-113">Registravimo DK sąskaitos apibrėžtos puslapyje **DK registravimo sąranka**.</span><span class="sxs-lookup"><span data-stu-id="0e020-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="0e020-114">Laiko operacijos registruojamos atskaitant sumas iš **išlaidų** sąskaitos ir įskaitant jas į **algalapio priskyrimo** sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="0e020-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="0e020-115">Išlaidų operacijos registruojamos atskaitant sumas iš **išlaidų** sąskaitos ir įskaitant jas į **korespondentinę sąskaitą už išlaidas**.</span><span class="sxs-lookup"><span data-stu-id="0e020-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="0e020-116">Užregistravus operacijas projekte, jei projektas susietas su projekto sutartimi, sistema anuliuoja visas sukauptas operacijas ir sukuria naujas apmokestinamas operacijas.</span><span class="sxs-lookup"><span data-stu-id="0e020-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="0e020-117">Apmokestinamos operacijos atitinka apskaitos taisykles, apibrėžtas atitinkamame projekto išlaidų ir pajamų profilyje.</span><span class="sxs-lookup"><span data-stu-id="0e020-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]