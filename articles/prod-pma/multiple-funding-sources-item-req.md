---
title: Prekių reikalavimai projekto sutartims su keliais finansavimo šaltiniais
description: Šiame straipsnyje pateikiama informacija apie tai, kaip konfigūruoti ir naudoti elementų reikalavimus naudojant kelis finansavimo šaltinius.
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

Kai kuriems sutartiniams susitarimams dėl projektais pagrįstų rezultatų gali prireikti kelių finansavimo šaltinių. Šiame straipsnyje paaiškinama, kaip pasirinkti ir konfigūruoti norimus finansavimo šaltinius, kai projektui ar projekto sutarčiai reikalingi keli šaltiniai.

## <a name="terminology"></a>Terminai

- **Finansavimo šaltinis** – subjektas, finansuojantis projekto sutarties darbą. Šis objektas gali būti vidinė organizacija arba išorinė SF sąskaita (klientas arba dotacija).
- **Projekto klientas** – objektas, kuriam pristatomas projekto darbas.
- **Sąskaitos faktūros sąskaita** – išorinis objektas, kuris moka už projekto darbą.

## <a name="example"></a>Pavyzdžiui

Contoso laimėjo įrangos atnaujinimo sutartį su dviem savo klientais: "Adatum US" ir "Adatum Corporate". Sutartis apima techninės įrangos ir diegimo paslaugas, kurios bus pristatytos į "Adatum US" (projekto klientą). Aparatinę įrangą finansuos "Adatum Corporate" (1 sąskaitos faktūros sąskaita), o montavimo darbus finansuos "Adatum US" (2 sąskaitos faktūros sąskaita).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Numatytųjų sąskaitos faktūros abonemento taisyklių, taikomų prekių reikalavimams, nustatymas

### <a name="prerequisites"></a>Būtinosios sąlygos

- Microsoft Dynamics 365"Finance" **10.0.27 arba naujesnė** versija reikalinga norint naudoti prekių reikalavimus, kurie turi kelias sąskaitų faktūrų sąskaitas faktūras.
- Jūsų sistemos administratorius turi įgalinti **reikalavimus Leisti elementą su keliais "Project Operations" sandėliuojamų / gamyba pagrįstų scenarijų finansavimo šaltiniais** darbo srityje Funkcijų **valdymas**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Numatytųjų sąskaitos faktūros paskyros taisyklių nustatymas

Norėdami nustatyti numatytąsias sąskaitos faktūros paskyros taisykles, atlikite šiuos veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.
1. Skirtuko **Bendra** sekcijoje **Pardavimo užsakymai ir prekių reikalavimai** nustatykite **parinktį Leisti projektams su keliais finansavimo šaltiniais** į **Taip**.
1. **Lauke Numatytasis klientas** nurodykite, iš kur pagal numatytuosius nustatymus gaunamas projekto pristatymo klientas pagal prekės reikalavimą:

    - **Iš finansavimo šaltinio** – numatytasis projekto pristatymo klientas gaunamas iš finansavimo šaltinio. Jei su projekto sutartimi siejami keli finansavimo šaltiniai, bus naudojamas pirmasis sąraše esantis finansavimo šaltinis.
    - **Iš projekto** – numatytasis projekto pristatymo klientas gaunamas iš kliento, pasirinkto **lauke Projekto įrašo abonementas**.

1. Pasirinktinai: nustatykite arba pakeiskite numatytąją sąskaitos faktūros paskyrą projekto įrašuose:

    1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir atidarykite išsamią projekto įrašo informaciją.
    2. Skirtuke **Bendra** nustatykite arba atnaujinkite lauką Numatytoji **sąskaitos faktūros sąskaita** faktūra. Jūsų nurodytas abonementas bus naudojamas kaip numatytoji sąskaitos faktūros sąskaita naujiems prekės reikalavimams, sukurtiems projektui. Jei paliksite lauką tuščią, pagal numatytuosius nustatymus bus naudojama pirmojo projekto sutarties finansavimo šaltinio sąskaitos faktūros sąskaita faktūra. Tačiau vartotojai galės pakeisti paskyrą, kai įrašys įrašą.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Pasirinkite sąskaitos faktūros paskyrą, kurią naudosite kurdami prekės reikalavimą

