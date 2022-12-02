---
title: Prekių reikalavimai projekto sutartims su keliais finansavimo šaltiniais
description: Šiame straipsnyje pateikiama informacija apie tai, kaip konfigūruoti ir naudoti elementų reikalavimus su keliais finansavimo šaltiniais.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028498"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Prekių reikalavimai projekto sutartims su keliais finansavimo šaltiniais

_**Taikoma (kam):**„Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_

Kai kuriems sutartiniams susitarimams, skirtiems projektais pagrįstiems rezultatams, gali prireikti kelių finansavimo šaltinių. Šiame straipsnyje paaiškinta, kaip pasirinkti ir konfigūruoti pageidaujamus finansavimo šaltinius, kai projektui arba projekto sutarčiai reikia kelių šaltinių.

## <a name="terminology"></a>Terminai

- **Finansavimo šaltinis** – objektas, iš kurio finansuojamos projekto sutartys dėl darbo. Šis objektas gali būti vidinė organizacija arba išorinis sąskaitos faktūros klientas (klientas arba subsidija).
- **Projekto klientas** – objektas, kuriam pateikiamas projekto darbas.
- **Sąskaitos faktūros klientas** – išorinis objektas, kuris moka už projekto darbą.

## <a name="example"></a>Pavyzdžiui

