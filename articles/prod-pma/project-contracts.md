---
title: Projekto sutartys
description: Šioje temoje pateikiami projekto sutarčių, kurias galite kurti įvairiems projektų tipams ir finansavimo šaltiniams, pavyzdžiai, taip pat sutarčių tvarkymo ir sąskaitų faktūrų išrašymo projektų klientams pavyzdžiai.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cfc5183ce28574d865389eba72cafd3528741cc
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683502"
---
# <a name="project-contracts"></a>Projekto sutartys

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiami projekto sutarčių, kurias galite kurti įvairiems projektų tipams ir finansavimo šaltiniams, pavyzdžiai, taip pat sutarčių tvarkymo ir sąskaitų faktūrų išrašymo projektų klientams pavyzdžiai.

Projekto, kurį kuriate projekto sutarčiai, tipu nustatomas būdas, naudojamas sąskaitoms faktūroms išrašyti projekto klientams. Galite keisti projekto sutartį ir susijusį projektą, tačiau negalite keisti projekto tipo. 

Naudodami projekto sutartį vienu metu galite išrašyti vieno ar kelių projektų sąskaitą faktūrą. Projekto sutartis taip pat padeda užtikrinti nuoseklią sąskaitų faktūrų išrašymo tvarką kiekvienam projekto struktūroje esančiam subprojektui. 

Kiekvienas projektas, kuriam bus išrašyta sąskaita faktūra, turi būti susietas su projekto sutartimi. Projekto sutarties parametrai taikomi visiems su ta projekto sutartimi susietiems projektams ir subprojektams. 

Projekto sutartyje gali būti nurodytas vienas ar daugiau finansavimo šaltinių. Todėl galite išskaidyti sąskaitas tarp kelių skyrėjų, nustatyti finansavimo limitus, kad finansavimo šaltiniams teikiamos sąskaitos neviršytų nustatytos sumos, ir konfigūruoti apmokestinamų išlaidų finansavimo taisykles.

## <a name="funding-for-project-contracts"></a>Projektų sutarčių finansavimas
Kai kuriose projektų sutartyse nurodyta, kad projekto išlaidų finansavimo atsakomybė atitenka kelioms šalims. Štai keli pavyzdžiai:

-   Stambus klientas, turintis keletą padalinių, prašo, kad projekto finansavimas būtų išskaidytas padaliniams.
-   Jūsų įmonė patiria bendrų didelio projekto išlaidų su išorine organizacija.
-   Kelių projektą bendrai finansuoja dvi savivaldybės.
-   Tilto statybos projektą finansuoja valstybinė institucija ir privati korporacija.

Dynamics 365 Finance galite padalyti vienos operacijos ar viso projekto atsiskaitymą keliems klientams, dotacijoms ar organizacijoms. 

Projektuose, kuriuose yra keletas finansuotojų, visos šalys, prisidedančios prie išplėstinio finansavimo projekto finansavimo, vadinamos finansavimo šaltiniais. Apibrėžus klientą, organizaciją arba dotaciją kaip finansavimo šaltinį, galima juos priskirti vienai arba keletui finansavimo taisyklių. Finansavimo taisyklėse nurodomi kriterijai, apibrėžiantys, kaip mokesčiai paskirstomi tarp įvairių projekto finansavimo šaltinių. 

Atsargose laikomos prekės, pvz., tokios, kurios atsiranda pirkimo paraiškose ir pirkimo užsakymuose, negali būti išskaidytos, todėl išlaidų suma negali būti išskaidyta tarp kelių finansavimo šaltinių paskirstymo metu. Todėl finansavimo šaltinio reikšmė lieka 0 (nulis), kol neužregistruojama atsargų problema. Užregistravus atsargų problemą, išlaidų suma paskirstoma pagal projektui taikomas kliento paskirstymo taisykles.

Čia pateikiami keli veiksmai, kuriuos atlikę lengviau paskirstysite atsiskaitymą tarp kelių finansavimo šaltinių.

