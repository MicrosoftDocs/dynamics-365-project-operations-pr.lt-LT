---
title: Užbaigimo išlaidų apskaičiavimo metodai
description: Šioje temoje pateikta informacija apie metodus, naudojamus norint apskaičiuoti išlaidas projektui užbaigti.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c6d3cd6056466be686f15c9f332c8274aeb0ac19
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013946"
---
# <a name="cost-to-complete-methods"></a>Užbaigimo išlaidų apskaičiavimo metodai

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje pateikta informacija apie metodus, naudojamus norint apskaičiuoti išlaidas projektui užbaigti. Yra keli metodai, kuriuos galite naudoti projekto užbaigimo išlaidoms apskaičiuoti. 

Kurdami projekto įvertinimą, puslapyje **Kurti įvertinimą**, lauke **Baigimo metodo išlaidos**, galite pasirinkti vienas iš toliau nurodytų metodų užbaigimo išlaidoms apskaičiuoti.

| Užbaigimo išlaidų apskaičiavimo metodas    | Aprašo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Visos išlaidos – faktinės            | Įveskite numatomas išlaidas neautomatiškai laukuose **Visos išlaidos** arba **Visas kiekis** naudodami mygtuką **Išlaidų įvertinimas**, esantį **įvertinimo puslapyje**. Sistema iš visos jūsų įvestos sumos atima faktines išlaidas. Visa suma yra projekto užbaigimo išlaidos. Šis metodas nenaudoja išlaidų įvertinimų ir išteklių priskyrimo, įvestų į „Project Operations“ „Microsoft Dataverse“ aplinkoje. Jei reikia, visas išlaidas arba visą kiekį galima atnaujinti neautomatiškai.  |
| Visa prognozuojama suma – faktinė        | Visai prognozuojamai projekto sumai nustatyti naudojamas išteklių priskyrimas ir išlaidų įvertinimai. Faktinės išlaidos palyginamos su šia prognoze ir apskaičiuojamos užbaigimo išlaidos.                                                                                                                                                                                                                                                                          |
| Kaip ankstesnis įvertinimas         | Šiuo atveju naudojami tie patys įvertinimo metodai, kurie buvo naudojami ankstesniu laikotarpiu. Šiam metodui reikia prognozės modelio, jei ankstesniam modeliui reikėjo prognozės modelio.                                                                                                                                                                                                                                                                                                                           |
| Nustatyti, kad sąnaudos baigtųsi nuliu | Paprastai naudojamas prieš pašalinant įvertinamą projektą, šis metodas suderina bendrus įvertinimus su užregistruotomis faktinėmis operacijomis ir išvalo stulpelį **Užbaigimo išlaidos**. Baigus rezultatas visada yra 100 procentų. Kiekvienos jūsų sukurtos sąnaudų eilutės žymės langelis **Prognozavimas** išvalomas, o bendras įvertinimas nukopijuojamas iš ankstesnio sąnaudų įvertinimo. Faktinis įvertinimo laikotarpio suvartojimas atskaitomas iš projekto sąnaudų.              |
| Iš sąnaudų šablono           | Užbaigimo sąnaudų apskaičiavimo metodas, nustatomos sąnaudų šablone, susietame su pasirinktu įvertinamu projektu.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]