---
title: Tiekėjo mokėjimo sulaikymo sąlygų kūrimas ir taikymas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip nustatyti ir išlaikyti tiekėjo mokėjimų užlaikymo sąlygas.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 2cd18375d93e503ac532cb3839c691231ea46681
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916758"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Tiekėjo mokėjimo sulaikymo sąlygų kūrimas ir taikymas

[!include [banner](../includes/banner.md)] 

Projekto tiekėjo mokėjimų sulaikymo sąlygų nustatymas yra naudingas, kai jūsų organizacija nori sulaikyti tiekėjui atliktų mokėjimų dalį. Pavyzdžiui, jei norite sulaikyti mokėjimą tiekėjui, kol pristatyti produktai atitiks jūsų lūkesčius. Tariantis dėl tiekėjo sutarties, galima nurodyti tiekėjo mokėjimo sulaikymo sąlygas.

## <a name="create-vendor-payment-retention-terms"></a>Tiekėjo mokėjimo sulaikymo sąlygų kūrimas

Galite įvesti tiekėjo mokėjimo sulaikymo procentą ir anksčiau sulaikytų sumų, kurios dabar bus pervestos, procentą. Sumos automatiškai sulaikomos tiekėjo sąskaitose faktūrose, kol sutarties būsena tampa užbaigta. Nustatę sulaikymo sąlygas, galite jas taikyti bet kuriam to tiekėjo projektui.

Atlikite toliau nurodytus veiksmus, kad nustatytumėte ir tvarkytumėte tiekėjui atliekamų mokėjimų sulaikymo sąlygas. 

1. Pasirinkite **Projektų valdymas ir apskaita** > **Sulaikymas** > **Tiekėjui atliekamų mokėjimų sulaikymo sąlygos**.
2. Pasirinkite **Naujas**, jei norite įtraukti naują tiekėjo sulaikymo sąlygą. Naujos sąlygos lauko **Taisyklės ID** reikšmė įvedama automatiškai. 
3. Įveskite trumpą aprašymą lauke **Aprašas**, o „FastTab“ **Sąlygos** pasirinkite **Įtraukti eilutę** ir įveskite šias sąlygų reikšmes.

   - **Pristatytų vienetų procentinė dalis**: įveskite sąlygos įvykdymo procentą. Sumos automatiškai sulaikomos tiekėjo sąskaitose faktūrose, kol projekto baigimo etapas sutaps su nurodyta būsena. Pavyzdžiui, jei įvesite 50,00, sumos sulaikomos tol, kol 50 % projekto bus baigta.
   - **Sulaikymo procentas**: įveskite tiekėjo sąskaitos faktūros sumos procentinę dalį, kuri bus sulaikyta. Pavyzdžiui, jei įvesite 10,00, tada 10 procentų tiekėjo sąskaitos faktūros sumos bus sulaikyti, kol projektas pasieks baigimo procentą, nustatytą lauke **Pristatytų vienetų skaičius**.
   - **Išleidimo procentas**: pasirinkite **Įtraukti eilutę** ir įveskite bet kurių anksčiau sulaikytų sumų, kurios bus išliestos, pasirinkto projekto baigimo lygio procentą.

> [!NOTE]
> Jei skirtingiems projekto baigimo lygiams taikote daugiau nei vieną etapą, įveskite atskirą kiekvienos sulaikymo taisyklės tiekėjo sulaikymo sąlygos eilutę. Kiekviena eilutė gali nurodyti skirtingą sulaikymo procentą ir skirtingą kiekvieno skirto projekto baigimo lygio procentą.

Sukūrę tiekėjo sulaikymo sąlygas, galite jas taikyti projektui.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Tiekėjo sulaikymo sąlygų taikymas projektui

1. Pasirinkite **Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai** ir atidarykite projektą iš projektų sąrašo puslapio.
2. „FastTab“ **Tiekėjų sutartys** pasirinkite **Įtraukti eilutę**.
3. Lauke **Kliento kodas** pasirinkite vieną iš pateiktų parinkčių. 

   - **Lentelė**: tiekėjo sulaikymo sąlygos taikomos vienam tiekėjui.
   - **Grupė**: tiekėjo sulaikymo sąlygos taikomos visiems tiekėjams, priklausantiems tiekėjų grupei.
   - **Visi**: tiekėjo sulaikymo sąlygos taikomos visiems tiekėjams.

4. Lauke **Tiekėjas / tiekėjų grupė** pasirinkite tiekėją arba tiekėjų grupę, kuriai taikomos tiekėjo sulaikymo sąlygos. Jei ankstesniame veiksme pasirinkote **Visi**, šis laukas nepasiekiamas.
5. Lauke **Tiekėjo sulaikymo sąlygos** pasirinkite sulaikymo sąlygas, kurias sukūrėte ankstesnėje procedūroje.
6. Jei projekte taip pat nustatytos tiekėjo „mokėjimo sumokėjus“ (PWP) sąlygos, įveskite ribinę projekto dalį lauke **PWP ribinės vertės procentas**.

Tiekėjo saugojimo sąlygos taip pat rodomos pardavimo užsakymuose, kuriuos kuriate tiekėjui.


[!INCLUDE[footer-include](../includes/footer-banner.md)]