---
title: Kredito kortelių operacijų importavimas ir tvarkymas
description: Šioje temoje aiškinama, kaip importuoti ir prižiūrėti su išlaidomis susijusias kredito kortelių operacijas. Šias operacijas galima nustatyti taip, kad jos būtų automatiškai importuojamos pagal pasikartojantį grafiką, arba pagal poreikį jas galima importuoti neautomatiškai.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 6cec15e436bc699e361577c970dd5845c6c68908
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080989"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Kredito kortelių operacijų importavimas ir tvarkymas

[!include [banner](../includes/banner.md)]

Su išlaidomis susijusios kredito kortelių operacijos gali būti nustatytos taip, kad automatiškai būtų importuojamos pagal pasikartojantį grafiką. Arba operacijas galima importuoti neautomatiniu būdu, nes jos būtinos. Naudojant kredito kortelių operacijas duomenų objektas importuojamas.

Daugiau informacijos apie duomenų objektus žr. [Duomenų objektai](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

## <a name="import-credit-card-transactions"></a>Importuoti kredito kortelių operacijas

1. Puslapyje **Kredito kortelių operacijos** pažymėkite **Importavimo operacijos**. Jei pirmą kartą atidarote duomenų valdymą, sistema turi atnaujinti duomenų objektų sąrašą, kad galėtumėte tęsti.
2. Lauke **Pavadinimas** įveskite unikalų importavimo užduoties aprašą.
3. Lauke **Šaltinio duomenų formatas** pažymėkite failo, kuriame yra importuotos kredito kortelių operacijos, formatą.
4. Pažymėkite **Įkelti** , tada raskite ir pažymėkite failą, kurį norite importuoti.
5. Įkėlus failą, patikrinkite kredito kortelės operacijos failo susiejimą ir kredito kortelių operacijų duomenų įrašo stulpelius pasirinkdami plytelės saitą **Žiūrėti struktūrą**. Jei yra susiejimo klaidų, arba jei turite pakeisti susiejimą, pakeiskite susiejimą skirtuke **Susiejimo vizualizavimas** arba skirtuke **Susiejimo informacija**.
6. Norėdami automatizuoti kredito kortelių operacijas, pažymėkite **Kurti pasikartojančias duomenų užduotis**. Tada galite nustatyti pasikartojimą, apibrėžiantį, kaip dažnai reikia importuoti kreditinės kortelės operacijas. Baigę pasirinkite **Gerai**.
7. Jei norite importuoti pažymėtą failą dabar, pasirinkite **Importuoti**.
8. Jei importuojant įvyksta klaida, galite peržiūrėti vykdymo žurnalą arba sustojimo duomenis, kad pamatytumėte klaidas, kurias reikia pataisyti, kad būtų galima užtikrinti sėkmingą importavimą.

> [!NOTE]
> Jei turite importuoti daugiau nei vieną failo formatą, turite sukurti atskiras kiekvieno formato tipo importavimo užduotis.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Iš naujo priskirti nutrauktų darbuotojų kredito kortelių operacijas

Nutraukus darbuotojo įrašą, darbuotojo „Active Directory Domain Services“ (AD DS) abonementas išjungiamas. Tačiau gali būti aktyvios kredito kortelių operacijos, kurios turi būti apmokamos ir kompensuojamos. Puslapyje **Kreditinių kortelių operacijos** , galite iš naujo paskirti darbuotoją bet kuriai kredito kortelės operacijai, kai susijęs darbuotojas buvo nutrauktas.

Pažymėkite vieną arba kelias kredito kortelės operacijas, tada pažymėkite **Iš naujo priskirti operacijas**. Tada galite pasirinkti kitą darbuotoją, kad galėtumėte priskirti operacijas su kortelėmis. Iš naujo pristačius operacijas su kreditinėmis kortelėmis, jas galima pažymėti išlaidų ataskaitai ir apmokėtu įprastu išlaidų ataskaitos kompensavimo procesu.
