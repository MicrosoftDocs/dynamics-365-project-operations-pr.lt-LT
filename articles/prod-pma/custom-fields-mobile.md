---
title: Mobiliųjų įrenginių programėlės „Microsoft Dynamics 365 Project Timesheet“, skirtos „iOS“ ir „Android“, pasirinktinių laukų diegimas
description: Šioje temoje pateikiami įprasti būdai kaip naudoti plėtinius norint įdiegti pasirinktinius laukus.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003052"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="4a814-103">Mobiliųjų įrenginių programėlės „Microsoft Dynamics 365 Project Timesheet“, skirtos „iOS“ ir „Android“, pasirinktinių laukų diegimas</span><span class="sxs-lookup"><span data-stu-id="4a814-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a814-104">Šioje temoje pateikiami įprasti būdai kaip naudoti plėtinius norint įdiegti pasirinktinius laukus.</span><span class="sxs-lookup"><span data-stu-id="4a814-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="4a814-105">Aprašomos šios temos:</span><span class="sxs-lookup"><span data-stu-id="4a814-105">The following topics are covered:</span></span>

- <span data-ttu-id="4a814-106">Įvairūs duomenų tipai, kuriuos palaiko pasirinktinio lauko sistema</span><span class="sxs-lookup"><span data-stu-id="4a814-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="4a814-107">Kaip rodyti tik skaitomus arba redaguojamus grafiko įrašų laukus ir įrašyti vartotojo pateikiamas reikšmes į duomenų bazę</span><span class="sxs-lookup"><span data-stu-id="4a814-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="4a814-108">Kaip rodyti tik skaitomus laukus grafiko antraštėje</span><span class="sxs-lookup"><span data-stu-id="4a814-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="4a814-109">Kaip integruoti kitą pasirinktinę verslo logiką norint įvesti numatytąsias reikšmes į laukus ir atlikti papildomą tikrinimą</span><span class="sxs-lookup"><span data-stu-id="4a814-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="4a814-110">Auditorija</span><span class="sxs-lookup"><span data-stu-id="4a814-110">Audience</span></span>

