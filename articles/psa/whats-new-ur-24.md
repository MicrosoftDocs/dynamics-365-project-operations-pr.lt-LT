---
title: Kas nauja arba pakeista „Project Service Automation“ V3 24 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 24 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6c8348e65307f63a251f97bf1ea17578e7026da8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080788"
---
# <a name="project-service-automation-update-release-24-v3"></a>„Project Service Automation“ V3 24 naujinimo leidimas

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 24 atnaujintame leidime. Ši versija turi naują komponavimo versijos numerį V 3.10.42.43 ir ją galima pasiekti per 2020 m. spalio mėn. automatinį naujinimą.

## <a name="update-release-24"></a>24 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**„Sales“**

Buvo pataisytos šios problemos:

- Problema nustatant numatytąjį produktų kainoraštį.
- Pasiūlymo laimėjimo efektyvumas yra lėtas dėl įterptųjų kainų sąrašo ir vaidmens kainos įrašų kopijos.
- **Projekto sutartis / pardavimų telkinys** > **Produkto linijos elementas / užsakymo linijos kiekis** yra automatiškai suapvalinamas iki artimiausio sveikojo skaičiaus.
- Iškelti iki sistemos teisių, kai skaitomi kainoraščiai.
- Kopijuoti kliento adreso laukus **address1_freighttermscode** ir **address1_shippingmethodcode** į pasiūlymą / užsakymą. 


**Laikas ir išlaidos**

Buvo pataisytos šios problemos:

- **Laiko įrašo tinklelis** nepalaiko **tik datos** laiko elgsenos.
- **Laiko įrašas** nėra atnaujinamas automatiškai. Reikalingas rankinis atnaujinimas.
- Neįmanoma importuoti laiko įrašų iš priskyrimo, kai ištekliaus priskyrimuose yra pertrauka (0 valandų).
- Kai kuriate laiko įrašą, nustatykite tokią pat pradžią kaip **msdyn_date**.
- Iš naujo įjungti masinį redagavimą laiko įrašui.

**Išteklių valdymas**

Buvo pataisytos šios problemos:

- Bandymas atnaujinti tarp dieninio rezervavimo būseną be reikalavimo, išmes null-ref išimtį.
- Klaida įkeliant **suderinimo rodinį**.


**Projektų valdymas**

Buvo pataisytos šios problemos:

- **Projekto grafike** keičiant iš **rankinio** į **automatinį** , automatinis įrašymas yra nebaigiamas.
- Išlaidų sąnaudos neturėtų skaičiuoti **projekto stebėjimo tinklelio** nuokrypio.
- **Sąmatų žymės** stulpelių nenuosekli elgsena per įkėlimą prieš **Laiko fazės** tipo keitimą.
- Faktinė projekto kaina gali neatspindėti galutinių sumų iš **faktinių duomenų**.
- **Numatoma pabaigos data** **Suvestinės** skirtuke nesutampa su **WBS grafiku**.
- **Faktinių valandų atnaujinimas** atvirkštinėje įtraukoje veikia neteisingai.
- Projekto vadovas, nepriklausantis pagrindiniam **BU** , negali sukurti projekto.
- Užduoties arba kategorijos pakeitimai **išlaidų sąmatose** neišlieka.
- **Sutarties kopija** nukopijuoja sąskaitos faktūros grafikus ir vykdymo būseną.
- **Atnaujinti faktinius** mygtukas neteisingai apskaičiuoja suvestinės užduotis.
- „Microsoft Project“ priedai: pataisyti nulinių nuorodų klaidas, jei bet kuris komandos narys turi tuščią išteklių vienetą.

