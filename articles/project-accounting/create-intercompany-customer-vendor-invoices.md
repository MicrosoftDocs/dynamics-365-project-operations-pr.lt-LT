---
title: Įmonės vidaus kliento ir tiekėjo sąskaitų faktūrų kūrimas
description: Šioje temoje pateikiama informacija, kaip kurti įmonės vidaus klientų ir tiekėjų sąskaitas faktūras.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dd9aa1a4d167d556206a487e79983090b3f4592a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287473"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a><span data-ttu-id="241eb-103">Įmonės vidaus kliento ir tiekėjo sąskaitų faktūrų kūrimas</span><span class="sxs-lookup"><span data-stu-id="241eb-103">Create intercompany customer and vendor invoices</span></span>

<span data-ttu-id="241eb-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="241eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="241eb-105">Projekto apskaitininkas skolinimo juridiniame objekte sukuria įmonės vidaus kliento sąskaitą faktūrą, kurioje nurodomos projekto išlaidos, perduodamos skolinimosi juridiniam objektui.</span><span class="sxs-lookup"><span data-stu-id="241eb-105">A project accountant in a lending legal entity creates an intercompany customer invoice for the project costs that are being transferred to the borrowing entity.</span></span> <span data-ttu-id="241eb-106">Įmonės vidaus kliento sąskaitą faktūrą patvirtinus ir užregistravus, skolinimo juridinis objektas įmonės vidaus sąskaitą faktūrą siunčia skolinimosi juridiniam objektui.</span><span class="sxs-lookup"><span data-stu-id="241eb-106">After the intercompany customer invoice is approved and posted, the lending legal entity sends the intercompany invoice to the borrowing legal entity.</span></span>

<span data-ttu-id="241eb-107">Skolinimo juridinio objekto projekto apskaitininkas gali nustatyti paketinį procesą, kad įmonės vidaus sąskaitos faktūros būtų generuojamos reguliariai.</span><span class="sxs-lookup"><span data-stu-id="241eb-107">The project accountant for the lending legal entity can set up a batch process to generate intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="241eb-108">Kad būtų sukurtos paketinės įmonės vidaus sąskaitos faktūros, projekto apskaitininkas nurodo kriterijus, pvz., konkrečius projektus.</span><span class="sxs-lookup"><span data-stu-id="241eb-108">The project accountant specifies the criteria, such as specific projects, to create intercompany invoices in a batch.</span></span>

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a><span data-ttu-id="241eb-109">Neautomatinis įmonės vidaus klientų sąskaitų faktūrų, skirtų projekto operacijoms, kūrimas</span><span class="sxs-lookup"><span data-stu-id="241eb-109">Manually create an intercompany customer invoice for project transactions</span></span> 

<span data-ttu-id="241eb-110">Šią procedūrą naudokite, jei norite neautomatiškai kurti įmonės vidaus klientų sąskaitas faktūras, skirtas projekto operacijoms.</span><span class="sxs-lookup"><span data-stu-id="241eb-110">Use this procedure to manually create an intercompany customer invoice for project transactions.</span></span> <span data-ttu-id="241eb-111">Ieškokite valandų, kurias užregistravo su projektais dirbantys darbuotojai skolinimosi juridiniuose objektuose, ir išlaidų, kurias patyrė jūsų juridinis objektas dėl skolinimosi juridinių objektų.</span><span class="sxs-lookup"><span data-stu-id="241eb-111">Search for hours that were posted by workers on projects in the borrowing legal entities and for expenses that were incurred by your legal entity on behalf of borrowing legal entities.</span></span> <span data-ttu-id="241eb-112">Galite ieškoti pagal juridinio objekto pavadinimą, projekto sutarties numerį, projekto numerį, datos diapazoną arba pagal bet kokį šių parinkčių derinį.</span><span class="sxs-lookup"><span data-stu-id="241eb-112">You can search by legal entity name, project contract number, project number, date range, or any combination of these options.</span></span> <span data-ttu-id="241eb-113">Ieškos rezultatuose pasirinkite operacijas, kurias norite įtraukti į įmonės vidaus sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="241eb-113">In the search results, select the transactions to add to an intercompany invoice.</span></span>

