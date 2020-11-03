---
title: Būtinų pasirinktinių laukų įtraukimas į kainų sąranką ir operacijų objektus
description: Šioje temoje pateikta informacija apie tai, kaip įtraukti būtinas pasirinktinių lauko nuorodų į objektus ir formas bei rodinius.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e589465eb98723b3b49c5d96e263eb3abf15eb2c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080876"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Būtinų pasirinktinių laukų įtraukimas į kainų sąranką ir operacijų objektus

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Šioje temoje informacija pateikiama manant, kad baigėte temos [Pasirinktinių laukų ir objektų kūrimas ir objektai, naudojami kaip kainodaros dimensijos](create-custom-fields-entities-pricing-dimensions.md) procedūras. Jei neatlikote šių procedūrų, grįžkite ir jas atlikite, o tada grįžkite į šią temą. 

Šioje temoje procedūromis parodoma, kaip įtraukti reikiamas pasirinktinio lauko nuorodas į objektus ir į vartotojo sąsajos (UI) elementus, pvz., formas ir rodinius.

## <a name="add-custom-pricing-dimension-fields"></a>Pasirinktinių kainos dimensijų laukų įtraukimas 
Sukūrus pasirinktinius laukus ir objektus, kitas žingsnis – kainų sąrankos ir operacinių objektų supažindinimas su bet kokiais pasirinktiniais objektais ar parinkčių rinkiniais, kuriant nuorodos laukus. Atsižvelgiant į tai, ar jūsų kainos dimensijų sąraše yra parinkčių rinkinio dimensijos, objekto dimensijos, ar abi, atlikite tik **„Parinkčių rinkinio pasirinktinių kainų dimensijos“** arba **„Objekto pasirinktinių kainų dimensijos“** , arba abiejuose skyriuose nurodytus žingsnius.

### <a name="option-set-based-custom-pricing-dimensions"></a>Parinkčių rinkinio pasirinktinių kainų dimensijos
Kai pasirinktinė kainodaros dimensija yra sukurta pagal parinkčių rinkinį, įtraukite ją kaip lauką į pagrindinius objektus. Toliau nurodytoje procedūroje **„Išteklių darbo vieta“** ir **„Išteklių darbo valandos“** naudojamos kaip parinkčių rinkinio pasirinktinių kainų dimensijos. Pirmiausia šias dimensijas reikia įtraukti kaip laukus į kainų objektus **„Vaidmenų kaina“** ir **„Vaidmenų kainos antkainis“**.

1. Projektų operacijose pasirinkite **Parametrai** > **Sprendimai** ir dukart spustelėkite **\<your organization name> kainodaros dimensijas**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Vaidmenų kaina“**.
3. Išplėskite objektą **„Vaidmenų kaina“** ir pasirinkite **„Laukai“**.
4. Pasirinkite **Naujas** ir sukurkite naują lauką pavadinimu **Išteklių darbo vieta** , tada pasirinkite **Parinkčių rinkinys** kaip lauko tipą. 
5. Pasirinkite **„Naudoti esamą parinkčių rinkinį“** , pasirinkite parinkčių rinkinį **„Išteklių darbo vieta“** , tada pasirinkite **„Įrašyti“**.
6. Pakartokite 1–5 žingsnius, kad įtrauktumėte šį lauką į objektą **„Vaidmenų kainos antkainis“**. 
7. Pakartokite 1–5 žingsnius parinkčių rinkiniui **„Išteklių darbo valandos“**.

> [!IMPORTANT]
> Kai įtraukiate lauką į daugiau nei vieną objektą, visiems objektams naudokite tą patį lauko pavadinimą. 

Projekto pardavimo ir įvertinimo etapuose darbo bandymų, kuriuos reikia atlikti **„Vietoje“** ir **„Darbo vietoje“** darbui, **„Įprastu laiku“** ir **„Viršvalandžiais“** , apskaičiavimas naudojamas įvertinti pasiūlymo / projekto vertę. Laukai **Išteklių darbo vieta“** ir **„Išteklių darbo valandos“** bus įtraukti į įvertinimo objektus: **„Pasiūlymo eilutės informacija“** , **„Sutarties eilutės informacija“** , **„Projekto komandos narys“** ir **„Įvertinimo eilutė“**.

