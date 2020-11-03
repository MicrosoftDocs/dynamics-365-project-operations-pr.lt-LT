---
title: Kas nauja arba pakeista programos „Project Service Automation“ 3 versijoje
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 3 versijoje.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0c198a0fd293008b73422f3f60ea023f918e0ddc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080798"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Kas nauja arba pakeista programos „Project Service Automation“ 3 versijoje
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Šioje temoje pateikiama informacijos apie programos „Project Service Automation“ (PSA) vartotojo sąsajos (UI), funkcijų ir terminologijos pakeitimus, palyginant 1 arba 2 versiją su 3 versija.

## <a name="project-scheduling"></a>Projektų planavimas
Projekto grafikas, kuris ankstesnėse versijose buvo vadinamas darbo paskirstymo struktūra (WBS), buvo pervadintas pasirenkant pavadinimą Grafikas ir pasiekiamas spustelint skirtuką **Grafikas**. 

![Projekto grafikas](media/psa-schedule-01.png)

Grafikas dabar turi naują interaktyvumo paviršių, kuris yra modernus ir prieinamas. Tačiau pagrindinis „Project Service Automation“ planavimo modulis nepasikeitė. Naudodamiesi grafiko tinklelio juostelės valdymo mygtukais galite pasiekti grafiką, panašiai kaip ir naudodamiesi ankstesne programos „Project Service Automation“ versija. Toliau išvardijami papildomi grafiko pakeitimai.

- **Ganto diagrama** – Ganto diagramos nebėra. Naujos išvaizdos Ganto diagrama vėl bus pasiekiama atlikus būsimą naujinimą.
- **Stulpelių antraštės** – spustelėdami šalia stulpelio pavadinimo esantį indikatorių galite paslėpti tinklelio stulpelių antraštes. 
- **Stulpeliai** – spustelėdami **Įtraukti stulpelį** galite rodyti paslėptus stulpelius. 
- **Operacijos kategorija** – į grafiko tinklelį įtraukta peržvalga **Operacijos kategorija** , kuri rodoma pagal numatytuosius nustatymus. 
 
## <a name="project-templates"></a>Projekto šablonai
Atlikti toliau išvardyti projekto šablono funkcijų pakeitimai.

### <a name="create-a-project-template"></a>Projekto šablono kūrimas 
3 versijoje galite sukurti projekto šabloną, kuris bus panašus į ankstesnių „Project Service Automation“ versijų šablonus. Šablone gali būti tik grafikas, o grafike gali būti priskyrimų, tačiau jie nėra būtini. Jei grafike yra priskyrimų, jie gali būti skirti tik bendriesiems ištekliams. Galite generuoti bendrųjų išteklių reikalavimus, tačiau jų negalima rezervuoti šablone kartu su realiais ištekliais. Šablone negalite rezervuoti komandai skirtų realių išteklių. 

### <a name="create-a-template-from-an-existing-template"></a>Šablono kūrimas pagal esamą šabloną
Kuriant naują projekto šabloną pagal esamą „Project Service Automation“ 3 versijos šabloną, įvyksta tai, kas nurodyta toliau. 

- Šaltinio projekto grafikas kopijuojamas į šabloną. 
- Bendrieji ištekliai kopijuojami į komandą ir nukopijuojami visi bendrųjų išteklių priskyrimai. Bendrųjų išteklių reikalavimai nekopijuojami. 

### <a name="create-a-template-from-an-existing-project"></a>Šablono kūrimas pagal esamą projektą
Kuriant naują projekto šabloną pagal esamą projektą, įvyksta tai, kas nurodyta toliau. 

- Šaltinio projekto grafikas kopijuojamas į šabloną. 
- Bendrieji ištekliai kopijuojami į komandą ir išsaugomi visi bendrųjų išteklių priskyrimai. Bendrųjų išteklių reikalavimai nekopijuojami.    
- Įvardyti ištekliai (priskirti arba nepriskirti) pašalinami iš komandos ir keičiami bendraisiais ištekliais.
- Jei yra informacijos apie klientą, ji pašalinama. 
- Jei yra nuorodų į pasiūlymus ir sutartis, jos pašalinamos. 

### <a name="create-a-project-from-a-template"></a>Projekto kūrimas pagal šabloną
Kuriant naują projektą iš šablono „Project Service Automation“ 3 versijoje, įvyksta tai, kas nurodyta toliau.

