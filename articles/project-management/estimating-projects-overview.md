---
title: Finansinio įvertinimo sąvokos
description: Šiame straipsnyje pateikiama informacija apie projekto operacijų projektų finansines sąmatas.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f8a4c3dd31cf5612c352331891178ac0ab852921
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931018"
---
# <a name="financial-estimation-concepts"></a>Finansinio įvertinimo sąvokos

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ savo projektus galite finansiškai įvertinti dviem toliau nurodytais etapais. 
1. Etape prieš parduodant, kai sandoris dar nėra laimėtas. 
2. Vykdymo etapo metu, sukūrus projekto sutartį. 

Sukurti projektu pagrįsto darbo finansinį įvertinimą galite pasinaudodami bet kuriais iš toliau nurodytų 3 puslapių.
- Puslapyje **Pasiūlymo eilutė**, pasinaudodami pasiūlymo eilutės informacija.  
- Puslapyje **Projekto sutarties eilutė**, pasinaudodami sutarties eilutės informacija. 
- Puslapyje **Projektas**, pasinaudojami skirtuko **Užduotys** arba **Išlaidų įvertinimai** puslapiais.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Projekto pasiūlymo naudojimas įvertinimui sukurti
Projektu pagrįstame pasiūlyme galite naudoti objektą **Pasiūlymo eilutės informacija** ir įvertinti reikiamo pristatyti darbo dydį. Tada galite bendrinti įvertinimą su klientu.

Projektu pagrįstose pasiūlymo eilutėse gali nebūti jokios arba daug pasiūlymo eilutės informacijos. Pasiūlymo eilutės informacija naudojama norint apskaičiuoti laiką, išlaidas arba mokesčius. „Microsoft Dynamics 365 Project Operations“ programoje negalima atlikti medžiagų įvertinimo pagal pasiūlymo eilutės išsamią informaciją. Tai vadinama operacijų klasėmis. Įvertintas mokesčių sumas taip pat galima įvesti operacijos klasėje.

Be operacijų klasių pasiūlymo eilutės informacijos dalyje taip pat nurodomas operacijos tipas. Palaikomi du pasiūlymo eilutės informacijos operacijų tipai: **Savikainos** ir **Projekto sutarties**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Projekto sutarties naudojimas įvertinimui sukurti

Jei kurdami projektu pagrįstą sutartį naudojote pasiūlymą, kiekvieno pasiūlymo eilutės įvertinimas nukopijuojamas į projekto sutartį. Projekto sutarties struktūra yra tokia pati, kaip ir projekto pasiūlymo: pateikiamos eilutės, eilučių informacija ir sąskaitų faktūrų grafikai.

Įvertinimus galima atlikti tiesiogiai projekto sutartyje, pvz., projekto pasiūlymo dalyje. Projekto pasiūlymo įvertinimas atliekamas naudojant sutarties eilutes ir sutarties eilutės informaciją. Sutarties eilutės informaciją taip pat galima sugeneruoti pagal projekto planą, sukurtą naudojant metodą „iš apačios į viršų“.

Sutarties eilutės informaciją galima panaudoti norint apskaičiuoti laiką, išlaidas arba mokesčius. Įvertintas mokesčių sumas taip pat galima įvesti sutarties eilutės informacijos dalyje.

Medžiagos įvertinimai negalimi sutarties eilutės informacijai.

## <a name="use-a-project-to-create-an-estimate"></a>Projekto naudojimas įvertinimui sukurti 

Galite įvertinti darbo su projektais laiką ir išlaidas. „Project Operations“ nepalaikomi projektų medžiagų ar mokesčių įvertinimai.

Laiko įvertinimai generuojami kuriant užduotį ir nurodant bendrojo ištekliaus, kuris reikalingas norint atlikti užduotį, atributus. Laiko įvertinimai generuojami pagal suplanuotas užduotis. Laiko įvertinimai nekuriami, jei bendruosius komandos narius kuriate atskirai nuo grafiko.

Išlaidų įvertinimus galima įvesti puslapio **Išlaidų įvertinimai** tinklelyje.

Projekto įvertinimo kūrimas laikomas geriausia praktika, nes galite sukurti kiekvienos projekto plano užduoties darbo arba laiko ir išlaidų nuo smulkmenų prie bendrųjų principų vedančius įvertinimus. Tada šį išsamų įvertinimą galite naudoti norėdami sukurti kiekvienos pasiūlymo eilutės įvertinimą ir patikimesnį kliento pasiūlymą. Kai išsamų įvertinimą importuojate arba sukuriate pasiūlymo eilutėje naudodami projekto planą, į „Project Operations“ importuojamos šių įvertinimų pardavimo ir savikainos reikšmės. Importavę projekto pasiūlyme galite peržiūrėti pelningumo, maržų ir ekonominio pagrįstumo metriką.

