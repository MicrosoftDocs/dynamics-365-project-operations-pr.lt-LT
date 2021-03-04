---
title: Pardavimo kainoraščio sąranka
description: Šioje temoje pateikta informacija apie pardavimų kainoraščius, skirtus projektų kainodarai.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: eb8dfa61a2d17ba644daf1552889cbcde0f1e47a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176261"
---
# <a name="set-up-a-sales-price-list"></a>Pardavimo kainoraščio sąranka

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projekto pasiūlymams ir sutartims taikomas kitoks projekto kainoraščio kainų keitimo modelis nei produktų kainoraščiui. Produktų katalogu pagrįstoje pasiūlymo eilutėje galite pakeisti vaidmenų ir kategorijų kainas tiesiog pasiūlymo eilutėje, nes kiekviena pasiūlymo eilutė nurodo tik vieną katalogo prekę. Tačiau projektu pagrįstoje pasiūlymo eilutėje negalima keisti vaidmenų ir kategorijų kainų tiesiog pasiūlymo eilutėje. Galite naudoti projekto kainoraštį, kad dirbtumėte su dviem skirtingais perrašymo modeliais.

> [!NOTE]
> Rekomenduojame turėti atskirą projekto išteklių kainoraštį ir katalogo prekių kainoraštį, nes keičiant kainas jie veikia skirtingai.

Kiekvienam iš toliau nurodytų objektų galima sudaryti vieną arba kelis susijusius projekto kainodaros pardavimo kainoraščius.

- Klientas (kodas) 
- Galimybė 
- Pasiūlymas 
- Projekto sutartis

Šių objektų susiejimą su kainoraščiu nurodo projekto kainoraščiai. Su pardavimo objektais Klientas, Galimybė, Pasiūlymas ir Projekto sutartis galite susieti vieną arba kelis kainoraščius.

Numatytasis projekto kainoraštis nėra automatiškai pridedamas prie kliento įrašo. Tačiau projekto kainoraštį prie kliento įrašo galite pridėti patys. Vis dėlto projekto kainoraštį pridėti patys turėtumėte, tik jei su klientu esate sudarę pasirinktinės kainodaros sutartį. 

Kai projekto kainoraštis pridedamas prie pardavimo objekto, tikrinama toliau nurodyta informacija:

- Kainoraščio kontekstas yra **Pardavimas**. 
- Kainoraščio valiuta atitinka kliento valiutą. 

Automatiškai nustatant susijusius projekto kainoraščius projekto sutartyje naudojama toliau nurodytą pirmumo seka:

1. Pasiūlymas
2. Galimybė
3. Klientas 
4. Visuotiniai parametrai 

Kai projekto kainoraštis įvedamas pagal numatytuosius parametrus, sistema tikrina, ar valiuta atitinka kliento valiutą, ir įvestų numatytųjų kainoraščių kontekstas yra **Pardavimai**.

Galite susieti kelis kainoraščius su objektais Klientas, Galimybė, Pasiūlymas ir Projekto sutartis. Jei sudarant ilgalaikių projektų sutartis jums gali prireikti daugiau nei vieno kainoraščio, siekiant įtraukti dėl infliacijos atnaujintas kainas, šis pajėgumas palaiko konkrečiai datai nustatomas kainas. Tačiau jei su objektais Klientas, Galimybė, Pasiūlymas arba Projekto sutartis susietų kainoraščių galiojimo datos persidengia, numatytosios kainos gali būti netinkamos. Todėl reikia užtikrinti, kad projekto kainoraščiai, kurių galiojimo datos persidengia, nebūtų susieti su šiais objektais.


[!INCLUDE[footer-include](../includes/footer-banner.md)]