---
title: Projektu pagrįstų sutarties eilučių apžvalga
description: Šiame straipsnyje pateikiama informacija apie darbą su projektu pagrįstomis sutarčių eilutėmis.
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d32edac6537a4b0f51e9d2f72cb4a7342606d2c5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931432"
---
# <a name="project-based-contract-lines-overview"></a>Projektu pagrįstų sutarties eilučių apžvalga

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projektu pagrįstos sutarčių eilutės programoje „Dynamics 365 Project Operations“ sukurtos tam tikriems projekto darbo komponentams įvertinti ir atsiskaitymo sutartims pateikti. Projektu pagrįstos sutarties eilutės struktūra išplečiama projektų sąmatų ir sąskaitų išrašymo scenarijams, taikant tolesnes koncepcijas.

- Atsiskaitymo metodas
- Projektų ir užduočių susiejimas
- Įtrauktų operacijų klasės
- Limitas, kurio negalima viršyti
- Apmokestinimo sąranka
- Sąmatos naudojant išsamią sutarties eilutės informaciją
- Sutarties eilutės klientai

Šioje lentelėje yra projektu pagrįstų sutarčių eilučių skirtukas **Bendra**, kurio laukai padeda nustatyti detaliojo, visapusiško projektinio darbo sąmatų ir sąskaitų išrašymo tvarką.