<span data-ttu-id="4a814-111">Ši tema skirta programuotojams, integruojantiems pasirinktinius laukus į „Microsoft Dynamics 365 Project Timesheet“ mobiliųjų įrenginių programėlę, skirtą „Apple iOS“ ir „Google"Android“.</span><span class="sxs-lookup"><span data-stu-id="4a814-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="4a814-112">Daroma prielaida, kad skaitytojai yra susipažinę su X++ kūrimu ir projekto grafikų funkcijomis.</span><span class="sxs-lookup"><span data-stu-id="4a814-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="4a814-113">Duomenų sutartis – „TSTimesheetCustomField“ X++ klasė</span><span class="sxs-lookup"><span data-stu-id="4a814-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="4a814-114">**TSTimesheetCustomField** klasė yra X++ duomenų sutarties klasė, kuri pateikia informaciją apie grafiko funkcijų pasirinktinį lauką.</span><span class="sxs-lookup"><span data-stu-id="4a814-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="4a814-115">Pasirinktinio lauko objektų sąrašai perduodami į „TSTimesheetDetails“ duomenų sutartį ir „TSTimesheetEntry“ duomenų sutartį, kad būtų rodomi pasirinktiniai laukai mobiliųjų įrenginių programėlėje.</span><span class="sxs-lookup"><span data-stu-id="4a814-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="4a814-116">**TSTimesheetDetails** – grafiko antraštės sutartis.</span><span class="sxs-lookup"><span data-stu-id="4a814-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="4a814-117">**TSTimesheetEntry** – grafiko operacijos sutartis.</span><span class="sxs-lookup"><span data-stu-id="4a814-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="4a814-118">Šių objektų grupės, turinčios tą pačią projekto informaciją ir **timesheetLineRecId**, sudaro eilutę.</span><span class="sxs-lookup"><span data-stu-id="4a814-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="4a814-119">fieldBaseType (tipai)</span><span class="sxs-lookup"><span data-stu-id="4a814-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="4a814-120">Ypatybė **FieldBaseType** objekte **TsTimesheetCustom** nustato lauko, kuris rodomas programėlėje, tipą.</span><span class="sxs-lookup"><span data-stu-id="4a814-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="4a814-121">Toliau pateiktos palaikomos **Tipai** reikšmės.</span><span class="sxs-lookup"><span data-stu-id="4a814-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="4a814-122">Tipų reikšmės</span><span class="sxs-lookup"><span data-stu-id="4a814-122">Types value</span></span> | <span data-ttu-id="4a814-123">Tipas</span><span class="sxs-lookup"><span data-stu-id="4a814-123">Type</span></span>              | <span data-ttu-id="4a814-124">Pastabos</span><span class="sxs-lookup"><span data-stu-id="4a814-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="4a814-125">0</span><span class="sxs-lookup"><span data-stu-id="4a814-125">0</span></span>           | <span data-ttu-id="4a814-126">Eilutė (ir išvardijimas)</span><span class="sxs-lookup"><span data-stu-id="4a814-126">String (and Enum)</span></span> | <span data-ttu-id="4a814-127">Laukas rodomas kaip teksto laukas.</span><span class="sxs-lookup"><span data-stu-id="4a814-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="4a814-128">1</span><span class="sxs-lookup"><span data-stu-id="4a814-128">1</span></span>           | <span data-ttu-id="4a814-129">Integer</span><span class="sxs-lookup"><span data-stu-id="4a814-129">Integer</span></span>           | <span data-ttu-id="4a814-130">Reikšmė rodoma kaip skaičius be dešimtainių skilčių.</span><span class="sxs-lookup"><span data-stu-id="4a814-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="4a814-131">2</span><span class="sxs-lookup"><span data-stu-id="4a814-131">2</span></span>           | <span data-ttu-id="4a814-132">Tikroji</span><span class="sxs-lookup"><span data-stu-id="4a814-132">Real</span></span>              | <span data-ttu-id="4a814-133">Reikšmė rodoma kaip skaičius su dešimtainėmis skiltimis.</span><span class="sxs-lookup"><span data-stu-id="4a814-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="4a814-134">Norėdami tikrąją reikšmę programėlėje rodyti kaip valiutą, naudokite ypatybę **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="4a814-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="4a814-135">Ypatybę **numberOfDecimals** galite naudoti, jei norite nustatyti rodomų dešimtainių skilčių skaičių.</span><span class="sxs-lookup"><span data-stu-id="4a814-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="4a814-136">3</span><span class="sxs-lookup"><span data-stu-id="4a814-136">3</span></span>           | <span data-ttu-id="4a814-137">Data</span><span class="sxs-lookup"><span data-stu-id="4a814-137">Date</span></span>              | <span data-ttu-id="4a814-138">Datos formatai nustatomi pagal vartotojo parametrą **Datos, laiko ir skaičiaus formatas**, kuris yra nustatytas **Kalbos ir šalies / regiono nuostata** dalyje **Vartotojo parinktys**.</span><span class="sxs-lookup"><span data-stu-id="4a814-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="4a814-139">4</span><span class="sxs-lookup"><span data-stu-id="4a814-139">4</span></span>           | <span data-ttu-id="4a814-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="4a814-140">Boolean</span></span>           | |
| <span data-ttu-id="4a814-141">15</span><span class="sxs-lookup"><span data-stu-id="4a814-141">15</span></span>          | <span data-ttu-id="4a814-142">GUID</span><span class="sxs-lookup"><span data-stu-id="4a814-142">GUID</span></span>              | |
| <span data-ttu-id="4a814-143">16</span><span class="sxs-lookup"><span data-stu-id="4a814-143">16</span></span>          | <span data-ttu-id="4a814-144">Int64</span><span class="sxs-lookup"><span data-stu-id="4a814-144">Int64</span></span>             | |

