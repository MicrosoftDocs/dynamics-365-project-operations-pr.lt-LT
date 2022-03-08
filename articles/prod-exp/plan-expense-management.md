---
title: Išlaidų valdymo konfigūravimas
description: Šiame straipsnyje aprašomos pastabos ir sprendimai, kuriuos turite padaryti planavimo proceso metu, prieš konfigūruodami išlaidų valdymą programoje „Microsoft Dynamics 365 Finance“.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eca4362b0ff5d37b131e1d96e311aa48ac20397618314936944ba66e458dbdc2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007471"
---
# <a name="configure-expense-management"></a>Išlaidų valdymo konfigūravimas

Šioje temoje aprašomos pastabos ir sprendimai, kuriuos turite padaryti planavimo proceso metu, prieš konfigūruodami išlaidų valdymą. Išlaidų valdyme galite saugoti informaciją apie mokėjimo būdus, kelionių paraiškas, išlaidų ataskaitas, strategijas ir kt.

Kadangi daugelis sprendimų, kuriuos turite atlikti planuodami savo išlaidų valdymo konfigūraciją, priklauso nuo organizacijos hierarchijos ir finansinės struktūros, turite nurodyti šių sričių planavimo dokumentus.

## <a name="intercompany-expenses"></a>Vidinės įmonės išlaidos

Kai įjungiate vidinės įmonės išlaidas, leidžiate juridiniams subjektams ir darbuotojams patirti išlaidų kito juridinio subjekto vardu ir rinkti mokėjimus iš jūsų organizacijos darbo juridinio subjekto. Pavyzdžiui, darbuotojas, esantis juridiniame subjekte A, baigia projektą, skirtą juridiniam subjektui B, o vykdant projektą patirta su kelionėmis susijusių išlaidų. Jei vidinės įmonės išlaidos įjungtos, darbuotojas gali pateikti išlaidų ataskaitą, kuria registruotos išlaidos bus priskirtos juridiniam subjektui B, o išlaidas apmokėti turės juridinis subjektas A. Jei jūsų organizacija neturi kelių juridinių subjektų, jums nereikia įjungti vidinės įmonės išlaidų.

**Sprendimas:** ar norite įjungti vidinės įmonės išlaidas?

## <a name="financial-management"></a>Finansų valdymas

Išlaidų valdymas glaudžiai integruotas su jūsų organizacijos finansų valdymu. Daug jūsų išlaidų valdymo konfigūracijų priklausys nuo sprendimų, susijusių su jūsų organizacijos finansais. Tolesniuose skyriuose aprašomos įvairios sritys, kuriose reikia planuoti ir priimti sprendimus, atsižvelgiant į jūsų organizacijos finansinius sprendimus ir vadovų komandos rekomendacijas.

### <a name="per-diems"></a>Dienpinigiai

Turite nustatyti darbuotojų dienpinigius, kuriuos teikia jūsų organizacija. Kadangi dienpinigiai paprastai skirti tokioms išlaidoms kaip maitinimo, apgyvendinimo ir kitos atsitiktinės išlaidos, galite sukurti jūsų organizacijos siūlomų dienpinigių taisykles. Dienpinigiai gali būti pagrįsti metų laiku, kelionės vieta arba abiem. Kai sukuriate dienpinigius, galite nurodyti, kad už dienpinigius procentinė dalis bus išskaičiuota, jei darbuotojas gaus papildomą maitinimą ar aptarnavimą. Be to, galite apibrėžti dienpinigių normas ir nustatyti mažiausią bei didžiausią valandų skaičių, už kurias būtų skiriami dienpinigiai darbuotojui keliaujant.

**Sprendimai**

- Pirmosios ir paskutinės dienų numatytosios dienpinigių taisyklės.

    - Koks minimalus skaičius valandų, už kurias per dieną darbuotojas gali prašyti ir gauti dienpinigių?
    - Ar maisto išlaidoms padengti siūlomos sumos už pirmąją ir paskutinę dienas sumažintos? Jei sumažintos, kokiu procentu?
    - Ar apgyvendinimo išlaidoms padengti siūlomos sumos už pirmąją ir paskutinę dienas sumažintos? Jei sumažintos, kokiu procentu?
    - Ar kitoms išlaidoms padengti siūlomos sumos už pirmąją ir paskutinę dienas sumažintos? Jei sumažintos, kokiu procentu?

