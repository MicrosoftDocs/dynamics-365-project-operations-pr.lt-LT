---
title: Išankstinės projektu pagrįstos sąskaitos faktūros valdymas
description: Šioje temoje pateikiama informacija apie tai, kaip valdyti išankstines projektu pagrįstas sąskaitas faktūras ir su jomis dirbti.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cba74c14f6d039dce0650f25ee04cbe35ec8f668b774cdaaa3bbf1aab99cb44d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989336"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Išankstinės projektu pagrįstos sąskaitos faktūros valdymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Programoje „Dynamics 365 Project Operations” išankstinės sąskaitos faktūros kuriamos kaip „Dynamics 365 Sales” sąskaitų faktūrų plėtinys. Tačiau sąskaitų faktūrų išrašymo procesas programose „Sales” ir „Project Operations” labai skiriasi. Pavyzdžiui, neįmanoma sukurti naujos sąskaitos faktūros „Project Operations” puslapyje **Sąskaitų faktūrų sąrašas**, bet tai įmanoma padaryti programoje „Sales”. Šie skirtumai ir plėtiniai naudojami projektų, kurie skiriasi nuo įprastos pardavimo užsakymo sąskaitos faktūros, sąskaitų faktūrų išrašymo procesams palaikyti.

> [!IMPORTANT]
> Dėl šių skirtumų nenaudokite pakaitomis sąskaitų faktūrų programose „Sales” ir „Project Operations”.

## <a name="invoice-header"></a>Sąskaitos faktūros antraštė

Šią informaciją galima rasti „Proforma” sąskaitos faktūros antraštėje programoje „Project Operations”.

| Laukas | Vieta | Aprašymas |
| --- | --- | --- | 
| **Sąskaitos faktūros ID** | Skirtukas **Suvestinė** | Automatiškai generuojamas ID kuriant „Proforma” sąskaitą faktūrą. Tik skaitomas laukas, kurio redagavimas užrakinamas. Šis laukas naudojamas kaip kiekvienos „Proforma” sąskaitos faktūros nuoroda. |
| **Pavadinimas** | Skirtukas **Suvestinė** | Pagal numatytuosius nustatymus, nustatykite projekto sutarties pavadinimą. Šį lauką galima redaguoti. | 
| **Valiuta** | Skirtukas **Suvestinė** | Pagal numatytuosius nustatymus, nustatykite projekto sutarties valiutą. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Kainoraštis** | Skirtukas **Suvestinė** | Pagal numatytuosius nustatymus, nustatykite projekto sutarties kainoraštį. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Galimybė** | Skirtukas **Suvestinė** | Susietos galimybės nuoroda. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Sutartis** | Skirtukas **Suvestinė** | Susietos projekto sutarties nuoroda. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Klientas** | Skirtukas **Suvestinė** | Susietos projekto sutarties nuoroda. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Aprašas** | Skirtukas **Suvestinė** | Sąskaitą faktūrą apibūdinantis teksto laukas. Šį lauką galima redaguoti. | 
| **Kam išrašyti sąskaitą** ir susiję laukai | **Suvestinės skirtukas** | Numatytosios reikšmės nustatomos iš projekto sutarties kliento. Šį lauką galima redaguoti.  | 
| **Būsena** | Skirtukas **Suvestinė** | Nustatomos šios parinktys: **Aktyvinta**, **Uždaryta**, **Apmokėta** ir **Atšaukta** ir jas galima redaguoti. Nepalaikomos „Project Operations” būsenos yra **Uždaryta** ir **Atšaukta**. </br> Sukūrus sąskaitą faktūrą, būsena nustatoma kaip **Suaktyvinta**. </br>Būsena turi būti nustatyta kaip **Apmokėta** tik patvirtinus sąskaitą faktūrą.  | 
| **Projekto sąskaitos faktūros būsena** | Skirtukas **Suvestinė** | Nustatomos šios parinktys: **Juodraštis**, **Peržiūrima**, **Patvirtinta** ir jas galima redaguoti. Esant būsenoms **Juodraštis** ir **Peržiūrima**, sąskaitą faktūrą galima redaguoti. Patvirtinus sąskaitą faktūrą, jos redaguoti nebegalima. | 
| **Išsami suma** | Skirtukas **Suvestinė** | Visose sąskaitos faktūros eilutėse esančių kiekių suma, atlikus išankstinius apmokėjimus ir atskaitymus. Tik skaitomas laukas, kurio redagavimas užrakinamas.  Šis laukas naudojamas galutinei sumai apskaičiuoti. | 
| **Nuolaida (%)** | Skirtukas **Suvestinė** | Šį lauką galima redaguoti norint įvesti nuolaidos procentą. „Project Operations” funkcijos nepalaiko šio lauko. Tai nepalaikomas laukas.|  
| **Nuolaidos suma** | Skirtukas **Suvestinė** | Šį lauką galima redaguoti norint įvesti nuolaidos sumą. „Project Operations” funkcijos nepalaiko šio lauko. Tai nepalaikomas laukas. |  
| **Suma be transportavimo mokesčio** | **Suvestinės skirtukas** | Bendra sąskaitos faktūros suma pritaikius nuolaidas. Tik skaitomas laukas, kurio redagavimas užrakinamas. Šis laukas naudojamas galutinei sumai apskaičiuoti.  | 
| **Transportavimo mokesčio suma** | Skirtukas **Suvestinė** | Šį lauką galima redaguoti norint įvesti transportavimo mokesčio sumą. „Project Operations” funkcijos nepalaiko šio lauko. Tai nepalaikomas laukas. |
| **Bendra mokesčių suma** | Skirtukas **Suvestinė** | Bendroji mokesčių suma iš visų sąskaitoje faktūroje esančių sąskaitos faktūros eilučių. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Bendra suma** | Skirtukas **Suvestinė** | Suma pritaikius nuolaidas ir mokesčius. Suma yra suma, kurią turi sumokėti klientas. | 

