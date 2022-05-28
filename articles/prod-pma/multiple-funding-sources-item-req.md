---
title: Projekto sutarčių su keliais finansavimo šaltiniais prekių reikalavimai
description: Šioje temoje pateikiama informacija apie tai, kaip konfigūruoti ir naudoti prekių poreikius su keliais lėšų skyrimo šaltiniais.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d4af03e02d3c2eb0d442e6213ff5b9cf583d54b3
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8728090"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Projekto sutarčių su keliais finansavimo šaltiniais prekių reikalavimai

_**Taikoma (kam):**„Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_

Kai kuriems sutartiniams susitarimams dėl projektų rezultatų gali prireikti kelių finansavimo šaltinių. Šioje temoje paaiškinama, kaip pasirinkti ir konfigūruoti norimus lėšų skyrimo šaltinius, kai projektui ar projekto sutarčiai reikalingi keli šaltiniai.

## <a name="terminology"></a>Terminai

- **Finansavimo šaltinis** – subjektas, finansuojantis projekto rangos darbus. Šis objektas gali būti vidinė organizacija arba išorinė SF sąskaita (klientas arba dotacija).
- **Projekto klientas** – objektas, kuriam pristatomas projekto darbas.
- **SF sąskaita** – išorinis subjektas, kuris moka už projekto darbą.

## <a name="example"></a>Pavyzdžiui

Contoso laimėjo įrangos atnaujinimo sutartį su dviem savo klientais: "Adatum US" ir "Adatum Corporate". Sutartis apima techninės įrangos ir diegimo paslaugas, kurios bus pristatytos "Adatum US" (projekto klientui). Aparatinę įrangą finansuos "Adatum Corporate" (sąskaitos faktūros sąskaita 1), o diegimo darbus finansuos "Adatum US" (2 sąskaitos faktūros sąskaita).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Nustatyti SF sąskaitos numatytąsias taisykles, skirtas prekių poreikiams

### <a name="prerequisites"></a>Būtinosios sąlygos

- Microsoft Dynamics 365 Finansų ir operacijų **versija 10.0.27 arba naujesnė** versija reikalinga norint naudoti prekių reikalavimus, kuriuose yra kelios sąskaitos faktūros sąskaitos faktūros.
- Jūsų sistemos administratorius darbo srityje Funkcijų valdymas turi įgalinti **reikalavimus Leisti prekę su keliais projekto operacijų sukauptų / gamybos scenarijų finansavimo** šaltiniais **.**

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Nustatyti SF sąskaitos numatytąsias taisykles

Norėdami nustatyti numatytąsias SF sąskaitos taisykles, atlikite šiuos veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.
1. Skirtuko **Bendra** **skyriuje Pardavimo užsakymai ir Prekių poreikiai** nustatykite **parinktį Leisti projektus su keliais lėšų skyrimo šaltiniais** į **Taip**.
1. Lauke **Numatytasis pirkėjas** nurodykite, iš kur pagal numatytuosius nustatymus yra prekės poreikio projekto pristatymo klientas:

    - **Iš lėšų skyrimo šaltinio** – numatytasis projekto pristatymo klientas gaunamas iš finansavimo šaltinio. Jei su projekto sutartimi susieti keli finansavimo šaltiniai, bus naudojamas pirmasis sąrašo finansavimo šaltinis.
    - **Iš projekto** – numatytasis projekto pristatymo klientas gaunamas iš kliento, pasirinkto lauke **Projekto įrašo sąskaita**.

1. Pasirinktinai: nustatykite arba pakeiskite numatytąją SF sąskaitą projekto įrašuose:

    1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir atidarykite išsamią projekto įrašo informaciją.
    2. Skirtuke **Bendra** nustatykite arba atnaujinkite lauką Numatytoji **SF sąskaita**. Jūsų nurodyta sąskaita bus naudojama kaip numatytoji SF sąskaita naujiems projektui sukurtiems prekių poreikiams. Jei paliksite lauką tuščią, pagal numatytuosius nustatymus bus naudojama pirmojo projekto sutarties lėšų skyrimo šaltinio SF sąskaita. Tačiau vartotojai galės pakeisti paskyrą, kai išsaugos įrašą.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Pasirinkti SF sąskaitą, kuri bus naudojama kuriant prekės poreikį

Norėdami pasirinkti SF sąskaitą faktūrą, kuri bus naudojama kuriant prekės poreikį, atlikite šiuos veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir pasirinkite projekto įrašą.
1. Skirtuke **Planas** pasirinkite **Prekės poreikiai**.
1. Sukurkite naują prekės poreikio įrašą.

    - Pagal numatytuosius nustatymus **įrašo SF sąskaitos** laukas nustatomas į SF sąskaitą, nustatytą projektui. Galite pakeisti sf sąskaitos **lauko vertę** ir įrašyti įrašą. Įrašę įrašą nebegalite atnaujinti **SF sąskaitos** vertės. Jei turite atnaujinti prekės poreikio **SF sąskaitos** vertę, panaikinkite esamą prekės poreikį ir sukurkite naują, kurio reikšmė yra norima.
    - Pagal numatytuosius nustatymus **prekės poreikio laukas Pirkėjas** nustatomas pagal numatytąją **kliento** vertę, nustatytą **puslapyje Projektų valdymo ir apskaitos parametrai**.

    Įrašius prekės poreikio įrašą, sistema susieja jį su Prekės poreikio **pardavimo užsakymo** antraštės įrašu. Jei nė vienoje atviro pardavimo užsakymo antraštėje nėra pasirinktos SF sąskaitos, sistema ją sukurs ir susies su ja prekės poreikio eilutę.

> [!NOTE]
> Prekės poreikiams visada išrašoma visa SF sąskaita faktūra, kuri nustatyta įraše. Sistema šiuo metu nepalaiko lėšų paskirstymo taisyklių, kuriose yra prekių poreikis, ir ji neskirstys registravimo pagal lėšų paskirstymo taisyklių nustatymą.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Prekės poreikio kūrimas iš prekės prognozės įrašo

Norėdami sukurti prekės poreikį iš prekės prognozės įrašo, atlikite šiuos veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir pasirinkite projekto įrašą.
1. Skirtuke **Planas** pasirinkite **Prekių prognozės**.
1. Sukurkite naują prekių prognozės įrašą.
1. Pasirinktinai: skirtuko **Projektas** **lauke Lėšų skyrimo šaltinis** pasirinkite norimą SF sąskaitą.
1. Pasirinkite **Kurti prekės poreikį** ir patvirtinkite gautą pranešimą.

    > [!NOTE]
    > Sistema nukopijuoja **lėšų skyrimo šaltinio** vertę iš prekės prognozės įrašo į naujai sukurtą prekės poreikio įrašą.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Numatytoji SF sąskaita, kai sistema automatiškai sukuria prekės poreikį iš pirkimo užsakymo eilutės

**Jei puslapyje Projektų valdymo ir apskaitos parametrai parinktis** Kurti prekės poreikį **nustatyta į** Taip **·**, sistema automatiškai sukuria prekės poreikį, kai įrašoma nauja projekto pirkimo užsakymo eilutė. Pagal numatytuosius nustatymus **laukai SF sąskaita** ir **Prekės poreikis** nustatomi kaip projekto įrašo lauko Numatytoji SF sąskaita **vertė**. Sistema šiuo metu nepalaiko šio tipo įrašų SF sąskaitos atnaujinimo ar keitimo.
