---
title: Projektinių sutarčių kopijavimas
description: Šiame straipsnyje pateikiama informacija apie projekto sutarčių kopijavimą programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410374"
---
# <a name="copy-project-based-contracts"></a>Projektinių sutarčių kopijavimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Galite lengvai kurti naujas projekto sutartis kopijuodami esamas sutartis vienu iš dviejų būdų:

- **Puslapyje Projekto sutartys** pasirinkite projekto sutartį, tada pasirinkite **Kopijuoti**.
- Informacijos puslapyje **Projekto sutartis** pasirinkite **Kopijuoti**.

Abiem atvejais pasirodo dialogo langas, kuriame galite nustatyti nukopijuotos sutarties parametrus. Dialogo lange yra šie laukai. Atsižvelgiant į pasirinktas reikšmes, kopijavimo procesas gali keistis.

| Laukas | Aprašą | Tolesnis poveikis |
| --- | --- | --- |
| Tema | Įveskite paskirties sutarties temą. Atidarius dialogo langą, sistema nustato lauką į šaltinio sutarties pavadinimą, tačiau prie jo pridedamas žodis "kopijuoti". | Nėra jokio tolesnio šio lauko poveikio. |
| kliente | Kliento įmonės arba kliento įrašo nuoroda. Atidarius dialogo langą, sistema nustato lauką į šaltinio sutarties paskyrą. | Šis laukas yra pirminis klientas sutartyje. |
| Įmonė, kuriai priklauso | Įmonė, atsakinga už projektų, susijusių su šiuo sandoriu, pristatymą. Atidarius dialogo langą, sistema nustato lauką į šaltinio sutartį valdančią įmonę. | Valdančioji įmonė yra juridinis asmuo, kuris vykdys projektą po to, kai sandoris bus uždarytas. Valdančios bendrovės valiuta turi atitikti sutartinio vieneto valiutą. |
| Sutartį sudarantis vienetas | Organizacijos padalinys, atsakingas už projektų, susijusių su šiuo sandoriu, pristatymą. Atidarius dialogo langą, sistema nustato lauką į šaltinio sutarties sudarymo vienetą. | Sutartį sudarantis vienetas yra įmonės padalinys, kuris vykdys projektus po to, kai sandoris bus uždarytas. Kiekvienas sutartį sudarantis vienetas turi valiutą. Ši valiuta naudojama pranešant apie apskaičiuotas ir faktines išlaidas, patirtas projekto metu. |
| Valiuta | Valiuta, kuria vykdoma operacija. Atidarius dialogo langą, sistema nustato lauką į šaltinio sutarties valiutą. Valiutą galima keisti. Jei taip, laukas **Kopijuoti kainodarą** visada nustatomas kaip **Ne**, nes kainoraščiai šaltinio sutartyje nebėra aktualūs. | Ši valiuta naudojama numatytiesiems kainoraščiams, finansiniams sutarties įverčiams generuoti ir klientui išrašyti sąskaitą faktūrą, kai sandoris laimimas. |
| Pageidaujama pristatymo data | Pristatymo data, kurios prašo klientas. | Ši data naudojama kaip pabaigos data, kai tam tikru dažnumu kuriate sąskaitų faktūrų išrašymo datas. |
| Kopijavimo įkainiai | Vertė, nurodanti, ar sutartyje nustatyta kainodara turėtų būti nukopijuota iš šaltinio sutarties. | Jei laukas nustatytas kaip **Taip**, projekto ir produkto kainoraščio nuorodos nukopijuojamos iš šaltinio sutarties į tikslinę sutartį. Jei jis nustatytas kaip **Ne**, naudojami numatytieji kainoraščiai, pagrįsti naujausiais kainoraščiais paskyroje arba projekto parametruose. |

Kai dialogo lange pasirenkate **Gerai**, sistema sukuria sutarties kopiją pagal jūsų nustatytas parametrų reikšmes. Tada atidaroma nauja sutartis.

Ši informacija **nėra** nukopijuojama iš šaltinio sutarties į tikslinę sutartį, nes ji būdinga kiekvienai sutarčiai:

- Sąskaitos faktūros grafikai
- Sutarties ir sutarties eilutės klientai
- Projekto nuoroda projektais pagrįstos sutarties eilutėse
- Kliento biudžeto informacija

Kopijuojamos projektų ir produktų sutarčių eilutės, sutarčių eilučių duomenyse pateikti įvertinimai ir sutarčių lygio vertės, kurių vertė neviršijama. Numatytųjų kainų ir išlaidų tarifų įvedimas priklauso nuo pasirinkimo, esančio **dialogo lango Kopijuoti parametrus** lauke Kopijuoti **kainodarą**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
