---
title: Darbo paskirstymo struktūros apžvalga
description: Darbo paskirstymo struktūra (WBS) yra darbo, kuris bus atliekamas vykdant projektą, aprašas. Tai užduočių hierarchija, vaizduojanti projekto komandos darbo sudėties ir kiekvieno komponento arba užduoties dydžio, savikainos ir trukmės suvokimą.
author: Yowelle
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d0cfcc27c69695fc6fe897e798b2831528833e6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080811"
---
# <a name="work-breakdown-structures-overview"></a>Darbo paskirstymo struktūros apžvalga

[!include [banner](../includes/banner.md)]

Darbo paskirstymo struktūra (WBS) yra darbo, kuris bus atliekamas vykdant projektą, aprašas. Tai užduočių hierarchija, vaizduojanti projekto komandos darbo sudėties ir kiekvieno komponento arba užduoties dydžio, savikainos ir trukmės suvokimą. WBS yra trys svarbiausi tikslai.

-   Aprašyti užduočių darbo suskirstymą arba sudėtį.
-   Sudaryti projekto darbo grafiką.
-   Įvertinti kiekvienos užduoties savikainą.

WBS išsamumo laipsnis priklauso nuo tikslumo lygio, pagal kurį vertinama, ir sekimo lygio, kurio reikia pagal minėtus vertinimus. Vykdant projektus, kurių metu nukrypimai nuo grafiko arba savikainos beveik netoleruojami, paprastai reikia parengti išsamesnes WBS ir kruopščiai sekti darbo eigą bei savikainą atsižvelgiant į WBS. Tokie projektai dažnai parengiami statybų ir inžinerijos srityse. 

Priešingai, projektai tam tikrose srityse, pvz., žiniasklaidoje ir reklamoje, programinėje įrangoje ir IT infrastruktūroje, paprastai yra unikalūs, o produktyvumas yra susijęs su užduotį atliekančio asmens patirtimi ir kompetencija. Todėl šiose srityse naudojama WBS, siekiant įvertinti projekto dydį, o ne atidžiai sekti šio projekto eigą. 

WBS kūrimas yra daug pastangų reikalaujantis procesas, kuris paprastai užtrunka ilgai ir reikalauja, kad nemažai žmonių bendradarbiautų ir pateiktų informaciją. Šioje temoje aprašoma, kaip naudoti WBS patobulinimus, norint patenkinti vertinimo ir sekimo reikalavimus.

## <a name="prerequisites-for-creating-a-wbs"></a>WBS kūrimo būtinosios sąlygos
Norėdami sukurti WBS, turite mokėti sukurti darbo grafiką ir apskaičiuoti darbo savikainą.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Darbo grafiko kūrimo būtinosios sąlygos

Norėdami naudoti visas WBS funkcijų planavimo galimybes, atlikite toliau aprašomus sąrankos veiksmus.

1.  Numatytojo kalendoriaus ir projekto kalendoriaus nustatymas
    1.  Spustelėkite **Projektų valdymas ir apskaita** &gt; **Sąranka** &gt; **Projektų valdymo ir apskaitos parametrai** &gt; **Planavimas**. Lauke **Numatytasis darbo kalendorius** nurodykite numatytąjį kalendorių. Šis numatytasis darbo kalendorius bus naudojamas kuriant visus naujus projektus.
    2.  Galite pakeisti tam tikro projekto numatytąjį kalendorių. Spustelėkite išsamios informacijos apie projektą puslapį, tada „FastTab” **Projekto komanda ir planavimas** atnaujinkite lauką **Planavimo kalendorius**, pasirinkę kitą kalendorių.

2.  Nustatykite įprastas darbo dienas ir darbo valandas. Kalendorius, kurį nustatėte kaip projekto darbo kalendorių, bus naudojamas WBS siekiant nustatyti toliau pateikiamą informaciją.

-   Darbo dienos ir šventės
-   Darbo valandų skaičius per dieną

Jei norite nustatyti kalendoriaus darbo dienas ir darbo valandas arba sukurti naują kalendorių, spustelėkite **Organizacijos administravimas** &gt; **Bendra** &gt; **Kalendoriai**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Darbo savikainos įvertinimo būtinosios sąlygos

Norėdami naudotis visomis WBS esančiomis savikainos įvertinimo galimybėmis, turite nustatyti darbuotojų, darbo, išlaidų ir mokesčių bei elementų kategorijų savikainą ir pardavimo kainas.