-   Nurodykite, kad visose įvestose projekto operacijose naudojama tokia pati pardavimo valiuta kaip ir projekto sutartyje.
-   Nustatykite finansavimo limitus, kad finansavimo šaltiniui nebūtų išrašyta sąskaita, kurios suma viršytų sumą, nurodytą projekte.
-   Konfigūruokite kiekvieno darbuotojo, elemento, kategorijos, kategorijos grupės ir operacijų tipo (arba visų transakcijų tipų) finansavimo taisykles ir finansavimo limitus.
-   Pažymėkite pasirinktines pradžios ir pabaigos datas, kad nustatytumėte kiekvienos finansavimo taisyklės galiojimo laikotarpį.
-   Nurodykite procentinę dalį, už kurią atsako kiekvienas finansavimo šaltinis.
-   Nurodykite, kuris finansavimo šaltinis yra atsakingas už apvalinimo skirtumus, atsiradusius skaičiuojant finansavimo paskirstymą.
-   Nustatykite taisykles, kuriomis apibrėžiama, kaip projekto išlaidų sąskaitos išrašomos išoriniams klientams ir teikiamos vidinėms organizacijoms.
-   Įrašykite operacijas į atidėtą finansavimo klientą, kol bus gautas papildomas finansavimas arba kol nuspręsite dengti išlaidas organizacijos viduje.

Siekiant nustatyti, kokią mokesčių grupę sieti su operacija, projekte ieškoma mokesčių grupės priskyrimo. Jeigu projekto lygyje nebuvo atliktas mokesčių grupės priskyrimas, ieškoma projekto sutartyje.

### <a name="example-multiple-funding-sources-simple"></a>Pavyzdys: keli finansavimo šaltiniai (paprasti)

Šioje lentelėje pateikiami kelių finansavimo šaltinių finansavimo paskirstymo scenarijai. Šie scenarijai grindžiami toliau pateikiamomis prielaidomis.

-   Prioriteto parametrai įtraukiami į lėšų paskirstymą prieš taikant kitus finansavimo taisyklių kriterijus.
-   Nenurodytas datų diapazonas, apibrėžiantis finansavimo taisyklės galiojimo laikotarpį.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenarijus</strong></td>
<td><strong>Finansavimo šaltinis</strong></td>
<td><strong>Paskirstymo procentinė dalis</strong></td>
<td><strong>Paskirstymo prioritetas</strong></td>
</tr>
<tr class="even">
<td>Norite skirti išlaidas vienam finansavimo šaltiniui tol, kol jo lėšos bus išeikvotos, skirti išlaidas antram finansavimo šaltiniui tol, kol jo lėšos bus išeikvotos ir pagaliau skirti likusias išlaidas trečiam finansavimo šaltiniui.</td>
<td><ul>
<li>1-as finansavimo šaltinis</li>
<li>2-as finansavimo šaltinis</li>
<li>3-ias finansavimo šaltinis</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Norite skirti 75 procentus išlaidų vienam finansavimo šaltiniui ir 25 procentus antram finansavimo šaltiniui. Kai bus išeikvotas bet kuris šių finansavimo šaltinių, norite, kad likusios išlaidos būtų sumokėtos iš trečio finansavimo šaltinio.</td>
<td><ul>
<li>1-as finansavimo šaltinis</li>
<li>2-as finansavimo šaltinis</li>
<li>3-ias finansavimo šaltinis</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Norite skirti 75 procentus išlaidų vienam finansavimo šaltiniui ir 25 procentus antram finansavimo šaltiniui. Kai bus išeikvotas bet kuris šių finansavimo šaltinių, norite, kad likusios išlaidos būtų išskaidytos tarp trečio ir ketvirto finansavimo šaltinio.</td>
<td><ul>
<li>1-as finansavimo šaltinis</li>
<li>2-as finansavimo šaltinis</li>
<li>3-ias finansavimo šaltinis</li>
<li>4 finansavimo šaltinis</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Norite skirti pirmus 25 procentus išlaidų vienam finansavimo šaltiniui ir likusią dalį antram finansavimo šaltiniui.</td>
<td><ul>
<li>1-as finansavimo šaltinis</li>
<li>2-as finansavimo šaltinis</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Pavyzdys: keli finansavimo šaltiniai (sudėtiniai)

Turite tris finansavimo šaltinius, kuriuos norite naudoti toliau pateikiama tvarka.

