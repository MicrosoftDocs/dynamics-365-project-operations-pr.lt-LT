---
title: Kainodaros dimensijų apžvalga
description: Šioje temoje pateikiama informacija apie kainodaros dimensijas programoje „Dynamics 365 Project Operations“.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080943"
---
# <a name="pricing-dimensions-overview"></a>Kainodaros dimensijų apžvalga

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Dimensijos, naudojamos žmogiškųjų išteklių kainodarai ir savikainai nustatyti, skirstomos į dvi kategorijas:

- Žmonės
- Suplanuotas darbas

Dėl to egzistuoja dviejų tipų kainodaros dimensijų reikšmės:

- **Parinkčių rinkiniai** – dimensijos, kurios yra reikšmių rinkiniams skirti fiksuoti išvardijimai.
- **Objektu pagrįstos reikšmės** – dimensijos, kurios gali būti kintančiu reikšmių rinkiniu.

## <a name="pricing-dimensions"></a>Kainodaros dimensijos

„Dynamics 365 Project Operations“ pateikiamas su numatytuoju kainodaros dimensijų rinkiniu. Kainodaros dimensijas galite peržiūrėti apsilankę **„Project Operations“** > **Parametrai**. Parametrų įraše, esančiame skirtuke **Suma pagrįstos kainodaros dimensijos** , patvirtinkite, kad vaidmuo **msdyn_resourcecategory** ir išteklių organizacinio vieneto **msdyn_organizationalunit** laukai **Taikoma pardavimui** ir **Taikoma savikainai** nustatyti į **Taip**. Įgalinus šiuos laukus, galėsite nustatyti kiekvieno vaidmens ir organizacinio vieneto derinio kainą ir savikainą.

Jei jums reikia nustatyti išteklių kainą arba savikainą naudojant papildomus atributus, galite sukurti pritaikytus laukus, objektus ir dimensijas.

## <a name="pricing-human-resource-time"></a>Žmogiškųjų išteklių laiko kainodara
Kaip organizacijos nustato kainą žmogiškųjų išteklių laikui dažnai yra svarbus strateginis aspektas, turintis tiesioginės įtakos organizacijos pelningumui. Dirbkite su finansų komandomis ir praktikos vadovais, kai jūsų organizacija yra pasirengusi nustatyti, kaip ji nori nustatyti sąskaitų ir savikainos tarifus, skirtus žmogiškųjų išteklių laikui.

Vienas iš kitų kainodaros aspektų yra ar reikia pakartotinai naudoti laukus arba objektus, kurie šiuo metu nėra kainodaros dimensijos, tačiau taikomi kaip jūsų organizacijos kainodaros dimensija. Laukai, kaip **Operacijos kategorija** ( **msdyn_transactioncategory** ) ir **Rezervuojami ištekliai** ( **bookableresource** ), yra potencialių dimensijų pavyzdžiai. 

Įvertinkite, ar jūsų kainodaros dimensija turi būti lentelė ar parinkčių rinkinys. Jei numatote dimensijos reikšmių pakitimus, kurie viršys 10 ar 12, ir jums reikia papildomų atributų šioms reikšmėms, galite sukurti objektą, o ne parinkčių rinkinį. Parinkčių rinkinio tvarkymui, pavyzdžiui, įtraukiant ar šalinant reikšmes, būtinas administratorius arba kūrėjas, o įtraukti naujų eilučių į lentelę gali daugelis vartotojų.

Toliau pateiktame pavyzdyje pateikiami sąskaitų tarifai, nustatyti pagal vaidmenį ir išteklių organizacijos vienetą, kuriam priklauso išteklius. Savikainos tarifai paprastai nustatomi pagal darbuotojo atlyginimų juostą ir organizacijos vienetą, kuriam jie priklauso. Šiame pavyzdyje sąskaitų ir savikainos tarifų lentelės atrodo taip:

**Pavyzdiniai sąskaitų tarifai**

| Vaidmuo        | Organizacijos vienetas    |Vienetas      |Kaina      |Valiuta  |
| ------------|-------------|----------|----------:|----------|
| Kūrėjas   | „Danys“, JAV  |Hour | 200|USD     |
| Kūrėjas   | „Danys India“ |Hour|   112|USD     |


**Pavyzdiniai savikainos tarifai**

| Atlyginimų juosta     | Organizacijos vienetas    |Vienetas      |Kaina      |Valiuta  |
| ----------------|-------------|----------|----------:|----------|
| „My company_Band1“ | „Danys“, JAV  |Hour | 145|USD     |
| „My company_Band2“ | „Danys India“ |Hour|   67|USD     |