-   Norėdami nustatyti darbo, išlaidų ir mokesčių kategorijų savikainą ir pardavimo kainas, spustelėkite **Projektų valdymas ir apskaita** &gt; **Sąranka** &gt; **Kainos**.
-   Norėdami nustatyti elementų savikainą ir pardavimo kainą, naudokite kiekvieno elemento puslapį **Prekybos sutartys** sąrašo puslapyje **Išleisti produktai**, esančiame Produkto informacijos valdymas.

## <a name="creating-a-wbs"></a>WBS kūrimas
Kuriant WBS, atliekami trys veiksmai.

1.  **Darbo skaidymas** – darbas suskirstomas į įveikiamas dalis arba užduotis.
2.  **Darbo grafikas** – įvertinamas laikas, kurio reikia norint atlikti užduotį, nustatomos užduočių tarpusavio priklausomybės ir pasirenkamos užduočių pradžios ir pabaigos datos.
3.  **Savikainos įvertinimas** – įvertinama kiekvienos užduoties savikaina.

Tolesniuose skyriuose aptariama, kaip WBS galimybės gali padėti vykdant pirmiau minėtas veiklas.

### <a name="work-decomposition"></a>Darbo skaidymas

Darbo suskirstymo arba skaidymo kūrimas paprastai yra pirmas veiksmas, atliekamas kuriant WBS. WBS funkcijos palaiko toliau nurodytas pagrindines darbo suskirstymo arba skaidymo konstrukcijas. 

**Projekto šakninė užduotis** Projekto šakninė užduotis yra projekto aukščiausio lygio suvestinės užduotis. Joje yra kuriamos visos kitos projekto užduotys. Šakninės užduoties pavadinimas visada nustatomas pagal projekto pavadinimą. Šakninio mazgo pastangos, datos ir trukmė apibendrina užduočių, esančių šakninėje užduotyje, reikšmes. Negalite nei modifikuoti šakninio mazgo ypatybių, nei jo panaikinti.

**Suvestinės arba konteinerio užduotys** Suvestinės užduotis yra užduotis, kurioje yra antrinių užduočių arba susijusių užduočių. Pati suvestinė užduotis neturi jokių darbo pastangų nei savikainos. Vietoj to, suvestinės užduoties darbo pastangos ir savikaina yra susijusių užduočių darbo pastangų ir savikainos suma. Susijusių užduočių anksčiausia pradžios data naudojama kaip suvestinės užduoties pradžios data, o susijusių užduočių vėliausia pabaigos data naudojama kaip pabaigos data. Suvestinės užduoties pavadinimą galima modifikuoti, tačiau pastangų, datų ir trukmės planavimo ypatybių modifikuoti negalima. Jei panaikinate suvestinės užduotį, taip pat panaikinate visas su ja susijusias užduotis. 

**Lapo mazgo užduotys** Lapo mazgo užduotis yra smulkiausias projekto darbo paketas. Lapo mazgas rodo prognozuojamas pastangas, planuojamą išteklių skaičių, planuojamą pradžios datą bei pabaigos datą ir trukmę. 

Norėdami įgalinti darbo hierarchijos arba projekto skaidymo kūrimą, galite atlikti toliau nurodytas hierarchijos operacijas. 

**Nauja užduotis** Visos naujai sukurtos užduotys automatiškai įtraukiamos į šakninį mazgą, o užduočiai automatiškai priskiriamas WBS numeris. WBS numeris atitinka užduoties hierarchijos lygį. Užduotims, esančioms projekto šakninės užduoties pirmajame lygyje, naudojama 1, 2, 3 ir t. t. numeravimo schema. Užduotims, esančioms žemiau pirmojo lygio, naudojama 1.1, 1.2, 1.3 ir t. t. numeravimo schema. Kiekviename lygyje, įtraukiamame į ankstesnį lygį, naudojama nauja taškinė skaitmenų seka. 

Šiuo metu negalite tinkinti WBS numeravimo. 

**Užduoties įtrauka** Kai įtraukiate užduotį, ji tampa ankstesnės užduoties antrine užduotimi. Naujos antrinės užduoties WBS numeris automatiškai perskaičiuojamas pagal naujo pirminio objekto WBS numerį. Pirminė užduotis dabar yra suvestinės arba konteinerio užduotis, todėl tampa su ja susijusių užduočių apibendrinimu. 

