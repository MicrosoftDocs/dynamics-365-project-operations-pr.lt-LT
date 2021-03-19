---
title: „Project Operations“ laukų kaip kainodaros dimensijų nustatymas
description: Šioje temoje pateikiama informacijos apie laukų naudojimą, pvz., „Dynamics 365 Project Operations“ kainodaros dimensijas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274648"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="ba33d-103">„Project Operations“ laukai kaip kainodaros dimensijos</span><span class="sxs-lookup"><span data-stu-id="ba33d-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="ba33d-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="ba33d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ba33d-105">Objektas **Faktiniai duomenys** turi daug laukų, kuriuos galima naudoti kaip išteklių kainodaros dimensijas.</span><span class="sxs-lookup"><span data-stu-id="ba33d-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="ba33d-106">Pavyzdžiui, vienas įprastas laukas yra **Rezervuojami ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="ba33d-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="ba33d-107">Mažesnėms įmonėms, turinčioms mažiau nei 20-30 apmokėtinų išteklių, gali būti paprasčiau turėti konkrečius kiekvienų išteklių sąskaitų ir savikainos tarifus.</span><span class="sxs-lookup"><span data-stu-id="ba33d-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="ba33d-108">Tačiau, kaip auga apmokama darbo jėga, išteklių valdymo lygis gali tapti nerealu.</span><span class="sxs-lookup"><span data-stu-id="ba33d-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="ba33d-109">Išteklių išlaidos ir vekselių tarifai pradeda skirtis, nes ištekliai yra skatinami, daugiau patirties arba įgyja kitą įgūdžių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="ba33d-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="ba33d-110">Kitas pavyzdys – operacijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="ba33d-110">Another example is that of transaction category.</span></span> <span data-ttu-id="ba33d-111">Klientai ir diegėjai naudojo operacijos kategoriją darbui klasifikuoti ir naudotų kainos ir savikainos lauką remiantis darbo kategorija.</span><span class="sxs-lookup"><span data-stu-id="ba33d-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]