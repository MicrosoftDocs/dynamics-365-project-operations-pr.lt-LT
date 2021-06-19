---
title: Koreguojamosios projektu pagrįstos sąskaitos faktūros
description: Šioje temoje pateikiama informacija apie tai, kaip sukurti ir patvirtinti koreguojamąsias projektu pagrįstas sąskaitas faktūras „Project Operations“.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012281"
---
# <a name="corrective-project-based-invoices"></a>Koreguojamosios projektu pagrįstos sąskaitos faktūros

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Patvirtintą projekto sąskaitą faktūrą galima pataisyti, kad būtų apdoroti pakeitimai arba kreditai, dėl kurių susitarta su klientu ir projekto vadovu.

Norėdami redaguoti patvirtintą sąskaitą faktūrą, atidarykite patvirtintą sąskaitą faktūrą ir pasirinkite **Taisyti šią sąskaitą faktūrą**. 

> [!NOTE]
> Šį pasirinkimą galima atlikti tik tada, jei projekto sąskaita faktūra yra patvirtinta arba projektu pagrįstoje sąskaitoje faktūroje yra nurodyti avansai arba išankstiniai apmokėjimai ar avansų arba išankstinių apmokėjimų suderinimai.

Iš patvirtintos sąskaitos faktūros sukuriama naujas sąskaitos faktūros juodraštis. Visa sąskaitos faktūros eilučių informacija iš anksčiau patvirtintos sąskaitos faktūros kopijuojama į naują juodraštį. Toliau pateikiami keli svarbiausi dalykai, kuriuos reikia suprasti apie naujai pataisytos sąskaitos faktūros eilučių informaciją.

- Visi kiekiai yra atnaujinti į nulį. „Dynamics 365 Project Operations“ reiškia, kad bus sukurtos visos prekės, kurioms išrašyta sąskaita faktūra. Jei reikia, galite neautomatiškai atnaujinti šiuos kiekius, kad nurodytumėte kiekį, už kurį išrašyta sąskaita faktūra, įskaitomą kiekį. Atsižvelgiant į įvestą kiekį, programa apskaičiuoja įskaitytą kiekį. Šią sumą atspindi faktiniai duomenys, sukurti patvirtinus pataisytą sąskaitą faktūrą. Jei norite pakeisti mokesčio sumą, turite įvesti teisingą mokesčio sumą, o ne mokesčio sumą, kuri yra įskaitoma.
- Etapų pataisymai visada apdorojami kaip visapusiški įskaitymai.


> [!IMPORTANT]
> Kai sąskaitos faktūros eilutės išsami informacija apima kitų jau apmokėtų mokesčių korekcijas, laukas **Taisymas** nustatomas kaip **Taip**. Kai sąskaitose faktūrose pateikiama pakoreguota SF eilutės išsami informacija, laukas **Yra taisymų** nustatomas kaip **Taip**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Faktiniai duomenys, kai patvirtinta koreguojamoji sąskaita faktūra

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
Sąskaitos faktūros išrašymas už visą anksčiau į sąskaitą faktūrą įtrauktos medžiagos operacijos kreditą.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pardavimo, už kurį išrašyta sąskaita, atšaukimas pagal pradinės sąskaitos faktūros medžiagos eilutės informacijos srityje nurodytą kiekį ir sumą.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Naujas faktinis pardavimas, už kurį neišrašyta sąskaita, susijęs su pradinės sąskaitos faktūros medžiagos eilutės informacijos srityje nurodytu kiekiu ir suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Sąskaitos faktūros išrašymas už dalinį medžiagos operacijos kreditą.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pardavimo, už kurį išrašyta sąskaita, atšaukimas pagal pradinės sąskaitos faktūros medžiagos eilutės informacijos srityje nurodytą kiekį ir sumą, už kurią išrašyta sąskaita faktūra.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Naujas faktinis pardavimas, už kurį neišrašyta sąskaita, apmokestinamas pagal kiekį ir sumą, nurodytą redaguotos sąskaitos faktūros eilutės išsamios informacijos srityje, jo atšaukimas ir atitinkamas faktinis pardavimas, už kurį išrašyta sąskaita.
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
Šis scenarijus nepalaikomas.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
