---
title: Atsargose nelaikomų medžiagų įsigijimas naudojant laukiančią tiekėjo sąskaitą faktūrą
description: Šioje temoje paaiškinama, kaip įrašyti laukiančias tiekėjų sąskaitas faktūras.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009046"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Atsargose nelaikomų medžiagų įsigijimas naudojant laukiančią tiekėjo sąskaitą faktūrą

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Kai įmonė projektui įsigyja atsargose nelaikomų medžiagų, galima iš karto įrašyti projekto kaštus. 

Pavyzdžiui, „Contoso Robotics US“ vykdo įrangos atnaujinimo projektą ir turi gauti programinės įrangos licencijų. Šios licencijos įsigyjamos iš trečiosios šalies tiekėjo.  Naudodamas „Dynamics 365 Finance“, mokėtinų sumų klerkas įrašo laukiančios tiekėjo sąskaitos faktūros dokumentą, o licencijos kaštus tiesiogiai priskiria įrangos atnaujinimo projektui. 

> [!IMPORTANT]
> Prieš naudodami šioje temoje aprašytas funkcijas, peržiūrėkite ir pritaikykite reikiamas konfigūracijas. Norėdami sužinoti daugiau, žr. [Galimybės naudoti atsargose nelaikomas medžiagas ir laukiančias tiekėjų sąskaitas faktūras įjungimas](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Su projektu susijusios laukiančios tiekėjo sąskaitos faktūros registravimas 

Laukiančias tiekėjų sąskaitas faktūras galima įrašyti puslapyje **Laukiančios tiekėjų sąskaitos faktūros** (**Mokėtinos sumos** > **Sąskaitos faktūros** > **Laukiančios tiekėjų sąskaitos faktūros**). Norėdami registruoti su projektu susijusią laukiančią tiekėjo sąskaitą faktūrą, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Mokėtinos sumos** > **Sąskaitos faktūros** ir pasirinkite **Nauja**. 
2. Lauke **Sąskaitos faktūros klientas** pasirinkite tiekėją, o lauke **Numeris** įveskite tiekėjo sąskaitos faktūros identifikavimo duomenis.
3. Į tiekėjo sąskaitą faktūrą įtraukite eilutę, o lauke **Prekės numeris** pasirinkite iš tiekėjo įsigytą atsargose nelaikomą prekę. 

    > [!NOTE]
    > Tiekėjų sąskaitų faktūrų eilučių, pagrįstų viešųjų pirkimų kategorija, pagal projektą įrašyti negalima. 
    
5. Įtraukite įsigytą kiekį. Sistema automatiškai įves vieneto kainą pagal ne atsargose laikomos prekės kainos konfigūraciją. 
6. Patikrinkite bendrąją sumą ir kitą reikiamą informaciją eilutėje.
7. Eilutės išsamios informacijos srities skirtuke **Projektas** pasirinkite projekto, į kurį bus įrašoma ši prekė, ID.
8. Arba pasirinkite veiklos numerį ir atnaujinkite projekto kategoriją bei eilutės ypatybę.
9. Užregistruokite laukiančią tiekėjo sąskaitą faktūrą. Kai sąskaita faktūra užregistruojama, sistema įrašo toliau nurodytus dalykus.
    
    - Tiekėjo balanso suma.
    - PVM suma.
    - Projekto kaštai įrašomi į viešųjų pirkimų integravimo sąskaitą.
    - Projekto faktinė operacija sprendime „Dataverse“. Ši operacija toliau apdorojama naudojant [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md). Užregistravus šį žurnalą, suma iš viešųjų pirkimų integravimo sąskaitos perkeliama į projekto kaštų sąskaitą.
