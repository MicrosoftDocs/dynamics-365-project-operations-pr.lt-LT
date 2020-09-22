---
title: Duomenų pavyzdžių įdiegimas
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: kfend
ms.suite: ''
ms.technology: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.assetid: 8580fc8b-868a-42a3-aa04-2afab28d6de4
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 1c1300116fe42091620267fb128ca6c63184970e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753621"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Duomenų pavyzdžių diegimas programoje „Project Service“

Tam, kad jums būtų lengviau kurti savo demonstracinę aplinką, „Microsoft“ teikia atsisiunčiamus pavyzdžių duomenų paketus, kuriuose parodomos mobiliųjų įrenginių programėlių galimybės. Galimi du toliau nurodyti duomenų paketų pavyzdžių tipai.
- nuorodos / sąrankos duomenys
- demonstraciniai duomenys (nuorodos / sąrankos ir operacijų duomenys, pvz., darbo užsakymai ir projektai)

**Nuorodos** duomenų pavyzdžiai atsisiunčiami naudojant tris skirtingus paketus, todėl galite įdiegti duomenis tik programoje „Project Service“ ar tik „Field Service“ arba galite įdiegti duomenų pavyzdžius abiejose programose vienu metu.

Toliau nurodyti sąrankos / nuorodos duomenų paketų pavyzdžiai.