| Laukas | Aprašo | Tolesnis poveikis |
| --- | --- | --- |
| **Pavadinimas** | Sutarties eilutės pavadinimas. Taip nustatomas atskiras sutarties komponentas, kuris yra vertinamas. Vykdant projekto sutartį, sukurtą pagal pasiūlymą, ši reikšmė kopijuojama iš atitinkamos projektu pagrįstos pasiūlymo eilutės reikšmės. | Pavadinimas, nukopijuotas į projekto sąskaitos faktūros eilutę, sukurtą pagal šią sutarties eilutę sukūrus sąskaitą faktūrą. |
| **Atsiskaitymo metodas** | Vykdant projekto sutartį, sukurtą pagal pasiūlymą, ši reikšmė kopijuojama iš atitinkamo lauko pasiūlymo eilutėje. Tai parinkčių rinkinys, vaizduojantis du pagrindinius sutarčių modelius, kuriuos palaiko „Project Operations“.</br>- **Fiksuota kaina**</br>- **Laikas ir medžiagos** | Pagal nurodytos sutarties eilutės atsiskaitymo metodą faktinė operacija bus apdorota. Jei sutarties eilutė, į kurią nurodo faktinis įrašas, turi sąskaitų už laiką ir medžiagas išrašymo būdą, kuriami išlaidų ir faktinio pardavimo be sąskaitų įrašai. Jei faktiniame įraše nurodyta sutarties eilutė turi fiksuotą kainos išrašymo metodą, sukuriami tik faktiniai kaštai. |
| **Project** | Šį lauką naudokite, jei norite nustatyti projektą, kuris bus naudojamas šiam įsipareigojimui vykdyti. | Ši reikšmė bus naudojama kartu su **įtrauktomis užduotimis** ir **įtrauktomis operacijos klasėmis**, kad faktinių duomenų arba įvertinimo eilutės įraše būtų nustatyta sutarties eilutės nuoroda. |
| **Įtrauktos užduotys** | Nurodo, ar šioje sutarties eilutėje yra visos pasirinkto projekto užduotys, ar tik rinkinio užduočių pogrupis. Tai yra parinkčių rinkinys, galintis apimti toliau nurodytas reikšmes.</br>- **Visos projekto užduotys**</br>- **Tik pasirinktos projekto užduotys**. Tuščia šio lauko reikšmė yra lygi **visų projekto užduočių** pasirinkimui. | Jei pasirenkama **Tik pasirinktos užduotys**, galite pažymėti specifines užduotis ir susieti jas su šia sutarties eilute puslapio **Projektas** skirtuke **Sąskaitų išrašymo sąranka**. Ši reikšmė bus naudojama kartu su klasėmis **Projektas** ir **Įtraukta operacija**, kad būtų išspręsta sutarties eilutės nuoroda faktiniame arba įvertintame eilutės įraše. |
| **Įtraukti laiką** | Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto laiko operacijos arba darbo savikainos bus įtrauktos į sutarties eilutę. Reikšmė **Ne** nurodo, kad šioje sutarties eilutėje nebus įtrauktos laiko operacijos ar darbo išlaidos. Reikšmė **Taip** nurodo, kad jos bus įtrauktos. | Ši reikšmė naudojama kartu su projektu, kad faktinių duomenų arba įvertinimo eilutės įraše būtų nustatyta sutarties eilutės nuoroda. |
| **Įtraukti išlaidas** | Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto išlaidos savikainos bus įtrauktos į sutarties eilutę. Reikšmė **Ne** nurodo, kad šioje sutarties eilutėje išlaidų kaštai nebus įtraukti. Reikšmė **Taip** nurodo, kad tai bus įtraukta. | Ši reikšmė naudojama kartu su projektu, kad faktinių duomenų arba įvertinimo eilutės įraše būtų nustatyta sutarties eilutės nuoroda. |
| **Įtraukti medžiagas** | Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto medžiagos savikainos bus įtrauktos į sutarties eilutę. Reikšme **Ne** nurodoma, kad medžiagos savikainos nebus įtrauktos į sutarties eilutę. Reikšmė **Taip** nurodo, kad tai bus įtraukta. | Ši reikšmė naudojama kartu su projektu, kad faktinių duomenų arba įvertinimo eilutės įraše būtų nustatyta sutarties eilutės nuoroda. |
| **Įtraukti mokestį** | Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto mokesčiai bus įtraukti į sutarties eilutę. Reikšmė **Ne** nurodo, kad šioje sutarties eilutėje mokesčiai nebus įtraukti. Reikšmė **Taip** nurodo, kad jos bus įtrauktos. | Ši reikšmė naudojama kartu su projektu, kad faktinių duomenų arba įvertinimo eilutės įraše būtų nustatyta sutarties eilutės nuoroda. |
| **Sutarties suma** | Fiksuotos kainos sutarties eilutėje ši suma yra sutarta reikšmė, kuri bus išrašyta klientui už visus su šia sutarties eilute susietus darbo komponentus. Laiko ir medžiagų sutarties eilutėje ši suma yra įvertinta reikšmė, kuri bus išrašyta klientui už visus su šia sutarties eilute susietus darbo komponentus. Vykdant projekto sutartį, kuri sukurta pagal pasiūlymą, ši reikšmė kopijuojama iš atitinkamo lauko pasiūlymo eilutėje. Kai projektu pagrįstoje sutarties eilutėje pateikiama eilutės informacija, šio lauko neleidžiama redaguoti ir jis apibendrinamas iš sumos, nurodytos sutarties eilutės informacijoje. | Kai sutarties eilutėje yra eilutės informacija, šią reikšmę galima modifikuoti keičiant eilutės išsamios informacijos sumas. Fiksuotos kainos sutarties eilutėje ši reikšmė naudojama sumai iki mokesčių generuoti periodinio atsiskaitymo etapuose. |
| **Įvertintas mokestis** | Vartotojas gali redaguoti šį lauką ir įvesti numatomą mokesčio sumą sutarties eilutėje. Kai projektu pagrįstoje sutarties eilutėje pateikiama eilutės informacija, šio lauko neleidžiama redaguoti ir jis apibendrinamas iš mokesčių sumos, nurodytos sutarties eilutės informacijoje. | Kai sutarties eilutėje yra eilutės informacija, šią reikšmę galima modifikuoti keičiant eilutės išsamios informacijos mokesčių sumas. Fiksuotos kainos sutarties eilutėje ši reikšmė naudojama mokesčiams generuoti periodinio atsiskaitymo etapuose. |
| **Sutarties suma po mokesčių** | Sutarties eilutės suma po mokesčių. Šis laukas yra tik skaitomas ir apskaičiuojamas kaip **sutarties suma + mokesčiai**. | Fiksuotos kainos sutarties eilutėje ši reikšmė naudojama periodinio atsiskaitymo etapams generuoti. |
| **Limitas, kurio negalima viršyti** | Vartotojas gali redaguoti šį lauką ir jis yra prieinamas tik projektu pagrįstose sutarties eilutėse, kurių atsiskaitymo metodas nustatytas kaip laikas ir medžiagos. | Vartotojas gali redaguoti šį lauką. Kai faktinis laiko ir medžiagų įrašas nurodo šią laiko ir medžiagų sutarties eilutę, faktinio įrašo sumos dydis įvertinamas pagal sutarties eilutės neviršijamą ribą. Šis vertinimas baigiamas po to, kai už jau panaudotas ir paskirtas sumas atsiskaitoma. |
| **Kliento biudžetas** | Šį lauką galima redaguoti ir jis nukopijuojamas iš atitinkamo lauko pasiūlymo eilutėje, jei sutartis buvo sukurta pagal pasiūlymą. | Šis laukas naudojamas tik informacijai ir neturi jokios reikšmės tolesnėms operacijoms. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Projektu pagrįstų sutarčių eilučių skirtuke Bendra pateiktos parinkčių tikrinimo taisyklės

