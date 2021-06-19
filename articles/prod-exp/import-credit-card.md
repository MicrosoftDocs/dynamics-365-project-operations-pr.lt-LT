---
title: Kredito kortelių operacijų importavimas ir tvarkymas
description: Šioje temoje aiškinama, kaip importuoti ir prižiūrėti su išlaidomis susijusias kredito kortelių operacijas. Šias operacijas galima nustatyti taip, kad jos būtų automatiškai importuojamos pagal pasikartojantį grafiką, arba pagal poreikį jas galima importuoti neautomatiškai.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edeab157aa2fa6cf518ad086b4c1f22c5b45fa04
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005171"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="575b8-104">Kredito kortelių operacijų importavimas ir tvarkymas</span><span class="sxs-lookup"><span data-stu-id="575b8-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="575b8-105">Su išlaidomis susijusios kredito kortelių operacijos gali būti nustatytos taip, kad automatiškai būtų importuojamos pagal pasikartojantį grafiką.</span><span class="sxs-lookup"><span data-stu-id="575b8-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="575b8-106">Arba operacijas galima importuoti neautomatiniu būdu, nes jos būtinos.</span><span class="sxs-lookup"><span data-stu-id="575b8-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="575b8-107">Naudojant kredito kortelių operacijas duomenų objektas importuojamas.</span><span class="sxs-lookup"><span data-stu-id="575b8-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="575b8-108">Daugiau informacijos apie duomenų objektus žr. [Duomenų objektai](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="575b8-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="575b8-109">Importuoti kredito kortelių operacijas</span><span class="sxs-lookup"><span data-stu-id="575b8-109">Import credit card transactions</span></span>

1. <span data-ttu-id="575b8-110">Puslapyje **Kredito kortelių operacijos** pažymėkite **Importavimo operacijos**.</span><span class="sxs-lookup"><span data-stu-id="575b8-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="575b8-111">Jei pirmą kartą atidarote duomenų valdymą, sistema turi atnaujinti duomenų objektų sąrašą, kad galėtumėte tęsti.</span><span class="sxs-lookup"><span data-stu-id="575b8-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="575b8-112">Lauke **Pavadinimas** įveskite unikalų importavimo užduoties aprašą.</span><span class="sxs-lookup"><span data-stu-id="575b8-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="575b8-113">Lauke **Šaltinio duomenų formatas** pažymėkite failo, kuriame yra importuotos kredito kortelių operacijos, formatą.</span><span class="sxs-lookup"><span data-stu-id="575b8-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="575b8-114">Pažymėkite **Įkelti**, tada raskite ir pažymėkite failą, kurį norite importuoti.</span><span class="sxs-lookup"><span data-stu-id="575b8-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="575b8-115">Įkėlus failą, patikrinkite kredito kortelės operacijos failo susiejimą ir kredito kortelių operacijų duomenų įrašo stulpelius pasirinkdami plytelės saitą **Žiūrėti struktūrą**.</span><span class="sxs-lookup"><span data-stu-id="575b8-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="575b8-116">Jei yra susiejimo klaidų, arba jei turite pakeisti susiejimą, pakeiskite susiejimą skirtuke **Susiejimo vizualizavimas** arba skirtuke **Susiejimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="575b8-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="575b8-117">Norėdami automatizuoti kredito kortelių operacijas, pažymėkite **Kurti pasikartojančias duomenų užduotis**.</span><span class="sxs-lookup"><span data-stu-id="575b8-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="575b8-118">Tada galite nustatyti pasikartojimą, apibrėžiantį, kaip dažnai reikia importuoti kreditinės kortelės operacijas.</span><span class="sxs-lookup"><span data-stu-id="575b8-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="575b8-119">Baigę pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="575b8-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="575b8-120">Jei norite importuoti pažymėtą failą dabar, pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="575b8-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="575b8-121">Jei importuojant įvyksta klaida, galite peržiūrėti vykdymo žurnalą arba sustojimo duomenis, kad pamatytumėte klaidas, kurias reikia pataisyti, kad būtų galima užtikrinti sėkmingą importavimą.</span><span class="sxs-lookup"><span data-stu-id="575b8-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="575b8-122">Jei turite importuoti daugiau nei vieną failo formatą, turite sukurti atskiras kiekvieno formato tipo importavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="575b8-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="575b8-123">Iš naujo priskirti nutrauktų darbuotojų kredito kortelių operacijas</span><span class="sxs-lookup"><span data-stu-id="575b8-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="575b8-124">Nutraukus darbuotojo įrašą, darbuotojo „Active Directory Domain Services“ (AD DS) abonementas išjungiamas.</span><span class="sxs-lookup"><span data-stu-id="575b8-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="575b8-125">Tačiau gali būti aktyvios kredito kortelių operacijos, kurios turi būti apmokamos ir kompensuojamos.</span><span class="sxs-lookup"><span data-stu-id="575b8-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="575b8-126">Puslapyje **Kreditinių kortelių operacijos**, galite iš naujo paskirti darbuotoją bet kuriai kredito kortelės operacijai, kai susijęs darbuotojas buvo nutrauktas.</span><span class="sxs-lookup"><span data-stu-id="575b8-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="575b8-127">Pažymėkite vieną arba kelias kredito kortelės operacijas, tada pažymėkite **Iš naujo priskirti operacijas**.</span><span class="sxs-lookup"><span data-stu-id="575b8-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="575b8-128">Tada galite pasirinkti kitą darbuotoją, kad galėtumėte priskirti operacijas su kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="575b8-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="575b8-129">Iš naujo pristačius operacijas su kreditinėmis kortelėmis, jas galima pažymėti išlaidų ataskaitai ir apmokėtu įprastu išlaidų ataskaitos kompensavimo procesu.</span><span class="sxs-lookup"><span data-stu-id="575b8-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]