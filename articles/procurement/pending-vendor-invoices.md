---
title: Nelaikomų medžiagų arba įsigijimo kategorijų pirkimas naudojant laukiančią tiekėjo SF
description: Šiame straipsnyje paaiškinama, kaip įrašyti laukiančias tiekėjo SF.
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
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Nelaikomų medžiagų arba įsigijimo kategorijų pirkimas naudojant laukiančią tiekėjo SF

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Kadangi įmonė įsigyja projekto nelaikomas medžiagas ar pirkimo kategorijas, išlaidos gali būti nedelsiant užregistruotos pagal projektą. 

Pvz., „Contoso Robotics US“ vykdo įrangos atnaujinimo projektą ir nori programinės įrangos licencijų. Šios licencijos įsigyjamos iš trečiosios šalies tiekėjo.  Naudodamasis Dynamics 365 Finance, mokėtinų sumų tarnautojas įrašo laukiantį tiekėjo SF dokumentą ir priskiria licencijos išlaidas tiesiogiai įrangos atnaujinimo projektui. 

> [!IMPORTANT]
> Prieš naudodami šiame straipsnyje aprašytas funkcijas, peržiūrėkite ir taikykite reikiamas konfigūracijas. Daugiau informacijos ieškokite [Enable non-stocked materials and waiting waiting vendor SF](configure-materials-nonstocked.md) ir [Use procurement categories with project purchase orders and waiting vendor SF](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Su projektu susijusios laukiančios tiekėjo sąskaitos faktūros registravimas 

Laukiančias tiekėjų sąskaitas faktūras galima įrašyti puslapyje **Laukiančios tiekėjų sąskaitos faktūros** (**Mokėtinos sumos** > **Sąskaitos faktūros** > **Laukiančios tiekėjų sąskaitos faktūros**). Norėdami registruoti su projektu susijusią laukiančią tiekėjo sąskaitą faktūrą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Mokėtinų sumų** > **SF** ir pasirinkite **Naujas**. 
1. Lauke **SF sąskaita** pasirinkite tiekėją, tada lauke Numeris **įveskite** tiekėjo SF identifikavimo duomenis.
1. Įtraukite eilutę į tiekėjo SF, tada lauke Prekės numeris **pasirinkite** nelaikomą prekę, įsigytą iš tiekėjo. Arba lauke Įsigijimo kategorija **pasirinkite** įsigijimo kategoriją, įsigytą iš tiekėjo.   
1. Įtraukite įsigytą kiekį. Sistema užpildo vieneto kainą, pagrįstą nelaikomos prekės kainos konfigūracija. 
1. Patikrinkite bendrąją sumą ir kitą reikiamą informaciją eilutėje.
1. Eilutės išsamios informacijos **skirtuke Projektas** pasirinkite projekto, į kurį bus įrašytas šis elementas, ID.
1. Pasirinktinai: pasirinkite veiklos numerį ir atnaujinkite projekto kategoriją bei eilutės ypatybę.
1. Registruoti laukiančią tiekėjo SF. Užregistravus SF, sistema įrašo šią informaciją:
    
    - Tiekėjo balanso suma.
    - PVM suma.
    - Projekto kaštai įrašomi į viešųjų pirkimų integravimo sąskaitą.
    - Projekto faktinės savikainos operacija, pateikta „Dataverse“.  Ši operacija toliau apdorojama naudojant [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md). Užregistravus šį žurnalą, suma iš viešųjų pirkimų integravimo sąskaitos perkeliama į projekto kaštų sąskaitą. 
    - Pirkiniai, už kuriuos projekto klientui išrašomos sąskaitos naudojant sąskaitų išrašymo pagal laiką ir medžiagas būdą. Be to, pirkiniams „Dataverse“ sukuriamos pardavimo operacijos, kurioms neišrašyta sąskaita. Pardavimo kainoms ir pardavimo operacijoms, kurioms neišrašytos sąskaitos, naudojamas „Dataverse“ produktų kainoraštis.
