---
title: Sąskaitų faktūrų įsiskolinimų peržiūra projektuose ir projektų sutartyse
description: Šiame straipsnyje pateikiama informacija apie tai, kaip peržiūrėti laiko, savikainos ir produktų įsiskolinimus ir kaip juos pažymėti kaip paruoštus išrašyti sąskaitą faktūrą.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 833ace7fd6285191f4b023a029286cd36b5de8f4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928902"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Sąskaitų faktūrų įsiskolinimų peržiūra projektuose ir projektų sutartyse

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kai operacijai galima išrašyti sukurtą ir apdorotą sąskaitą faktūrą, operaciją reikia pažymėti kaip **Paruošta išrašyti sąskaitą faktūrą**. Šiame straipsnyje aprašyti operacijų tipai, kuriuos galima sukurti.

## <a name="review-the-time-and-material-billing-backlog"></a>Laiko ir medžiagų atsiskaitymo įsiskolinimų peržiūra

Kai laiko arba savikainos įrašas yra pateikiamas ir patvirtinamas projektui, PSA sukuria faktinį projektą. Jei projekto ir operacijos klasė yra susiejama su laiko ir medžiagų projekto sutarties eilute, sukuriami du faktiniai elementai, kai įrašas patvirtinamas:

- Faktinė savikaina 
- Pardavimas, už kurį neišrašyta sąskaita

Pardavimo, už kurį neišrašyta sąskaita, faktiniai elementai nurodo atsiskaitymo įsiskolinimą, ir jų atsiskaitymo būsena turi būti nustatyta į **Paruošta išrašyti sąskaitą faktūrą**. Sukūrus projekto sąskaitą faktūrą, pardavimo, už kurį neapmokėta, faktiniai elementai, pažymėti kaip **Paruošta išrašyti sąskaitą faktūrą**, nukopijuojami kaip sąskaitos faktūros eilutės informacija.

Jei norite peržiūrėti laiko ir medžiagos sąskaitų siuntimo nežurnalą, pereikite į **Pardavimai** \> **Sąskaitos** \> **Laiko ir medžiagų atsiskaitymo peržiūra**. Pažymėkite visus pardavimo, už kurį neišrašyta sąskaita, faktinius elementus, kurie paruošti sąskaitos faktūros išrašymui, tada pažymėkite **Paruošta išrašyti sąskaitą faktūra**. Šių faktinių elementų atsiskaitymo būsena pakeičiama į **Paruošta išrašyti sąskaitą faktūrą**.

![Laiko ir medžiagų atsiskaitymo nebaigtos užduotys.](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Produktų atsiskaitymo įsiskolinimų peržiūra

PSA, kai projekto sutartyje yra produktu pagrįstų sutarties eilučių, šios eilutės laikomos paruoštos sąskaitos faktūros išrašymui, kai tik projekto sutarčiai sukuriama sąskaita faktūra. Visi projektai, kurie turi sutarties eilučių, kurios pažymėtos kaip **Paruošta išrašyti sąskaitą faktūrą**, yra nukopijuojami į projekto sąskaitą faktūrą kaip projekto sąskaitos faktūros eilutės.

Norėdami peržiūrėti produktų sąskaitų siuntimo žurnalą **Pardavimai** \> **Sąskaitų išrašymas** \> **Produktų sąskaitų faktūrų išrašymas**. Pažymėkite visas produktu pagrįstas sutarties eilutes, kurios paruoštos sąskaitos faktūros išrašymui, tada pažymėkite **Paruošta išrašyti sąskaitą faktūrą**. Šių eilučių atsiskaitymo būsena pakeičiama į **Paruošta išrašyti sąskaitą faktūrą**.

![Produktų atsiskaitymo nebaigtos užduotys.](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Fiksuotos kainos sutarčių atsiskaitymo etapų peržiūra

Kiekvienoje projekto sutarties eilutėje, kuriai taikomas fiksuotos kainos atsiskaitymo metodas, turi būti apibrėžti sutarties etapai. Šiems sutarties etapams sąskaitą faktūrą galima išrašyti, tik jei jie pažymėti kaip **Paruošta išrašyti sąskaitą faktūrą**. 

Norėdami peržiūrėti atsiskaitymo etapus, į **Pardavimai** \> **Sąskaitos** \> **Fiksuotas kainų gairės.** Pažymėkite visus etapus, kurie paruošti sąskaitos faktūros išrašymui, tada pažymėkite **Paruošta išrašyti sąskaitą faktūrą**. Šių etapų atsiskaitymo būsena pakeičiama į **Paruošta išrašyti sąskaitą faktūrą**.

![Fiksuotos kainos gairės.](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
