---
title: Laiko įrašų kūrimas
description: Šioje temoje pateikiama informacija apie tai, kaip kurti laiko įrašus.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 4b8f88da372cd56b19bed82ad6918da6ddd6f202
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593530"
---
# <a name="create-time-entries"></a>Laiko įrašų kūrimas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ankstesnėse Dynamics 365 Project Service Automation versijose laiko įrašai buvo įvedami kas savaitę. „Project Service Automation“ 3 versijoje laiko įrašai įvedami kasdien. Tačiau sukūrus kelis laiko įrašus, galite atlikti masinį kūrimą arba juos kopijuoti.

## <a name="create-a-time-entry"></a>Laiko įrašo kūrimas

Norėdami sukurti laiko įrašą, atlikite toliau nurodytus veiksmus.

1. Puslapyje **Laiko įrašai** pasirinkite **Naujas**.
2. Dialogo lange **Spartusis kūrimas: laiko įrašas** įveskite laiko įrašo trukmę minutėmis, valandomis arba dienomis. Trukmę įveskite šiuo formatu: *x* minutės, *x* valandos arba *x* dienos. Valandas ir dienas taip pat galite įvesti naudodami dešimtaines reikšmes, pavyzdžiui, *x.x* valandos arba *x.x* dienos.
3. Pažymėkite laiko įrašo tipą ir projektą, kuriam įvedate laiko įrašą.
4. Lauke **Projekto užduotis** raskite šio laiko įrašo užduotį.

    > [!NOTE]
    > Jei kuriate laiko įrašą užduočiai, kuri nėra priskirta naudotojui, lauke **Projekto užduotis** pažymėkite mygtuką **Ieškoti**, pažymėkite **Keisti rodinį**, tada pažymėkite **Visos aktyvios projekto užduotus**, kad sudarytumėte visų užduočių sąrašą.

5. Įveskite parašymą, jei jo reikia, tada pasirinkite **Įrašyti ir uždaryti**.

Sukūrę ir įrašę laiko įrašą, galite redaguoti jį laiko įrašų tinklelyje. Laiko įrašų tinklelis palaiko du formatus:

- Galite įvesti laiko įrašus formatu **hh: mm**. Tada šis formatas konvertuojamas į valandas ir trupmenas.
- Galite tiesiogiai įvesti valandas ir trupmenas.

Atkreipkite dėmesį, kad valandos trupmena nėra minutės. Todėl 1,5 valandos atitinka 1 valandą ir 30 minučių. Ta pati taisyklė taikoma dienos trupmenoms. Viena diena yra 24 valandos, o 0,5 dienos yra 12 valandų.

## <a name="bulk-create-time-entries"></a>Masinis laiko įrašų kūrimas

Sukūrus kelis laiko įrašus, galite juos nukopijuoti, kad sukurtumėte didelį kiekį papildomų laiko įrašų.

1. Puslapyje **Laiko įrašai** pasirinkite **Kopijuoti savaitę**.
2. Laukų grupėje **Nuo laikotarpio** laukuose **Pradžios data** ir **Pabaigos data** apibrėžkite datų intervalą, iš kurio kopijuosite laiko įrašus.
3. Laukų grupėje **Iki laikotarpio** lauke **Pradžios data** nurodykite datą, kuriai kurti laiko įrašus.
4. Pažymėkite **Kopijuoti**, kad sukurtumėte laiko įrašų, kurie atitinka savaitės dieną, kuri nurodyta laukų grupėje **Iki laikotarpio**, kopiją. Pavyzdžiui, praeitos savaitės pirmadienio laiko įrašas yra nukopijuojamas į savaitės, kuri nurodytą laukų grupėje **Iki periodo**, pirmadienį.

## <a name="import-data-for-time-entries"></a>Duomenų importavimas laiko įrašams

Galite importuoti duomenis iš projekto rezervacijų ir priskyrimų. Importuodami duomenis galite nurodyti importuotinų rezervacijų datų intervalą, tada konkrečiai pasirinkti rezervacijas, kurios turėtų būti sukurtos kaip laiko įrašų **Juodraštis**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Grupavimo pagal, rūšiavimo, ieškos ir filtravimo galimybės

Galite grupuoti ir filtruoti laiko įrašus pagal dimensijas, nurodytas stulpeliuose. Lauke **Grupuoti pagal** pažymėkite dimensiją, kurią norite naudoti laiko įrašams filtruoti. Taip pat galite rikiuoti laiko įrašus didėjimo arba mažėjimo tvarka naudodami stulpelių antraščių rūšiavimo rodyklę. Be to, galite rodyti arba slėpti įrašus pažymėdami mygtuką **Filtras** stulpelių antraštėse, tada dialogo lange **Ieška** įvesdami tekstą, kuris turi būti naudojamas laiko įrašų ieškai pagal projekto pavadinimą, projekto užduotį, laiko įrašą arba išteklius.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
