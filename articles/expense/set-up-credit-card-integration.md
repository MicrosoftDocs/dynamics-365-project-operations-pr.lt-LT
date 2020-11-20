---
title: Kredito kortelės integravimo nustatymas
description: Šioje temoje aiškinama, kaip importuoti ir prižiūrėti su išlaidomis susijusias kredito kortelių operacijas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120868"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="d285c-103">Kredito kortelės integravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d285c-103">Set up credit card integration</span></span>

<span data-ttu-id="d285c-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="d285c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d285c-105">Su išlaidomis susijusios kredito kortelių operacijos gali būti nustatytos taip, kad automatiškai būtų importuojamos pagal pasikartojantį grafiką.</span><span class="sxs-lookup"><span data-stu-id="d285c-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="d285c-106">Arba operacijas galima importuoti neautomatiniu būdu, nes jos būtinos.</span><span class="sxs-lookup"><span data-stu-id="d285c-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="d285c-107">Naudojant kredito kortelių operacijas duomenų objektas importuojamas.</span><span class="sxs-lookup"><span data-stu-id="d285c-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="d285c-108">Importuoti kredito kortelių operacijas</span><span class="sxs-lookup"><span data-stu-id="d285c-108">Import credit card transactions</span></span>

1. <span data-ttu-id="d285c-109">Puslapyje **Kredito kortelių operacijos** pažymėkite **Importavimo operacijos**.</span><span class="sxs-lookup"><span data-stu-id="d285c-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="d285c-110">Jei pirmą kartą atidarote duomenų valdymą, sistema turi atnaujinti duomenų objektų sąrašą, kad galėtumėte tęsti.</span><span class="sxs-lookup"><span data-stu-id="d285c-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="d285c-111">Lauke **Pavadinimas** įveskite unikalų importavimo užduoties aprašą.</span><span class="sxs-lookup"><span data-stu-id="d285c-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="d285c-112">Lauke **Šaltinio duomenų formatas** pažymėkite failo, kuriame yra importuotos kredito kortelių operacijos, formatą.</span><span class="sxs-lookup"><span data-stu-id="d285c-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="d285c-113">Pažymėkite **Įkelti**, tada raskite ir pažymėkite failą, kurį norite importuoti.</span><span class="sxs-lookup"><span data-stu-id="d285c-113">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="d285c-114">Įkėlus failą, patikrinkite kredito kortelės operacijos failo susiejimą ir kredito kortelių operacijų duomenų įrašo stulpelius pasirinkdami plytelės saitą **Žiūrėti struktūrą**.</span><span class="sxs-lookup"><span data-stu-id="d285c-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="d285c-115">Jei yra susiejimo klaidų, arba jei turite pakeisti susiejimą, pakeiskite susiejimą skirtuke **Susiejimo vizualizavimas** arba skirtuke **Susiejimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="d285c-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="d285c-116">Norėdami automatizuoti kredito kortelių operacijas, pažymėkite **Kurti pasikartojančias duomenų užduotis**.</span><span class="sxs-lookup"><span data-stu-id="d285c-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="d285c-117">Tada galite nustatyti pasikartojimą, apibrėžiantį, kaip dažnai reikia importuoti kreditinės kortelės operacijas.</span><span class="sxs-lookup"><span data-stu-id="d285c-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="d285c-118">Baigę pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d285c-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="d285c-119">Jei norite importuoti pažymėtą failą dabar, pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="d285c-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="d285c-120">Jei importuojant įvyksta klaida, galite peržiūrėti vykdymo žurnalą arba sustojimo duomenis, kad pamatytumėte klaidas, kurias reikia pataisyti, kad būtų galima užtikrinti sėkmingą importavimą.</span><span class="sxs-lookup"><span data-stu-id="d285c-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="d285c-121">Jei turite importuoti daugiau nei vieną failo formatą, turite sukurti atskiras kiekvieno formato tipo importavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="d285c-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="d285c-122">Iš naujo priskirti nutrauktų darbuotojų kredito kortelių operacijas</span><span class="sxs-lookup"><span data-stu-id="d285c-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="d285c-123">Nutraukus darbuotojo įrašą, darbuotojo „Active Directory Domain Services“ (AD DS) abonementas išjungiamas.</span><span class="sxs-lookup"><span data-stu-id="d285c-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="d285c-124">Tačiau gali būti aktyvios kredito kortelių operacijos, kurios turi būti apmokamos ir kompensuojamos.</span><span class="sxs-lookup"><span data-stu-id="d285c-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="d285c-125">Puslapyje **Kreditinių kortelių operacijos**, galite iš naujo paskirti darbuotoją bet kuriai kredito kortelės operacijai, kai susijęs darbuotojas buvo nutrauktas.</span><span class="sxs-lookup"><span data-stu-id="d285c-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="d285c-126">Pažymėkite vieną arba kelias kredito kortelės operacijas, tada pažymėkite **Iš naujo priskirti operacijas**.</span><span class="sxs-lookup"><span data-stu-id="d285c-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="d285c-127">Tada galite pasirinkti kitą darbuotoją, kad galėtumėte priskirti operacijas su kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="d285c-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="d285c-128">Iš naujo pristačius operacijas su kreditinėmis kortelėmis, jas galima pažymėti išlaidų ataskaitai ir apmokėtu įprastu išlaidų ataskaitos kompensavimo procesu.</span><span class="sxs-lookup"><span data-stu-id="d285c-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