## <a name="understanding-estimates"></a>Įvertinimų paaiškinimas

Naudokite šią lentelę kaip vadovą, kad suprastumėte verslo logiką, naudojamą vertinant.

| Scenarijus                                                                                                                                                                                                                                                                                                                                          | Objekto įrašas                                                                                                                                                                                                       | Operacijos tipas | Operacijos klasė | Papildoma informacija                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Kai reikia apskaičiuoti pasiūlymo laiko pardavimo vertę                                                                                                                                                                                                                                                                                    | Sukuriamas pasiūlymo eilutės informacijos (QLD) įrašas                                                                                                                                                                               | Projekto sutartis | Time        | Operacijos kilmės lauko iš pardavimo pusės QLD eilutė nurodo į savikainos pusės QLD |
|                                                                                                                                                                                                                                                                                     | Antrą QLD įrašą sukuria sistema, kad būtų išsaugotos atitinkamos savikainos vertės. Visus ne su pinigais susijusius laukus iš pardavimo QLD į savikainos QLD nukopijuoja sistema.                                                                                                                                                                               | Išlaidos | Time        | Operacijos kilmės lauko iš pardavimo pusės pasiūlymo kainos informacijos (QLD) eilutė nurodo į savikainos pusės QLD |
| Kai reikia apskaičiuoti sutarties laiko pardavimo vertę                                                                                                                                                                                                                                                                                 | Sukuriamas pasiūlymo sutarties eilutės informacijos (CLD) įrašas                                                                                                                                                                    | Projekto sutartis | Time        | Operacijos kilmės lauko iš pardavimo pusės CLD eilutė nurodo į savikainos CLD      |
|                                                                                                                                                                                                                                                                                  | Antrą CLD įrašą sukuria sistema, kad būtų išsaugotos atitinkamos savikainos vertės. Visus ne su pinigais susijusius laukus iš pardavimo CLD į savikainos CLD nukopijuoja sistema.                                                                                                                                                                    | Išlaidos | Time        | Operacijos kilmės lauko iš pardavimo pusės CLD eilutė nurodo į savikainos CLD      |
| Kai vartotojas aprašo išteklių projekto užduoties lauke                                                                                                                                                                                                                                                                                            | Įvertinimo eilutės įrašas, skirtas užduoties pardavimo vertei rodyti, sukuriamas, kai sukuriama užduotis, į kurią įtrauktos visos reikiamos kainodaros dimensijos. Vaidmens ir organizacijos vienetai yra kainodaros dimensijos | Projekto sutartis | Laikas        |                                                                                   |
|     | Įvertinimo eilutės įrašas, skirtas užduoties savikainos vertei rodyti, sukuriamas, kai sukuriama užduotis, į kurią įtrauktos visos reikiamos kainodaros dimensijos. Visus ne su pinigais susijusius laukus iš pardavimo įvertinimo eilutės į savikainos įvertinimo eilutę nukopijuoja sistema. Vaidmens ir organizacijos vienetai yra kainodaros matmenys, taikomi savikainos ir sąskaitų tarifams.                                                                                                                                                                                                                | Savikaina             | Laikas           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Pasiūlymo eilutės informacijos ir sutarties eilutės informacijos objektų tinkinimas

Jei pridėjote pasirinktinį lauką pasiūlymo eilutės informacijos dalyje ir norite, kad sistema įvestų lauko vertę kaip numatytąją vertę susijusioje savikainos eilutėje, kurią sistema sukuria, naudokite priedo registracijos įrankius **PreOperationContractLineDetailUpdate** ir **PreOperationQuoteLineDetailUpdate**. Šie priedai turi būti iš naujo užregistruoti pakeitus pasiūlymo eilutės informaciją arba sutarties eilutės informaciją. Norėdami užbaigti sprendimus, atlikite toliau nurodytus veiksmus.

1. Atidarykite PluginRegistrationTool ir prisijunkite prie savo internetinio egzemplioriaus.
2. Pasirinkite **Ieškoti** ir ieškokite priedo, kurį norite naujinti.
3. Pasirinkite priedą, tada pagrindiniame puslapyje pasirinkite **Pasirinkti**.
4. Pasirinkite norimo naujinti priedo veiksmą, spustelėkite dešiniuoju pelės mygtuku ir pasirinkite **Naujinti**.
5. Dialogo lango **Esamo veiksmo naujinimas** lauke **Filtravimo atributai** pasirinkite daugtaškio mygtuką (**...**):
6. Dialogo lange **Atributų pasirinkimas** pasirinkite pasirinktinių atributų žymės langelius.
7. Pasirinkite **Gerai**, kad uždarytumėte dialogo langą, tada pasirinkite **Veiksmo naujinimas**.
8. Pakartokite 1–7 veiksmus ir su antru priedu.
9. Uždarykite **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