1.  Vienodai naudoti 2-ą finansavimo šaltinį ir 3-ią finansavimo šaltinį tol, kol bus išeikvotas 2-as finansavimo šaltinis.
2.  Toliau naudoti 3-ią finansavimo šaltinį tol, kol jis bus išeikvotas.
3.  Išeikvojus 3-ią finansavimo šaltinį, naudoti 1-ą finansavimo šaltinį.

Norėdami pasiekti šį tikslą, turite atlikti toliau nurodytus veiksmus veiksmus.

-   Nustatykite 2-o finansavimo šaltinio ir 3-io finansavimo šaltinio atitinkamas finansavimo limito sumas.
-   Sukurkite tolesnes finansavimo taisykles.
    -   1 taisyklė (1 prioritetas): skirti 50 procentų operacijų 2-am finansavimo šaltiniui ir 50 procentų 3-iam finansavimo šaltiniui.
    -   2 taisyklė (2 prioritetas): skirti 100 procentų operacijų 3-iam finansavimo šaltiniui.
    -   3 taisyklė (3 prioritetas): skirti 100 procentų operacijų 1-am finansavimo šaltiniui.

Ši sąranka veikia, nes operacijos tikrinamos pagal taisykles ir limitus, siekiant nustatyti, ar kuri nors iš jų taikoma operacijai. Jei operacijai netaikomos jokios konkrečios taisyklės ar limitai, taikoma visų operacijų taisyklė. Visų operacijų taisyklė taikoma visoms operacijoms. 

Jei randama operacijai taikoma taisyklė, šioje taisyklėje paskirstoma procentinė dalis taikoma pirmiausiai, bet tik patikrinus, ar neviršijama nustatytų limitų. Jei pasiektas limitas, o finansavimo šaltinio lėšos išeikvotos, su šiuo finansavimo limitu susijusios taisyklės nepaisoma ir programa tikrina kitą taikomą taisyklę. 

Kai kuriais atvejais pagal taisyklę galima paskirstyti tik dalį operacijos. Taip gali nutikti, jei limito pasiekiama skiriant operaciją. Šiuo atveju tik tam tikra suma paskirstoma pagal šią taisyklę, pvz., po 50 procentų kiekvienam finansavimo šaltiniui. Tai yra 1 taisyklės atvejis, aprašytas anksčiau šiame skyriuje. Likusi dalis paskirstoma pagal kitą sekoje esančią taisyklę. 

Toliau pateikiamoje lentelėje šis scenarijus nagrinėjamas išsamiau.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Aktyvinimas</strong></td>
<td><strong>Išsami informacija</strong></td>
</tr>
<tr class="even">
<td>Finansavimo taisyklės</td>
<td><ul>
<li>1 taisyklė (1 prioritetas): visos operacijos. 2-am finansavimo šaltiniui skirti 50 % ir 3-iam finansavimo šaltiniui – 50 %.</li>
<li>2 taisyklė (2 prioritetas): visos operacijos. 3-iam finansavimo šaltiniui skirti 100 %.</li>
<li>3 taisyklė (2 prioritetas): visos operacijos. 1-am finansavimo šaltiniui skirti 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Finansavimo limitai</td>
<td><ul>
<li>1-o finansavimo šaltinio limitas yra 10 000,00</li>
<li>2-o finansavimo šaltinio limitas yra 500,00</li>
<li>3-io finansavimo šaltinio limitas yra 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>1 operacija</td>
<td><strong>Operacijos suma:</strong> 100,00<strong>Finansavimas:</strong> operacija apmokama tik pagal 1 taisyklę, nes taikoma tai, kad operacija visiškai apmokama pagal 1 taisyklę. Operacija finansuojama po lygiai 2-o finansavimo šaltinio ir 3-io finansavimo šaltinio.
<ul>
<li>2-as finansavimo šaltinis: 50,00</li>
<li>3-ias finansavimo šaltinis: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>2 operacija</td>
<td><strong>Operacijos suma:</strong> 5000,00<strong>Finansavimas:</strong> operacija apmokama pagal visas tris taisykles. <strong>1 taisyklė</strong>
<ul>
<li>2-as finansavimo šaltinis: 450,00</li>
<li>3-ias finansavimo šaltinis: 450,00</li>
</ul>
<strong>2 taisyklė</strong>
<ul>
<li>3-ias finansavimo šaltinis: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>3 taisyklė</strong>
<ul>
<li>1-as finansavimo šaltinis: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Iš viso lėšų, skirtų kiekvienam finansavimo šaltiniui</td>
<td><ul>
<li>1-as finansavimo šaltinis: 3850,00</li>
<li>2-as finansavimo šaltinis: 500,00</li>
<li>3-ias finansavimo šaltinis: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Atsiskaitymo taisyklės
Kai aptariate projekto sutartį su klientu, nustatote kaip ir kada galite išrašyti klientui sąskaitą faktūrą už darbą su projektu. Nustatę projekto sutartį ir projektą, galite nustatyti projekto sąskaitų išrašymo taisykles. Sąskaitų išrašymo taisyklės grindžiamos projekto terminais, nustatytais projekto sutartyje. Kokias atsiskaitymo taisykles galite sukurti priklauso nuo projekto sutarties ir projekto tipo sąlygų, pvz., laiko ir medžiagų arba fiksuotos kainos, kurias siejate su atsiskaitymo taisykle. Galite sukurti daugiau nei vieną projekto sutarties atsiskaitymo taisyklę. Taip pat galite priskirti atsiskaitymo taisyklę keliems projektams, susijusiems su ta pačia projekto sutartimi ir turintiems panašias atsiskaitymo sąlygas. 