> [!NOTE] 
> Kai į užduotį, kuri prieš įtraukos operaciją buvo lapo mazgas, įtraukiate užduotis, naujai sukurta suvestinės užduotis netenka joje pateiktų datų, pastangų ir išteklių skaičiaus. Dabar joje naudojama naujų susijusių užduočių reikšmių suvestinė. 

**Atvirkštinė užduoties įtrauka** Kai atliksite atvirkštinę užduoties įtrauką, ji nebebus su pirminiu objektu susijusia užduotimi. Šios užduoties WBS skaičius automatiškai perskaičiuojamas, kad atspindėtų naują užduoties hierarchijos lygį. Užduoties ankstesnės pirminės užduoties pastangos, savikaina ir datos perskaičiuojamos taip, kad į juos nebūtų įtraukta minėta užduotis. 

**Perkelti aukštyn arba perkelti žemyn** Spustelėję **Perkelti aukštyn** ir **Perkelti žemyn**, pakeičiate užduoties padėtį jos pirminio objekto hierarchijoje. Užduoties padėtis nedaro įtakos užduoties pastangoms, savikainai, datoms ar trukmei. Tačiau užduoties WBS skaičius automatiškai perskaičiuojamas, kad atspindėtų naują užduoties padėtį.

### <a name="schedule-estimation"></a>Grafiko įvertinimas

Grafiko įvertinimas paprastai yra antras veiksmas kuriant WBS. Sukūrus užduotis, rekomenduojama atlikti grafiko įvertinimą. „Finance“ puslapyje **Darbo paskirstymo struktūra** yra du skyriai. Viršutinė sritis skirta grafikui įvertinti, o apatinėje srityje yra skirtukas **Įvertinta savikaina ir pajamos**, kuriame galite įvertinti savikainą. 
**Užduoties priklausomybės** WBS galite sukurti ankstesnius ryšius tarp užduočių. Užduočiai priskyrus ankstesnes užduotis, tą užduotį bus galima pradėti tik atlikus visas ankstesnes užduotis. Suplanuota užduoties pradžios data automatiškai nustatoma pagal vėliausią visų ankstesnių užduočių datą. 

**Užduočių planavimas** Lapo mazgo užduočių planavimą nustato toliau pateikiami veiksniai.

-   Ankstesnės užduotys
-   Pastangos
-   Išteklių skaičius
-   pradžios ir pabaigos datos;

Lapo mazgo užduoties, neturinčios ankstesnių užduočių, pradžios data automatiškai nustatoma pagal projekto grafiko pradžios datą. Lapo mazgo užduoties trukmė visada apskaičiuojama kaip darbo dienų skaičius nuo jos pradžios datos iki pabaigos datos. 

*<strong><em>Planavimo taisyklės</em></strong>* Įjungus automatinio planavimo pagalbą, toliau pateikiamos taisyklės taikomos planuojant lapo mazgo užduočių užduotis.

-   Pagal projekto planavimo kalendorių, užduoties pradžios ir pabaigos datos turi būti darbo dienos.
-   Užduoties, kuri turi ankstesnių užduočių, pradžios data automatiškai nustatoma pagal vėliausią ankstesnių užduočių atlikimo pabaigos datą.
-   Užduoties pastangos automatiškai apskaičiuojamos toliau nurodytu būdu.

Darbuotojų skaičius × Trukmė × Valandų skaičius per įprastą darbo dieną projekto kalendoriuje. 

Kai kuriais atvejais galite norėti nukrypti nuo šių taisyklių. Galite išjungti automatinį planavimą, kad „Finance“ nebūtų automatiškai nustatomos arba taisomos bet kokios lapo mazgo užduočių ypatybės. Įvedant užduoties, dėl kurios pažeidžiamos bet kokios planavimo taisyklės, informaciją, rodoma užduoties planavimo klaidos piktograma. Jei nenorite, kad būtų rodomos planavimo klaidos, išjunkite šią funkciją, spustelėję **Planavimo klaidos rodomos**. 

> [!NOTE] 
> Suvestinės arba konteinerio užduoties reikšmės ir toliau apskaičiuojamos kaip susijusių užduočių reikšmių suma, neatsižvelgiant į tai, ar automatinio planavimo pagalba įjungta, ar ne. 

**Planavimo klaidų taisymas** Kai automatinio planavimo pagalba įjungta, tikėtina, kad planavimo klaidų nebus. Tačiau, jei išjungsite automatinio planavimo pagalbą, o paskui vėl įjungsite, WBS gali būti rodomos planavimo klaidų piktogramos. 