- <span data-ttu-id="4a814-145">Jei ypatybė **stringOptions** nėra pateikta objekte **TSTimesheetCustomField**, laisvos formos teksto laukas pateikiamas vartotojui.</span><span class="sxs-lookup"><span data-stu-id="4a814-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="4a814-146">Ypatybė **StringLength** gali būti naudojama norint nustatyti maksimalų eilutės ilgį, kurį vartotojai gali įvesti.</span><span class="sxs-lookup"><span data-stu-id="4a814-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="4a814-147">Jei ypatybė **stringOptions** yra pateikta objekte **TSTimesheetCustomField**, šie sąrašo elementai yra vienintelės reikšmės, kurias vartotojai gali pažymėti naudodami parinkčių mygtukus (išrinkimo mygtukus).</span><span class="sxs-lookup"><span data-stu-id="4a814-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="4a814-148">Tokiu atveju eilutės laukas gali veikti kaip išvardijimo reikšmė, skirta vartotojo įrašui.</span><span class="sxs-lookup"><span data-stu-id="4a814-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="4a814-149">Norėdami įrašyti reikšmę į duomenų bazę kaip išvardijimą, rankiniu būdu (naudodami komandų grandinę) susiekite eilutės reikšmę prieš įrašydami į duomenų bazę (kaip pavyzdį žr. tolesnį šios temos skyrių „TSTimesheetEntryService“ klasės komandų grandinės naudojimas norint įrašyti grafiko įrašą iš programėlės į duomenų bazę“).</span><span class="sxs-lookup"><span data-stu-id="4a814-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="4a814-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="4a814-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="4a814-151">Naudodami šią ypatybę, galite formatuoti tikrąsias reikšmes kaip valiutą.</span><span class="sxs-lookup"><span data-stu-id="4a814-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="4a814-152">Šis metodas taikomas tik tada, kai **fieldBaseType** reikšmė yra **Tikroji**.</span><span class="sxs-lookup"><span data-stu-id="4a814-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="4a814-153">**TSCustomFieldExtendedType:None** – formatavimas netaikomas.</span><span class="sxs-lookup"><span data-stu-id="4a814-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="4a814-154">**TSCustomFieldExtendedType::Currency** – reikšmės formatavimas kaip valiutos.</span><span class="sxs-lookup"><span data-stu-id="4a814-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="4a814-155">Kai valiutos formatavimas aktyvus, lauką **stringValue** galima naudoti norint perduoti valiutos kodą, kuris turi būti rodomas programėlėje.</span><span class="sxs-lookup"><span data-stu-id="4a814-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="4a814-156">Reikšmė yra tik skaitoma.</span><span class="sxs-lookup"><span data-stu-id="4a814-156">The value is a read-only value.</span></span>

    <span data-ttu-id="4a814-157">Lauke **realValue** yra rodoma pinigų suma, kurią reikia įrašyti į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="4a814-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="4a814-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="4a814-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="4a814-159">Galite naudoti šią ypatybę norėdami nurodyti, kur programėlėje turi būti rodomas pasirinktinis laukas.</span><span class="sxs-lookup"><span data-stu-id="4a814-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="4a814-160">**TSCustomFieldSection::Header** – laukas bus rodomas programėlės skyriuje **Žiūrėti daugiau informacijos**.</span><span class="sxs-lookup"><span data-stu-id="4a814-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="4a814-161">Šie laukai visada yra tik skaitomi.</span><span class="sxs-lookup"><span data-stu-id="4a814-161">These fields are always read-only.</span></span>
- <span data-ttu-id="4a814-162">**TSCustomFieldSection::Line** – laukas bus rodomas po visų paruoštų eilutės laukų grafiko įrašuose.</span><span class="sxs-lookup"><span data-stu-id="4a814-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="4a814-163">Šiuos laukus galima arba redaguoti, arba tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="4a814-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="4a814-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="4a814-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="4a814-165">Ši ypatybė nustato lauką, kai reikšmės, kurias pateikia programėlė, įrašomos atgal į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="4a814-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="4a814-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="4a814-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="4a814-167">Ši ypatybė nustato lauką, kai reikšmės, kurias pateikia programėlė, įrašomos atgal į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="4a814-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="4a814-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="4a814-168">isEditable (NoYes)</span></span>

<span data-ttu-id="4a814-169">Nustatykite šią ypatybę kaip **Taip**, jei norite, kad lauką grafiko įrašo skyriuje galėtų redaguoti vartotojai.</span><span class="sxs-lookup"><span data-stu-id="4a814-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="4a814-170">Nustatykite ypatybę kaip **Ne**, kad laukas būtų tik skaitomas.</span><span class="sxs-lookup"><span data-stu-id="4a814-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="4a814-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="4a814-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="4a814-172">Nustatykite šią ypatybę kaip **Taip**, jei norite, kad laukas grafiko įrašo skyriuje būtų privalomas.</span><span class="sxs-lookup"><span data-stu-id="4a814-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="4a814-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="4a814-173">label (str)</span></span>

<span data-ttu-id="4a814-174">Ši ypatybė nurodo žymą, kuri rodoma šalia lauko programėlėje.</span><span class="sxs-lookup"><span data-stu-id="4a814-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="4a814-175">stringOptions (eilučių sąrašas)</span><span class="sxs-lookup"><span data-stu-id="4a814-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="4a814-176">Ši ypatybė taikoma tik tada, kai **fieldBaseType** yra nustatytas kaip **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="4a814-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="4a814-177">Jei **stringOptions** yra nustatytas, eilutės reikšmės, kurias galima pasirinkti naudojant parinkčių mygtukus (išrinkimo mygtukus), nurodomos sąrašo eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="4a814-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="4a814-178">Jei nėra jokių eilučių, galima naudoti lauko laisvos formos įrašo eilutės (pavyzdys pateiktas šios temos tolimesniame skyriuje „TSTimesheetEntryService“ klasės komandų grandinės naudojimas norint įrašyti grafiko įrašą iš programėlės atgal į duomenų bazę“).</span><span class="sxs-lookup"><span data-stu-id="4a814-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="4a814-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="4a814-179">stringLength (int)</span></span>

