---
title: Atsargose nelaikomų medžiagų arba įsigijimo kategorijų įsigijimas naudojant laukiančią tiekėjo sąskaitą faktūrą
description: Šiame straipsnyje temoje paaiškinama, kaip įrašyti laukiančias tiekėjų sąskaitas faktūras.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922002"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Atsargose nelaikomų medžiagų arba įsigijimo kategorijų įsigijimas naudojant laukiančią tiekėjo sąskaitą faktūrą

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Kai įmonė projektui įsigyja atsargose nelaikomų medžiagų arba įsigijimo kategorijų, galima iš karto įrašyti projekto kaštus. 

Pvz., „Contoso Robotics US“ vykdo įrangos atnaujinimo projektą ir nori programinės įrangos licencijų. Šios licencijos įsigyjamos iš trečiosios šalies tiekėjo.  Naudodamas „Dynamics 365 Finance“, mokėtinų sumų klerkas įrašo laukiančios tiekėjo sąskaitos faktūros dokumentą, o licencijos kaštus tiesiogiai priskiria įrangos atnaujinimo projektui. 

> [!IMPORTANT]
> Prieš naudodami šiame straipsnyje aprašytas funkcijas, peržiūrėkite ir pritaikykite reikiamas konfigūracijas. Norėdami gauti daugiau informacijos, žr. [Galimybės naudoti atsargose nelaikomas medžiagas ir laukiančias tiekėjų sąskaitas faktūras įjungimas](configure-materials-nonstocked.md) ir [Tiekimo kategorijų naudojimas su projekto pirkimo užsakymais ir laukiančiomis sąskaitomis faktūromis](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Su projektu susijusios laukiančios tiekėjo sąskaitos faktūros registravimas 

Laukiančias tiekėjų sąskaitas faktūras galima įrašyti puslapyje **Laukiančios tiekėjų sąskaitos faktūros** (**Mokėtinos sumos** > **Sąskaitos faktūros** > **Laukiančios tiekėjų sąskaitos faktūros**). Norėdami registruoti su projektu susijusią laukiančią tiekėjo sąskaitą faktūrą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mokėtinos sumos** > **Sąskaitos faktūros** ir pasirinkite **Nauja**. 
1. Lauke **Sąskaitos faktūros klientas** pasirinkite tiekėją, tada lauke **Numeris** įveskite tiekėjo sąskaitos faktūros identifikavimo duomenis.
1. Į tiekėjo sąskaitą faktūrą įtraukite eilutę, tada lauke **Prekės numeris** pasirinkite iš tiekėjo įsigytą atsargose nelaikomą prekę. Arba lauke **Įsigijimo kategorija** pasirinkite iš tiekėjo įsigytą įsigijimo kategoriją.   
1. Įtraukite įsigytą kiekį. Sistema automatiškai įveda vieneto kainą pagal ne atsargose laikomos prekės kainos konfigūraciją. 
1. Patikrinkite bendrąją sumą ir kitą reikiamą informaciją eilutėje.
1. Eilutės išsamios informacijos srities skirtuke **Projektas** pasirinkite projekto, į kurį bus įrašoma ši prekė, ID.
1. Pasirinktinai: pasirinkite veiklos numerį ir atnaujinkite projekto kategoriją bei eilutės ypatybę.
1. Užregistruokite laukiančią tiekėjo sąskaitą faktūrą. Kai sąskaita faktūra užregistruojama, sistema įrašo šią informaciją:
    
    - Tiekėjo balanso suma.
    - PVM suma.
    - Projekto kaštai įrašomi į viešųjų pirkimų integravimo sąskaitą.
    - Projekto faktinės savikainos operacija, pateikta „Dataverse“.  Ši operacija toliau apdorojama naudojant [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md). Užregistravus šį žurnalą, suma iš viešųjų pirkimų integravimo sąskaitos perkeliama į projekto kaštų sąskaitą. 
    - Pirkiniai, už kuriuos projekto klientui išrašomos sąskaitos naudojant sąskaitų išrašymo pagal laiką ir medžiagas būdą. Be to, pirkiniams „Dataverse“ sukuriamos pardavimo operacijos, kurioms neišrašyta sąskaita. Pardavimo kainoms ir pardavimo operacijoms, kurioms neišrašytos sąskaitos, naudojamas „Dataverse“ produktų kainoraštis.
