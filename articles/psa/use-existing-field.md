---
title: „Project Service“ esamo lauko kaip kainodaros dimensijos naudojimas
description: Šioje temoje pateikta informacija apie tai, kaip esamus „Project Service“ laukus naudoti kaip kainodaros dimensijas.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281578"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="142da-103">„Project Service“ esamo lauko kaip kainodaros dimensijos naudojimas</span><span class="sxs-lookup"><span data-stu-id="142da-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="142da-104">„Project Service Automation“ (PSA) objekte **Faktiniai duomenys** yra daug laukų, kuriuos galima naudoti kaip kainodaros dimensijas ištekliais grindžiamai kainodarai projekto organizacijose.</span><span class="sxs-lookup"><span data-stu-id="142da-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="142da-105">Pavyzdžiui, vienas įprastas laukas yra **Rezervuojami ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="142da-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="142da-106">Mažesnėms įmonėms, turinčioms mažiau nei 20-30 apmokėtinų išteklių, gali būti paprasčiau turėti konkrečius kiekvienų išteklių sąskaitų ir savikainos tarifus.</span><span class="sxs-lookup"><span data-stu-id="142da-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="142da-107">Tačiau, kai apmokestinama darbo jėga didėja, konkrečius tarifus gali būti nerealistiška išlaikyti, nes ištekliaus savikaina ir sąskaitų tarifas pradeda skirtis, kai ištekliai perkeliami į aukštesnį lygį, įgyja daugiau patirties arba kitokių įgūdžių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="142da-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="142da-108">Kadangi šis metodas vis tiek tinka tam tikro dydžio įmonėms, žr. temą [Rezervuojamų išteklių kaip kainodaros dimensijos naudojimas](bookable-resource-pricing-dimension.md), kad suprastumėte, kaip esamą „Project Service“ lauką galima naudoti kaip kainodaros dimensiją.</span><span class="sxs-lookup"><span data-stu-id="142da-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="142da-109">Kitas pavyzdys – operacijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="142da-109">Another example is that of transaction category.</span></span> <span data-ttu-id="142da-110">Klientai ir diegėjai naudojo PSA operacijos kategoriją darbui klasifikuoti ir naudotų kainos ir savikainos lauką remiantis darbo kategorija.</span><span class="sxs-lookup"><span data-stu-id="142da-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="142da-111">Daugiau informacijos žr. [Operacijos kategorijos kaip kainodaros dimensijos naudojimas](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="142da-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]