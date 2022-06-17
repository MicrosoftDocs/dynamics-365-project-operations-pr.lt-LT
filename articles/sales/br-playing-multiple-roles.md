---
title: Projekto pardavimo ir išlaidų įvertinimas, kai rezervuojami ištekliai projekte atlieka kelis vaidmenis
description: Šiame straipsnyje paaiškinama, kaip naudoti kainodaros dimensijas, kad būtų galima palaikyti išteklių, kurie užpildo kelis projekto vaidmenis, kainodaros ir įkainojimo įvertinimus.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9bb59537aaa75d9003925bec37642a2fa7c9ca22
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923474"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Projekto pardavimo ir išlaidų įvertinimas, kai rezervuojami ištekliai projekte atlieka kelis vaidmenis 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, „Lite” versijos visuotinis diegimas – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_ 

Projektu pagrįstoms įmonėms dažnai reikia vieno ištekliaus, kad projekte atliktų kelis vaidmenis. Kiekvienas vaidmuo gali būti įkainotas skirtingai. Tai reiškia, kad tokiam pačiam ištekliaus laikui projekte gali būti skirtas kitoks finansinis įvertinimas, atsižvelgiant į kiekvieno vaidmens apmokestinimo ir savikainos tarifus. Galite nustatyti įvardyto ištekliaus reikšmes komandos nario įraše, naudodami skirtingus perrašymus kiekvienai užduočiai, kuriai priskirtas komandos narys.

Toliau pateiktame pavyzdyje paaiškinama, kaip atliekant paprastą reikšmės perrašymą ištekliai gali turėti projekte kelis vaidmenis su skirtingais savikainos ir apmokestinimo tarifais.

## <a name="create-tasks"></a>Kurti užduotis
Norėdami kurti užduotis, turite įtraukti užduočių, taip pat suvestinių užduočių, po kurių turite priskirti užduotį prieš įtraukdami užduoties trukmę. 

### <a name="add-tasks-and-summary-tasks"></a>Užduočių ir suvestinių užduočių įtraukimas
Kad įtrauktumėte užduotį, atlikite toliau nurodytus veiksmus.

1. Eikite į **Projektai** ir atidarykite projektą, į kurį norite įtraukti užduočių.
2. Pasirinkite **Įtraukti naują užduotį**. Įveskite užduoties pavadinimą, tada paspauskite **Enter**.
3. Įveskite kitos užduoties pavadinimą ir paspauskite **Enter**. Šiuos veiksmus kartokite, kol turėsite visą užduočių sąrašą.
3. Norėdami užduotis perkelti į žemesnį lygį dalyje **Suvestinės** užduotys, pasirinkite tris vertikalius taškus greta užduoties pavadinimo ir tada pasirinkite **Atlikti antrinę užduotį**. 

  > [!TIP]
  > Norėdami pasirinkti daugiau nei vieną užduotį, pasirinkite užduotį, paspauskite ir laikykite **Ctrl**, o tada pasirinkite kitą užduotį.
  >
  > Taip pat galite pasirinkti **Perkelti antrinę užduotį į aukštesnį lygį**, kad perkeltumėte užduotis, esančias dalyje **Suvestinės** užduotys.

### <a name="assign-tasks"></a>Užduočių priskyrimas

Norėdami priskirti užduotis, atlikite toliau nurodytus veiksmus.

1. Užduoties stulpelyje  **Priskirta**  pasirinkite asmens piktogramą.
2. Pasirinkite komandos narį iš sąrašo arba įveskite tekstą ir ieškokite vardo ir pavardės.

### <a name="add-task-duration-and-columns"></a>Užduoties trukmės ir stulpelių įtraukimas

Dažnai lengviausia pradėti kurti projektą nurodant trukmę. Norėdami įtraukti užduoties trukmę, atlikite toliau nurodytus veiksmus.

1. Užduoties stulpelyje **Trukmė** įveskite dienų skaičių – numatomą laiką, kiek užtruks atlikti užduotį. Jei norite naudoti kitus laiko matavimo vienetus, įveskite skaičių su žodžiu **val.**, **sav.** arba **mėn.**
2. Jei norite, kad užduotis būtų rodoma rodinyje **Laiko planavimo juosta** kaip rombo formos etapas, stulpelyje **Trukmė** įveskite **0 d.**
3. Paspaudę **Enter** pereikite prie kitos užduoties lauko **Trukmė** ir tęskite trukmės įvedimą.

  > [!NOTE]
  > Negalima įvesti suvestinių užduočių trukmės.

Į savo projektą galite įtraukti stulpelių ir pateikti daugiau informacijos. Norėdami tai padaryti, pasirinkite **Įtraukti stulpelį**. 