**Planavimo klaidų taisymas konkrečioje užduotyje** Dukart spustelėjus tam tikros užduoties planavimo klaidos piktogramą, dialogo lange rodomos visos tos užduoties planavimo klaidos. Galite spręsti, kurias užduoties planavimo klaidas taisyti. 

**Visų planavimo klaidų taisymas** Jei norite, kad „Finance“ taisytų visas planavimo klaidas WBS, veiksmų srityje spustelėkite **Taisyti visus planavimo neatitikimus**. 

> [!NOTE] 
> Ši funkcija gali sukelti reikšmingų WBS keitimų. Klaidos taisomos toliau pateikiama tvarka.

1.  Įvertintos visų užduočių pastangos modifikuojamos taip, kad jos būtų lygios pajėgumui, apibrėžtam projekto kalendoriuje.
2.  Kiekvienos užduoties pradžios data modifikuojama taip, kad užduotis būtų paleidžiama atlikus visas ankstesnes užduotis.
3.  Kiekvienos užduoties pradžios data modifikuojama, norint pašalinti tarpus tarp ankstesnių užduočių pradžios datų.

### <a name="cost-estimation"></a>Kainos vertinimas

Kaip buvo minėta anksčiau šiame dokumente, galite įvesti kiekvieno lapo mazgo užduoties savikainos įvertinimą, naudodami skirtuką **Įvertinta savikaina ir pajamos**, esantį puslapio **Darbo paskirstymo struktūra** apatinėje srityje. 

> [!NOTE] 
> Negalima modifikuoti suvestinės arba konteinerio užduoties savikainos įvertinimo. Suvestinės užduoties savikainos įvertinimas prilygsta lapo mazgo užduočių savikainos įvertinimo sumai. Įvertinta bendra kiekvienos užduoties savikaina skaičiuojama kaip toliau pateikiamų operacijų tipų įvertintų savikainos sumų suma.

-   Darbas
-   Elementas arba medžiaga
-   Išlaidos

Operacijos tipas **Mokestis** naudojamas mokesčiais pagrįstoms pajamoms įvertinti. Šis operacijos tipas neturi savikainos komponento ir todėl į jį neatsižvelgiama įvertinant savikainą. 

Operacijos tipas **Klientas** naudojamas sutartyje nustatytai pardavimo vertei įrašyti naudojant fiksuotos vertės projekto tipą. Į šį operacijos tipą taip pat neatsižvelgiama įvertinant savikainą. 

Įvertinę kiekvienos užduoties darbo, medžiagos ir išlaidų savikainą, įvertintai savikainai turite priskirti projekto kategoriją. 

**Darbo savikainos įvertinimas** Kiekvienai lapo mazgo užduočiai priskiriate darbo pastangų valandas ir numatytąją kategoriją. Todėl nustačius užduoties grafiką, šios užduoties darbo savikainos įvertinimas automatiškai įtraukiamas į numatytąją darbo kategoriją. Šis savikainos įvertinimas rodomas skirtuke **Įvertinta savikaina ir pajamos** tos užduoties tinklelyje **Eilutės informacija**. Jei reikia daugiau darbo savikainos įvertinimų, galite įtraukti juos šiame skirtuke. Jei padidinsite arba sumažinsite darbo savikainos įvertinimo valandas, užduoties grafikas automatiškai perskaičiuojamas. 

**Išlaidų ir medžiagų savikainos įvertinimas** Skirtuke **Įvertinta savikaina ir pajamos** taip pat galite įvertinti užduoties išlaidų ir medžiagų savikainą, jei reikia įvertinti. 

Kiekvienos darbo ar išlaidų įvertinimo eilutės savikaina ir pardavimo kaina priklauso nuo sąrankos, apibrėžtos kiekvienai kategorijai kainodaros lentelėse, esančiose **Projektų valdymas ir apskaita** &gt; **Sąranka** &gt; **Kainodara**. Elementų savikaina ir pardavimo kaina pagal numatytuosius parametrus įtraukiamos iš elementų arba prekybos sutarčių sąrašo puslapyje **Išleisti produktai**, esančiame Produkto informacijos valdymas.

## <a name="tracking-progress-on-the-wbs"></a>Darbo eigos sekimas WBS
Kai kuriose srityse projekto eiga stebima WBS labai detaliai, o kitose eiga stebima aukštesniu WBS lygiu. Šiame skyriuje aprašoma, kaip galite naudoti WBS sekimą projekto reikalavimams sekti. 

