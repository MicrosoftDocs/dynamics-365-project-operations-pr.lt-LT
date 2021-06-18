---
title: Atsargose nelaikomų medžiagų įsigijimas naudojant laukiančią tiekėjo sąskaitą faktūrą
description: Šioje temoje paaiškinama, kaip įrašyti laukiančias tiekėjų sąskaitas faktūras.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993813"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="4edac-103">Atsargose nelaikomų medžiagų įsigijimas naudojant laukiančią tiekėjo sąskaitą faktūrą</span><span class="sxs-lookup"><span data-stu-id="4edac-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="4edac-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="4edac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4edac-105">Kai įmonė projektui įsigyja atsargose nelaikomų medžiagų, galima iš karto įrašyti projekto kaštus.</span><span class="sxs-lookup"><span data-stu-id="4edac-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="4edac-106">Pavyzdžiui, „Contoso Robotics US“ vykdo įrangos atnaujinimo projektą ir turi gauti programinės įrangos licencijų.</span><span class="sxs-lookup"><span data-stu-id="4edac-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="4edac-107">Šios licencijos įsigyjamos iš trečiosios šalies tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="4edac-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="4edac-108">Naudodamas „Dynamics 365 Finance“, mokėtinų sumų klerkas įrašo laukiančios tiekėjo sąskaitos faktūros dokumentą, o licencijos kaštus tiesiogiai priskiria įrangos atnaujinimo projektui.</span><span class="sxs-lookup"><span data-stu-id="4edac-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="4edac-109">Prieš naudodami šioje temoje aprašytas funkcijas, peržiūrėkite ir pritaikykite reikiamas konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="4edac-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="4edac-110">Norėdami sužinoti daugiau, žr. [Galimybės naudoti atsargose nelaikomas medžiagas ir laukiančias tiekėjų sąskaitas faktūras įjungimas](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="4edac-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="4edac-111">Su projektu susijusios laukiančios tiekėjo sąskaitos faktūros registravimas</span><span class="sxs-lookup"><span data-stu-id="4edac-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="4edac-112">Laukiančias tiekėjų sąskaitas faktūras galima įrašyti puslapyje **Laukiančios tiekėjų sąskaitos faktūros** (**Mokėtinos sumos** > **Sąskaitos faktūros** > **Laukiančios tiekėjų sąskaitos faktūros**).</span><span class="sxs-lookup"><span data-stu-id="4edac-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="4edac-113">Norėdami registruoti su projektu susijusią laukiančią tiekėjo sąskaitą faktūrą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="4edac-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="4edac-114">Nueikite į **Mokėtinos sumos** > **Sąskaitos faktūros** ir pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="4edac-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="4edac-115">Lauke **Sąskaitos faktūros klientas** pasirinkite tiekėją, o lauke **Numeris** įveskite tiekėjo sąskaitos faktūros identifikavimo duomenis.</span><span class="sxs-lookup"><span data-stu-id="4edac-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="4edac-116">Į tiekėjo sąskaitą faktūrą įtraukite eilutę, o lauke **Prekės numeris** pasirinkite iš tiekėjo įsigytą atsargose nelaikomą prekę.</span><span class="sxs-lookup"><span data-stu-id="4edac-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="4edac-117">Tiekėjų sąskaitų faktūrų eilučių, pagrįstų viešųjų pirkimų kategorija, pagal projektą įrašyti negalima.</span><span class="sxs-lookup"><span data-stu-id="4edac-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="4edac-118">Įtraukite įsigytą kiekį.</span><span class="sxs-lookup"><span data-stu-id="4edac-118">Add the quantity purchased.</span></span> <span data-ttu-id="4edac-119">Sistema automatiškai įves vieneto kainą pagal ne atsargose laikomos prekės kainos konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="4edac-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="4edac-120">Patikrinkite bendrąją sumą ir kitą reikiamą informaciją eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4edac-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="4edac-121">Eilutės išsamios informacijos srities skirtuke **Projektas** pasirinkite projekto, į kurį bus įrašoma ši prekė, ID.</span><span class="sxs-lookup"><span data-stu-id="4edac-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="4edac-122">Arba pasirinkite veiklos numerį ir atnaujinkite projekto kategoriją bei eilutės ypatybę.</span><span class="sxs-lookup"><span data-stu-id="4edac-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="4edac-123">Užregistruokite laukiančią tiekėjo sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="4edac-123">Post pending vendor invoice.</span></span> <span data-ttu-id="4edac-124">Kai sąskaita faktūra užregistruojama, sistema įrašo toliau nurodytus dalykus.</span><span class="sxs-lookup"><span data-stu-id="4edac-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="4edac-125">Tiekėjo balanso suma.</span><span class="sxs-lookup"><span data-stu-id="4edac-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="4edac-126">PVM suma.</span><span class="sxs-lookup"><span data-stu-id="4edac-126">The sales tax amount.</span></span>
    - <span data-ttu-id="4edac-127">Projekto kaštai įrašomi į viešųjų pirkimų integravimo sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="4edac-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="4edac-128">Projekto faktinė operacija sprendime „Dataverse“.</span><span class="sxs-lookup"><span data-stu-id="4edac-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="4edac-129">Ši operacija toliau apdorojama naudojant [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="4edac-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="4edac-130">Užregistravus šį žurnalą, suma iš viešųjų pirkimų integravimo sąskaitos perkeliama į projekto kaštų sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="4edac-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
