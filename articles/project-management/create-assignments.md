---
title: Išteklių priskyrimų kūrimas
description: Šioje temoje pateikta informacija apie bendrųjų ir įvardytųjų išteklių priskyrimų kūrimą.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d2e7c9a340a482a62afc0c9f0aa46c24fda27ca6ef56fdc0160f06af846c0b53
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987896"
---
# <a name="create-resource-assignments"></a>Išteklių priskyrimų kūrimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


Išteklių priskyrimas yra tiesioginė projekto komandos nario jungtis į lapų mazgo užduotį. Šioje temoje pateikiama informacija apie skirtingus išteklių priskyrimo būdus.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Bendrojo komandos nario kūrimas priskiriant užduotį


Kurdami bendrąjį komandos narį per užduoties priskyrimą, jūs sukuriate vietos rezervavimo ženklą arba bendrąjį išteklių. Šis bendrasis išteklius apibūdina įvardytųjų išteklių, su kuriais norite dirbti atlikdami užduotis, charakteristikas. Tada galite generuoti reikalavimą arba pateikti užklausą naudojant reikalavimą, kuris yra naudojamas įvardytųjų išteklių paieškai ir rezervavimui atlikti.

1. Užduoties grafiko tinklelyje pasirinkite langelyje **Ištekliai** esančią išteklių piktogramą.
2. Įveskite pavadinimą, kuris bus vietos rezervavimo ženklo išteklių pavadinimas. Pavyzdžiui, „Programos vadovas“.
3. Pasirinkite **„Kurti“**, o tada lauke **„Spartusis projekto komandos nario kūrimas“** nustatykite bendrųjų išteklių vaidmenį.
4. Užduočiai pasirinkdami išteklių parinktyje **Išteklių išrinkiklis**, priskirkite užduotis šiems vietos rezervavimo ženklo ištekliams. Ištekliai išvardyti skirtuke **Komandos nariai**.
5. Baigę bendrojo ištekliaus priskyrimą, skirtuke **Komanda** pasirinkite bendrąjį išteklių, o tada pasirinkite **Generuoti reikalavimą**, kad sukurtumėte ištekliaus reikalavimą, skirtą bendrajam ištekliui.
6. Bendrajam ištekliui pasirinkite **Rezervuoti**, o tada naudokite grafiko lentą, kad surastumėte ir užrezervuotumėte tikrus išteklius. Taip pat galite išteklių vadovui pateikti reikalavimą, kad jis būtų įvykdytas.
7. Kai bendrasis išteklius visiškai įvykdytas (vykdant dalinį išteklių reikalavimą išteklius nebus priskiriamas) su įvardytuoju ištekliumi, bendrasis išteklius pašalinamas iš komandos. Bendriesiems ištekliams užduotys priskiriamos įvardytajam ištekliui, kuris įvykdė bendrojo ištekliaus reikalavimą.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Įvardytų išteklių priskyrimas iš visų rezervuojamų išteklių sąrašo

Norėdami ieškoti visų aktyvių rezervuojamų išteklių ir juos priskirti prie bet kurios lapo mazgo užduoties, galite naudoti ieškos laukelį, esantį parinktyje **Išteklių parinkiklis**. Tokiu būdu priskirti ištekliai įtraukiami į komandą neatliekant jokių rezervacijų. Taip pat galima įtraukti komandos narį ir vietoje paskirstymo metodo pažymėti **Nėra**. Ištekliai rodomi skirtukuose **Komanda**, **Išteklių priskyrimas** ir **Suderinimas** kaip ištekliai, turintys tik priskyrimus ir rezervavimo deficitą. Jei norite pasinaudoti jų prieinamumu, juos rezervuokite.

1. Užduočių tinklelyje, lentoje arba laiko planavimo juostoje pereikite prie langelio **Priskirta (kam)**.
2. Ieškos lauke pradėkite vesti pavadinimą. Pavadinimo ieškos rezultatai pateikiami **„Išteklių išrinkiklis“**, parinktyje **„Kiti ištekliai“**.
3. Pažymėkite išteklių, kurį norite priskirti užduočiai arba pažymėkite ištekliaus pavadinimą parinktyje **Kiti komandos ištekliai**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]