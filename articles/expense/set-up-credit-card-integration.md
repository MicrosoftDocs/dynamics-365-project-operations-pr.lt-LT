---
title: Kredito kortelės integravimo nustatymas
description: Šiame straipsnyje paaiškinama, kaip dirbti su išlaidomis susijusiomis kredito kortelių operacijomis.
author: suvaidya
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4d32754548af67bdd5b9f7345f6363bd6193b36d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924505"
---
# <a name="set-up-credit-card-integration"></a>Kredito kortelės integravimo nustatymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Su išlaidomis susijusios kredito kortelių operacijos gali būti nustatytos taip, kad automatiškai būtų importuojamos pagal pasikartojantį grafiką. Arba operacijas galima importuoti neautomatiniu būdu, nes jos būtinos. Kredito kortelių operacijos importuojamos naudojant kredito kortelės operacijų duomenų objektą.

## <a name="import-credit-card-transactions"></a>Importuoti kredito kortelių operacijas

Norėdami importuoti kredito kortelės operacijas, atlikite toliau nurodytus veiksmus.

1. Puslapyje **Kredito kortelių operacijos** pažymėkite **Importavimo operacijos**. Jei duomenų valdymą atidarote pirmą kartą, sistema turi atnaujinti duomenų objektų sąrašą, kad galėtumėte tęsti.
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

Nutraukus darbuotojo įrašą, darbuotojo Active Directory domenų tarnybų (AD DS) abonementas išjungiamas. Tačiau gali būti aktyvios kredito kortelių operacijos, kurios turi būti apmokamos ir kompensuojamos. Puslapyje **Kredito kortelės operacijos** galite iš naujo priskirti darbuotoją bet kuriai kredito kortelės operacijai, kurios susietasis darbuotojas atleistas.

Pažymėkite vieną arba kelias kredito kortelės operacijas, tada pažymėkite **Iš naujo priskirti operacijas**. Tada galite pasirinkti kitą darbuotoją, kad galėtumėte priskirti operacijas su kortelėmis. Iš naujo pristačius operacijas su kreditinėmis kortelėmis, jas galima pažymėti išlaidų ataskaitai ir apmokėtu įprastu išlaidų ataskaitos kompensavimo procesu.

## <a name="delete-credit-card-transactions"></a>Kredito kortelių operacijų panaikinimas 

Kartais importavus kredito kortelės operacijas, tam tikras operacijas gali tekti panaikinti. Taip gali būti dėl to, kad operacijos yra dublikatai arba dėl to, kad duomenys nėra tikslūs. Administratoriai gali naudoti funkciją **Kredito kortelių operacijų panaikinimas** ir pasirinkti bei panaikinti kredito kortelių operacijas, kurios **nepridėtos** prie išlaidų ataskaitos. 

1. Eikite į **Periodinės užduotys** > **Kredito kortelių operacijų panaikinimas**.
2. Pasirinkite **Filtruoti** ir pateikite informaciją, pagal kurią norite identifikuoti norimus įtraukti įrašus.
3. Norėdami panaikinti įrašus, pasirinkite **Gerai**. 

## <a name="storing-credit-card-numbers"></a>Kredito kortelių numerių saugojimas

Yra trys galimybės saugoti kredito kortelių numerius. Kredito kortelių numeriai saugomi **puslapyje Išlaidų valdymo parametrai**.

- **Užkirsti kelią kortelės numerio įvedimui** – kredito kortelių numeriai nesaugomi.
- **Maišos kortelių numeriai (saugokite paskutinius keturis skaitmenis)** - Paskutiniai keturi kredito kortelių numerių skaitmenys saugomi šifruotu formatu.
- **Parduotuvės kortelių numeriai** – kredito kortelių numeriai saugomi nešifruotu formatu. Ši parinktis neatitinka mokėjimo kortelių pramonės (PCI) duomenų saugumo standarto (DSS). Todėl, kad jų organizacija atitiktų PCI DSS taisykles, organizacijos administratoriai turėtų pasirinkti arba nesaugoti kredito kortelių numerių, arba saugoti maišos kortelių numerius.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
