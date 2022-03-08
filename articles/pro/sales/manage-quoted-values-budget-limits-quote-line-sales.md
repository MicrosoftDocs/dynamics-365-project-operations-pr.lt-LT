---
title: Projektu pagrįstų pasiūlymo eilučių apžvalga
description: Šioje temoje pateikiama informacija apie projektu pagrįstų pasiūlymo eilučių naudojimą projektiniam darbui.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369881"
---
# <a name="project-based-quote-lines-overview"></a>Projektu pagrįstų pasiūlymo eilučių apžvalga 

_**Taikoma (kam):** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projektu pagrįstos pasiūlymo eilutės yra skirtos padėti įvertinti projekto darbą. Projektu pagrįstos pasiūlymo eilutės struktūra yra pratęsta projekto sąmatoms pagal šias sąvokas:

- Atsiskaitymo metodas
- Projektų ir užduočių susiejimas
- Įtrauktų operacijų klasės
- Limitas, kurio negalima viršyti
- Apmokestinimo sąranka
- Vertinimas pagal pasiūlymo eilutės išsamią informaciją
- Pasiūlymo eilutės klientai

Šioje lentelėje pateikiama informacija apie laukus, esančius projektu pagrįsto pasiūlymo eilutės skirtuke **Bendroji informacija**. Šie laukai padeda nustatyti išsamaus projekto darbo įvertinimo pagrindą.

| **Laukas** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- |
| Pavadinimas / vardas ir pavardė | Pasiūlymo eilutės pavadinimas, padedantis nustatyti diskretišką vertinamo pasiūlymo komponentą. | Nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šios pasiūlymo eilutės laimėjus pasiūlymą. |
| Atsiskaitymo metodas | Pasiūlyme, sukurtame iš galimybės, ši vertė nukopijuojama iš atitinkamo galimybių eilutės lauko. Į šį lauką įtraukti du pagrindiniai sutarties modeliai, kuriuos palaiko „Dynamics 365 Project Operations“:</br>- Fiksuota kaina</br>- Laikas ir medžiaga.| Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |
| Project | Naudokite šį pasirinktinį lauką, kad nustatytumėte projektą, kuris bus naudojamas šiam įsipareigojimui vykdyti. Kai projektas susiejamas su pasiūlymo eilute, jis padeda nustatyti apmokestinamąsias užduotis ir su projektu pagrįstu vertinimu pateikti pasiūlymo eilutę kaip pasiūlymo eilutės išsamią informaciją. Kai projektas nesusietas su projektu pagrįsta pasiūlymo eilute, įvertis turėtų būti kuriamas rankiniu būdu sukūrus kiekvienos pasiūlymo eilutės išsamią informaciją. | Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.|
| Įtrauktos užduotys | Nurodo, ar ši pasiūlymo eilutė naudojama visoms ar kai kurioms pasirinkto projekto užduotims. Šis laukas gali turėti tokias reikšmes:</br>- Visos projekto užduotys</br>- Tik pasirinktos projekto užduotys</br>Tuščia šio lauko reikšmė yra lygiavertė parinkčiai **Visos projekto užduotys**. | Kai projekto puslapyje pasirinkta **Tik pasirinktos projekto užduotys**, skirtuke **Užduočių atsiskaitymo sąranka** galima pasirinkti konkrečias užduotis ir susieti jas su pasiūlymo eilute. Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |
| Įtraukti laiką | Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto laiko operacijos arba darbo savikainos bus įtrauktos į šio pasiūlymo eilutės įvertinimą. **Ne** vertė nurodo, kad laiko operacijos arba darbo sąnaudos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą. **Taip** vertė nurodo, kad laiko operacijos arba darbo sąnaudos bus įtrauktos į šio pasiūlymo eilutės įvertinimą. | Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |
| Įtraukti išlaidas | Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto išlaidos savikainos bus įtrauktos į šio pasiūlymo eilutės įvertinimą. **Ne** vertė nurodo, kad išlaidos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą. **Taip** vertė nurodo, kad išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą. | Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |
| Įtraukti medžiagą | Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto medžiagos savikainos bus įtrauktos į šio pasiūlymo eilutės įvertinimą. Reikšme **Ne** nurodoma, kad medžiagos savikainos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą. Reikšme **Taip** nurodoma, kad medžiagos savikainos bus įtrauktos į šio pasiūlymo eilutės įvertinimą. | Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |
| Įtraukti mokestį | Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto mokesčiai bus įtraukti į šio pasiūlymo eilutės įvertinimą. Reikšme **Ne** nurodoma, kad mokesčiai nebus įtraukti į šio pasiūlymo eilutės įvertinimą. Reikšme **Taip** nurodoma, kad mokesčiai bus įtraukti į šio pasiūlymo eilutės įvertinimą. | Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |
| Pasiūlyta suma | Tai suma, kuri bus pasiūlyta pirkėjui už visą prognozuojamą darbą šioje projektu pagrįstoje pasiūlymo eilutėje. Pasiūlyme, sukurtame iš galimybės, ši vertė nukopijuojama iš galimybių eilutės lauko **Kliento biudžetas**. Kai projektu pagrįsto pasiūlymo eilutėje yra eilutės informacija, šis laukas užrakintas (jo redaguoti negalima) ir yra apibendrintas pagal sumą, esančią pasiūlymo eilutės informacijoje. | Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |
| Įvertintas mokestis | Tai yra redaguojamas vartotojo laukas, į kurį reikia įtraukti numatomą mokesčio sumą, nurodytą pasiūlymo eilutėje. Kai projektu pagrįsto pasiūlymo eilutėje yra eilutės informacija, šis laukas užrakintas (jo redaguoti negalima) ir yra apibendrintas pagal mokesčio sumą, esančią pasiūlymo eilutės informacijoje. | Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |
| Pasiūlyta suma išskaičius mokestį | Šis laukas yra pasiūlymo eilutės suma išskaičius mokesčius; jį galima tik skaityti. Šio lauko suma apskaičiuojama kaip *Pasiūlyta suma + mokestis*. | Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |
| Limitas, kurio negalima viršyti | Šį lauką galima redaguoti ir jis yra tik projektu pagrįsto pasiūlymo eilutėse, kuriose yra atsiskaitymo būdas **Laikas ir medžiagos**. | Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |
| Kliento biudžetas | Šį lauką galima redaguoti ir jis nukopijuojamas iš atitinkamo galimybių eilutės lauko, jei pasiūlymas buvo sukurtas iš galimybės. | Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Su projektu pagrįstų pasiūlymo eilučių skirtuke Bendra laukų tikrinimo taisyklės

