---
title: Kainodaros dimensijų apžvalga
description: Šiame straipsnyje pateikiama informacija apie kainodaros dimensijas programoje Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 294dcff8e9717aaa3a0459daf87cb7d608c96106
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918046"
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

„Dynamics 365 Project Operations“ pateikiama su numatytuoju kainodaros dimensijų rinkiniu. Kainodaros dimensijas galite peržiūrėti apsilankę **„Project Operations“** > **Parametrai**. Parametrų įraše, esančiame skirtuke **Suma pagrįstos kainodaros dimensijos**, patvirtinkite, kad vaidmuo **msdyn_resourcecategory** ir išteklių organizacinio vieneto **msdyn_organizationalunit** laukai **Taikoma pardavimui** ir **Taikoma savikainai** nustatyti į **Taip**. Įgalinus šiuos laukus, galėsite nustatyti kiekvieno vaidmens ir organizacinio vieneto derinio kainą ir savikainą.

![„Project Service“ parametrų ekrano kopija su pažymėtu lauku „Taikoma pardavimui“.](media/PS-OOB-parameters.png)

Jei jums reikia nustatyti išteklių kainą arba savikainą naudojant papildomus atributus, galite sukurti pritaikytus laukus, objektus ir dimensijas. Daugiau informacijos rasite šiuose straipsniuose. 
  
  > [!NOTE]
  > Procedūras reikia atlikti tokia tvarka, kokia jos nurodytos.

1. [Sprendimo pasirinktinėms kainodaros dimensijoms kūrimas](../sales/create-solution-custompd.md)
2. [Pasirinktinių laukų ir objektų kūrimas](create-custom-fields-entities-pricing-dimensions.md)
3. [Pasirinktinių laukų įtraukimas į kainų sąranką ir operacijų objektus ](add-custom-fields-price-setup-transactional-entities.md)
4. [Pasirinktinių laukų kaip kainodaros dimensijų nustatymas ](set-up-custom-fields-pricing-dimensions.md)
5. [Atnaujinti priedo atributus, kad įtrauktumėte naujas kainodaros dimensijas](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Žmogiškųjų išteklių laiko kainodara
Kaip organizacijos nustato kainą žmogiškųjų išteklių laikui dažnai yra svarbus strateginis aspektas, turintis tiesioginės įtakos organizacijos pelningumui. Dirbkite su finansų komandomis ir praktikos vadovais, kai jūsų organizacija yra pasirengusi nustatyti, kaip ji nori nustatyti sąskaitų ir savikainos tarifus, skirtus žmogiškųjų išteklių laikui.

Vienas iš kitų kainodaros aspektų yra ar reikia pakartotinai naudoti laukus arba objektus, kurie šiuo metu nėra kainodaros dimensijos, tačiau taikomi kaip jūsų organizacijos kainodaros dimensija. Laukai, kaip **Operacijos kategorija** (**msdyn_transactioncategory**) ir **Rezervuojami ištekliai** (**bookableresource**), yra potencialių dimensijų pavyzdžiai. 

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]