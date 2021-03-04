---
title: Projekto grafikai
description: Šioje temoje pateikta informacija apie tai, kaip sukurti grafiką.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2877f12a9ea3d288c4cf41f406cd8ca3e6cee821
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148428"
---
# <a name="project-schedules"></a>Projekto grafikai 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekto grafikas nurodo, kokius darbus reikia atlikti, kurie ištekliai atliks darbą ir laikotarpį, per kurį darbą reikia atlikti. Jis atspindi visą darbą, susijusį su projekto atlikimu laiku. Programoje Dynamics 365 Project Service Automation sukurkite projekto grafiką, suskaidydami darbą į valdomuosius uždavinius, įvertindami laiką, kurio reikia kiekvienai užduočiai atlikti, nustatydami užduočių priklausomybes ir užduoties trukmę bei įvertindami bendruosius išteklius, kurie atliks užduotis. Projekto grafikas sukuriamas projekto puslapio skirtuke **Grafikas**.
 
## <a name="tasks"></a>Užduotys

Pirmasis veiksmas kuriant projekto grafiką yra suskaidyti darbą iki valdomų dalių. PSA grafikas palaiko šias funkcijas:

- Projekto šakninis mazgas
- Suvestinės arba konteinerio užduotys
- Lapo mazgo užduotys

### <a name="project-root-node"></a>Projekto šakninis mazgas

Projekto šakninis mazgas yra projekto aukščiausiojo lygio suvestinės užduotis. Joje yra kuriamos visos kitos projekto užduotys. Šakninio mazgo pavadinimas visada nustatomas projekto pavadinimu. Šakninio mazgo pastangos, datos ir trukmė yra apibendrinamos pagal reikšmes, pateiktomis žemiau esančioje hierarchijoje. Negalite redaguoti šakninio mazgo ypatybių. Taip pat negalite panaikinti šakninio mazgo.

### <a name="summary-or-container-tasks"></a>Suvestinės arba konteinerio užduotys 

Suvestinės užduotys turi papildomų užduočių arba konteinerio užduočių. Jos neturi darbo pastangų arba savikainos. Jų darbo pastangos ir savikaina yra darbo pastangų ir jų konteinerio užduočių kainos apibendrinamoji reikšmė. Suvestinės užduoties pradžios data yra konteinerio užduočių pradžios data, o pabaigos data yra konteinerio užduočių pabaigos data. Suvestinės užduoties pavadinimą galima redaguoti, tačiau planavimo ypatybių (pastangų, datų ir trukmės) redaguoti negalima. Jei panaikinate suvestinės užduotį, taip pat panaikinate visas jos konteinerio užduotis.

### <a name="leaf-node-tasks"></a>Lapo mazgo užduotys

Lapo mazgo užduotys vaizduoja patį smulkiausią projekto darbą. Jos rodo apskaičiuotas pastangas, išteklius, planuojamas pradžios ir pabaigos datas bei trukmę.
 
## <a name="creating-a-task-hierarchy"></a>Užduočių hierarchijos kūrimas

Galite sukurti užduoties hierarchiją naudodamiesi šiomis parinktimis:

- Mygtukas **Pridėti užduotį**
- Mygtukas **Įtraukti užduotį**
- Mygtukas **Atvirkštinė užduoties įtrauka**
- Mygtukai **Perkelti aukštyn** ir **Perkelti žemyn**
- Spartieji klavišai, pritaikyti neįgaliesiems, ir klaviatūros spartieji klavišai

### <a name="add-task"></a>Pridėti užduotį

Mygtukas **Pridėti užduotį** leidžia sukurti naują užduotį hierarchijoje. Jei nepasirinksite vietos, užduotis bus pridėta į pabaigą. 

Kiekvienai užduočiai priskiriamas grafiko ID. Grafiko ID nurodo užduoties gylį ir padėtį hierarchijoje. Jis naudoja struktūros numeravimą. Užduotims, esančioms pirmajame lygyje po projekto šakninio mazgo, naudojama 1, 2, 3 ir t. t. numeravimo schema. Užduotims, esančioms žemiau pirmojo lygio, naudojama 1.1, 1.2, 1.3 ir t. t. numeravimo schema.

### <a name="indent-task"></a>Įtraukti užduotį

