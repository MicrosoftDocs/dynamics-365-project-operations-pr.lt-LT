---
title: Darbo paskirstymo struktūros kūrimas
description: Šioje temoje paaiškinta, kaip kurti darbo paskirstymo struktūrą (WBS), įskaitant naujos planavimo sąsajos pagrindinius valdiklius.
author: ruhercul
ms.date: 01/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 701c386af8a227308d6868deda27a63e6101e85f667b0392501bb0490329f484
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998741"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Darbo paskirstymo struktūros (WBS) kūrimas

Projekto grafikas nurodo, kokius darbus reikia atlikti, kurie ištekliai atliks darbą ir laikotarpį, per kurį darbą reikia atlikti. Grafikas atspindi visą darbą, susijusį su projekto atlikimu laiku. Naudodami „Dynamics 365 Project Operations“ galite sukurti projekto grafiką:

  - Suskirstydami darbą į įvykdomas užduotis;
  - Apskaičiuodami laiką, kurio reikia kiekvienai užduočiai atlikti;
  - Nustatydami užduoties priklausomybes;
  - Nustatydami užduoties trukmes;
  - Apskaičiuodami bendruosius išteklius, kurie atliks užduotis. 

Projekto grafikas sukuriamas puslapio **Projektas** skirtuke **Grafikas**.

## <a name="tasks"></a>Užduotys

Pirmasis veiksmas kuriant projekto grafiką yra suskaidyti darbą iki valdomų dalių. „Project Operations“ grafikas palaiko šias funkcijas:

- Suvestinės arba konteinerio užduotys
- Lapo mazgo užduotys

### <a name="summary-tasks"></a>Suvestinės užduotys

Suvestinės užduotys gali saugoti kitas suvestines užduotis arba lapo mazgo užduotis. Jos neturi darbo pastangų arba savikainos. Jų darbo pastangos ir savikaina yra darbo pastangų ir jų konteinerio užduočių kainos apibendrinamoji reikšmė. Suvestinės užduoties pradžios data yra konteinerio užduočių pradžios data, o pabaigos data yra konteinerio užduočių pabaigos data. Suvestinės užduoties pavadinimą galima redaguoti, tačiau planavimo ypatybių, įskaitant pastangas, datas ir trukmes, redaguoti negalima. Jei panaikinate suvestinės užduotį, taip pat panaikinate visas jos konteinerio užduotis.

### <a name="leaf-node-tasks"></a>Lapo mazgo užduotys

Lapo mazgo užduotys vaizduoja patį smulkiausią projekto darbą. Jos rodo apskaičiuotas pastangas, išteklius, planuojamas pradžios ir pabaigos datas bei trukmę.

## <a name="create-a-task-hierarchy"></a>Užduočių hierarchijos kūrimas

### <a name="add-a-task"></a>Užduoties įtraukimas

Norėdami įtraukti vieną ar daugiau užduočių, atlikite toliau nurodytus veiksmus.

1. Eikite į **Projektai** ir pasirinkite bei atidarykite projekto įrašą, kuriam norite sukurti grafiką. 
2. Pasirinkite skirtuką **Užduotys**. 
3. Pasirinkite **Įtraukti naują užduotį**, įveskite užduoties pavadinimą, o tada paspauskite „Enter“ (įvesti).
2. Įveskite kitos užduoties pavadinimą ir dar kartą paspauskite „Enter“ (įvesti), kol bus sudarytas visas užduočių sąrašas.

### <a name="manage-hierarchy-of-a-task"></a>Užduoties hierarchijos valdymas

Kai užduotis įtraukiama, ji tampa antriniu virš jos esančios užduoties elementu. Užduoties grafiko ID perskaičiuojama taip, kad ji būtų pagrįsta nauju pirminės užduoties grafiko ID ir sektų struktūros numeravimo schemą. Pirminė užduotis dabar yra suvestinės užduotis. Todėl ji tampa antrinių užduočių apibendrinamąja reikšme. Kai užduotis perkeliama į aukštesnį lygį, ji nebėra antrinis pirminės užduoties elementas. Grafiko ID perskaičiuojamas taip, kad atspindėtų užduoties atnaujintą gylį ir padėtį hierarchijoje. Ankstesnės pirminės užduoties pastangos, savikaina ir datos perskaičiuojamos taip, kad į juos nebūtų įtraukta ši užduotis.

Norėdami perkelti užduotį į žemesnį arba aukštesnį lygį, atlikite toliau nurodytus veiksmus.

1. Puslapio **Projektas** skirtuko **Užduotys** dalyje **Suvestinės užduotys** pasirinkite tris vertikalius taškus greta užduoties pavadinimo, o tada pasirinkite **Padaryti antrine užduotimi**. 
2. Pažymėkite užduotį, kurią norite perkelti į žemesnį arba aukštesnį lygį. Norėdami pasirinkti daugiau nei vieną užduotį, pasirinkite užduotį, paspauskite ir laikykite „Ctrl“ klavišą, o tada pasirinkite papildomas užduotis.
2. Pasirinkite **Perkelti į žemesnį lygį** arba **Pakelti antrinę užduotį į aukštesnį lygį**, kad perkeltumėte užduotis į arba iš suvestinės užduočių.

### <a name="move-tasks-up-and-down"></a>Užduočių perkėlimas aukštyn ir žemyn

Užduotis galite perkelti į bet kurį darbo paskirstymo struktūros lygį vienu iš dviejų būdų:

