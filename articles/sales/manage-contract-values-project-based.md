---
title: Darbas su projektu pagrįstomis sutarčių eilutėmis
description: Šioje temoje pateikta informacija apie projektu pagrįstas sutarčių eilutes.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 14d880eccd5547c122ebe37b63022e64fa2fb6fe
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181731"
---
# <a name="work-with-projectbased-contract-lines"></a>Darbas su projektu pagrįstomis sutarčių eilutėmis

Projektu pagrįstos sutarčių eilutės programoje „Dynamics 365 Project Operations“ sukurtos tam tikriems projekto darbo su aktyvu komponentams įvertinti ir atsiskaitymo už juos sąskaitoms pateikti. Projektu pagrįstos sutarties eilutės struktūra išplečiama projektų sąmatų ir sąskaitų išrašymo scenarijams, taikant tolesnes koncepcijas.

- Atsiskaitymo metodas
- Projektų ir užduočių susiejimas
- Įtrauktų operacijų klasės
- Limitas, kurio negalima viršyti
- Apmokestinimo sąranka
- Sąmatos naudojant išsamią sutarties eilutės informaciją
- Sutarties eilutės klientai

Projektu pagrįstų sutarties eilučių skirtuke **Bendra** įtraukti toliau nurodyti laukai. Šie laukai padeda nustatyti išsamaus, visapusiško projektinio darbo sąmatų ir sąskaitų išrašymo tvarką.

| Laukas | Aprašo | Tolesnis poveikis |
| --- | --- | --- |
| **Pavadinimas** | Sutarties eilutės pavadinimas, identifikuojantis atskirą sutarties komponentą, kuris yra vertinamas. Vykdant projekto sutartį, sukurtą pagal pasiūlymą, ši reikšmė kopijuojama iš atitinkamos projektu pagrįstos pasiūlymo eilutės reikšmės. | Ši lauko reikšmė nukopijuojama į projekto sąskaitos faktūros eilutę, sukurtą pagal šią sutarties eilutę sukūrus sąskaitą faktūrą. |
| **Atsiskaitymo metodas** | Vykdant projekto sutartį, sukurtą pagal pasiūlymą, ši reikšmė kopijuojama iš atitinkamo lauko pasiūlymo eilutėje. Tai parinkčių rinkinys, vaizduojantis du pagrindinius sutarčių modelius, kuriuos palaiko „Project Operations“.</br>- **Fiksuota kaina**</br>- **Laikas ir medžiagos** | Pagal nurodytos sutarties eilutės atsiskaitymo metodą faktinė operacija bus apdorota. Jei sutarties eilutė, į kurią nurodo faktinis įrašas, turi sąskaitų už laiką ir medžiagas išrašymo būdą, kuriami išlaidų ir faktinio pardavimo be sąskaitų įrašai. Jei faktiniame įraše nurodyta sutarties eilutė turi fiksuotą kainos išrašymo metodą, sukuriami tik faktiniai kaštai. |
| **Project** | Šį lauką naudokite, jei norite nustatyti projektą, kuris bus naudojamas šiam įsipareigojimui vykdyti. | Šio lauko reikšmė bus naudojama kartu su laukais **Įtrauktos užduotys** ir **Įtrauktos operacijų klasės**, kad būtų išspręsta sutarties eilutės nuoroda faktiniame arba įvertintame eilutės įraše. |
| **Įtraukti laiką** | Vėliavėlė nurodo, ar šioje sutarties eilutėje įtrauktos pasirinkto projekto laiko operacijos ar darbo išlaidos. Reikšmė **Ne** nurodo, kad šioje sutarties eilutėje nebus įtrauktos laiko operacijos ar darbo išlaidos. Reikšmė **Taip** nurodo, kad jos bus įtrauktos. | Šio lauko reikšmė yra naudojama kartu su projektu, kad būtų išspręsta sutarties eilutės nuoroda faktiniame arba įvertintame eilutės įraše. |
| **Įtraukti išlaidas** | Vėliavėlė nurodo, ar šioje sutarties eilutėje bus įtraukti išlaidų kaštai. Reikšmė **Ne** nurodo, kad šioje sutarties eilutėje išlaidų kaštai nebus įtraukti. Reikšmė **Taip** nurodo, kad tai bus įtraukta. | Šio lauko reikšmė yra naudojama kartu su projektu, kad būtų išspręsta sutarties eilutės nuoroda faktiniame arba įvertintame eilutės įraše. |
| **Įtraukti mokestį** | Vėliavėlė nurodo, ar šioje sutarties eilutėje bus įtraukti mokesčiai. Reikšmė **Ne** nurodo, kad šioje sutarties eilutėje mokesčiai nebus įtraukti. Reikšmė **Taip** nurodo, kad jos bus įtrauktos. | Šio lauko reikšmė yra naudojama kartu su projektu, kad būtų išspręsta sutarties eilutės nuoroda faktiniame arba įvertintame eilutės įraše. |
| **Sutarties suma** | Fiksuotos kainos sutarties eilutėje tai yra sutarta reikšmė, kuri bus išrašyta klientui už visus su šia sutarties eilute susietus darbo komponentus. Laiko ir medžiagų sutarties eilutėje ši suma yra įvertinta reikšmė, kuri bus išrašyta klientui už visus su šia sutarties eilute susietus darbo komponentus. Vykdant projekto sutartį, kuri sukurta pagal pasiūlymą, ši reikšmė kopijuojama iš atitinkamo lauko pasiūlymo eilutėje. Kai projektu pagrįstoje sutarties eilutėje pateikiama eilutės informacija, šio lauko neleidžiama redaguoti ir jis apibendrinamas iš sumos, nurodytos sutarties eilutės informacijoje. | Kai sutarties eilutėje yra eilutės informacija, šią reikšmę galima modifikuoti keičiant eilutės išsamios informacijos sumas. Fiksuotos kainos sutarties eilutėje ši reikšmė naudojama sumai iki mokesčių generuoti periodinio atsiskaitymo etapuose. |
| **Įvertintas mokestis** | Vartotojas gali redaguoti šį lauką ir įvesti numatomą mokesčio sumą sutarties eilutėje. Kai projektu pagrįstoje sutarties eilutėje pateikiama eilutės informacija, šio lauko neleidžiama redaguoti ir jis apibendrinamas iš mokesčių sumos, nurodytos sutarties eilutės informacijoje. | Kai sutarties eilutėje yra eilutės informacija, šią reikšmę galima modifikuoti keičiant eilutės išsamios informacijos mokesčių sumas. Fiksuotos kainos sutarties eilutėje ši reikšmė naudojama mokesčiams generuoti periodinio atsiskaitymo etapuose. |
| **Sutarties suma po mokesčių** | Sutarties eilutės suma po mokesčių. Šis laukas yra tik skaitomas ir apskaičiuojamas kaip **sutarties suma + mokesčiai**. | Fiksuotos kainos sutarties eilutėje ši reikšmė naudojama periodinio atsiskaitymo etapams generuoti. |
| **Limitas, kurio negalima viršyti** | Vartotojas gali redaguoti šį lauką ir jis yra prieinamas tik projektu pagrįstose sutarties eilutėse, kuriose taikomas atsiskaitymo už laiką ir medžiagas metodas. | Vartotojas gali redaguoti šį lauką. Kai faktinis laiko ar išlaidų įrašas nurodo šią laiko ir medžiagų sutarties eilutę, faktinio įrašo sumos dydis įvertinamas pagal šios sutarties eilutės neviršijamą ribą, atsižvelgus į jau išleistas ir paskirtas sumas. |
| **Kliento biudžetas** | Šį lauką galima redaguoti ir jis nukopijuojamas iš atitinkamo lauko pasiūlymo eilutėje, jei sutartis buvo sukurta pagal pasiūlymą. | Šis laukas naudojamas tik informacijai ir neturi jokios reikšmės tolesnėms operacijoms. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Projektu pagrįstų sutarčių eilučių skirtuke Bendra pateikta parinkčių tikrinimo taisyklė