<span data-ttu-id="4a814-180">Ši ypatybė nurodo maksimalų eilutės lauko ilgį.</span><span class="sxs-lookup"><span data-stu-id="4a814-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="4a814-181">Ji taikoma tik tada, kai **fieldBaseType** yra nustatytas kaip **Eilutė**.</span><span class="sxs-lookup"><span data-stu-id="4a814-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="4a814-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="4a814-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="4a814-183">Šios ypatybės nurodo dešimtainių skilčių, kurios rodomos tikrajam laukui, skaičių.</span><span class="sxs-lookup"><span data-stu-id="4a814-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="4a814-184">Ji taikoma tik tada, kai **fieldBaseType** yra nustatytas kaip **Tikrasis**.</span><span class="sxs-lookup"><span data-stu-id="4a814-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="4a814-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="4a814-185">orderSequence (int)</span></span>

<span data-ttu-id="4a814-186">Ši ypatybė valdo tvarką, kuria pasirinktiniai laukai rodomi programėlėje, kai nurodomas daugiau nei vienas pasirinktinis laukas.</span><span class="sxs-lookup"><span data-stu-id="4a814-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="4a814-187">Laukai, kuriuose yra mažesni skaičiai, rodomi pirmiausia.</span><span class="sxs-lookup"><span data-stu-id="4a814-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="4a814-188">booleanValue (Bulio logikos)</span><span class="sxs-lookup"><span data-stu-id="4a814-188">booleanValue (boolean)</span></span>

<span data-ttu-id="4a814-189">**Bulio logikos** tipo laukams, ši ypatybė perduoda lauko Bulio logikos reikšmę tarp serverio ir programėlės.</span><span class="sxs-lookup"><span data-stu-id="4a814-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="4a814-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="4a814-190">guidValue (guid)</span></span>

<span data-ttu-id="4a814-191">**GUID** tipo laukams, ši ypatybė perduoda lauko globaliai unikalaus identifikatoriaus (GUID) reikšmę tarp serverio ir programėlės.</span><span class="sxs-lookup"><span data-stu-id="4a814-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="4a814-192">int64Value (Int64)</span><span class="sxs-lookup"><span data-stu-id="4a814-192">int64Value (int64)</span></span>

<span data-ttu-id="4a814-193">**Int64** tipo laukams, ši ypatybė perduoda lauko „int64“ reikšmę tarp serverio ir programėlės.</span><span class="sxs-lookup"><span data-stu-id="4a814-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="4a814-194">intValue (INT)</span><span class="sxs-lookup"><span data-stu-id="4a814-194">intValue (int)</span></span>

<span data-ttu-id="4a814-195">**Int** tipo laukams, ši ypatybė perduoda lauko „int“ reikšmę tarp serverio ir programėlės.</span><span class="sxs-lookup"><span data-stu-id="4a814-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="4a814-196">realValue (Real)</span><span class="sxs-lookup"><span data-stu-id="4a814-196">realValue (real)</span></span>

<span data-ttu-id="4a814-197">**Tikrasis** tipo laukams, ši ypatybė perduoda lauko tikrąją reikšmę tarp serverio ir programėlės.</span><span class="sxs-lookup"><span data-stu-id="4a814-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="4a814-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="4a814-198">stringValue (str)</span></span>

<span data-ttu-id="4a814-199">**Eilutė** tipo laukams, ši ypatybė perduoda lauko eilutės reikšmę tarp serverio ir programėlės.</span><span class="sxs-lookup"><span data-stu-id="4a814-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="4a814-200">Ji taip pat naudojama **Tikrasis** tipo laukams, kurie suformatuoti kaip valiuta.</span><span class="sxs-lookup"><span data-stu-id="4a814-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="4a814-201">Šiuose laukuose ypatybė naudojama valiutos kodui į programėlę perduoti.</span><span class="sxs-lookup"><span data-stu-id="4a814-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="4a814-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="4a814-202">dateValue (date)</span></span>

