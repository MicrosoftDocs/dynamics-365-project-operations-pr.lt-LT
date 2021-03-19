---
title: Dienpinigiai
description: Šioje temoje pateikta informacija apie dienpinigių taisykles, kurios naudojamos išlaidų valdyme.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 70e26a5e0f9a06730a2166318006429195335d4d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276313"
---
# <a name="per-diems"></a><span data-ttu-id="7cdd6-103">Dienpinigiai</span><span class="sxs-lookup"><span data-stu-id="7cdd6-103">Per diems</span></span>

<span data-ttu-id="7cdd6-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="7cdd6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="7cdd6-105">Dienpinigiai yra pašalpa, mokama darbuotojui, kuris keliauja darbo reikalais.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="7cdd6-106">Išlaidų valdyme galite sukurti dienpinigius skirtingoms keliavimo situacijoms.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="7cdd6-107">Dienpinigiai gali būti pagrįsti metų laiku, kelionės vieta arba abiem.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="7cdd6-108">Kai sukuriate dienpinigius, galite nurodyti, kad už dienpinigius procentinė dalis bus išskaičiuota, jei darbuotojas gaus papildomą maitinimą ar aptarnavimą.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="7cdd6-109">Taip pat galite nustatyti mažiausią ir didžiausią valandų skaičių, už kurias būtų skiriami dienpinigiai darbuotojui keliaujant.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="7cdd6-110">Konfigūracija</span><span class="sxs-lookup"><span data-stu-id="7cdd6-110">Configuration</span></span> 

1. <span data-ttu-id="7cdd6-111">Norėdami įtraukti dienpinigius, eikite į **Sąranka** > **Skaičiavimai ir kodai** > **Dienpinigių vietos**.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="7cdd6-112">Kiekvienai įtrauktai vietai pažymėkite dienpinigius ir valiutą, galiojančią nuo konkrečios pradžios iki pabaigos datos viešbučiui, maitinimuisi ir kitoms išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="7cdd6-113">Dienpinigiai ir valiutos sukonfigūruojami **Sąranka** > **Skaičiavimai ir kodai** > **Dienpinigiai**.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="7cdd6-114">Puslapyje **Dienpinigių vietos** konfigūruokite dienpinigių normas.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="7cdd6-115">Dienpinigių normos leidžia apibrėžti viešbučių, maitinimosi ir kitų išlaidų dienos pašalpos procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="7cdd6-116">Jei norite nurodyti mažesnę procentinę dalį pusryčiams, pietums arba vakarienei, atnaujinkite laukų, esančių puslapio **Išlaidų valdymo parametrai** skirtuke **Dienpinigiai**, reikšmes.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="7cdd6-117">Pateikti išlaidas pagal dienpinigius</span><span class="sxs-lookup"><span data-stu-id="7cdd6-117">Submit expenses using per diem</span></span>
<span data-ttu-id="7cdd6-118">Norėdami pateikti išlaidas, panaudojant dienpinigius, kurdami išlaidų ataskaitą naudokite išlaidų kategoriją **Dienpinigiai**.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="7cdd6-119">Įveskite reikšmes **Dienpinigiai nuo datos**, **Dienpinigiai iki datos** ir **Dienpinigių vietos**.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="7cdd6-120">Suma bus apskaičiuota pagal pasirinktos vietos dienpinigius, o mažesnė procentinė dalis už maistą bus apskaičiuota pagal dienpinigių normas.</span><span class="sxs-lookup"><span data-stu-id="7cdd6-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]