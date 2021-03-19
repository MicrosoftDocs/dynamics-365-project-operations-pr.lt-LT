---
title: „Proforma“ sąskaitos faktūros valdymas
description: Šioje temoje pateikiama informacija apie „Proforma“ sąskaitos faktūros valdymą ir darbą su ja.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29e301062f8f3ba955a95953bc2e891f3acaf765
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287698"
---
# <a name="manage-a-proforma-invoice"></a>„Proforma“ sąskaitos faktūros valdymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Programoje „Dynamics 365 Project Operations” išankstinės sąskaitos faktūros kuriamos kaip „Dynamics 365 Sales” sąskaitų faktūrų plėtinys. Tačiau sąskaitų faktūrų išrašymo procesas programose „Sales” ir „Project Operations” labai skiriasi. Pavyzdžiui, neįmanoma sukurti naujos sąskaitos faktūros „Project Operations” puslapyje **Sąskaitų faktūrų sąrašas**, bet tai įmanoma padaryti programoje „Sales”. Šie skirtumai ir plėtiniai naudojami projektų, kurie skiriasi nuo įprastos pardavimo užsakymo sąskaitos faktūros, sąskaitų faktūrų išrašymo procesams palaikyti.

> [!IMPORTANT]
> Dėl šių skirtumų nenaudokite pakaitomis sąskaitų faktūrų programose „Sales” ir „Project Operations”.

## <a name="invoice-header"></a>Sąskaitos faktūros antraštė

Šią informaciją galima rasti „Proforma” sąskaitos faktūros antraštėje programoje „Project Operations”.

| Laukas | Vieta | Aprašo | Tolesnis poveikis |
| --- | --- | --- | --- |
| **Sąskaitos faktūros numeris** | Skirtukas **Suvestinė** | Automatiškai generuojamas ID kuriant „Proforma” sąskaitą faktūrą. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šis laukas naudojamas kaip kiekvienos „Proforma” sąskaitos faktūros nuoroda. |
| **Pavadinimas** | Skirtukas **Suvestinė** | Pagal numatytuosius nustatymus, nustatykite projekto sutarties pavadinimą. Šį lauką gali redaguoti vartotojas. | &nbsp;  |
| **Valiuta** | Skirtukas **Suvestinė** | Pagal numatytuosius nustatymus, nustatykite projekto sutarties valiutą. Tik skaitomas laukas, kurio redagavimas užrakinamas. |&nbsp; |
| **Kainoraštis** | Skirtukas **Suvestinė** | Pagal numatytuosius nustatymus, nustatykite projekto sutarties kainoraštį. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Galimybė** | Skirtukas **Suvestinė** | Susietos galimybės nuoroda. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp;  |
| **Sutartis** | Skirtukas **Suvestinė** | Susietos projekto sutarties nuoroda. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Klientas** | Skirtukas **Suvestinė** | Susietos projekto sutarties nuoroda. Tik skaitomas laukas, kurio redagavimas užrakinamas. |&nbsp;  |
| **Aprašas** | Skirtukas **Suvestinė** | Sąskaitą faktūrą apibūdinantis teksto laukas. Šį lauką gali redaguoti vartotojas. | &nbsp; |
| **Kam išrašyti sąskaitą** ir susiję laukai | **Suvestinės skirtukas** | Numatytosios reikšmės nustatomos iš projekto sutarties kliento. Šį lauką gali redaguoti vartotojas.  | &nbsp; |
| **Būsena** | Skirtukas **Suvestinė** | Nustatomos šios pasirinktys: **Suaktyvinta**, **Uždaryta**, **Apmokėta** ir **Atšaukta**, jas gali redaguoti vartotojas. | Nepalaikomos „Project Operations” būsenos yra **Uždaryta** ir **Atšaukta**. </br> Sukūrus sąskaitą faktūrą, būsena nustatoma kaip **Suaktyvinta**. </br>Būsena turi būti nustatyta kaip **Apmokėta** tik patvirtinus sąskaitą faktūrą. |
| **Projekto sąskaitos faktūros būsena** | Skirtukas **Suvestinė** | Nustatomos šios pasirinktys: **Juodraštis**, **Peržiūrima** ir **Patvirtinta**, jas gali redaguoti vartotojas. | Esant būsenoms **Juodraštis** ir **Peržiūrima**, sąskaitą faktūrą galima redaguoti. Patvirtinus sąskaitą faktūrą, jos redaguoti nebegalima. |
| **Išsami suma** | Skirtukas **Suvestinė** | Visose sąskaitos faktūros eilutėse esančių kiekių suma, atlikus išankstinius apmokėjimus ir atskaitymus. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šis laukas naudojamas galutinei sumai apskaičiuoti. |
| **Nuolaida (%)** | Skirtukas **Suvestinė** | Šį lauką galima redaguoti norint įvesti nuolaidos procentą. „Project Operations” funkcijos nepalaiko šio lauko. | Tai nepalaikomas laukas. |
| **Nuolaidos suma** | Skirtukas **Suvestinė** | Šį lauką galima redaguoti norint įvesti nuolaidos sumą. „Project Operations” funkcijos nepalaiko šio lauko. | Tai nepalaikomas laukas. |
| **Suma be transportavimo mokesčio** | **Suvestinės skirtukas** | Bendra sąskaitos faktūros suma pritaikius nuolaidas. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šis laukas naudojamas galutinei sumai apskaičiuoti. |
| **Transportavimo mokesčio suma** | Skirtukas **Suvestinė** | Šį lauką galima redaguoti norint įvesti transportavimo mokesčio sumą. „Project Operations” funkcijos nepalaiko šio lauko. | Tai nepalaikomas laukas. |
| **Bendra mokesčių suma** | Skirtukas **Suvestinė** | Bendroji mokesčių suma iš visų sąskaitoje faktūroje esančių sąskaitos faktūros eilučių. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Joks. |
| **Bendra suma** | Skirtukas **Suvestinė** | Suma pritaikius nuolaidas ir mokesčius. | Suma yra suma, kurią turi sumokėti klientas. |

