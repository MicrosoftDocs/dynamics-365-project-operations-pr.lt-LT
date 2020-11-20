---
title: Įvertinimų kūrimas pasiūlymo eilutėje
description: Šioje temoje pateikta informacija apie tai, kaip sukurti projekto pasiūlymo eilutės įvertinimą.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 97030689eddb88576ffcf9dd848f8a0776512192
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122938"
---
# <a name="create-estimates-on-a-quote-line"></a>Įvertinimų kūrimas pasiūlymo eilutėje

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projektu pagrįstame pasiūlyme galite naudoti pasiūlymo eilutės informacijos objektą ir įvertinti reikiamo pristatyti darbo dydį. Tada galite bendrinti įvertinimą su klientu.

Projektu pagrįstose pasiūlymo eilutėse neturi būti pasiūlymo eilutės informacijos. Taip pat šiose eilutėse gali būti pateikta daug pasiūlymo eilutės informacijos. Pasiūlymo eilutės informacija naudojama norint apskaičiuoti laiką, išlaidas arba mokesčius. „Dynamics 365 Project Operations“ neleidžia atlikti medžiagų įvertinimo pagal pasiūlymo eilutės informaciją. Tai vadinama operacijų klasėmis. Įvertintas mokesčių sumas taip pat galima įvesti operacijos klasėje.

Be operacijų klasių pasiūlymo eilutės informacijos dalyje taip pat nurodomas operacijos tipas. Egzistuoja du pasiūlymo eilutės informacijos operacijų tipai: **Savikainos** ir **Projekto sutarties**.

## <a name="estimate-by-using-a-contract"></a>Įvertinimas naudojant sutartį

Jei kurdami projektu pagrįstą sutartį naudojote „Project Operations“ pasiūlymą, kiekvieno pasiūlymo eilutės įvertinimas nukopijuojamas į projekto sutartį. Projekto sutarties struktūra yra tokia pati, kaip ir projekto pasiūlymo: pateikiamos eilutės, eilučių informacija ir sąskaitų faktūrų grafikai.

Įvertinimus galima atlikti tiesiogiai projekto sutartyje, pvz., projekto pasiūlymo dalyje. Projekto pasiūlymo įvertinimas atliekamas naudojant sutarties eilutes ir sutarties eilutės informaciją. Sutarties eilutės informaciją taip pat galima sugeneruoti pagal projekto planą, sukurtą naudojant metodą „iš apačios į viršų“.

Sutarties eilutės informaciją galima panaudoti norint apskaičiuoti laiką, išlaidas arba mokesčius. Įvertintas mokesčių sumas taip pat galima įvesti sutarties eilutės informacijos dalyje.

Medžiagos įvertinimai negalimi sutarties eilutės informacijai.

Projekto sutarties dalyje palaikomi procesai – sąskaitos faktūros kūrimas ir patvirtinimas. Naudojant sąskaitos faktūros procesą, sukuriamas projektu pagrįstos sąskaitos faktūros juodraštis, kuriame įtraukiami visi iki esamos datos esančių pardavimų, už kuriuos neišrašyta sąskaita, faktiniai duomenys.

Patvirtinus sutartis tampa skirta tik skaityti ir jos būsena iš **Juodraštis** pakeičiama į **Patvirtinta**. Atlikę šį veiksmą, jo atšaukti negalite. Šis veiksmas yra nuolatinis, todėl geriausia sutartį saugoti nustačius būseną **Juodraštis**.

Vieninteliai skirtumai tarp sutarčių juodraščių ir patvirtintų sutarčių yra jų būsenos, taip pat tai, kad juodraštines sutartis galima redaguoti, o patvirtintų sutarčių – ne. Sukurti sąskaitas faktūras ir sekti faktinius duomenis galima naudojant juodraštines ir patvirtintas sutartis.

Negalima keisti užsakymų sutartims arba projektams.

## <a name="estimating-projects"></a>Projektų vertinimas

Galite apskaičiuoti laiką ir išlaidas projektams, bet ne medžiagoms ar mokesčiams.

Laiko įvertinimai generuojami kuriant užduotį ir nurodant bendrojo ištekliaus, kuris reikalingas norint atlikti užduotį, atributus. Laiko įvertinimai generuojami pagal suplanuotas užduotis. Laiko įvertinimai nekuriami, jei bendruosius komandos narius kuriate atskirai nuo grafiko.

Išlaidų įvertinimus galima įvesti puslapio **Įvertinimai** tinklelyje.

## <a name="understand-estimation"></a>Įvertinimo paaiškinimas

Naudokite šią lentelę kaip vadovą, kad suprastumėte verslo logiką, naudojamą vertinimo etapu.