- Grafikas, komanda ir priskyrimai kopijuojami į naują projektą.   
- Pradžios data yra kopijavimo data arba vartotojo pasirinkta data.   
- Bendriesiems komandos nariams skirti šablone nurodyti išteklių reikalavimai nekopijuojami ir negeneruojami automatiškai. Juos reikės generuoti. 

## <a name="copy-a-project"></a>Projekto kopijavimas
Kopijuojant projektą „Project Service Automation“ 3 versijoje, įvyksta tai, kas nurodyta toliau. 

- Numatoma pradžios data kopijuojama, tačiau ją galima keisti.  
- Kopijuojamas projekto grafikas ir užduotys. 
- Kopijuojami bendrieji ištekliai ir jų priskyrimai. Bendrųjų išteklių reikalavimai nekopijuojami. Juos reikės generuoti iš naujo. 
- Realūs ištekliai ir jų priskyrimai nekopijuojami. Jie pakeičiami bendraisiais ištekliais. 
- Faktiniai duomenys į naują projektą nekopijuojami. 

## <a name="move-a-scheduled-project"></a>Suplanuoto projekto perkėlimas
Perkėlus esamo projekto grafiką, įvyksta tai, kas nurodyta toliau. 

- Automatiškai perkeliamos užduočių datos, kad atitiktų perkėlimo laikotarpį. 
- Priskirti bendrieji ištekliai ir toliau lieka priskirti.   
- Jei jie sugeneruojami prieš perkeliant projektą, bendriesiems ištekliams taikomi reikalavimai išlieka nepakitę ir automatiškai iš naujo negeneruojami. Turėsite juos sugeneruoti iš naujo, kad būtų atsižvelgta į perkeliant užduotį atsiradusius naujus priskyrimus. 
- Pakeičiami realių išteklių priskyrimai, kad jie atitiktų užduoties datos perkėlimą. Realių išteklių rezervavimai nekinta. Norėdami modifikuoti rezervavimus, turėsite naudoti suderinimo rodinį. 
- Komandos ištekliai su rezervavimais, bet jokie priskyrimai nekeičiami. 
- Faktiniai duomenys neperkeliami. 

## <a name="estimates"></a>Įvertinimai
Išskiriami du įvertinimų skirtukai, **Išteklių priskyrimas** ir **Įvertinimai**. Skirtuke **Išteklių priskyrimas** pateikiami pastangų įvertinimai ir rodomi užduočių išteklių priskyrimai pagal laiko etapus. Galite redaguoti įvertinimus atsižvelgdami į tai, ką sukūrė planavimo mechanizmas.

![Išteklių priskyrimų skirtukas, kuriame rodomi pastangų įvertinimai ir užduočių išteklių priskyrimai](media/resource-assignments-tab-02.png)

Skirtuke **Įvertinimai** rodomos išteklių priskyrimų išlaidų ir pardavimo sumos. Sumos yra tik skaitomos. Išlaidų ir pardavimo įkainiai dabar kuriami pagal komandos nario priskyrimus grafike. Tai reiškia, kad jokių priskyrimų neturinti užduotis rodoma nepriskirtų užduočių talpykloje. Tai taip pat reiškia, kad neturint numatytosios įkainių dimensijos **vaidmuo** , jei turite su projektu susietą klientą arba sutartį / pasiūlymą, nenumatomos išlaidos arba pardavimai. 

![Skirtukas Įvertinimai, kuriame rodomos išlaidų ir pardavimo sumos](media/estimates-tab-03.png)
  
Grafiko rodinyje taip pat palaikoma užduočių kategorija. Įvertinimų rodiniuose pagal laiko etapus grupuojant pagal kategoriją užtikrinamos geresnės galimybės, ypač ypač jei jūsų projekte taip pat numatyti išlaidų įvertinimai. Išlaidų įvertinimai įvedami naudojantis atskiro skirtuko tinkleliu. 

Išlaidų įvertinimus galima įvesti skirtuko **Išlaidų įvertinimai** tinklelyje. 

