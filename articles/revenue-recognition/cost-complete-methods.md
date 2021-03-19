---
title: Užbaigimo išlaidų apskaičiavimo metodai
description: Šioje temoje pateikta informacija apie metodus, naudojamus norint apskaičiuoti išlaidas projektui užbaigti.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 837cb3abe33e6e74087b8aae8b072bf4a21dc933
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279058"
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