---
title: Pasirinktinių laukų įtraukimas į kainų sąranką ir operacinius objektus
description: Šiame straipsnyje pateikiama informacija apie tai, kaip įtraukti pasirinktinius laukus į kainų sąranką ir operacinius objektus.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: b666d1767306b9833fba36c6ed2c59a633c5fdf0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920484"
---
# <a name="add-custom-fields-to-price-setup-and-transactional-entities"></a>Pasirinktinių laukų įtraukimas į kainų sąranką ir operacinius objektus 

[!include [banner](../includes/psa-now-project-operations.md)]

Šiame straipsnyje informacija pateikiama manant, kad baigėte straipsnio [„Pasirinktinių laukų ir objektų kūrimas“](create-custom-fields-entities.md) procedūras. Jei neatlikote šių procedūrų, grįžkite ir jas atlikite, o tada grįžkite į šią straipsnį. 

Šiame straipsnyje procedūromis parodoma, kaip įtraukti reikiamas pasirinktinio lauko nuorodas į objektus ir į vartotojo sąsajos (UI) elementus, pvz., formas ir rodinius.

## <a name="add-custom-pricing-dimension-fields"></a>Pasirinktinių kainos dimensijų laukų įtraukimas 
Sukūrus pasirinktinius laukus ir objektus, kitas žingsnis – kainų sąrankos ir operacinių objektų supažindinimas su bet kokiais pasirinktiniais objektais ar parinkčių rinkiniais, kuriant nuorodos laukus. Atsižvelgiant į tai, ar jūsų kainos dimensijų sąraše yra parinkčių rinkinio dimensijos, objekto dimensijos, ar abi, atlikite tik **„Parinkčių rinkinio pasirinktinių kainų dimensijos“** arba **„Objekto pasirinktinių kainų dimensijos“**, arba abiejuose skyriuose nurodytus žingsnius.

### <a name="option-set-based-custom-pricing-dimensions"></a>Parinkčių rinkinio pasirinktinių kainų dimensijos
Kai pasirinktinių kainų dimensija yra sukurta pagal parinkčių rinkinį, įtraukite ją kaip lauką į pagrindinius „Project Service“ objektus. Toliau nurodytoje procedūroje **„Išteklių darbo vieta“** ir **„Išteklių darbo valandos“** naudojamos kaip parinkčių rinkinio pasirinktinių kainų dimensijos. Pirmiausia šias dimensijas reikia įtraukti kaip laukus į kainų objektus **„Vaidmenų kaina“** ir **„Vaidmenų kainos antkainis“**.

1. „Project Service Automation“ (PSA) spustelėkite **Nustatymai** > **Sprendimai**, tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Vaidmenų kaina“**.
3. Išplėskite objektą **„Vaidmenų kaina“** ir pasirinkite **„Laukai“**.
4. Spustelėkite **„Naujas“** ir sukurkite naują lauką pavadinimu **„Išteklių darbo vieta“**, tada pasirinkite **„Parinkčių rinkinys“** kaip lauko tipą. 
5. Pasirinkite **„Naudoti esamą parinkčių rinkinį“**, pasirinkite parinkčių rinkinį **„Išteklių darbo vieta“**, tada spustelėkite **„Įrašyti“**.
6. Pakartokite 1–5 žingsnius, kad įtrauktumėte šį lauką į objektą **„Vaidmenų kainos antkainis“**. 
7. Pakartokite 1–5 žingsnius parinkčių rinkiniui **„Išteklių darbo valandos“**.

> [!IMPORTANT]
> Kai įtraukiate lauką į daugiau nei vieną objektą, visiems objektams naudokite tą patį lauko pavadinimą. 

> ![Išteklių darbo vietos įtraukimas į vaidmenų kainą.](media/RWL-Field.png)

Projekto pardavimo ir įvertinimo etapuose darbo bandymų, kuriuos reikia atlikti **„Vietoje“** ir **„Darbo vietoje“** darbui, **„Įprastu laiku“** ir **„Viršvalandžiais“**, apskaičiavimas naudojamas įvertinti pasiūlymo / projekto vertę. **Ištekliaus darbo vietos** ir **ištekliaus darbo valandų** laukai bus įtraukti į įvertinimo objektus: **Pasiūlymo eilutės informaciją**, **Sutarties eilutės informaciją**, **Projekto užduotį**, **Projekto komandos narį** ir **Įvertinimo eilutę**.

