---
title: Projektu pagrįstų pasiūlymų kopijavimas
description: Šiame straipsnyje pateikta informacija apie tai, kaip kopijuoti projektu pagrįstus pasiūlymus programoje „Project Operations“.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6c3b964d89d6d24ae5d32dd9e5e79fcd1e90c19d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914918"
---
# <a name="copy-project-based-quotes"></a>Projektu pagrįstų pasiūlymų kopijavimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Galite lengvai sukurti naują projekto pasiūlymą nukopijuodami esamą. 

- Jei norite kopijuoti projekto pasiūlymą, puslapio **Projekto pasiūlymai** sąraše arba išsamios informacijos puslapyje **Projekto pasiūlymas** pažymėkite norimą kopijuoti projekto pasiūlymą, o tada pažymėkite **Kopijuoti**.

Taip atidarysite dialogo puslapį, kuriame galėsite įvesti kopijos parametrus. Šioje lentelėje išvardyti laukai, įtraukiami į dialogo puslapį. Atsižvelgiant į pažymėtas reikšmes, kopijavimo procesas gali pasikeisti.

| **Laukas** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- |
| Tema | Įveskite tikslinio pasiūlymo aktualią temą arba pavadinimą. Kai atidaromas dialogo langas, sistema nustatys šaltinio pasiūlymo temą su pridėtu tekstu **-kopija**. | |
| Potencialus klientas | Nurodo į kliento įmonę arba kliento įrašą. Kai atidaromas dialogo langas, sistema nustatys ją šaltinio pasiūlymo abonemente. | Šis laukas yra pirminis klientas pasiūlyme. |
| Sutartį sudarantis vienetas | Organizacijos vienetas, atsakingas už su šiuo sandėriu susijusių projektų pristatymą.
Kai atidaromas dialogo langas, sistema nustatys ją šaltinio pasiūlymo sutartį sudarančiu vienetu. | Sutartį sudarantis vienetas yra įmonės padalinys, kuris vykdys projektus po to, kai sandoris bus uždarytas. Kiekvienas sutartį sudarantis vienetas turi valiutą. Valiuta naudojama apskaičiuoti apytiksles ir faktines išlaidas, patirtas vykdant projektą. |
| Valiuta | Tai valiuta, kuria sudaromas sandėris. Kai atidaromas dialogo langas, sistema nustatys ją šaltinio pasiūlymo valiuta. Tai galima modifikuoti ir, jei tai pasikeis, laukas **Kopijavimo kainodara** visada nustatomas į **Ne**. Taip yra todėl, kad kainoraščiai šaltinio pasiūlyme nebeaktualūs. | Valiuta naudojama kainoraščiui nustatyti, kad būtų galima apskaičiuoti pasiūlymo finansinį įvertinimą ir galiausiai išrašyti sąskaitą faktūrą klientui, kai sandoris laimėtas. |
| Pageidaujama pristatymo data | Tai yra kliento pareikalauta pristatymo data. | Ji naudojama kaip pabaigos data kuriant sąskaitų faktūrų išrašymo datas pagal tam tikrą dažnumą. |
| Kopijavimo įkainiai | Taip / Ne reikšmė nurodo, ar pasiūlymo kainos turėtų būti kopijuojamos iš šaltinio pasiūlymo. | Jei pasirinkta **Taip**, projekto kainoraštis ir produktų kainoraščio nuorodos kopijuojamos iš šaltinio pasiūlymo į tikslinį pasiūlymą. Jei pasirinkta **Ne**, kainoraščiai iš naujo nustatomi pagal naujausius kainoraščius, nustatytus kliento arba projekto parametruose. |

Kai dialogo lango puslapyje pasirenkate **Gerai**, sistema sukuria projekto pasiūlymo kopiją pagal dialogo lange pažymėtus parametrus. Atidaromas naujas projekto pasiūlymas. 

> [!NOTE]
> Ši informacija nėra kopijuojama iš šaltinio į tikslinį pasiūlymą:
>
> - Sąskaitos faktūros grafikai
> - Pasiūlymo ir pasiūlymo eilutės klientai
> - Projekto nuoroda projekte – pagrįstos pasiūlymo eilutės – kliento biudžeto informacija
>
>Kadangi tai yra specifinė kiekvieno pasiūlymo informacija, šie laukai ir įrašai nebus kopijuojami. Pasiūlymo lygyje bus kopijuojamos projektų ir produktų pasiūlymo eilutės, pasiūlymo eilutės išsamios informacijos įvertinimai ir „Neviršyti“ reikšmės. Kaios ir išlaidų tarifų numatytosios reikšmės priklauso nuo parinkties **Kopijuoti įkainius**, pasirinktos dialogo lango puslapyje **Kopijuoti parametrus**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]