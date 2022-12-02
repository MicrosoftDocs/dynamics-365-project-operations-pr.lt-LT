---
title: Projektu pagrįstų sutarčių kopijavimas
description: Šiame straipsnyje pateikiama informacija apie projekto sutarčių kopijavimą programoje „Microsoft Dynamics 365 Project Operations“.
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
# <a name="copy-project-based-contracts"></a>Projektu pagrįstų sutarčių kopijavimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Galite lengvai sukurti naujas projekto sutartis, nukopijuodami esamas sutartis vienu iš dviejų būdu.

- Sąrašo puslapyje **Projekto sutartys** pasirinkite projekto sutartį, tada pasirinkite **Kopijuoti**.
- Informacijos puslapyje **Projekto sutartis** pasirinkite **Kopijuoti**.

Abiem atvejais atsidarys dialogo langas, kuriame galėsite nustatyti nukopijuotos sutarties parametrus. Į dialogo langą įtraukti toliau nurodyti laukai. Atsižvelgiant į pasirinktas reikšmes, kopijavimo procesas gali pasikeisti.

| Laukas | Aprašą | Tolesnis poveikis |
| --- | --- | --- |
| Tema | Įveskite paskirties sutarties temą. Kai atidaromas dialogo langas, sistema nustato šį lauką į šaltinio sutarties pavadinimą, bet pridedamas žodis „kopija“. | Nėra jokio tolesnio šio lauko poveikio. |
| kliente | Kliento įmonės arba kliento įrašo nuoroda. Kai atidaromas dialogo langas, sistema nustato šį lauką į šaltinio sutarties klientą. | Šis laukas yra pirminis klientas sutartyje. |
| Įmonė, kuriai priklauso | Įmonė, atsakinga už su šiuo sandoriu susijusių projektų pristatymą. Kai atidaromas dialogo langas, sistema nustato šį lauką į šaltinio sutarties valdomą įmonę. | Valdoma įmonė yra juridinis asmuo, kuris vykdys projektą, kai bus sudarytas sandoris. Valdomos įmonės valiuta turi sutapti su sutartį sudarančio vieneto valiuta. |
| Sutartį sudarantis vienetas | Organizacijos vienetas, atsakingas už su šiuo sandoriu susijusių projektų pristatymą. Kai atidaromas dialogo langas, sistema nustato šį lauką į šaltinio sutarties sutartį sudarantį vienetą. | Sutartį sudarantis vienetas yra įmonės padalinys, kuris vykdys projektus po to, kai sandoris bus uždarytas. Kiekvienas sutartį sudarantis vienetas turi valiutą. Ši valiuta naudojama apskaičiuoti apytiksles ir faktines išlaidas, patiriamas vykdant projektą. |
| Valiuta | Valiuta, kuria vykdoma operacija. Kai atidaromas dialogo langas, sistema nustato šį lauką į šaltinio sutarties valiutą. Valiutą galima keisti. Jei ji pakeista, lauko **Kopijuoti įkainius** reikšmė visada nustatomas kaip **Ne**, nes šaltinio sutarties kainoraščiai nebėra aktualūs. | Ši valiuta naudojama numatytajam kainoraščiui nustatyti, kad būtų galima apskaičiuoti sutarties finansinį įvertinimą ir išrašyti sąskaitą faktūrą klientui, kai sandoris bus laimėtas. |
| Pageidaujama pristatymo data | Kliento prašyta pristatymo data. | Ši data naudojama kaip pabaigos data, kuriant sąskaitų faktūrų išrašymo datas pagal tam tikrą dažnumą. |
| Kopijuoti įkainius | Reikšmė, nurodanti, ar sutarties įkainiai turėtų būti nukopijuoti iš šaltinio sutarties. | Jei laukas nustatytas kaip **Taip**, projekto ir produktų kainoraščio nuorodos nukopijuojamos iš šaltinio sutarties į paskirties sutartį. Jei nustatyta kaip **Ne**, numatytieji kainoraščiai naudojami pagal naujausius kainoraščius, nustatytus kliento arba projekto parametruose. |

Kai dialogo lange pasirenkate **Gerai**, sistema sukuria sutarties kopiją pagal nustatytas parametrų reikšmes. Tada atidaroma nauja sutartis.

Ši informacija iš šaltinio sutarties į paskirties sutartį **nekopijuojama**, nes ji specifinė kiekvienai sutarčiai:

- Sąskaitos faktūros grafikai
- Sutarties ir sutarties eilutės klientai
- Projekto nuoroda projektais pagrįstos sutarties eilutėse
- Kliento biudžeto informacija

Sutarties lygyje bus kopijuojamos projektų ir produktų sutarties eilutės, sutarties eilutės informacijoje esantys įvertinimai ir „Neviršyti“ reikšmės. Numatytųjų kainų ir savikainos tarifų įrašai priklauso nuo lauko **Kopijuoti įkainius**, esančio dialogo lange **Kopijuoti parametrus**, pasirinkimo.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
