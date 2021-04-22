---
title: Projekto sutarties patvirtinimas
description: Šioje temoje pateikta informacija, kaip patvirtinti sutartį programoje „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d807d3631f40a93ec7dbd918b64c287fd4875c79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273838"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="fa57e-103">Projekto sutarties patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="fa57e-103">Confirm a project contract</span></span>

<span data-ttu-id="fa57e-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="fa57e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fa57e-105">„Dynamics 365 Project Operations“ projekto sutartis gali būti aktyvi dėl tipo **Patvirtinta** arba uždaryta dėl tipo **Pralaimėta**.</span><span class="sxs-lookup"><span data-stu-id="fa57e-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="fa57e-106">Patvirtinus projekto sutartį, būsena atnaujinama iš **Juodraštis** į **Aktyvi** ir būsenos tipas yra **Patvirtinta**.</span><span class="sxs-lookup"><span data-stu-id="fa57e-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="fa57e-107">Aktyvios arba uždarytos sutarties negalima redaguoti arba atidaryti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="fa57e-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="fa57e-108">Projekto sutarties patvirtinimo finansinis poveikis</span><span class="sxs-lookup"><span data-stu-id="fa57e-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="fa57e-109">Kai patvirtinama projekto sutartis, programa perskaičiuoja išlaidas atšaukdama senesnius išlaidų faktinius duomenis ir iš naujo sukurdama naujus išlaidų faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="fa57e-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="fa57e-110">Tada apdorojamos naujos faktinės išlaidos pagal susietos projekto sutarties eilutės atsiskaitymo būdą.</span><span class="sxs-lookup"><span data-stu-id="fa57e-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="fa57e-111">Jei faktinių išlaidų nuoroda yra laiko ir medžiagų sutarties eilutė, programa automatiškai perkuria atitinkamas neapmokestintas pardavimo faktines sumas.</span><span class="sxs-lookup"><span data-stu-id="fa57e-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="fa57e-112">Jei faktinių išlaidų nuoroda yra fiksuotos kainos sutarties eilutė, programa sustabdo pakartotinį faktinių išlaidų apdorojimą.</span><span class="sxs-lookup"><span data-stu-id="fa57e-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="fa57e-113">Siekiant neviršyti apribojimų, apmokestinamumo sąranka, kainodaros bei faktinių išlaidos yra įvertinamos ir tada atnaujinamos kaip patvirtinimo proceso dalis.</span><span class="sxs-lookup"><span data-stu-id="fa57e-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="fa57e-114">Projekto sutarties kaip prarastos uždarymas</span><span class="sxs-lookup"><span data-stu-id="fa57e-114">Close a project contract as lost</span></span>

<span data-ttu-id="fa57e-115">Kai uždarote projekto sutartį kaip prarastą, sutarties būsena atnaujinama į **Uždaryta**, o būsenos tipas yra **Prarasta**.</span><span class="sxs-lookup"><span data-stu-id="fa57e-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="fa57e-116">Projekto sutartis tampa tik skaitoma.</span><span class="sxs-lookup"><span data-stu-id="fa57e-116">The project contract becomes read-only.</span></span> <span data-ttu-id="fa57e-117">Prieš įvykdant keitimus pateikiamas patvirtinimo dialogo langas, nes uždarytos projekto sutarties iš naujo atidaryti negalima.</span><span class="sxs-lookup"><span data-stu-id="fa57e-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="fa57e-118">Jei projekto sutarties, kuri uždaryta kaip prarasta, eilutėse nurodytas projektas, tas projektas taip pat pažymimas kaip uždarytas.</span><span class="sxs-lookup"><span data-stu-id="fa57e-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="fa57e-119">Nuo tos dienos atšaukiami visi išteklių rezervavimai.</span><span class="sxs-lookup"><span data-stu-id="fa57e-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="fa57e-120">Visos neapmokestintos faktinės pardavimo sumos, kurių dar nėra sąskaitoje faktūroje, bus anuliuotos.</span><span class="sxs-lookup"><span data-stu-id="fa57e-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="fa57e-121">Jei „Dynamics 365 Project Operations“ uždarysite projekto sutartį kaip pralaimėtą, tai nepadarys įtakos susietos galimybės būsenai.</span><span class="sxs-lookup"><span data-stu-id="fa57e-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="fa57e-122">Galimybė liks atidaryta ir ją reikės uždaryti neautomatiškai.</span><span class="sxs-lookup"><span data-stu-id="fa57e-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]