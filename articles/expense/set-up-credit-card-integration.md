---
title: Kredito kortelės integravimo nustatymas
description: Šioje temoje aiškinama, kaip dirbti naudojant su išlaidomis susijusias kredito kortelės operacijas.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001836"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="6419c-103">Kredito kortelės integravimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="6419c-103">Set up credit card integration</span></span>

<span data-ttu-id="6419c-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="6419c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6419c-105">Su išlaidomis susijusios kredito kortelių operacijos gali būti nustatytos taip, kad automatiškai būtų importuojamos pagal pasikartojantį grafiką.</span><span class="sxs-lookup"><span data-stu-id="6419c-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="6419c-106">Arba operacijas galima importuoti neautomatiniu būdu, nes jos būtinos.</span><span class="sxs-lookup"><span data-stu-id="6419c-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="6419c-107">Kredito kortelių operacijos importuojamos naudojant kredito kortelės operacijų duomenų objektą.</span><span class="sxs-lookup"><span data-stu-id="6419c-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="6419c-108">Importuoti kredito kortelių operacijas</span><span class="sxs-lookup"><span data-stu-id="6419c-108">Import credit card transactions</span></span>

<span data-ttu-id="6419c-109">Norėdami importuoti kredito kortelės operacijas, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6419c-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="6419c-110">Puslapyje **Kredito kortelių operacijos** pažymėkite **Importavimo operacijos**.</span><span class="sxs-lookup"><span data-stu-id="6419c-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="6419c-111">Jei pirmą kartą atidarote duomenų valdymą, sistema turi atnaujinti duomenų objektų sąrašą, kad galėtumėte tęsti.</span><span class="sxs-lookup"><span data-stu-id="6419c-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="6419c-112">Lauke **Pavadinimas** įveskite unikalų importavimo užduoties aprašą.</span><span class="sxs-lookup"><span data-stu-id="6419c-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="6419c-113">Lauke **Šaltinio duomenų formatas** pažymėkite failo, kuriame yra importuotos kredito kortelių operacijos, formatą.</span><span class="sxs-lookup"><span data-stu-id="6419c-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="6419c-114">Pažymėkite **Įkelti**, tada raskite ir pažymėkite failą, kurį norite importuoti.</span><span class="sxs-lookup"><span data-stu-id="6419c-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="6419c-115">Nusiuntę failą, patikrinkite kredito kortelės operacijos failo susiejimą ir kredito kortelės operacijų duomenų įrašo stulpelius pasirinkdami plytelės saitą **Žiūrėti struktūrą**.</span><span class="sxs-lookup"><span data-stu-id="6419c-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="6419c-116">Jei yra susiejimo klaidų, arba jei turite pakeisti susiejimą, pakeiskite susiejimą skirtuke **Susiejimo vizualizavimas** arba skirtuke **Susiejimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="6419c-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="6419c-117">Norėdami automatizuoti kredito kortelių operacijas, pažymėkite **Kurti pasikartojančias duomenų užduotis**.</span><span class="sxs-lookup"><span data-stu-id="6419c-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="6419c-118">Tada galite nustatyti pasikartojimą, apibrėžiantį, kaip dažnai reikia importuoti kreditinės kortelės operacijas.</span><span class="sxs-lookup"><span data-stu-id="6419c-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="6419c-119">Baigę pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6419c-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="6419c-120">Jei norite importuoti pažymėtą failą dabar, pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="6419c-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="6419c-121">Jei importuojant įvyksta klaidų, galite peržiūrėti vykdymo žurnalą arba paruošimo duomenis ir peržiūrėti reikiamas ištaisyti klaidas, kad užtikrintumėte, jog bus importuota sėkmingai.</span><span class="sxs-lookup"><span data-stu-id="6419c-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="6419c-122">Jei norite importuoti daugiau nei vieną failo formatą, kiekvienam formato tipui reikia sukuti atskirų importavimo užduočių.</span><span class="sxs-lookup"><span data-stu-id="6419c-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="6419c-123">Iš naujo priskirti nutrauktų darbuotojų kredito kortelių operacijas</span><span class="sxs-lookup"><span data-stu-id="6419c-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="6419c-124">Nutraukus darbuotojo įrašą, darbuotojo „Active Directory Domain Services“ (AD DS) abonementas išjungiamas.</span><span class="sxs-lookup"><span data-stu-id="6419c-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="6419c-125">Tačiau gali būti aktyvios kredito kortelių operacijos, kurios turi būti apmokamos ir kompensuojamos.</span><span class="sxs-lookup"><span data-stu-id="6419c-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="6419c-126">Puslapyje **Kredito kortelės operacijos** galite iš naujo priskirti darbuotoją bet kuriai kredito kortelės operacijai, kurios susietasis darbuotojas atleistas.</span><span class="sxs-lookup"><span data-stu-id="6419c-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="6419c-127">Pažymėkite vieną arba kelias kredito kortelės operacijas, tada pažymėkite **Iš naujo priskirti operacijas**.</span><span class="sxs-lookup"><span data-stu-id="6419c-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="6419c-128">Tada galite pasirinkti kitą darbuotoją, kad galėtumėte priskirti operacijas su kortelėmis.</span><span class="sxs-lookup"><span data-stu-id="6419c-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="6419c-129">Iš naujo pristačius operacijas su kreditinėmis kortelėmis, jas galima pažymėti išlaidų ataskaitai ir apmokėtu įprastu išlaidų ataskaitos kompensavimo procesu.</span><span class="sxs-lookup"><span data-stu-id="6419c-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="6419c-130">Kredito kortelių operacijų panaikinimas</span><span class="sxs-lookup"><span data-stu-id="6419c-130">Delete credit card transactions</span></span> 

<span data-ttu-id="6419c-131">Kartais importavus kredito kortelės operacijas, tam tikras operacijas gali tekti panaikinti.</span><span class="sxs-lookup"><span data-stu-id="6419c-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="6419c-132">Taip gali nutikti dėl to, kad operacijos yra dublikatai, arba duomenys gali būti netikslūs.</span><span class="sxs-lookup"><span data-stu-id="6419c-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="6419c-133">Administratoriai gali naudoti funkciją **Kredito kortelių operacijų panaikinimas** ir pasirinkti bei panaikinti kredito kortelių operacijas, kurios **nepridėtos** prie išlaidų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="6419c-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="6419c-134">Eikite į **Periodinės užduotys** > **Kredito kortelių operacijų panaikinimas**.</span><span class="sxs-lookup"><span data-stu-id="6419c-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="6419c-135">Pasirinkite **Filtruoti** ir pateikite informaciją, pagal kurią norite identifikuoti norimus įtraukti įrašus.</span><span class="sxs-lookup"><span data-stu-id="6419c-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="6419c-136">Norėdami panaikinti įrašus, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="6419c-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