1. Projektų operacijose pasirinkite **Parametrai** > **Sprendimai** , o tada dukart spustelėkite **\<your organization name> kainodaros dimensijas**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Pasiūlymo eilutės informacija“**.
3. Išplėskite objektą **„Pasiūlymo eilutės informacija“** ir pasirinkite **„Laukai“**.
4. Pasirinkite **Naujas** ir sukurkite naują lauką pavadinimu **Išteklių darbo vieta** , tada pasirinkite lauko tipą **Parinkčių rinkinys**. 
5. Pasirinkite **„Naudoti esamą parinkčių rinkinį“** ir **„Išteklių darbo vieta“** , tada spustelėkite **„Įrašyti“**.
6. Pakartokite 1–5 žingsnius, kad įtrauktumėte šį lauką į objektus **„Projekto sutarties eilutės informacija“** , **„Projekto komandos narys“** ir **„Įvertinimo eilutė“**.
7. Pakartokite 1–6 žingsnius parinkčių rinkiniui **„Išteklių darbo valandos“**. 

Užsakymo pristatymo ir SF išrašymui baigtas darbas turi būti tiksliai įkainotas, kad būtų galima pažymėti, ar jis projekto faktiniais duomenimis buvo atliktas **„Vietoje“** arba **„Darbo vietoje“** , taip pat ar jis buvo užbaigtas **„Įprastu laiku“** ar **„Viršvalandžiais“**. Laukai **„Išteklių darbo vieta“** ir **„Išteklių darbo valandos“** turi būti įtraukti į objektus **„Laiko įrašas“** , **„Faktinis“** , **„Sąskaitos faktūros eilutės informacija“** ir **„Žurnalo eilutė“**.

1. Pasirinkite **Parametrai** > **Sprendimai** , o tada dukart spustelėkite **\<your organization name> kainodaros dimensijas**.
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Laiko įrašas“**.
3. Išplėskite objektą **„Pasiūlymo eilutės informacija“** , o tada pasirinkite **„Laukai“**.
4. Pasirinkite **Naujas** ir sukurkite naują lauką pavadinimu **Išteklių darbo vieta** , tada pasirinkite **Parinkčių rinkinys** kaip lauko tipą. 
5. Pasirinkite **„Naudoti esamą parinkčių rinkinį“** , pasirinkite parinkčių rinkinį **„Išteklių darbo vieta“** , tada pasirinkite **„Įrašyti“**.
6. Pakartokite 1–5 žingsnius, kad įtrauktumėte šį lauką į objektus **„Faktinis“** , **„Sąskaitos faktūros eilutės informacija“** ir **„Žurnalo eilutė“**.
7. Pakartokite 1–6 žingsnius parinkčių rinkiniui **„Išteklių darbo valandos“**. 

Taip užbaigiami schemos pakeitimai, reikalingi parinkčių rinkinio pasirinktinėms dimensijoms.

## <a name="entity-based-custom-pricing-dimensions"></a>Objekto pasirinktinių kainų dimensijos

Kai pasirinktinių kainų dimensijos yra objektas, reikia įtraukti 1:N ryšį tarp dimensijos objekto ir pagrindinių objektų. Naudojant aukščiau minėtą standartinį pavadinimo pavyzdį logiška, kad kiekvienam darbuotojui priskiriamas standartinis pavadinimas. SA gaunamas rezultatas, jums reikės 1:N ryšio iš „Standartinio pavadinimo“ į „Rezervuojamus išteklius“ arba N:1 ryšio, jei jis buvo sukurtas iš „Rezervuojamų išteklių“ į „Standartinį pavadinimą“.

1. Projektų operacijose pasirinkite **Parametrai** > **Sprendimai** , o tada dukart spustelėkite **\<your organization name> kainodaros dimensijas**. 
2. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Standartinis pavadinimas“**.
3. Išplėskite objektą **„Standartinis pavadinimas“** ir pasirinkite **„1:N ryšiai“**.
4. Pasirinkite **„Naujas“** , kad sukurtumėte naują 1:N ryšį pavadinimu **„Standartinis rezervuojamų išteklių pavadinimas“**. Įveskite reikiamą informaciją ir pasirinkite **„Įrašyti“**.

