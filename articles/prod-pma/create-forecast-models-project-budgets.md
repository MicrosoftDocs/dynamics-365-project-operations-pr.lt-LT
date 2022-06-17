---
title: Projektų biudžetų prognozės modelių kūrimas
description: Šiame straipsnyje aprašoma, kaip sukurti likusių biudžetų prognozės modelį.
author: Yowelle
ms.date: 04/24/2020
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
ms.openlocfilehash: e6b1419c41124d2062595f7346efb7538e50ee33
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916712"
---
# <a name="create-forecast-models-for-project-budgets"></a>Projektų biudžetų prognozės modelių kūrimas 

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti likusių biudžetų prognozės modelį. Projektas, kuriam taikoma biudžeto kontrolė, naudoja dviejų tipų biudžetus: pradinį ir likusį. Kurdami projekto biudžetą turite nurodyti pradinio ir likusio biudžeto prognozės modelius, sukurtus puslapyje **Prognozės modeliai**. Projektų biudžetai, pagrįsti nurodytais modeliais, kuriami patvirtinant projekto biudžetą.

> [!NOTE]
> Prognozės modelis, naudojamas biudžeto kontrolėje, negali turėti papildomo modelio arba būti naudojamas kaip papildomas modelis.

1. Pasirinkite **Projektų valdymas ir apskaita** > **Sąranka** > **Prognozės**  > **Prognozės modeliai**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują prognozės modelį, tada įveskite modelio ID numerį ir naujo modelio pavadinimą. 
3. Nustatykite parinktį **Sustabdytas** į parametrą **Taip**, kad būtų išvengta bet kokių prognozės modelio prognozės eilučių pakeitimų. 
4. Jei prognozės eilutės, su kuriomis susietas modelis, turėtų generuoti grynųjų pinigų srauto prognozes didžiojoje knygoje, nustatykite parinktį **Įtraukti į pinigų srauto prognozes** į parametrą **Taip**. 
5. Norėdami naudoti projekto datą kaip sąskaitos faktūros datą, nustatykite parinktį **Prognozės sąskaitos faktūros data** į parametrą **Taip**. 
6. Lauke **Biudžeto tipas** pasirinkite vieną iš toliau nurodytų modelių tipų.

   - **Pradinis biudžetas**: naudokite pradinio biudžeto sumas, kurios patvirtintos sukūrus ir patvirtinus pradinį biudžetą.
   - **Likęs biudžetas**: projekto vykdymo metu naudokite likusio biudžeto sumas. Šio prognozės modelio likučiai sumažinami pagal faktines organizacijas ir padidinami arba sumažinami pagal biudžeto peržiūras.
   - **Perkėlimas**: naudokite projekto perkeliamas biudžeto sumas. Perkėlimas – tai pasirinktinis procesas, kurį galima vykdyti, norint perkelti nepanaudotas biudžeto sumas iš vienų finansinių metų į kitus.

7. Nustatykite toliau nurodytas parinktis pagal poreikį.

   - Įjunkite parinktį **Prognozės sąskaitos faktūros data**, norėdami naudoti projekto datą kaip sąskaitos faktūros datą.
   - Įjunkite parinktį **Prognozė su NG**, norėdami kurti prognozę pagal nebaigtą gamybą (NG), tada pasirinkite NG tipą. 
   - Numatytąjį **biudžeto tipą** galite palikti kaip **nenurodytą** arba galite įvesti naują tipą. Pakeitus įrašą, biudžeto tipas nekeičiamas.     
    > [!NOTE]
    > Jei pakeisite numatytąjį biudžeto tipą, visos kitos parinktys nebus pasiekiamos atnaujinus, o šio prognozės modelio pakartotinai naudoti negalima. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]