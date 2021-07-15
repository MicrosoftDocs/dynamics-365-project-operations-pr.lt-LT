---
title: „Microsoft Project Client” integravimas
description: Gali būti sudėtinga planuoti ir laikytis projekto grafiko, todėl projektų vadovai turi naudoti įrankius, padedančius susitvarkyti su šia užduotimi. Integravimas su „Microsoft Project Client” padeda atidaryti ir valdyti projekto darbo paskirstymo struktūrą.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b312ec5b1f4e6a98a2cbf1667b2f55b758b2d613
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269845"
---
# <a name="microsoft-project-client-integration"></a>„Microsoft Project Client” integravimas

[!include [banner](../includes/banner.md)]

Gali būti sudėtinga planuoti ir laikytis projekto grafiko, todėl projektų vadovai turi naudoti įrankius, padedančius susitvarkyti su šia užduotimi. Integravimas su „Microsoft Project Client” padeda atidaryti ir valdyti projekto darbo paskirstymo struktūrą. Projektų vadovas gali bet kokius keitimus publikuoti „Dynamics 365 Finance” projekto darbo paskirstymo struktūroje.

> [!NOTE]
> Jei naudojate liepos mėn. naujinimą (10.0.4 versija), turite įdiegti KB 4054797 ir 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>„Microsoft Project Client” papildinio konfigūravimas
Siekiant įgalinti integravimą su „Microsoft Project Client”, reikalaujama įdiegti „Microsoft Dynamics 365” papildinį į vartotojo programą „Microsoft Project Client”. Tai atliekama atidarius **projektų valdymo darbo sritį**.

• Spustelėkite **Konfigūruoti projekto kliento papildinį** iš darbo srities skyriaus **Saitai** > **Sąranka**.

• Spustelėkite **Atidaryti**, tada paraginti, spustelėkite **Vykdyti**.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Programoje „Microsoft Project Client” atidarykite ir redaguokite darbo paskirstymo struktūros juodraštį
Jei „Dynamics 365 Finance” esantis projektas jau turi sukurtą darbo paskirstymo struktūrą, šią darbo paskirstymo struktūrą galima atidaryti programoje „Microsoft Project Client”, jeigu darbo paskirstymo struktūra yra juodraščio būsenos. Norėdami atidaryti puslapį **Projektas**, spustelėkite skirtuke **Planas** esantį saitą **Atidaryti programoje „Microsoft Project”**. Šis puslapis taip pat gali būti atidarytas programoje „Microsoft Project Client”, skirtuke **„Microsoft Dynamics 365”** spustelint **Atidaryti**. Sąraše pasirinkite **Juridinis subjektas** ir **Projektas**.

> [!NOTE]
> Jei naudojate naršyklę „Internet Explorer” jums reikės spustelėti **Įrašyti**, kad rankiniu būdu atidarytumėte iš tos vietos, į kurią atsisiųstas failas. Arba spustelėkite **Įrašyti ir atidaryti**, kad atidarytumėte failą programoje „Microsoft Project Client”. Įrašydami nepervardykite failo.

Prieš redaguodami failą programoje „Microsoft Project Client”, turite jį išregistruoti. Skirtuke **„Microsoft Dynamics 365”** spustelėkite **Išregistruoti**. Taip kiti vartotojai negalės tuo pačiu metu redaguoti darbo paskirstymo struktūros programoje „Finance”. Jei atlikę redagavimą, norite publikuoti darbo paskirstymo struktūrą, skirtuke **„Microsoft Dynamics 365”** spustelėkite **Įregistruoti**.

Jei projekto komanda jau buvo įtraukta į projektą programoje „Finance”, į išteklių sąrašą bus įrašyti komandos nariai. Jeigu projekto komanda dar nebuvo įtraukta į projektą, galite pasirinkti išteklius ir sukurti komandą programoje „Microsoft Project Client” skirtuke **„Microsoft Dynamics 365”** spustelėdami mygtuką **Ištekliai**. 

Vykdant įregistravimo procesą toliau pateikiami duomenys bus sinchronizuojami su „Finance”.

•   Užduoties pavadinimas

•   Pradžios data

•   Pabaigos data

•   Ankstesnės užduotys

•   Išteklių pavadinimai

•   Kategorija

•   Išteklių kategorija

•   Darbo valandos

•   Pastabos

•   Pirmumas

> [!NOTE]
> Jeigu į savo „Microsoft Project Client” failą įtrauksite kitų stulpelių, jie nebus įrašyti faile ir nebus rodomi, kai failas bus dar kartą atidarytas.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Esamo projekto darbo paskirstymo struktūros kūrimas, naudojant „Microsoft Project Client”
Norėdami sukurti naują darbo paskirstymo struktūrą, naudojant „Microsoft Project Client”, atlikite tolesnius veiksmus.


1.  Atidarykite „Microsoft Project Client”.

2.  Skirtuke **„Microsoft Dynamics 365”** spustelėkite **Atidaryti**.

3.  Pasirinkite projekto **Juridinį subjektą**.

4.  Pasirinkite **Projektas**.

5.  Skirtuke **„Microsoft Dynamics 365”** spustelėkite **Išregistruoti**.

6.  Kai būsite pasirengę publikuoti programoje „Finance”, skirtuke **„Microsoft Dynamics 365”** spustelėkite **Įregistruoti**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Esamo projekto esamos darbo paskirstymo struktūros keitimas, naudojant „Microsoft Project Client”
Jei norite sukurti naują darbo paskirstymo struktūrą naudodami „Microsoft Project Client” ir pakeisti esamo projekto darbo paskirstymo struktūrą, atlikite toliau nurodytus veiksmus.

1.  Atidarykite „Microsoft Project Client”.

2.  Programoje „Microsoft Project Client” sukurkite grafiką.

3.  Skirtuke **„Microsoft Dynamics 365”** spustelėkite **Įrašyti pakeitimus** > **Keisti esamą projektą**.

4.  Pasirinkite projekto **Juridinį subjektą**.

5.  Pasirinkite **Projektas**.

6.  Spustelėkite **Gerai**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Naujo projekto kūrimas programoje „Microsoft Project Client”


1.  Atidarykite „Microsoft Project Client”.

2.  Programoje „Microsoft Project Client” sukurkite grafiką.

3.  Skirtuke **„Microsoft Dynamics 365”** spustelėkite **Įrašyti pakeitimus** > **Įrašyti į naują projektą**.

4.  Pasirinkite projekto **Juridinį subjektą**.

5.  Jeigu reikia, įveskite **Projekto ID**.

6.  Įveskite **projekto pavadinimą**.

7.  Pasirinkite **Projekto tipas**, **Projekto grupė** ir **Projekto sutarties ID**. Arba galite sukurti naują projekto sutartį spustelėję **Nauja**.

8.  Pasirinkite **kalendorių**, kurį naudosite paskirstydami išteklius.

11. Spustelėkite **Gerai**.

> [!NOTE]
> Papildinys „Project Client“ nepalaiko toliau nurodytų simbolių projekto ID formatu.
> 
>   - Pabraukimo brūkšnys
>   - Laikotarpis
>   - Tarpas
>   - Pasvirasis brūkšnys

[!INCLUDE[footer-include](../includes/footer-banner.md)]