1. <span data-ttu-id="241eb-114">Programoje „Dynamics 365 Finance“ eikite į **Projektų valdymas ir apskaita** > **Projekto sąskaitos faktūros** > **Vidinių įmonių klientų SF**.</span><span class="sxs-lookup"><span data-stu-id="241eb-114">In Dynamics 365 Finance, go to **Project management and accounting** > **Project invoices** > **Intercompany customer invoices**.</span></span> <span data-ttu-id="241eb-115">**Vidinių įmonių klientų SF** sąrašo puslapyje esančioje veiksmų srityje pasirinkite **Naujas.**</span><span class="sxs-lookup"><span data-stu-id="241eb-115">On the **Intercompany customer invoices**  list page, on the Action Pane, select **New.**</span></span>
2. <span data-ttu-id="241eb-116">Puslapyje **Kurti vidinės įmonės SF**, lauke **Juridinis objektas**, pasirinkite skolinimosi juridinį objektą.</span><span class="sxs-lookup"><span data-stu-id="241eb-116">On the **Create intercompany invoice** page, in the **Legal entity** field, select a borrowing legal entity.</span></span>
3. <span data-ttu-id="241eb-117">Pasirinktinai: įveskite konkrečios projekto sutarties ir projekto numerius.</span><span class="sxs-lookup"><span data-stu-id="241eb-117">Optional: Enter a specific project contract and project number.</span></span>
4. <span data-ttu-id="241eb-118">Susiaurinkite iešką pasirinkdami datų diapazoną.</span><span class="sxs-lookup"><span data-stu-id="241eb-118">Narrow the search by selecting a date range.</span></span> <span data-ttu-id="241eb-119">Laukuose **Pradžios data** ir **Pabaigos data** įveskite konkrečias datas.</span><span class="sxs-lookup"><span data-stu-id="241eb-119">Enter specific dates in the **Start date** and **End date** fields.</span></span> <span data-ttu-id="241eb-120">Ieškos rezultatuose rodomos tik tos įmonės vidaus operacijos, kurios užregistruotos šio datų diapazono ribose.</span><span class="sxs-lookup"><span data-stu-id="241eb-120">Only intercompany transactions that are posted within this date range are displayed in the search results.</span></span>
5. <span data-ttu-id="241eb-121">Nustatykite **išplėstinio projekto žurnalo eilutės parametrą** kaip **Taip** ir pasirinkite **Ieškoti**.</span><span class="sxs-lookup"><span data-stu-id="241eb-121">Set **Project advanced journal line parameter** to **Yes** and select **Search**.</span></span>
6. <span data-ttu-id="241eb-122">Ieškos rezultatuose pasirinkite operacijas, kurias norite įtraukti į įmonės vidaus sąskaitos faktūros pasiūlymą, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="241eb-122">In the search results, select the transactions to include in the intercompany invoice proposal, and then select **OK**.</span></span>
7. <span data-ttu-id="241eb-123">**Vidinių įmonių klientų SF** puslapyje rodomos iš ieškos rezultatų pasirinktos įmonės vidaus projekto operacijos.</span><span class="sxs-lookup"><span data-stu-id="241eb-123">On the **Intercompany customer invoice** page, the intercompany project transactions that you selected from the search results are displayed.</span></span> <span data-ttu-id="241eb-124">Jei norite modifikuoti operacijas prieš išsiųsdami sąskaitą faktūrą skolinimosi juridiniam objektui, atlikite toliau nurodytus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="241eb-124">To modify the transactions before you send the invoice to the borrowing legal entity, do the following:</span></span>
  
    1. <span data-ttu-id="241eb-125">Atidarykite puslapį **Kurti SF pasiūlymą**.</span><span class="sxs-lookup"><span data-stu-id="241eb-125">Open the **Create invoice proposal** page.</span></span> <span data-ttu-id="241eb-126">Pasirinkite papildomas šios sąskaitos faktūros įmonės vidaus operacijas, o tada pasirinkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="241eb-126">Select additional intercompany transactions for the current invoice, and then select **Add line**.</span></span>
    2. <span data-ttu-id="241eb-127">Jei norite eilutę pašalinti, pažymėkite ją, tada pasirinkite **Šalinti**.</span><span class="sxs-lookup"><span data-stu-id="241eb-127">To remove a line, select it, and then select **Remove**.</span></span>
    3. <span data-ttu-id="241eb-128">Peržiūrėkite komentarus, priežastis, finansines dimensijas ir kitą informaciją apie pasirinktą eilutę, naudodami **Sąskaitos faktūros eilutės**  „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="241eb-128">View comments, reasons, financial dimensions, and other information about a selected line on the  **Invoice lines**  FastTab.</span></span>
    