Standartinį pavadinimą taip pat reikės įtraukti į kainų objektus, **„Vaidmenų kaina“** ir **„Vaidmenų kainos antkainis“**. Tai taip pat atliekama naudojant 1:N ryšius tarp objektų **„Standartinis pavadinimas“** ir **„Vaidmenų kaina“** bei tarp objektų **„Standartinis pavadinimas“** ir **„Vaidmenų kainos antkainis“**.

1. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Standartinis pavadinimas“**.
2. Išplėskite objektą **„Standartinis pavadinimas“** ir pasirinkite **„1:N ryšiai“**.
3. Pasirinkite **„Naujas“** , kad sukurtumėte naują 1:N ryšį pavadinimu **„Standartinis vaidmenų kainos pavadinimas“**. Įveskite reikiamą informaciją ir pasirinkite **„Įrašyti“**.
4. Pakartokite 1–4 žingsnius ir sukurkite 1:N ryšius tarp objektų **„Standartinis pavadinimas“** ir **v„Vaidmenų kainos antkainis“**.

Projekto pardavimo ir įvertinimo etapuose pasiūlymo / projekto įkainojimui reikia apskaičiuoti, kiek darbo bandymų reikia atlikti kiekvienam standartiniam pavadinimui. Tai reiškia, kad 1:N ryšiams iš „Standartinis pavadinimas“ į kiekvieną iš šių įvertinimo objektų reikia: 

- **Pasiūlymo eilutės informacija**
- **Projekto sutarties eilutės informacija**
- **Projekto komandos narys**
- **Įvertinimo eilutė**

5. Pakartokite 1–5 žingsnius, kad sukurtumėte 1:N ryšius iš **„Standartinis pavadinimas“** į **„Pasiūlymo eilutės informacija“** , **„Projekto sutarties eilutės informacija“** , **„Projekto komandos narys“** ir **„Įvertinimo eilutė“**.

  Užsakymo pristatymo ir SF išrašymo etapuose kiekvieno standartinio pavadinimo užbaigtas darbas turi būti tiksliai įkainotas pagal projekto faktinius duomenis. Tai reiškia, kad reikia 1:N ryšių iš **„Standartinis pavadinimas“** į objektus **„Laiko įrašas“** , **„Faktinis“** , **Sąskaitos faktūros eilutės informacija“** ir **Žurnalo eilutė“**.

6. Pakartokite 1–6 žingsnius, kad sukurtumėte 1:N ryšius iš **„Standartinis pavadinimas“** į objektus **„Laiko įrašas“** , **„Faktinis“** , **Sąskaitos faktūros eilutės informacija“** ir **Žurnalo eilutė“**.

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Nustatykite Dimensijos reikšmę pagal platformos susiejimų funkcijas.
„Laiko įrašui“ būtų naudinga turėti sistemos numatytąją reikšmę „Laiko įraše“ esančiam „Standartiniam pavadinimui“ iš „Rezervuojamų išteklių“, įrašinėjančių laiko įrašą. Atlikite šiuos veiksmus, jei norite įtraukti laukų susiejimus į 1:N ryšiams iš **„Rezervuojami ištekliai“** į **„Laiko įrašas“**.

1. Sprendimų naršyklėje, kairiojoje naršymo srities pusėje pasirinkite **„Objektai“ > „Standartinis pavadinimas“**.
2. Išplėskite objektą **„Standartinis pavadinimas“** ir pasirinkite **„1:N ryšiai“**.
3. Du kartus spustelėkite **„Rezervuojami ištekliai laiko įrašui“**. Puslapyje **„Ryšis“** pasirinkite **„Naudoti laukų susiejimus“**. 
4. Pasirinkite **„Naujas“** , jei norite sukurti naują laukų susiejimą nuo lauko **„Standartinis pavadinimas“** , esančio objekte **„Rezervuojami ištekliai“** , iki nuorodos lauko **„Standartinis pavadinimas“** , esančio objekte **„Laiko įrašas“**. 