![Skirtukas Išlaidų įvertinimai, kuriame rodomas išlaidų įvertinimų tinklelis](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Išteklių valdymas
„Project Service Automation“ 3 versijoje, kurioje naudojama nauja vieningoji kliento vartotojo sąsaja ir esama ryšių tarp rezervavimų ir priskyrimų pakeitimų, itin pasikeitė personalo priskyrimo projektui tvarka naudojantis bendraisiais arba realiais ištekliais (lyginant su 2 ir 1 versija). Tačiau tiek **realių** , tiek **bendrųjų** rezervuojamų išteklių sąvokos išlieka nepakitusios, taip pat nekinta komandos nariai, reikalavimai, priskyrimai ir rezervavimai.   

![Išteklių parinkiklio naudojimas](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Realių rezervuojamų išteklių priskyrimas 
„Project Service Automation“ 3 versijoje rezervacijos ir užduočių priskyrimai nėra taip glaudžiai persipynę kaip ankstesnėse „Project Service Automation“ versijose. Naudodamiesi komandos tinkleliu galite rezervuoti panašų į rinkoje esantį **realų** komandos narį.

Grafike naudodamiesi išteklių parinkikliu galite pasirinkti komandos rodinyje sukurtą komandos narį, paskui priskirti jam užduočių. Galite ir toliau skirti jiems užduočių, net ir pasibaigus jų rezervavimams. Naudodamiesi skirtuku **Suderinimas** galite suderinti skirtingų rezervavimų ir priskyrimų turinčius komandos narius.

Išteklių parinkiklyje rodomi projekto komandos nariai. Naudodamiesi išteklių parinkikliu taip pat galite ieškoti kitų rezervuojamų išteklių, kurie dar nėra įtraukti į jūsų projekto komandą, ir juos peržiūrėti. Galite priskirti jiems užduotį ir jie taps projekto komandos dalimi. Norėdami juos rezervuoti, turėsite naudotis skirtuku **Grafiko lenta** arba **Suderinimas**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Bendrųjų rezervuojamų išteklių priskyrimas užduočių ir projektų komandai ir vykdymas naudojantis grafiko lentoje nurodytais realiais ištekliais 
„Project Service Automation“ 3 versijoje generuojant bendruosius išteklius komandos generavimo funkcija nenaudojama. Tačiau galite sukurti ir tiesiogiai priskirti grafike nurodytus bendruosius išteklius – grafiko išteklių langelyje įveskite bendrųjų išteklių pareigų pavadinimą. Arba langelyje galite pažymėti išteklių piktogramą, o paskui, naudodamiesi išteklių parinkikliu, įvesti norimų sukurti bendrųjų išteklių pavadinimą. Taip atidarysite sparčiojo kūrimo sritį, kurioje galėsite nustatyti bendrųjų išteklių komandos nario vaidmenį ir organizacijos vienetą. Sukūrus išteklius, jiems priskiriama užduotis ir tiems bendriesiems ištekliams galite priskirti kitų grafike nurodytų užduočių.    
 
Priskyrę ištekliams visas atitinkamas užduotis, galite sugeneruoti išteklių reikalavimą ir vykdyti jį tiesiogiai rezervuodami naudodamiesi **Grafiko lenta** arba pateikdami išteklių užklausą. Bendrieji ištekliai taip pat gali būti tiesiogiai įtraukiami į komandos narių tinklelį. 

Į projekto komandą įtraukiama bendrųjų išteklių be išteklių reikalavimų ir nurodant projekto pradžios / pabaigos datas, kol sugeneruojamas išteklių reikalavimas. Norėdami sugeneruoti reikalavimą, pažymėkite bendruosius išteklius ir spustelėkite **Generuoti**. Dabar rodomas reikalavimo saitas ir reikiamų valandų laukelis užpildomas nurodant priskirtas valandas. Norėdami atidaryti ir atnaujinti reikalavimą, galite spustelėti saitą.
  
Kai įvardytas išteklius parengia rezervavimą ir visiškai jį įvykdo, bendrieji ištekliai pakeičiami įvardytu ištekliumi, o grafiko priskyrimas atnaujinamas naudojant įvardytą išteklių. 

Reikalavimams siūlomi ištekliai dabar saugomi skirtuke, o ne atskirame skyriuje.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Bendrųjų išteklių vykdymas naudojantis keliais įvardytais ištekliais
Kai reikalavimas vykdomas naudojantis keliais ištekliais, bendrieji ištekliai lieka komandoje ir priskirti užduočiai. Įvardyti rezervuoti komandos nariai nepriskiriami pareigų daliai. Projekto vadovas darbą gali priskirti reikiamiems realiems ištekliams.  Rodinyje **Suderinimas** pateikiamas kelių išteklių rezervavimų išskaidymas į kelis užduočių priskyrimus. Tai atliekama ne automatiškai, nes sudėtingesniais atvejais, pvz., tada, kai reikalavimą sudaro užduočių paketas, reikia atsižvelgti į tai, kaip projekto vadovas ketina priskirti. Kadangi sistema negali suprasti ketinimų, prielaidos gali būti kitokios, nei numatyta, ir gaunamas netinkamas arba nenuspėjamas rezultatas. Nuspėjamas rezultatas yra tada, kai bendrieji ištekliai lieka priskirti tol, kol projekto vadovas sąmoningai priskiria išteklius naudodamasis rodiniu **Suderinimas**.

### <a name="reconciliation"></a>Suderinimas
Skirtuke **Suderinimas** rodomi visi kiekvieno projekto komandos nario rezervavimai ir priskyrimai. Rodinio langeliuose rodomos valandos, kuriomis gali būti nurodomi nuo kelių mėnesių iki kelių dienų trukmės laikotarpiai. Naudodamiesi šiuo rodiniu projektų vadovai gali suderinti komandos narių rezervavimus su jų projekto komandos priskyrimais. Tai naudinga, kadangi rezervavimai ir užduočių priskyrimai nėra artimai susieti, todėl planuojant projektą galima elgtis lanksčiau. 

![Skirtukas Suderinimas, kuriame rodomi projekto komandos narių rezervavimai ir priskyrimai](media/resource-reconciliation-tab-06.png)

Kiekvieno ištekliaus rodinyje atsižvelgiama į skirtumą tarp komandos nario rezervavimų ir jam priskirtų užduočių apibendrinamosios reikšmės ir rodomi du toliau minimi galimi projekto rezervavimų ir priskyrimų skirtumai. 

- **Rezervavimų trūkumas** – rezervavimų trūkumas fiksuojamas tuo atveju, kai esama daugiau išteklių priskyrimų negu rezervavimų. Kadangi šie pajėgumai nebuvo rezervuoti, projektų vadovas gali tai pataisyti išplėsdamas išteklių rezervavimus, kad padengtų trūkumą. 
- **Rezervavimų perteklius** – rezervavimų perteklius fiksuojamas tuo atveju, kai rezervavus išteklius projektui, jiems nebuvo priskirta užduočių.  Tai gali būti priimtina tuo atveju, kai, pavyzdžiui, ištekliai buvo rezervuoti prieš priskiriant užduotį. Tačiau kitais atvejais išteklių priskyrimas gali būti neplanuotas ir projekto vadovas turėtų apsvarstyti galimybę atšaukti išteklių rezervavimus, kad būtų galima jais pasinaudoti kitam projektui. 

Jei esama užduočių, kurios priskirtos ištekliams be rezervavimų (rezervavimų trūkumo atveju), galite pažymėti bendrą rezervavimų trūkumą ir spustelėti **Pratęsti rezervavimą**. Čia galite peržiūrėti rezervavimą, kurio reikia norint imtis spręsti išteklių trūkumo ir jų pasiekiamumo problemą. 
 
## <a name="time-and-expense"></a>Laikas ir išlaidos
Šiame skyriuje pateikiama informacijos apie programos „Project Service Automation“ 3 versijos laiko, išlaidų ir patvirtinimo pakeitimus. Kadangi funkcija **Laiko įrašas** yra Dynamics 365 Project Service Automation sprendimo dalis, ji atnaujinta, kad būtų išnaudojamos vieningosios sąsajos sistemos galimybės. Tokiu būdu galima užtikrinti pastovią vartotojo sąsają, kurią rengiant pasirinktas poreikius atitinkantis dizainas, kad būtų galima optimaliai peržiūrėti bet kokio dydžio ekrane arba bet kokiame įrenginyje. 

### <a name="landing-page"></a>Nukreipimo puslapis
Nepratęsiamo pasirinktinio laiko įrašo funkcija 3 versijoje nebenaudojama. Dabar galima naudotis pratęsiamo ir prieinamo vietinio tinklelio funkcija. Laiko įrašo funkcija pasiekiama naudojantis kairėje pusėje esančia svetainės struktūra. Kadangi buvo atliktas šis pakeitimas, nebegalėsite vienu metu įvesti vienos savaitės trukmės laiko. Tinklelyje atskirai turėsite sukurti kiekvienos dienos laiko įrašą. Sukūrę keletą laiko įrašų, naudodamiesi toliau šioje temoje paaiškinta funkcija **Kopijuoti** , vartotojai vienu metu gali kurti kelis laiko įrašus. 

![Laiko įrašo nukreipimo puslapis](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Naujų laiko įrašų kūrimas 
Juostelėje spustelėję **Naujas** atidarykite laiko įrašo sparčiojo kūrimo puslapį, kuriame įveskite trukmę minutėmis, valandomis arba dienomis. Norėdami tai padaryti, tiesiog pradėkite vesti h, m arba d, nurodydami ir kiekį.  

![Laiko įrašo spartusis kūrimas](media/quick-create-time-entry-08.png)

Peržvalgos laukai susiejami su sistemos rodiniais. Pavyzdžiui, įvedus projekto informaciją, pagal numatytuosius nustatymus nustatomas lauko **Projekto užduotis** rodinys **Mano atidarytos projekto užduotys** Norėdami kurti vartotojui nepriskirtų užduočių laiko įrašus, peržvalgoje spustelėkite **Keisti rodinį** ir pažymėkite **Visos aktyvios projekto užduotys**. Sukūrę laiko įrašą, kuris rodomas tinklelyje, tiesiogiai tinklelyje galite redaguoti bet kurias eilutės reikšmes.  

### <a name="bulk-createcopy"></a>Masinis kūrimas / kopijavimas 
Sukūrę keletą laiko įrašų, naudodamiesi kopijavimo funkcija, vienu metu galite kurti kelis papildomus laiko įrašus. Spustelėję **Kopijuoti** atidarykite dialogo langą **Kopijuoti**. Laukelyje **Iš laikotarpio: pradžios data** nustatykite datą, iš kurios turi būti kopijuojami laikotarpiai. Laukelyje **Į laikotarpį: pradžios data** nurodykite datą, kurioje turi būti kuriami laiko įrašai. Spustelėję **Kopijuoti** nukopijuokite laiko įrašus į atitinkamą laukelyje **Į laikotarpį** nurodytą savaitės dieną. Pavyzdžiui, praėjusios savaitės pirmadienio laiko įrašas kopijuojamas į laukelyje **Į laikotarpį** nurodytos savaitės pirmadienį. 

![Kelių laiko įrašų kopijavimas vienu metu](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importuoti duomenis 
Atliekant priskyrimus ir keitimus taikomas tas pats vartotojo sąsajos modelis, kai vartotojai gali nurodyti datą, iš kurios reikia importuoti rezervavimus. Tada turite pasirinkti konkrečius rezervavimus, kuriuos reikia kopijuoti į laiko įrašus **Juodraštis**. Naudodamiesi 3 versija, tinklelyje ir kalendoriuje nebegalėsite matyti laiko įrašų **Siūloma** modelio.  

### <a name="change-in-calendar-control"></a>Kalendoriaus valdiklio keitimas
3 versijoje atsisakėme pasirinktinio kalendoriaus valdiklio ir dabar naudojame UC kalendorių, kuriame rodomi savaitės laiko įrašai. Naudodamiesi šiuo kalendoriumi galite peržiūrėti dieną, savaitę ir mėnesį. 

> [!NOTE]
> Kalendorius ribotas vienu požiūriu – šis valdiklis nepalaiko veiksmų atskiruose kalendoriaus elementuose. Pavyzdžiui, negalėsite pažymėti vieno ar kelių kalendoriaus elementų ir jų pateikti arba naikinti. Spustelėjus kalendoriaus elementą, atidaromas puslapis **Laiko įrašo objektas** , kuriame galima atlikti papildomus veiksmus. 

### <a name="extensibility"></a>Išplečiamumas
**Duomenų įrašymas tik laiko ir išlaidų įrašų objektų pasirinktiniuose laukuose** – laiko įrašas naudoja platformos redaguojamą tinklelį, tik skaitomą tinklelį ir kalendoriaus valdiklius. Visi šie valdikliai vietiniai, todėl bus palaikomi tinkinimai. Naudodamiesi „Project Service Automation“ 3 versija galite įtraukti papildomų pasirinktinių laukų, nustatyti peržvalgos laukus ir kurti jų atsargines kopijas su pasirinktiniais rodiniais. Taip pat galite nustatyti pasirinktinę verslo logiką pagal pasirinktas pasirinktinių laukų reikšmes.  

**Duomenų įrašymas laiko ir išlaidų įrašų pasirinktiniuose laukuose ir jų platinimas pateikimo ir patvirtinimo srautą palaikančiuose objektuose** – tipinis laiko įrašų apdorojimas pavaizduotas toliau pateikiamoje diagramoje.

![Laiko įrašo srauto apdorojimas](media/process-time-entries-10.png)

Jei verslo reikalavimuose nurodoma, kad laiko ir išlaidų objektai turi fiksuoti pasirinktinių kainų dimensijas ir platinti reikšmes (kurias laiko ir įrašo ištekliai nustato pasirinktinių kainų dimensijoje) visuose ankstesnio grafiko objektuose, žr. [Pasirinktinių laukų nustatymas kaip kainų dimensijų](set-up-pricing-dimensions.md)

Norėdami, kad verslo reikalavimai būtų palaikomi tuo atveju, kai laiko ir išlaidų objektai turi fiksuoti pasirinktines ne kainų dimensijas ir platinti reikšmes, galite naudotis kainų dimensijų sąranka ir pasirinktines dimensijas išreikšti kaip kainų dimensijas be savikainos ir sąskaitų tarifų. Arba į kiekvieną objektą galite įtraukti pasirinktinį lauką (visuose objektuose naudodami tą patį lauko pavadinimą). Galima sukurti pasirinktinius priedus, kad, naudojantis objektais Operacijos kilmė ir Operacijos ryšys, būtų susiejami pateikimo / patvirtinimo sraute dalyvaujančių objektų įrašai.  

### <a name="delegate-time-and-expense-entry"></a>Laiko ir išlaidų įrašų perdavimas
Common Data Service platforma nepalaiko vieno vartotojo apsimetimo kitu vartotoju, o tai reiškia, kad „Project Service Automation“ 3 versijoje nepalaikomi perduoti laiko ir išlaidų įrašai. Tačiau partneriai ir klientai surado problemos sprendimo būdą, kaip naudojantis 3 versija įjungti perduotų laiko įrašų patirčių palaikymą. Tai tik vienas iš problemos sprendimo būdų, o ne visas sprendimas, todėl svarbu suprasti apribojimus ir šiuo metodu naudotis tik tuo atveju, jei apribojimai priimtini. 

> [!IMPORTANT]
> Ši informacija turėtų būti laikoma tik siūloma rekomendacija, kaip partneris / klientas galėtų atlikti pasirinktinį diegimą. Produktų grupė neteikia oficialaus šios funkcijos palaikymo naudojantis bet kuriais mūsų pagalbos tarnybos kanalais.

### <a name="customization-details"></a>Išsami informacija apie tinkinimą 
Atlikdami tinkinimą į kūrimo ir redagavimo patirtis galite įtraukti **Rezervavimo išteklių** , taigi vartotojas, pakeisdamas lauką **Rezervavimo ištekliai** , kad jis būtų paskirtas kitam vartotojui, kurio laiko ir išlaidų įrašai turi būti kuriami, gali veikti kaip atstovas. Toliau aprašyti veiksmai, atliekami perduodant įrašą. Ta pati informacija taikoma perduodant išlaidų įrašą. 
 
1.  Įsitikinkite, kad įgaliotasis vartotojas turi visuotinę saugią prieigą prie projektų ir projektų užduočių. 
1.  Kadangi laukas **Rezervuojami ištekliai** (objekto **Laiko įrašas** laukas) puslapyje **Spartusis kūrimas** nerodomas, turite jį įtraukti.

    -arba-

    Sukurkite pasirinktinį rodinį, kuris apima **Rezervuojamo ištekliaus** skiltį, kad būtų rodomi tik ištekliui sukurti laiko įrašai. Publikuokite tinkinimus programos modulio dizaino įrankyje, kad jie būtų rodomi puslapio **Laiko įrašai** **Rodinių išrinkiklyje**. Yra du priedai, kuriais naudojantis nustatomas ne projekto laiko įrašų vadovas:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Sukurkite naują priedą, kad laukas **Vadovas** būtų perrašomas lauke **Rezervuojami ištekliai** priskirto vartotojo vadovui. Naudokite tą patį **Vykdymo etapą** kuris naudojamas nepatvirtintam (OOB) priedui (prieš patikrinimą) ir naudokite didesnį negu OOB priedo **Vykdymo tvarkos** skaičių (didesnį nei 1). Taip užtikrinsite, kad pasirinktinis priedas bus įvykdytas po OOB priedų.  
 
### <a name="end-user-experience"></a>Galutinio vartotojo patirtis
1.  Kurdami laiko įrašą sparčiojo kūrimo puslapyje, įveskite išsamią informaciją apie projektą ir projekto užduotį, o paskui lauke **Rezervuojami ištekliai** pasirinkite vartotoją, kuriam reikia įrašyti laiko įrašus. 
2.  Pagal numatytuosius nustatymus šis laukas nustatomas prisijungusiam vartotojui, tačiau, kadangi vartotojas šį lauką perrašė, laiko įrašas dabar kuriamas pasirinktiems **Rezervuojamiems ištekliams**.
3.  Pateikus šiems įrašams sukurtus laiko įrašus, kaip įprastai, sudaroma tvirtintojui skirta įrašų eilė. 
4.  Atšaukus kitam vartotojui sukurtus laiko įrašus, vėl nustatoma laiko įrašų būsena **Juodraštis** (kai laukas **Rezervuojami ištekliai** nustatytas kitam vartotojui). 
5.  Arba galite įjungti pasirinktinį rodinį, skirtą kitam vartotojui sukurtiems laiko įrašams filtruoti. 
 
### <a name="limitations"></a>Apribojimai
Funkcijos **Kopijuoti** ir **Importuoti** veikia tik prisijungusio vartotojo kontekste. Tai reiškia, kad neįmanoma kopijuoti arba importuoti laiko įrašų, sukurtų vartotojo, prisijungusio kaip rezervuojami ištekliai.

Ne projektui skirti laiko įrašai nukreipiami rezervuojamų išteklių vadovui, kad juos patvirtintų, tik tuo atveju, jei atliktas ankstesniame skyriuje **Išsami informacija apie tinkinimą** nurodytas 4 veiksmas. Priešingu atveju, kito vartotojo ne projekto laiko įrašai bus neteisingai nukreipiami prisijungusio vartotojo vadovui. 

### <a name="other-changes"></a>Kiti pakeitimai 
Panaikinta funkcija **Rezervavimai ir užduotys**. 

## <a name="multidimensional-pricing"></a>Kelių dimensijų įkainiai
Siekiant užtikrinti maksimalų lankstumą ir patenkinti įvairius verslo reikalavimus, programos „Project Service Automation“ 3 versija palaiko atskirai savikainos ir sąskaitų tarifams taikomus kainų dimensijų rinkinius. Dimensijų reikšmes galima nustatyti kaip numatytąsias ir išlaidų bei įkainių nustatymo proceso metu perkelti iš išteklių profilių į laiko įrašą ir projekto faktinius duomenis. Atliekant konkrečiam klientui būdingą konfigūraciją ir modifikavimą arba išplėtimą naudojama standartinė tinkinimo infrastruktūra.

„Project Service Automation“ pateikiama su numatytuoju kainų dimensijų bei vaidmenų ir išteklių vienetų rinkiniu ir galima nustatyti kiekvienam vaidmens ir organizacijos vieneto deriniui skirtą kainą ir savikainą.

„Project Service Automation“ klientai, norintys šiuos parengtus naudoti laukus 3 versijoje toliau naudoti kaip kainų dimensijas, jokių pokyčių nepastebės. Galite toliau naudoti „Project Service Automation“ kaip įprasta. Tačiau jei ištekliams skirtas kainas ar savikainą reikia nustatyti naudojantis kitais papildomais atributais, naudodamiesi 3 versija „Project Service Automation“ galite įtraukti savo pasirinktines kainų dimensijas. Pasirinktinių kainų dimensijų išplėtimas yra sudėtinga konfigūravimo patirtis. 

## <a name="quotes-and-contracts"></a>Pasiūlymai ir sutartys
„Project Service Automation“ 3 versijoje pasikeitė pasiūlymų ir sutarčių sąrankos ir valdymo aspektai. Tolesniuose skyriuose pateikiama daugiau informacijos.

### <a name="set-up-chargeability-options"></a>Apmokestinimo parinkčių nustatymas
1 ir 2 versijose tam tikrų pasiūlymų ir sutarčių vaidmenų ir kategorijų apmokestinimo sąranka buvo atliekama naudojantis rodiniu **Apmokestinimas** , esančiu pasiūlymo ar sutarties eilutės naršymo juostos viršuje. Čia taip pat galėjote nustatyti tiems vaidmenims ir toms išlaidų kategorijoms skirtas kainas.

3 versijoje ir naujesnėse versijose apmokestinimo parinktys pagal vaidmenį ir išlaidų kategoriją bus nustatomos pasiūlymo arba sutarties eilutės lygiu. Įkainių sąranka skiriasi nuo apmokestinimo sąrankos. Puslapiuose **Pasiūlymo eilutė** ir **Sutarties eilutė** rasite skirtukus **Apmokestinami vaidmenys** ir **Apmokestinamos kategorijos** ir nereikės naudotis viršutine naršymo juosta.

![Apmokestinami vaidmenys](media/chargeable-12.png)
 
Atliekant apmokestinamų vaidmenų ir apmokestinamų kategorijų sąranką taip pat naudojamasi iš anksto nustatytu redaguojamu tinklelio valdikliu. Kiekvieno vaidmens ir kategorijos atsiskaitymo tipo palaikomos parinktys teikiant pasiūlymą ir sudarant sutartį išlieka nepakitusios, t. y., kaip ir ankstesnėse versijose ( **Apmokestinama** ir **Neapmokestinama** ). Tipas **Nemokama** teikiant pasiūlymą ar sudarant sutartį nepalaikomas. Tipas **Nemokama** palaikomas tik tvirtinant laiką ir išlaidas.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Pasirinktinių „Project Service Automation“ pasiūlymui ir projekto sutarčiai taikomų įkainių kūrimas ir redagavimas
1 ir 2 versijose norint pasinaudoti pasirinktiniu konkrečių pasiūlymų ir sutarčių kainoraščiu, tai buvo atliekama naudojantis rodinio **Apmokestinimas** parinktimi **Redaguoti kainas**. Rodinį **Apmokestinimas** buvo galima rasti viršutinėje pasiūlymo eilutės arba sutarties eilutės naršymo juostoje. Čia taip pat galėjote nustatyti vaidmenims ir (arba) išlaidų kategorijoms skirtas apmokestinimo parinktis.

3 versijoje ir naujesnėse versijose „Project Service Automation“ pasiūlymo ir „Project Service Automation“ projekto sutarties pasirinktinio projekto kainoraščio kūrimas ir naudojimasis juo nebėra apmokestinimo sąrankos dalis. „Project Service Automation“ pasiūlymas ir „Project Service Automation“ projektų sutartys turi naują skirtuką **Projekto kainoraščiai**. Šiame skirtuke rodomas visų prie „Project Service Automation“ pasiūlymo ar projekto sutarties pridėtų projektų kainoraščių susietasis rodinys. Norėdami pagal esamą kainoraštį, kuris jau susietas su projekto pasiūlymu arba sutartimi, sukurti pasirinktinį kainoraštį, spustelėkite **Kurti pasirinktines kainas**. Tai atlikus sukuriamos visų susietų kainoraščių kopijos, kurios pridedamos prie pasiūlymo ar sutarties. Dabar galite atidaryti kainoraštį ir redaguoti vaidmens arba išlaidų kategorijos kainą, kad pakeisti įkainiai būtų taikomi tik šiam pasiūlymui arba sutarčiai. 
  
Šioje iliustracijoje pavaizduotas rodinys prieš sukuriant pasirinktinius kainoraščius.

![Prieš pasirinktinius kainoraščius](media/before-custom-price-lists-13.png)

Šioje iliustracijoje pavaizduotas rodinys sukūrus pasirinktinius kainoraščius.

![Po pasirinktinių kainoraščių](media/after-custom-price-lists-14.png)

> [!NOTE]
> Spustelėjus **Kurti pasirinktines kaina** gali tekti šiek tiek palaukti, kol bus sukurtas pasirinktinis kainoraštis. Rekomenduojame atnaujinti tinklelį, o ne spustelėti kelis kartus. Pasirinktinis kainoraštis sukurtas, jei prie susieto kainoraščio pavadinimo pridėtas pasiūlymo pavadinimas arba projekto sutarties pavadinimas.
