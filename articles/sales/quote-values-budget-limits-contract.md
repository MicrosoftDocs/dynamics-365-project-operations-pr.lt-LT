---
title: Projekto pasiūlymo parametrai
description: Šioje temoje pateikta informacija apie informaciją ir parametrus, taikomus projekto pasiūlymams ir jų poveikį.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3f11188a47c6f0c7de9fb591fd3be3e22f8f7d842fb6d075c1f43d9baea4d225
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993476"
---
# <a name="header-details-for-project-based-quotes"></a>Projektu pagrįstų pasiūlymų antraštės išsami informacija

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_


Šiame straipsnyje paaiškinama projekto pasiūlymui taikoma informacija. Į tai įeina visi parametrai, kurie turi įtakos visoms pasiūlymo eilutėms ir informacija apie pasiūlymą, apibendrintą visuose eilutės elementuose, kad būtų galima vykdyti projekto pasiūlymo KPI.

Šioje lentelėje išvardyti projekto pasiūlymo santraukos informacijos laukai, kurie yra unikalūs programoje „Dynamics 365 Project Operations“ arba kurie turi kai kurių svarbių pasiūlymų veikimo pakeitimų naudojant „Dynamics 365 Sales“.

| **Laukas** | **Vieta** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Tipas | Suvestinės skirtukas (paslėptas) | Šis parinkčių rinkinio laukas sutelkia šias parinktis:</br>- Darbu pagrįsta (veikia tik kai įdiegta „Project Operations“)</br>- Elementu pagrįsta (yra tik jei turite įsidiegę „Project Operations“ ir „Sales")</br>- Pagrįstas aptarnavimo priežiūra (yra, kai įdiegta „Dynamics 365 Field Service“) | Kai naudojate „Project Operations“ programą, ši lauko reikšmė automatiškai nustatoma kaip **Darbu pagrįsta**. Taip pasiūlymas klasifikuojamas kaip projektu pagrįstas pasiūlymas. Pasiūlymas turi būti pagrįstas projektu, kad būtų galima įjungti visus projekto plėtinius ir funkcijas. |
| Įmonė, kuriai priklauso | Santrauka | Juridinis objektas, kuriame atsižvelgiama į išlaidas ir pajamas, sukauptas iš šio projekto arba projektų, susijusių su šiuo pasiūlymu. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. | Valdančioji įmonė atitinka juridinio subjekto koncepciją „Project Operations“ **Projekto valdymo ir apskaitos** modulyje. Visos išlaidos ir pajamos, gautos iš šio projekto, bus įtrauktos į valdančiosios įmonės DK. |
| Potencialus klientas | Skirtukas Suvestinė | Nurodo į kliento įmonę arba kliento įrašą. Galiojantis klientas, kurį galima nurodyti projekto pasiūlyme, turi būti nustatytas kaip klientas pasiūlymo valdančioje įmonėje. Valdančioji įmonė rodo juridinių subjektų sąrašą ir jie yra nustatyti „Project Operations“ **Projekto valdymo ir apskaitos** modulyje. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. | Projekto pasiūlymo valiuta nustatoma pagal kliento valiutą. Tačiau ją galima pakeisti prieš įrašant pasiūlymą. |
| Klientų tvarkytuvas | Skirtukas Suvestinė | Klientų vadybininko, atsakingo už sandorį, vardas. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. | Klientų vadybininkas yra atsakingas už ryšių su klientu viso projekto metu valdymą. Remiantis rezervuojamų išteklių įrašo susiejimu su klientų vadybininku, sutartį sudarantis vienetas projekto pasiūlyme laikomas numatytuoju.|
| Sutartį sudarantis vienetas | Skirtukas Suvestinė | Organizacijos vienetas, atsakingas už su šiuo pasiūlymu susijusio projekto arba projektų pristatymą. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. | Sutartį sudarantis vienetas yra įmonės padalinys, kuris vykdys projektus po to, kai sandoris bus uždarytas. Kiekvienas sutartį sudarantis vienetas turi valiutą, o ši valiuta naudojama projekto metu padarytoms sąmatinėms ir faktinėms išlaidoms. |
| Produkto kainoraštis | Skirtukas Suvestinė | Tai kainoraštis, naudojamas numatytosioms produktu pagrįsto pasiūlymo eilučių kainoms. Šio lauko pasirinkčių sąrašas rodo kainoraščių sąrašus, kuriuose kainoraščių valiuta atitinka pasiūlymo valiutą. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. Šis laukas galimybėje yra gaunamas iš kliento įrašo, tačiau jį galima keisti. | Kai pasiūlymas laimėtas, šio lauko vertė nukopijuojama į projekto sutarties eilutę, kuri sukuriama. |
| Valiuta | Skirtukas Suvestinė | Čia nurodoma valiuta, kuri bus naudojama pateikiant šio sandorio vertę. Tai taip pat valiuta, kuria klientui bus išrašyta sąskaita faktūra, jei sandoris bus laimėtas. Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. Šis laukas galimybėje yra gaunamas iš kliento įrašo, tačiau vartotojas jį gali pakeisti.  | Įrašius pasiūlymą, šio lauko nebegalima redaguoti. Jis naudojamas numatytosioms pasiūlymo produkto ir projekto kainoraščio reikšmėms gauti. Pasiūlymo valiuta naudojama, kad atitiktų kainoraščio valiutą. |
| Limitas, kurio negalima viršyti | Skirtukas Suvestinė | Jis nurodo sutartinę viršutinę galutinės vertės ribą, su kuria klientas sutinka šiam sandoriui. | Ši viršutinė riba įvertinama vykdant ir taikoma visiems eilutės elementams ir su šiuo sandoriu susijusiems projektams. |
| Pageidaujama pristatymo data | Skirtukas Suvestinė | Kai pasiūlymas, sukuriamas iš galimybės, šis laukas nukopijuojamas iš atitinkamo galimybės eilutės lauko. | Ši data naudojama kaip sąskaitų faktūrų generavimo grafiko pabaigos data. |

Toliau nurodyti skirtukai ir KPI, kuriuos galite naudoti projekto pasiūlyme ir kurie yra unikalūs „Project Operations“ arba kurių veikimas iš esmės skiriasi nuo „Sales“ pasiūlymų:

| **Laukas** | **Vieta** | **Aprašas** |
| --- | --- | --- |
| Pelningumo analizė | Skirtukas pasiūlyme | Skirtukas rodo toliau pateiktas metrikas.</br>- Bendra apmokestinama savikaina</br></br>- Bendra neapmokestinama savikaina</br>- Bendrosios pajamos</br>- Bendrosios pajamos (pagrindinės)</br>- Bruto marža</br>- Pakoreguota bruto marža|
| Palyginimas su kliento lūkesčiais | Skirtukas pasiūlyme | Šis skirtukas rodo toliau pateiktas metrikas.</br>- Numatomas baigimas</br>- Pageidaujamas baigimas</br>- Kliento biudžetas</br>- Pasiūlymo vertė |
| Pasiūlymo analizė | Skirtukas pasiūlyme | Šiame skirtuke apibendrinami šie svarbiausi projekto pasiūlymo KPI</br>- Palyginimas su kliento lūkesčiais dėl biudžeto ir grafiko</br>- Bruto marža</br>- Pakoreguota bruto marža |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
