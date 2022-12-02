---
title: Valiutos neatitikimo klaida
description: Šiame straipsnyje pateikiama trikčių diagnostikos informacija apie valiutos neatitikimo klaidą, įvykstančią įrašant tam tikrų tipų įrašus.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914734"
---
# <a name="currency-mismatch-error"></a>Valiutos neatitikimo klaida 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Įrašant projektą, sutartį, pasiūlymą ar rezervuojamus išteklius gali įvykti klaida: **Valdančios įmonės valiuta nesutampa su sutartį sudarančio vieneto valiuta. Norėdami tęsti, pasirinkite kitą valdančią įmonę arba sutartį sudarantį vienetą**. Ji įvyksta todėl, kad yra sutartį sudarančio vieneto valiutos ir valdančios įmonės valiutos neatitikimas.


## <a name="resolution"></a>Vertinimas

Norėdami išspręsti šią problemą, atlikite toliau nurodytus veiksmus.
- Patikrinkite šio įrašo sutartį sudarančio vieneto valiutą. Valiutą galite matyti atidarę organizacinio vieneto įrašą ir patikrinę reikšmę skirtuke **Bendra** esantį lauką **Valiuta**.
- Patikrinkite valdančios įmonės valiutą. Valiutą galite matyti įmonės įraše nuėję **Susiję** > **Didžiosios knygos**. Dukart spustelėkite su įmone susietą didžiąją knygą ir patikrinkite reikšmę, esančią skirtuko **Bendra** lauke **Apskaitos valiuta**.

Jei sutartį sudarančio vieneto ir didžiosios knygos įrašo nustatyta valiuta nesutampa, pakoreguokite konfigūraciją arba įrašydami įrašą pasirinkite kitas reikšmes. Sugretinant sistemai reikia šių įrašų, kad būtų užtikrinti tinkami vidiniai įmonės sąskaitų faktūrų išrašymo srautai. Daugiau informacijos apie vidines įmonės konfigūracijas žr. [Vidinių įmonės operacijų kūrimas](../../project-accounting/create-intercompany-transactions.md).

Jei įmonės įrašas neturi susieto didžiosios knygos įrašo, tai reiškia, kad nustatant aplinką nesukurta konfigūracija. Konfigūraciją turi pataisyti sistemos administratorius. Sistemos administratorius turi eiti į **Dvigubo rašymo konfigūracijos**, tada sustabdyti ir iš naujo paleisti **Didžiųjų knygų dvigubo rašymo schemą** ir atlikti pradinį šios schemos ir jos būtinųjų sąlygų sinchronizavimą. Daugiau informacijos žr. [„Project Operations“ dvigubo rašymo schemų versijas](../../environment/resource-dual-write-maps.md).