## <a name="project-based-invoice-lines"></a>Projektu pagrįstos sąskaitos faktūros eilutės

Programoje „Project Operations” visada yra viena sąskaitos faktūros eilutė, skirta kiekvienai projekto sutarties eilutei. Sąskaitos faktūros eilutė sukuriama, net jei nėra faktinių duomenų. Šią informaciją galima rasti „Proforma” sąskaitos faktūros eilutėje.

| Laukas | Vieta | Aprašo | Tolesnis poveikis |
| --- | --- | --- | --- |
| **Sąskaitos faktūros numeris** | Skirtukas **Bendra informacija** | Sąskaitos faktūros ID nuoroda. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Sąskaitos faktūros ID saitą galima naudoti norint grįžti prie sąskaitos faktūros antraštės. |
| **Pavadinimas** | Skirtukas **Bendra informacija** | Sąskaitos faktūros pavadinimas, pagal numatytuosius nustatymus nustatomas iš sutarties eilutės pavadinimo. Šį lauką gali redaguoti vartotojas. | &nbsp; |
| **Project** | Skirtukas **Bendra informacija** | Projektas, esantis susijusio projekto sutarties eilutėje. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Projekto saitą galima naudoti norint pereiti prie projekto. |
| **Atsiskaitymo metodas** | Skirtukas **Bendra informacija** | Atsiskaitymo metodas, esantis susijusio projekto sutarties eilutėje. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Sutarties eilutės suma** | Skirtukas **Bendra informacija** | Sutarties suma, esanti susijusio projekto sutarties eilutėje. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Išrašyta sąskaita faktūra iki datos** | Skirtukas **Bendra informacija** | Bendroji suma, esanti šios sąskaitos faktūros visų sąskaitos faktūros eilučių informacijoje. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Suma** | Skirtukas **Bendra informacija** | Bendroji suma, esanti šios sąskaitos faktūros visų apmokestinamos sąskaitos faktūros eilučių informacijoje. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šis laukas naudojamas galutinei sumai, esančiai sąskaitos faktūros antraštėje, apskaičiuoti. |
| **Mokestis** | Skirtukas **Bendra informacija** | Mokesčių suma, esanti šios sąskaitos faktūros eilutės visų sąskaitos faktūros eilučių informacijoje. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šis laukas naudojamas galutinei mokesčių sumai, esančiai sąskaitos faktūros antraštėje, apskaičiuoti. |
| **Išplėstinė suma** | Skirtukas **Bendra informacija** | Bendroji suma (**Mokesčiai ir sumos**), esanti šios sąskaitos faktūros eilutės visų apmokestinamų sąskaitos faktūros eilučių informacijoje. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šis laukas naudojamas galutinei sumai, esančiai sąskaitos faktūros antraštėje, apskaičiuoti. |

