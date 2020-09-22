---
title: Projektų išteklių paskirstymas
description: Šioje temoje pateikta informacija apie projektų išteklių paskirstymą.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753632"
---
# <a name="project-resourcing"></a>Projektų išteklių paskirstymas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikta informacija apie projektų išteklių paskirstymą.

Projekto planavimo etape projektų vadovams ir išteklių vadovams gali būti sudėtinga paskirstyti išteklus. Jie turi nustatyti ir rezervuoti tinkamus išteklius, kurie bus naudojami darbo su projektu metu. Programoje „Dynamics 365 Finance” projektų išteklių paskirstymo galimybės leidžia nustatyti laikinais ištekliais laikomus vaidmenis, kuriuos galima rezervuoti konkrečiam įtraukimui arba įtraukimo daliai. Šis išteklių paskirstymo tipas leidžia projektų vadovams ir išteklių vadovams atlikti tolesnes užduotis.

- Apibrėžti reikiamas kompetencijas turintį vaidmenį, kad jis lengvai atitiktų išteklius.
- Naudoti vaidmenis, siekiant apibrėžti pradinio įtraukimo grafiką, kuris yra pagrįstas rezervuotais ištekliais.
- Pagal projektui priskirtus vaidmenis ir išteklius įvertinti išlaidas ir nustatyti pradinį biudžetą.
- Naudoti vaidmenis, siekiant įvertinti išteklių rezervavimų, reikalingų kiekvienam įtraukimui, skaičių.
- Įvertinti išteklių, reikalingų visam projekto ciklui, skaičių.
- Sukurti darbo paskirstymo struktūros (WBS) juodraštį, naudojant pradinį išteklių priskyrimą.