Taisyklė: projektas ir tam tikra operacijų klasė gali būti įtraukti tik į vieną projektu pagrįstą sutarties eilutę.

| Sutartis | Sutarties eilutė | Project | Įtraukti laiką | Įtraukti išlaidas | Įtraukti mokestį | Galioja / negalioja | Priežastis                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Taip          | Taip             | Taip         | Negalioja       | Pažeidžia taisyklę. Projekto P1 laikas, išlaidos ir mokesčiai įtraukiami į abi sutarties eilutes, CL1 ir CL2.                                                                                       |
| C1       | CL2           | P1      | Taip          | Taip             | Taip         | Negalioja       | Pažeidžia taisyklę. Projekto P1 laikas, išlaidos ir mokesčiai įtraukiami į abi sutarties eilutes, CL1 ir CL2.                                                                                       |
| C1       | CL1           | P1      | Taip          | No              | Taip         | Negalioja       | Pažeidžia taisyklę. Projekto P1 laikas ir mokesčiai įtraukiami į abi sutarties eilutes, CL1 ir CL2.                                                                                                   |
| C1       | CL2           | P1      | Taip          | Taip             | Taip         | Negalioja       | Pažeidžia taisyklę. Projekto P1 laikas ir mokesčiai įtraukiami į abi sutarties eilutes, CL1 ir CL2.                                                                                                   |
| C1       | CL1           | P1      | Taip          | No              | Taip         | Tinkama           | Projekto P1 laikas ir mokesčiai įtraukiami į CL1. P1 projekto išlaidos yra įtrauktos į CL2. </br>   Nėra persidengiančių elementų, įtrauktų į kiekvieną sutarties eilutę, todėl jie yra galiojantys.  |
| C1       | CL2           | P1      | No           | Taip             | No          | Tinkama           | Projekto P1 laikas ir mokesčiai įtraukiami į CL1. P1 projekto išlaidos yra įtrauktos į CL2. </br>   Nėra persidengiančių elementų, įtrauktų į kiekvieną sutarties eilutę, todėl jie yra galiojantys.  |
| C1       | CL1           | P1      | Taip          | Taip             | Taip         | Negalioja       | Pažeidžia taisyklę. P1 projekto laikas, išlaidos ir mokesčiai įtraukiami į dviejų sutarčių eilutes.                                                                                               |
| CL2      | CL2           | P1      | Taip          | Taip             | Taip         | Negalioja       | Pažeidžia taisyklę. P1 projekto laikas, išlaidos ir mokesčiai įtraukiami į dviejų sutarčių eilutes.                                                                                               |
