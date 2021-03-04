---
title: Išlaidų kvito apdorojimas
description: Šioje temoje pateikiama informacija apie optinio simbolių atpažinimo (OCR) apdorojimą kvitams. Ši funkcija skirta pagerinti vartotojų aplinką kuriant išlaidų ataskaitas programoje „Microsoft Dynamics 365 Finance“.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 64901610144f9dfe274bd4c2294ab32659743a1a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960302"
---
# <a name="expense-receipt-processing"></a>Išlaidų kvito apdorojimas

Išlaidų įrašas buvo patobulintas diegiant optinio simbolių atpažinimo (OCR) duomenų apdorojimą kvitams. Ši funkcija skirta pagerinti vartotojų aplinką kuriant išlaidų ataskaitas.

## <a name="key-features"></a>Pagrindinės funkcijos

- Iš kvitų nuskaitomi pardavėjo pavadinimas, data ir bendra suma.
- Funkcija bandys gretinti nepridėtus kvitus su nepridėtų išlaidų operacijomis.
- Vartotojai gali kurti neautomatiniu būdu įvestas išlaidų operacijas iš kvitų.

## <a name="usage-examples"></a>Naudojimo pavyzdžiai

Norėdami automatiškai pridėti kvitus, kuriuose yra kredito kortelių operacijų, kai sukuriama išlaidų ataskaita, atlikite toliau nurodytus veiksmus.

  1. Atidarykite **Išlaidų valdymo** darbo sritį.
  2. Skirtuke **Kvitai** patikrinkite ar yra nepridėtų kvitų. Taip pat galite įkelti kvitus skirtuke **Kvitai**.
  3. Skirtuke **Išlaidos** patikrinkite ar yra nepridėtų išlaidų. Paprastai išlaidų administratorius importuoja šias išlaidas iš kredito kortelės tiekėjo.
  4. Pažymėkite **Naują išlaidų ataskaitą**. Atkreipkite dėmesį, kad kurdami išlaidų ataskaitą galite įtraukti išlaidas ir kvitus. Jei pridėsite išlaidas ir kvitus, automatiškai sugretinami kvitai ir išlaidos.

Jei norite kurti išlaidas arba sugretinti išlaidas iš kvito, atlikite toliau nurodytus veiksmus.

  1. Išlaidų ataskaitoje, skirtuke **Kvitai**, pridėkite kvitą pažymėdami **Įtraukti kvitus**.
  2. Atkreipkite dėmesį į parinktis **Kurti** ir **Gretinti**, esančias po nusiųsto kvito vaizdu.

      - Pasirinkite **Kurti**, kad sukurtumėte rankiniu būdu įvestą išlaidų operaciją ir užpildytumėte iš kvito gautas reikšmes.
      - Jei pažymėjote **Gretinti**, sistema bandys sugretinti esamas išlaidas su kvitu.

## <a name="installation"></a>Diegimas

Ši funkcija veikia kartu su funkcija **Išlaidų ataskaitų pertvarkymas**, kad išlaidų tvarkymas būtų paprastesnis. Ši funkcija pasiekiama tik 2 pakopos ir aplinkose, kurios yra smėlio dėžė ir gamyba.

Norėdami naudoti šias išplėstinių išlaidų galimybes, įdiekite „Expense Management Service“ papildinį, skirtą „Microsoft Dynamics 365 Finance“ ir įgalinkite savo egzempliorių funkcijas. Galite pasiekti papildinį iš savo projekto programoje „Microsoft Dynamics Lifecycle Services“ (LCS).

1. Prisijunkite prie LCS ir atidarykite pageidaujamą aplinką.
2. Eikite į **Pilna išsami informacija**.
3. Pažymėkite **Prižiūrėti** arba slinkite žemyn į  **Aplinkos papildinių** „FastTab“.
4. Pažymėkite **Įdiegti naują papildinį**.
5. Pasirinkite **„Expense Management Service“**.
6. Vadovaukitės įdiegimo vadovu ir sutikite su terminais ir sąlygomis.
7. Pasirinkti **Diegti**.

**Funkcijų valdymo** darbo srityje Įjunkite šias funkcijas:

- Išlaidų ataskaitų pertvarkymas
- Automatiškai gretinti ir kurti išlaidas iš kvito

Įjungus šias funkcijas atliekami šie veiksmai:

- Esama **Išlaidų valdymo** darbo sritis pakeičiama nauja darbo sritimi.
- Įtraukiamas naujas išlaidų lauko matomumo meniu elementas.
- Dar galite atidaryti buvusių **Išlaidų ataskaitų** puslapį nuėję į **Išlaidų valdymas > Mano išlaidos > Išlaidų ataskaitos**.
- Darbo eigos ir bet kokie patvirtinimai vis dar pateksite į esamų išlaidų ataskaitų puslapį.
- Kvitai bus apdorojami per „Microsoft Azure Cognitive Services“, o metaduomenys bus išskleisti ir įtraukti.
- Įtraukiama parinktis, leidžianti kurti išlaidų ataskaitą, kurioje yra suderintų nepridėtų kvitų.
- Prie išlaidų ataskaitų pridėta parinktis leidžia sukurti išlaidų eilutę iš kvito arba bando sugretinti esamą kvitą su esama išlaidų eilute.

Daugiau informacijos apie funkciją Išlaidų ataskaitų pertvarkymas žr. [Išlaidų ataskaitų pertvarkymas](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

**Ar „Microsoft“ naudoja mano duomenis savo modeliams?**

Ne, „Microsoft“ sukūrė bendrąjį mašininio mokymo modelį, skirtą kvito apdorojimo paslaugai. Šis modelis nėra pagrįstas jūsų įkeliamais kvitais.

**Kur ši funkciją prieinama ir apdorojama?**

Šiuo metu funkcija palaikoma Jungtinėse Valstijose.

**Kur yra mano kvitai?**

Jei norite išskleisti lauko duomenis, „Finance“ susisieks su „Cognitive Services“. „Cognitive Services“ išsaugos jūsų kvito kopiją iki 24 valandų, kol vyksta apdorojimas. Baigus apdorojimą „Cognitive Services“ pašalins kvitą. Kvitai vis tiek saugomi programoje „Finance“.

Daugiau informacijos žr [Kvitų supratimo įjungimas naudojant naują formų atpažinimo funkciją](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]