Galite nustatyti toliau nurodytus atsiskaitymo taisyklių tipus.

-   **Pristatymo vienetas** – klientui išrašoma sąskaita faktūra atlikus pristatymo vienetą. Pristatymo vienetai apibrėžiami sutartyje.
-   **Vykdymo eiga** – klientui išrašoma sąskaita faktūra, kai įvykdote nurodytą procentinę dalį projekto. Galite nustatyti atsiskaitymo taisyklę, kad būtų automatiškai skaičiuojama atlikto darbo procentinė dalis, arba galite rankiniu būdu skaičiuoti atlikto darbo procentinę dalį ir klientui išrašomos sąskaitos faktūros sumą.
-   **Etapas** – klientui išrašoma sąskaita faktūra už visą projekto etapą jį pasiekus.
-   **Mokestis** – klientui išrašoma sąskaita faktūra už jūsų paslaugas ir pridedamas administravimo mokestis, kuris paprastai yra paslaugų sumos procentinė dalis.
-   **Laikas ir medžiagos** – klientui išrašoma sąskaita faktūra už laiko pardavimo vertę ir medžiagas, naudojamas projekte.

Visiems atsiskaitymo taisyklių tipams galite nurodyti užlaikymo procentinį dydį, kuris išskaičiuojamas iš kliento sąskaitų faktūrų tol, kol projektas pasieks sutarto etapo. Mokėjimo užlaikymo procentinis dydis nurodomas projekto sutartyje. Suma apskaičiuojama pagal visą kliento sąskaitoje faktūroje esančių eilučių vertę ir atimama iš jos. 

Galite priskirti apmokestinamas kategorijas atsiskaitymo taisyklėms **Laikas ir medžiagos** ir **Vykdymo eiga**. Apmokestinamosiomis kategorijomis nurodomos operacijos, kurios turi būti įtrauktos į kliento sąskaitas faktūras. 

Kai būsite pasirengę išrašyti klientui sąskaitą faktūrą, pagal atsiskaitymo taisykles bus paskaičiuota projekto sąskaitos faktūros suma ir sugeneruotas projekto sąskaitos faktūros pasiūlymas. 

Tolesniuose skyriuose pateikiami pavyzdžiai, kaip nustatyti ir tvarkyti projekto atsiskaitymo taisykles.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Pavyzdys: atsiskaitymo taisyklės, pagrįstos pristatytų vienetų skaičiumi, kūrimas

Jūsų organizacija sudaro sutartį, pagal kurią ji surengs kliento darbuotojams iš viso penkis mokymo seansus, kurių kiekvieno savikaina yra 10 000. Sąskaitą faktūrą klientui išrašote po kiekvieno mokymo seanso. 

Nustatydami sutarties atsiskaitymo taisykles, naudojate tolesnes reikšmes.

