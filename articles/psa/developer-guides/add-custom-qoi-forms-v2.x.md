---
title: Įtraukti naujas pasirinktinių objektų formas (Project Service Automation 2.x)
description: Šioje temoje pateikta informacija, kaip įtraukti pasirinktinių objektų formas, skirtas galimybėms, pasiūlymams, užsakymams arba sąskaitoms faktūroms Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081030"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Įtraukti naujas pasirinktinių objektų formas (Project Service Automation 2.x)

## <a name="type-field"></a>Lauko tipas 

Dynamics 365 Project Service Automation priklauso nuo Galimybės, Pasiūlymas, Užsakymas ir Sąskaita faktūra objektuose esančio lauko **Tipas** ( **msdyn\_ordertype** ), kad būtų atskirtos šių objektų **darbo pagrindo** versijos nuo **elemento pagrindu** ir **paslaugų pagrindu** versijų. Darbo pagrįstas šių objektų versijas tvarko PSA. Daug verslo logikos kliento pusėje ir sprendimo serverio pusėje priklauso nuo lauko **Tipas**. Todėl, kai objektai kuriami, svarbu, kad laukas būtų inicijuojamas naudojant teisingą reikšmę. Neteisinga reikšmė gali sukelti neteisingą veikimą, o tam tikra verslo logika gali veikti netinkamai.

## <a name="automatic-form-switching"></a>Automatinis formų perjungimas

Kad būtų išvengta galimų duomenų sugadinimo ir nenumatyto veikimo, dėl neteisingo pardavimo objekto įrašų inicijavimo ir redagavimo, PSA dabar turi logiką automatiniam formų perjungimui laukelių formose. Ši logika nukreipia vartotojus į teisingą darbo su darbo pagrindo versija arba bet kokio kito Galimybės, Pasiūlymas, Užsakymas arba Sąskaita faktūra objekto tipo formą. Kai vartotojas atidaro Galimybės, Pasiūlymas, užsakymas arba Sąskaita faktūra objekto darbo pagrindo versiją, forma perjungiama į **Projekto informacija**.

Automatinė formų perjungimo logika priklauso nuo **formid** reikšmės ir **msdyn\_OrderType** lauko susiejimo. Visos laukelių formos įtrauktos į tą susiejimą. Tačiau pasirinktines formas reikia pridėti rankiniu būdu, kad būtų nurodoma, kurią objekto versiją jos skirtos apdoroti. Tai priklauso nuo **msdyn\_OrderType** lauko. Jei formos perjungimas nėra susiejtas, logika pereis į out-of-box formą pagal reikšmę, įrašytą objekto lauke **msdyn\_ordertype**.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Pridėkite pasirinktines formas ir įjunkite formų perjungimo logiką.

Toliau pateiktame pavyzdyje parodyta, kaip įtraukti pasirinktinę formą, **Mano projekto informacija** , kuri veiktų su darbo pagrindo galimybėmis. Tas pats procesas naudojamas pridedant pasirinktines formas taip, kad jos dirbtų su citatomis, užsakymais ir sąskaitomis faktūromis.

Norėdami sukurti pasirinktinę **Projekto informacija** formos versiją, atlikite šiuos veiksmus.

1. Galimybės objekte atidarykite **Projekto informacija** formą ir sukurkite kopiją po **Mano Projekto informacija** pavadinimu.
2. Atidarykite naują formą, tada ypatybėse įsitikinkite, kad yra formos inicijavimo scenarijai iš **Projekto informacija** formos. 

    > [!IMPORTANT]
    > Nepašalinkite scenarijų. Kitu atveju kai kurie duomenys gali būti inicijuoti neteisingai.

3. Patikrinkite, ar formoje yra **Tipas** ( **msdyn\_ordertype** ) laukas. 

    > [!IMPORTANT]
    > Nepašalinkite šio lauko. Priešingu atveju inicijavimo scenarijai nepavyks.

4. Raskite naujos formos **formid** reikšmę. Tai padaryti galite dviem skirtingais būdais:

    - Eksportuokite **Mano projekto informacija** formą kaip nevaldomojo sprendimo dalį, tada susiraskite **formid** reikšmę eksportuoto sprendimo faile customization.xml.
    - Formų rengyklėje atidarykite **Mano projekto informacija** formą, tada URL ieškokite visuotinio unikalaus identifikatoriaus (GUID) šalia **fromid** parametro, kaip pavaizduota sekančioje iliustracijoje.

    ![Naujos formos formId reikšmė URL](media/how-to-add-custom-forms-in-v2.0.png)

5. Sukurkite **msdyn\_ordertype** susiejimą su **formid** reikšme redaguodami msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js žiniatinklio išteklių. Pašalinkite kodą iš ištekliaus ir jį pakeiskite šiuo kodu.

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

6. Įrašykite ir publikuokite tinkinimus.