1. PSA pasirinkite **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Pasiūlymo eilutės informacija“**.
3. Išplėskite objektą **„Pasiūlymo eilutės informacija“** ir pasirinkite **„Laukai“**.
4. Spustelėkite **„Naujas“** ir sukurkite naują lauką pavadinimu **„Išteklių darbo vieta“**, tada pasirinkite lauko tipą **„Parinkčių rinkinys“**. 
5. Pasirinkite **„Naudoti esamą parinkčių rinkinį“** ir **„Išteklių darbo vieta“**, tada spustelėkite **„Įrašyti“**.
6. Pakartokite 1–5 žingsnius, kad įtrauktumėte šį lauką į **Projekto sutarties eilutės informaciją**, **Projekto užduotį**, **Projekto komandos nario** ir **Įvertinimo eilutės** objektus.
7. Pakartokite 1–6 žingsnius parinkčių rinkiniui **„Išteklių darbo valandos“**. 

> ![Išteklių darbo vietos įtraukimas į įvertinimo eilutę.](media/RWL-Default-Value.png)


Užsakymo pristatymo ir SF išrašymui baigtas darbas turi būti tiksliai įkainotas, kad būtų galima pažymėti, ar jis projekto faktiniais duomenimis buvo atliktas **„Vietoje“** arba **„Darbo vietoje“**, taip pat ar jis buvo užbaigtas **„Įprastu laiku“** ar **„Viršvalandžiais“**. Laukai **„Išteklių darbo vieta“** ir **„Išteklių darbo valandos“** turi būti įtraukti į objektus **„Laiko įrašas“**, **„Faktinis“**, **„Sąskaitos faktūros eilutės informacija“** ir **„Žurnalo eilutė“**.

1. PSA pasirinkite **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Laiko įrašas“**.
3. Išplėskite objektą **„Pasiūlymo eilutės informacija“**, o tada pasirinkite **„Laukai“**.
4. Spustelėkite **„Naujas“** ir sukurkite naują lauką pavadinimu **„Išteklių darbo vieta“**, tada pasirinkite **„Parinkčių rinkinys“** kaip lauko tipą. 
5. Pasirinkite **„Naudoti esamą parinkčių rinkinį“**, pasirinkite parinkčių rinkinį **„Išteklių darbo vieta“**, tada spustelėkite **„Įrašyti“**.
6. Pakartokite 1–5 žingsnius, kad įtrauktumėte šį lauką į objektus **„Faktinis“**, **„Sąskaitos faktūros eilutės informacija“** ir **„Žurnalo eilutė“**.
7. Pakartokite 1–6 žingsnius parinkčių rinkiniui **„Išteklių darbo valandos“**. 

> ![Išteklių darbo vietos įtraukimas į laiko įrašą.](media/RWL-time-entry.png)

Taip užbaigiami schemos pakeitimai, reikalingi parinkčių rinkinio pasirinktinėms dimensijoms.

## <a name="entity-based-custom-pricing-dimensions"></a>Objekto pasirinktinių kainų dimensijos

Kai pasirinktinių kainų dimensijos yra objektas, reikia įtraukti 1:N ryšį tarp dimensijos objekto ir pagrindinių „Project Service“ objektų. Naudojant aukščiau minėtą standartinį pavadinimo pavyzdį logiška, kad kiekvienam darbuotojui priskiriamas standartinis pavadinimas. SA gaunamas rezultatas, jums reikės 1:N ryšio iš „Standartinio pavadinimo“ į „Rezervuojamus išteklius“ arba N:1 ryšio, jei jis buvo sukurtas iš „Rezervuojamų išteklių“ į „Standartinį pavadinimą“.

1. PSA pasirinkite **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Standartinis pavadinimas“**.
3. Išplėskite objektą **„Standartinis pavadinimas“** ir pasirinkite **„1:N ryšiai“**.
4. Spustelėkite **„Naujas“**, kad sukurtumėte naują 1:N ryšį pavadinimu **„Standartinis rezervuojamų išteklių pavadinimas“**. Įveskite reikiamą informaciją ir spustelėkite **„Įrašyti“**.

> ![Standartinio pavadinimo įtraukimas į rezervuojamus išteklius kaip nuorodos laukas.](media/ST-BR.png)

