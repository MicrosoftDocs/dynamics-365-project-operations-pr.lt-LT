---
title: Planavimo režimai
description: Šioje temoje pateikta informacijos apie planavimo režimus.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: cb507528c4815f5149c813bba0a354f7d840a4a5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588424"
---
# <a name="scheduling-modes"></a>Planavimo režimai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


„Dynamics 365 Project Operations“ organizacijoms suteikia galimybę apibrėžti, kaip jos valdo pagrindinių kintamųjų pakeitimus darbo paskirstymo struktūros užduotyse. Atsižvelgdami į konkrečius organizacijos poreikius, projektų vadovai kurdami projektą gali atlikti planavimo režimo pakeitimų.

Sprendime „Project Operations“ galimi trys toliau nurodyti planavimo režimai.

  - Fiksuota trukmė (tai yra numatytasis režimas)
  - Fiksuotos pastangos (*Darbas*)
  - Fiksuoti vienetai

Reikšmės, kurioms turi įtakos konkretaus planavimo režimo apibrėžimas, nustatomos pagal toliau nurodytą formulę.

  Pastangos = trukmė x vienetai

Kai nustatote projekto planavimo režimą, nustatote vieną iš šių reikšmių, kurių keisti negalima. Laikant šią reikšmę vienodą, jai suteikiama pirmenybė, o sistemai pranešama jos nekeisti pasikeitus kitoms dviem reikšmėms. Toliau pateiktoje lentelėje pateikiama informacija apie konkretaus režimo pasirinkimo poveikį.

| **Šioje užduotyje**             | **Jei peržiūrite vienetus**   | **Jei peržiūrite trukmę** | **Jei peržiūrite pastangas**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Fiksuotų vienetų užduotis     | Trukmė perskaičiuojama. | Pastangos perskaičiuojamos.    | Trukmė perskaičiuojama. |
| Fiksuotų pastangų užduotis    | Trukmė perskaičiuojama. | Vienetai perskaičiuojami.    | Trukmė perskaičiuojama. |
| Fiksuotos trukmės užduotis  | Pastangos perskaičiuojamos.   | Pastangos perskaičiuojamos.    | Vienetai perskaičiuojami.   |

Norėdami daugiau sužinoti apie tam tikro režimo poveikį, žr. [Užduoties tipo keitimas norint tiksliau planuoti](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). Temoje vietoj termino **Pastangos** naudojamas terminas **Darbas**.

## <a name="change-the-organizations-scheduling-mode"></a>Organizacijos planavimo režimo keitimas

Norėdami apibrėžti organizacijos planavimo režimą, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Parametrai** \> **Bendra** \>**Parametrai** ir pasirinkite projekto parametrą. 
2. Puslapyje **Projekto parametrai** pasirinkite numatytąjį organizacijos planavimo režimą, tada apibrėžkite projekto vadovo galimybę perrašyti parametrą kuriant naują projektą.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Projekto planavimo režimo parametro keitimas

Jei organizacija projekto vadovui leidžia perrašyti numatytąjį planavimo režimą, projekto vadovas gali jį pakeisti kurdami naują projektą. Tačiau įrašius projektą planavimo režimo keisti negalima.

## <a name="copied-projects"></a>Nukopijuoti projektai

Kadangi projektas sukuriamas atliekant projekto kopijavimo veiksmą, projekto vadovas negali nustatyti planavimo režimo. Numatyta, kad paskirties projektas visada bus nustatytas kaip organizacijos lygiu apibrėžtas projektas.

## <a name="copied-tasks"></a>Nukopijuotos užduotys

Kai užduotis nukopijuojama iš vieno projekto į kitą, ji paveldi paskirties projekto planavimo režimą.
