---
title: Projektu pagrįstų pasiūlymo eilučių apžvalga – „Lite“ versija
description: Šioje temoje pateikiama informacija apie projektu pagrįstų pasiūlymo eilučių naudojimą projektiniam darbui. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181102"
---
# <a name="project-based-quote-lines-overview---lite"></a>Projektu pagrįstų pasiūlymo eilučių apžvalga – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

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
| Pavadinimas / vardas, pavardė | Pasiūlymo eilutės pavadinimas, kuris turėtų padėti nustatyti atskirą vertinamo pasiūlymo komponentą. | Nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šios pasiūlymo eilutės laimėjus pasiūlymą. |
| Atsiskaitymo metodas | Pasiūlyme, sukurtame iš galimybės, ši vertė nukopijuojama iš atitinkamo galimybių eilutės lauko. Šiame lauke yra du pagrindiniai sutarčių sudarymo modeliai, palaikomi „Dynamics 365 Project Operations":</br>- Fiksuota kaina</br>- Laikas ir medžiaga.| Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą. |
| Project | Naudokite šį pasirinktinį lauką, kad nustatytumėte projektą, kuris bus naudojamas šiam įsipareigojimui vykdyti. Kai projektas susiejamas su pasiūlymo eilute, jis padeda nustatyti apmokestinamąsias užduotis ir su projektu pagrįstu vertinimu pateikti pasiūlymo eilutę kaip pasiūlymo eilutės išsamią informaciją. Kai projektas nesusietas su projektu pagrįsta pasiūlymo eilute, įvertis turėtų būti kuriamas rankiniu būdu sukūrus kiekvienos pasiūlymo eilutės išsamią informaciją. | Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.|
| Įtrauktos užduotys | Nurodo, ar ši pasiūlymo eilutė naudojama visoms ar kai kurioms pasirinkto projekto užduotims. Šis laukas gali turėti tokias reikšmes:</br>- Visos projekto užduotys</br>- Tik pasirinktos projekto užduotys</br>Tuščia šio lauko reikšmė yra lygiavertė parinkčiai **Visos projekto užduotys**. | Kai pasirinkta **Tik pasirinktos projekto užduotys**, projekto puslapio skirtuke **Užduočių atsiskaitymo sąranka** galite pasirinkti konkrečias užduotis ir susieti jas su šia pasiūlymo eilute. Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą. |
| Įtraukti laiką | **Taip**/**Ne** vėliavėlė nurodo, ar pasirinkto projekto laiko operacijos arba darbo išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą. **Ne** vertė nurodo, kad laiko operacijos arba darbo sąnaudos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą. **Taip** vertė nurodo, kad laiko operacijos arba darbo sąnaudos bus įtrauktos į šio pasiūlymo eilutės įvertinimą. | Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą. |
| Įtraukti išlaidas | **Taip**/**Ne** vėliavėlė nurodo, ar pasirinkto projekto išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą. **Ne** vertė nurodo, kad išlaidos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą. **Taip** vertė nurodo, kad išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą. | Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą. |
| Įtraukti mokestį | **Taip**/**Ne** vėliavėlė nurodo, ar pasirinkto projekto mokesčiai bus įtraukti į šio pasiūlymo eilutės įvertinimą. **Ne** vertė nurodo, kad mokesčiai nebus įtraukti į šio pasiūlymo eilutės įvertinimą. **Taip** vertė nurodo, kad mokesčiai bus įtraukti į šio pasiūlymo eilutės įvertinimą. | Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą. |
| Pasiūlyta suma | Tai yra suma, kuri bus pasiūlyta klientui už visus šio projektu pagrįsto pasiūlymo eilutės numatytus darbus. Pasiūlyme, sukurtame iš galimybės, ši vertė nukopijuojama iš galimybių eilutės lauko **Kliento biudžetas**. Kai projektu pagrįsto pasiūlymo eilutėje yra eilutės informacija, šis laukas užrakintas (jo redaguoti negalima) ir yra apibendrintas pagal sumą, esančią pasiūlymo eilutės informacijoje. | Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą. |
| Įvertintas mokestis | Tai yra redaguojamas vartotojo laukas, į kurį reikia įtraukti numatomą mokesčio sumą, nurodytą pasiūlymo eilutėje. Kai projektu pagrįsto pasiūlymo eilutėje yra eilutės informacija, šis laukas užrakintas (jo redaguoti negalima) ir yra apibendrintas pagal mokesčio sumą, esančią pasiūlymo eilutės informacijoje. | Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą. |
| Pasiūlyta suma išskaičius mokestį | Šis laukas yra pasiūlymo eilutės suma išskaičius mokesčius; jį galima tik skaityti. Šio lauko suma apskaičiuojama kaip *Pasiūlyta suma + mokestis*. | Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą. |
| Limitas, kurio negalima viršyti | Šį lauką galima redaguoti ir jis yra tik projektu pagrįsto pasiūlymo eilutėse, kuriose yra atsiskaitymo būdas **Laikas ir medžiagos**. | Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą. |
| Kliento biudžetas | Šį lauką galima redaguoti ir jis nukopijuojamas iš atitinkamo galimybių eilutės lauko, jei pasiūlymas buvo sukurtas iš galimybės. | Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Su projektu pagrįstų pasiūlymo eilučių skirtuke Bendra laukų tikrinimo taisyklės

**1 taisyklė**: jei laukas **Įtrauktos užduotys** yra tuščias arba jei jis nustatytas kaip **Visos projekto užduotys**, projektas įtraukiamas į pasiūlymo eilutę.

**2 taisyklė**: jei laukas **Įtrauktos užduotys** yra tuščias arba jei jis nustatytas kaip **Visos projekto užduotys**, į vieną pasiūlymo projektu pagrįsto pasiūlymo eilutę galima įtraukti tik projektą ir tam tikros klasės operacijas.

**3 taisyklė**: jei laukas **Įtrauktos užduotys** nustatytas kaip **Tik pasirinktos projekto užduotys**, į kelias pasiūlymo projektu pagrįsto pasiūlymo eilutes galima įtraukti projektą ir tam tikros klasės operacijas.

**4 taisyklė**: jei galimybė turi kelis pasiūlymus, gali būti pasiūlymo eilučių iš skirtingų pasiūlymų, kurie visi nurodo tą patį projektą ir įtraukia tą pačią operacijos klasę.

**5 taisyklė**: jei pasiūlymai nepriklauso tai pačiai galimybei, jie negali apimti to paties projekto ir operacijos klasės.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Galimybė</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Pasiūlymas</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Pasiūlymo eilutė</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="90" valign="top">
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
                    <strong>Įterpti</strong>
                </p>
                <p>
                    <strong>Rinkliava</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Galioja / negalioja</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Priežastis</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Negalioja </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
2 taisyklės pažeidimas. Laikas, išlaidos ir mokesčiai už P1 projektą įtraukiami į pasiūlymo eilutes – QL1 ir QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Negalioja </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
2 taisyklės pažeidimas. Laikas ir mokesčiai už P1 projektą įtraukiami į pasiūlymo eilutes – QL1 ir QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Tinkama </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
P1 projekto laikas ir mokesčiai yra įtraukti į QL1.
P1 projekto išlaidos yra įtrauktos į QL2.
Nepersidengia tai, kas įtraukta į kiekvieną pasiūlymo eilutę, todėl ji galioja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Negalioja </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Aukščiau pateiktos 2 taisyklės pažeidimas </p>
                <p>
Q1 apima laiką, išlaidas ir mokesčius P1 projekto antriniame užduočių rinkinyje.
                </p>
                <p>
QL2 apima laiką, išlaidas ir mokesčius už visą projektą P1 ir sutampa su tuo, kas įtraukta į pirmąjį ketvirtį.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
            <td width="54" rowspan="2" valign="top">
                <p>
Tinkama </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pagal pirmiau nurodytą taisyklę nr. 3 </p>
                <p>
Q1 apima laiką, išlaidas ir mokesčius P1 projekto antriniame užduočių rinkinyje.
                </p>
                <p>
QL2 apima P1 projekto antrinio užduočių rinkinio laiką, išlaidas ir mokesčius.
                </p>
                <p>
Vienintelis papildomas tikrinimas yra apie QL1 užduočių antrinį rinkinį, kuris skiriasi nuo QL2 užduočių antrinio rinkinio. Taip užtikrina persidengimų nebūvimą. Tai atlieka sistema, kai užduotys yra susietos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Visos projekto užduotys arba tuščias laukas </p>
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
            <td width="54" valign="top">
                <p>
Tinkama </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Remiantis taisykle Nr. 5, Q1 ir Q2 yra du tos pačios galimybės pasiūlymai, todėl jie abu gali įvertinti tuos pačius projekto komponentus.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
2 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Visos projekto užduotys arba tuščias laukas </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Visos projekto užduotys arba tuščias laukas </p>
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
            <td width="54" valign="top">
                <p>
Tinkama </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Remiantis taisykle Nr. 4, Q1 ir Q2 yra du skirtingų galimybių pasiūlymai, todėl jie abu negali įvertinti tų pačių to paties projekto komponentų.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
1 KETV. </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="90" valign="top">
                <p>
Visos projekto užduotys arba tuščias laukas </p>
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
            <td width="54" valign="top">
                <p>
Negalioja </p>
            </td>
        </tr>
    </tbody>
</table>

