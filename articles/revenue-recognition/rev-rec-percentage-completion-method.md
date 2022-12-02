---
title: Fiksuotos kainos pajamų įvertinimo projektai
description: Šiame straipsnyje pateikiama informacijos apie fiksuotos kainos pajamų naudojimą projektuose.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928396"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Fiksuotos kainos pajamų įvertinimo projektai 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Kai kuriate projekto sutarties eilutę naudodami toliau nurodytus atributus programoje „Dynamics 365 Project Operations“, esančioje „Microsoft Dataverse“, sistema automatiškai sukuria fiksuotos kainos pajamų įvertinimo projektą. Šio projekto informacija pagrįsta toliau nurodytais elementais.

  - Fiksuotos kainos atsiskaitymo metodas.
  - Susietas projektas.
  - Bent vienas etapas, apibrėžtas puslapio **Projekto sutarties eilutė** skirtuke **Sąskaitos faktūros grafikas**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Fiksuotos kainos pajamų įvertinimo projektų peržiūra
Norėdami peržiūrėti fiksuotos kainos pajamų įvertinimo projektus, atlikite toliau nurodytus veiksmus.

1. „Dynamics 365 Finance“ aplinkoje eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Fiksuotos kainos pajamų įvertinimo projektai**.
2. Pasirinkite projektą, kurį norite peržiūrėti, ir dukart spustelėkite **Vertinamo projekto ID**, kad atidarytumėte įrašą ir peržiūrėtumėte projekto informaciją.
3. Išplėskite skirtuką **Projektas**. Matysite vieną projektą tinklelyje **Pasirinkti projektai**. Sistema naudoja jį kaip numatytąjį projektą, nes tai yra projektas, susietas su projekto sutarties eilute. 
4. Norėdami pakeisti susiejimą, pasirinkite papildomus projektus ir pridėkite juos prie tinklelio **Pasirinkti projektai**. Jei šiame tinklelyje pasirenkami keli projektai, projekto įvykdymo procentinė vertė ir pajamų įvertinimai apskaičiuojami kartu visiems pasirinktiems projektams.

  Projekto išlaidas, pajamų profilį, sąnaudų šabloną ir laikotarpio kodą galima nustatyti rankiniu būdu. Jei jie nenustatomi rankiniu būdu, nustatomos numatytosios reikšmės atliekant pirmąjį įvertinimo skaičiavimą remiantis sukonfigūruotomis projekto išlaidų ir pajamų profilių taisyklėmis.



[!INCLUDE[footer-include](../includes/footer-banner.md)]