1 taisyklė: jei laukas **Įtrauktos užduotys** yra tuščias arba nustatytas kaip **Visos projekto užduotys**, visos projekto užduotys įtraukiamos į sutarties eilutę.

2 taisyklė: kai laukas **Įtrauktos užduotys** yra tuščias arba aiškiai nustatytas kaip **Visos projekto užduotys**, projektas ir tam tikra operacijų klasė gali būti įtraukti tik į vieną projektu pagrįstą sutarties eilutę.

3 taisyklė: kai laukas **Įtrauktos užduotys** yra nustatytas kaip **Tik pasirinktos projekto užduotys**, projektas ir tam tikra operacijų klasė gali būti įtraukti į kelias projektu pagrįstas sutarties eilutes.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Sutartis</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Sutarties eilutė</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Įtrauktos užduotys</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Įtraukti laiką</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Įtraukti išlaidas</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Įtraukti medžiagas</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Įtraukti</strong>
                </p>
                <p>
                    <strong>Rinkliava</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Galioja / negalioja</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Priežastis</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Negalioja </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
2 taisyklės pažeidimas. P1 projekto laikas, išlaidos, medžiagos ir mokesčiai įtraukiami ir abi sutarties eilutes CL1 ir CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Negalioja </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
2 taisyklės pažeidimas. P1 projekto laikas, medžiagos ir mokesčiai įtraukiami ir abi sutarties eilutes CL1 ir CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Tinkama </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
P1 projekto laikas, medžiagos ir mokesčiai įtraukiami į CL1.
                </p>
                <ul>
                    <li>
P1 projekto išlaidos yra įtrauktos į CL2.
                    </li>
                </ul>
                <p>
Tarp įtraukiamų į kiekvieną sutarties eilutę duomenų persidengimo nėra, todėl jie yra tinkami.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Negalioja </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
2 taisyklės pažeidimas </p>
                <p>
C1 apima P1 projekto antrinio užduočių rinkinio laiką, medžiagas, išlaidas ir mokesčius.
                </p>
                <p>
CL2 apima viso P1 projekto laiką, medžiagas, išlaidas ir mokesčius, todėl persidengia su duomenimis, įtrauktais į C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Tinkama </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Pagal taisyklę Nr. 3 </p>
                <p>
C1 apima P1 projekto antrinio užduočių rinkinio laiką, išlaidas, medžiagas ir mokesčius.
                </p>
                <p>
CL2 apima rinkinio laiką, išlaidas, medžiagas ir mokesčius, skirtus P1 projekto antriniam užduočių rinkiniui.
                </p>
                <p>
Vienintelis papildomas tikrinimas atliekamas apie CL1 antrinį užduočių rinkinį ir skiriasi nuo CL2 antrinio užduočių rinkinio, siekiant užtikrinti, kad jame nebus persidengimų. Tai atlieka sistema, kai užduotys yra susietos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="48" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
            <td width="42" valign="top">
                <p>
Taip </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