„Finance“ yra trys rodiniai, skirti projekto WBS: planavimo rodinys, pastangų sekimo rodinys ir savikainos sekimo rodinys.

### <a name="planning-view"></a>Planavimo rodinys

Planavimo rodinyje rodomas suplanuotas arba pradinis grafiko ir savikainos informacijos įvertinimas. Nors funkcijų, skirtų projekto WBS versijai ir pagrindui sekti, nėra, šios rodinio reikšmės yra skirtos vaizduoti pagrindinę versiją. Šios temos grafiko įvertinimo ir savikainos įvertinimo skyriuose aprašomas šis rodinys ir jo naudojimas kuriant WBS.

### <a name="effort-tracking-view"></a>Pastangų sekimo rodinys

Rodinyje Pastangų sekimas rodomas WBS užduočių eigos sekimas. Jis palygina sukauptas faktines užduoties pastangų valandas ir suplanuotas pastangų valandas. Toliau pateikiamose formulėse pateikiamos pastangų sekimo rodinio reikšmės.

-   Eiga procentais = faktinės pastangos iki šios datos ÷ planuojamų užduoties pastangų
-   Likusios pastangos (dar vadinamos Įvertinimu iki pabaigos \[ETC\]) = planuojamos pastangos – faktinės pastangos iki šios datos
-   Įvertinimas pabaigoje (EAC) = likusios pastangos – faktinės pastangos iki šios datos
-   Numatomos pastangos nuokrypis = planuojamos pastangos – EAC

Pastangų sekimo rodinyje rodoma šios užduoties pastangų nuokrypio prognozė, atsižvelgiant į tai, ar EAC yra didesnis ar mažesnis nei planuotos pastangos.

-   Jei EAC yra didesnis nei planuojamos pastangos, prognozuojama, kad užduotis užtruks ilgiau, nei buvo planuota iš pradžių, ir atsiliekama nuo grafiko.
-   Jei EAC yra mažesnis nei planuojamos pastangos, prognozuojama, kad užduotis užtruks mažiau laiko, nei buvo planuota iš pradžių, ir kad ji įgyvendinama greičiau, nei nurodyta grafike.

**Projektų vadovo nauja pastangų prognozė** Kartais projektų vadovas arba kitas asmuo, sekantys projekto eigą, turės peržiūrėti pradinius užduoties įvertinimus. Dėl įvairių priežasčių užduotis gali būti atliekama greičiau arba lėčiau nei iš pradžių tikėtasi. Pavyzdžiui, aprėptis buvo sumažinta arba darbuotojai turi mažiau patirties nei planuota iš pradžių. Prognozės yra projekto vadovo įvertinimų suvokimas, atsižvelgiant į dabartinę projekto būseną. Apskritai neturėtumėte keisti pradinių skaičių, nes projekto pradinis planas yra publikuotas projekto grafiko ir savikainos įvertinimų, su kuriais sutiko visos projekto suinteresuotosios šalys, dokumentas. 

Yra du būdai, kaip projektų vadovai gali modifikuoti užduočių pastangas.

-   Modifikuokite likusias pastangas, kurios automatiškai nustatomos siekiant atnaujinti užduoties faktines likusias pastangas.
-   Modifikuokite eigą procentais, kuri automatiškai nustatoma siekiant atnaujinti patikslintą užduoties eigą.

Taikant šiuos metodus, perskaičiuojamos užduoties ETC, EAC bei eiga procentais ir prognozuojamas užduoties pastangų nuokrypis. Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir atnaujinamas prognozuojamas pastangų nuokrypis. 

**Modifikuotos suvestinės užduočių pastangos** Galite modifikuoti suvestinės arba konteinerio užduočių pastangas. Neatsižvelgiant į tai, ar modifikuojate šias reikšmes pagal suvestinių užduočių likusias pastangas ar eigą procentais, skaičiavimas automatiškai atliekamas toliau pateikiama tvarka.

1.  Užduoties EAC, ETC bei eiga procentais apskaičiuojami.
2.  Naujas EAC paskiriamas į antrines užduotis pagal tą pačią proporciją kaip ir pradinis EAC dydis.
3.  Kiekvienoje lapo mazgo užduotyje apskaičiuojamas naujas EAC.
4.  Visų paveiktų antrinių užduočių likusios pastangos ir eiga procentais perskaičiuojamos pagal naują EAC reikšmę. Taip pat perskaičiuojamas užduočių pastangų nuokrypis.
5.  Suvestinių užduočių EAC taip pat perskaičiuojamos pagal lapo mazgus.

