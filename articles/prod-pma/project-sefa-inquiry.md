---
title: Federalinių subsidijų tyrimo išlaidų grafikas
description: Šiame straipsnyje pateikta informacija apie federalinių subsidijų tyrimo išlaidų grafiką.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 00f9e97b9a6b3e8fe5e9cf9143e670612869b84c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916666"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Federalinių subsidijų tyrimo išlaidų grafikas

[!include [banner](../includes/banner.md)]

Pagal Valdymo biuro ir biudžeto aplinkraštį A-133, agentūroms, gaunančioms federalinių lėšų, taikomi audito reikalavimai, kurie dar vadinami pavieniu auditu. Auditas naudojamas siekiant reguliariai pranešti apie federalinių subsidijų pajamas ir išlaidas. Pavienio audito ataskaitos dalyje įtrauktas federalinių subsidijų išlaidų grafikas (SEFA).

Federalinių subsidijų tyrimo išlaidų grafike yra vietinės federalinės pagalbos katalogo (CFDA) pavadinimas ir numeris, subsidijos numeris, subsidijos metai, lėšas suteikiančios federalinės agentūros pavadinimas ir tarpininkaujančio subjekto pavadinimas. Tyrimas yra skirtas konkrečiam laikotarpiui. Paprastai tas laikotarpis sutampa su finansinių ataskaitų laikotarpiu – tai yra finansiniai metai.

Tyrimas apima subsidijas, kurias planuojama skirti pasirinktą laikotarpį. Tyrimo stulpelyje **Cedento agentūra** rodomas subsidijos klientas arba cedento agentūra (jei subsidija perduodama). Dėl perduodamos subsidijos stulpelyje **Tarpininkavimo agentūra** rodomas subsidijos klientas. Jei subsidija nėra perduodama, stulpelis **Tarpininkavimo agentūra** yra tuščias.

## <a name="set-up-the-cfda-clusters"></a>CFDA grupių nustatymas

Reikia nustatyti CFDA grupes, kurios gali būti susietos su CFDA numeriais federalinių subsidijų tyrimo išlaidų grafike.

1. Eikite į **Projektų valdymas ir apskaita \> Sąranka \> Subsidijos \> Federalinės vietinės pagalbos grupių katalogas**.
2. Pasirinkite **Naujas** norėdami sukurti CFDA grupę.
3. Įveskite grupės pavadinimą.
4. Pasirinkite **Įrašyti**, kad įrašytumėte keitimus.

## <a name="set-up-cfda-numbers"></a>CFDA numerių nustatymas

Reikia nustatyti CFDA numerius, kurie gali būti įtraukti į subsidijas ir į federalinių subsidijų tyrimo išlaidų grafiką.

1. Eikite į **Projektų valdymas ir apskaita \> Sąranka \> Subsidijos \> Federalinės vietinės pagalbos numerių katalogas**.
2. Pasirinkite **Naujas** norėdami sukurti CFDA numerį.
3. Stulpelyje **Numeris** įveskite CFDA numerį.
4. Paspauskite **Tabuliavimo** klavišą.
5. Stulpelyje **Aprašas** įveskite CFDA pavadinimą.
6. Paspauskite **Tabuliavimo** klavišą.
7. Pasirinktinai: lauke **Programų grupė** įtraukite atitinkamą CFDA grupę.
8. Pasirinkite **Įrašyti**, kad įrašytumėte keitimus.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Federalinių subsidijų tyrimo išlaidų grafiko ataskaitos subsidijų nustatymas

1. Eikite į **Projektų valdymas ir apskaita \> Subsidijos \> Subsidijos** ir pasirinkite esamą subsidiją.
2. „FastTab“ lauke **Sąranka**, lauke **Federalinės nacionalinės paramos katalogas** priskirkite CFDA numerį. Subsidijos CFDA numeris nustato ataskaitų CFDA grupę.
3. „FastTab“ **Kontaktinė informacija** įveskite cedento informaciją atlikdami šiuos veiksmus:

    1. Lauke **Subsidijos klientas** įveskite už subsidiją atsakingą klientą. Esamos subsidijos informacija jau turbūt įvesta.
    2. Nurodykite, ar subsidijos klientas yra finansuotojas. Jei subsidijos klientas yra finansuotojas, žymės langelį **Perduoti** palikite tuščią. Jei finansuotojas yra kitas klientas, o subsidijos klientas atsako už pinigų leidimą ir sekimą, pažymėkite žymės langelį **Perduoti**.

4. Jei ankstesniame veiksme pažymėjote žymės langelį **Perduoti**, lauke **Cedento agentūra** įveskite subsidiją suteikusį klientą. Cedento agentūra ir subsidijos klientas negali būti tas pats klientas.

Čia pateikiamas perduodamos subsidijos pavyzdys:

Federalinė vyriausybė finansavo valstijos infrastruktūros projektą. Federalinė vyriausybė skyrė lėšų valstijai. Šiuo atveju federalinė vyriausybė yra cedento agentūra, o valstija yra subsidijos klientas.

> [!NOTE] 
> Pirmą kartą įjungus funkciją, pradiniai CFDA numeriai bus įvesti naudojant esamus subsidijų numerius.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Subsidijų šalinimas iš SEFA ataskaitų remiantis subsidijų tipu

1. Eikite į **Projektų valdymas ir apskaita \> Sąranka \> Subsidijos \> Subsidijų tipai**.
2. „FastTab“ lauke **Numatytoji informacija** pažymėkite žymės langelį **Pašalinti iš federalinių subsidijų išlaidų grafiko**.
3. Pasirinkite **Įrašyti**, kad įrašytumėte keitimus.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Federalinių subsidijų tyrimo išlaidų grafiko vykdymas

1. Eikite į **Projektų valdymas ir apskaita \> Tyrimai ir ataskaitos \> Subsidijos tyrimas \> Federalinių subsidijų išlaidų grafikas**.
2. Skyriuje **Parametrai** atlikite šiuos veiksmus:

    1. Lauke **Datų intervalas** pasirinkite datų intervalo kodą. Arba laukuose **Pradžios data** ir **Pabaigos data** nustatykite datų intervalą.
    2. Pasirinktinai: jei į tyrimą kaip pajamas norite įtraukti tik išrašytų sąskaitų faktūrų operacijas, parinktį **Įtraukti tik išrašytų sąskaitų faktūrų pajamas** nustatykite į **Taip**.

## <a name="columns"></a>Stulpeliai

Federalinių subsidijų tyrimo išlaidų grafike yra šie stulpeliai:

- Federalinės vietinės pagalbos grupės pavadinimo katalogas
- Cedento agentūra
- Tarpininkavimo agentūra
- Subsidijos pavadinimas
- Subsidijos ID
- Subsidijos paraiškos ID
- Federalinė vietinės pagalbos katalogas
- Kvitai
- Išlaidos


[!INCLUDE[footer-include](../includes/footer-banner.md)]