- Numatytosios dienpinigių taisyklės.

    - Ar maisto išlaidoms skirta dienpinigių suma sumažinama, jei, pavyzdžiui, maistas yra nemokamas? Jei sumažinama, kokiu procentu sumažinama suma už kiekvieną patiekala?
    - Ar maistui skirtos sumos sumažinimas apskaičiuojamas pagal dieną, kelionę, ar pagal patiekalų skaičių per dieną?
    - Ar dienpinigių sumas reikia suapvalinti reguliariai, ar iki artimiausios didesnės apvalinimo sumos?
    - Ar dienpinigiai apskaičiuojami pagal 24 valandų laikotarpį, ar kalendorinę dieną?

- Dienpinigių taisyklės, pagrįstos vieta.

    - Ar dienpinigių suma priklauso nuo vietos? Kokios vietos įtrauktos?
    - Jei dienpinigių suma priklauso nuo vietos, kokio dydžio procentinė suma skiriama kiekvienai vietai, atsižvelgiant į toliau nurodytus išlaidų tipus?

        - Maitinimas
        - Viešbutis
        - Kitos išlaidos

### <a name="expense-management-journals-and-accounts"></a>Išlaidų valdymo žurnalai ir klientai

Vykdant išlaidų valdymą reikia naudoti kelis žurnalus ir klientus. Pavyzdžiui, turite nuspręsti, ar tas pats klientas naudojamas tiek tvarkant avansinius mokėjimus, tiek sprendžiant kredito kortelių ginčus.

**Sprendimai**

- Kuriame DK žurnalae registruojamos patvirtintos išlaidų ataskaitos?
- Kuris klientas naudojamas tvarkant avansinius mokėjimus?
- Ar avansiniai mokėjimai turi būti registruojami nedelsiant?

### <a name="payment-methods"></a>Mokėjimo būdai

Kai leidžiate darbuotojams registruoti išlaidas jūsų įmonės vardu, turite nustatyti mokėjimo būdus, kuriuos darbuotojai gali naudoti. Pavyzdžiui, galite leisti darbuotojams naudoti grynuosius pinigus arba įmonės kredito kortelę. Taip pat galite leisti darbuotojams naudoti asmenines kredito korteles, o tada grąžinti darbuotojams pinigus. Turite nustatyti šiuos sprendimus, skirtus kiekvienam leidžiam mokėjimo būdui.

**Sprendimai**

- Kokie mokėjimo būdai leidžiami?
- Kam priklauso mokėjimo būdo išlaidos?
- Ar naudojama korespondentinio tipo sąskaita? Jei korespondentinio tipo sąskaita naudojama, kokia ji?
- Jei korespondentinio tipo sąskaita naudojama, kokia tai sąskaita?
- Jei mokėjimo būdas yra kredito kortelė, ar mokėjimo būdą reikia naudoti tik apdorojant importuojamas operacijas?

### <a name="expense-categories-and-shared-categories"></a>Išlaidų kategorijos ir bendrai naudojamos kategorijos

Kai darbuotojai kuria išlaidų ataskaitą, visos užregistruotos išlaidos turi būti susietos su išlaidų kategorija. Išlaidų kategorijos gaunamos iš bendrai naudojamų kategorijų, kurias galima bendrai naudoti jūsų organizacijos juridiniuose subjektuose. Šias kategorijas taip pat galima bendrai naudoti srityje Projektų valdymas ir apskaita, atsižvelgiant į jūsų organizacijos sąranką. Atsižvelgdami į savo organizacijos pobūdį ir diegimo komandos pateiktus nurodymus, nustatykite, ar kategorijos, naudojamos dalyje Išlaidų valdymas, bus naudojamos tik dalyje Išlaidų valdyma,s ar bus bendrai naudojamos srityse Projekto valdymas ir apskaita bei Išlaidų valdymas. Atminkite: šias kategorijas galima bendrai naudoti dalyse Projektas ir Apskaita arba Projektas ir Gamyba, bet ne Išlaidos ir Gamyba. Turite atlikti šiuos kiekvienos išlaidų kategorijos sprendimus.

