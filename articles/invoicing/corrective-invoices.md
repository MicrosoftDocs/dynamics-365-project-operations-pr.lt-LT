---
title: Koreguojamųjų projektu pagrįstų sąskaitų faktūrų kūrimas
description: Šioje temoje pateikiama informacija apie koreguojamąsias sąskaitas faktūras „Project Operations“.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cde82bb3c5777458a63a44a131af284e6ed5d7532de6aacbb5eb860c1fcddebd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006210"
---
# <a name="create-corrective-project-based-invoices"></a>Koreguojamųjų projektu pagrįstų sąskaitų faktūrų kūrimas 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Patvirtintą projekto sąskaitą faktūrą galima pataisyti, kad būtų apdoroti pakeitimai arba kreditai, dėl kurių susitarta su klientu ir projekto vadovu.

Norėdami redaguoti patvirtintą sąskaitą faktūrą, atidarykite patvirtintą sąskaitą faktūrą ir pasirinkite **Taisyti šią sąskaitą faktūrą**. 

> [!NOTE]
> Šis pasirinkimas nepasiekiamas, jei projekto sąskaita faktūra nepatvirtinta.

Iš patvirtintos sąskaitos faktūros sukuriama naujas sąskaitos faktūros juodraštis. Visa sąskaitos faktūros eilučių informacija iš anksčiau patvirtintos sąskaitos faktūros kopijuojama į naują juodraštį. Toliau nurodyta keletas svarbių dalykų, kad geriau suprastumėte apie išsamią eilutės informaciją naujoje koreguotoje sąskaitoje faktūroje.

- Visi kiekiai yra atnaujinti į nulį. Tai reiškia, kad bus sukurtos visos prekės, kurioms išrašyta sąskaita faktūra. Jei reikia, galite neautomatiškai atnaujinti šiuos kiekius, kad nurodytumėte kiekį, už kurį išrašyta sąskaita faktūra, įskaitomą kiekį. Atsižvelgiant į įvestą kiekį, programa apskaičiuoja įskaitytą kiekį. Šią sumą atspindi faktiniai duomenys, sukurti patvirtinus pataisytą sąskaitą faktūrą. Jei norite pakeisti mokesčio sumą, turite įvesti teisingą mokesčio sumą, o ne mokesčio sumą, kuri yra įskaitoma.
- Etapų pataisymai visada apdorojami kaip visapusiški įskaitymai.
- Išankstinio apmokėjimo arba avanso sumos gali būti pataisytos, jei klientui išrašyta sąskaita faktūra už klaidingą sumą.
- Išankstinių apmokėjimų ir avansų derinimą galima pataisyti, jei klaidinga suma buvo naudojama derinant pagal anksčiau patvirtintos sąskaitos faktūros mokesčius.

> [!IMPORTANT]
> Sąskaitos faktūros eilutės išsamioje informacijoje, apimančioje kitų jau apmokėtų mokesčių korekcijas, laukas **Taisymas** nustatomas kaip **Taip**. Sąskaitos faktūros, kurių eilučių informacija pataisyta, turi lauką **Yra pataisymų**, kuris taip pat nustatytas į parinktį **Taip**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Faktiniai duomenys sukuriami patvirtinus koreguojamąją sąskaitą faktūrą

