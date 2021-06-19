---
title: Darbas su asmeninėmis išlaidomis išlaidų ataskaitoje
description: Šioje temoje pateikiama informacija apie tai, kaip dirbti su asmeninėmis išlaidomis, kurias darbuotojai patiria keliaudami verslo tikslais.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025694"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="becfa-103">Darbas su asmeninėmis išlaidomis išlaidų ataskaitoje</span><span class="sxs-lookup"><span data-stu-id="becfa-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="becfa-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="becfa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="becfa-105">Verslo kelionių metu darbuotojas gali apmokėti asmenines išlaidas savo įmonės kredito kortele.</span><span class="sxs-lookup"><span data-stu-id="becfa-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="becfa-106">Jei asmeninių išlaidų tvarkymo procesas nenurodytas, išlaidų ataskaitos patvirtinimo procesas gali būti sutrikdytas darbuotojui pateikus su preke susijusių išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="becfa-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="becfa-107">Yra du būdai, kuriuos galite naudoti norėdami dirbti su darbuotojo asmeninėmis išlaidomis:</span><span class="sxs-lookup"><span data-stu-id="becfa-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="becfa-108">**Apmokėta darbuotojo**: jūsų organizacija neapmoka asmeninių išlaidų, kurios rodomos įmonės kredito kortelės sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="becfa-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="becfa-109">Vietoje to, darbuotojas moka kredito kortelės tiekėjui tiesiogiai už išlaidas.</span><span class="sxs-lookup"><span data-stu-id="becfa-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="becfa-110">**Apmokėta įmonės**: jūsų organizacija apmoka visą sąskaitą už įmonės kredito kortelę, o tada nurašo nuo darbuotojo sąskaitos asmeninėms išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="becfa-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="becfa-111">Būdą, kurį jūsų organizacija naudoja, galite pasirinkti puslapyje **Išlaidų valdymo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="becfa-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="becfa-112">Įjungti išlaidų skaidymo funkciją, kai asmeninės sumos lauke yra nustatyta reikšmė</span><span class="sxs-lookup"><span data-stu-id="becfa-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="becfa-113">Funkcija **Įjungti išlaidų skaidymo funkciją, kai asmeninės sumos lauke yra nustatyta reikšmė** taikoma tik išlaidų ataskaitoms, kurios yra patvirtintos naudojant eilutės lygio darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="becfa-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="becfa-114">Ataskaitos yra patvirtinamos įėjus į **Išlaidų ataskaitų apdorojimas** > **Išlaidų ataskaitos, priskirtos man** > **Atidaryti išlaidų ataskaitą**.</span><span class="sxs-lookup"><span data-stu-id="becfa-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="becfa-115">Norėdami įjungti šią funkciją, eikite į **Darbo sritys** > **Funkcijų tvarkymas**, pasirinkite **Įjungti išlaidų skaidymo funkciją, kai asmeninės sumos lauke yra nustatyta reikšmė**, tada pažymėkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="becfa-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="becfa-116">Kai ši funkcija įjungta, išlaidų eilutės, kurios naudoja šią funkciją, pateikia dvi eilutes, kai pateikiama ataskaita.</span><span class="sxs-lookup"><span data-stu-id="becfa-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="becfa-117">Dvi eilutės generuojamos taip, kad tvirtinantojas galėtų patvirtinti kiekvieną eilutę atskirai.</span><span class="sxs-lookup"><span data-stu-id="becfa-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
