---
title: Produkto kainoraščiai
description: Šioje temoje pateikta informacija apie kainoraščius katalogo kainodara, naudojama projektų pasiūlymams ir sutartims.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8bfd4eaa6f4bcbbdf398683a25a3b0079cfedd535ef32d383993883607f7ef5a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999236"
---
# <a name="product-price-lists"></a>Produkto kainoraščiai

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

 „Project Operations“ **Produkto kainoraščiai** ir susiję kainoraščio objektai palaiko produktų įkainojimo funkciją produktu pagrįsto pasiūlymo ir sutarties eilutėse. Kai produktai naudojami projektuose, naudojami projekto kainoraščių kainų sąrašo elemento įrašai. 

Produktus reikia nustatyti taip, kad produktų kataloge jie turėtų numatytąją savikainą ir kainoraščius. Norėdami konfigūruoti numatytąją savikainą ir kainoraščius, naudokite sąrašo kainą, standartinę kainą ir dabartinę kainą. Numatytosios sąrašo kainos naudojamos pasiūlymo eilutėje arba projekto sutarties eilutėje tik tada, kai sistema negali rasti to produkto kainoraščio eilutės produkto kainoraštyje pasiūlymui ar projekto sutarčiai.

Produkto katalogo eilučių savikainą galima keisti tarp pasiūlymų. Šis pajėgumas svarbus, nes jei tiksliai neseksite savikainos, negalėsite nustatyti operacijų pelno projektų rezervavime. Pagal numatytuosius nustatymus, produkto standartinė savikaina naudojama kaip savikaina. Tačiau numatytąją savikainą galima atnaujinti pasiūlymo eilutėje, jei yra kita to pasiūlymo savikaina.

## <a name="price-list-items"></a>Kainų sąrašo elementai

Galite įtraukti produktus iš produktų katalogo į skirtingus kainoraščius. Produktų kainoraščių eilutės visada nurodo konkretų vienetą. Produktų kainodara kainų sąrašo elementams galima sukonfigūruoti kaip valiutos sumą. Arba ją galima sukonfigūruoti kaip kainų sąrašo, dabartinės kainos arba standartinės kainos funkciją.

Įkainojimo funkcija palaiko įvairias apvalinimo parinktis, kai produkto kainos konfigūruojamos kaip kainų sąrašo, standartinės kainos arba dabartinės kainos funkcija. Be to, kad galite pasinaudoti kelių kainodaros metodų ir apvalinimo parinkčių privalumais, jūs taip pat galite susieti nuolaidų sąrašus su kainoraščio elementais. 

 
## <a name="default-product-price-list"></a>Numatytasis produkto kainoraštis
Kiekvienas kliento įrašas turi lauką **Numatytasis kainoraštis**, kuriame galite nurodyti kainoraštį, atitinkantį kliento valiutą. Šiame lauke numatytoji reikšmė automatiškai neįvesta. Kai egzistuoja pasirinktinės kainodaros sutartis su konkrečiu klientu, galite naudoti šį lauką, kad susietumėte kainoraštį su tuo klientu.

Galimybės, pasiūlymo ir projekto sutarties objektai naudoja toliau pateikiamą tvarką, kad būtų įvesti numatytieji produktų kainoraščiai. Tas pats užsakymas naudojamas projektų kainoraščiams.

1.  Pasiūlymas
2.  Galimybė
3.  Klientas
4.  Visuotiniai parametrai 

Pagal numatytuosius nustatymus, pasiūlymo eilutėje esančiame lauke **Produktas** pateikiamas visų aktyviųjų produktų, esančių pasiūlymo produkto kainoraštyje, sąrašas. Jei produktas nebuvo suaktyvintas arba jei tai yra juodraštinis produktas, jis nepateikiamas sąraše, net jei jis yra kainoraštyje. 

Produktų katalogo eilutės įtraukiamos kaip sąskaitos faktūros eilutės pirmoje sąskaitoje faktūroje, sukurtoje projekto sutarčiai. Juodraštinėje sąskaitoje faktūroje šias sąskaitų faktūrų eilutes galima panaikinti. Tokiu atveju eilutės bus rodomos kitoje sąskaitoje faktūroje tol, kol joms nebus išrašyta sąskaita faktūra, arba kol sąskaita faktūra nebus išsiųsta klientui. Negalite sukurti sąskaitos faktūros daliniui produkto sąskaitos faktūros eilutės kiekiui. Kai projekto sutarties produktų eilutėms išrašoma sąskaita faktūra, sukuriami faktiniai duomenys. Tačiau šie faktiniai duomenys nesusieti su susijusio projekto objektu. Kitaip tariant, produktu pagrįsto projekto sutarties eilutės nepriklauso nuo jokio projektu pagrįsto naudojimo. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