- Pažymėkite dar vieną užduotį ir nuvilkite jas į norimą vietą.
- Pažymėkite vieną ar daugiau užduočių, spustelėkite dešiniuoju pelės mygtuku ir pasirinkite **Iškirpti**, grafike pasirinkite paskirties langelį, o tada spustelėkite dešiniuoju pelės mygtuku ir pasirinkite **Įklijuoti**.

## <a name="task-attributes"></a>Užduoties atributai

Užduoties pavadinimas apibūdina darbą, kurį reikia atlikti. Programoje „Project Operations“ atributai, susieti su užduotimi, apibūdina užduoties grafiką ir personalo reikalavimus.

## <a name="schedule-attributes"></a>Grafiko atributai

Atributai **Pastangos**, **Pradžios data**, **Pabaigos data** ir **Trukmė** apibrėžia užduoties grafiką.

Šioje lentelėje rodomi papildomi grafiko atributai.

| **Galutinis rodomas pavadinimas** | **Galutinis aprašas** |
| --- | --- |
| Pastangos užbaigtos (valandos) | Užbaigtas užduoties darbas valandomis. |
| Trukmė | Rodoma užduoties trukmė dienomis. |
| Bendros pastangos | Bendra užduoties darbo apimtis valandomis. |
| Pabaiga | Pabaigos data ir laikas. |
| % užbaigta | Užbaigtos užduoties procentinė dalis. |
| Projekto talpykla | Užduočių lentą galima grupuoti pagal segmentą, kad kiekvienas segmentas turėtų savo stulpelį. |
| Likusios pastangos (val.) | Likęs užduoties darbas valandomis. |
| Paleisti | Pradžios data ir laikas. |
| Pavadinimas / vardas ir pavardė | Užduoties pavadinimas. |
| ID | Darbo paskirstymo struktūroje esančios užduoties ID. |

Kaip administratorius galite apibrėžti užduoties objekto pasirinktinius laukus. Tačiau laukų grafiko tinklelyje rodyti negalima. Norėdami peržiūrėti pasirinktinius laukus, juos įtraukite į **Projekto užduotis** išsamios informacijos puslapį.

## <a name="staffing-attributes"></a>Darbuotojų atributai

Personalo atributai pasiekiami grafiko lauke **Ištekliai**. Galite ieškoti esamų išteklių arba pasirinkti **Kurti** ir skyde **Spartusis kūrimas** pridėti projekto komandos narį kaip naują išteklių.

Laukai **Vaidmuo**, **Išteklių paskirstymo vienetas** ir **Padėties pavadinimas** yra naudojami apibūdinti užduoties personalo reikalavimus. Šie personalo atributai su užduočių grafiku naudojami pasiekiamiems ištekliams rasti, kad būtų galima atlikti šią užduotį.

   - **Vaidmuo**: nurodykite ištekliaus, kurio reikia užduočiai atlikti, tipą.
   - **Išteklių paskirstymo vienetas**: nurodykite vienetą, iš kurio turėtų būti skiriami užduoties ištekliai. Šis atributas paveikia užduoties savikainos ir pardavimo įvertinimą, jei ištekliaus savikaina ir sąskaitos tarifas nustatyti pagal išteklių paskirstymo vienetus.
   - **Padėties pavadinimas**: įveskite bendrojo ištekliaus pavadinimą, kuris tarnaus kaip ištekliaus, kuris galiausiai atliks darbą, vietos rezervavimo ženklas.

Lauke **Ištekliai** yra bendrojo ištekliaus ar, kai jis yra, įvardytojo ištekliaus padėties pavadinimas.

Lauke **Kategorija** yra reikšmės, kurios nurodo platesnį darbo tipą, į kurį užduotis gali būti grupuojama. Šis laukas nepaveikia planavimo ar personalo. Vietoje to laukas naudojamas tik ataskaitoms teikti.

## <a name="task-dependencies"></a>Užduoties priklausomybės

Galite naudoti grafiką programoje „Project Operations“, kad kurtumėte ankstesnės užduotues ryšius tarp užduočių. Laukas **Ankstesnė užduotis** naudoja vieną ar daugiau reikšmių, kad nustatytų užduotis, nuo kurių priklauso užduotis. Užduočiai priskyrus ankstesnės užduoties reikšmes, užduotį pradėti galima tik atlikus visas ankstesnes užduotis. Dėl priklausomybės suplanuota užduoties pradžios data nustatoma iš naujo į datą, kai ankstesnės užduotys yra atliktos.

Užduočių režimas nepaveikia naujinimų, atliktų su ankstesnėmis / priklausomų užduočių pradžios ir pabaigos datomis.

## <a name="accessibility-and-keyboard-shortcuts"></a>Spartieji klavišai, pritaikyti neįgaliesiems, ir klaviatūros spartieji klavišai

Tinklelis **Grafikas** yra visiškai pasiekiamas ir gali būti naudojamas su ekrano skaitytuvais, pavyzdžiui, „Narrator“, „JAWS“ ar „NVDA“. Galite judėti per tinklelio sritį naudodami rodyklių klavišus (kaip programoje „Microsoft Excel“), galite naudoti tabuliavimo klavišą, kad pasiektumėte interaktyviuosius vartotojo sąsajos elementus, o norėdami pasirinkti ir atidaryti išplečiamuosius meniu galite naudoti rodyklės žemyn, „Enter“ arba tarpo klavišus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]