8. <span data-ttu-id="241eb-129">Jei įmonės vidaus kliento sąskaitą faktūrą norite užregistruoti, veiksmų srityje pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="241eb-129">To post the intercompany customer invoice, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="241eb-130">Jei jūsų organizacija reikalauja, kad prieš užregistruojant įmonės vidaus sąskaitos faktūros turi būti peržiūrėtos, sistemos administratorius gali nustatyti įmonės vidaus sąskaitų faktūrų darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="241eb-130">If your organization requires that intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="241eb-131">Jei įmonės vidaus sąskaitų faktūrų darbo eiga nenustatyta, įmonės vidaus sąskaitą faktūrą galite užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="241eb-131">If a workflow is not set up for intercompany invoices, you can post the intercompany invoice.</span></span>

## <a name="create-a-batch-job-for-intercompany-invoices"></a><span data-ttu-id="241eb-132">Įmonės vidaus sąskaitų faktūrų paketinės užduoties kūrimas</span><span class="sxs-lookup"><span data-stu-id="241eb-132">Create a batch job for intercompany invoices</span></span>

<span data-ttu-id="241eb-133">Vienu metu galite sukurti keletą įmonės vidaus sąskaitų faktūrų visiems skolinimosi juridiniams objektams.</span><span class="sxs-lookup"><span data-stu-id="241eb-133">You can create multiple intercompany invoices at the same time for all borrowing legal entities.</span></span> <span data-ttu-id="241eb-134">Naudodami ieškos funkcijas galite ieškoti, pvz., visų operacijų, kurias užregistravo pasiskolinti darbuotojai, ir susijusių su projektais, kuriuos valdo kiti juridiniai objektai.</span><span class="sxs-lookup"><span data-stu-id="241eb-134">Using search functionality, you can for example, search for all transactions that are posted by borrowed workers and related to projects that are managed by other legal entities.</span></span> <span data-ttu-id="241eb-135">Tada kiekvienam skolinimosi juridiniam objektui galite sukurti įmonės vidaus sąskaitą faktūrą, skirtą operacijoms, kurios nurodytos ieškos rezultatuose.</span><span class="sxs-lookup"><span data-stu-id="241eb-135">Then, for each borrowing legal entity, you can create an intercompany invoice for the transactions provided in the search results.</span></span>