- [**V902PSMasterData** – tik „Project Service“ 3.x versija](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** – tik „Field Service“ 8.x versija](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** – „Field Service“ 8.x ir „Project Service“ 3.x versijos](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Naujausias **demonstracinių** duomenų paketas:

 - [**FPSDemoData** – „Field Service“ 8.x ir „Project Service“ 3.x versijos](https://aka.ms/fpsdemodatapackage)

   Vartotojams skirtos diegimo instrukcijos (kūrimo ir konfigūravimo skiltis) gali šiek tiek skirtis, bet likusi informacija yra tokia pati kaip informacija ankstesniame [**tinklaraščio skelbime**](https://aka.ms/fpsdemodatablog). Šiame pakete pateiktas apribotas demonstracinių duomenų rinkinys ir jo diegimas trunka 3 val.

Šie pavyzdžių duomenų paketai teikiami tik anglų kalba.

> [!IMPORTANT]
> **Duomenų pavyzdžių pašalinti neįmanoma.** Šiuos paketus turėtumėte diegti tik demonstracinėse, vertinimo, mokymo arba bandymo sistemose. Taip pat atkreipkite dėmesį, kad negalima įdiegti atskiro paketo ir tada įdiegti kito atskiro paketo. (T. y. negalite įdiegti **FSMasterData**, o tada įdiegti **PSMasterData**, arba atvirkščiai). Jei ateityje reikės pavyzdžių duomenų abiejose programose, turite įdiegti paketą **v902FPSMasterData**.

Kai įdiegiate bet kurį pavyzdžių duomenų paketą, diegimo proceso metu atliekami toliau nurodyti veiksmai.

- Sukuria arba nustato numatytuosius parametrus, skirtus naudoti „Project Service“, „Field Service“ arba abiejose programose (jei taikoma).

- Importuoja programų pavyzdžių duomenis, pvz., užsakomus išteklius, konkrečių programų vaidmenis, pardavimo ir išlaidų kainoraščius, organizacijų vienetus, pardavimo proceso įrašus ir kitus objektus, kad būtų parodytos pagrindinės galimybės.  

Įdiegę **demonstracinių duomenų** paketą gaunate pirmiau nurodytus ir papildomus operacijų duomenis, pvz., darbo užsakymų ir projektų duomenis.

Įdomu, kokias galimybes galite demonstruoti naudodami pavyzdžių duomenis? Peržiūrėkite toliau pateiktą sugalvotą „Fabrikam Robotics“ scenarijų skiltyje [Techninės pastabos](#technical-notes).

Jei turite klausimų apie šių pavyzdžių duomenų paketų diegimą, [atsiųskite mums el. laišką adresu fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Reikalavimai

Diegimo protokolas numato toliau nurodytą informaciją apie paskirties egzempliorių (organizacijos).

- Pagrindinė kalba yra anglų ir pagrindinė valiuta yra JAV doleris (USD).

- Organizacija dar neturi „Project Service“ arba „Field Service“ duomenų arba turi tik pagrindinius numatytuosius duomenis, kurie teikiami kiekvienai naujai organizacijai.

- Tinkama verslo programos versija jau įdiegta.
       
    - **FPSDemoData arba v902FPSMasterData:** organizacija įdiegusi „Field Service“ 8.x versiją ir „Project Service“ 3.x versiją.

    - **v902PSMasterData:** organizacija įdiegusi „Project Service“ 3.x versiją.

    - **v902FSMasterData:** organizacija įdiegusi „Field Service“ 8.x versiją.

> [!NOTE]
> Jei duomenų pavyzdžius reikia įdiegti esamoje „Project Service“ ir „Field Service“ bandomojoje ar demonstracinėje aplinkoje, kurioje jau yra duomenų (nerekomenduojama), jums reikia laikinai sustabdyti išankstinį saugos patikrinimą, kurį atlieka diegimo programa. Norėdami gauti daugiau informacijos, žr. toliau pateiktą techninę informaciją.

## <a name="prepare-for-installation"></a>Pasiruošimas diegti

Turite paleisti diegimo programą kompiuteryje, kuriame įdiegta nesena „Windows“ versija (pageidaujama – „Windows 10“).

Turėtumėte pasirengti palikti kompiuterį prijungtą prie tinklo; **sąrankos / nuorodos duomenų** diegimas truks iki **1 valandos**. (Paprastai **FPSMasterData** diegimas trunka apie 30 minučių; tai apima abiejų programų duomenų pavyzdžių diegimą.) **FPSDemoData** diegimas truks apie **3 valandas**.

Kompiuterio ekrano užsklandos funkcija turi būti išjungta. Kitu atveju diegimo seanso kredencialai gali būti prarasti, kai įjungiama ekrano užsklanda (nebent seansas liks aktyvus).

> [!div class="mx-imgBorder"]
> ![Ekrano užsklandos parametrų ekrano kopija; ekrano užsklanda išjungta](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Atsisiuntimas ir išpakavimas

„Project Service“ ir „Field Service“ duomenų pavyzdžių diegimo programą platinama kaip savaime išsiskleidžiantis vykdomasis failą. Failų vardai gali skirtis, priklausomai nuo pavyzdžių duomenų paketo, bet veiksmai yra vienodi, nepriklausomai nuo diegiamo paketo.

Atsisiuntę paketą paleiskite EXE failą ir sutikite su sąlygomis, kad išpakuotumėte suglaudintą ZIP failą. Turite išskleisti to failo turinį kompiuterio aplanke.

Priklausomai nuo operacinės sistemos ir saugos parametrų, išpakavus ZIP failą gali reikėti atlikti toliau nurodytus veiksmus.

1. Raskite ir dešiniuoju pelės mygtuku spustelėkite failą **FPSDemoData.dll** aplanke **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Pasirinkite **Atblokuoti**.

3. Pasirinkite **Taikyti**.

4. Pasirinkite **Gerai**.


## <a name="create-or-configure-users"></a>Vartotojų kūrimas ir konfigūravimas

**FPSDemoData** paketui būtini šeši vartotojai, o **FPSMasterData** paketui – vienas vartotojas. Pasirinkite jūsų duomenų paketo pavyzdžiui tinkamą skaičių.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Vartotojų kūrimas arba konfigūravimas – sąrankos / nuorodos duomenų paketai

Paketas **FPSMasterData** sukurtas įdiegti su vienu vartotoju Spencer Low, naudojant čia aprašytus parametrus. Norėdami tinkamai įdiegti paketą, turite sukurti (arba laikinai pervardyti) vartotojus savo aplinkoje, kad jie atitiktų gaunamą duomenų pavyzdžių konfigūraciją.

Norėdami sukurti arba konfigūruoti vartotojus, pasirinkite **Parametrai** > **Sauga** > **Vartotojai** ir atlikite toliau nurodytus veiksmus.

1. Nustatykite UserFullname = "Spencer Low" su vartotojo vardu „spencerl“ (**mažosios raidės**) į projektų vadovo ir praktikos vadovo vaidmenis.

2. Pasirinkite vartotoją **Spencer Low**, o po to pasirinkite **Tvarkyti vaidmenis**. Raskite ir pasirinkite vaidmenį **Sistemos administratorius**, tada pasirinkite **Gerai**, kad Spencer Low suteiktumėte visas administratoriaus teises. Šis veiksmas yra būtinas norint užtikrinti, kad įrašų pavyzdžiai kuriami nustačius tinkamą vartotojo nuosavybę, ir tinkamai užpildyti rodinius.

3. Naudojant atsisiųstą paketą jums reikia atnaujinti duomenų susiejimo failą į numatytojo vartotojo konteksto el. pašto adresą. Norėdami tai padaryti, atidarykite **PkgFolder**, tada raskite ir atidarykite failą **ImportUserMapFile.xml** programoje „Notepad“ (arba „Visual Studio“ ar kitoje XML rengyklėje). Nustatykite lauką **DefaultUserToMapTo=** į vartotojo Spencer Low el. pašto adresą.

4. Jei nenaudojate Spencer Low su vartotojo vardu **spencerl**, turite atnaujinti papildomą failą. Atidarykite failą **DemoDataPreImportConfig.xml** ir raskite žymę **userstocreateandconfigure**. Atnaujinkite **\<prisijungimo\>** žymę nurodydami vartotojo Spencer Low vartotojo vardą. Norėdami gauti papildomos informacijos, žr. [techninę informaciją](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Vartotojų kūrimas ir konfigūravimas – demonstracinių duomenų paketas

Demonstraciniam duomenų paketui būtini šeši vartotojai. Norėdami tinkamai įdiegti paketą, atlikite toliau nurodytus veiksmus.

 1. Sukurkite arba laikinai pervardykite esamus vartotojus, kad jie atitiktų gaunamą duomenų konfigūracijos pavyzdį, pasirinkdami **Parametrai** > **Sauga** > **Vartotojai**.
 
    Šie vaidmenys reikalingi tik naudojant asmenims skirtus demonstracinius duomenis.  
    - User Fullname="David So" kaip „Field Service“ technikas   
    - User Fullname="Jamie Reding" kaip „Customer Service“ ir kaip „Field Service“ dispečeris   
    - User Fullname="Molly Clark" kaip klientų vadovė   
    - User Fullname="Spencer Low" kaip praktikos ir projektų vadovas  
    - User Fullname="Veronica Quek" kaip komandos narė   
    - User Fullname="William Danys"
  
2. Importuodami demonstracinius duomenis, priskirkite šešiems pirmiau nurodytiems vartotojams administratoriaus vaidmenį, kad įrašų pavyzdžiai būti tinkamai importuoti. 

3. Atidarykite **PkgFolder** ir raskite bei atidarykite **ImportUserMapFile.xml**. Atnaujinkite laukus **New=** nurodydami el. pašto adresus, kurie atitinka vartotojus jūsų sistemoje.

   > [!div class="mx-imgBorder"]
   > ![„UserMapFile“ ekrano kopija](media/sample-data-7.png)

4. Jei vartotojui, kurio vardas ir pavardė „Spencer Low“, priskirtas vartotojo ID nėra **spencerl**, turite atnaujinti papildomą failą. Atidarykite**DemoDataPreImportConfig.xml** ir raskite žymę **userstocreateandconfigure**. Atnaujinkite **\<prisijungimo\>** žymę nurodydami „loginId“ (skiriamos didžiosios ir mažosios raidės). 

5. Pirmojo vartotojo kalendorius (žymėje **userstocreateandconfigure**) naudojamas užpildant visų užsakomų išteklių darbo valandas demonstracinių duomenų importavimo metu. Pasirinkite **Parametrai** > **Sauga** > **Vartotojai**, raskite vartotoją „Spencer Low“ ir atidarykite parinktį „Darbo valandas“. Redaguokite esamas darbo valandas, pasirinkdami parinktį **Visas pasikartojantis savaitės grafikas nuo pradžios iki galo**. Užtikrinkite, kad **lauke Darbo valandos nustatyta reikšmė į 8:00–17:00 val. (9 valandos), pirmadienis–penktadienis, o lauke Laiko juosta – reikšmė Ramiojo vandenyno laikas (JAV ir Kanada)**. Tai reikia atlikti siekiant užtikrinti, kad projekto ir grafiko lentos duomenys būtų rodomi tinkamai.

**Rekomendacija:** galite dabar sukurti organizacijos duomenų atsarginę kopiją, jei duomenų pavyzdžių diegimo metu kils problemų ir norėsite juos atkurti. Daugiau informacijos rasite [Egzempliorių atsarginių kopijų kūrimas ir atkūrimas](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Paleiskite Package Deployer

1. Raskite ir paleiskite **PackageDeployer.exe** aplanke **v902FPSMasterData** ARBA **PackageDeployer_FPSDemoData**.

2. Sutikite su sąlygomis.

3. Kitame lange:

   a. Pasirinkite visuotinio diegimo tipą **„Office 365**“.

   b. Naudokite sistemos administratoriaus vartotojo, sukonfigūruoto dalyje Vartotojų kūrimas ir konfigūravimas, vartotojo vardą ir slaptažodį" (Spencer Low su vartotojo vardu „spencerl“).

   c. Įsitikinkite, kad žymės langelis **Rodyti galimų organizacijų sąrašą** yra pažymėtas.

      > [!div class="mx-imgBorder"]
      > ![Ekrano kopijos Package Deployer langas pasirinkus „Rodyti galimų organizacijų sąrašą“](media/sample-data-2.png)

4. Pasirinkite organizaciją, kurioje norite įdiegti duomenų pavyzdžius.

5. Pasirinkite **Toliau**, kol pamatysite dialogo langą **Demonstracinių duomenų sąranka**.

   > [!div class="mx-imgBorder"]
   > ![Demonstracinių duomenų diegimo būsenos lango ekrano kopija](media/sample-data-3.png)

6. Prieš tęsdami atkreipkite dėmesį, kad duomenų pavyzdžių diegimas gali užtrukti iki vienos valandos (paprastai – apie 10 minučių). Kompiuteris privalo būti įjungtas ir prijungtas prie tinklo diegimo proceso metu, o seansas turi būti aktyvus.   

7. Kai būsite pasiruošę, spustelėkite **Toliau**, kad pradėtumėte duomenų pavyzdžių diegimo procesą. Įkėlus duomenų pavyzdžius, spustelėkite **Baigti**.

## <a name="verify-the-sample-data-installation"></a>Duomenų pavyzdžių diegimo patikrinimas

Patikrinkite, ar kad įrašų ir objektų tipų skaičius „Fabrikam Robotics“ išgalvotame scenarijuje rodomas tinkamai.

Visiškai įkėlus duomenų pavyzdžius, prisijunkite kaip vartotojas Spencer Low ir patikrinkite toliau nurodytą informaciją.

- Jei įdiegta programa „Project Service“, pasirinkite **Project Service** > **Parametrai** > **Kainoraščiai**. Įsitikinkite, kad sąskaitos tarifai ir išlaidų tarifai nurodyti naudojant tinkamą kiekvienos šalies / regiono valiutą duomenų rinkinyje.

- Jei įdiegta programa „Project Service“, pasirinkite **Universal Resource Scheduling** > **Parametrai** > **Organizacijos vienetai**. Įsitikinkite, kad kainoraštis su tinkama valiuta yra susietas su kiekvienu organizacijos vienetu (išskyrus miestų įrašus). Jei kainoraštis nesusietas, raskite ir susiekite tinkamą kainoraštį.

- Jei įdiegta programa „Field Service“, pasirinkite **Project Service** > **Parametrai** > **Kainoraščiai**. Įsitikinkite, kad nurodyti sąskaitos tarifai ir išlaidų tarifai. Pasirinkite **Field Service** > **Parametrai** > **Kainoraščiai** ir patikrinkite, ar sąskaitos tarifai ir išlaidų tarifai yra nurodyti naudojant tinkamą valiutą, skirtą kiekvienai šaliai / regionui duomenų rinkinyje.

  > [!div class="mx-imgBorder"]
  > ![Aktyviųjų kainoraščių ekrano kopija](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Aktyviųjų organizacijos vienetų ekrano kopija](media/sample-data-5.png)

## <a name="technical-notes"></a>Techninės pastabos

Toliau rasite daugiau techninės informacijos apie šių duomenų diegimą.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Duomenų pavyzdžių diegimas aplinkoje, kurioje yra duomenų (nerekomenduojama)

Jei duomenų pavyzdžius reikia įdiegti esamoje „Field Service“ arba „Project Service“ bandomojoje ar demonstracinėje aplinkoje, kurioje jau yra duomenų, jums reikia laikinai sustabdyti išankstinį saugos patikrinimą, kurį atlieka diegimo programa.

Norėdami tai padaryti, pasirinkite aplanką **PkgFolder** ir raskite bei atidarykite failą **DemoDataPreImportConfig.xml** naudodami „Notepad“ (arba kitą XML rengyklę).

Raskite toliau nurodytą reikšmę ir pakeiskite parametrą iš „true“ į „false“.

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Dėl šio pakeitimo diegimo programa neatliks tam tikrų svarbių saugos patikrinimų, įskaitant toliau nurodytuosius.

- Patikrinimas, ar yra ne daugiau kaip vienas aktyvus **organizacijos vieneto** įrašas ir jo pervardijimas į **Fabrikam US**.

- Patikrinimas, ar yra ne daugiau kaip vienas aktyvus **darbo šablono** įrašas.

- Patikrinimas, ar yra ne daugiau kaip vienas aktyvus **projekto parametro** įrašas ir to įrašo pervardijimas į **Parametrai**.

### <a name="configuration-components"></a>Konfigūracijos komponentai

Šiame išankstinio konfigūravimo faile yra keletas kitų konfigūravimo komponentų. Toliau nurodyti kai kurie iš šių komponentų, skirtų techniniams vartotojams.

- **\<RequiredSolutions\>** nurodo būtinuosius sprendimo diegimus ir jų versijos numerius.

- **\<InstallSampleData\>** kontroliuoja, ar diegiami parengti naudoti duomenų pavyzdžiai, skirti programoms.

    - „false“ – praleidžia šių įtaisytųjų duomenų (kuriuos galima pašalinti) diegimą

    - „true“ – įdiegia įtaisytuosius duomenis, sutampančius su FS ir PSA duomenų pavyzdžių diegimu

- **\<PreImportDataCollection\>** nurodo paprastųjų failų duomenų struktūras ir susijusius įrašus, kurie bus importuojami prieš pagrindinių duomenų pavyzdžių diegimą.

- **\<EntitiesToEnableScheduling\>** nurodo, kurie objektai turi būti įgalinti „Microsoft Dynamics Scheduling“ (taip pat – „Universal Resource Scheduling“) rezervavime.

- **\<UsersToCreateAndConfigure\>** nurodo užsakomus išteklius, kurie bus sukurti (jei jie dar nesukurti) prieš duomenų pavyzdžių importavimą. Atkreipkite dėmesį, kad šaltinio sistemos duomenų pavyzdžių užsakomi ištekliai atitinka paskirties sistemos užsakomų išteklių įrašus kiekvieno ištekliaus lauke FullName ir prisijungimo informacijos lauke. Todėl šiame iš anksto sukonfigūruotame faile pavadinimų keisti negalima, nebent pirmiausia importuosite duomenų pavyzdžius į paskirties sistemą naudodami šiuos pavadinimus, tada pervardysite užsakomus išteklius į norimą vardų rinkinį kartu su įjungtų vartotojų įrašais ir eksportuosite duomenis dar kartą, kad importuotumėte į galutinę paskirties sistemą (atitinkamai atnaujindami senus ir naujus failo **ImportUserMapFile.xml** įrašus).

- **\<PluginsToDisable\>** nurodo itin diskretiškus eilutės elemento priedus, kurie turi būti išjungti duomenų pavyzdžių importavimo metu ir vėliau vėl įjungti.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Išgalvotas „Fabrikam Robotics“ scenarijus

„Field Service“ ir „Project Service“ nuorodos duomenų pavyzdžių paketai įdiegia **„Fabrikam“ gamybos pagrindinių duomenų (v3.0.0.0) sprendimą** su maždaug 4000 įrašų ir 40 skirtingų objektų. Atskiruose „Field Service“ ir „Project Service“ duomenų pavyzdžių paketuose yra tos programos **v902FPSMasterData** duomenų pavyzdžių antrinis rinkinys. **Demonstracinių duomenų** paketas diegia **„Fabrikam“ gamybos demonstracinių duomenų (v3.0.0.7) sprendimą**, įskaitant maždaug 22 000 įrašų 148 objektuose.

Išgalvota įmonė „Fabrikam Robotics“ yra elektroninių įrenginių surinkimo robotų gamintoja ir ji yra žinoma dėl savo produktų kokybės, naujovių ir kokybiško klientų aptarnavimo, įskaitant diegimo planavimą, diegimą ir nuolat teikiamas techninės priežiūros paslaugas. „Fabrikam“ įsikūrusi Jungtinėse Valstijose („Fabrikam US“) ir vykdo projektų aptarnavimo operacijas Prancūzijoje, Indijoje, Jungtinėje Karalystėje bei Šveicarijoje.

„Field Service“ operacijų centras yra Jungtinėse Valstijose (daugiausia – didžiajame Sietlo regione). Įmonė yra tikslingai naudoja daiktų interneto („IoT“) ryšį, kad stebėtų klientų turto efektyvumą ir teiktų vis veiksmingesnes paslaugas vietoje.

Toliau pateikta išsami duomenų pavyzdžių apžvalga.

- Įprasti duomenų pavyzdžių elementai (įtraukti į abi programas)

    - 1 vartotojas

    - 71 klientas

    - 137 kontaktai

    - Įvairūs operacijų tipai ir kategorijos

    - 50 produktų ir 1 produktų kainoraštis

    - 14 kainoraščių

    - 31 ypatybė (išteklių įgūdžiai) 2 įvertinimo modeliuose su 3 lygiais (vertinimo reikšmės)

- „Project Service“

    - 8 organizacijos vienetai

    - 6 konkrečių vaidmenų naudojimo lygiai

    - Virš 2,8 tūkst. vaidmenų ir kainos specifikacijų

- Field Service

    - 4 teritorijos

    - 5 darbo užsakymų tipai

    - 22 klientų turto vienetai

    - 9 incidentų tipai su įvairiomis susijusiomis išteklių ypatybėmis (9), paslaugomis (13) ir aptarnavimo užduotimis (13)
   
**Demonstracinių duomenų** paketas įdiegia maždaug 179 darbo užsakymus, 12 projektų ir susijusius operacijų duomenis. 

### <a name="change-the-work-hours-for-sample-resources"></a>Išteklių pavyzdžių darbo valandų keitimas

Pagal numatytuosius parametrus nustatytas 24 darbo valandų kalendorius.

Jei norite pakeisti rezervuojamų išteklių pavyzdžių darbo valandas, pasirinkite **Universal Resource Scheduling** > **Planavimas** > **Ištekliai**.

Pasirinkite vartotoją (pvz., Spencer Low) ir pakeiskite Spenserio darbo valandas į valandas, kurias norite taikyti keliems vartotojams. Pasirinkite **Universal Resource Scheduling** > **Parametrai** > **Darbo valandų šablonai** ir redaguokite įrašą **Numatytasis darbo šablonas**. Lauke **Šablono išteklius** pasirinkite vartotoją, kurio darbo valandas norite taikyti kitiems ištekliams. Norėdami planuoti **Universal Resource Scheduling** > **Planavimas** > **Ištekliai** > **Aktyvūs rezervuojami ištekliai**. Pasirinkite išteklius, kuruos norite keisti, ir pasirinkite **Nustatyti kalendorių**. Išplečiamajame sąraše **Darbo šablonas** pasirinkite šabloną **Numatytosios darbo valandos** arba kitą šabloną su tinkamu šablono ištekliumi. Atidarę grafiko lentą turėtumėte matyti atnaujintas išteklių darbo valandas.

> [!div class="mx-imgBorder"]
> ![Aktyviųjų užsakomų išteklių ekrano kopija](media/sample-data-6.png)