## <a name="invoice-line-details"></a>Sąskaitos faktūros eilutės informacija

Kiekvienoje projekto sąskaitoje faktūroje esančios sąskaitos faktūros eilutėje yra sąskaitos faktūros eilutės informacija. Ši eilutės informacija yra susijusi su pardavimo, už kurį neišrašyta sąskaita, faktiniais elementais ir etapais, kurie yra susiję su sutarties eilute, kurią nurodo sąskaitos faktūros eilutė. Visos šios operacijos pažymėtos kaip **Parengta išrašyti sąskaitą faktūrą**.

Sąskaitos faktūros eilutės informacija, skirta eilutei **Laiko ir medžiagų sąskaita faktūra**, puslapyje **Sąskaitos faktūros eilutė** grupuojama į **Apmokestinama**, **Neapmokestinama** ir **Nemokama**. **Apmokestinamos sąskaitos faktūros eilutės** išsami informacija pridedama prie sąskaitos faktūros bendrosios sumos. Laukai **Nemokama** ir **Neapmokestinami faktiniai duomenys** nepridedami prie sąskaitos faktūros eilutės bendrosios sumos.

Sąskaitos faktūros eilutės informacija, skirta eilutei **Fiksuotos kainos sąskaita faktūra**, kuriama iš etapų, susijusioje sutarties eilutėje pažymėtų kaip **Parengta išrašyti sąskaitą faktūrą**. Sukūrus sąskaitos faktūros eilutės išsamią informaciją iš etapo, etapo atsiskaitymo būsena atnaujinama į **Kliento sąskaita faktūra sukurta**.

### <a name="edit-invoice-line-details"></a>Sąskaitos faktūros eilutės išsamios informacijos redagavimas

Toliau nurodyti laukai pateikiami sąskaitos faktūros eilutės informacijoje, kuri yra paremta faktiniu pardavimu, už kurį neišrašyta sąskaita.