1. <span data-ttu-id="241eb-136">Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Projekto sąskaitos faktūros** > **Kurti vidinių įmonių klientų SF**.</span><span class="sxs-lookup"><span data-stu-id="241eb-136">Go to **Project management and accounting** > **Periodic** > **Project invoices** > **Create intercompany customer invoices**.</span></span>
2. <span data-ttu-id="241eb-137">Puslapyje **Kurti vidinių įmonių klientų SF**, lauke **Įmonė**, pasirinkite juridinį objektą, kuriam kurti sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="241eb-137">On the **Create intercompany customer invoices** page, in the **Company**  field, select a legal entity to invoice.</span></span> <span data-ttu-id="241eb-138">Jei nepasirinksite įmonės, bus rodomos visų skolinimosi juridinių objektų visos operacijos, atitinkančios ieškos kriterijus.</span><span class="sxs-lookup"><span data-stu-id="241eb-138">If you don't select a company, all transactions that meet the search criteria are displayed for all borrowing legal entities.</span></span>
3. <span data-ttu-id="241eb-139">Dalyje **Kurti po vieną SF** pasirinkite, ar kurti įmonės vidaus operacijų sąskaitą faktūrą pagal projektą ar pagal skolinimosi juridinį objektą.</span><span class="sxs-lookup"><span data-stu-id="241eb-139">In **Create one invoice per**, select whether to create an invoice for intercompany transactions based on a project or based on a borrowing legal entity.</span></span>
4. <span data-ttu-id="241eb-140">Pasirinktinai: jei norite pasirinkti konkretų projektą ir projekto sutartį, kad būtų sukurtos įmonės vidaus sąskaitos faktūros, spustelėkite **Pasirinkti**.</span><span class="sxs-lookup"><span data-stu-id="241eb-140">Optional: To select a specific project and project contract to create intercompany invoices for, click **Select**.</span></span> <span data-ttu-id="241eb-141">Puslapyje **Užklausa**, lauke **Kriterijai**, pasirinkite projekto sutartį, projekto numerį (arba abu), o tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="241eb-141">On the **Inquiry** page, in the **Criteria** field, select the project contract, project number, or both, and then select **OK**.</span></span>
5. <span data-ttu-id="241eb-142">Skirtuke **Paketas** nustatykite paketinį procesą, kad įmonės vidaus sąskaitos faktūros būtų kuriamos reguliariai.</span><span class="sxs-lookup"><span data-stu-id="241eb-142">On the **Batch** tab, set up a batch process to create intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="241eb-143">Daugiau informacijos žr. [Paketinio apdorojimo užduoties pateikimas naudojant formą](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).</span><span class="sxs-lookup"><span data-stu-id="241eb-143">For more information, see [Submit a batch processing job from a form](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).</span></span>
6. <span data-ttu-id="241eb-144">Jei įmonės vidaus sąskaitas faktūras norite užregistruoti, veiksmų srityje pasirinkite **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="241eb-144">To post the intercompany invoices, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="241eb-145">Jei jūsų organizacija reikalauja prieš užregistruojant įmonės vidaus sąskaitas faktūras peržiūrėti, sistemos administratorius gali nustatyti įmonės vidaus sąskaitų faktūrų darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="241eb-145">If your organization requires intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="241eb-146">Jei įmonės vidaus sąskaitų faktūrų darbo eiga nenustatyta, įmonės vidaus sąskaitas faktūras galite užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="241eb-146">If a workflow is not set up for intercompany invoices, you can post the intercompany invoices.</span></span>

## <a name="post-the-intercompany-vendor-invoice"></a><span data-ttu-id="241eb-147">Įmonės vidaus tiekėjo sąskaitos faktūros registravimas</span><span class="sxs-lookup"><span data-stu-id="241eb-147">Post the intercompany vendor invoice</span></span>

<span data-ttu-id="241eb-148">Užregistravus atitinkamą įmonės vidaus kliento sąskaitą faktūrą, skolinimosi juridinio objekto projekto apskaitininkas gali peržiūrėti laukiančias įmonės vidaus tiekėjo sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="241eb-148">A project accountant in the borrowing legal entity can review intercompany pending vendor invoices when the corresponding intercompany customer invoice is posted.</span></span> <span data-ttu-id="241eb-149">Finansų srityje, skolinimosi juridiniame objekte, eikite į **Mokėtinos sumos** > **Sąskaitos faktūros** > **Laukianti tiekėjo SF**.</span><span class="sxs-lookup"><span data-stu-id="241eb-149">In Finance, in the borrowing legal entity, go to **Accounts payable** > **Invoices** > **Pending vendor invoice**.</span></span> <span data-ttu-id="241eb-150">Laukiančios sąskaitos faktūros numeris sutaps su įmonės vidaus kliento sąskaitos faktūros numeriu.</span><span class="sxs-lookup"><span data-stu-id="241eb-150">The pending invoice number will match the intercompany customer invoice number.</span></span> <span data-ttu-id="241eb-151">Patikrinkite, ar sąskaita faktūra teisinga, o tada ją užregistruokite.</span><span class="sxs-lookup"><span data-stu-id="241eb-151">Verify that the invoice is correct and then post the invoice.</span></span> <span data-ttu-id="241eb-152">Įmonės vidaus tiekėjo sąskaitą faktūrą užregistravus, sukuriama projekto antrinės knygos ir didžiosios knygos operacija, atspindinti operacijos išlaidas skolinimosi juridiniame objekte.</span><span class="sxs-lookup"><span data-stu-id="241eb-152">Posting intercompany vendor invoice creates a project subledger and a general ledger transaction that reflects the transaction costs in the borrowing legal entity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]