Norėdami pasirinkti sąskaitos faktūros paskyrą, kurią norite naudoti kurdami prekės reikalavimą, atlikite šiuos veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir pasirinkite projekto įrašą.
1. Skirtuke **Planas** pasirinkite **Elemento reikalavimai**.
1. Sukurkite naują elemento reikalavimo įrašą.

    - Pagal numatytuosius **nustatymus įrašo lauke Sąskaitos faktūros paskyra** nustatoma kaip sf abonementas, nustatytas projektui. Galite pakeisti lauko Sąskaitos faktūros abonementas **reikšmę** ir tada įrašyti įrašą. Įrašę įrašą, nebegalite naujinti **sąskaitos faktūros abonemento** reikšmės. Jei turite atnaujinti **prekės reikalavimo sąskaitos faktūros paskyros** reikšmę, panaikinkite esamą prekės reikalavimą ir sukurkite naują, turintį norimą reikšmę.
    - Pagal numatytuosius **parametrus prekės reikalavimo laukas Klientas** nustatomas pagal numatytąją **kliento** reikšmę, nustatytą **puslapyje Projekto valdymo ir apskaitos parametrai**.

    Įrašius prekės poreikio įrašą, sistema susieja jį su prekės reikalavimo pardavimo užsakymo **antraštės** įrašu. Jei nė vienoje atidaryto pardavimo užsakymo antraštėje nėra pasirinktos SF sąskaitos faktūros, sistema ją sukurs ir susies su juo prekės reikalavimo eilutę.

> [!NOTE]
> Prekių reikalavimai visada visiškai išrašomi sąskaitoje faktūroje nurodytame sąskaitos faktūros abonemente, kuris nustatytas įraše. Šiuo metu sistema nepalaiko finansavimo paskirstymo taisyklių, kuriose taikomi elementų reikalavimai, ir ji neskirstys registravimo pagal finansavimo paskirstymo taisyklių nustatymą.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Elemento reikalavimo kūrimas iš elemento prognozės įrašo

Norėdami sukurti elemento reikalavimą iš prekės prognozės įrašo, atlikite šiuos veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir pasirinkite projekto įrašą.
1. Skirtuke **Planas** pasirinkite **Elementų prognozės**.
1. Naujo elemento prognozės įrašo kūrimas.
1. Pasirenkama: skirtuko **Projektas** **lauke Finansavimo šaltinis** pasirinkite norimą sąskaitos faktūros sąskaitą.
1. Pasirinkite **Sukurti elemento reikalavimą** ir patvirtinkite gautą pranešimą.

    > [!NOTE]
    > Sistema nukopijuoja finansavimo šaltinio **reikšmę** iš prekės prognozės įrašo į naujai sukurtą elemento reikalavimo įrašą.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Numatytoji sąskaitos faktūros sąskaita faktūra, kai sistema automatiškai sukuria prekės reikalavimą iš pirkimo užsakymo eilutės

Jei parinktis Kurti elemento reikalavimą **puslapyje** Projekto valdymas ir apskaitos parametrai **nustatyta kaip** Taip **·**, sistema automatiškai sukuria elemento reikalavimą, kai įrašoma nauja projekto pirkimo užsakymo eilutė. Pagal numatytuosius **nustatymus laukai Sąskaitos faktūros sąskaita** ir **prekės reikalavimas** nustatomi kaip projekto įrašo lauko Numatytoji **sąskaitos faktūros sąskaita** reikšmė. Šiuo metu sistema nepalaiko tokio tipo įrašų sąskaitos faktūros abonemento naujinimo ar keitimo.
