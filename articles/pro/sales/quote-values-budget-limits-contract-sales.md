---
title: Projekto pasiūlymo suvestinės informacija (Sales)
description: Šioje temoje pateikta informacija apie informaciją ir parametrus, taikomus projekto pasiūlymams ir jų poveikį. („Sales“)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d050258ae457bb4392d5fa761442cfc7a444feb0
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966825"
---
# <a name="summary-information-on-a-project-quote-sales"></a>Projekto pasiūlymo suvestinės informacija (Sales)

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šiame straipsnyje paaiškinama projekto pasiūlymui taikoma informacija. Į tai įeina visi parametrai, kurie turi įtakos visoms pasiūlymo eilutėms ir informacija apie pasiūlymą, apibendrintą visuose eilutės elementuose, kad būtų galima vykdyti projekto pasiūlymo KPI.

Toliau esančioje lentelėje išvardyti projekto pasiūlymo suvestinės informacijos laukai, kurie yra unikalūs „Dynamics 365 Project Operations“ arba kurių veikimas iš esmės skiriasi nuo „Dynamics 365 Sales“ pasiūlymų.

| **Laukas** | **Vieta** | **Atitiktis, tikslas ir gairės** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Tipas | Suvestinės skirtukas (paslėptas) | Šis parinkčių rinkinio laukas sutelkia šias parinktis:</br>- Darbu pagrįsta (veikia tik kai įdiegta „Project Operations“)</br>- Elementu pagrįsta (yra tik jei turite įsidiegę „Project Operations“ ir „Sales")</br>- Pagrįstas aptarnavimo priežiūra (yra, kai įdiegta „Dynamics 365 Field Service“) | Kai naudojate „Project Operations“ programą, ši lauko reikšmė automatiškai nustatoma kaip **Darbu pagrįsta**. Taip pasiūlymas klasifikuojamas kaip projektu pagrįstas pasiūlymas. Pasiūlymas turi būti pagrįstas projektu, kad būtų galima įjungti visus projekto plėtinius ir funkcijas. |
| Potencialus klientas | Skirtukas Suvestinė | Nurodo į kliento įmonę arba kliento įrašą. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. | Projekto pasiūlymo valiuta nustatoma pagal kliento valiutą. Tačiau ją galima pakeisti prieš įrašant pasiūlymą. |
| Klientų tvarkytuvas | Skirtukas Suvestinė | Klientų vadybininko, atsakingo už sandorį, vardas. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. | Klientų vadybininkas yra atsakingas už ryšių su klientu viso projekto metu valdymą. Remiantis rezervuojamų išteklių įrašo susiejimu su klientų vadybininku, sutartį sudarantis vienetas projekto pasiūlyme laikomas numatytuoju. |
| Sutartį sudarantis vienetas | Skirtukas Suvestinė | Organizacijos vienetas, atsakingas už su šiuo pasiūlymu susijusio projekto arba projektų pristatymą. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. | Sutartį sudarantis vienetas yra įmonės padalinys, kuris vykdys projektus po to, kai sandoris bus uždarytas. Kiekvienas sutartį sudarantis vienetas turi valiutą, o ši valiuta naudojama projekto metu padarytoms sąmatinėms ir faktinėms išlaidoms. |
| Produkto kainoraštis | Skirtukas Suvestinė | Tai kainoraštis, naudojamas numatytosioms produktu pagrįsto pasiūlymo eilučių kainoms. Šio lauko pasirinkčių sąrašas rodo kainoraščių sąrašus, kuriuose kainoraščių valiuta atitinka pasiūlymo valiutą. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. Šis laukas galimybėje yra gaunamas iš kliento įrašo, tačiau jį galima keisti. | Kai pasiūlymas laimėtas, šio lauko vertė nukopijuojama į projekto sutarties eilutę, kuri sukuriama. |
| Valiuta | Skirtukas Suvestinė | Čia nurodoma valiuta, kuri bus naudojama pateikiant šio sandorio vertę. Tai taip pat valiuta, kuria klientui bus išrašyta sąskaita faktūra, jei sandoris bus laimėtas. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. Šis laukas galimybėje yra gaunamas iš kliento įrašo, tačiau vartotojas jį gali pakeisti. | Įrašius pasiūlymą, šio lauko nebegalima redaguoti. Jis naudojamas numatytosioms pasiūlymo produkto ir projekto kainoraščio reikšmėms gauti. Pasiūlymo valiuta naudojama, kad atitiktų kainoraščio valiutą. |
| Limitas, kurio negalima viršyti | Skirtukas Suvestinė | Jis nurodo sutartinę viršutinę galutinės vertės ribą, su kuria klientas sutinka šiam sandoriui. | Ši viršutinė riba įvertinama vykdant ir taikoma visiems eilutės elementams ir su šiuo sandoriu susijusiems projektams. |
| Pageidaujama pristatymo data | Skirtukas Suvestinė | Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. | Ši data naudojama kaip sąskaitų faktūrų generavimo grafiko pabaigos data. |

Toliau nurodyti skirtukai ir KPI, kuriuos galite naudoti projekto pasiūlyme ir kurie yra unikalūs „Project Operations“ arba kurių veikimas iš esmės skiriasi nuo „Sales“ pasiūlymų:

| **Laukas** | **Vieta** | **Atitiktis, tikslas ir gairės** |
| --- | --- | --- |
| Pelningumo analizė | Skirtukas pasiūlyme | Skirtukas rodo toliau pateiktas metrikas.</br>- Bendra apmokestinama savikaina</br></br>- Bendra neapmokestinama savikaina</br>- Bendrosios pajamos</br>- Bendrosios pajamos (pagrindinės)</br>- Bruto marža</br>- Pakoreguota bruto marža|
| Palyginimas su kliento lūkesčiais | Skirtukas pasiūlyme | Šis skirtukas rodo toliau pateiktas metrikas.</br>- Numatomas baigimas</br>- Pageidaujamas baigimas</br>- Kliento biudžetas</br>- Pasiūlymo vertė |
| Pasiūlymo analizė | Skirtukas pasiūlyme | Šiame skirtuke apibendrinami šie svarbiausi projekto pasiūlymo KPI</br>- Palyginimas su kliento lūkesčiais dėl biudžeto ir grafiko</br>- Bruto marža</br>- Pakoreguota bruto marža |
