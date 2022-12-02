---
title: Projekto sutarčių kopijavimas
description: Šiame straipsnyje pateikiama informacija apie projekto sutarčių kopijavimą programoje „Dynamics Project Operations“.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8fa17bbd5738e4bc6330c728a3418a2be6828eef
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410070"
---
# <a name="copy-project-contracts"></a>Projekto sutarčių kopijavimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Galite lengvai sukurti naujas projekto sutartis, padarydami esamų sutarčių kopijas vienu iš dviejų būdu. 

  - Sąrašo puslapyje **Projekto sutartys** pasirinkite projekto sutartį ir pasirinkite **Kopijuoti**.
  - Informacijos puslapyje **Projekto sutartis** pasirinkite **Kopijuoti**.

Atsidarys dialogo lango puslapis, kuriame galėsite pasirinkti sutarties kopijos parametrus. Į dialogo langą įtraukti toliau nurodyti laukai. Atsižvelgiant į šiame dialogo lange pasirinktas reikšmes, kopijavimo procesas gali pasikeisti.

| **Laukas** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- |
| Tema | Įveskite paskirties sutarties temą. Kai atidaromas dialogo lango puslapis, sistema nustatys šį lauką į šaltinio sutarties pavadinimą su pridėtu tekstu **kopija**. | Nėra jokio tolesnio šio lauko poveikio. |
| Klientas | Nurodo į kliento įmonę arba kliento įrašą. Kai atidaromas dialogo langas, sistema nustatys šį lauką į šaltinio sutarties klientą. | Šis laukas yra pirminis klientas sutartyje. |
| Sutartį sudarantis vienetas | Organizacijos vienetas, atsakingas už su šiuo sandėriu susijusių projektų pristatymą. Kai atidaromas dialogo lango puslapis, sistema nustatys ją šaltinio sutartį sudarančiu vienetu. | Sutartį sudarantis vienetas yra įmonės padalinys, kuris vykdys projektus po to, kai sandoris bus uždarytas. Kiekvienas sutartį sudarantis vienetas turi valiutą. Ši valiuta naudojama apskaičiuoti apytiksles ir faktines išlaidas, patirtas vykdant projektą. |
| Valiuta | Valiuta, kuria vykdoma operacija. Kai atidaromas dialogo lango puslapis, sistema nustatys lauką į šaltinio sutarties valiutą. Valiutą galima keisti. Jei ji pakeista, laukas **Kopijuoti kainodarą** visada nustatomas į parinktį **Ne**, nes šaltinio sutarties kainoraščiai nebėra aktualūs. | Valiuta naudojama numatytajam kainoraščiui nustatyti, kad būtų galima apskaičiuoti sutarties finansinį įvertinimą ir išrašyti sąskaitą faktūrą klientui, kai sandoris laimėtas. |
| Pageidaujama pristatymo data | Kliento prašyta pristatymo data. | Ši data naudojama kaip pabaigos data kuriant sąskaitų faktūrų išrašymo datas pagal tam tikrą dažnumą. |
| Kopijavimo įkainiai | Nurodo, ar sutarties kainos turėtų būti kopijuojamos iš šaltinio sutarties. | Jei laukas nustatytas į parinktį **Taip**, projekto ir produktų kainoraščio nuorodos kopijuojamos iš šaltinio sutarties į paskirties sutartį. Jei pasirinkta **Ne**, numatytieji kainoraščiai nustatomi pagal naujausius kainoraščius, nustatytus kliento arba projekto parametruose. |

Kai dialogo lango puslapyje pasirenkate **Gerai**, sistema sukuria sutarties kopiją pagal pažymėtus parametrus. Atidaroma nauja sutartis.

Ši informacija nėra kopijuojama iš **šaltinio** į **paskirties pasiūlymą**.

  - Sąskaitos faktūros grafikai
  - Sutarties ir sutarties eilutės klientai
  - Projekto nuoroda projektais pagrįstos sutarties eilutėse
  - Kliento biudžeto informacija

Kadangi tai yra specifinė kiekvienos sutarties informacija, šie laukai ir įrašai nebus kopijuojami. Sutarties lygyje bus kopijuojamos projektų ir produktų sutarties eilutės, sutarties eilutės informacijos įvertinimai ir „Neviršyti“ reikšmės. Kainos ir išlaidų tarifų numatytosios reikšmės priklauso lauko **Kopijuoti įkainius**, esančio dialogo lango puslapyje **Kopijuoti parametrus**, pasirinkimo.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