Daugiau informacijos žr. [Projekto kūrimas](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Bendrojo projekto komandos nario vaidmens ir organizacijos vieneto nustatymas
Norėdami nustatyti bendrojo projekto komandos nario vaidmenį ir organizacijos vienetą, atlikite toliau nurodytus veiksmus.

1. Puslapyje **Užduotys** pasirinkite **A užduoties** eilutę **Užduotis**. 
2. Dalyje **Priskirti** pasirinkite **Bendrųjų išteklių įtraukimas**. Bus atidarytas puslapis **Spartusis komandos nario kūrimas**.
3. **Komandos nario sparčiojo kūrimo** puslapyje nurodykite bendrojo komandos nario, kuris gali atlikti šią užduotį, atributus.
4. Pasirinkite atitinkamą vaidmenį ir organizacijos vienetą, tada spauskite **Įrašyti ir uždaryti**. Bendrinis komandos narys sukurtas ir priskirtas šiai užduočiai. 
5. Pakartokite 1–4 veiksmus su **B užduotimi**. Tačiau **B užduotyje** bendrajam komandos nariui turi būti priskirtas kitas vaidmuo ir organizacijos vienetas nei **A užduotyje**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Projekto užduoties vaidmens ir organizacijos vieneto nustatymas
Norėdami nustatyti užduoties vaidmenį ir organizacijos vienetą, atlikite toliau nurodytus veiksmus.

1. Sukūrę **A užduotį**, ją pasirinkite ir tada pasirinkite **i** piktogramą, kad atidarytumėte sritį **Išsami užduoties informacija**. 
2. Srityje **Išsami užduoties informacija** slinkite į apačią ir pasirinkite **Peržiūrėti išsamią informaciją**, kad atidarytumėte puslapį **Išsami užduoties informacija**.
3. Puslapyje **Išsami užduoties informacija** į laukus **Vaidmuo** ir **Organizacijos vienetas** įtraukite reikšmes, kurios būtinos ištekliams norint atlikti šią užduotį. 

  > [!NOTE]
  > Jei šį scenarijų užbaigsite naudodamiesi „Project Operations“ demonstracinius duomenimis, kaip vaidmenį pasirinkite **Konsultacijų vadovas**, o kaip organizacijos vienetą – **Fabrikam US**.

4. Pasirinkite **B užduotis** ir tada pasirinkite užduotį.
5. Norėdami atidaryti sritį **Išsami užduoties informacija**, pasirinkite **i** piktogramą. 
6. Srityje **Išsami užduoties informacija** slinkite į apačią ir pasirinkite **Rodyti išsamią informaciją**, kad atidarytumėte puslapį **Išsami užduoties informacija**.
7. Puslapyje **Išsami užduoties informacija**, į laukus **Vaidmuo** ir **Organizacijos vienetas** įtraukite reikšmes, kurios būtinos ištekliams, kad atliktų šią užduotį. **B užduoties** laukų **vaidmens** ir **organizacijos vieneto** reikšmės turi būti kitokios nei **A užduoties**. 

  > [!NOTE]
  > Jei šį scenarijų užbaigsite naudodamiesi „Project Operations“ demonstracinius duomenimis, kaip vaidmenį pasirinkite **Tinklo technikas**, o kaip organizacijos vienetą – **Fabrikam US**.

8. Išsaugokite ir uždarykite **išsamios užduoties informacijos** puslapį. 

## <a name="team-member-and-estimates-behavior"></a>Komandos nario ir įvertinimų veikimo būdas 
Norėdami suprasti **komandos narių** tinklelio ir įvertinimų veikimo būdą, atlikite toliau nurodytus veiksmus.

1. **Komandos narių** tinklelyje pasirinkite du bendruosius komandos narius, tada pasirinkite **Generuoti reikalavimus**. Tai sukurs reikalavimus ištekliui. 
2. Pasirinkite komandos nario eilutę **konsultacijų vadovui** ir tada pasirinkite **Rezervuoti**. Atidaroma grafiko lenta su išteklių sąrašu. Pasirinkite išteklius ir tada pasirinkite **Rezervuoti**, kad rezervuotumėte išteklius pagal tą reikalavimą.
3. Pasirinkite komandos nario eilutę **tinklo technikui** ir tada pasirinkite **Rezervuoti**. Atidaroma grafiko lenta su išteklių sąrašu. Pasirinkite tuos pačius išteklius kaip anksčiau ir tada pasirinkite **Rezervuoti**, kad rezervuotumėte išteklius pagal tą reikalavimą.

### <a name="team-member-grid"></a>Komandos nario tinklelis 

**Komandos narių** tinklelyje du bendrųjų komandos narių įrašai panaikinami ir pakeičiami tik vienu ištekliumi. Yra vienas to ištekliaus reikšmių rinkinys, kuris yra numatytasis **vaidmens** ir **organizacijos vieneto** reikšmių rinkinys.

Išplėtę to komandos nario įrašo eilutę, komandos nario įraše galite matyti skirtingą priskyrimą abiem užduotims. Kiekviena priskyrimo eilutė turi tam tikras **vaidmens** ir **organizacijos vieneto** reikšmes. 

### <a name="estimates-grid"></a>Įvertinimo tinklelis 

**Įvertinimų** tinklelyje abu to paties ištekliaus priskyrimai įkainoti skirtingai. **A užduoties** priskyrimas ištekliui yra įkainotas naudojant **vaidmens** **Konsultavimo vadovas** atributo reikšmę. **B užduoties** priskyrimas tam pačiam ištekliui yra įkainotas naudojant **vaidmens** **Tinklo technikas** atributo reikšmę.


[!INCLUDE[footer-include](../includes/footer-banner.md)]