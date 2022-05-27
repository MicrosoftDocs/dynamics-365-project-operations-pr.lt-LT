---
title: Fiksuotos kainos pajamų įvertinimo projektai
description: Šioje temoje pateikiama informacijos apie fiksuotos kainos pajamų naudojimą projektuose.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 290608e5663f9c953212c156771bbf1ad6b1e901
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578718"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Fiksuotos kainos pajamų įvertinimo projektai 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Kai kuriate projekto sutarties eilutę naudodami toliau nurodytus atributus programoje „Dynamics 365 Project Operations“, esančioje „Microsoft Dataverse“, sistema automatiškai sukuria fiksuotos kainos pajamų įvertinimo projektą. Šio projekto informacija pagrįsta toliau nurodytais elementais.

  - Fiksuotos kainos atsiskaitymo metodas.
  - Susietas projektas.
  - Bent vienas etapas, apibrėžtas puslapio **Projekto sutarties eilutė** skirtuke **Sąskaitos faktūros grafikas**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Fiksuotos kainos pajamų įvertinimo projektų peržiūra
Norėdami peržiūrėti fiksuotos kainos pajamų įvertinimo projektus, atlikite toliau nurodytus veiksmus.

1. Dynamics 365 Finance aplinkoje eikite į **Projektų valdymo ir apskaitos** > **projektai** > **Fiksuotos kainos pajamų sąmatos projektai**.
2. Pasirinkite projektą, kurį norite peržiūrėti, ir dukart spustelėkite **Vertinamo projekto ID**, kad atidarytumėte įrašą ir peržiūrėtumėte projekto informaciją.
3. Išplėskite skirtuką **Projektas**. Matysite vieną projektą tinklelyje **Pasirinkti projektai**. Sistema naudoja jį kaip numatytąjį projektą, nes tai yra projektas, susietas su projekto sutarties eilute. 
4. Norėdami pakeisti susiejimą, pasirinkite papildomus projektus ir pridėkite juos prie tinklelio **Pasirinkti projektai**. Jei šiame tinklelyje pasirenkami keli projektai, projekto įvykdymo procentinė vertė ir pajamų įvertinimai apskaičiuojami kartu visiems pasirinktiems projektams.

  Projekto išlaidas, pajamų profilį, sąnaudų šabloną ir laikotarpio kodą galima nustatyti rankiniu būdu. Jei jie nenustatomi rankiniu būdu, nustatomos numatytosios reikšmės atliekant pirmąjį įvertinimo skaičiavimą remiantis sukonfigūruotomis projekto išlaidų ir pajamų profilių taisyklėmis.



[!INCLUDE[footer-include](../includes/footer-banner.md)]