**1 taisyklė**: jei laukas **Įtrauktos užduotys** yra tuščias arba jei jis nustatytas kaip **Visos projekto užduotys**, projektas įtraukiamas į pasiūlymo eilutę.

**2 taisyklė**: jei laukas **Įtrauktos užduotys** yra tuščias arba jei jis nustatytas kaip **Visos projekto užduotys**, į vieną pasiūlymo projektu pagrįsto pasiūlymo eilutę galima įtraukti tik projektą ir tam tikros klasės operacijas.

**3 taisyklė**: jei laukas **Įtrauktos užduotys** nustatytas kaip **Tik pasirinktos projekto užduotys**, į kelias pasiūlymo projektu pagrįsto pasiūlymo eilutes galima įtraukti projektą ir tam tikros klasės operacijas.

**4 taisyklė**: jei galimybė turi kelis pasiūlymus, gali būti pasiūlymo eilučių iš skirtingų pasiūlymų, kurie visi nurodo tą patį projektą ir įtraukia tą pačią operacijos klasę.

**5 taisyklė**: jei pasiūlymai nepriklauso tai pačiai galimybei, jie negali apimti to paties projekto ir operacijos klasės.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Galimybė</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Pasiūlymas</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Pasiūlymo eilutė</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Įtrauktos užduotys</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Įtraukti laiką</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Įtraukti išlaidas</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Įtraukti medžiagą</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Įtraukti</strong>
                </p>
                <p>
                    <strong>Rinkliava</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Galioja / negalioja</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Priežastis</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Negalioja </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
2 taisyklės pažeidimas. Laikas, išlaidos ir mokesčiai už P1 projektą įtraukiami į pasiūlymo eilutes – QL1 ir QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Negalioja </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
2 taisyklės pažeidimas. Laikas, medžiagos, išlaidos ir mokesčiai už P1 projektą įtraukiami į pasiūlymo eilutes – QL1 ir QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Tinkama </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
P1 projekto laikas, medžiagos ir mokesčiai įtraukiami į QL1 <br>
P1 projekto išlaidos yra įtrauktos į QL2 <br>
Tarp įtraukiamų į kiekvieną pasiūlymo eilutę duomenų persidengimo nėra, todėl jie yra tinkami.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Negalioja </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
2 taisyklės pažeidimas </p>
                <p>
Q1 apima P1 projekto antrinio užduočių rinkinio laiką, medžiagą, išlaidas ir mokesčius </p>
                <p>
QL2 apima laiką, išlaidas ir mokesčius už visą P1 projektą, todėl persidengia su tuo, kas įtraukta į Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tuščias </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Tinkama </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Pagal taisyklę Nr. 3, </p>
                <p>
Q1 apima P1 projekto antrinio užduočių rinkinio laiką, medžiagą, išlaidas ir mokesčius.
                </p>
                <p>
QL2 apima rinkinio laiką, medžiagą, išlaidas, medžiagas ir mokesčius, skirtus P1 projekto antriniam užduočių rinkiniui.
                </p>
                <p>
Vienintelis papildomas tikrinimas atliekamas apie QL1 antrinį užduočių rinkinį, kuris skiriasi nuo QL2 antrinio užduočių rinkinio, siekiant užtikrinti, kad jame nebus persidengimo. Tai atlieka sistema, kai užduotys yra susietos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tik pasirinktos užduotys </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Visos projekto užduotys arba tuščias laukas </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Tinkama </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Pagal 5 taisyklę, Q1 ir Q2 yra du tos pačios galimybės pasiūlymai, todėl juos abu galima taikyti vertinant tuos pačius projekto komponentus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
2 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Visos projekto užduotys arba tuščias laukas </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Visos projekto užduotys arba tuščias laukas </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Negalioja </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Pagal 4 taisyklę, Q1 ir Q2 yra du skirtingų galimybių pasiūlymai, todėl jų negalima taikyti vertinant tuos pačius to paties projekto komponentus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Visos projekto užduotys arba tuščias laukas </p>
            </td>
            <td width="45" valign="top">
                <p>
Taip </p>
            </td>
            <td width="46" valign="top">
                <p>
Taip </p>
            </td>
            <td width="43" valign="top">
                <p>
Taip </p>
            </td>
            <td width="41" valign="top">
                <p>
Taip </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
