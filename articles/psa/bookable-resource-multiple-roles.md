---
title: Įvertinti projekto pardavimus ir kaštus, kai rezervuojamas išteklius užpildo kelis projekto vaidmenis
description: Šioje temoje pateikta informacija apie tai, kaip kainų dimensijas galima naudoti išteklių kainodarai, kuri užpildo kelis projekto vaidmenis, palaikyti.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080888"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Įvertinti projekto pardavimus ir kaštus, kai rezervuojamas išteklius užpildo kelis projekto vaidmenis 

Projektų įmonėms dažnai reikia vieno ištekliaus keliems projekto vaidmenims. Kiekvienas iš šių vaidmenų gali būti įkainotas skirtingai, o tai reiškia, kad tas pats ištekliaus laikas projekto metu, priklausomai nuo sąskaitos ir kainų tarifų kiekvienam vaidmeniui, gali būti skirtingai finansiškai įvertintas. „Project Service Automation“ leidžia nustatyti nurodyto ištekliaus komandos nario įrašo reikšmes ir atlikti įvairius, kiekvienos, komandos nariui priskirtos užduoties perrašymus.

Toliau pateiktame pavyzdyje aiškinama, kaip paprastas šios reikšmės perrašymas leidžia ištekliui turėti kelis vaidmenis projekte su skirtingais išlaidų ir sąskaitų tarifais.

## <a name="create-tasks"></a>Kurti užduotis
Sukurkite dvi, 40 valandų trukmės A ir B projekto užduotis. Pasirinkite A užduotį kaip pirmtaką B užduočiai vykdyti.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Priskirkite vaidmenį ir organizacijos vienetą bendrajam projekto komandos nariui

1. **Grafiko** puslapyje, pasirinkite **užduoties** A eilutę. 
2. **Išteklių** lauke, išskleidžiamame sąraše pasirinkite **sukurti**.
3. **Komandos nario sparčiojo kūrimo** puslapyje nurodykite bendrojo komandos nario, kuris gali atlikti šią užduotį, atributus.
4. Pasirinkite atitinkamą vaidmenį ir organizacijos vienetą, tada spauskite **Įrašyti ir uždaryti**. Bendrinis komandos narys sukurtas ir priskirtas šiai užduočiai. 

Pakartokite šiuos veiksmus su užduotimi B ir įsitikinkite, kad bendrojo komandos nario vaidmuo ir organizacijos vienetas, sukurtas B užduočiai, skiriasi nuo A užduoties. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Priskirkite vaidmenį ir organizacijos vienetą projekto užduočiai

1. Kai sukuriate A užduotį, ją pažymėkite ir pasirinkite **Redaguoti užduotį**.
2. **Užduoties išsami informacija** puslapyje raskite **vaidmens** ir **organizacijos vieneto** laukus, pridėkite reikšmes, būtinas ištekliui, atliekančiam šią užduotį. 

  > [!NOTE]
  > Jei šiuos scenarijus užbaigiate naudodami „Project Service Automation“ demonstracinės versijos duomenis, pasirinkite **Konsultavimo vadovą** ir **„Fabrikam“ JAV** kaip organizacijos vienetą.

3. Pasirinkite B užduotį ir tada spauskite **Redaguoti užduotį**.
4. **Užduoties išsami informacija** puslapyje raskite **vaidmens** ir **organizacijos vieneto** laukus, pridėkite reikšmes, būtinas ištekliui, atliekančiam šią užduotį. Įsitikinkite, kad B užduoties reikšmės **vaidmens** ir **organizacijos vieneto** laukuose yra skirtingos nuo A užduoties. 

  > [!NOTE]
  > Jei šiuos scenarijus užbaigiate naudodami „Project Service Automation“ demonstracinės versijos duomenis, pasirinkite **Tinklo techniką** vaidmeniui ir **„Fabrikam“ JAV** kaip organizacijos vienetą.

5. Išsaugokite ir uždarykite **išsamios užduoties informacijos** puslapį. 

## <a name="team-member-and-estimates-behaviour"></a>Komandos narys ir sąmatos elgsena 

1. **Užduoties išsami informacija** puslapyje, **komandos nario** sekcijoje pažymėkite du bendruosius komandos narius ir pažymėkite **Generuoti reikalavimus**. Tai sukurs reikalavimus ištekliui. 
2. Pasirinkite komandos nario eilutę **konsultacijų vadovui** ir spauskite **rezervuoti**. Atsidaro tvarkaraščio lenta ir rezervuojamas išteklius pagal reikalavimą.
3. Pasirinkite komandos nario eilutę **tinklo technikui** ir spauskite **rezervuoti**. Atsidaro tvarkaraščio lenta ir rezervuojamas tas pats išteklius pagal reikalavimą.

### <a name="team-member-grid"></a>Komandos nario tinklelis 
**Komandos nario** tinklelyje atkreipkite dėmesį, kad du bendrojo komandos nario įrašai yra ištrinti, o juos pakeitė vienas išteklius. Yra vienas to ištekliaus reikšmių rinkinys, kuris rodo numatytąjį **vaidmens** ir **organizacijos vieneto** reikšmių rinkinį.
Išplėtus tos komandos nario įrašo eilutę, galite matyti atskiras paskirtas užduotis abiems užduotims. Kiekviena paskyrimo eilutė turi tam tikras **vaidmens** ir **organizacijos vieneto** reikšmes. 

### <a name="estimates-grid"></a>Įvertinimo tinklelis 
Kai pereisite į **sąmatų** tinklelį, pastebėsite, kad abi to paties ištekliaus užduotys įkainojamos skirtingai.
A užduoties priskyrimas ištekliui yra įkainotas naudojant **Vaidmens** **Konsultavimo vadovo** atributo reikšmę. B užduoties priskyrimas tam pačiam ištekliui yra įkainotas naudojant **Vaidmens** **Tinklo techniko** atributo reikšmę.





