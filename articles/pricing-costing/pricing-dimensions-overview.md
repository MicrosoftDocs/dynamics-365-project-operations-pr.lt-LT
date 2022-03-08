---
title: Kainodaros dimensijų apžvalga
description: Šioje temoje pateikiama informacijos apie „Dynamics 365 Project Operations“ kainodaros dimensijas.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: e8d62dcf9975e5427926210a881dec2c256f1b8b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368486"
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

![„Project Service“ parametrų ekrano kopija su pažymėtu lauku „Taikoma pardavimui“](media/PS-OOB-parameters.png)

Jei jums reikia nustatyti išteklių kainą arba savikainą naudojant papildomus atributus, galite sukurti pritaikytus laukus, objektus ir dimensijas. Daugiau informacijos žr. tolesnėse temose. 
  
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

| Vaidmuo        | Org. vienetai    |Vienetas      |Kainos      |Valiuta  |
| ------------|-------------|----------|----------:|----------|
| Developer   | „Contoso“ JAV  |Valanda | 200|USD     |
| Developer   | Contoso India |Valanda|   112|USD     |


**Pavyzdiniai savikainos tarifai**

| Atlyginimų juosta     | Org. vienetai    |Vienetas      |Kainos      |Valiuta  |
| ----------------|-------------|----------|----------:|----------|
| „My company_Band1“ | „Contoso“ JAV  |Valanda | 145|USD     |
| „My company_Band2“ | Contoso India |Valanda|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]