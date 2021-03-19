---
title: Priedo atributų atnaujinimas norint įtraukti naujų kainodaros dimensijų
description: Šioje temoje pateikta informacija apie kainodaros dimensijų priedo atributų atnaujinimą.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281803"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Priedo atributų atnaujinimas norint įtraukti naujų kainodaros dimensijų

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Jei nenaudojate „Project Service Automation“ (PSA) pasiūlymo teikimo ir sutarties sudarymo funkcijų, galite praleisti šią temą.

Šioje temoje daroma prielaida, kad atlikote temose [Pasirinktinių laukų ir objektų kūrimas](create-custom-fields-entities.md), [Pasirinktinių laukų įtraukimas į kainos sąranką ir operacijų objektus](field-references.md) bei [Pasirinktinių laukų kaip kainodaros dimensijų nustatymas](set-up-pricing-dimensions.md) nurodytas procedūras. Jei neatlikote šių procedūrų, grįžkite ir jas atlikite, o tada grįžkite į šią temą.

Kai pasiūlymo eilutės informacija sukuriama projekto pasiūlymo eilutės puslapyje **Pasiūlymo eilutė**, sistema sukuria dvi įvertinimo eilutes fone – vieną eilutę įvertinimo savikainos pusei, ir vieną pardavimo pusei. Tas pats taikoma projekto sutarties eilutėms.

Kai keičiate kiekį arba lauką savikainos pusėje, šis pakeitimas perkeliamas į pardavimo pusę. Tai įmanoma dėl šių priedų, kuriuos pakeitus kainodaros dimensijas reikia iš naujo užregistruoti.

- PreOperationContractLineDetailUpdate - atnaujina **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - atnaujina **msdyn_quotelinetransaction**.

Toliau aprašytuose veiksmuose paaiškinta, kaip užregistruoti priedus.

1. Atidarykite **PluginRegistrationTool** ir prisijunkite prie savo internetinio egzemplioriaus.
2. Spustelėkite **Ieška** ir ieškokite priedo, kurį norite naujinti.

 ![Ieškos medžio ekrano kopija](media/PRT-1.png)

3. Kai priedas bus rastas, pasirinkite jį, tada spustelėkite **Pasirinkti pagrindinėje formoje**.

4. Pasirinkite norimo naujinti priedo veiksmą, spustelėkite dešiniuoju pelės mygtuku ir pasirinkite **Naujinti**.

 ![Priedo, kuris bus atnaujintas, ekrano kopija](media/PRT-2.png)
 
5. Naujinimo lange filtravimo atributuose spustelėkite daugtaškį (**...**).

 ![Esamo veiksmo konfigūravimo informacijos naujinimo ekrano kopija](media/PRT-3.png)
 
6. Pažymėkite kainodaros atributo žymės langelius.

 ![Ekrano kopija, kurioje matomas kainodaros atributų žymės langelių pasirinkimas](media/PRT-4.png)

7. Spustelėkite **Gerai**, kad uždarytumėte puslapį, tada pasirinkite **Atnaujinti veiksmą**.

 ![Ekrano kopija, kurioje rodomas mygtukas „Atnaujinti veiksmą“](media/PRT-5.png)
 
8. Šį procesą pakartokite su antru priedu **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction naujinimas**.

9. Uždarykite priedų registravimo įrankį.



[!INCLUDE[footer-include](../includes/footer-banner.md)]