| Laukas | Aprašo | Tolesnis poveikis |
| --- | --- | --- |
| **Sąskaitos faktūros eilutė** | **Sąskaitos faktūros eilutės ID** nuoroda. Tik skaitomas laukas, redagavimas užrakintas. | Šį saitą galima naudoti norint grįžti prie sąskaitos faktūros antraštės. |
| **Aprašas** | Sąskaitos faktūros eilutės informacijos aprašas. Nustatoma pagal numatytuosius nustatymus iš lauko **Vidiniai komentarai**, esančio dalyje **Laiko įrašas** ir iš lauko **Aprašas**, esančio dalyje **Išlaidų įrašas**. Lauką gali redaguoti vartotojas.| &nbsp; |
| **Išorinis aprašas** | Sąskaitos faktūros eilutės informacijos aprašas. Nustatoma pagal numatytuosius nustatymus iš lauko **Išoriniai komentarai**, esančio dalyje **Laiko įrašas** ir iš lauko **Aprašas**, esančio dalyje **Išlaidų įrašas**. Lauką gali redaguoti vartotojas. | Šį aprašą galima naudoti nustatant, kas turėtų būti išspausdintoje sąskaitoje faktūroje, kuri bus siunčiama klientui. Programoje „Project Operations” „Proforma“ sąskaitoje faktūroje nėra reikiamų funkcijų, skirtų sąskaitos faktūros spausdinimo parametrams konfigūruoti. |
| **Pradžios data** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį lauką galima redaguoti naudojant naują sąskaitos faktūros eilutės išsamią informaciją, neparemtą šaltinio faktiniais duomenimis. |
| **Project** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Nustatoma pagal numatytuosius nustatymus projektui susijusiose sutarties eilutėje. |
| **Užduotis** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį lauką galima redaguoti naudojant naują sąskaitos faktūros eilutės išsamią informaciją, neparemtą šaltinio faktiniais duomenimis. Išplečiamajame sąraše rodomos visos užduotys, susietos su susijusia projekto sutarties eilute.  |
| **Operacijos kategorija** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį lauką galima redaguoti naudojant naują sąskaitos faktūros eilutės išsamią informaciją, neparemtą faktiniu šaltiniu. |
| **Vaidmuo** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį lauką galima redaguoti naudojant naują sąskaitos faktūros eilutės išsamią informaciją, neparemtą šaltinio faktiniais duomenimis. |
| **Rezervuojamas išteklius** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį lauką galima redaguoti naudojant naują sąskaitos faktūros eilutės išsamią informaciją, neparemtą faktiniu šaltiniu. |
| **Išteklių paskirstymo įmonė** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį lauką galima redaguoti naudojant naują sąskaitos faktūros eilutės išsamią informaciją, neparemtą šaltinio faktiniais duomenimis. |
| **Išteklių paskirstymo vienetas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį lauką galima redaguoti naudojant naują sąskaitos faktūros eilutės išsamią informaciją, neparemtą šaltinio faktiniais duomenimis. |
| **Kiekis** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį lauką galima redaguoti naudojant naują sąskaitos faktūros eilutės išsamią informaciją, neparemtą šaltinio faktiniais duomenimis. |
| **Vieneto grafikas** | Sąskaitos faktūros eilutės laiko informacija visada nustatyta kaip „Laikas” ir jos negalima redaguoti. Išlaidos nustatomos pagal numatytuosius nustatymus iš šaltinio išlaidų faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Pagal numatytuosius nustatymus nustatoma kaip **Laikas** naujos sąskaitos faktūros eilutės informacijoje, kuri neparemta faktiniais duomenimis. |
| **Vienetas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį lauką galima redaguoti naudojant naują sąskaitos faktūros eilutės išsamią informaciją, neparemtą šaltinio faktiniais duomenimis |
| **Kainos** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį lauką galima redaguoti naudojant naują sąskaitos faktūros eilutės išsamią informaciją, neparemtą šaltinio faktiniais duomenimis. Jei neįvedama jokia reikšmė, ji nustatoma pagal numatytuosius nustatymus paspaudus **Įrašyti**. |
| **Valiuta** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Nustatoma pagal numatytuosius nustatymus iš sąskaitos faktūros antraštės, kuriant naują sąskaitos faktūros informaciją be faktinio atsarginių kopijų kūrimo.  Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Suma** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Apskaičiuojama kaip **Kiekis \* kaina** kuriant nauja sąskaitos faktūros informaciją be atsarginių kopijų kūrimo faktinių duomenų. Apskaičiuojama paspaudus **Įrašyti**. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Mokestis** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Lauką gali redaguoti vartotojas | Lauką gali redaguoti vartotojas, kurdamas naują sąskaitos faktūros eilutės informaciją be atsarginių kopijų kūrimo faktinių duomenų. |
| **Išplėstinė suma** | Apskaičiuotasis laukas, apskaičiuojamas kaip **Suma + mokestis**. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Atsiskaitymo tipas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Lauką gali redaguoti vartotojas. | Pasirinkus **Apmokestinama**, pridedama eilutė į sąskaitų faktūrų eilučių bendrąsias sumas. Pasirinkus **Nemokama** ir **Neapmokestinama**, ji nebus įtraukta į sąskaitų faktūrų eilučių bendrąsias sumas. |
| **Operacijos tipas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Pagal numatytuosius nustatymus nustatoma kaip **Pardavimas, už kurį išrašyta sąskaita** ir užrakinama sukuriant naują **Sąskaitos faktūros eilutės informacija** be atsarginių kopijų kūrimo faktinių duomenų.  |
| **Operacijos klasė** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Pagal numatytuosius nustatymus nustatomas atsižvelgiant į tai, ar vartotojas pasirenka sukurti sąskaitos faktūros eilutės informaciją **Laikas**, **Išlaidos** arba **Mokestis** taip pat kuriant naują **Sąskaitos faktūros eilutės informaciją** be faktinio atsarginių kopijų kūrimo. Užrakinta redagavimui. |