[![Projekto ciklas](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Vykdant projekto planavimą, planuojamus išteklius galima pakeisti darbuotojams priskirtais ištekliais. Be to, bet kuriame projekto etape projekto vadovas gali grįžti ir atnaujinti išteklių paskirstymo rezervavimus.

## <a name="set-up-project-resources"></a>Projekto išteklių nustatymas
Turite nustatyti kalendorių ir susieti jį su darbuotoju. Kalendorius naudojamas projekto ir projektui rezervuotų išteklių darbo laiko grafikui sudaryti. Atlikdami kalendoriaus sąranką, projekto vadovai išteklių optimizavimo metu gali koreguoti išteklių paskirstymą. Ištekliams gali būti taikomi apribojimai pagal kalendoriaus grafiką. Kalendorių galite nustatyti puslapyje **Kalendorius**.

Kai nustatote darbuotoją kaip projekto išteklių, galite pasirinkti iš darbuotojų, dirbančių įmonėje, kuriai nustatote išteklius. Arba galite pasirinkti darbuotojus iš kitų jūsų organizacijoje esančių įmonių. Šie darbuotojai vadinami vidinės įmonės ištekliais.

Toliau pateikiamose procedūrose paaiškinama, kaip nustatyti darbuotoją kaip jūsų įmonės projekto išteklių ir kaip nustatyti vidinės įmonės projekto išteklius.

### <a name="set-up-a-worker-as-a-project-resource"></a>Darbuotojo kaip projekto ištekliaus nustatymas

1. Puslapyje **Darbuotojai** sąraše **Darbuotojai** pasirinkite darbuotoją, kurį įtraukiate kaip projekto išteklių, ir atidarykite darbuotojo įrašą.
2. Veiksmų srityje pasirinkite **Projektas** &gt; **Sąranka** &gt; **Projekto sąranka**.
3. Pasirinkite kalendorių, tada uždarykite puslapį.

Taip pat galite nurodyti išteklių numatytuosius projektus kaip išankstinio priskyrimo tipą. Išankstinius priskyrimus galima naudoti, kai išteklių vadovas arba projektų vadovas iš anksto žino, su kuriais projektais dirbs išteklius. Išankstiniai priskyrimai taip pat gali būti grindžiami projekto rėmėjo ar kliento prašymu. Norėdami iš anksto priskirti projektą, puslapio **Projektų priskyrimas** skirtuko **Projektai** sąraše **Likę projektai** pažymėkite atitinkamą projektą.

### <a name="set-up-an-intercompany-resource"></a>Vidinės įmonės išteklių nustatymas

Kai nustatote darbuotoją kaip vidinės įmonės išteklių, turite atlikti sąranką ir nuomojančioje, ir besiskolinančioje įmonėje.

**Nuomojančioje įmonėje**

1. Programoje „Finance” patikrinkite, ar pažymėta nuomojanti įmonė, tada atlikite ankstesniame skyriuje „Darbuotojo kaip projekto ištekliaus nustatymas” pateiktą procedūrą.
2. Puslapyje **Vidinės įmonės apskaita** pasirinkite **Nauja**.
3. Lauke **Juridinio subjekto ID** pažymėkite nuomojančią įmonę. Tinkamai užpildykite likusius laukus ir pasirinkite **Įrašyti**.
4. Puslapyje **Perkėlimo kaina** pasirinkite **Nauja**.
5. Lauke **Besiskolinančio juridinio subjekto ID** pažymėkite tinkamą įmonę.
6. Jeigu norite besiskolinančiai įmonei išnuomoti tik tą išteklių, kurį sukūrėte šio skyriaus pradžioje, lauke **Ištekliai**, pasirinkite sukurto ištekliaus pavadinimą. Jeigu norite, kad besiskolinančioji įmonė galėtų pasiekti visus nuomojančios įmonės išteklius, palikite lauką **Ištekliai** tuščią.
7. Puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **Vidinė įmonė** nustatykite parinktį **Įgalinti vidinės įmonės išteklių planavimą ir grafikų sudarymą** kaip **Taip**.

**Besiskolinančioje įmonėje**

- Puslapio **Išteklių sąrašas** ieškos filtre įveskite ištekliaus, kurį sukūrėte nuomojančiai įmonei, pavadinimą, kad patikrintumėte, ar pavadinimas įtrauktas į besiskolinančios įmonės išteklių sąrašą.

## <a name="manage-resource-competencies"></a>Išteklių kompetencijų valdymas
Išteklių kompetencijos yra esminė išteklių valdymo dalis. Kompetencijas galima naudoti kaip bazinį planą, skirtą nustatyti, ar išteklius turi tinkamų įgūdžių, išsilavinimą, sertifikavimą ir darbo projektuose patirties. Turite nustatyti šią informaciją kiekvienam ištekliui ir reguliariai ją atnaujinti. Tokiu būdu, maksimizuojate galimybes, kai konkretaus ištekliaus kompetencijos atitinka reikalavimus projekto ištekliaus priskyrimo metu.

[![Įgūdžių, sertifikavimo, išsilavinimo ir darbo projektuose patirties pavyzdžiai](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

Toliau pateikiamose procedūrose paaiškinama, kaip nustatyti kai kurias išteklių kompetencijas.

Norėdami nustatyti darbuotojo kompetencijas, galite naudoti sąrašo **Darbuotojai** puslapį žmogiškųjų išteklių dalyje arba sąrašo **Ištekliai** puslapį projektų valdymo ir apskaitos dalyje. Atliekant toliau pateikiamas procedūras, naudojamas sąrašo **Darbuotojai** puslapis, esantis žmogiškųjų išteklių dalyje.

### <a name="set-up-competencies-certificates"></a>Kompetencijų nustatymas: sertifikatai

1. Sąrašo **Darbuotojai** puslapyje pažymėkite darbuotojo eilutę, kad įtrauktumėte sertifikatų informaciją.
2. Veiksmų srityje, skirtuke **Darbuotojas**, grupėje **Kompetencijos**, pasirinkite **Sertifikatai**.
3. Pasirinkite **Naujas**, tada lauke **Sertifikato tipas** pasirinkite **PMP**.
4. Lauke **Pradžios data** pasirinkite **2015-10-01**, tada pasirinkite **Įrašyti**.

### <a name="set-up-competencies-skills"></a>Kompetencijų nustatymas: įgūdžiai

1. Sąrašo **Darbuotojai** puslapyje įsitikinkite, kad darbuotojas, kurį naudojote ankstesnėje procedūroje, vis dar pažymėtas. Tada veiksmų srityje, skirtuke **Darbuotojas**, grupėje **Kompetencijos**, pasirinkite **Įgūdžiai**.
2. Pasirinkite **Naujas**.
3. Lauke **Įgūdis** pasirinkite **Projektų valdymas**.
4. Lauke **Lygis** pažymėkite **5 lygis – ekspertas**.
5. Lauke **Lygio data** pažymėkite **2014-01-14**.
6. Lauke **Patirties metai** įveskite **10**.
7. Spustelėkite **Įrašyti** ir uždarykite puslapį.

## <a name="create-a-new-project"></a>Kurti naują projektą
1. Puslapyje **Projektų valdymas** pasirinkite **Naujas projektas** ir įveskite toliau nurodytas reikšmes.

    - **Projekto tipas:** laikas ir medžiagos
    - **Projekto pavadinimas:** XYZ Upgrade Phase 2
    - **Projektų grupė:** TM\_WIP
    - **Projekto sutarties ID:** 00000002

2. Pasirinkite **Kurti projektą**.

### <a name="assign-a-resource-to-a-project"></a>Išteklių priskyrimas projektui

1. Puslapio **Darbuotojai** sąraše **Darbuotojai** pasirinkite darbuotojo, kuriam anksčiau nustatėte kompetencijas, įrašą, ir atidarykite darbuotojo įrašą.
2. Veiksmų srityje, skirtuke **Projektas**, grupėje **Sąranka**, pasirinkite **Priskirti projektus**.
3. Puslapyje **Išteklių tikrinimo projekto priskyrimai**, skirtuke **Projektai**, lauke **Įtraukti projektą į pasirinktus projektus** filtruokite projektą **XYZ Upgrade Phase 2**.
4. Srityje **Likę projektai**pasirinkite projektą, tada pasirinkite rodyklės mygtuką, kad įtrauktumėte jį į sritį **Pasirinkti projektai**.

Jeigu reikia, taip pat galite priskirti ištekliaus kategorijas. Kategorijos tipas yra arba **Išlaidos**, arba **Pajamos**. Kategorijos tipą nustato jūsų organizacija. Jeigu ištekliui nepriskirta jokių kategorijų, „Finance” ieško numatytosios kategorijos pagal išlaidų ir pajamų valandos kainą.

### <a name="set-up-project-resource-and-role-characteristics"></a>Projektų išteklių ir vaidmens ypatybių nustatymas

Projektų vadovas gali naudoti projekto išteklių paskirstymo funkcijas, kad sukurtų projektui reikiamus vaidmenis. Vaidmenys gali būti naudojami, kai rezervuojant išteklius, patvirtinti ištekliai vis dar nėra žinomi. Vaidmenys gali būti laikinai rezervuojami kaip planuojami ištekliai, kad galėtumėte toliau vykdyti projekto planavimo etapus.

[![Vaidmens pavyzdys](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarijus:** įmonė „Contoso” buvo pasamdyta užbaigti laiko ir medžiagų projektą, turintį patvirtintą projekto chartiją. Jaunesnysis projekto vadovas vis dar nustato projekto aprėptį. Išteklių vadovas dabar nustato konkrečius išteklius, kurie bus rezervuojami darbui naujame projekte. Projektas yra svarbus, todėl projekto rėmėjas paprašė nustatyti vyresniojo projekto vadovo vaidmenį kaip vieną iš vaidmenų. Išteklių vadovas turi gauti naują išteklių ir apibrėžti vaidmenį sistemoje, nes jaunesniajam projekto vadovui planuojant projektą gali prireikti ištekliaus informacijos.

Toliau pateikiamais veiksmais parodoma, kaip išteklių vadovas gali nustatyti vyresniojo projekto vadovo vaidmenį ir susieti su juo ištekliaus charakteristikas. Vėliau vaidmenį galima naudoti norint ieškoti galimų išteklių, atitinkančių reikiamas išteklių kompetencijas.

1. Puslapyje **Vaidmenų nustatymas** pasirinkite **Naujas** ir įveskite toliau nurodytas reikšmes.

    - **Vaidmens ID:** vyresnysis projekto vadovas
    - **Aprašas:** vyresnysis projekto vadovas

2. Pasirinkite **Kurti**.
3. Pasirinkite vaidmenį **Vyresnysis projekto vadovas**, tada pasirinkite **Konfigūruoti ypatybes**.
4. Lauke **Charakteristikų tipas** pažymėkite **Įgūdis**.
5. Lauke **Galimos charakteristikos** įveskite ieškomą įgūdį.
6. Lauke **Charakteristikų tipas** pažymėkite **Sertifikatas**.
7. Lauke **Galimos charakteristikos** įveskite ieškomą sertifikato tipą.

### <a name="assign-a-project-resource-to-a-project"></a>Projekto išteklių priskyrimas projektui

1. Puslapyje **Visi projektai** pasirinkite projektą **XYZ Upgrade Phase 2**.
2. Skirtuke **Projekto komanda ir planavimas** pasirinkite **įtraukti**.
3. Lauke **Vaidmuo** pasirinkite **Komandos narys**.
4. Pasirinkite **Rezervuoti iš kalendoriaus**.
5. Puslapyje **Išteklių pasiekiamumas** pasirinkite **Peržiūrėti parametrus**.
6. Puslapyje **Koreguoti rodinio parametrus** įveskite toliau nurodytas reikšmes.

    - **Datų diapazono rodinio formatas:** diena
    - **Rodyti pasiekiamumo aprašus:** taip
    - **Rodyti likusį pajėgumą:** taip

7. Išteklių sąraše pasirinkite išteklių.
8. Pasirinkite **Rezervuoti galutinai** ir **Viso pajėgumo metodas**.


### <a name="assign-a-resource-to-a-default-role"></a>Ištekliaus priskyrimas numatytajam vaidmeniui

Norint padėti projekto ar išteklių vadovams, galima toliau detalizuoti projektui rezervuojamus išteklius. Numatytąjį vaidmenį galite susieti su esamais ištekliais arba su naujai gautu ištekliumi. Pavyzdžiui, kai Danielis buvo pasamdytas, jis turėjo patirtį ir įgūdžius, atitinkančius verslo analitiko vaidmenį. Išteklių vadovas priskyrė šį vaidmenį kaip numatytąjį Danieliaus vaidmenį. Todėl išteklių vadovas įtraukė Danielį į verslo analitikų, galinčių dirbti projektuose, telkinį.

Rezervuodami išteklius, projektų vadovai gali filtruoti vaidmens išteklius, galinčius dirbti projektuose. Jie gali naudoti šią informaciją kaip vieną kriterijų, kai atlieka keliais kriterijais grindžiamą sprendimų analizę išteklių panaudojimo metu. Be to, filtruodami jie gali įtraukti kitų išteklių charakteristikų, kad galėtų ieškoti išteklių, turinčių konkrečių įgūdžių, išsilavinimą ir patirtį, kurių reikia dirbant nurodytame projekte.

**Scenarijus:** pradėtas vykdyti patvirtintas projektas, o vyresniojo projekto vadovo vaidmuo buvo rezervuotas kaip planuotas išteklius projekto planavimo etape. Dabar išteklių vadovas gavo išteklių, kuris atitinka vyresniojo projekto vadovo vaidmenį.

1. Puslapyje **Išteklių sąrašas** pasirinkite **Danielis Goldschmidtas**.
2. Puslapyje **Ištekliaus vaidmuo** pasirinkite **Naujas** ir įveskite toliau nurodytas reikšmes.

    - **Įsigaliojimo data:** įveskite šiandienos datą.
    - **Galiojimo pabaigos data:** įveskite **Niekada**.
    - **Vaidmuo:** įveskite **vyresnysis projekto vadovas**.

3. Spustelėkite **Įrašyti** ir uždarykite puslapį.
4. Skirtuke **Kompetencijos** įtraukite įgūdį **ProjectMgmt** ir sertifikatą **PMP**.

## <a name="set-up-role-based-pricing"></a>Vaidmenimis grindžiamų kainų nustatymas
Visos išlaidos, pardavimai ir perkėlimų kainos gali būti nustatytos vaidmenims.

1. Puslapyje **Pardavimo kaina (valanda)** pasirinkite **Nauja** ir įveskite įsigaliojimo datą.
2. Stulpelyje **Vaidmuo** pasirinkite vaidmenį.
3. Stulpelyje **Kainodara** įveskite pasirinkto ištekliaus vaidmens kainą.

## <a name="form-a-project-team"></a>Formuokite projekto komandą
Norėdamas naudoti vaidmenis, kurie buvo anksčiau nustatyti projekte, projekto vadovas turi susieti šiuos vaidmenis su projektu. Projektui galima priskirti kelis vaidmenis. Siekiant išvengti painiavos, šie vaidmenys rezervavimo metu pažymimi automatiškai. Pavyzdžiui, jei projekto vadovui reikia trijų programinės įrangos inžinierių, automatiškai generuojami trys programinės įrangos inžinierių vaidmenys, turintys žymas **1-as programinės įrangos inžinierius**, **2-as programinės įrangos inžinierius** ir **3-ias programinės įrangos inžinierius**. Jei vaidmens charakteristikos anksčiau buvo nustatytos, ieškant išteklių jos taikomos kaip filtras. Jeigu reikia, galima įtraukti papildomų charakteristikų, siekiant dar labiau patikslinti iešką.

Taip pat galima tinkinti rodinio parametrus, siekiant suteikti geresnį išteklių pasiekiamumo rodinį. Galima rodyti pasiekiamumą pagal valandas, dienas, savaites, mėnesius, ketvirčius ir metus. Taip pat galima rodyti pasiekiamą ir likusį išteklių pajėgumą. Ši parinktis naudinga valdant laiką, kai įvertinate galimą veiklos arba išteklių pasiekiamumo laiką.

Projekto vadovas gali puslapyje pasirinkti vaidmenį, tada, jeigu yra pasiekiamas reikalavimus atitinkantis išteklius, pasirinkti rezervuoti išteklių, kad jis atliktų šį vaidmenį. Atkreipkite dėmesį, kad šiame planavimo etape išteklių rezervuoti nereikia. Kai sukursite WBS, galėsite keisti projekto vaidmenis darbuotojams priskirtais ištekliais. Jei vaidmenys keičiami darbuotojams priskirtais ištekliais WBS, išteklių sąranka automatiškai atnaujina projekto komandos sąrašą ir grafiką.

[![Projekto komandos sąrašas, kuriame išvardyti ir vaidmenys, ir faktiniai ištekliai](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projekto vadovas turi įvairių projekto ištekliaus rezervavimo parinkčių, pvz., **Pajėgumo likučio metodas**, **Viso pajėgumo metodas**, **Pajėgumo procentinės dalies rezervavimo metodas** ir **Nurodytos valandos**. Šios rezervavimo parinktys gali būti atšauktos bet kuriuo metu, jei pasikeičia išteklių priskyrimai. Palaikomi du rezervavimo tipai.

- **Rezervuoti galutinai** – rezervuotas išteklius buvo patvirtintas dirbti įtraukime nustatytą laiko tarpą.
- **Preliminarus rezervavimas** – rezervuotas išteklius buvo preliminariai paskirtas dirbti įtraukime nustatytą laiko tarpą.

Tolesne procedūra paaiškinama, kaip sukurti projekto komandą.

### <a name="create-a-project-team"></a>Kurti projekto komandą

1. Sąrašo **Visi projektai** puslapyje pasirinkite projektą, tada pasirinkite **Redaguoti**.
2. Skirtuko **Projekto komanda ir planavimas** lauke **Grafiko pabaigos data** įveskite grafiko pradžios datą plius vieną mėnesį. Pavyzdžiui, jei grafiko pradžios data yra 2017 m. birželio 24 d. (2017-06-24), įveskite **2017-07-24**.
3. Pasirinkite **Įtraukti**.
4. Srityje **Įtraukti vaidmenis į projektą**, lauke **Vaidmuo** pasirinkite **Vyresnysis projektų vadovas**.
5. Pasirinkite **Reikiamos kompetencijos**.
6. Puslapyje **Pasirinkite charakteristikas** charakteristikos, kurias anksčiau nustatėte vyresniojo projektų vadovo vaidmeniui, pasirenkamos pagal numatytuosius nustatymus. Pasirinkite **Gerai**.
7. Puslapyje **Įtraukti vaidmenis į projektą**, lauke **Išteklių skaičius** įveskite **1**.
8. Lauke **Ištekliai**, peržvalgos rodinyje parodomi visi ištekliai, turintys reikiamas kompetencijas. Pasirinkite **Danielis Goldschmidtas**, tada pasirinkite **Kurti**.
9. Puslapyje **Projektas** pasirinkite **Įtraukti**.
10. Srityje **Įtraukti vaidmenis į projektą**, lauke **Vaidmuo** pasirinkite **Komandos narys**. Lauke **Išteklių skaičius** įveskite **5**.
11. Pasirinkite **Kurti**.
12. Puslapyje **Projektai** pasirinkite **Naudoti išteklių**.

## <a name="resource-capacity-synchronization"></a>Išteklių pajėgumo sinchronizavimas
Išteklių sinchronizavimo procesai padeda užtikrinti, kad kalendoriaus ir pagrindinio kalendoriaus informacija naudojama planuojant projekto išteklius. Jei pakeičiamas kalendorius, procesai atlieka reikiamus projekto išteklių planavimo atnaujinimus. Procesai taip pat padeda gerinti efektyvumą, nes kalendoriaus išteklių informacija sinchronizuojama iš anksto. Todėl išteklių planavimo informacija atnaujinama greičiau. Rekomenduojame planuoti procesus kaip paketą, o ne po vieną. Priešingu atveju kyla pavojus, kad kas nors pamirš įtraukti paskutinį kartą sinchronizuotos informacijos datas. Jei paskutinį kartą nurodytos datos nebus naudojamos, sinchronizuojant datas gali atsirasti tarpų.

![Kalendoriaus sinchronizavimas](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Išteklių pajėgumų sumavimų sinchronizavimas

Sinchronizavimo procesas skirtas visai išteklių kalendoriaus informacijai sinchronizuoti. Į šią informacija įtraukta pagrindinio kalendoriaus informacija apie visus projekto išteklių kalendoriaus pajėgumo lentelės pakeitimus. Jei į projektą įtraukiami nauji ištekliai, sinchronizavimas padeda užtikrinti, kad atnaujinta kalendoriaus informacija yra pasiekiama. Šis sinchronizavimas gali būti atliktas bet kuriuo metu.

Rekomenduojame naudoti paketą. Šios parinktys yra pasiekiamos pajėgumų rezervavimų sinchronizavimo metu.

1. Pasirinkite **Projektų valdymas ir apskaita** &gt; **Periodinis** &gt; **Pajėgumų sinchronizavimas** &gt; **Išteklių pajėgumų sumavimų sinchronizavimas**.
2. Nustatykite parinktis toliau pateiktoje lentelėje.

    | Parinktis      | Aprašo |
    |-------------|-------------|
    | Laikotarpio kodas | Arba pasirinkite didžiosios knygos datų intervalo kodą, kad nustatytumėte išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios ir pabaigos datas. |
    | Pradžios data  | Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios datą. |
    | Pabaigos data    | Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pabaigos datą. |

[![Sinchronizavimo procesas](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Vaidmenų nustatymas WBS šablonuose
Projektų vadovai gali nustatyti WBS šablonus, kuriuos gali taikyti kurdami naujų projektų WBS. Kurdami šabloną projektų vadovai gali įtraukti vaidmenis. Naudokite toliau pateikiamą procedūrą, kad priskirtumėte vaidmeniui WBS šabloną.

1. Pasirinkite **Projektų valdymas ir apskaita** &gt; **Sąranka** &gt; **Projektai** &gt; **Darbo paskirstymo struktūros šablonai**.
2. Pasirinkite **Išsami informacija** pasirinktam WBS šablonui.
3. Sąraše pažymėkite užduotį, tada lauke **Vaidmuo** pasirinkite vaidmenį, kurį priskirsite užduočiai.

### <a name="work-with-a-wbs"></a>Darbas su WBS

Galite kurti naują WBS arba kopijuoti WBS iš esamo WBS šablono. Projekto vadovas gali lengvai tvarkyti išteklius, priskirdamas vaidmenis naujoms užduotims WBS. Vaidmenis galima keisti arba gavus išteklių, arba nustačius patvirtintą išteklių, kuris atliks užduotį. Šis lankstumas leidžia projektų vadovams atlikti toliau nurodytas užduotis užduotis.

- Nustatykite išteklių, reikalingų WBS darbo paketams, skaičių.
- Įvertinti projekto išlaidas.
- Nustatyti preliminarų biudžetą.
- Pagal vaidmenis ir išteklius įvertinti veiklos trukmę.
- Kurti projektų valdymo planus remiantis turima projekto informacija.

Į WBS buvo įtrauktos papildomos parinktys, skirtos geriau išnaudoti išteklių paskirstymo funkcijas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parinktis</th>
<th>Aprašo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Išteklių priskyrimai</td>
<td>Priskirtų išteklių, datų, valandų skaičiaus ir rezervavimo tipo, skirtų WBS užduotims, peržiūra.</td>
</tr>
<tr class="even">
<td>Automatinis komandos generavimas</td>
<td>Automatinis suplanuotų išteklių įtraukimas, naudojant su užduotimi susietus vaidmenis. Programa „Finance” automatiškai pasiūlo suplanuotus išteklius, naudodama vaidmenimis grindžiamą kelių kriterijų sprendimų analizę. Kai bus nustatyti WBS esančių užduočių vaidmenys ir pastangos (valandos) ir išleista struktūra, pasirinkite <strong>Automatinis komandos generavimas</strong>. Reikiamas suplanuotų išteklių skaičius įtraukiamas į WBS ir skirtuką <strong>Projekto ir komandos planavimas</strong>.</td>
</tr>
<tr class="odd">
<td>Ištekliai (išplečiamasis sąrašas)</td>
<td>Puslapyje <strong>Išteklių priskyrimo paleidimas</strong> galite pasirinkti išteklius ir, remdamiesi nustatyta trukme, priskirti juos prie galutinai rezervuojamų ir preliminariai rezervuojamų. Galite koreguoti rodinio parametrus, kad peržiūrėtumėte ir nustatytumėte išteklių veiklos trukmę. Naudodami toliau pateikiamas parinktis galite pasirinkti ir priskirti išteklius darbo paketo lygyje.
<ul>
<li><strong>Priimti</strong> – patvirtinti užduočiai priskirto ištekliaus pakeitimus.</li>
<li><strong>Atšaukti</strong> – atšaukti užduočiai priskirto ištekliaus pakeitimus.</li>
<li><strong>Priskirti automatiškai</strong> – pasiekiamas darbuotojams priskirtas išteklius, turintis atitinkantį vaidmenį, automatiškai pasirenkamas ir priskiriamas pasirinktai užduočiai.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Puslapyje **Visi projektai** pasirinkite projektą **XYZ Upgrade Phase 2**.
2. Pasirinkite **Planuoti** &gt; **Veiklos** &gt; **Darbo paskirstymo struktūra**.
3. Pasirinkite **Naujas**, kad įtrauktumėte toliau nurodytas veiklas į WBS.

    - Inicijavimas
    - Planavimas
    - Vykdoma
    - Stebėjimas ir valdymas
    - Uždaryti objektą

4. Nustatykite datas ir pastangas (valandas), kaip pavaizduota tolesnėje iliustracijoje.

    [![Datų ir pastangų nustatymas](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Pasirinkite užduoties eilutę **Inicijavimas**, tada lauke **Vaidmuo** pasirinkite **Vyresnysis projekto vadovas**.
6. Pasirinkite **Publikuoti**.
7. Toje pačioje eilutėje, lauke **Ištekliai** pasirinkite **Danielis Goldschmidtas**, tada pasirinkite **Priimti**.
8. Pasirinkite užduoties eilutę **Planavimas**, tada lauke **Vaidmuo** pasirinkite **Verslo analitikas**.
9. Pasirinkite **Publikuoti**, tada pasirinkite**Automatiškai generuoti komandą**.
10. Pasirodžiusiame pranešimo langelyje pasirinkite **Taip**.
11. Lauke **Ištekliai** patikrinkite, ar reikšmė yra **1-as verslo analitikas**.
12. Atidarykite ištekliaus **1-as verslo analitikas** peržvalgą ir pasirinkite **Išteklių priskyrimo paleidimas**. Tada pasirinkite užduočiai priskiriamą darbuotoją.
13. Pasirinkite **Preliminariai priskirti** &gt; **Viso pajėgumo metodas**.

    > [!NOTE] 
    > Negaunate įspėjimo, kad nurodytas išteklius dabar yra 2-as, nes išteklių skaičius lieka 1.

14. Puslapyje **Darbo paskirstymo struktūra** patikrinkite ištekliaus priskyrimą WBS, tada pasirinkite **Įrašyti**.

## <a name="resource-fulfillment-for-planned-resources"></a>Suplanuotų išteklių panaudojimas
Projekto vadovas gali planuoti reikiamus projekto išteklių vaidmenis. Išteklių vadovas matys šiuos suplanuotus išteklius kaip užklausas puslapyje **Išteklių panaudojimas** ir galės priskirti faktinius išteklius.

1. Puslapyje **Visi projektai** pasirinkite projektą **XYZ Upgrade Phase 2**.
2. Pasirinkite **Projektas**, tada pasirinkite **Redaguoti**.
3. Skirtuke **Projekto komanda ir planavimas** pasirinkite **įtraukti**.
4. Dialogo lange **Įtraukti vaidmenis** pasirinkite vaidmenį **Programinės įrangos kūrėjas**.
5. Spustelėkite **Kurti** ir uždarykite projekto puslapį.
6. Puslapyje **Išteklių panaudojimas** pasirinkite **1-as programinės įrangos kūrėjas** projektui **XYZ Upgrade project Phase 2**.
7. Pasirinkite darbuotoją, tada pasirinkite **Priskirti**.
8. Patikrinkite, ar eilutė **1-as programinės įrangos kūrėjas** buvo pašalinta projektui **XYZ Upgrade project Phase 2**.
9. Skirtuke **Projekto komanda ir planavimas**, skirtame projektui **XYZ Upgrade Phase 2**, patikrinkite, ar darbuotojas, kurį pasirinkote atlikdami ankstesnį veiksmą, buvo įtrauktas kaip **Programinės įrangos kūrėjas**.

## <a name="requests-for-project-resources"></a>Projektų išteklių prašymai
Projektų išteklių planavimo funkcijos leidžia išteklių vadovams tik paskirstyti darbuotojams įtraukimuose ar projektuose priskirtus išteklius. Norėdami įgalinti šias funkcijas, atlikite toliau pateikiamas užduotis arba patikrinkite, ar jos buvo atliktos.

- Nustatykite numerių sekas.
- Nustatykite projektų valdymo ir apskaitos darbo eigas.
- Įgalinkite išteklių užklausos darbo eigas.

Jeigu reikia, atlikę ankstesnes užduotis, galite atlikti toliau pateikiamas užduotis.

- Sukurkite ištekliaus užklausą iš preliminariai rezervuoto darbuotojui priskirto ištekliaus.
- Stebėkite išteklių užklausas.
- Vykdykite išteklių užklausas.
- Prašykite darbuotojui priskirto ištekliaus iš WBS.
- Rezervuokite išteklius projektui, neturėdami darbuotojui priskirto ištekliaus užklausos.

## <a name="monitor-project-teams"></a>Stebėkite projektų komandas
1. Puslapyje **Visi projektai** pasirinkite projekto **XYZ Upgrade Phase 2** saitą **Projekto ID**.
2. „FastTab” skirtuke **Projekto komanda ir planavimas** patikrinkite, ar išvardyti projekto ištekliai yra tinkami.
