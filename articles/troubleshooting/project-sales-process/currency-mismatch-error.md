---
title: Valiutos neatitikimo klaida
description: Šioje temoje pateikiama trikčių šalinimo informacija apie valiutos neatitikimo klaidą, kuri įvyksta įrašant konkrečius įrašų tipus.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589758"
---
# <a name="currency-mismatch-error"></a>Valiutos neatitikimo klaida 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Kai įrašote projektą, sutartį, pasiūlymą ar rezervuojamą išteklių, galite gauti klaidą, **valdomos įmonės valiuta neatitinka perkančiojo vieneto valiutos. Norėdami tęsti, pasirinkite kitą valdončią įmonę arba perkančiąjį vienetą**. Taip yra todėl, kad įrašo perkančiojo vieneto valiuta nesutampa su įrašo ir nuosavybės teise priklausančios įmonės valiuta.


## <a name="resolution"></a>Vertinimas

Norėdami išspręsti šią problemą, atlikite šiuos veiksmus:
- Patikrinkite šio įrašo perkančiojo vieneto valiutą. Valiutą galite pamatyti atidarę organizacinio vieneto įrašą ir patikrinę vertę skirtuke **Bendra**, esančiame **lauke Valiuta**.
- Patikrinkite nuosavybės teise priklausančios įmonės valiutą. Valiutą galite pamatyti įmonės įraše nuėję į **Susijusios** > **knygos**. Dukart spustelėkite dk įrašą, susietą su įmone, ir patikrinkite vertę, esančią **lauke Apskaitos valiuta** esančiame skirtuke **Bendra**.

Jei sutarties vienete nustatyta valiuta ir DK įrašas nesutampa, įrašykite įrašą koreguokite konfigūraciją arba pasirinkite skirtingas vertes. Sistemai reikia, kad šie įrašai atitiktų reikalavimus, kad būtų užtikrinti teisingi vidinės įmonės SF išrašymo srautai. Daugiau informacijos apie vidinės įmonės konfigūracijas ieškokite [Create intercompany transactions](../../project-accounting/create-intercompany-transactions.md).

Jei įmonės įraše nėra susieto DK įrašo, tai rodo, kad nustatant aplinką trūksta konfigūracijos. Konfigūraciją turi pataisyti sistemos administratorius. Sistemos administratorius turi pereiti į **dvigubo rašymo konfigūracijas** ir sustabdyti bei iš naujo paleisti **DK dvigubo rašymo žemėlapį**, iš pradžių sinchronizuodamas šį žemėlapį ir tai yra būtinos sąlygos. Daugiau informacijos žr. [„Project Operations“ dvigubo rašymo schemų versijas](../../environment/resource-dual-write-maps.md).