-   Pristatymo vienetas yra vienas mokymo seansas.
-   Vieneto kaina yra 10 000 už vieną mokymo seansą.
-   Bendras vienetų skaičius yra penki mokymo seansai.

Baigę vieną mokymo seansą, galite sukurti pirmo pristatyto vieneto sąskaitą faktūrą, kurios suma yra 10 000, ir išsiųsti šią sąskaitą faktūrą klientui.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Pavyzdys: atsiskaitymo taisyklės, pagrįstos nustatyta projekto įvykdymo procentine dalimi, kūrimas (skaičiuojama rankiniu būdu)

Jūsų organizacija, įmonė, konsultuojanti programinės įrangos klausimais, sudaro su klientu sutartį, pagal kurią ji sukurs dalį produkto, kurį kuria klientas. Sutariama, kad jūsų organizacija pateiks programinės įrangos kodą per šešis mėnesius. Sutariama, kad už šį darbą klientas sumokės jūsų organizacijai iš viso 100 000. Kaip nurodyta sutartyje, kuriate atsiskaitymo taisyklę išrašyti klientui sąskaitą faktūrą, pagrįstą atlikto darbo procentine dalimi.

-   Pirmo mėnesio pabaigoje susitinkate su klientu, kad nustatytumėte atlikto darbo procentinę dalį. Kartu su klientu peržiūrėję projektą, nusprendžiate, kad įvykdyta 15 proc. projekto.
-   Išrašote sąskaitą faktūrą, kurios suma yra 15 000 (15 proc. 100 000), ir išsiunčiate ją klientui.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Pavyzdys: atsiskaitymo taisyklės, pagrįstos nustatyta projekto įvykdymo procentine dalimi, kūrimas (skaičiuojama automatiškai)

Jūsų organizacija, programinės įrangos kūrimo įmonė, sutinka sukurti klientui atlyginimų apskaitos paketą už 30 000. Sutariama, kad klientas mokės jūsų organizacijai pagal atlikto darbo procentinę dalį. Numatomos projekto išlaidos yra 20 000. Projekto sutartyje nurodomos darbo kategorijos, kurias naudojate atsiskaitymo procese. Nustatote atsiskaitymo taisykles, pagal kurias automatiškai apskaičiuojamos sąskaitos faktūros sumos už atlikto kiekvienos kategorijos darbo procentinę dalį. Nustatote kiekvienos kategorijos biudžetą.

-   **Kūrimas** – išlaidos – 15 000, o pajamos – 20 000
-   **Diegimas** – išlaidos – 5000, o pajamos – 10 000

Kai pirmą kartą kuriate sąskaitą faktūrą klientui, sąskaitos faktūros suma skaičiuojama automatiškai pagal toliau pateikiamą informaciją.

-   Praėjus mėnesiui, projekto darbuotojas pateikia projekto grafiką. Darbuotojo darbo valandų savikaina yra 5000 už kūrimą ir 1000 už diegimą. Atlikta 33 proc. kūrimo darbo (5000 – faktinė savikaina / 15 000 – biudžeto išlaidos) ir 20 proc. diegimo darbo (1000 – faktinė savikaina / 5000 – biudžeto išlaidos).
-   Sąskaitos faktūros suma – 8667 apskaičiuojama automatiškai (33 proc. 20 000 + 20 proc. 10 000).
-   Išrašote sąskaitą faktūrą, kurios suma yra 8667, ir išsiunčiate ją klientui.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Pavyzdys: sutartais etapais pagrįstos atsiskaitymo taisyklės kūrimas

Jūsų organizacija, įmonė, konsultuojanti vadybos klausimais, sutaria atlikti vartojimo prekės, kurią klientas ketina pardavinėti, rinkos tyrimą. Sutariama, kad klientas naudosis jūsų paslaugomis tris mėnesius, pradedant kovą, ir sumokės jūsų organizacijai 50 000. Projektas susideda iš trijų etapų.

-   1 etapas: vartotojų duomenų rinkimas – kovo 31 d.
-   2 etapas: vartotojų duomenų analizė – balandžio 30 d.
-   3 etapas: produkto perspektyvumo pasiūlymo pateikimas – gegužės 31 d.

Sutariama, kad klientas sumokės jūsų organizacijai 10 000 už pirmą etapą, 20 000 už antrą etapą ir 20 000 už trečią etapą. 

