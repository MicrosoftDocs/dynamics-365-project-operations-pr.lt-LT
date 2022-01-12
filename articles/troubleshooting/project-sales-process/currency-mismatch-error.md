---
title: Valiutos neatitikimo klaida
description: Šioje temoje pateikiama trikčių šalinimo informacija apie valiutos neatitikimo klaidą, kuri atsiranda įrašant konkrečius įrašų tipus.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903729"
---
# <a name="currency-mismatch-error"></a>Valiutos neatitikimo klaida 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Įrašę projektą, sutartį, pasiūlymą ar rezervuojamą išteklių, galite gauti **klaidą, įmonės valiutos turėjimas neatitinka sutarties vieneto valiutos. Norėdami tęsti, pasirinkite kitą valdymo įmonę arba perkančiosios organizacijos vienetą**. Taip yra todėl, kad yra valiutos neatitikimas tarp įrašo perkančiosios vieneto valiutos ir turinčios įmonės valiutos.


## <a name="resolution"></a>Vertinimas

Norėdami išspręsti šią problemą, atlikite šiuos veiksmus:
- Patikrinkite šio įrašo perkančiojo vieneto valiutą. Valiutą galite matyti atidarę organizacijos vieneto įrašą ir patikrinę **lauko Valiuta skirtuko Bendra** **vertę**.
- Patikrinkite valdončios įmonės valiutą. Valiutą galite matyti įmonės **įraše nuvykę į Susijusios** > **knygos**. Dukart spustelėkite dk įrašą, susietą su įmone, ir **patikrinkite** vertę lauke Bendra, esančiame **lauke Apskaitos** valiuta.

Jei sutarties vienete nustatyta valiuta ir DK įrašas nesutampa, įrašydami įrašą koreguokite konfigūraciją arba pasirinkite skirtingas vertes. Sistema reikalauja, kad šie įrašai atitiktų, kad būtų užtikrinti teisingi vidinės įmonės SF išrašymo srautai. Daugiau informacijos apie vidinės įmonės konfigūracijas ieškokite [Create vidinės įmonės operacijas](../../project-accounting/create-intercompany-transactions.md).

Jei įmonės įraše nėra susieto DK įrašo, tai rodo, kad nustatant aplinką trūksta konfigūracijos. Konfigūraciją turi pataisyti sistemos administratorius. Sistemos administratorius turi eiti į **dvigubo rašymo konfigūracijas** ir sustabdyti bei iš naujo paleisti **Ledgers dvigubo rašymo žemėlapį** su pradiniu šio žemėlapio sinchronizavimu ir jo prielaidomis. Daugiau informacijos žr. [„Project Operations“ dvigubo rašymo schemų versijas](../../environment/resource-dual-write-maps.md).
