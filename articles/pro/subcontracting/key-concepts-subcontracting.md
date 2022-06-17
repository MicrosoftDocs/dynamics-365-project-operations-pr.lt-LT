---
title: Svarbiausios subrangos sutarties sąvokos
description: Šiame straipsnyje paaiškinamos kai kurios pagrindinės sąvokos, taikomos subrangos sutartims programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ac84d132a2d62528d97ed3776a78062a589a380
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927706"
---
# <a name="key-concepts-in-subcontracting"></a>Svarbiausios subrangos sutarties sąvokos

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Straipsnyje paaiškinamos kai kurios pagrindinės sąvokos, kurias turėtumėte žinoti prieš pradėdami naudoti subrangos funkciją programoje "Microsoft"Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Sutarties vienetas subrangos sutartyje

Sutarties vienetas yra padalinys ar praktika, turintys pateikti galutinį projektą. Sutarties vienetas taip pat yra padalinys, kuris sudaro sutartį su tiekėju.

## <a name="purchase-currency"></a>Pirkimo valiuta

Programoje „Project Operations” pirkimo valiuta yra valiuta, nurodyta kuriant subrangos sutartį. Taip pat tai yra valiuta kuria įrašomi projekto subrangovo išlaidos. Pirkimo valiuta gali skirtis nuo projekto valiutos, o projekto valiuta gali skirtis nuo pardavimo valiutos.

## <a name="billing-methods-on-subcontract-lines"></a>Atsiskaitymo metodai subrangos sutarties eilutėse

Projektams paprastai taikomi fiksuoto mokesčio ir vartojimu pagrįsti sutarčių sudarymo modeliai. „Project Operations” palaiko šiuos atsiskaitymo metodus pardavimo ir pirkimo kontekstuose. Pirkimo atsiskaitymo metodai veikia taip:

- **Laikas ir medžiagos** – kai subrangos sutarties eilutėje naudojamas metodas **Laikas ir medžiagos**, laiko sąnaudos projekte įrašomos kaip subrangovų darbas su šiuo projektu ir įrašo laikas. Tada šios subrangovų išlaidų operacijos suderinamos su tiekėjo sąskaitos faktūros eilutės elementais. Šiame modelyje projektų vadovai, naudojantys „Project Operations”, gali suderinti ir patikrinti tiekėjo SF eilutes, naudodami subrangovų įrašytą ir patvirtintą laiką. Patikrinus, ankščiau įrašyta savikaina po patvirtinimo atšaukiama, o nauja tiekėjo SF pagrįsta savikaina, sukuriama projekte.
- **Fiksuota kaina** – šiame fiksuoto mokesčio sutarties modelyje tiekėjo SF yra pagrįstos fiksuotomis gairėmis. Tačiau subrangovo ištekliai taip pat gali nurodyti laiką. Tada laiką peržiūri ir patvirtina projekto vadovas. Patvirtinus laiką, „Project Operations” sukuriama laikina projekto savikaina. Tiekėjui atsiuntus etapo SF, projekto vadovas gali su ja suderinti anksčiau įrašytą savikainą. Patikrinus, savikaina atšaukiama ir įrašoma etapu pagrįsta savikaina.

## <a name="project-price-lists-on-subcontracts"></a>Projekto kainoraščiai, esantys subrangos sutartyse

Projekto kainoraščiai yra kainoraščiai, naudojami laiko, išlaidų ir kitų su projektu susijusių komponentų pirkimo kainoms nustatyti. Programoje „Project Operations” gali būti keli kainų sąrašai, o kiekviename jų gali būti savo efektyvių pagal datą subrangos sutarčių. „Project Operations” nepalaiko persidengiančių efektyvių datų subrangos sutarties projekto kainoraščiuose.

## <a name="transaction-classes-on-subcontracts"></a>Subrangos sutarčių operacijų klasės

„Project Operations“ palaiko keturis operacijų klasių tipus:

- Laikas
- Išlaidos
- Medžiaga
- Rinkliava

Pirkimo išlaidos gali būti numatytos ir patirtos tik operacijų klasėse **Laikas**, **Išlaidos** ir **Medžiagos**. **Mokestis** yra tik pajamų operacijų klasė, nepasiekiama pirkimo turinyje.

## <a name="purchase-pricing-dimensions"></a>Pirkimo kainodaros dimensijos

Kainodaros dimensijos leidžia nuspręsti, kokie atributai naudojami nustatant pirkimo kainą ir numatytąsias laiko operacijas. Kalbant apie pirkimą, „Project Operations” palaiko tik fiksuotus dimensijų rinkinius pirkimo kainai ir numatytosioms reikšmėms nustatyti. Siekiant nustatyti pirkimo kainą ir numatytąsias reikšmes subrangos sutarties eilutėse ir subrangos sutarties operacijose, naudojami atributai **Vaidmuo** ir **Rezervuojami ištekliai**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
