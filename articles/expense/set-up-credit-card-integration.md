---
title: Kredito kortelės integravimo nustatymas
description: Šioje temoje aiškinama, kaip dirbti naudojant su išlaidomis susijusias kredito kortelės operacijas.
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
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
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866693"
---
# <a name="set-up-credit-card-integration"></a>Kredito kortelės integravimo nustatymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Su išlaidomis susijusios kredito kortelių operacijos gali būti nustatytos taip, kad automatiškai būtų importuojamos pagal pasikartojantį grafiką. Arba operacijas galima importuoti neautomatiniu būdu, nes jos būtinos. Kredito kortelių operacijos importuojamos naudojant kredito kortelės operacijų duomenų objektą.

## <a name="import-credit-card-transactions"></a>Importuoti kredito kortelių operacijas

Norėdami importuoti kredito kortelės operacijas, atlikite toliau nurodytus veiksmus.

1. Puslapyje **Kredito kortelių operacijos** pažymėkite **Importavimo operacijos**. Jei pirmą kartą atidarote duomenų valdymą, sistema turi atnaujinti duomenų objektų sąrašą, kad galėtumėte tęsti.
2. Lauke **Pavadinimas** įveskite unikalų importavimo užduoties aprašą.
3. Lauke **Šaltinio duomenų formatas** pažymėkite failo, kuriame yra importuotos kredito kortelių operacijos, formatą.
4. Pažymėkite **Įkelti**, tada raskite ir pažymėkite failą, kurį norite importuoti.
5. Nusiuntę failą, patikrinkite kredito kortelės operacijos failo susiejimą ir kredito kortelės operacijų duomenų įrašo stulpelius pasirinkdami plytelės saitą **Žiūrėti struktūrą**. Jei yra susiejimo klaidų, arba jei turite pakeisti susiejimą, pakeiskite susiejimą skirtuke **Susiejimo vizualizavimas** arba skirtuke **Susiejimo informacija**.
6. Norėdami automatizuoti kredito kortelių operacijas, pažymėkite **Kurti pasikartojančias duomenų užduotis**. Tada galite nustatyti pasikartojimą, apibrėžiantį, kaip dažnai reikia importuoti kreditinės kortelės operacijas. Baigę pasirinkite **Gerai**.
7. Jei norite importuoti pažymėtą failą dabar, pasirinkite **Importuoti**.
8. Jei importuojant įvyksta klaidų, galite peržiūrėti vykdymo žurnalą arba paruošimo duomenis ir peržiūrėti reikiamas ištaisyti klaidas, kad užtikrintumėte, jog bus importuota sėkmingai.

> [!NOTE]
> Jei norite importuoti daugiau nei vieną failo formatą, kiekvienam formato tipui reikia sukuti atskirų importavimo užduočių.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Iš naujo priskirti nutrauktų darbuotojų kredito kortelių operacijas

Nutraukus darbuotojo įrašą, darbuotojo „Active Directory Domain Services“ (AD DS) abonementas išjungiamas. Tačiau gali būti aktyvios kredito kortelių operacijos, kurios turi būti apmokamos ir kompensuojamos. Puslapyje **Kredito kortelės operacijos** galite iš naujo priskirti darbuotoją bet kuriai kredito kortelės operacijai, kurios susietasis darbuotojas atleistas.

Pažymėkite vieną arba kelias kredito kortelės operacijas, tada pažymėkite **Iš naujo priskirti operacijas**. Tada galite pasirinkti kitą darbuotoją, kad galėtumėte priskirti operacijas su kortelėmis. Iš naujo pristačius operacijas su kreditinėmis kortelėmis, jas galima pažymėti išlaidų ataskaitai ir apmokėtu įprastu išlaidų ataskaitos kompensavimo procesu.

## <a name="delete-credit-card-transactions"></a>Kredito kortelių operacijų panaikinimas 

Kartais importavus kredito kortelės operacijas, tam tikras operacijas gali tekti panaikinti. Taip gali nutikti dėl to, kad operacijos yra dublikatai, arba duomenys gali būti netikslūs. Administratoriai gali naudoti funkciją **Kredito kortelių operacijų panaikinimas** ir pasirinkti bei panaikinti kredito kortelių operacijas, kurios **nepridėtos** prie išlaidų ataskaitos. 

1. Eikite į **Periodinės užduotys** > **Kredito kortelių operacijų panaikinimas**.
2. Pasirinkite **Filtruoti** ir pateikite informaciją, pagal kurią norite identifikuoti norimus įtraukti įrašus.
3. Norėdami panaikinti įrašus, pasirinkite **Gerai**. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
