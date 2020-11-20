---
title: Projekto sutarties laukai ir informacija
description: Šioje temoje pateikta informacija apie laukus, kurie veikia sutarties eilutes, ir informacija apie sutartį, apibendrinančią visų eilučių elementus.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 082292c54682022933a4b46b856f9241078a9067
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088017"
---
# <a name="project-contract-fields-and-information"></a>Projekto sutarties laukai ir informacija 

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šioje temoje pateikiama informacija apie visai projekto sutarčiai taikomus laukus, įskaitant parametrus, turinčius įtakos visoms sutarties eilutėms. Taip pat įtraukta informacija apie sutartį, apibendrinanti visus eilučių elementus, kad būtų galima valdyti projekto sutarties KPI.

Toliau esančioje lentelėje išvardyti projekto sutarties laukai, kurie yra unikalūs „Dynamics 365 Project Operations“ arba kurių veikimas iš esmės skiriasi nuo „Dynamics 365 Sales“ pardavimo užsakymų.

| Laukas | Vieta | Atitiktis, tikslas ir gairės | Tolesnis poveikis |
| --- | --- | --- | --- |
| Tipas | Skirtukas **Suvestinė** (paslėptas) | Tai parinkčių rinkinio laukas su nurodytomis parinktimis:</br>- **Darbu pagrįsta** (veikia, tik kai įdiegta „Project Operations“)</br>- **Elementu pagrįsta** (yra, tik jei turite įsidiegę „Project Operations“ ir „Sales")</br>- **Pagrįstas aptarnavimo priežiūra** (yra, kai įdiegta „Dynamics 365 Field Service“) | Naudojant „Project Operations“ šio lauko numatytoji reikšmė yra **Pagrįsta darbu** ir sutartis klasifikuojama kaip projektu pagrįsta sutartis. Sutartis turi būti pagrįsta projektu, kad būtų galima įjungti visus projekto plėtinius ir funkcijas. |
| Potencialus klientas | Skirtukas **Suvestinė** | Kliento įmonės arba kliento įrašo nuoroda. Kai sutartis sukuriama iš pasiūlymo, šis laukas nukopijuojamas iš atitinkamo pasiūlymo įrašo lauko. | Projekto sutarties valiuta nustatoma pagal kliento valiutą. Ją galima pakeisti prieš įrašant sutartį. |
| Klientų tvarkytuvas | Skirtukas **Suvestinė** | Klientų vadybininko, atsakingo už sandorį, vardas. Kai sutartis sukuriama iš pasiūlymo, šis laukas nukopijuojamas iš atitinkamo pasiūlymo įrašo lauko. | Klientų vadybininkas yra atsakingas už ryšių su klientu viso projekto vykdymo metu valdymą. Remiantis rezervuojamų išteklių įrašo susiejimu su klientų vadybininku, sutartį sudarantis vienetas projekto sutartyje laikomas numatytuoju. |
| Sutartį sudarantis vienetas | Skirtukas **Suvestinė** | Organizacijos vienetas, atsakingas už su šia sutartimi susijusių projektų pristatymą. Kai sutartis sukuriama iš pasiūlymo, šis laukas nukopijuojamas iš atitinkamo pasiūlymo įrašo lauko. | Sutartį sudarantis vienetas yra įmonės padalinys, kuris vykdo projektus. Kiekvienas sutartį sudarantis vienetas turi valiutą, o ši valiuta naudojama projekto metu padarytoms sąmatinėms ir faktinėms išlaidoms. |
| Produkto kainoraštis | Skirtukas **Suvestinė** | Šis kainoraštis naudojamas numatytosioms produktu pagrįstos sutarties eilučių kainoms. Šio lauko išplečiamųjų parinkčių sąrašas rodo kainoraščių sąrašą, kur kainoraščių valiuta atitinka sutarties valiutą. Kai sutartis sukuriama iš pasiūlymo, šis laukas nukopijuojamas iš atitinkamo pasiūlymo įrašo lauko. Projekto sutartyje šis laukas nustatomas naudojant kliento įrašą, tačiau jį galima pakeisti. | Nėra šio lauko proceso pabaigos atitikties. |
| Valiuta | Skirtukas **Suvestinė** | Valiuta, naudojama šio sandorio vertei pranešti, ir valiuta, kuria klientui bus išrašyta sąskaita faktūra. Kai sutartis sukuriama iš pasiūlymo, šis laukas nukopijuojamas iš atitinkamo pasiūlymo įrašo lauko. Projekto sutartyje šis laukas nustatomas naudojant kliento įrašą, tačiau jį galima pakeisti. | Įrašius sutartį, šio lauko nebegalima redaguoti. Jis naudojamas numatytosioms sutarties produkto ir projekto kainoraščių reikšmėms gauti. Sutarties valiuta naudojama, kad atitiktų kainoraščio valiutą. |
| Limitas, kurio negalima viršyti | Skirtukas **Suvestinė** | Šis laukas nurodo sutartinę viršutinę galutinės vertės ribą, su kuria klientas sutiko sudarydamas šį sandorį. | Viršutinė riba įvertinama vykdant ir taikoma visiems eilutės elementams bei su šiuo sandoriu susijusiems projektams. |
| Pageidaujama pristatymo data | Skirtukas **Suvestinė** | Kai sutartis sukuriama iš projekto pasiūlymo, šis laukas nukopijuojamas iš atitinkamo projekto pasiūlymo lauko. | Ši data naudojama kaip sąskaitų faktūrų generavimo grafikų pabaigos data. |

Nurodyti KPI pasiekiami projekto sutarties skirtuke **Sutarties efektyvumas**.

| Laukas | Vieta | Atitiktis, tikslas ir gairės |
| --- | --- | --- |
| Sutarties vertė | Bendra sutartis | Bendra projekto sutarties vertė. |
| Išrašytos sąskaitos suma | Bendra sutartis | Visų šios sutarties sąskaitų faktūrų sumų suma. |
| Taikoma savikaina | Bendra sutartis | Visų su sutartimi susietų projektų visų faktinių užregistruotų išlaidų suma. |
| Bruto marža | Bendra sutartis | Sąskaitos faktūros suma – išlaidos, patirtos iki datos / sąskaitos faktūros suma |
| Numatoma marža | Bendra sutartis | (Sutarties vertė – numatomos išlaidos) / sutarties valueEstimated išlaidos = Visų su sutartimi susietų projektų apskaičiuotų išlaidų suma.|
| Sutarties vertė | Projektu pagrįstos eilutės | Sutarties eilutės reikšmė. |
| Išrašytos sąskaitos faktūros suma | Projektu pagrįstos eilutės | Fiksuotos kainos sutarties eilutė: visų išrašytų pardavimo etapo faktinių sumų suma, palyginti su šia sutarties eilute įvairiose sukurtose šios sutarties sąskaitose faktūrose. Laiko ir medžiagų sutarties eilutė: visų mokėtinų pardavimo faktinių sumų suma, palyginti su šia sutarties eilute įvairiose sukurtose šios sutarties sąskaitose faktūrose. |
| Taikoma savikaina | Projektu pagrįstos eilutės | Visų su sutarties eilute susietų projektų visų faktinių užregistruotų išlaidų suma. |
| Bruto marža | Projektu pagrįstos eilutės | (Sąskaitos faktūros suma – išlaidos, patirtos iki datos) / sąskaitos faktūros suma |
| Numatoma marža | Projektu pagrįstos eilutės | (Sutarties eilutės suma pagrindine valiuta – apskaičiuotos sutarties eilutės išlaidos pagrindine valiuta) / sutarties eilutės suma pagrindine valiuta |
| Taikoma savikaina | Projektu pagrįstos eilutės duomenys | Laikas: faktinės laiko savikainos, užregistruotos šiam vaidmeniui projekte, susietame su sutarties eilute, suma. Išlaidos: visos faktinės išlaidų savikainos, užregistruotos šiai kategorijai projekte, susietame su sutarties eilute, suma. |
| Užregistruotas kiekis | Projektu pagrįstos eilutės duomenys | Laikas: visos laiko savikainos, užregistruotos šiam vaidmeniui projekte, susietame su šia sutarties eilute, kiekis. Išlaidos: visi šios išlaidų kategorijos kiekiai išlaidų savikainos faktiniuose duomenyse – projekte, susietame su šia sutarties eilute. |
| Išrašytos sąskaitos suma | Projektu pagrįstos eilutės duomenys | Fiksuotos kainos sutarties eilutėje šis laukas paliekamas tuščias išsamios informacijos lygyje ir rodomas tik sutarties eilutės lygyje. Laiko ir medžiagų sutarties eilutės skaičiavimai atliekami išsamios informacijos lygyje. Išsami informacija rodo visų pajamų eilučių, kurioms išrašytos sąskaitos faktūros, sumą, palygintą su apmokėtina šios sutarties eilute. |
| Išrašytos sąskaitos kiekis | Projektu pagrįstos eilutės duomenys | Fiksuotos kainos sutarties eilutėje šis laukas paliekamas tuščias išsamios informacijos lygyje ir rodomas tik sutarties eilutės lygyje. Laiko ir medžiagų sutarties eilutės skaičiavimai atliekami laiko ir išlaidų išsamios informacijos lygyje. Laikas: visų šio vaidmens pajamų eilučių, kurioms išrašytos sąskaitos faktūros, valandų suma, palyginta su apmokėtina šios sutarties eilute. Išlaidos: visi šios išlaidų kategorijos kiekiai išlaidų savikainos faktiniuose duomenyse – projekte, susietame su šia sutarties eilute. |
| Sutarties vertė | Produktu pagrįstos eilutės | Šios produktu pagrįstos sutarties eilutės reikšmė. |
| Išrašytos sąskaitos suma | Produktu pagrįstos eilutės | Visų sąskaitos faktūros eilutėse esančių sumų suma, palyginta su šia produktu pagrįstos sutarties eilute įvairiose šios sutarties sąskaitose faktūrose. |
| Taikoma savikaina | Produktu pagrįstos eilutės | Visų produktu pagrįstos sutarties eilutės faktinių užregistruotų išlaidų suma. |
| Bruto marža | Projektu pagrįstos eilutės | Sąskaitos faktūros suma – išlaidos, patirtos iki datos / sąskaitos faktūros suma |
| Numatoma marža | Produktu pagrįstos eilutės | (Sutarties eilutės reikšmė – apskaičiuotos sutarties eilutės išlaidos) / sutarties eilutės reikšmė |