Standartinį pavadinimą taip pat reikės įtraukti į „Project Service“ kainų objektus, **„Vaidmenų kaina“** ir **„Vaidmenų kainos antkainis“**. Tai taip pat atliekama naudojant 1:N ryšius tarp objektų **„Standartinis pavadinimas“** ir **„Vaidmenų kaina“** bei tarp objektų **„Standartinis pavadinimas“** ir **„Vaidmenų kainos antkainis“**.

1. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Standartinis pavadinimas“**.
2. Išplėskite objektą **„Standartinis pavadinimas“** ir pasirinkite **„1:N ryšiai“**.
3. Spustelėkite **„Naujas“**, kad sukurtumėte naują 1:N ryšį pavadinimu **„Standartinis vaidmenų kainos pavadinimas“**. Įveskite reikiamą informaciją ir spustelėkite **„Įrašyti“**.
4. Pakartokite 1–4 žingsnius ir sukurkite 1:N ryšius tarp objektų **„Standartinis pavadinimas“** ir **v„Vaidmenų kainos antkainis“**.

Projekto pardavimo ir įvertinimo etapuose pasiūlymo / projekto įkainojimui reikia apskaičiuoti, kiek darbo bandymų reikia atlikti kiekvienam standartiniam pavadinimui. Tai reiškia, kad 1:N ryšiams iš „Standartinis pavadinimas“ į kiekvieną iš šių įvertinimo objektų naudojant „Project Service“ reikia: 

- **Pasiūlymo eilutės informacija**
- **Projekto sutarties eilutės informacija**
- **Projekto užduotis**
- **Projekto komandos narys**
- **Įvertinimo eilutė**

5. Pakartokite 1–5 žingsnius, kad sukurtumėte 1:N ryšius iš **Standartinio pavadinimo** į **Pasiūlymo eilutės informaciją**, **Projekto sutarties eilutės informaciją**, **Projekto užduotį**, **Projekto komandos narį** ir **Įvertinimo eilutę**.

> ![Standartinio pavadinimo įtraukimas į įvertinimo eilutę kaip nuorodos laukas.](media/ST-Estimate-Line.png)

Užsakymo pristatymo ir SF išrašymo etapuose kiekvieno standartinio pavadinimo užbaigtas darbas turi būti tiksliai įkainotas pagal projekto faktinius duomenis. Tai reiškia, kad reikia 1:N ryšių iš **„Standartinis pavadinimas“** į objektus **„Laiko įrašas“**, **„Faktinis“**, **Sąskaitos faktūros eilutės informacija“** ir **Žurnalo eilutė“**.

6. Pakartokite 1–6 žingsnius, kad sukurtumėte 1:N ryšius iš **„Standartinis pavadinimas“** į objektus **„Laiko įrašas“**, **„Faktinis“**, **Sąskaitos faktūros eilutės informacija“** ir **Žurnalo eilutė“**.

