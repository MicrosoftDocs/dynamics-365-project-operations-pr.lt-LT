---
title: Įvertinimai
description: Šioje temoje pateikiama informacija apie įvertinimų teikimą programėlėje „Dynamics 365 Project Service Automation“.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 95f739f0c724ff93c4d588776f9e49687bac2035
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132779"
---
# <a name="estimates"></a>Įvertinimai

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektu pagrįstame pasiūlyme galite naudoti pasiūlymo eilutės informacijos objektą ir įvertinti reikiamo pristatyti darbo dydį. Tada galite bendrinti įvertinimą su klientu.

Projektu pagrįstose pasiūlymo eilutėse neturi būti pasiūlymo eilutės informacijos. Taip pat šiose eilutėse gali būti pateikta daug pasiūlymo eilutės informacijos. Pasiūlymo eilutės informacija naudojama norint apskaičiuoti laiką, išlaidas arba mokesčius. PSA neleidžia atlikti medžiagų įvertinimo pagal pasiūlymo eilutės informaciją. Tai vadinama operacijų klasėmis. Įvertintas mokesčių sumas taip pat galima įvesti operacijos klasėje.

Be operacijų klasių pasiūlymo eilutės informacijos dalyje taip pat nurodomas operacijos tipas. PSA palaiko du pasiūlymo eilutės informacijos operacijų tipus: **savikainos** ir **projekto sutarties**.

## <a name="estimate-by-using-a-contract"></a>Įvertinimas naudojant sutartį

Jei kurdami projektu pagrįstą sutartį naudojote PSA pasiūlymą, kiekvieno pasiūlymo eilutės įvertinimas nukopijuojamas į projekto sutartį. Projekto sutarties struktūra yra tokia pati, kaip ir projekto pasiūlymo: pateikiamos eilutės, eilučių informacija ir sąskaitų faktūrų grafikai.

Įvertinimus galima atlikti tiesiogiai projekto sutartyje, pvz., projekto pasiūlymo dalyje. Projekto pasiūlymo įvertinimas atliekamas naudojant sutarties eilutes ir sutarties eilutės informaciją. Sutarties eilutės informaciją taip pat galima sugeneruoti pagal projekto planą, sukurtą naudojant metodą „iš apačios į viršų“.

Sutarties eilutės informaciją galima panaudoti norint apskaičiuoti laiką, išlaidas arba mokesčius. Įvertintas mokesčių sumas taip pat galima įvesti sutarties eilutės informacijos dalyje.

PSA neleidžia atlikti medžiagų įvertinimo pagal sutarties eilutės informaciją.

Projekto sutarties dalyje palaikomi procesai – sąskaitos faktūros kūrimas ir patvirtinimas. Naudojant sąskaitos faktūros procesą, sukuriamas projektu pagrįstos sąskaitos faktūros juodraštis, kuriame įtraukiami visi iki esamos datos esančių pardavimų, už kuriuos neišrašyta sąskaita, faktiniai duomenys.

Patvirtinus sutartis tampa skirta tik skaityti ir jos būsena iš **Juodraštis** pakeičiama į **Patvirtinta**. Atlikę šį veiksmą, jo atšaukti negalite. Šis veiksmas yra nuolatinis, todėl geriausia sutartį saugoti nustačius būseną **Juodraštis**.

Vieninteliai skirtumai tarp sutarčių juodraščių ir patvirtintų sutarčių yra jų būsenos, taip pat tai, kad juodraštines sutartis galima redaguoti, o patvirtintų sutarčių – ne. Sukurti sąskaitas faktūras ir sekti faktinius duomenis galima naudojant juodraštines ir patvirtintas sutartis.

PSA nepalaiko sutarčių arba projektų užsakymo keitimo galimybės.

## <a name="estimating-projects"></a>Projektų vertinimas

Galite įvertinti darbo su projektais laiką ir išlaidas. PSA neleidžia įvertinti projektų medžiagų arba mokesčių.

Laiko įvertinimai generuojami kuriant užduotį ir nurodant bendrojo ištekliaus, kuris reikalingas norint atlikti užduotį, atributus. Laiko įvertinimai generuojami pagal suplanuotas užduotis. Laiko įvertinimai nekuriami, jei bendruosius komandos narius kuriate atskirai nuo grafiko.

Išlaidų įvertinimus galima įvesti puslapio **Įvertinimai** tinklelyje.

## <a name="understanding-estimation"></a>Įvertinimo paaiškinimas

Naudokite šią lentelę kaip vadovą, kad suprastumėte verslo logiką, naudojamą vertinimo etapu.

