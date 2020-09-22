---
title: Kainodaros ir įkainojimo dimensijų pagrindinis puslapis
description: Šioje temoje pateikta kainodaros dimensijų apžvalga.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753677"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Kainodaros ir įkainojimo dimensijų pagrindinis puslapis

Dimensijos, naudojamos žmogiškųjų išteklių kainodarai ir savikainai nustatyti, skirstomos į dvi kategorijas:

- Žmonės
- Suplanuotas darbas

Dėl to egzistuoja dviejų tipų kainodaros dimensijų reikšmės programoje „Project Service Automation“ (PSA): 

- **Parinkčių rinkiniai** – dimensijos, kurios yra reikšmių rinkiniams skirti fiksuoti išvardijimai.
- **Objektu pagrįstos reikšmės** – dimensijos, kurios gali būti kintančiu reikšmių rinkiniu.

## <a name="pricing-dimensions"></a>Kainodaros dimensijos

PSA pateikiamas su numatytuoju kainodaros dimensijų rinkiniu. Jas galite peržiūrėti apsilankę **„Project Service“** > **Parametrai**. Parametrų įraše, esančiame skirtuke **Suma pagrįstos kainodaros dimensijos**, patvirtinkite, kad vaidmuo **msdyn_resourcecategory** ir išteklių organizacinio vieneto **msdyn_organizationalunit** laukai **Taikoma pardavimui** ir **Taikoma savikainai** nustatyti į **Taip**. Taip galėsite nustatyti kiekvieno vaidmens ir organizacinio vieneto derinio kainą ir savikainą.

![„Project Service“ parametrų ekrano kopija su pažymėtu lauku „Taikoma pardavimui“](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Jei naudojote visiškai parengtus vaidmens ir organizacinio vieneto laukus kaip kainodaros dimensijas prieš 3 PSA versiją, jokių pastebimų pakeitimų nebus. Galite toliau naudoti „Project Service“ kaip įprasta. 

Jei jums reikia nustatyti išteklių kainą arba savikainą naudojant papildomus atributus, galite sukurti pritaikytus laukus, objektus ir dimensijas. Daugiau informacijos rasite toliau pateikiamose temose, tačiau atkreipkite dėmesį, kad procedūras reikia atlikti toliau išvardyta tvarka:

- [Sukurti pritaikytus laukus ir objektus](create-custom-fields-entities.md)
- [Pridėti pritaikytus laukus prie kainos sąrankos ir operacijos objektų](field-references.md)
- [Nustatyti pritaikytus laukus kaip kainodaros dimensijas](set-up-pricing-dimensions.md)
- [Atnaujinti priedo atributus, kad įtrauktumėte naujas kainodaros dimensijas](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Žmogiškųjų išteklių laiko kainodara
Kaip organizacijos nustato kainą žmogiškųjų išteklių laikui dažnai yra svarbus strateginis aspektas, turintis tiesioginės įtakos organizacijos pelningumui. Dirbkite su finansų komandomis ir praktikos vadovais, kai jūsų organizacija yra pasirengusi nustatyti, kaip ji nori nustatyti sąskaitų ir savikainos tarifus, skirtus žmogiškųjų išteklių laikui.

Vienas iš kitų kainodaros aspektų yra ar reikia pakartotinai naudoti laukus arba objektus, kurie šiuo metu nėra kainodaros dimensijos, tačiau taikomi kaip jūsų organizacijos kainodaros dimensija. Laukai, kaip **Operacijos kategorija** (**msdyn_transactioncategory**) ir **Rezervuojami ištekliai** (**bookableresource**), yra potencialių dimensijų pavyzdžiai. 

Taip pat turėtumėte įvertinti, ar jūsų kainodaros dimensija turi būti lentelė ar parinkčių rinkinys. Jei numatote dimensijos reikšmių pakitimus, kurie viršys 10 ar 12, ir jums reikia papildomų atributų šioms reikšmėms, galite sukurti objektą, o ne parinkčių rinkinį. Parinkčių rinkinio tvarkymui, pavyzdžiui, įtraukiant ar šalinant reikšmes, būtinas administratorius arba kūrėjas, o įtraukti naujų eilučių į lentelę gali daugelis vartotojų.

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