**Sprendimai**

- Kokia tai yra išlaidų kategorija? Pavyzdžiui, skrydžių, viešbučių arba kilometražo kategorijos.
- Ar išlaidų kategoriją taip pat galima naudoti dalyje Projektų valdymas ir apskaita?
- Koks tai yra išlaidų tipas?
- Koks yra numatytasis išlaidų kategorijos mokėjimo būdas?
- Ar išlaidų kategorijos išlaidos turi būti detaliai išvardytos?
- Kokia yra pagrindinė numatytoji išlaidų kategorijos sąskaita?
- Kokia yra numatytoji išlaidų kategorijos prekės PVM grupė?
- Ar leidžiami papildomi išlaidų kategorijos mokėjimo būdai? Jei leidžiama taikyti papildomus mokėjimo būdus, kokie jie yra?
- Ar šioje išlaidų kategorijoje yra subkategorijų? Jei yra subkategorijų, taip pat reikia priimti toliau nurodytus sprendimus:

    - Ar kokioms nors subkategorijoms netaikomas mokesčių susigrąžinimas?
    - Kokia yra subkategorijų prekės PVM grupė?

Jei išlaidų kategorija taip pat naudojama srityje Projektų valdymas ir apskaita, atsakykite į likusius klausimus. Kitu atveju pereikite prie kito skyriaus.

- Kokios išlaidų sąskaitos bus naudojamos šioms išlaidoms?

    - Savikaina
    - Atlyginimo paskirstymas
    - NG – Savikaina
    - Išlaidos – Prekė
    - NG – Išlaidų vertė – Prekė
    - Sukauptas nuostolis
    - NG – sukauptas nuostolis

- Kokios įplaukų sąskaitos bus naudojamos tolesniais atvejais?

    - Įplaukos, kurioms išrašyta SF
    - Sukauptos įplaukos – Pardavimo vertė
    - NG – Pardavimo vertė
    - Sukauptos įplaukos – Gamyba
    - NG – Gamyba
    - Sukauptos įplaukos – Pelnas
    - NG – Pelnas
    - Sukauptos įplaukos – Abonementas
    - NG – Abonementas

### <a name="taxes"></a>Mokesčiai

Su išlaidomis susiję mokesčiai: turite nustatyti, kas įtraukta arba įjungta išlaidų ataskaitose.

**Sprendimai**

- Ar PVM įtrauktas į išlaidų sumas?
- Ar reikia įjungti išlaidų mokesčių atkūrimą?

    > [!NOTE]
    > Jei planuojate didžiąją knygą ir nusprendžiate taikyti JAV PVM ir naudoti mokesčių taisykles, negalite įjungti išlaidų mokesčių susigrąžinimo. (Norėdami taikyti JAV PVM ir naudoti mokesčių taisykles, nustatykite parinkties **Taikyti PVM mokesčių taisykles** parametrą **Taip**).

## <a name="policies"></a>Strategijos

Sukūrę išlaidų ataskaitų strategijas, galite padėti savo organizacijai sutaupyti laiko ir pinigų, kai darbuotojai registruoja išlaidas jos vardu. Strategijos padeda užtikrinti, kad darbuotojai galėtų neviršyti biudžeto, pateiktų visą reikalingą informaciją ir leistų pinigus tik tada, kai tai būtina. Turite priimti šiuos sprendimus dėl kiekvienos išlaidų ataskaitos strategijos ir kiekvienos jūsų sukurtos išlaidų ataskaitos patvirtinimo strategijos.

**Sprendimai**

- Koks politikos pavadinimas?
- Kam skirta išlaidų strategija?
- Jei anksčiau nutarėte įjungti vidinės įmonės išlaidas, kurioms jūsų organizacijos įmonėms ši strategija taikoma?
- Kada strategija įsigalioja?
- Kada strategijos galiojimas pasibaigia?
- Kas yra strategijos taisyklė?
- Koks politikos taisyklės rezultatas?


[!INCLUDE[footer-include](../includes/footer-banner.md)]