Kai užduotis įtraukiama, ji tampa antriniu virš jos esančios užduoties elementu. Užduoties grafiko ID perskaičiuojama taip, kad ji būtų pagrįsta nauju pirminės užduoties grafiko ID ir sektų struktūros numeravimo schemą. Pirminė užduotis dabar yra suvestinė užduotis arba konteinerio užduotis. Todėl ji tampa antrinių užduočių apibendrinamąja reikšme.

### <a name="outdent-task"></a>Atvirkštinė užduoties įtrauka 

Kai užduočiai pritaikoma atvirkštinė įtrauka, ji nebėra antrinis pirminės užduoties elementas. Grafiko ID perskaičiuojamas taip, kad atspindėtų užduoties atnaujintą gylį ir padėtį hierarchijoje. Ankstesnės pirminės užduoties pastangos, savikaina ir datos perskaičiuojamos taip, kad į juos nebūtų įtraukta ši užduotis.

### <a name="move-up-and-move-down"></a>Perkelti aukštyn arba perkelti žemyn. 

Mygtukai **Perkelti aukštyn** ir **Perkelti žemyn** pakeičia užduoties padėtį pirminėje hierarchijoje. Šio tipo pakeitimai nepaveikia užduoties pastangoms, savikainai, datoms ar trukmei. Paveikiamas tik užduoties grafiko ID. Grafiko ID perskaičiuojamas taip, kad atspindėtų užduoties naują padėtį pirminės užduoties antrinių užduočių sąraše.

### <a name="accessibility-and-keyboard-shortcuts"></a>Spartieji klavišai, pritaikyti neįgaliesiems, ir klaviatūros spartieji klavišai

Tinklelis **Grafikas** yra visiškai pasiekiamas ir gali būti naudojamas su ekrano skaitytuvais, pavyzdžiui, „Narrator“, „JAWS“ ar „NVDA“. Galite judėti per tinklelio sritį naudodami rodyklių klavišus (kaip programoje Microsoft Excel), galite naudoti tabuliavimo klavišą, kad pasiektumėte interaktyviuosius vartotojo sąsajos elementus, o norėdami pasirinkti ir iškviesti išplečiamuosius meniu galite naudoti rodyklės žemyn, ENTER arba tarpo klavišus. Stulpelių antraštės taip pat interaktyvios. Galite slėpti ir rodyti stulpelius, naudoti tabuliavimo ir rodyklių klavišus, kad judėtumėte per stulpelių antraštes, bei naudoti veiksmo mygtukus įrankių juostoje. Be to, galite naudoti šiuos sparčiuosius klavišus:

- **Atnaujinti**: ALT + SHIFT + F5
- **Pridėti**: ALT + SHIFT + INSERT
- **Naikinti**: ALT + SHIFT + DELETE
- **Pereiti aukštyn / žemyn**: ALT + SHIFT + rodyklė aukštyn / žemyn
- **Įtraukti / atvirkštinė įtrauka**: ALT_SHIFT + kairė / dešinė rodyklės
- **Išplėsti / sutraukti hierarchijas**: ALT + SHIFT + pliuso / minuso klavišai

## <a name="task-attributes"></a>Užduoties atributai

Užduoties pavadinimas apibūdina darbą, kurį reikia atlikti. Programoje PSA atributai, susieti su užduotimi, apibūdina užduoties grafiką ir personalo reikalavimus.

> ![Užduoties atributai](media/project-2.png)
 
### <a name="schedule-attributes"></a>Grafiko atributai

Atributai **Pastangos**, **Pradžios data**, **Pabaigos data** ir **Trukmė** apibrėžia užduoties grafiką.

Papildomo grafiko atributus sudaro:

- **Pastangų valandos**: įveskite valandų, reikalingų užduočiai užbaigti, įvertinimą. 
- **Trukmė**: nurodykite darbo dienų skaičių, kurio reikia užduočiai užbaigti.
- **Grafiko ID**: šis automatiškai sugeneruotas ID naudojamas užduotims hierarchijoje užsakyti. Priklausomybės tarp užduočių valdo faktinę tvarką, kurioje užduotys yra apdorojamos.
 
### <a name="staffing-attributes"></a>Darbuotojų atributai

Personalo atributai pasiekiami grafiko lauke **Ištekliai**. Galite ieškoti esamų išteklių arba spustelėti **Kurti** ir skyde **Spartusis kūrimas** pridėti projekto komandos narį kaip naują išteklių.