## <a name="project-based-invoice-lines"></a>Projektu pagrįstos sąskaitos faktūros eilutės

Programoje „Project Operations” visada yra viena sąskaitos faktūros eilutė, skirta kiekvienai projekto sutarties eilutei. Sąskaitos faktūros eilutė sukuriama, net jei nėra faktinių duomenų. Šią informaciją galima rasti „Proforma” sąskaitos faktūros eilutėje.

| Laukas | Vieta | Aprašymas | 
| --- | --- | --- |
| **Sąskaitos faktūros ID** | Skirtukas **Bendra informacija** | Sąskaitos faktūros ID nuoroda. Tik skaitomas laukas, kurio redagavimas užrakinamas. Sąskaitos faktūros ID saitą galima naudoti norint grįžti prie sąskaitos faktūros antraštės. | 
| **Pavadinimas** | Skirtukas **Bendra informacija** | Sąskaitos faktūros pavadinimas, pagal numatytuosius nustatymus nustatomas iš sutarties eilutės pavadinimo. Šį lauką galima redaguoti. |
| **Project** | Skirtukas **Bendra informacija** | Projektas, esantis susijusio projekto sutarties eilutėje. Tik skaitomas laukas, kurio redagavimas užrakinamas. Projekto saitą galima naudoti norint pereiti prie projekto. | 
| **Atsiskaitymo metodas** | Skirtukas **Bendra informacija** | Atsiskaitymo metodas, esantis susijusio projekto sutarties eilutėje. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Sutarties eilutės suma** | Skirtukas **Bendra informacija** | Sutarties suma, esanti susijusio projekto sutarties eilutėje. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Išrašyta sąskaita faktūra iki datos** | Skirtukas **Bendra informacija** | Bendroji suma, esanti šios sąskaitos faktūros visų sąskaitos faktūros eilučių informacijoje. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Suma** | Skirtukas **Bendra informacija** | Bendroji suma, esanti šios sąskaitos faktūros visų apmokestinamos sąskaitos faktūros eilučių informacijoje. Tik skaitomas laukas, kurio redagavimas užrakinamas. Šis laukas naudojamas galutinei sumai, esančiai sąskaitos faktūros antraštėje, apskaičiuoti. | 
| **Mokestis** | Skirtukas **Bendra informacija** | Mokesčių suma, esanti šios sąskaitos faktūros eilutės visų sąskaitos faktūros eilučių informacijoje. Tik skaitomas laukas, kurio redagavimas užrakinamas. Šis laukas naudojamas galutinei mokesčių sumai, esančiai sąskaitos faktūros antraštėje, apskaičiuoti. | 
| **Išplėstinė suma** | Skirtukas **Bendra informacija** | Bendroji suma (**Mokesčiai ir sumos**), esanti šios sąskaitos faktūros eilutės visų apmokestinamų sąskaitos faktūros eilučių informacijoje. Tik skaitomas laukas, kurio redagavimas užrakinamas. Šis laukas naudojamas galutinei sumai, esančiai sąskaitos faktūros antraštėje, apskaičiuoti. |