„Contoso“ laimėjo įrangos atnaujinimo sutartį su dviem savo klientais: „Adatum US“ ir „Adatum Corporate“. Į sutartį įtrauktos aparatūros ir diegimo paslaugos, kurios bus pateiktos „Adatum US“ (projekto klientas). Aparatūrą finansuos „Adatum Corporate“ (sąskaitos faktūros klientas 1), o diegimo darbus finansuos „Adatum US“ (sąskaitos faktūros klientas 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Sąskaitos faktūros kliento numatytojo vykdymo taisyklių, taikomų elementų reikalavimams, nustatymas

### <a name="prerequisites"></a>Būtinosios sąlygos

- Norint naudoti elementų reikalavimus, kurie turi kelis sąskaitų faktūrų klientus, reikia „Microsoft Dynamics 365 Finance“ **10.0.27** ar naujesnės versijos.
- Jūsų sistemos administratorius turi įjungti funkciją **Leisti elementų reikalavimus naudojant kelis finansavimo šaltinius, skirtus „Project Operations“ laikomų medžiagų / gamyba pagrįstiems scenarijams**, esančią darbo srityje **Funkcijų valdymas**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Sąskaitos faktūros klientų numatytojo vykdymo taisyklių nustatymas

Norėdami nustatyti numatytąsias sąskaitos faktūros kliento taisykles, atlikite toliau nurodytus veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.
1. Skirtuko **Bendra** skyriuje **Pardavimo užsakymai ir elementų reikalavimai** nustatykite parinktį **Leisti projektams su keliais finansavimo šaltiniais** kaip **Taip**.
1. Lauke **Numatytasis klientas** nurodykite, iš kur pagal numatytuosius nustatymus gaunamas projekto pristatymo klientas, kuriam taikomas elemento reikalavimas:

    - **Iš finansavimo šaltinio** – numatytasis projekto pristatymo klientas gaunamas iš finansavimo šaltinio. Jei su projekto sutartimi susieti keli finansavimo šaltiniai, bus naudojamas pirmasis sąraše esantis finansavimo šaltinis.
    - **Iš projekto** – numatytasis projekto pristatymo klientas gaunamas iš kliento, pasirinkto lauke **Projekto įrašo klientas**.

1. Pasirinktinai: nustatykite arba pakeiskite numatytąjį sąskaitos faktūros klientą projekto įrašuose:

    1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir atidarykite projekto įrašo išsamią informaciją.
    2. Skirtuke **Bendra** nustatykite arba atnaujinkite lauką **Numatytasis sąskaitos faktūros klientas**. Jūsų nurodytas klientas bus naudojamas kaip numatytasis sąskaitos faktūros klientas naujiems, projektui kuriamiems, elementų reikalavimams. Jei šį lauką paliksite tuščią, pagal numatytuosius nustatymus bus naudojamas pirmojo projekto sutarties finansavimo šaltinio sąskaitos faktūros klientas. Tačiau įrašę įrašą vartotojai galės pakeisti klientą.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Sąskaitos faktūros kliento, kuris bus naudojamas kuriant elemento reikalavimą, pasirinkimas

Norėdami pasirinkti sąskaitos faktūros klientą, kuris bus naudojamas kuriant elemento reikalavimą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir pasirinkite projekto įrašą.
1. Skirtuke **Planas** pasirinkite **Elementų reikalavimai**.
1. Sukurkite naują elemento reikalavimo įrašą.

    - Pagal numatytuosius nustatymus laukas **Sąskaitos faktūros klientas** įraše nustatomas kaip projektui nustatytas sąskaitos faktūros klientas. Galite pakeisti lauko **Sąskaitos faktūros klientas** reikšmę, tada įrašyti įrašą. Kai įrašas bus įrašytas nebegalėsite atnaujinti **Sąskaitos faktūros kliento** reikšmės. Jei reikės atnaujinti elemento reikalavimo **Sąskaitos faktūros kliento** reikšmę, panaikinkite esamą elemento reikalavimą, tada sukurkite naują su pageidaujama reikšme.
    - Pagal numatytuosius nustatymus elemento reikalavimo laukas **Klientas** pagrįstas **Numatytojo kliento** reikšme, kuri nustatoma puslapyje **Projektų valdymo ir apskaitos parametrai**.

    Įrašius elemento reikalavimo įrašą, sistema jį susieja su **Elemento reikalavimo pardavimo užsakymo** antraštės įrašu. Jei nė vienoje atviro pardavimo užsakymo antraštėje nėra pasirinkto sąskaitos faktūros kliento, sistema sukurs ir sukūrusi susies elemento reikalavimo eilutę.

> [!NOTE]
> Elementų reikalavimai visada visiškai įtraukiami į sąskaitą faktūrą, išrašytą įraše nustatytam sąskaitos faktūros klientui. Šiuo metu sistema nepalaiko finansavimo paskirstymo taisyklių, kuriose yra elementų reikalavimų, ir nesuskaidys registravimo pagal finansavimo paskirstymo taisyklių nustatymą.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Elemento reikalavimo kūrimas pagal elemento prognozės įrašą

Norėdami sukurti elemento reikalavimą pagal elemento prognozės įrašą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir pasirinkite projekto įrašą.
1. Skirtuke **Planas** pasirinkite **Elementų prognozės**.
1. Sukurkite naują elemento prognozės įrašą.
1. Pasirinktinai: skirtuko **Projektas** lauke **Finansavimo šaltinis** pasirinkite norimą sąskaitos faktūros klientą.
1. Pasirinkite **Kurti elemento reikalavimą** ir patvirtinkite pranešimą, kurį gausite.

    > [!NOTE]
    > Sistema nukopijuoja **Finansavimo šaltinio** reikšmę iš elemento prognozės įrašo į naujai kuriamą elemento reikalavimo įrašą.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Numatytasis sąskaitos faktūros klientas, kai sistema automatiškai sukuria elemento reikalavimą iš pirkimo užsakymo eilutės

Jei puslapyje **Projektų valdymo ir apskaitos parametrai** parinktis **Kurti elemento reikalavimą** nustatyta kaip **Taip**, sistema automatiškai sukuria elemento reikalavimą, kai įrašoma nauja projekto pirkimo užsakymo eilutė. Pagal numatytuosius nustatymus laukų **Sąskaitos faktūros klientas** ir **Elemento reikalavimas** reikšmės nustatomos pagal projekto įrašo lauko **Numatytasis sąskaitos faktūros klientas** reikšmę. Šiuo metu sistema nepalaiko šio tipo įrašų sąskaitos faktūros kliento naujinimo ar keitimo.
