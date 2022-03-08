---
title: Projektu pagrįstos sutarties eilutės apmokestinamų komponentų konfigūravimas
description: Šioje temoje pateikta informacija apie tai, kaip įtraukti apmokestinamus komponentus į sutarties eilutes naudojant „Project Operations“.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d18e56f29457151e07636b67ff8d9b184bf5014ef0ceeef9bb9d322672be4335
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003466"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Projektu pagrįstos sutarties eilutės apmokestinamų komponentų konfigūravimas

_**Taikoma (kam):** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Į projektais pagrįstą sutarties eilutę *įtraukti* komponentai ir *apmokestinami* komponentai.

Įtrauktiems komponentams taikomos toliau nurodytos sąlygos.

  - Sąskaitų išrašymo būdo ir klientų išskaidymas
  - Limitas, kurio negalima viršyti 
  - Sąskaitos faktūros dažnio parametrai, apibrėžti projektais pagrįstoje sutarties eilutėje

Įtrauktų komponentų pogrupis gali būti pažymėtas kaip apmokestinamas naudojant lauką **Atsiskaitymo tipas**. Laukas **Atsiskaitymo tipas** yra parinkčių rinkinys, leidžiantis toliau nurodytas reikšmes sutarties eilutės kontekste.

  - Apmokestinama
  - Neapmokestinama

Apmokestinamus komponentus galima apibrėžti užduotyse, vaidmenyse ir operacijų kategorijose.

Projekto sutarties eilutės apmokestinamumas apibrėžiamas užduotyse ir taikomas visoms į eilutę įtrauktoms operacijų klasėms. Jei sutarties eilutės laukas **Įtraukti užduotis** yra tuščias arba nustatytas kaip **Visas projektas**, skirtukas **Apmokestinamos užduotys** nebus pateiktas.

Projekto sutarties eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei. Jei sutarties eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinami vaidmenys** nebus pateiktas.

Projekto sutarties eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei. Jei laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinamos kategorijos** nebus pateiktas.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Projekto užduoties atnaujinimas į apmokestinamą arba neapmokestinamą

Projekto užduotis gali būti apmokestinama arba neapmokestinama konkrečioje sutarties eilutėje, todėl galima nustatyti toliau nurodytą sąranką.

Jei projekto sutarties eilutėje yra nurodyti **Laikas** ir tam tikra užduotis, **T1** su ja susieta kaip apmokestinama. Jei antroje sutarties eilutėje yra **Išlaidos**, T1 užduotį galite susieti sutarties eilutėje kaip neapmokestinamą. Todėl visas laikas, užfiksuotas užduotyje, yra apmokestinamas, o visos išlaidos – neapmokestinamos.

Užduoties sąskaitų išrašymo tipą galima sukonfigūruoti sutarties eilutės skirtuke **Apmokestinamosios užduotys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį sutarties eilutės užduočių papildomame tinklelyje. Arba galite atnaujinti lauką **Atsiskaitymo tipas**, esantį projekto, kuriame sutarties eilutės rodomos kaip susietos su užduotimi, atsiskaitymo už užduotis sąrankos papildomame tinklelyje.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą

Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečioje sutarties eilutėje.

Vaidmens atsiskaitymo tipą galima sukonfigūruoti sutarties eilutės skirtuke **Apmokestinami vaidmenys**. Norėdami tai atlikti, atnaujinkite lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamieji vaidmenys**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą

Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje sutarties eilutėje.

Operacijos atsiskaitymo tipą galima sukonfigūruoti projektais pagrįstos sutarties eilutės skirtuke **Apmokestinamos kategorijos**. Norėdami tai atlikti, atnaujinkite lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamosios kategorijos**.

### <a name="resolve-chargeability"></a>Apmokestinamumo sprendimas

Įvertinimas arba faktiniai sukurti laikui duomenys apmokestinami tik esant toliau nurodytoms sąlygoms.

   - Į sutarties eilutę įtraukta reikšmė **Laikas**.
   - Sutarties eilutėje **Vaidmuo** yra sukonfigūruotas kaip apmokestinamas.
   - Sutarties eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**.
 
 Jei šie trys punktai atitinkami, užduotis sukonfigūruojama kaip apmokestinama. 

Įvertinimas arba faktiniai sukurti išlaidoms duomenys apmokestinami tik esant toliau nurodytoms sąlygoms.

   - Į sutarties eilutę įtraukta reikšmė **Išlaidos**
   - Sutarties eilutėje **Operacijos kategorija** yra sukonfigūruota kaip apmokestinama
   - Sutarties eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinkta užduotis**
  
 Jei šie trys punktai atitinkami, **užduotis** sukonfigūruojama kaip apmokestinama. 

Įvertinimas arba faktiniai sukurti medžiagai duomenys apmokestinami tik esant toliau nurodytoms sąlygoms.

   - Į sutarties eilutę įtraukta reikšmė **Medžiagos**
   - Sutarties eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**

Jei šie du punktai atitinkami, **užduotis** sukonfigūruojama kaip apmokestinama. 

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
Atsiskaitymas pagal faktinį laiką: <strong>Apmokestinama</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: <strong>Apmokestinama</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: <strong>Apmokestinama</strong>
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
Atsiskaitymas pagal faktinį laiką: <strong>Apmokestinama</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines išlaidas: <strong>Apmokestinama</strong>
                </p>
                <p>
Atsiskaitymas pagal faktines medžiagas: <strong>Apmokestinama</strong>
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