Toliau esančioje lentelėje pateikti faktiniai duomenys, sukuriami patvirtinus koreguojamąją sąskaitą faktūrą.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenarijus</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Faktiniai duomenys, sukurti patvirtinant</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Patvirtinkite avanso arba išankstinio apmokėjimo, už kurį išrašyta sąskaita faktūra, pataisymą.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Išankstinio arba avansinio apmokėjimo pardavimo sumos, už kurią sąskaita faktūra neišrašyta, anuliavimas, sukurtas atlikti derinimą. Ši suma yra teigiama, nes ji skirta padengti neigiamą sumą, kuri sukurta išrašius sąskaitą faktūrą už išankstinį apmokėjimą arba avansą.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Pardavimo atšaukimo sąskaitos faktūros faktiniai duomenys sukuriami už išankstinio apmokėjimo arba avanso sumą, kad būtų atšauktas pradinis pardavimas, už kurį išrašyta sąskaita faktūra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Sukuriami nauji pardavimo sąskaitos faktūros duomenys pagal išankstinio apmokėjimo arba avanso pagrindu pataisytą sąskaitos faktūros eilutę.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Neapmokestinamo faktinio pardavimo neigiama išankstinio apmokėjimo arba avanso pagrindu pataisyta sąskaitos faktūros eilutė, kuri bus naudojama derinant.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Patvirtinimas apie anksčiau suderinto išankstinio apmokėjimo arba avanso pataisymą.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Išankstinio arba avansinio apmokėjimo pardavimo sumos, už kurią sąskaita faktūra neišrašyta, anuliavimas, sukurtas atlikti derinimą. Ši suma yra teigiama ir ji skirta padengti neigiamą sumą, kuri sukurta įvykdžius ankstesnį derinimą
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Pardavimo atšaukimo sąskaitos faktūros faktiniai duomenys pagal ankstesnės sąskaitos faktūros sumą.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauji pardavimo sąskaitos faktūros duomenys pagal pataisytą išankstinio apmokėjimo sumą, taikomą pataisytai sąskaita faktūrai.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Neapmokestinamo faktinio pardavimo neigiama iš pataisyto likučio išankstinio apmokėjimo arba avanso, kurį naudojant bus derinamos būsimos sąskaitos faktūros.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Viso kredito sąskaitų faktūrų išrašymas už ankstesnes laiko operacijas, kurių sąskaita faktūra išrašyta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinės laiko sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros valandos ir suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Pradinės laiko sąskaitos faktūros eilutės informacijos naujos faktinės pardavimo reikšmės, už kurią sąskaita faktūra neišrašyta, valandos ir suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Dalinio kredito už laiko operaciją išrašymas.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinės laiko sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros valandos ir suma, už kurias sąskaita faktūra išrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – šio proceso atšaukimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra apmokestinama už likusias valandas ir sumą, atėmus pakoreguotus skaičius sąskaitos faktūros eilutės informacijoje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Viso kredito sąskaitų faktūrų išrašymas už ankstesnes išlaidų operacijas, kurių sąskaita faktūra neišrašyta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinės išlaidų sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Pradinės išlaidų sąskaitos faktūros eilutės informacijos faktinės pardavimo sumos, už kurią sąskaita faktūra neišrašyta, kiekis ir suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Da;omop kredito sąskaitų faktūrų išrašymas už ankstesnes išlaidų operacijas, kurių sąskaita faktūra neišrašyta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinės išlaidų sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma, už kuriuos sąskaita faktūra išrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą pataisytoje sąskaitos faktūros eilučių informacijoje, taip pat – šio proceso atšaukimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra apmokestinama už likusius kiekį ir sumą, atėmus pakoreguotus skaičius sąskaitos faktūros eilutės informacijoje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Viso kredito sąskaitų faktūrų išrašymas už ankstesnes mokesčių operacijas, kurių sąskaita faktūra neišrašyta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinės mokesčio sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Pradinės mokesčio sąskaitos faktūros eilutės informacijos faktinės pardavimo sumos, už kurią sąskaita faktūra neišrašyta, kiekis ir suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Dalinio kredito sąskaitų faktūrų išrašymas už ankstesnes mokesčių operacijas, kurių sąskaita faktūra neišrašyta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinės mokesčio sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma, už kuriuos sąskaita faktūra išrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą pataisytoje sąskaitos faktūros eilučių informacijoje, taip pat – šio proceso atšaukimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Viso kredito sąskaitų faktūrų išrašymas už ankstesnį etapą, už kurį sąskaita faktūra išrašyta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinės etapo sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros ir suma.
                </p>
                <p>
Etapo sąskaitos faktūros būsena atnaujinta iš <b>Kliento sąskaita faktūra užregistruota</b> į <b>Parengta išrašyti sąskaitą faktūrą</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Dalinio kredito sąskaitų faktūrų išrašymas už ankstesnį etapą, už kurį sąskaita faktūra išrašyta.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nepalaikoma </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