Toliau nurodyti laukai pateikiami sąskaitos faktūros eilutės informacijoje, kuri yra paremta etapu.

| Laukas | Aprašo | Tolesnis poveikis |
| --- | --- | --- |
| **Sąskaitos faktūros eilutė** | **Sąskaitos faktūros eilutės ID** nuoroda. Tik skaitomas laukas, kurio redagavimas užrakinamas. | Šį saitą galima naudoti norint grįžti prie sąskaitos faktūros antraštės. |
| **Aprašas** | Sąskaitos faktūros eilutės informacijos aprašas. Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo aprašo. | &nbsp; |
|**Išorinis aprašas** | Sąskaitos faktūros eilutės informacijos, kuri yra nustatyta pagal numatytuosius nustatymus iš šaltinio etapo aprašo, aprašas. | Šį lauką galima naudoti nustatant, kas turėtų būti išspausdintoje sąskaitoje faktūroje, kuri bus siunčiama klientui. Programoje „Project Operations” „Proforma“ sąskaitoje faktūroje nėra reikiamų funkcijų, skirtų sąskaitos faktūros spausdinimo parametrams konfigūruoti. |
| **Pradžios data** | Nustatoma pagal numatytuosius nustatymus iš **Etapo** datos, esančios šaltinio etape. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Project** | Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Užduotis** | Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Operacijos kategorija** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Vaidmuo** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Rezervuojamas išteklius** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Išteklių paskirstymo vienetas** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Vieneto grafikas** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Vienetas** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Kainos** | Nustatoma pagal numatytuosius nustatymus iš sumos, esančios šaltinio etape. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Valiuta** | Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo. Tik skaitomas laukas, kurio redagavimas užrakinamas. |&nbsp; |
| **Suma** | Nustatoma pagal numatytuosius nustatymus iš sumos, esančios šaltinio etape. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Mokestis** | Nustatoma pagal numatytuosius nustatymus iš mokesčių sumos, esančios šaltinio etape. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Išplėstinė suma** | Nustatoma pagal numatytuosius nustatymus iš išplėstinės sumos, esančios šaltinio etape. Lauką gali redaguoti vartotojas | &nbsp; |
| **Atsiskaitymo tipas** | Pagal numatytuosius nustatymus visada nustatoma kaip **Apmokestinama**. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Operacijos tipas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |
| **Operacijos klasė** | Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo. Tik skaitomas laukas, kurio redagavimas užrakinamas. | &nbsp; |

## <a name="refresh-invoice-transactions"></a>Atnaujinti sąskaitos faktūros operacijas

Jei turite faktinių duomenų, kurie buvo pateikti sukūrus sąskaitą faktūrą, galite įtraukti šiuos faktinius duomenis į sąskaitą faktūrą.

1. Dalyje **Atsiskaitymo nebaigtų užduočių rodinys** pažymėkite duomenis kaip **Parengta išrašyti sąskaitą faktūrą**.   
2. Atidarykite „Proforma” sąskaitos faktūros juodraštį ir juostelėje **Veiksmai** spustelėkite **Atnaujinti sąskaitos faktūros eilutės operacijas**.

  Taip sukuriama sąskaitos faktūros eilutės išsami informacija bet kuriems faktiniams duomenims su praeities data ir pažymėtiems kaip **Parengta išrašyti sąskaitą faktūrą**, bet neįtrauktiems į sąskaitą faktūrą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]