Norėdami nustatyti lygį, kuriuo norite sekti ir prižiūrėti savo WBS, spustelėkite **Išplėsti iki lygio** pastangų sekimo rodinyje. Kaskart atidarant WBS, ji pastangų sekimo rodinyje automatiškai išplečiama iki nurodyto lygio.

### <a name="cost-tracking-view"></a>Savikainos sekimo rodinys

Savikainos sekimo rodinyje rodomas užduoties sąnaudų sekimas. Šiame rodinyje faktinė savikaina, kuri buvo išleista užduočiai iki šiol, palyginama su suplanuota užduoties savikaina. Toliau pateikiamose formulėse pateikiamos savikainos sekimo rodinio reikšmės.

-   Sąnaudų procentinė dalis = faktinė savikaina iki šios datos ÷ planuojama užduoties savikaina
-   Savikaina iki pabaigos (CTC) = planuojama savikaina – faktinė savikaina iki šios datos
-   Įvertinimas pabaigoje (EAC) = CTC + faktinė savikaina iki šios datos
-   Prognozuojamas savikainos nuokrypis = planuojama savikaina – EAC

Savikainos sekimo rodinyje rodoma šios užduoties savikainos nuokrypio prognozė, atsižvelgiant į tai, ar EAC yra didesnis ar mažesnis nei planuota savikaina.

-   Jei EAC yra didesnis nei planuota savikaina, prognozuojama, kad užduočiai prireiks daugiau pinigų, nei buvo planuota iš pradžių, ir biudžetas viršijamas.
-   Jei EAC yra mažesnis nei planuota savikaina, prognozuojama, kad užduočiai prireiks mažiau pinigų, nei buvo planuota iš pradžių, ir biudžetas neviršijamas.

**Projekto vadovo nauja savikainos prognozė** Projektų vadovai turi naudoti CTC, kad peržiūrėtų pradinį užduoties savikainos įvertinimą. Projektų vadovas gali pakeisti CTC reikšmę į savikainą, būtiną užduočiai užbaigti. Jei modifikuojate CTC reikšmę, užduoties CTC, EAC ir sąnaudų procentinė dalis bei prognozuojamas užduoties savikainos nuokrypis perskaičiuojami. Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei sąnaudos procentais ir atnaujinamas prognozuojamas savikainos nuokrypis. 

> [!NOTE] 
> Kai peržiūrite WBS užduoties pastangas pastangų sekimo rodinyje, užduoties CTC, EAC, sąnaudų procentinė dalis ir prognozuojamas savikainos nuokrypis perskaičiuojami savikainos sekimo rodinyje. Tačiau savikainos peržiūrėjimas neturi įtakos pastangų sekimo rodinio reikšmėms, nes savikaina pagal operacijos tipą (darbą, medžiagą arba išlaidas) arba projekto kategoriją neperžiūrima. 

**Suvestinės užduočių savikainos prognozės peržiūra** Galite peržiūrėti suvestinės užduočių savikainą, o skaičiavimai automatiškai atliekami toliau pateikiama tvarka.

1.  EAC, CTC ir užduoties sąnaudų procentinė dalis perskaičiuojami.
2.  Naujas EAC paskiriamas į antrines užduotis pagal tą pačią proporciją kaip ir pradinis užduočių EAC.
3.  Skaičiuojamas naujas kiekvienos užduoties EAC.
4.  Atsižvelgiant į EAC reikšmę, paveiktų antrinių užduočių CTS ir sąnaudų procentinė dalis perskaičiuojami. Taip pat perskaičiuojamas užduočių savikainos nuokrypis.
5.  Visų suvestinės užduočių EAC perskaičiuojamas remiantis šiuo pakeitimu.

Norėdami nustatyti lygį, kuriuo norite sekti ir prižiūrėti savo WBS, spustelėkite **Išplėsti iki lygio** savikainos sekimo rodinyje. Kaskart atidarant WBS, ji savikainos sekimo rodinyje išplečiama iki nurodyto lygio.

### <a name="earned-value-management"></a>Uždirbtos vertės valdymas