| Scenarijus                                                                                                                                                                                                                                                                                                                                          | Objekto įrašas                                                                                                                                                                                                       | Operacijos tipas | Operacijos klasė | Papildoma informacija                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Kai reikia apskaičiuoti pasiūlymo laiko pardavimo vertę                                                                                                                                                                                                                                                                                    | Sukuriamas pasiūlymo eilutės informacijos (QLD) įrašas                                                                                                                                                                               | Projekto sutartis | Time        | Operacijos kilmės lauko iš pardavimo pusės QLD eilutė nurodo į savikainos pusės QLD |
|                                                                                                                                                                                                                                                                                     | Antrą QLD įrašą sukuria sistema, kad būtų išsaugotos atitinkamos savikainos vertės. Visus ne su pinigais susijusius laukus iš pardavimo QLD į savikainos QLD nukopijuoja sistema.                                                                                                                                                                               | Išlaidos | Time        | Operacijos kilmės lauko iš pardavimo pusės pasiūlymo kainos informacijos (QLD) eilutė nurodo į savikainos pusės QLD |
| Kai reikia apskaičiuoti sutarties laiko pardavimo vertę                                                                                                                                                                                                                                                                                 | Sukuriamas pasiūlymo sutarties eilutės informacijos (CLD) įrašas                                                                                                                                                                    | Projekto sutartis | Time        | Operacijos kilmės lauko iš pardavimo pusės CLD eilutė nurodo į savikainos CLD      |
|                                                                                                                                                                                                                                                                                  | Antrą CLD įrašą sukuria sistema, kad būtų išsaugotos atitinkamos savikainos vertės. Visus ne su pinigais susijusius laukus iš pardavimo CLD į savikainos CLD nukopijuoja sistema.                                                                                                                                                                    | Išlaidos | Time        | Operacijos kilmės lauko iš pardavimo pusės CLD eilutė nurodo į savikainos CLD      |
| Kai vartotojas aprašo išteklių projekto užduoties lauke                                                                                                                                                                                                                                                                                            | Įvertinimo eilutės įrašas, skirtas užduoties pardavimo vertei rodyti, sukuriamas, kai sukuriama užduotis, į kurią įtrauktos visos reikiamos kainodaros dimensijos. Vaidmens ir organizacijos vienetai yra OOB Projekto Serviso kainodaros dimensijos | Projekto sutartis | Time        |                                                                                   |
|     | Įvertinimo eilutės įrašas, skirtas užduoties savikainos vertei rodyti, sukuriamas, kai sukuriama užduotis, į kurią įtrauktos visos reikiamos kainodaros dimensijos. Visus ne su pinigais susijusius laukus iš pardavimo įvertinimo eilutės į savikainos įvertinimo eilutę nukopijuoja sistema. Vaidmens ir organizacijos vienetai yra OOB PSA kainodaros matmenys, taikomi savikainos ir sąskaitų tarifams.                                                                                                                                                                                                                | Išlaidos             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Pasiūlymo eilutės informacijos ir sutarties eilutės informacijos objektų tinkinimas

Jei pridėjote pasirinktinį lauką pasiūlymo eilutės informacijos dalyje ir norite, kad sistema įvestų lauko vertę kaip numatytąją vertę susijusioje savikainos eilutėje, kurią sistema sukuria, naudokite priedų Preoperationkontraktlinedetailupdate ir Preoperationkotielinedetailupdate registracijos įrankius. Šie priedai turi būti iš naujo užregistruoti pakeitus pasiūlymo eilutės informaciją arba sutarties eilutės informaciją. Norėdami užbaigti sprendimus, atlikite toliau nurodytus veiksmus.

1. Atidarykite PluginRegistrationTool ir prisijunkite prie savo internetinio egzemplioriaus.
2. Pasirinkite **Ieškoti** ir ieškokite priedo, kurį norite naujinti.

    ![Paieška medžio dialogo lange](media/basic-guide-19.png)

3. Pasirinkite priedą, tada pagrindiniame puslapyje pasirinkite **Pasirinkti**.
4. Pasirinkite norimo naujinti priedo veiksmą, spustelėkite dešiniuoju pelės mygtuku ir pasirinkite **Naujinti**.

    ![Priedo veiksmo pasirinkimas](media/basic-guide-20.png)

5. Dialogo lango **Esamo veiksmo naujinimas** lauke **Filtravimo atributai** pasirinkite daugtaškio mygtuką (**...**):
 
    ![Dialogo langas Esamo veiksmo naujinimas](media/basic-guide-21.png)

6. Dialogo lange **Atributų pasirinkimas** pasirinkite pasirinktinių atributų žymės langelius.

    ![Dialogo langas Atributų pasirinkimas](media/basic-guide-22.png)

7. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą, tada pasirinkite **Veiksmo naujinimas**.
 
    ![Veiksmo naujinimo mygtukas](media/basic-guide-23.png)

8. Pakartokite 1–7 veiksmus ir su antru priedu.
9. Uždarykite PluginRegistrationTool.
