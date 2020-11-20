---
title: Kredito kortelės integravimo nustatymas
description: Šioje temoje aiškinama, kaip importuoti ir prižiūrėti su išlaidomis susijusias kredito kortelių operacijas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e0004f9096ea8a03745dbfce35fe0d32d3d707f6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120868"
---
# <a name="set-up-credit-card-integration"></a>Kredito kortelės integravimo nustatymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Su išlaidomis susijusios kredito kortelių operacijos gali būti nustatytos taip, kad automatiškai būtų importuojamos pagal pasikartojantį grafiką. Arba operacijas galima importuoti neautomatiniu būdu, nes jos būtinos. Naudojant kredito kortelių operacijas duomenų objektas importuojamas.

## <a name="import-credit-card-transactions"></a>Importuoti kredito kortelių operacijas

1. Puslapyje **Kredito kortelių operacijos** pažymėkite **Importavimo operacijos**. Jei pirmą kartą atidarote duomenų valdymą, sistema turi atnaujinti duomenų objektų sąrašą, kad galėtumėte tęsti.
2. Lauke **Pavadinimas** įveskite unikalų importavimo užduoties aprašą.
3. Lauke **Šaltinio duomenų formatas** pažymėkite failo, kuriame yra importuotos kredito kortelių operacijos, formatą.
4. Pažymėkite **Įkelti**, tada raskite ir pažymėkite failą, kurį norite importuoti.
5. Įkėlus failą, patikrinkite kredito kortelės operacijos failo susiejimą ir kredito kortelių operacijų duomenų įrašo stulpelius pasirinkdami plytelės saitą **Žiūrėti struktūrą**. Jei yra susiejimo klaidų, arba jei turite pakeisti susiejimą, pakeiskite susiejimą skirtuke **Susiejimo vizualizavimas** arba skirtuke **Susiejimo informacija**.
6. Norėdami automatizuoti kredito kortelių operacijas, pažymėkite **Kurti pasikartojančias duomenų užduotis**. Tada galite nustatyti pasikartojimą, apibrėžiantį, kaip dažnai reikia importuoti kreditinės kortelės operacijas. Baigę pasirinkite **Gerai**.
7. Jei norite importuoti pažymėtą failą dabar, pasirinkite **Importuoti**.
8. Jei importuojant įvyksta klaida, galite peržiūrėti vykdymo žurnalą arba sustojimo duomenis, kad pamatytumėte klaidas, kurias reikia pataisyti, kad būtų galima užtikrinti sėkmingą importavimą.

> [!NOTE]
> Jei turite importuoti daugiau nei vieną failo formatą, turite sukurti atskiras kiekvieno formato tipo importavimo užduotis.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Iš naujo priskirti nutrauktų darbuotojų kredito kortelių operacijas

Nutraukus darbuotojo įrašą, darbuotojo „Active Directory Domain Services“ (AD DS) abonementas išjungiamas. Tačiau gali būti aktyvios kredito kortelių operacijos, kurios turi būti apmokamos ir kompensuojamos. Puslapyje **Kreditinių kortelių operacijos**, galite iš naujo paskirti darbuotoją bet kuriai kredito kortelės operacijai, kai susijęs darbuotojas buvo nutrauktas.

Pažymėkite vieną arba kelias kredito kortelės operacijas, tada pažymėkite **Iš naujo priskirti operacijas**. Tada galite pasirinkti kitą darbuotoją, kad galėtumėte priskirti operacijas su kortelėmis. Iš naujo pristačius operacijas su kreditinėmis kortelėmis, jas galima pažymėti išlaidų ataskaitai ir apmokėtu įprastu išlaidų ataskaitos kompensavimo procesu.
