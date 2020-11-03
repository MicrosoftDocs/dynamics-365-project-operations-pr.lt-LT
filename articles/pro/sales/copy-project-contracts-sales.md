---
title: Projekto sutarčių kopijavimas
description: Šioje temoje pateikiama informacija apie projekto sutarčių kopijavimą programoje „Dynamics Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6da8e3ba8e062f3e06dc7f440caebdd93e496c65
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080741"
---
# <a name="copying-project-contracts"></a>Projekto sutarčių kopijavimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Galite lengvai sukurti naujas projekto sutartis, padarydami esamų sutarčių kopijas vienu iš dviejų būdu. 

  - Sąrašo puslapyje **Projekto sutartys** pasirinkite projekto sutartį ir pasirinkite **Kopijuoti**.
  - Informacijos puslapyje **Projekto sutartis** pasirinkite **Kopijuoti**.

Atsidarys dialogo lango puslapis, kuriame galėsite pasirinkti sutarties kopijos parametrus. Į dialogo langą įtraukti toliau nurodyti laukai. Atsižvelgiant į šiame dialogo lange pasirinktas reikšmes, kopijavimo procesas gali pasikeisti.

| **Laukas** | **Atitiktis, tikslas ir gairės** | **Tolesnis poveikis** |
| --- | --- | --- |
| Tema | Įveskite paskirties sutarties temą. Kai atidaromas dialogo lango puslapis, sistema nustatys šį lauką į šaltinio sutarties pavadinimą su pridėtu tekstu **kopija**. | Nėra jokio tolesnio šio lauko poveikio. |
| Klientas | Nurodo į kliento įmonę arba kliento įrašą. Kai atidaromas dialogo langas, sistema nustatys šį lauką į šaltinio sutarties klientą. | Šis laukas yra pirminis klientas sutartyje. |
| Sutartį sudarantis vienetas | Organizacijos vienetas, atsakingas už su šiuo sandėriu susijusių projektų pristatymą. Kai atidaromas dialogo lango puslapis, sistema nustatys ją šaltinio sutartį sudarančiu vienetu. | Sutartį sudarantis vienetas yra įmonės padalinys, kuris vykdys projektus po to, kai sandoris bus uždarytas. Kiekvienas sutartį sudarantis vienetas turi valiutą. Ši valiuta naudojama apskaičiuoti apytiksles ir faktines išlaidas, patirtas vykdant projektą. |
| Valiuta | Valiuta, kuria vykdoma operacija. Kai atidaromas dialogo lango puslapis, sistema nustatys lauką į šaltinio sutarties valiutą. Valiutą galima keisti. Jei ji pakeista, laukas **Kopijuoti kainodarą** visada nustatomas į parinktį **Ne** , nes šaltinio sutarties kainoraščiai nebėra aktualūs. | Valiuta naudojama numatytajam kainoraščiui nustatyti, kad būtų galima apskaičiuoti sutarties finansinį įvertinimą ir išrašyti sąskaitą faktūrą klientui, kai sandoris laimėtas. |
| Pageidaujama pristatymo data | Kliento prašyta pristatymo data. | Ši data naudojama kaip pabaigos data kuriant sąskaitų faktūrų išrašymo datas pagal tam tikrą dažnumą. |
| Kopijavimo įkainiai | Nurodo, ar sutarties kainos turėtų būti kopijuojamos iš šaltinio sutarties. | Jei laukas nustatytas į parinktį **Taip** , projekto ir produktų kainoraščio nuorodos kopijuojamos iš šaltinio sutarties į paskirties sutartį. Jei pasirinkta **Ne** , numatytieji kainoraščiai nustatomi pagal naujausius kainoraščius, nustatytus kliento arba projekto parametruose. |

Kai dialogo lango puslapyje pasirenkate **Gerai** , sistema sukuria sutarties kopiją pagal pažymėtus parametrus. Atidaroma nauja sutartis.

Ši informacija nėra kopijuojama iš **šaltinio** į **paskirties pasiūlymą**.

  - Sąskaitos faktūros grafikai
  - Sutarties ir sutarties eilutės klientai
  - Projekto nuoroda projektais pagrįstos sutarties eilutėse
  - Kliento biudžeto informacija

Kadangi tai yra specifinė kiekvienos sutarties informacija, šie laukai ir įrašai nebus kopijuojami. Sutarties lygyje bus kopijuojamos projektų ir produktų sutarties eilutės, sutarties eilutės informacijos įvertinimai ir „Neviršyti“ reikšmės. Kainos ir išlaidų tarifų numatytosios reikšmės priklauso lauko **Kopijuoti įkainius** , esančio dialogo lango puslapyje **Kopijuoti parametrus** , pasirinkimo.
