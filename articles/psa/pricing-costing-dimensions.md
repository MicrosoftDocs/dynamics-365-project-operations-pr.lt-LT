---
title: Kainodaros ir įkainojimo dimensijų pagrindinis puslapis
description: Šiame straipsnyje pateikiama kainodaros dimensijų apžvalga.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 88c77d90bccaa5f10e8f75d60ae121d699bc0976
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925452"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Kainodaros ir įkainojimo dimensijų pagrindinis puslapis

[!include [banner](../includes/psa-now-project-operations.md)]

Dimensijos, naudojamos darbo kainodarai ir savikainai nustatyti projektų vykdymo organizacijose, yra veikiamos šių atributų:

- Darbuotojai, kurie dirba pagal jų patirtį, vaidmenį ir lokaciją
- Atliekamas darbas pagal jo sudėtingumą arba dienos metą

Atsižvelgiant į įprastą šių darbo atributų ir žmonių, reikalingų atlikti darbui, pobūdį, išskiriami du „Project Service Automation“ kainodaros dimensijų reikšmių tipai: 

- **Parinkčių rinkiniai** – atributai, kurie yra fiksuoti reikšmių rinkinių išvardijimai.
- **Objektų reikšmės** – atributai, galintys turėti įvairų reikšmių rinkinį, kuris yra ribotas, bet ilgainiui gali kisti.

## <a name="pricing-dimensions"></a>Kainodaros dimensijos

PSA pateikiamas su numatytuoju kainodaros dimensijų rinkiniu. Jas galite peržiūrėti apsilankę **„Project Service“** > **Parametrai**. Parametrų įraše, esančiame skirtuke **Suma pagrįstos kainodaros dimensijos**, patvirtinkite, kad vaidmuo **msdyn_resourcecategory** ir išteklių organizacinio vieneto **msdyn_organizationalunit** laukai **Taikoma pardavimui** ir **Taikoma savikainai** nustatyti į **Taip**. Taip galėsite nustatyti kiekvieno vaidmens ir organizacinio vieneto derinio kainą ir savikainą.

![„Project Service“ parametrų ekrano kopija su pažymėtu lauku „Taikoma pardavimui“.](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Jei naudojote visiškai parengtus vaidmens ir organizacinio vieneto laukus kaip kainodaros dimensijas prieš 3 PSA versiją, jokių pastebimų pakeitimų nebus. Galite toliau naudoti „Project Service“ kaip įprasta. 

Jei jums reikia nustatyti išteklių kainą arba savikainą naudojant papildomus atributus, galite sukurti pritaikytus laukus, objektus ir dimensijas. Norėdami gauti daugiau informacijos, žiūrėkite šiuos straipsnius, tačiau atkreipkite dėmesį, kad turite atlikti procedūras toliau nurodyta tvarka:

- [Sukurti pritaikytus laukus ir objektus](create-custom-fields-entities.md)
- [Pridėti pritaikytus laukus prie kainos sąrankos ir operacijos objektų](field-references.md)
- [Pasirinktinių laukų kaip kainodaros dimensijų nustatymas ](set-up-pricing-dimensions.md)
- [Atnaujinti priedo atributus, kad įtrauktumėte naujas kainodaros dimensijas](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Žmogiškųjų išteklių laiko kainodara
Kaip organizacijos nustato kainą žmogiškųjų išteklių laikui dažnai yra svarbus strateginis aspektas, turintis tiesioginės įtakos organizacijos pelningumui. Dirbkite su finansų komandomis ir praktikos vadovais, kai jūsų organizacija yra pasirengusi nustatyti, kaip ji nori nustatyti sąskaitų ir savikainos tarifus, skirtus žmogiškųjų išteklių laikui.

Vienas iš kitų kainodaros aspektų yra ar reikia pakartotinai naudoti laukus arba objektus, kurie šiuo metu nėra kainodaros dimensijos, tačiau taikomi kaip jūsų organizacijos kainodaros dimensija. Laukai, kaip **Operacijos kategorija** (**msdyn_transactioncategory**) ir **Rezervuojami ištekliai** (**bookableresource**), yra potencialių dimensijų pavyzdžiai. 

Įvertinkite, ar jūsų kainodaros dimensija turi būti lentelė ar parinkčių rinkinys. Jei numatote dimensijos reikšmių pakitimus, kurie viršys 10 ar 12, o jums reikia papildomų atributų šioms reikšmėms, sukurkite objektą, o ne parinkčių rinkinį. Parinkčių rinkinio tvarkymui, pavyzdžiui, įtraukiant ar šalinant reikšmes, būtinas administratorius arba kūrėjas, o įtraukti naujas eilutes į lentelę gali dauguma verslo vartotojų.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