| Scenarijus                                                                                                                                                                                                                                                                                                                                          | Objekto įrašas                                                                                                                                                                                                       | Operacijos tipas | Operacijos klasė | Papildoma informacija                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Kai reikia apskaičiuoti pasiūlymo laiko pardavimo vertę                                                                                                                                                                                                                                                                                    | Sukuriamas pasiūlymo eilutės informacijos (QLD) įrašas                                                                                                                                                                               | Projekto sutartis | Time        | Operacijos kilmės lauko iš pardavimo pusės QLD eilutė nurodo į savikainos pusės QLD |
|                                                                                                                                                                                                                                                                                     | Antrą QLD įrašą sukuria sistema, kad būtų išsaugotos atitinkamos savikainos vertės. Visus ne su pinigais susijusius laukus iš pardavimo QLD į savikainos QLD nukopijuoja sistema.                                                                                                                                                                               | Išlaidos | Time        | Operacijos kilmės lauko iš pardavimo pusės pasiūlymo kainos informacijos (QLD) eilutė nurodo į savikainos pusės QLD |
| Kai reikia apskaičiuoti sutarties laiko pardavimo vertę                                                                                                                                                                                                                                                                                 | Sukuriamas pasiūlymo sutarties eilutės informacijos (CLD) įrašas                                                                                                                                                                    | Projekto sutartis | Time        | Operacijos kilmės lauko iš pardavimo pusės CLD eilutė nurodo į savikainos CLD      |
|                                                                                                                                                                                                                                                                                  | Antrą CLD įrašą sukuria sistema, kad būtų išsaugotos atitinkamos savikainos vertės. Visus ne su pinigais susijusius laukus iš pardavimo CLD į savikainos CLD nukopijuoja sistema.                                                                                                                                                                    | Išlaidos | Time        | Operacijos kilmės lauko iš pardavimo pusės CLD eilutė nurodo į savikainos CLD      |
| Kai vartotojas aprašo išteklių projekto užduoties lauke                                                                                                                                                                                                                                                                                            | Įvertinimo eilutės įrašas, skirtas užduoties pardavimo vertei rodyti, sukuriamas, kai sukuriama užduotis, į kurią įtrauktos visos reikiamos kainodaros dimensijos. Vaidmens ir organizacijos vienetai yra kainodaros dimensijos | Projekto sutartis | Laikas        |                                                                                   |
|     | Įvertinimo eilutės įrašas, skirtas užduoties savikainos vertei rodyti, sukuriamas, kai sukuriama užduotis, į kurią įtrauktos visos reikiamos kainodaros dimensijos. Visus ne su pinigais susijusius laukus iš pardavimo įvertinimo eilutės į savikainos įvertinimo eilutę nukopijuoja sistema. Vaidmens ir organizacijos vienetai yra kainodaros matmenys, taikomi savikainos ir sąskaitų tarifams.                                                                                                                                                                                                                | Savikaina             | Laikas           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Pasiūlymo eilutės informacijos ir sutarties eilutės informacijos objektų tinkinimas

Jei pridėjote pasirinktinį lauką pasiūlymo eilutės informacijos dalyje ir norite, kad sistema įvestų lauko vertę kaip numatytąją vertę susijusioje savikainos eilutėje, kurią sistema sukuria, naudokite priedų Preoperationkontraktlinedetailupdate ir Preoperationkotielinedetailupdate registracijos įrankius. Šie priedai turi būti iš naujo užregistruoti pakeitus pasiūlymo eilutės informaciją arba sutarties eilutės informaciją. Norėdami užbaigti sprendimus, atlikite toliau nurodytus veiksmus.

1. Atidarykite PluginRegistrationTool ir prisijunkite prie savo internetinio egzemplioriaus.
2. Pasirinkite **Ieškoti** ir ieškokite priedo, kurį norite naujinti.
3. Pasirinkite priedą, tada pagrindiniame puslapyje pasirinkite **Pasirinkti**.
4. Pasirinkite norimo naujinti priedo veiksmą, spustelėkite dešiniuoju pelės mygtuku ir pasirinkite **Naujinti**.
5. Dialogo lango **Esamo veiksmo naujinimas** lauke **Filtravimo atributai** pasirinkite daugtaškio mygtuką (**...**):
6. Dialogo lange **Atributų pasirinkimas** pasirinkite pasirinktinių atributų žymės langelius.
7. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą, tada pasirinkite **Veiksmo naujinimas**.
8. Pakartokite 1–7 veiksmus ir su antru priedu.
9. Uždarykite PluginRegistrationTool.