> ![Standartinio pavadinimo įtraukimas į laiko įrašą kaip nuorodos laukas.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Nustatykite Dimensijos reikšmę pagal platformos susiejimų funkcijas.
„Laiko įrašui“ būtų naudinga turėti sistemos numatytąją reikšmę „Laiko įraše“ esančiam „Standartiniam pavadinimui“ iš „Rezervuojamų išteklių“, įrašinėjančių laiko įrašą. Atlikite šiuos veiksmus, jei norite įtraukti laukų susiejimus į 1:N ryšiams iš **„Rezervuojami ištekliai“** į **„Laiko įrašas“**.

1. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Standartinis pavadinimas“**.
2. Išplėskite objektą **„Standartinis pavadinimas“** ir pasirinkite **„1:N ryšiai“**.
3. Du kartus spustelėkite **„Rezervuojami ištekliai laiko įrašui“**. Puslapyje **„Ryšis“** spustelėkite **„Naudoti laukų susiejimus“**. 
4. Spustelėkite **„Naujas“**, jei norite sukurti naują laukų susiejimą nuo lauko **„Standartinis pavadinimas“**, esančio objekte **„Rezervuojami ištekliai“**, iki nuorodos lauko **„Standartinis pavadinimas“**, esančio objekte **„Laiko įrašas“**. 

> ![Nustatykite laukų susiejimus, kad galėtumėte vykdyti numatytuosius „Standartinis pavadinimas“ nuo „Rezervuojami ištekliai“ iki „Laiko įrašas“.](media/ST-Mapping2.png)


Taip užbaigiami schemos pakeitimai, reikalingi objekto pasirinktinėms dimensijoms.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Pasirinktinių laukų įtraukimas į formas, rodinius ir veiklos taisykles

Atlikus visus reikiamus schemos pakeitimus, reikia padaryti laukus matomus vartotojo sąsajoje, įtraukiant juos į formas ir rodinius.

1. Atidarykite formą arba rodinį. Dešinėje naršymo srityje pasirinkite lauką ir nuvilkite jį ant formų laukų. 
2. Jei redaguojate rodinį, naudokite tinkamą naršymo sritį, spustelėkite **„Įtraukti laukus“**, o dialogo lange **„Laukų sąrašas“** pasirinkite reikiamus laukus ir spustelėkite **„Gerai“**.

Toliau esančioje lentelėje pateikiamas išsamus paruoštų formų ir rodinių sąrašas pagal objektą, kuriuos reikės atnaujinti naujuose laukuose. Jei šiuose objektų tinkinimuose yra papildomų rodinių arba formų, į juos taip pat įtraukite naujų laukų.

| „Project Service“ objektas        | Formos, kurioms reikia naujo lauko   |Rodiniai, kuriems reikia naujo lauko      |
| ------------------------------|---------------------------------|----------------------------------|
|  Vaidmens kaina|• Informacija |• Aktyviųjų išteklių kategorijų kainos<br> • Išteklių kategorijos kainos susietasis rodinys|
|  Vaidmens kainos antkainis|• Informacija|• Aktyviojo vaidmens kainos antkainis<br>• Vaidmens kainos antkainio susietasis rodinys|
|  Pasiūlymo eilutės informacija|• Projekto informacija<br>• Spartusis projekto kūrimas|• Aktyviojo pasiūlymo eilutės informacija<br>• Jungtinių pasiūlymo eilučių informacija<br>• Pasiūlymo eilutės informacijos susietasis rodinys|
|  • Projekto sutarties eilutės informacija|• Projekto informacija<br>• Spartusis projekto kūrimas|• Bendra sutarties eilučių informacija<br>• Aktyvios sutarties eilutės informacija<br>• Sutarties eilučių informacijos susietasis rodinys|
|  Projekto užduotis|• Informacija<br>• Nauja forma||
|  Projekto komandos narys|• Informacija<br>• Nauja forma|• Aktyvieji projekto komandos nariai<br>• Projekto komandos nariai<br>• Projekto komandos narių susietasis rodinys|
|  Laiko įrašas|• Informacija<br>• Laiko įrašo kūrimas|• Mano laiko įrašai pagal datą<br>• Mano laiko įrašai šią savaitę<br>• Laiko įrašai, skirti patvirtinti|
|  Žurnalo eilutė|• Informacija<br>• Spartusis kūrimas|• Aktyviojo žurnalo eilutės<br>• Žurnalo eilučių susietasis rodinys|
|  Sąskaitos faktūros eilutės informacija|• Informacija<br>• Spartusis kūrimas|• Aktyvioji sąskaitos faktūros eilutės išsami informacija<br>• Apmokestinamos sąskaitų faktūrų operacijos<br>• Nemokamos sąskaitos faktūros operacijos<br>• Sąskaitos faktūros eilutės informacijos susietasis rodinys<br>• Neapmokestinamos sąskaitos faktūros operacijos|
|  Faktinis|• Informacija<br>• Aktyvieji faktiniai duomenys|• Faktinis susietasis rodinys|

Pasirinktinius laukus taip pat gali reikėti įtraukti į veiklos taisykles atsižvelgiant į tai, ką nustatėte. Vienas iš paruoštų pavyzdžių yra skirtas veiklos taisyklei **„Laiko įrašo redagavimas atsižvelgiant į būseną“**. Ši taisyklė apibrėžia, kuriuos laukus reikia užrakinti, kai „Laiko įrašas“ yra neredaguojamoje būsenoje, tokioje kaip **„Patvirtinta“**. Įtraukite laukus į šią veiklos taisyklę, kad nebūtų galima laukų redaguoti, kai „Laiko įrašas“ yra bet kokioje būsenoje, išskyrus **„Juodraštis“** arba **„Grąžinta“**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
