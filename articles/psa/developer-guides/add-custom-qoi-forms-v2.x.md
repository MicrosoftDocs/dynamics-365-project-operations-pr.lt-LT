---
title: Įtraukti naujas pasirinktinių objektų formas (Project Service Automation 2.x)
description: Šioje temoje pateikta informacija, kaip įtraukti pasirinktinių objektų formas, skirtas galimybėms, pasiūlymams, užsakymams arba sąskaitoms faktūroms Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 400d817ee7cbae6f6da95db4286ad6c4d6ff349a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008006"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="fdfac-103">Įtraukti naujas pasirinktinių objektų formas (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="fdfac-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="fdfac-104">Lauko tipas</span><span class="sxs-lookup"><span data-stu-id="fdfac-104">Type field</span></span> 

<span data-ttu-id="fdfac-105">Dynamics 365 Project Service Automation priklauso nuo Galimybės, Pasiūlymas, Užsakymas ir Sąskaita faktūra objektuose esančio lauko **Tipas** (**msdyn\_ordertype**), kad būtų atskirtos šių objektų **darbo pagrindo** versijos nuo **elemento pagrindu** ir **paslaugų pagrindu** versijų.</span><span class="sxs-lookup"><span data-stu-id="fdfac-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="fdfac-106">Darbo pagrįstas šių objektų versijas tvarko PSA.</span><span class="sxs-lookup"><span data-stu-id="fdfac-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="fdfac-107">Daug verslo logikos kliento pusėje ir sprendimo serverio pusėje priklauso nuo lauko **Tipas**.</span><span class="sxs-lookup"><span data-stu-id="fdfac-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="fdfac-108">Todėl, kai objektai kuriami, svarbu, kad laukas būtų inicijuojamas naudojant teisingą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fdfac-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="fdfac-109">Neteisinga reikšmė gali sukelti neteisingą veikimą, o tam tikra verslo logika gali veikti netinkamai.</span><span class="sxs-lookup"><span data-stu-id="fdfac-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="fdfac-110">Automatinis formų perjungimas</span><span class="sxs-lookup"><span data-stu-id="fdfac-110">Automatic form switching</span></span>

<span data-ttu-id="fdfac-111">Kad būtų išvengta galimų duomenų sugadinimo ir nenumatyto veikimo, dėl neteisingo pardavimo objekto įrašų inicijavimo ir redagavimo, PSA dabar turi logiką automatiniam formų perjungimui laukelių formose.</span><span class="sxs-lookup"><span data-stu-id="fdfac-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="fdfac-112">Ši logika nukreipia vartotojus į teisingą darbo su darbo pagrindo versija arba bet kokio kito Galimybės, Pasiūlymas, Užsakymas arba Sąskaita faktūra objekto tipo formą.</span><span class="sxs-lookup"><span data-stu-id="fdfac-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="fdfac-113">Kai vartotojas atidaro Galimybės, Pasiūlymas, užsakymas arba Sąskaita faktūra objekto darbo pagrindo versiją, forma perjungiama į **Projekto informacija**.</span><span class="sxs-lookup"><span data-stu-id="fdfac-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="fdfac-114">Automatinė formų perjungimo logika priklauso nuo **formid** reikšmės ir **msdyn\_OrderType** lauko susiejimo.</span><span class="sxs-lookup"><span data-stu-id="fdfac-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="fdfac-115">Visos laukelių formos įtrauktos į tą susiejimą.</span><span class="sxs-lookup"><span data-stu-id="fdfac-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="fdfac-116">Tačiau pasirinktines formas reikia pridėti rankiniu būdu, kad būtų nurodoma, kurią objekto versiją jos skirtos apdoroti.</span><span class="sxs-lookup"><span data-stu-id="fdfac-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="fdfac-117">Tai priklauso nuo **msdyn\_OrderType** lauko.</span><span class="sxs-lookup"><span data-stu-id="fdfac-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="fdfac-118">Jei formos perjungimas nėra susiejtas, logika pereis į out-of-box formą pagal reikšmę, įrašytą objekto lauke **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="fdfac-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="fdfac-119">Pridėkite pasirinktines formas ir įjunkite formų perjungimo logiką.</span><span class="sxs-lookup"><span data-stu-id="fdfac-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="fdfac-120">Toliau pateiktame pavyzdyje parodyta, kaip įtraukti pasirinktinę formą, **Mano projekto informacija**, kuri veiktų su darbo pagrindo galimybėmis.</span><span class="sxs-lookup"><span data-stu-id="fdfac-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="fdfac-121">Tas pats procesas naudojamas pridedant pasirinktines formas taip, kad jos dirbtų su citatomis, užsakymais ir sąskaitomis faktūromis.</span><span class="sxs-lookup"><span data-stu-id="fdfac-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="fdfac-122">Norėdami sukurti pasirinktinę **Projekto informacija** formos versiją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="fdfac-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="fdfac-123">Galimybės objekte atidarykite **Projekto informacija** formą ir sukurkite kopiją po **Mano Projekto informacija** pavadinimu.</span><span class="sxs-lookup"><span data-stu-id="fdfac-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="fdfac-124">Atidarykite naują formą, tada ypatybėse įsitikinkite, kad yra formos inicijavimo scenarijai iš **Projekto informacija** formos.</span><span class="sxs-lookup"><span data-stu-id="fdfac-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="fdfac-125">Nepašalinkite scenarijų.</span><span class="sxs-lookup"><span data-stu-id="fdfac-125">Don't remove the scripts.</span></span> <span data-ttu-id="fdfac-126">Kitu atveju kai kurie duomenys gali būti inicijuoti neteisingai.</span><span class="sxs-lookup"><span data-stu-id="fdfac-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="fdfac-127">Patikrinkite, ar formoje yra **Tipas** (**msdyn\_ordertype**) laukas.</span><span class="sxs-lookup"><span data-stu-id="fdfac-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="fdfac-128">Nepašalinkite šio lauko.</span><span class="sxs-lookup"><span data-stu-id="fdfac-128">Don't remove this field.</span></span> <span data-ttu-id="fdfac-129">Priešingu atveju inicijavimo scenarijai nepavyks.</span><span class="sxs-lookup"><span data-stu-id="fdfac-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="fdfac-130">Raskite naujos formos **formid** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="fdfac-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="fdfac-131">Tai padaryti galite dviem skirtingais būdais:</span><span class="sxs-lookup"><span data-stu-id="fdfac-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="fdfac-132">Eksportuokite **Mano projekto informacija** formą kaip nevaldomojo sprendimo dalį, tada susiraskite **formid** reikšmę eksportuoto sprendimo faile customization.xml.</span><span class="sxs-lookup"><span data-stu-id="fdfac-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="fdfac-133">Formų rengyklėje atidarykite **Mano projekto informacija** formą, tada URL ieškokite visuotinio unikalaus identifikatoriaus (GUID) šalia **fromid** parametro, kaip pavaizduota sekančioje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="fdfac-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Naujos formos formId reikšmė URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="fdfac-135">Sukurkite **msdyn\_ordertype** susiejimą su **formid** reikšme redaguodami msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js žiniatinklio išteklių.</span><span class="sxs-lookup"><span data-stu-id="fdfac-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="fdfac-136">Pašalinkite kodą iš ištekliaus ir jį pakeiskite šiuo kodu.</span><span class="sxs-lookup"><span data-stu-id="fdfac-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="fdfac-137">Įrašykite ir publikuokite tinkinimus.</span><span class="sxs-lookup"><span data-stu-id="fdfac-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]