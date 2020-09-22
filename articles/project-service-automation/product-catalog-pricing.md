---
title: Produktų katalogo kainodara
description: Šioje temoje pateikta informacija apie tai, kaip veikia produktų katalogo kainodara programoje Dynamics 365 Project Service Automation (PSA).
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f1a8b1af-0767-4d83-82ef-367aac7a630f
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8f296f6af9f60f40b726fddb095785dfb9831dc3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753780"
---
# <a name="product-catalog-pricing"></a>Produktų katalogo kainodara 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Kainoraščiai ir kainoraščio elementų objektai palaiko produktų katalogo kainodarą. Daugiausiai ši funkcija naudojama katalogu pagrįstoms eilutėms projektų pasiūlymuose ir projekto sutartyse.

Projektu pagrįstoms eilutėms sutartyje pateikiamas sandėris po to, kai jis buvo laimėtas. Kadangi derybų procesas dažniausiai įvyksta prieš jas laimint, prie pasiūlymo pridėta kainodara visada kopijuojama į naują kainoraštį tokia, kokia yra ir pridedama prie sutarties. Šio naujo kainoraščio negalima pakeisti už sutarties aprėpties ribų. Šis apribojimas padeda apsaugoti tarifo kortelę, dėl kurios buvo susiderėta, nuo bet kokių kainų pakeitimų, atsirandančių pagrindiniame kainoraštyje.

Produktus reikia nustatyti taip, kad produktų kataloge jie turėtų numatytąją savikainą ir kainoraščius. Norėdami konfigūruoti numatytąją savikainą ir kainoraščius, turite naudoti sąrašo kainą, standartinę kainą ir dabartinę kainą. Numatytosios sąrašo kainos naudojamos pasiūlymo eilutėje arba projekto sutarties eilutėje tik tada, kai sistema negali rasti to produkto kainoraščio eilutės produkto kainoraštyje pasiūlymui ar projekto sutarčiai.

Produkto katalogo eilučių savikainą galima keisti tarp pasiūlymų. Šis pajėgumas svarbus, nes jei tiksliai neseksite savikainos, negalėsite nustatyti operacijų pelno projektų rezervavime. Pagal numatytuosius nustatymus, produkto standartinė savikaina naudojama kaip savikaina. Tačiau numatytąją savikainą galima atnaujinti pasiūlymo eilutėje, jei yra kita to pasiūlymo savikaina.

## <a name="price-list-items"></a>Kainų sąrašo elementai

Galite įtraukti produktus iš produktų katalogo į skirtingus kainoraščius. Produktų kainoraščių eilutės visada nurodo konkretų vienetą. Produktų kainodara kainų sąrašo elementams galima sukonfigūruoti kaip valiutos sumą. Arba ją galima sukonfigūruoti kaip kainų sąrašo, dabartinės kainos arba standartinės kainos funkciją.

Programoje PSA palaikomos įvairios apvalinimo parinktys, kai kainos konfigūruojamos kaip kainų sąrašo, standartinės kainos arba dabartinės kainos funkcija. Be to, kad galite pasinaudoti kelių kainodaros metodų ir apvalinimo parinkčių privalumais, jūs taip pat galite susieti nuolaidų sąrašus su kainoraščio elementais. 

> ![Produktų įtraukimas iš katalogų į skirtingus kainoraščius](media/basic-guide-16.png)

Kai pasiūlymui kuriate naują pasirinktinį kainoraštį pasirinkdami parinktį **Kurti pasirinktinį kainoraštį** puslapyje **Projekto pasiūlymas**, PSA sukuria kainoraščio kopiją, o laukas **Objektas**, esantis naujo kainoraščio antraštėje, nustatomas į **Pardavimo objektas**. Naujo kainoraščio pavadinimas sujungiamas su pasiūlymo pavadinimu ir laiko žyma. Taip pat galite naudoti naujo kainoraščio pavadinimą ir pasiūlymo pavadinimą pasirinktinėse darbo eigose, kad suaktyvintumėte papildomą peržiūrą ir pasiūlymų, naudojančių pasirinktinę kainodarą, patvirtinimą.

 
## <a name="default-product-price-list"></a>Numatytasis produkto kainoraštis
Kiekvienas kliento įrašas turi lauką **Numatytasis kainoraštis**, kuriame galite nurodyti kainoraštį, atitinkantį kliento valiutą. Programoje PSA šiame lauke numatytoji reikšmė automatiškai neįvesta. Kai egzistuoja pasirinktinės kainodaros sutartis su konkrečiu klientu, galite naudoti šį lauką, kad susietumėte kainoraštį su tuo klientu.

Galimybės, pasiūlymo ir projekto sutarties objektai naudoja toliau pateikiamą tvarką, kad būtų įvesti numatytieji produktų kainoraščiai. Tas pats užsakymas naudojamas projektų kainoraščiams.

1.  Pasiūlymas
2.  Galimybė
3.  Klientas
4.  Visuotiniai PSA parametrai

Pagal numatytuosius nustatymus, pasiūlymo eilutėje esančiame lauke **Produktas** pateikiamas visų aktyviųjų produktų, esančių pasiūlymo produkto kainoraštyje, sąrašas. Jei produktas nebuvo suaktyvintas arba jei tai yra juodraštinis produktas, jis nepateikiamas sąraše, net jei jis yra kainoraštyje. 

Produktų katalogo eilutės įtraukiamos kaip sąskaitos faktūros eilutės pirmoje sąskaitoje faktūroje, sukurtoje projekto sutarčiai. Juodraštinėje sąskaitoje faktūroje šias sąskaitų faktūrų eilutes galima panaikinti. Tokiu atveju eilutės bus rodomos kitoje sąskaitoje faktūroje tol, kol joms nebus išrašyta sąskaita faktūra, arba kol sąskaita faktūra nebus išsiųsta klientui. Programoje PSA negalite sukurti sąskaitos faktūros daliniui produkto sąskaitos faktūros eilutės kiekiui. Kai projekto sutarties produktų eilutėms išrašoma sąskaita faktūra, sukuriami faktiniai duomenys. Tačiau šie faktiniai duomenys nesusieti su susijusio projekto objektu. Kitaip tariant, produktu pagrįsto projekto sutarties eilutės nepriklauso nuo jokio projektu pagrįsto naudojimo. PSA neseka medžiagų suvartojimo projektuose.
