---
title: Pasiūlymo eilutės apmokestinamų komponentų konfigūravimas
description: Šioje temoje pateikta informacija apie apmokestinamų ir neapmokestinamų komponentų nustatymą projektais pagrįsto pasiūlymo eilutėje.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858303"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Pasiūlymo eilutės apmokestinamų komponentų konfigūravimas 

_**Taikoma (kam):** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projektais pagrįsto pasiūlymo eilutėje pateikiama *įtrauktų* ir *apmokestinamų* sąvoka.

Įtrauktiems komponentams taikomos toliau nurodytos sąlygos.

  - Sąskaitų išrašymo būdo ir klientų išskaidymas
  - Limitas, kurio negalima viršyti 
  - Sąskaitos faktūros dažnio parametrai, apibrėžti projektais pagrįsto pasiūlymo eilutėje

Įtrauktų komponentų pogrupis gali būti pažymėtas kaip apmokestinamas naudojant lauką **Atsiskaitymo tipas**. Laukas **Atsiskaitymo tipas** yra parinkčių rinkinys, leidžiantis toliau nurodytas reikšmes pasiūlymo eilutės kontekste.

  - Apmokestinama
  - Neapmokestinama

Apmokestinamus komponentus galima apibrėžti užduotyse, vaidmenyse ir operacijų kategorijose.

Pasiūlymo eilutės apmokestinamumas apibrėžiamas užduotyse ir taikomas visoms į eilutę įtrauktoms operacijų klasėms. Jei laukas **Įtraukti užduotis** yra tuščias arba nustatytas į parinktį **Visas projektas**, skirtukas **Apmokestinamos užduotys** nebus pateiktas.

Pasiūlymo eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei. Jei projekto pasiūlymo eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinami vaidmenys** nebus pateiktas.

Pasiūlymo eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei. Jei projekto pasiūlymo eilutės laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinamos kategorijos** nebus pateiktas.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Projekto užduoties atnaujinimas į apmokestinamą arba neapmokestinamą

Projekto užduotis gali būti apmokestinama arba neapmokestinama konkrečios projektais pagrįsto pasiūlymo eilutės kontekste, todėl galima nustatyti toliau nurodytą sąranką.

Jei projekto pasiūlymo eilutėje yra **Laikas** ir užduotis **T1**, užduotis susieta su pasiūlymo eilute kaip apmokestinama. Jei antroje išlaidas eilutėje yra **Išlaidos**, **T1** užduotį galite susieti išlaidas eilutėje kaip neapmokestinamą. Todėl visas laikas, užfiksuotas užduotyje, yra apmokestinamas, o visos užduotyje įrašytos išlaidos – neapmokestinamos.

Užduoties sąskaitų išrašymo tipą galima sukonfigūruoti projektu pagrįstos pasiūlymo eilutės skirtuke **Apmokestinamosios užduotys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Pasiūlymo eilučių užduotys**. Arba galite atnaujinti projekto užduoties atsiskaitymo tipą lauke **Atsiskaitymo tipas**, esantį projekto, kuriame pasiūlymo eilutės rodomos kaip susietos su užduotimi, atsiskaitymo už užduotis sąrankos papildomame tinklelyje.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą

Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečios projektais pagrįsto pasiūlymo eilutės kontekste.

Vaidmens sąskaitų išrašymo tipą galima sukonfigūruoti pasiūlymo eilutės skirtuke **Apmokestinamieji vaidmenys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamieji vaidmenys**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą

Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje pasiūlymo eilutėje.

Operacijos sąskaitų išrašymo tipą galima sukonfigūruoti pasiūlymo eilutės skirtuke **Apmokestinamosios kategorijos**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamosios kategorijos**.

### <a name="resolve-chargeability"></a>Apmokestinamumo sprendimas
Įvertinimas arba faktiniai sukurti laikui duomenys bus apmokestinami tik esant toliau nurodytoms sąlygoms.

   - Į pasiūlymo eilutę įtraukta reikšmė **Laikas**.
   - Pasiūlymo eilutėje **Vaidmuo** yra sukonfigūruotas kaip apmokestinamas.
   - Pasiūlymo eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**. 

Jei šie trys punktai atitinkami, **užduotis** taip pat sukonfigūruojama kaip apmokestinama. 

Įvertinimas arba faktiniai sukurti išlaidoms duomenys apmokestinami tik esant toliau nurodytoms sąlygoms. 

   - Į pasiūlymo eilutę įtraukta reikšmė **Išlaidos**.
   - Pasiūlymo eilutėje **Operacijos kategorija** yra sukonfigūruota kaip apmokestinama.
   - Pasiūlymo eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**.