<span data-ttu-id="4a814-203">**Data** tipo laukams, ši ypatybė perduoda lauko datos reikšmę tarp serverio ir programėlės.</span><span class="sxs-lookup"><span data-stu-id="4a814-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="4a814-204">Pasirinktinio lauko rodymas ir įrašymas grafiko įrašo skyriuje</span><span class="sxs-lookup"><span data-stu-id="4a814-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="4a814-205">Toliau pateikiama grafiko įrašo kūrimo mobiliųjų įrenginių programėlėje ekrano kopija.</span><span class="sxs-lookup"><span data-stu-id="4a814-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="4a814-206">Joje rodomi paruošti laukai ir pasirinktinis laukas skyriuje „Laiko įrašas“, pavadinimu „Testavimo eilutė“, su jau nustatyta „Antroji parinktis“ reikšme.</span><span class="sxs-lookup"><span data-stu-id="4a814-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Testavimo eilutės pasirinktinis laukas programėlėje](media/timesheet-entry.jpg)



<span data-ttu-id="4a814-208">Toliau pateikiama mobiliųjų įrenginių programėlės ekrano kopija, kurioje vartotojas pasirenka vieną iš išvardijimo parinkčių, pasiekiamų pasirinktiniam laukui „Testavimo eilutė“.</span><span class="sxs-lookup"><span data-stu-id="4a814-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="4a814-209">Dvi parinktys – „Pirmoji parinktis“ ir „Antroji parinktis“ – yra rodomos kaip išrinkimo mygtukai.</span><span class="sxs-lookup"><span data-stu-id="4a814-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="4a814-210">Šiuo metu pasirinkta antroji parinktis.</span><span class="sxs-lookup"><span data-stu-id="4a814-210">The second option is currently selected.</span></span>

