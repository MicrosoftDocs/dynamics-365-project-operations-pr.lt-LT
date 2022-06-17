---
title: Kas nauja arba pakeista „Project Service Automation“ V3 36 atnaujintame leidime
description: Šiame straipsnyje išvardijamos funkcijos ir taisymai, kuriuos galima rasti 36 naujinimo leidime Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: a8942713109075da2503c9d22d40b6ac95ae00be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924992"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 36 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Ji suderinama su „Dynamics 365 9.x“. Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šiame straipsnyje išvardijamos naujos arba pakeistos "Project Service Automation Update Release 36, V3" funkcijos ir taisymai. Ši versija turi naują komponavimo versijos numerį V3.10.57.152 ir ją galima pasiekti per 2021 m. spalio mėn. automatinį naujinimą.

## <a name="update-release-36"></a>36 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

Buvo pataisytos tolesnės problemos.

**Bendroji informacija**
- Lauko **Numatytasis darbo valandų šablonas** pavadinimas neteisingai išverstas puslapyje **Projekto parametrai**.
- Asinchroniniai priedai netinkamai tvarko išimtis, susijusias su **SharedVariableService**.

**Laikas ir išlaidos**
- Kai trūksta žurnalo eilučių arba vartotojas neturi tinkamų teisių jas skaityti, atšaukus projektų patvirtinimus įvyksta netinkama klaida.
- Vartotojai negali atšaukti patvirtinimo, kai išlaidų arba laiko įrašas turi daugiau nei vieną susietą projekto patvirtinimą.
- **Neatvykimas** ir **Atostogos** netinkamai išversta į kinų kalbą **Laiko įrašo** greito kūrimo puslapio peržvalgoje.

**Išteklių valdymas**
- Vartotojas negali ieškoti išteklių **Planavimo pagalbinėje priemonėje**, kai rodinio režimas nustatytas į **Diena**, **Savaitė** arba **Mėnuo**.
- Bendruose ištekliuose neteisingai leidžiama palikti tuščius pozicijų pavadinimus. 
- Sutarties (kaip prarastos) uždarymas neatšaukia ateities rezervacijų.

**Pardavimas**
- Kai aplinkoje yra didelis produktų kiekis, sumažėja našumas **Medžiagų įvertinimo** tinklelyje.
- Kai projektą kuriate iš šablono, projekto valiuta pagal numatytuosius nustatymus nėra nustatoma į atitinkamą projekto vadovo sutarties vienetą.
- Faktinės sumos ne visada atitinka tai, kas yra vykdomame projekte, arba sumos tampa neigiamos konkrečiuose atšaukimo scenarijuose.
- Klaida įvyksta, kai projektą, sukurtą iš projekto šablono, susiejate su sutarties eilute.
- Vartotojai gali panaikinti sutarties eilutę su etapais **Parengta išrašyti sąskaitą faktūrą** ir **Sukurta sąskaita faktūra**. Tai neturėtų būti leidžiama.
- Kai įvertinimai importuojami iš projekto, pasiūlymo eilutės išsamus apmokestinimas nustatomas neteisingai, kai įgalinamas užduotimis pagrįstas pasiūlymo eilutės sąskaitos išrašymas.
- Kai įtraukiate fiksuotos kainos sąskaitos išrašymo etapą, etapas neatspindimas etapo papildomame tinklelyje, kol neatnaujinamas puslapis.
- Sugeneruojama neapibrėžta nuorodos išimtis, kai sukuriate projekto sutartį su neapibrėžtu pasiūlymo pavadinimu.
- Rankinio režimo užduotys, kai projekto valiuta skiriasi nuo ištekliaus valiutos, lemia neteisingą kainos įvertinimą.
- Vartotojai negali atšaukti operacijos, kuri sėkmingai pataisyta taisomąja sąskaita faktūra.
- Išjungtos operacijų kategorijos rodomos **Išlaidų įvertinimo** tinklelyje.



