---
title: Tiekėjo užlaikymo nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti tiekėjo užlaikymą.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583714"
---
# <a name="set-up-vendor-retention"></a>Tiekėjo užlaikymo nustatymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje pateikiama informacija, kaip nustatyti tiekėjo užlaikymą.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Tiekėjo užlaikymo sąskaitos nustatymas didžiojoje knygoje

1. Dalyje Dynamics 365 Finance eikite į **DK** > **registravimo nustatymo nustatymus** > **Sąskaitos, skirtos automatinėms operacijoms**.
2. Įtraukite naują eilutę.
3. Lauke **Registravimo tipas** pasirinkite **Tiekėjo užlaikymas**.
4. Pasirinkite pagrindinę tiekėjo užlaikymo registravimo sąskaitą.

## <a name="create-vendor-retention-terms"></a>Tiekėjo užlaikymo sąlygų kūrimas

Naudokite puslapį **Tiekėjo užlaikymo sąlygos** norėdami nustatyti ir prižiūrėti tiekėjo mokėjimų užlaikymo sąlygas. Įveskite tiekėjo mokėjimo procentinę dalį, kurią norite užlaikyti, ir anksčiau užlaikytų sumų, kurias norite išleisti, procentinę dalį. Sumos automatiškai sulaikomos tiekėjo sąskaitose faktūrose, kol sutarties būsena tampa užbaigta. Nustatę tiekėjo užlaikymo sąlygas, galite jas pritaikyti bet kuriam projektui, su kuriuo tiekėjas dirba.

1. Naudodami „Finance“ eikite į **Projektų valdymas ir apskaita** > **Nustatymas** > **Užlaikymas** > **Tiekėjo mokėjimo užlaikymo sąlygos**.
2. Pasirinkite **Naujas**, jei norite įtraukti naują tiekėjo sulaikymo sąlygą. Lauke **Taisyklės ID** automatiškai įvedama naujos sąlygos reikšmė. 
3. Lauke **Aprašas** įveskite aprašomąjį naujos sąlygos pavadinimą.
4. Skirtuke **Sąlygos** pasirinkite **Įtraukti eilutę** norėdami įvesti tiekėjo užlaikymo sąlygą.
5. Lauke **Pristatytų vienetų procentinė dalis** įveskite taisyklės įvykdymo procentinį dydį. Sumos automatiškai užlaikomos tiekėjo sąskaitose faktūrose, kol projekto įvykdymo etapas susilygina su įvestu procentiniu dydžiu. Pavyzdžiui, jei įvesite 50,00, sumos sulaikomos tol, kol 50 % projekto bus baigta.
6. Lauke **Užlaikytina procentinė dalis** įveskite tiekėjo sąskaitos faktūros sumos procentinę dalį, kuri bus užlaikoma. Pvz., jei šiame lauke įvedate 10,00, užlaikoma 10 procentų tiekėjo sąskaitų faktūrų sumos, kol pasiekiamas projekto įvykdymo procentinis dydis, pasirinktas lauke **Pristatytų vienetų procentinė dalis**.
7. Lauke **Išleidžiama procentinė dalis** įveskite bet kurios anksčiau užlaikytos sumos procentinę dalį, kurią norite išleisti pasiekus pasirinktą projekto įvykdymo lygį.

> [!NOTE]
> Jei naudojate daugiau nei vieną skirtingų projekto įvykdymo lygių etapą, įveskite atskirą kiekvienos užlaikymo taisyklės tiekėjo užlaikymo sąlygos eilutę. Kiekvienoje eilutėje galima nurodyti skirtingą procentinę dalį, kurią norite užlaikyti ir kurią reikia išleisti pasiekus kiekvieną nustatytą projekto įvykdymo lygį.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Projekto tiekėjo sutarties nustatymas

Nustatykite projektui taikomas tiekėjo užlaikymo sąlygas. Tiekėjo saugojimo sąlygos taip pat rodomos pardavimo užsakymuose, kuriuos kuriate tiekėjui.

1. Naudodami „Finance“ eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai**. 
2. Pažymėkite projektą ir veiksmų srityje pažymėkite **Projektų grupė** > **Tiekėjų sutartys**.
3. Puslapyje **Tiekėjų sutartys** įtraukite naują eilutę.
4. Lauke **Kliento kodas** pasirinkite vieną iš pateiktų parinkčių:
   - **Lentelė**: tiekėjo sulaikymo sąlygos taikomos vienam tiekėjui.
   - **Grupė**: tiekėjo sulaikymo sąlygos taikomos visiems tiekėjams, priklausantiems tiekėjų grupei.
   - **Visi**: tiekėjo sulaikymo sąlygos taikomos visiems tiekėjams.
5. Lauke **Tiekėjas / tiekėjų grupė** pasirinkite tiekėją arba tiekėjų grupę, kuriai taikomos tiekėjo užlaikymo sąlygos. Jei ankstesniame veiksme pasirinkote **Visi**, šis laukas nepasiekiamas.
6. Lauke **Tiekėjo užlaikymo sąlygos** pasirinkite šiam tiekėjui taikytinų užlaikymo sąlygų taisyklės ID.