## <a name="invoice-line-details"></a>Sąskaitos faktūros eilutės informacija

Kiekvienoje projekto sąskaitoje faktūroje esančios sąskaitos faktūros eilutėje yra sąskaitos faktūros eilutės informacija. Ši eilutės informacija yra susijusi su pardavimo, už kurį neišrašyta sąskaita, faktiniais elementais ir etapais, kurie yra susiję su sutarties eilute, kurią nurodo sąskaitos faktūros eilutė. Visos šios operacijos pažymėtos kaip **Parengta išrašyti sąskaitą faktūrą**.

Eilutės **Laiko ir medžiagos sąskaita faktūra** atveju eilutės išsami informacija puslapyje **Sąskaitos faktūros eilutė** sugrupuojama į **Apmokestinama**, **Neapmokestinama** ir **Nemokama**. **Apmokestinamos sąskaitos faktūros eilutės** išsami informacija pridedama prie sąskaitos faktūros bendrosios sumos. Laukai **Nemokama** ir **Neapmokestinami faktiniai duomenys** nepridedami prie sąskaitos faktūros eilutės bendrosios sumos.

Eilutei **Fiksuotos kainos sąskaita faktūra** sąskaitos faktūros eilutės išsami informacija sukuriama pagal etapus, susijusioje sutarties eilutėje pažymėtus kaip **Parengta išrašyti sąskaitą faktūrą**. Sukūrus sąskaitos faktūros eilutės išsamią informaciją iš etapo, etapo atsiskaitymo būsena atnaujinama į **Kliento sąskaita faktūra sukurta**.

### <a name="edit-invoice-line-details"></a>Sąskaitos faktūros eilutės išsamios informacijos redagavimas

Toliau nurodyti laukai pateikiami sąskaitos faktūros eilutės informacijoje, kuri yra paremta faktiniu pardavimu, už kurį neišrašyta sąskaita.

| Laukas | Aprašymas |
| --- | --- | 
| **Sąskaitos faktūros eilutė** | **Sąskaitos faktūros eilutės ID** nuoroda. Šis laukas yra tik skaitomas ir užrakintas, kad negalėtumėte redaguoti. Šį saitą galima naudoti norint grįžti prie sąskaitos faktūros antraštės. | 
| **Aprašas** | Sąskaitos faktūros eilutės informacijos aprašas. Nustatoma pagal numatytuosius nustatymus iš lauko **Vidiniai komentarai**, esančio dalyje **Laiko įrašas** ir iš lauko **Aprašas**, esančio dalyje **Išlaidų įrašas**. Lauką galima redaguoti.| 
| **Išorinis aprašas** | Sąskaitos faktūros eilutės informacijos aprašas. Nustatoma pagal numatytuosius nustatymus iš lauko **Išoriniai komentarai**, esančio dalyje **Laiko įrašas** ir iš lauko **Aprašas**, esančio dalyje **Išlaidų įrašas**. Lauką galima redaguoti. Šį aprašą galima naudoti nustatant, kas turėtų būti išspausdintoje sąskaitoje faktūroje, kuri bus siunčiama klientui. Programoje „Project Operations” „Proforma“ sąskaitoje faktūroje nėra reikiamų funkcijų, skirtų sąskaitos faktūros spausdinimo parametrams konfigūruoti. | 
| **Pradžios data** | Tai yra tik skaitomas laukas, pagal numatytuosius parametrus nustatytas faktiniame šaltinyje. |
| **Project** | Tai yra tik skaitomas laukas, pagal numatytuosius parametrus susijusios sutarties eilutės projekte nustatytas faktiniame šaltinyje. |  
| **Užduotis** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Operacijos kategorija** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Vaidmuo** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. |  
| **Rezervuotini ištekliai** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Išteklių paskirstymo įmonė** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Išteklių paskirstymo vienetas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Kiekis** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. |  
| **Vieneto grafikas** | Sąskaitos faktūros eilutės laiko informacija visada nustatyta kaip „Laikas” ir jos negalima redaguoti. Išlaidos nustatomos pagal numatytuosius nustatymus iš šaltinio išlaidų faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Vienetas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. |  
| **Kainos** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Valiuta** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Suma** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Mokestis** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Lauką galima redaguoti.| 
| **Išplėstinė suma** | Apskaičiuotasis laukas, apskaičiuojamas kaip **Suma + mokestis**. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Atsiskaitymo tipas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Lauką galima redaguoti. Pasirinkus **Apmokestinama**, pridedama eilutė į sąskaitų faktūrų eilučių bendrąsias sumas. Pasirinkus **Nemokama** ir **Neapmokestinama**, ji nebus įtraukta į sąskaitų faktūrų eilučių bendrąsias sumas.| 
| **Pasirinkti produktą** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Produktas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Produkto pavadinimas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. |  
| **Įtraukiamasis aprašas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Operacijos tipas** | Tai yra tik skaitomas laukas, pagal numatytuosius parametrus kaip **Pardavimas, už kurį išrašyta sąskaita** nustatytas faktiniame šaltinyje. |  
| **Operacijos klasė** | Nustatoma pagal numatytuosius nustatymus iš šaltinio faktinių duomenų. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 