Galite naudoti uždirbtos vertės metodą (EVM), norėdami sekti projekto eigą. Galite peržiūrėti uždirbtos vertės metriką projektų vadovo vaidmenų centre. Uždirbtos vertės diagramos komponentas rodo suplanuotos vertės ir faktinės savikainos laipsniškai laike išdėstytas vertes. Uždirbta vertė šiai dienai rodoma kaip taškas. Uždirbtos vertės laipsniškai laike išdėstyti duomenys šiuo metu nepasiekiami. 

Uždirbtos vertės laipsniško išdėstymo laike diagrama rodoma pagal savaitę arba mėnesį. Šiame skyriuje aprašomi trys EVM pagrindai: suplanuota vertė, uždirbta vertė ir faktinė savikaina. 

**Suplanuota vertė** EVM teorijoje teigiama, kad suplanuotos vertės grafikas atitinka spartą, kuria projekto komanda suplanavo uždirbti projekto vertę. 

„Finance“ pateikiant suplanuotą vertę, naudojama 0:100 uždirbimo taisyklė. Pagal šią taisyklę užduoties vertė registruojama užduotyje nuo jos pabaigos datos. Vertė neregistruojama, kol užduotis nėra 100 proc. užbaigta. 

Projektų valdyme ir apskaitoje įvedate lapo mazgų pabaigos datą ir suplanuotą savikainą. Kai suplanuotos vertės grafikas rodomas pagal savaitę, visų lapo mazgo užduočių suplanuota vertė apibendrinama pagal savaitę per visą projekto trukmę. 

**Uždirbta vertė** EVM teorijoje teigiama, kad uždirbtos vertės grafikas atitinka spartą, kuria projekto komanda faktiškai uždirba projekto vertę. 

„Finance“ pateikiant uždirbtą vertę, naudojama 0:100 uždirbimo taisyklė. Pagal šią taisyklę užduoties vertė registruojama užduotyje nuo jos pabaigos datos. Vertė neregistruojama, kol užduotis nėra 100 proc. užbaigta. 

Kai uždirbta vertė apskaičiuojama, atsižvelgiama į kiekvienos užduoties eigos procentinę dalį. Remiantis 0:100 uždirbimo taisykle, apskaičiuojant uždirbtą vertę laikotarpio pabaigoje atsižvelgiama tik į per atitinkamą laikotarpį atliktas užduotis. Projekto uždirbta reikšmė apskaičiuojama visoms užduotims, kurios buvo atliktos kuriant grafiką. 

> [!NOTE] 
> Šiuo metu WBS sekimo sistemoje nėra duomenų struktūrų, kuriose būtų saugoma retrospektyvinė kiekvienos užduoties eigos procentinė dalis. Todėl uždirbta vertė gali būti pateikiama tik nuo kubo apdorojimo laiko. Reguliariai apdorokite kubą, kad atnaujintumėte uždirbtos vertės duomenis, rodomus vaidmenų centre. 

**Faktinė savikaina** EVM teorijoje teigiama, kad faktinės savikainos grafikas atitinka spartą, kuria pinigai panaudojami projektui vykdyti. 

Projekte užregistruotos operacijos naudojamos faktinei sąnaudų eilutei pateikti. Sąnaudos yra apibendrintos pagal datą. Paskui šie duomenys naudojami faktinių sąnaudų grafikui pateikti pagal savaitę arba mėnesį uždirbtos vertės diagramoje.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Kaip naudoti planuojamos vertės, uždirbtos vertės ir faktinės savikainos sąvokas

**Grafiko nuokrypis** Planuodami sukuriate darbo prognozę laiko planavimo juostoje. Todėl suplanuota vertė yra sparta, kuria, projekto planuotojų nuomone, projekto darbas galėjo būti užbaigtas. Pradėjus vykdyti projektą, darbas užbaigiamas ir projektas uždirba vertę. Palyginę suplanuotą vertę ir uždirbtą vertę, matysite, kaip vykdomas projekto darbas. Šio palyginimo rezultatas vadinamas grafiko nuokrypiu. 

Jei suplanuota vertė per laikotarpį yra didesnė už uždirbtą vertę, su projektu susijusio darbo buvo padaryta mažiau, nei planuota. Todėl projektą vėluojama atlikti. Kadangi suplanuota vertė ir uždirbta vertė išreiškiami pinigais, projekto vėlavimo trukmei taip pat suteikiama piniginė išraiška. 