Laukai **Vaidmuo**, **Išteklių paskirstymo vienetas** ir **Padėties pavadinimas** yra naudojami apibūdinti užduoties personalo reikalavimus. Šie personalo atributai su užduočių grafiku naudojami pasiekiamiems ištekliams rasti, kad būtų galima atlikti šią užduotį.

**Vaidmuo** – nurodykite ištekliaus, kurio reikia užduočiai atlikti, tipą.

**Išteklių paskirstymo vienetas** – nurodykite vienetą, iš kurio turėtų būti skiriami užduoties ištekliai. Šis atributas paveikia užduoties savikainos ir pardavimo įvertinimą, jei ištekliaus savikaina ir sąskaitos tarifas nustatyti pagal išteklių paskirstymo vienetus.

**Padėties pavadinimas** – įveskite bendrajam ištekliui skirtą pavadinimą, kuris tarnaus kaip ištekliaus, kuris galiausiai atliks darbą, vietos rezervavimo ženklas

Lauke **Ištekliai** yra bendrojo ištekliaus ar, kai jis yra, įvardytojo ištekliaus padėties pavadinimas.

Lauke **Kategorija** yra reikšmės, kurios nurodo platesnį darbo tipą, į kurį užduotis gali būti grupuojama. Šis laukas nepaveikia planavimo ar personalo. Jis naudojamas tik ataskaitoms teikti.

### <a name="task-dependencies"></a>Užduoties priklausomybės 

Galite naudoti grafiką programoje PSA, kad kurtumėte ankstesnius ryšius tarp užduočių. Laukas **Ankstesnė veikla**, esantis po lauku **Užduotys**, pritaiko vieną ar daugiau reikšmių, kad nurodytų užduotis, nuo kurių užduotis priklauso. Užduočiai priskyrus ankstesnes reikšmes, užduotį pradėti galima tik atlikus visas ankstesnes užduotis. Dėl priklausomybės suplanuota užduoties pradžios data nustatoma iš naujo į datą, kai ankstesnės užduotys yra atliktos.

Užduočių režimas nepaveikia naujinimų, atliktų su ankstesnėmis / priklausomų užduočių pradžios ir pabaigos datomis.

## <a name="task-mode"></a>Užduoties režimas 

Užduoties režimas apibrėžia lapų mazgo užduočių planavimą. PSA palaiko du užduoties režimus kiekvienai užduočiai: automatinį planavimą ir rankinį planavimą.

### <a name="auto-scheduling"></a>Automatinis planavimas 
 
Kai užduoties režimas nustatytas į **Automatiškai suplanuota** užduočiai, užduočių planavimo modulis užduočių atributams naudoja planavimo taisykles, kad nustatytų užduoties grafiką.

#### <a name="scheduling-rules"></a>Planavimo taisyklės

Pagal numatytuosius nustatymus, jei lapo mazgo užduotis neturi ankstesnės veiklos, jos pradžios data nustatoma į projekto suplanuotą pradžios datą. Lapo mazgo užduoties trukmė visada apskaičiuojama kaip darbo dienų skaičius nuo jos pradžios datos iki pabaigos datos. Planuojant užduotį automatiškai, planavimo modulis taiko šias taisykles:

- Pagal projekto planavimo kalendorių, užduoties pradžios ir pabaigos datos turi būti darbo dienos. 
- Bet kuriai užduočiai, turinčiai ankstesnių užduočių, pradžios dara automatiškai nustatoma į vėliausią ankstesnių užduočių pabaigos datą.
- Pastangos skaičiuojamos naudojant šią formulę: darbuotojų skaičius x trukmė x valandos standartinėje darbo dienoje projekto kalendoriuje.

### <a name="manual-scheduling"></a>Neautomatinis planavimas

Jei automatinio planavimo taisyklės neatitinka jūsų reikalavimų, galite nustatyti užduoties režimą užduočiai į **Suplanuota rankiniu būdu**. Šis parametras neleidžia planavimo moduliui skaičiuoti kitų planavimo atributų reikšmių. Neatsižvelgiant į užduoties režimą, jei nustatysite užduotims ankstesnę veiklą, tai visada paveiks priklausomos užduoties pradžios datą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]