Toliau nurodyti laukai pateikiami sąskaitos faktūros eilutės informacijos srityje, kuri yra paremta etapu.

| Laukas | Aprašymas |
| --- | --- | 
| **Sąskaitos faktūros eilutė** | **Sąskaitos faktūros eilutės ID** nuoroda. Tik skaitomas laukas, kurio redagavimas užrakinamas. Šį saitą galima naudoti norint grįžti prie sąskaitos faktūros antraštės.  | 
| **Aprašas** | Sąskaitos faktūros eilutės informacijos aprašas. Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo aprašo. | 
|**Išorinis aprašas** | Sąskaitos faktūros eilutės informacijos, kuri yra nustatyta pagal numatytuosius nustatymus iš šaltinio etapo aprašo, aprašas. Šį lauką galima naudoti nustatant, kas turėtų būti išspausdintoje sąskaitoje faktūroje, kuri bus siunčiama klientui. Programoje „Project Operations” „Proforma“ sąskaitoje faktūroje nėra reikiamų funkcijų, skirtų sąskaitos faktūros spausdinimo parametrams konfigūruoti. | 
| **Pradžios data** | Nustatoma pagal numatytuosius nustatymus iš **Etapo** datos, esančios šaltinio etape. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Project** | Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Užduotis** | Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Operacijos kategorija** | Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Vaidmuo** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Rezervuojamas išteklius** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Išteklių paskirstymo vienetas** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Vieneto grafikas** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Vienetas** | Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Kainos** | Nustatoma pagal numatytuosius nustatymus iš sumos, esančios šaltinio etape. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Valiuta** | Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Suma** | Nustatoma pagal numatytuosius nustatymus iš sumos, esančios šaltinio etape. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Mokestis** | Nustatoma pagal numatytuosius nustatymus iš mokesčių sumos, esančios šaltinio etape. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Išplėstinė suma** | Nustatoma pagal numatytuosius nustatymus iš išplėstinės sumos, esančios šaltinio etape. Lauką galima redaguoti. | 
| **Atsiskaitymo tipas** | Pagal numatytuosius nustatymus visada nustatoma kaip **Apmokestinama**. Tik skaitomas laukas, kurio redagavimas užrakinamas. |
| **Operacijos tipas** | Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 
| **Operacijos klasė** | Nustatoma pagal numatytuosius nustatymus iš šaltinio etapo. Tik skaitomas laukas, kurio redagavimas užrakinamas. | 

## <a name="refresh-invoice-transactions"></a>Atnaujinti sąskaitos faktūros operacijas

Jei turite faktinių duomenų, kurie buvo pateikti sukūrus sąskaitą faktūrą, galite įtraukti šiuos faktinius duomenis į sąskaitą faktūrą.

1. Dalyje **Atsiskaitymo nebaigtų užduočių rodinys** pažymėkite duomenis kaip **Parengta išrašyti sąskaitą faktūrą**.   
2. Atidarykite išankstinės sąskaitos faktūros juodraštį ir juostoje **Veiksmai** pasirinkite **Atnaujinti sąskaitos faktūros eilutės operacijas**.

  Sąskaitos faktūros eilutės išsami informacija sukuriama bet kokiems faktiniams duomenims su praeities data ir pažymėtiems kaip **Parengta išrašyti sąskaitą faktūrą**, bet į sąskaitą faktūrą neįtrauktiems.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