Jei suplanuota vertė per laikotarpį yra mažesnė už uždirbtą vertę, su projektu susijusio darbo buvo padaryta daugiau, nei planuota. Todėl projektas vykdomas greičiau nei nurodyta grafike. Šiam papildomam laikui taip pat suteikiama piniginė vertė.

**Savikainos nuokrypis** Kadangi įvertinant uždirbtą vertę savikaina naudojama kaip daugiklis, uždirbta vertė nurodo atlikto projekto darbo savikainą. Vykdant projektą, operacijų žurnale pateikiamas pinigų, faktiškai išleidžiamų tam projektui, įrašas. Palyginę uždirbtą vertę su faktine savikaina, pamatysite išleidžiamų pinigų sumą lyginant su uždirbama verte. Šio palyginimo rezultatas vadinamas savikainos nuokrypiu. 

Jei faktinė per laikotarpį išleista savikaina yra didesnė už uždirbtą vertę, buvo išleista daugiau pinigų nei uždirbta. Todėl projekto biudžetas viršytas. 

Jei faktinė per laikotarpį išleista savikaina yra mažesnė už uždirbtą vertę, buvo uždirbta daugiau pinigų nei išleista. Todėl projekto biudžetas neviršytas.

## <a name="wbs-templates"></a>WBS šablonai
Galite naudoti WBS šablonų funkcijas, kad sukurtumėte standartinius projektų šablonus. Jei jūsų įmonėje siūlomi projektai, kurių metu atliekama daug pasikartojančio darbo, apsvarstykite galimybę sukurti WBS šabloną. 

Galite sukurti WBS šabloną pagal esamo projekto WBS, kad žinias ir geriausią praktiką, kurias sukaupėte planuodami projektą, galima būtų pakartotinai panaudoti vykdant panašius projektus ateityje. Tačiau kartais gali būti neverta įrašyti visos WBS kaip šabloną. Todėl taip pat galite kurti šablonus pagal projekto WBS dalis.

### <a name="saving-a-projects-wbs-as-a-template"></a>Projekto WBS įrašymas šablono forma 

Sukūrę šabloną, galite importuoti jį į naujo projekto WBS šakniniame mazge arba bet kurioje užduotyje projekto WBS.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>WBS šablono importavimas į projekto WBS

Kai importuojate užduotis, šablono užduotys sutvarkomos pagal užduoties, kurioje jos importuojamos, pradžios datą. Importuojant, su šablono užduotimis susiję ankstesni ryšiai naudojami importuotų užduočių pradžios datoms apskaičiuoti. Paskirties projekto standartinis darbo kalendorius naudojamas norint apskaičiuoti importuotų užduočių pabaigos datas, kad būtų išsaugotos darbo dienos ir standartinės darbo valandos, apibrėžtos esamo projekto darbo kalendoriuje. 

Savikainos sumos ir pardavimo kainos įvertinimo eilutėse naudojamos siekiant užtikrinti, kad tam tikro projekto arba projekto sutarties kainoms būtų priskirtos galiojančios datos.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Projekto WBS ir WBS šablono skirtumai

-   WBS šablonų užduotyse nėra pradžios datų ir pabaigos datų.

Darbo ir nedarbo dienos WBS šablonuose nenustatomos.

-   WBS šablonuose visada naudojamas planavimo kalendorius, kuris nustatomas kaip numatytasis visų projektų kalendorius.

Numatytasis planavimo kalendorius naudojamas tik darbo valandomis per standartinę darbo dieną sužinoti.

-   Ankstesni ryšiai nekopijuojami į WBS šabloną.

Kadangi WBS šablonuose nėra datų, ankstesnės užduoties pabaigos data pagrįsta pradžios datos logika nereikalinga.

-   Darbo savikainos įvertinimo eilutė automatiškai sukuriama, kai užduotis sukuriama WBS šablone. Pardavimo kaina ir savikainos suma kopijuojamos iš pasirinkto darbuotojo.

Išlaidas ir elemento savikainą galima kurti rankiniu būdu, lygiai taip pat, kaip jos kuriamos projekto WBS.

-   Planavimo klaidos rodomos, kai yra nukrypimų nuo toliau pateikiamos formulės.

Pastangos = išteklių skaičius × trukmė × valandų skaičius per standartinę darbo dieną 

Galite ištaisyti visas planavimo klaidas vienu metu, spustelėdami **Taisyti visas planavimo klaidas**. 

Taip pat galite ištaisyti planavimo klaidas po vieną, spustelėdami kiekvienos užduoties įspėjimo piktogramą.



