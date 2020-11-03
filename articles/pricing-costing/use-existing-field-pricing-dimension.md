---
title: „Project Operations“ laukų kaip kainodaros dimensijų nustatymas
description: Šioje temoje pateikiama informacija apie kainodaros dimensijas programoje „Dynamics 365 Project Operations“.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 56ff45169058d96d7ef81a710de309eec698a75f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080899"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="0cb4f-103">„Project Operations“ laukų kaip kainodaros dimensijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="0cb4f-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="0cb4f-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="0cb4f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0cb4f-105">Objektas **Faktiniai duomenys** turi daug laukų, kuriuos galima naudoti kaip išteklių kainodaros dimensijas.</span><span class="sxs-lookup"><span data-stu-id="0cb4f-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="0cb4f-106">Pavyzdžiui, vienas įprastas laukas yra **Rezervuojami ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="0cb4f-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="0cb4f-107">Mažesnėms įmonėms, turinčioms mažiau nei 20-30 apmokėtinų išteklių, gali būti paprasčiau turėti konkrečius kiekvienų išteklių sąskaitų ir savikainos tarifus.</span><span class="sxs-lookup"><span data-stu-id="0cb4f-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="0cb4f-108">Tačiau, kaip auga apmokama darbo jėga, išteklių valdymo lygis gali tapti nerealu.</span><span class="sxs-lookup"><span data-stu-id="0cb4f-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="0cb4f-109">Išteklių išlaidos ir vekselių tarifai pradeda skirtis, nes ištekliai yra skatinami, daugiau patirties arba įgyja kitą įgūdžių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="0cb4f-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="0cb4f-110">Kitas pavyzdys – operacijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="0cb4f-110">Another example is that of transaction category.</span></span> <span data-ttu-id="0cb4f-111">Klientai ir diegėjai naudojo operacijos kategoriją darbui klasifikuoti ir naudotų kainos ir savikainos lauką remiantis darbo kategorija.</span><span class="sxs-lookup"><span data-stu-id="0cb4f-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