![Parinkčių mygtukai (išrinkimo mygtukai), skirti testavimo eilutės pasirinktiniam laukui](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="4a814-212">Išplėskite lentelę „TSTimesheetLine“, kad joje būtų pasirinktinis laukas</span><span class="sxs-lookup"><span data-stu-id="4a814-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="4a814-213">Esant įprastam scenarijui, gali būti, kad duomenys, skirti pasirinktiniam laukui grafiko įrašo skyriuje, bus įrašyti į lentelę „TSTimesheetLine“.</span><span class="sxs-lookup"><span data-stu-id="4a814-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="4a814-214">Tačiau galima naudoti kitas lenteles, jei duomenys gali būti nuskaitomi pagal „TSTimesheetTrans“ įrašą, kuris yra pateiktas, arba jei jis neturi specifinio įrašo konteksto (pavyzdžiui, jei lauko reikšmė nustatyta kaip tik skaitomas projekto parametruose).</span><span class="sxs-lookup"><span data-stu-id="4a814-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="4a814-215">Atkreipkite dėmesį, kad pasirinktiniai laukai neturi jokio atsarginio duomenų bazės įrašo.</span><span class="sxs-lookup"><span data-stu-id="4a814-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="4a814-216">Jie gali būti dinamiškai sugeneruoti pagal X++ logiką.</span><span class="sxs-lookup"><span data-stu-id="4a814-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="4a814-217">Šis metodas gali būti naudingas tik skaityti galimuose scenarijuose (dinamiškai sugeneruotų pasirinktinio lauko verčių pavyzdį žr. skyriuje „Komandų grandinės naudojimas klasės „TSTimesheetDetails“ metode „buildCustomFieldListForHeader“ norint užpildyti grafiko išsamią informaciją“).</span><span class="sxs-lookup"><span data-stu-id="4a814-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="4a814-218">Toliau pateikiama taikomosios programos objektų medžio „Visual Studio“ ekrano kopija.</span><span class="sxs-lookup"><span data-stu-id="4a814-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="4a814-219">Joje rodomas lentelės „TSTimesheetLine“ plėtinys su „TestLineString“ lauku, įtrauktu kaip pasirinktinis laukas.</span><span class="sxs-lookup"><span data-stu-id="4a814-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Atskira eilutė](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="4a814-221">Naudokite komandų grandinę, esančią metode „buildCustomFieldList“ klasėje „TSTimesheetSettings“, kad galėtumėte rodyti lauką grafiko įrašo skyriuje</span><span class="sxs-lookup"><span data-stu-id="4a814-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="4a814-222">Šis kodas valdo lauko rodymo parametrus programėlėje.</span><span class="sxs-lookup"><span data-stu-id="4a814-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="4a814-223">Pavyzdžiui, jis valdo lauko tipą, žymą, ar laukas yra privalomas ir kokiame skyriuje rodomas laukas.</span><span class="sxs-lookup"><span data-stu-id="4a814-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="4a814-224">Tolimesniame pavyzdyje rodomas eilutės laukas laiko įrašuose.</span><span class="sxs-lookup"><span data-stu-id="4a814-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="4a814-225">Šiame lauke yra dvi parinktys – **Pirmoji parinktis** ir **Antroji parinktis**, pasiekiamos parinkčių mygtukais (išrinkimo mygtukais).</span><span class="sxs-lookup"><span data-stu-id="4a814-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="4a814-226">Programėlės laukas yra susietas su lauku **TestLineString**, kuris yra įtraukiamas į lentelę „TSTimesheetLine“.</span><span class="sxs-lookup"><span data-stu-id="4a814-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="4a814-227">Atkreipkite dėmesį, kad **TSTimesheetCustomField::newFromMetatdata()** metodas naudojamas siekiant supaprastinti šių pasirinktinio lauko ypatybių inicijavimą: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ir **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="4a814-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="4a814-228">Taip pat galite nustatyti šiuos parametrus rankiniu būdų, jei to pageidaujate.</span><span class="sxs-lookup"><span data-stu-id="4a814-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="4a814-229">Naudokite komandų grandinę, esančią metode „buildCustomFieldListForEntry“ klasėje „TSTimesheetEntry“, kad įvestumėte reikšmes į grafiko įrašą</span><span class="sxs-lookup"><span data-stu-id="4a814-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="4a814-230">Metodas **buildCustomFieldListForEntry** naudojamas norint įvesti reikšmes į įrašytas grafiko eilutes mobiliųjų įrenginių programėlėje.</span><span class="sxs-lookup"><span data-stu-id="4a814-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="4a814-231">Kaip parametras naudojamas „TSTimesheetTrans“ įrašas.</span><span class="sxs-lookup"><span data-stu-id="4a814-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="4a814-232">Laukai iš to įrašo gali būti naudojami pasirinktinio lauko vertei užpildyti programėlėje.</span><span class="sxs-lookup"><span data-stu-id="4a814-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="4a814-233">Naudokite komandų grandinę klasėje „TSTimesheetEntryService“, kad atgal į duomenų bazę įrašytumėte grafiko įrašą</span><span class="sxs-lookup"><span data-stu-id="4a814-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="4a814-234">Norėdami vėl įrašyti pasirinktinį lauką į duomenų bazę įprasto naudojimo metu, turite išplėsti kelis metodus.</span><span class="sxs-lookup"><span data-stu-id="4a814-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="4a814-235">Metodas **timesheetLineNeedsUpdating** naudojamas norint nustatyti, ar programėlėje vartotojas pakeitė eilutės įrašą ir jis turi būti įrašytas į duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="4a814-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="4a814-236">Jei našumo problema neaktuali, šį metodą galima supaprastinti, kad jis visada grįžtų į reikšmę **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="4a814-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="4a814-237">Metodus **populateTimesheetLineFromEntryDuringCreate** ir **populateTimesheetLineFromEntryDuringUpdate** galima išplėsti, kad jie įvestų reikšmes į „TSTimesheetLine“ duomenų bazę iš pateikto „TSTimesheetEntry“ duomenų sutarties įrašo.</span><span class="sxs-lookup"><span data-stu-id="4a814-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="4a814-238">Pateiktame pavyzdyje atkreipkite dėmesį į tai, kaip duomenų bazės lauko ir įvesties lauko susiejimas rankiniu būdu atliekamas naudojant X++ kodą.</span><span class="sxs-lookup"><span data-stu-id="4a814-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="4a814-239">Metodą **populateTimesheetWeekFromEntry** taip pat galima išplėsti, jei pasirinktinis laukas, susietas su objektu **TSTimesheetEntry**, turi būti įrašytas atgal į „TSTimesheetLineweek“ duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="4a814-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="4a814-240">Toliau pateiktame pavyzdyje įrašoma **firstOption** arba **secondOption** reikšmė, kurią vartotojas pasirenka duomenų bazėje kaip pirminę eilutės reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4a814-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="4a814-241">Jei duomenų bazės laukas yra **Išvardijimas** tipo laukas, šias reikšmes galima rankiniu būdu susieti su išvardijimo reikšme ir tada įrašyti į duomenų bazės lentelės išvardijimo lauką.</span><span class="sxs-lookup"><span data-stu-id="4a814-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="4a814-242">Pasirinktinio lauko rodymas grafiko antraštės skyriuje</span><span class="sxs-lookup"><span data-stu-id="4a814-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="4a814-243">Toliau pateikiama mobiliųjų įrenginių programėlės ekrano kopija, kurioje vartotojas peržiūri grafiką.</span><span class="sxs-lookup"><span data-stu-id="4a814-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="4a814-244">Mygtukas „Daugiau informacijos“ buvo pažymėtas viršutiniame dešiniajame kampe, kad būtų rodoma parinktis „Žiūrėti daugiau informacijos“.</span><span class="sxs-lookup"><span data-stu-id="4a814-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Komanda „Žiūrėti daugiau informacijos“](media/show-more.png)

<span data-ttu-id="4a814-246">Toliau pateikiama mobiliųjų įrenginių programėlės grafiko skyriaus „Daugiau“ ekrano kopija.</span><span class="sxs-lookup"><span data-stu-id="4a814-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="4a814-247">Pasirinktinis laukas, vadinamas „Šio grafiko naudingumo koeficientas (apskaičiuotas pasirinktinis laukas)“, įtrauktas į grafiko antraštės skyrių.</span><span class="sxs-lookup"><span data-stu-id="4a814-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="4a814-248">Pasirinktiniam laukui nustatoma tik skaitymo reikšmė „0,667“.</span><span class="sxs-lookup"><span data-stu-id="4a814-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Daugiau skyrių](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="4a814-250">Išplėskite lentelę „TSTimesheetTable“, kad joje būtų pasirinktinis laukas</span><span class="sxs-lookup"><span data-stu-id="4a814-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="4a814-251">Esant įprastam scenarijui, gali būti, kad duomenys, skirti pasirinktiniam laukui antraštės skyriuje, bus ištraukti iš lentelės „TSTimesheetHeader“.</span><span class="sxs-lookup"><span data-stu-id="4a814-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="4a814-252">Tačiau galima naudoti kitas lenteles, jei duomenys gali būti nuskaitomi pagal „TSTimesheetTable“ įrašą, kuris yra pateiktas, arba jei jis neturi specifinio įrašo konteksto (pavyzdžiui, jei lauko reikšmė nustatyta kaip tik skaitomas projekto parametruose).</span><span class="sxs-lookup"><span data-stu-id="4a814-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="4a814-253">Atkreipkite dėmesį, kad pasirinktiniai laukai neturi jokio atsarginio duomenų bazės įrašo.</span><span class="sxs-lookup"><span data-stu-id="4a814-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="4a814-254">Jie gali būti dinamiškai sugeneruoti pagal X++ logiką.</span><span class="sxs-lookup"><span data-stu-id="4a814-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="4a814-255">Šis metodas parodytas tolesniame pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="4a814-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="4a814-256">Antraštės skyriaus laukai programėlėje visada yra tik skaitomi.</span><span class="sxs-lookup"><span data-stu-id="4a814-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="4a814-257">Naudokite komandų grandinę, esančią metode „buildCustomFieldList“ klasėje „TSTimesheetSettings“, kad galėtumėte rodyti lauką antraštės skyriuje</span><span class="sxs-lookup"><span data-stu-id="4a814-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="4a814-258">Šis kodas valdo lauko rodymo parametrus programėlėje.</span><span class="sxs-lookup"><span data-stu-id="4a814-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="4a814-259">Pavyzdžiui, jis valdo lauko tipą, žymą, ar laukas yra privalomas ir kokiame skyriuje rodomas laukas.</span><span class="sxs-lookup"><span data-stu-id="4a814-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="4a814-260">Toliau pateiktame pavyzdyje rodoma apskaičiuota reikšmė programėlės antraštės skyriuje.</span><span class="sxs-lookup"><span data-stu-id="4a814-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="4a814-261">Naudokite komandų grandinę, esančią metode „buildCustomFieldListForHeader“ klasėje „TSTimesheetDetails“, kad užpildytumėte grafiko išsamią informaciją</span><span class="sxs-lookup"><span data-stu-id="4a814-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="4a814-262">Metodas **buildCustomFieldListForHeader** naudojamas norint užpildyti grafiko antraštės išsamią informaciją mobiliųjų įrenginių programėlėje.</span><span class="sxs-lookup"><span data-stu-id="4a814-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="4a814-263">Kaip parametras naudojamas „TSTimesheetTable“ įrašas.</span><span class="sxs-lookup"><span data-stu-id="4a814-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="4a814-264">Laukai iš to įrašo gali būti naudojami pasirinktinio lauko vertei užpildyti programėlėje.</span><span class="sxs-lookup"><span data-stu-id="4a814-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="4a814-265">Toliau pateiktame pavyzdyje nenuskaitomos jokios reikšmės iš duomenų bazės.</span><span class="sxs-lookup"><span data-stu-id="4a814-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="4a814-266">Vietoje to naudojama X++ logika, pagal kurią sugeneruojama apskaičiuota reikšmė, kuri rodoma programėlėje.</span><span class="sxs-lookup"><span data-stu-id="4a814-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="4a814-267">Kitos konfigūravimo / išplėtimo galimybės</span><span class="sxs-lookup"><span data-stu-id="4a814-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="4a814-268">Papildomo programėlės tikrinimo įtraukimas</span><span class="sxs-lookup"><span data-stu-id="4a814-268">Adding additional validation for the app</span></span>

<span data-ttu-id="4a814-269">Esama grafiko funkcijų duomenų bazėje logika ir toliau veiks, kaip numatyta.</span><span class="sxs-lookup"><span data-stu-id="4a814-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="4a814-270">Kad būtų nutrauktos įrašymo arba pateikimo operacijos ir rodomas konkretus klaidos pranešimas, į kodą naudodami komandų plėtinio grandinę galite įtraukti **rodyti klaidą („pranešimas vartotojui“)**.</span><span class="sxs-lookup"><span data-stu-id="4a814-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="4a814-271">Toliau pateikiami trys naudingi išplečiamų metodų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="4a814-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="4a814-272">Jei grafiko eilutės įrašymo operacijos metu **validateWrite** lentelėje „TSTimesheetLine“ rodo **klaida**, mobiliųjų įrenginių programėlėje rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="4a814-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="4a814-273">Jei grafiko pateikimo į programėlę operacijos metu **validateSubmit** lentelėje „TSTimesheetTable“ rodo **klaida**, vartotojui rodomas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="4a814-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="4a814-274">Logika, kuri užpildo laukus (pvz., **Eilutės ypatybė**), kai lentelėje „TSTimesheetLine“ naudojamas metodas **įterpti**, vis dar veiks.</span><span class="sxs-lookup"><span data-stu-id="4a814-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="4a814-275">Paruoštų laukų paslėpimo ir pažymėjimo tik kaip skaitomų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="4a814-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="4a814-276">Projekto parametruose galite nustatyti, kad paruošti laukai mobiliųjų įrenginių programėlėje būtų tik skaitomi arba paslėpti.</span><span class="sxs-lookup"><span data-stu-id="4a814-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="4a814-277">Nustatykite parinktis puslapio **Projektų valdymo ir apskaitos parametrai** skyriaus **Mobiliųjų įrenginių grafikai** skirtuke **Grafikas**.</span><span class="sxs-lookup"><span data-stu-id="4a814-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Projekto parametrai](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="4a814-279">Veiklų, kurias galima pasirinkti naudojant plėtinius, keitimas</span><span class="sxs-lookup"><span data-stu-id="4a814-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="4a814-280">Veiklos, kurias galima pasirinkti projektui, užpildomos naudojant metodus **getActivitiesForProject()** ir **getActivityQuery()** klasėje **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="4a814-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="4a814-281">Galite naudoti komandų grandinę, kad pakeistumėte šį veikimą, ir veiklos, kurias galite pasirinkti konkrečiam objektui, atitiktų jūsų verslo scenarijų.</span><span class="sxs-lookup"><span data-stu-id="4a814-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="4a814-282">Numatytosios projekto kategorijos įvedimas į grafiko įrašus</span><span class="sxs-lookup"><span data-stu-id="4a814-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="4a814-283">Numatytosios projekto kategorijos įrašas grafiko įrašuose pateikiamas trimis lygiais.</span><span class="sxs-lookup"><span data-stu-id="4a814-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="4a814-284">Galite naudoti komandų grandinę, kad išplėstumėte bet kurio ar visų šių lygių veikimą ir pasiektumėte pageidaujamą veikimą.</span><span class="sxs-lookup"><span data-stu-id="4a814-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="4a814-285">Naudojama tolesnė hierarchija.</span><span class="sxs-lookup"><span data-stu-id="4a814-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="4a814-286">Programėlė bando įvesti numatytąją kategoriją iš projekto išteklių.</span><span class="sxs-lookup"><span data-stu-id="4a814-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="4a814-287">Ši numatytoji kategorija yra nustatyta metoduose **getCurrentUserResource** ir **getDelegatedResourcesForCurrentUser** klasėje **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="4a814-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="4a814-288">Jei numatytoji kategorija nepateikta projekto išteklių lygyje, programėlė bando ją ištraukti iš projekto veiklos.</span><span class="sxs-lookup"><span data-stu-id="4a814-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="4a814-289">Ši numatytoji kategorija yra nustatyta metode **getActivitiesForProject** klasėje **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="4a814-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="4a814-290">Jei numatytoji kategorija nepateikta projekto veiklos lygyje, numatytoji kategorija paimama iš projekto parametrų.</span><span class="sxs-lookup"><span data-stu-id="4a814-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="4a814-291">Ši numatytoji kategorija yra nustatyta metode **getProjectDetailsbyRule** klasėje **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="4a814-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]