Jei šie trys punktai atitinkami, **užduotis** taip pat sukonfigūruojama kaip apmokestinama. 

Įvertinimas arba faktiniai sukurti medžiagai duomenys bus apmokestinami tik esant toliau nurodytoms sąlygoms.

   - Į pasiūlymo eilutę įtraukta reikšmė **Medžiagos**.
   - Pasiūlymo eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**.

Jei šie du punktai atitinkami, **užduotis** taip pat gali būti sukonfigūruota kaip apmokestinama. 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Įtrauktas laikas</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Įtrauktos išlaidos</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Įtrauktos medžiagos</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Įtrauktos užduotys</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Vaidmuo</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategorija.</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Užduotis</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Poveikis apmokestinimui</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Taip </p>
            </td>
            <td width="78" valign="top">
                <p>
Taip </p>
            </td>
            <td width="63" valign="top">
                <p>
Taip </p>
            </td>
            <td width="75" valign="top">
                <p>
Visas projektas </p>
            </td>
            <td width="65" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="70" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="65" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką: Apmokestinamas </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: Apmokestinamas </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: Apmokestinama </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Taip </p>
            </td>
            <td width="78" valign="top">
                <p>
Taip </p>
            </td>
            <td width="63" valign="top">
                <p>
Taip </p>
            </td>
            <td width="75" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="65" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="70" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="65" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką: Apmokestinamas </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: Apmokestinamas </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: Apmokestinama </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Taip </p>
            </td>
            <td width="78" valign="top">
                <p>
Taip </p>
            </td>
            <td width="63" valign="top">
                <p>
Taip </p>
            </td>
            <td width="75" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neapmokestinama</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="65" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: Apmokestinamas </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: Apmokestinama </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Taip </p>
            </td>
            <td width="78" valign="top">
                <p>
Taip </p>
            </td>
            <td width="63" valign="top">
                <p>
Taip </p>
            </td>
            <td width="75" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="65" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="70" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neapmokestinama</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: <strong>Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: <strong>Neapmokestinamas</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Taip </p>
            </td>
            <td width="78" valign="top">
                <p>
Taip </p>
            </td>
            <td width="63" valign="top">
                <p>
Taip </p>
            </td>
            <td width="75" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neapmokestinama</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neapmokestinama</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: <strong>Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: <strong> Neapmokestinamas</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Taip </p>
            </td>
            <td width="78" valign="top">
                <p>
Taip </p>
            </td>
            <td width="63" valign="top">
                <p>
Taip </p>
            </td>
            <td width="75" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neapmokestinama</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Neapmokestinama</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: <strong> Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: Apmokestinama </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Taip </p>
            </td>
            <td width="63" valign="top">
                <p>
Taip </p>
            </td>
            <td width="75" valign="top">
                <p>
Visas projektas </p>
            </td>
            <td width="65" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Apmokestinama</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką: <strong>Nėra</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: Apmokestinamas </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: Apmokestinama </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Taip </p>
            </td>
            <td width="63" valign="top">
                <p>
Taip </p>
            </td>
            <td width="75" valign="top">
                <p>
Visas projektas </p>
            </td>
            <td width="65" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Neapmokestinama</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką: <strong>Nėra</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: <strong> Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: Apmokestinama </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Taip </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Taip </p>
            </td>
            <td width="75" valign="top">
                <p>
Visas projektas </p>
            </td>
            <td width="65" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="70" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="65" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką: Apmokestinamas </p>
                <p>
Atsiskaitymas pagal faktines išlaidas:<strong> Nėra</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: Apmokestinama </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Taip </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Taip </p>
            </td>
            <td width="75" valign="top">
                <p>
Visas projektas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neapmokestinama</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="65" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką:<strong>Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines išlaidas:<strong> Nėra</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: Apmokestinama </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Taip </p>
            </td>
            <td width="78" valign="top">
                <p>
Taip </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Visas projektas </p>
            </td>
            <td width="65" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="70" valign="top">
                <p>
Apmokestinama </p>
            </td>
            <td width="65" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką: Apmokestinamas </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: Apmokestinamas </p>
                <p>
Atsiskaitymas pagal faktinę medžiagą: <strong> Nėra</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Taip </p>
            </td>
            <td width="78" valign="top">
                <p>
Taip </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Visas projektas </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Neapmokestinama</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Neapmokestinama</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Negalima nustatyti </p>
            </td>
            <td width="350" valign="top">
                <p>
Atsiskaitymas pagal faktinį laiką:<strong>Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines išlaidas:<strong> Neapmokestinamas</strong>
                </p>
                <p>
Atsiskaitymas pagal faktinę medžiagą:<strong> Nėra</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
