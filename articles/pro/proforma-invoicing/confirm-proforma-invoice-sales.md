---
title: „Proforma“ sąskaitos faktūros patvirtinimas – „Lite“ versija
description: Šioje temoje pateikta informacija, kaip patvirtinti išankstines sąskaitas faktūras programoje „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176531"
---
# <a name="confirm-a-proforma-invoice---lite"></a>„Proforma“ sąskaitos faktūros patvirtinimas – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_


Patvirtinus išankstinę sąskaitą faktūrą, projekto sąskaitos faktūros būsena atnaujinama į **Patvirtinta**. Patvirtinus sąskaitą faktūrą, ji tampa tik skaitoma. Ateityje sąskaitą faktūrą galima pataisyti tik tuo atveju, jei yra klientų inicijuotų pataisymų ar kreditų arba jei sąskaita faktūra pažymėta kaip apmokėta.

Šioje lentelėje išvardyti sistemos sukurtos faktiniai duomenys. Šie faktiniai duomenys kuriami tuo metu, kai prieš patvirtinant atliekamos tam tikros operacijos projekto sąskaitos faktūros juodraštyje.

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
Avansinio arba išankstinio apmokėjimo sąskaita faktūra </p>
            </td>
            <td width="408" valign="top">
                <p>
Tipo <strong>Išankstinis apmokėjimas</strong> faktinės pardavimo sumos, už kurias išrašyta sąskaita faktūra, sukuriamos kaip avansinio arba išankstinio apmokėjimo sumos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Neapmokestinamo faktinio pardavimo neigiama išankstinio arba avansinio apmokėjimo suma, kuri bus naudojama derinant.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Visiškai suderinus išankstinį arba avansinį apmokėjimą sąskaitoje faktūroje.
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
Pardavimo faktinė suma, už kurią sąskaita faktūra išrašyta, šioje sąskaitoje faktūroje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Dalinai suderinus išankstinį arba avansinį apmokėjimą sąskaitoje faktūroje.
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
Pardavimo faktinė suma, už kurią sąskaita faktūra išrašyta, šioje sąskaitoje faktūroje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Neapmokestinta faktinė likusio išankstinio arba avansinio apmokėjimo pardavimo neigiama suma, kuri bus naudojama būsimose sąskaitose faktūrose.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Laiko operacijos sąskaitos faktūros išrašymas neredaguojant sąskaitos faktūros juodraščio.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Apmokestintos faktinės pardavimo valandos ir suma pradiniame laiko patvirtinime.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Sąskaitos faktūros išrašymas už laiko operaciją, redaguotą norint sumažinti kiekį.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusias valandas bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Sąskaitos faktūros išrašymas už laiko operaciją, redaguotą norint padidinti kiekį.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Išlaidų operacijos sąskaitos faktūros išrašymas neredaguojant sąskaitos faktūros juodraščio.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Apmokestina faktinis pardavimo kiekis ir suma pradiniame išlaidų patvirtinime </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Sąskaitos faktūros išrašymas už išlaidų operaciją, redaguotą norint sumažinti kiekį.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusį kiekį bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Sąskaitos faktūros išrašymas už išlaidų operaciją, redaguotą norint padidinti kiekį.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Sąskaitos faktūros išrašymo už mokestį.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pradinės žurnalo eilutės neapmokestinto pardavimo anuliavimo sąskaitos faktūros mokesčio suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Apmokestinti faktiniai pardavimo kiekis ir suma pradinėje mokesčio žurnalo eilutėje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Etapo sąskaitų faktūrų išrašymas.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Projekto sutarties eilutės pradinio etapo apmokestinta faktinė pardavimo suma.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Produktais pagrįstos sutarties eilutės sąskaitos faktūros išrašymas.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Produkto eilutės apmokestintas faktinis pardavimo kiekis ir suma, nuskaityti iš produktais pagrįstos sutarties eilutės.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]