Taip užbaigiami schemos pakeitimai, reikalingi objekto pasirinktinėms dimensijoms.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Pasirinktinių laukų įtraukimas į formas, rodinius ir veiklos taisykles

Atlikus visus reikiamus schemos pakeitimus, reikia padaryti laukus matomus vartotojo sąsajoje, įtraukiant juos į formas ir rodinius.

1. Atidarykite formą arba rodinį. Dešinėje naršymo srityje pasirinkite lauką ir nuvilkite jį ant formų laukų. 
2. Jei redaguojate rodinį, naudokite tinkamą naršymo sritį, spustelėkite **„Įtraukti laukus“** , o dialogo lange **„Laukų sąrašas“** pasirinkite reikiamus laukus ir spustelėkite **„Gerai“**.

Toliau esančioje lentelėje pateikiamas išsamus paruoštų formų ir rodinių sąrašas pagal objektą, kuriuos reikės atnaujinti naujuose laukuose. Jei šiuose objektų tinkinimuose yra papildomų rodinių arba formų, į juos taip pat įtraukite naujų laukų.

| Entity        | Formos, kurioms reikia naujo lauko   |Rodiniai, kuriems reikia naujo lauko      |
| ------------------------------|---------------------------------|----------------------------------|
|  Vaidmens kaina|• Informacija |• Aktyviųjų išteklių kategorijų kainos<br> • Išteklių kategorijos kainos susietasis rodinys|
|  Vaidmens kainos antkainis|• Informacija|• Aktyviojo vaidmens kainos antkainis<br>• Vaidmens kainos antkainio susietasis rodinys|
|  Pasiūlymo eilutės informacija|• Projekto informacija<br>• Spartusis projekto kūrimas|• Aktyviojo pasiūlymo eilutės informacija<br>• Jungtinių pasiūlymo eilučių informacija<br>• Pasiūlymo eilutės informacijos susietasis rodinys|
|  • Projekto sutarties eilutės informacija|• Projekto informacija<br>• Spartusis projekto kūrimas|• Bendra sutarties eilučių informacija<br>• Aktyvios sutarties eilutės informacija<br>• Sutarties eilučių informacijos susietasis rodinys|
|  Projekto komandos narys|• Informacija<br>• Nauja forma|• Aktyvieji projekto komandos nariai<br>• Projekto komandos nariai<br>• Projekto komandos narių susietasis rodinys|
|  Laiko įrašas|• Informacija<br>• Laiko įrašo kūrimas|• Mano laiko įrašai pagal datą<br>• Mano laiko įrašai šią savaitę<br>• Laiko įrašai, skirti patvirtinti|
|  Žurnalo eilutė|• Informacija<br>• Spartusis kūrimas|• Aktyviojo žurnalo eilutės<br>• Žurnalo eilučių susietasis rodinys|
|  Sąskaitos faktūros eilutės informacija|• Informacija<br>• Spartusis kūrimas|• Aktyvioji sąskaitos faktūros eilutės išsami informacija<br>• Apmokestinamos sąskaitų faktūrų operacijos<br>• Nemokamos sąskaitos faktūros operacijos<br>• Sąskaitos faktūros eilutės informacijos susietasis rodinys<br>• Neapmokestinamos sąskaitos faktūros operacijos|
|  Faktinis|• Informacija<br>• Aktyvieji faktiniai duomenys|• Faktinis susietasis rodinys|

Pasirinktinius laukus taip pat gali reikėti įtraukti į veiklos taisykles atsižvelgiant į tai, ką nustatėte. Vienas iš paruoštų pavyzdžių yra skirtas veiklos taisyklei **„Laiko įrašo redagavimas atsižvelgiant į būseną“**. Ši taisyklė apibrėžia, kuriuos laukus reikia užrakinti, kai „Laiko įrašas“ yra neredaguojamoje būsenoje, tokioje kaip **„Patvirtinta“**. Įtraukite laukus į šią veiklos taisyklę, kad nebūtų galima laukų redaguoti, kai „Laiko įrašas“ yra bet kokioje būsenoje, išskyrus **„Juodraštis“** arba **„Grąžinta“**.