Rengdami projekto sutartį, sutariate, kad išrašysite klientui sąskaitas faktūras pagal įvykdytus etapus. Į atsiskaitymo taisyklės sąranką įtraukiami tolesni veiksmai.

-   Projekto etapus apibrėžimas.
-   Įvykdžius kiekvieną etapą, klientui išrašomos sąskaitos faktūros sumos nustatymas.

Kovo 31 d. įvykdžius pirmą etapą, pažymite etapą kaip įvykdytą, tada kuriate sąskaitą faktūrą, kurios suma yra 10 000, ir siunčiate ją klientui. Negalite sukurti sąskaitos faktūros už etapą, kol nepažymėjote jo kaip įvykdytą.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Pavyzdys: paslaugomis ir administravimo mokesčiu pagrįstos atsiskaitymo taisyklės kūrimas

Jūsų organizacija, įmonė, konsultuojanti vadybos klausimais, sutaria atlikti rinkos tyrimą, kad įvertintų produkto, kurį kuria klientas – mažmeninė įmonė – perspektyvumą. Sutarties sąlygose nurodoma, kad suteiksite trijų savo geriausių vadybos klausimais konsultuojančių specialistų paslaugas ir jie atliks tyrimą, grindžiamą laiku ir medžiagomis. Sutariama, kad klientas mokės 100 už valandą ir papildomą 10 proc. administravimo mokestį už konsultavimo valandas, priskiriamas projektui. 

Rengdami projekto sutartį, sukurkite atsiskaitymo taisyklę pridėti 10 proc. administravimo mokestį prie konsultavimo valandų, kurios yra priskiriamos projektui. 

Kai sukursite klientui sąskaitą faktūrą, į ją bus įtrauktas 10 proc. administravimo mokestis ir konsultavimo valandų savikaina. Pavyzdžiui, jei trys konsultantai su šiuo projektu iš viso dirbo 200 valandų, sąskaita faktūra, kurios suma yra 22 000, kuriama remiantis toliau pateikiamas skaičiavimais.

-   200 valandų po 100 už valandą = 20 000
-   10 proc. administravimo mokestis = 2000
-   Bendra sąskaitos faktūros suma – 22 000

Jeigu mokesčius moka klientas, o jūs projekto sutartyje pasirinkote PVM grupę, PVM grupė automatiškai įvedama į atsiskaitymo taisyklę, susijusią su mokesčiais.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Pavyzdys: laiko ir medžiagų vertės atsiskaitymo taisyklės kūrimas

Sutariama, kad jūsų organizacija, programinės įrangos klausimais konsultuojanti įmonė, suteiks penkis techninius konsultantus, kurie ateinančius šešis mėnesius dirbs klientui programinės įrangos kūrimo projekte. Sutariama, kad klientas mokės 150 už kiekvieną konsultavimo valandą, taip pat apmokės raštinės reikmenų išlaidas. Kiekvieno mėnesio pabaigoje jūsų organizacija siunčia klientui sąskaitą faktūrą. 

Rengdami projekto sutartį, sutariate, kad išrašysite klientui sąskaitą faktūrą kiekvieną mėnesį už projekte panaudotą laiką ir medžiagas. Kuriate atsiskaitymo taisyklę, į kurią yra įtraukta tolesnė informacija.

-   Sutarties laikotarpis yra šeši mėnesiai.
-   Konsultavimo laikas skaičiuojamas pagal 150 už valandą tarifą.
-   Sąskaita faktūra už raštinės reikmenis išrašoma pagal savikainą, o bendros projekto išlaidos negali viršyti 10 000.
-   Sąskaitą faktūrą klientui kuriate kiekvieno kalendorinio mėnesio pabaigoje projekto vykdymo metu.

Per pirmą mėnesį projekto konsultantai iš viso užrašė 800 valandų. Projektui priskiriamų raštinės reikmenų išlaidų suma yra 2000. Todėl mėnesio pabaigoje kuriate sąskaitą faktūrą, kurios suma yra 122 000. Suma skaičiuojama taip: 800 valandų po 150 už valandą ir 2000 už raštinės reikmenis.





[!INCLUDE[footer-include](../includes/footer-banner.md)]