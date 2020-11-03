---
title: Tvarkyti išteklius
description: Šioje temoje pateikiama informacija apie tai, kaip galite tvarkyti išteklius.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081037"
---
# <a name="manage-resources"></a>Tvarkyti išteklius

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Į Dynamics 365 Project Service Automation įeina išteklių valdymo ataskaitų sritis, teikianti vaizdinį išteklių poreikio ir naudojimo visoje organizacijoje apžvalgą. Šioje ataskaitų srityje galite naudoti diagramas, kad galėtumėte vizualizuoti šią informaciją:

- **Išteklių poreikis** – diagramoje **Aktyvių išteklių užklausa** rodomi pateikt ištekliai. Ištekliai yra agreguojami pagal vaidmenį arba projektą.
- **Nepateiktų išteklių poreikis** – diagramoje **Nepriskirtų išteklių poreikis** rodomi visi nepateikti išteklių reikalavimai. Tai padeda išteklių vadovams peržiūrėti poreikį, kuris nėra patvirtintas ir gali būti pateiktas naudojant išteklių užklausą.
- **Apmokėtinas realizavimas per paskutinę savaitę** – diagramoje **Naudojimas pagal vaidmenį** rodoma organizacijos faktinis apmokamas realizavimas pagal vaidmenį lyginant su tiksliniu apmokėtinu realizavimu pagal vaidmenį.

    > [!NOTE]
    > Kad pasiektumėte diagramą **Naudojimas pagal vaidmenį** , sukurkite užduotį, kuri vykdo darbo eigą UpdateRoleUtilization. Ši pasikartojanti užduotis vykdoma kas septynias dienas, kad apskaičiuotų apmokėtiną realizavimą per ankstesnes septynias dienas. Rezultatai sujungiami pagal vaidmenį.

## <a name="manage-project-team-members"></a>Projekto komandos narių valdymas

Projektų vadovai gali naudoti išteklių vadovo ataskaitų sritį, kad valdytų projektų išteklius. Pavyzdžiui, jie gali įtraukti komandos narį tiesiogiai į projektą ir rezervuoti komandos narį vykdyti išteklių reikalavimus, kurie buvo užfiksuoti bendrųjų išteklių.

### <a name="add-a-team-member-directly-to-a-project"></a>Komandos nario įtraukimas tiesiogiai į projektą

Norėdami įtraukti komandos narį tiesiogiai į projektą, puslapio **Projektai** skirtuke **Komanda** pasirinkite **Naujas**. Atsiras dialogo langas **Spartusis kūrimas: projekto komandos narys**. Šiame dialogo lange galite atlikti šias užduotis:

- **Rezervuokite įvardytuosius išteklius** – lauke **Rezervuojami ištekliai** pasirinkite ištekliaus pavadinimą. Tada pažymėkite vaidmenį, nustatykite laikotarpį ir pažymėkite paskirstymo metodą. Jūsų pažymėtas įvardytas išteklius įtraukiamas į projektą naudojant pasirinktą paskirstymo metodą ir išteklių kalendorių.
- **Įtraukite bendrąjį išteklių** – palikite lauką **Rezervuojami ištekliai** tuščią, o tada pažymėkite vaidmenį, nustatykite laikotarpį ir pažymėkite pageidaujamą paskirstymo metodą. Bendrasis išteklius įtraukiamas į komandą kaip vietos rezervavimo ženklas, kad būtų išlaikytas poreikio modelis, kuris naudojamas įvardytiesiems ištekliams komandoje užsakyti. Reikalavimas pateikiamas pagal projekto kalendorių.
- **Įtraukite įvardytąjį išteklių į komandą nenaudojant išteklių pajėgumo** – lauke **Rezervuojami ištekliai** pažymėkite išteklių. Tada pasirinkite laikotarpį ir pažymėkite **Nėra** kaip paskirstymo metodą. Išteklius įtraukiamas į komandą, tačiau ištekliaus pajėgumas užsakyme nenaudojamas.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Užsakykite komandos narį, kad būtų galima vykdyti išteklių reikalavimus bendriesiems ištekliams

Naudodami PSA galite užsakyti bendrąjį išteklių projekto komandoje ir nurodyti vaidmenį, būtiną pajėgumą ir šio pajėgumo paskirstymą. Kaip išteklių reikalavimus galite nurodyti su bendruoju ištekliumi susietus atributus. Į šiuos atributus įtraukti būtini įgūdžiai, pageidaujamas organizacijos vienetas ir pageidautini ištekliai.

Vadovaukitės šiais veiksmais, kad nustatytumėte bendrūjų išteklių kūrėjams būtinus įgūdžius.

1. Puslapio **Projektai** skirtuke **Komanda** pažymėkite **Naujas** , kad rezervuotumėte bendrąjį išteklių.

    ![Komandoje rezervuotas bendrasis išteklius](media/Resource-Management-image9.png)

2. Rodinyje **Viso komandos nariai** , stulpelyje **Ištekliaus reikalavimas** pažymėkite nuorodą, kad įtrauktumėte bendriesiems ištekliams būtinus įgūdžius.

    ![Reikalavimų nuoroda](media/Resource-Management-image10.png)

3. Pasirodžiusio puslapio **Ištekliaus reikalavimas** tinklelyje **Įgūdžiai** pasirinkite elipsę ( **...** ), o tada pažymėkite **Įtraukti naują reikalavimo charakteristiką** , kad įtrauktumėte kūrėjui būtinus įgūdžius.

    ![Komanda „Įtraukti naują reikalavimo charakteristiką“](media/Resource-Management-image11.png)

4. Pasirodžiusiame dialogo lange **Spartusis kūrimas: reikalavimo charakteristika** esančiame lauke **Charakteristika** pasirinkite būtiną įgūdį. Tada lauke **Įvertinimo reikšmė** pažymėkite šio įgūdžio kompetencijos lygį. Galiausiai lauke **Ištekliaus reikalavimas** nustatykite reikalavimą šaltinio ištekliams iš organizacijos vienetų arba net įvardytų išteklių. Baigę pasirinkite **Įrašyti**.

    ![Spartusis kūrimas: dialogo langas „Reikalavimo charakteristika“](media/Resource-Management-image12.png)

5. Puslapyje **Ištekliaus reikalavimas** pažymėkite **Rezervuoti** , kad būtų įvykdyti ištekliaus reikalavimai.

    ![Rezervavimo mygtukas puslapyje „Ištekliaus reikalavimas“](media/Resource-Management-image13.png)

    Bendrąjį išteklių taip pat galite pasirinkti tinklelyje **Visi komandos nariai** , o tada pažymėti **Rezervuoti**.

    ![Rezervavimo mygtukas virš tinklelio „Visi komandos nariai“](media/Resource-Management-image14.png)

    > [!NOTE]
    > Šiame pavyzdyje yra 40 reikiamų valandų, tačiau nėra faktinių rezervuotų valandų, nes bendrieji ištekliai neturi užsakymų. Be to, nėra priskirtų valandų, nes bendrasis išteklius buvo įtrauktas tiesiogiai į komandą. Jis nebuvo įtrauktas naudojant užduočių priskyrimą.

    Puslapyje **Planavimo pagalbinė priemonė** galite filtruoti prieinamus išteklius pagal reikalavimus, nurodytus ištekliaus reikalavime. Ištekliai rūšiuojami pagal rūšiavimo parametrus, apibrėžtus grafiko lentoje.

    ![Planavimo pagalbinės priemonės puslapis](media/Resource-Management-image15.png)

    Toliau pateikiami keli dažnai naudojami filtrai:

    - **Charakteristikos kartu su įvertinimu** – filtruoja pagal įgūdžius, sertifikatus ir kitas išteklių ypatybes bei pateikia kompetencijos įvertinimus.
    - **Vaidmenys** – filtruoja pagal rezervuojamiems ištekliams priskirtus numatytuosius vaidmenis.
    - **Organizacijos vienetai** – filtruoja rezervuojamus išteklius pagal organizacijos vienetus, kuriems jie yra priskirti.

6. Jei netenkina pradinio reikalavimo ieškos rezultatai, galite pakeisti filtro kriterijus. Kairėje pusėje išplėskite skydą **Filtro rodinys** , o tada pažymėkite **Ieškoti** , kad rastumėte papildomų išteklių.

    ![Filtro rodinio skydas](media/Resource-Management-image16.png)

7. Norėdami pakeisti rezultatų rikiavimą, pažymėkite **Rūšiuoti**.

    ![Rikiavimo komanda](media/Resource-Management-image17.png)

8. Pasirinkite išteklius pagal reikalavime nurodytą poreikį, kaip nurodyta tinklelio viršuje. Galite išvalyti tinklelio langelių žymėjimą ir palikti tą išteklių pajėgumą atvirą. Vienu metu tik vieną išteklių galima pažymėti kaip rezervuotą.

9. Pasirinkite **Rezervuoti** , kad rezervuotumėte pažymėtą išteklių ir palikite grafiko lentą atvirą, kad galėtumėte pažymėti papildomus išteklius. Arba pažymėkite **Rezervuoti ir išeiti** , kad rezervuotumėte pasirinktą išteklių ir uždarytumėte grafiko lentą.

    ![Ištekliai, skirti rezervavimui](media/Resource-Management-image19.png)

    Gaunate pranešimą apie rezervuotas valandas. Poreikio rodikliai rodo kiek rezervavimo reikalavimas yra tenkinamas ir kiek lieka. Taip pat galite matyti, kiek suvartojama pasirinkto ištekliaus pajėgumo. Pasirinkite **Išplėsti** , kad peržiūrėtumėte daugiau informacijos apie išteklių rezervavimus.

9. Grįžkite į rodinį **Visi komandos nariai**. Atkreipkite dėmesį, kad tinklelyje bendrasis išteklius pakeistas į įvardytąjį išteklių, o 40 valandos įvardytos kaip rezervuotos tam ištekliui.

    ![Atnaujintas visų komandos narių tinklelis](media/Resource-Management-image20.png)

    > [!NOTE]
    > Nerodomos paskirtos valandos, nes jos buvo rezervuotos tiesiogiai komandoje. Jos nebuvo rezervuotos naudojant užduočių priskyrimą.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Bendrųjų išteklių priskyrimas užduotims atlikti ir išteklių reikalavimams generuoti

Programoje PSA galite kurti užduotis, o tada joms priskirti bendruosius išteklius. Tokiu būdu išteklių poreikį gali pavaizduoti vietos rezervavimo ženklai, kol įvertinate savo grafiką ir finansinius skaičius. Tada galite generuoti išteklių reikalavimus, skirtus bendriesiems ištekliams ir juos vykdyti.

1. Puslapio **Projektai** skirtuke **Grafikas** pasirinkite **Įtraukti** , kad sukurtumėte užduotį.

    ![Kurti naują užduotį](media/Resource-Management-image21.png)

2. Lauke **Ištekliai** pažymėkite simbolį **Išteklių parinkiklis**. Atsiras išteklių parinkiklis ir bus rodomi esami projekto komandos nariai.

    ![Išteklių parinkiklis](media/Resource-Management-image22.png)

3. Įveskite naujo bendrojo ištekliaus pavadinimą, o tada pasirinkite **Kurti**.

    ![Įvesti naujo bendrojo ištekliaus pavadinimą](media/Resource-Management-image23.png)

4. Dialogo lange **Spartusis kūrimas: projekto komandos narys** , esančiame lauke **Vaidmuo** , pažymėkite bendrajam ištekliui skirtą vaidmenį. Lauke **Išteklių paskirstymo vienetas** pažymėkite bendrajam ištekliui skirtą organizacijos vienetą. Tada pasirinkite **Įrašyti**.

    ![Spartusis kūrimas: projekto komandos nario dialogo langas](media/Resource-Management-image24.png)

    Dabar užduotis priskirta bendrajam komandos nariui.

    ![Bendrojo komandos natio priskyrimas užduočiai](media/Resource-Management-image25.png)

    Skirtuke **Komanda** matysite naują bendrąjį komandos narį. Atkreipkite dėmesį, kad jam priskirtos tik valandos. Šios valandos yra visų užduočių, priskirtų bendrajam komandos nariui, suma. Bendrasis komandos narys dar neturi reikiamų valandų arba ištekliaus reikalavimo.

    ![Bendrasis komandos narys skirtuke „Komanda“](media/Resource-Management-image26.png)

5. Dabar galite priskirti bendrąjį komandos narį kitoms užduotims naudodami išteklių parinkiklį.

    ![Bendrasis komandos narys išteklių parinkiklyje](media/Resource-Management-image27.png)

    Baigę priskirti bendrąjį išteklių užduotims, galite generuoti bendrajam ištekliui skirtą išteklio reikalavimą.

5. Skirtuke **Komanda** pasirinkite bendrąjį išteklių, o tada pasirinkite **Generuoti reikalavimą**.

    ![Komanda „Generuoti reikalavimą“](media/Resource-Management-image28.png)

    Sugeneravus reikalavimą, bendrasis komandos narys turės reikiamas valandas ir nuorodą į ištekliaus reikalavimą.

    ![Ištekliaus reikalavimo nuoroda](media/Resource-Management-image29.png)

    Rezervavus įvardytąjį išteklių, bendrasis išteklius pašalinamas iš komandos ir pakeičiamas įvardytuoju ištekliumi.

    ![Bendrojo ištekliaus keitimas įvardytuoju ištekliumi](media/Resource-Management-image30.png)

    Skirtuke **Grafikas** bendrojo ištekliaus užduotys pašalinamos ir pakeičiamos įvardytuoju ištekliumi.

    ![Bendrojo ištekliaus užduočių keitimas įvardytuoju ištekliumi grafiko skirtuke](media/Resource-Management-image31.png)

    > [!NOTE]
    > Taip nutinka tik tada, kai nurodytas įvardytasis išteklius yra visiškai rezervuotas bendrojo ištekliaus reikalavimui. Kai įvardytasis išteklius iš dalies pakeičia bendrojo ištekliaus reikalavimą arba kai keli įvardytieji ištekliai pakeičia bendrojo ištekliaus reikalavimą, bendrasis išteklius išlieka priskirtas užduočiai.

    Šioje iliustracijoje pateikiama 80 valandų užduotis planuojama penkioms dienoms (16 valandų per dieną per penkias dienas) ir yra priskirta bendrajam ištekliui, kurio pavadinimas yra **Funkcinis**.

    ![80 valandų, penkių dienų užduotis, priskirta funkciniam bendrajam ištekliui](media/Resource-Management-image32.png)

    Kai generuojate reikalavimą, jis skirtas 80 valandų penkioms dienoms.

    ![Reikalavimas, sugeneruotas 80 valandų per penkias dienas](media/Resource-Management-image33.png)

    Kadangi prieinami ištekliai veikia tik aštuonias valandas per dieną, reikalavimui įvykdyti reikia dviejų išteklių.

    ![Antras išteklius](media/Resource-Management-image35.png)

    Skirtuke **Komanda** dabar galite matyti, kad bendrasis išteklius neturi reikiamų valandų, tačiau priskirtos valandos vis tiek rodomos kartu su dviem įvardytaisiais ištekliais, kurie įtraukti į vykdymą.

    ![Du įvardytieji ištekliai komandos skirtuke](media/Resource-Management-image36.png)

    Skirtuke **Grafikas** bendrasis išteklius lieka priskirtas užduočiai.

    ![Bendrieji ištekliai grafiko skirtuke](media/Resource-Management-image37.png)

PSA nepriskiria abiejų išteklių užduočiai, nes tai lemtų mažiau nuspėjamą grafiką. Šiame paprastame pavyzdyje nesunku po lygiai padalinti valandas tarp dviejų išteklių. Tačiau sudėtingesniais atvejais, į kuriuos įeina kelios užduotys ar keli ištekliai, PSA turėtų daryti prielaidas apie tai, kaip reikėtų paskirstyti rezervavimus, kurie gaunami keliems ištekliams keliose užduotyse.

Todėl šiais atvejais projektų vadovas yra atsakingas už kelių rezervavimų analizavimą ir jų priskyrimą pagal poreikį. Norėdamas priskirti rezervavimus, projektų vadovas priskiria užduotis iš bendrųjų išteklių įvardytiems ištekliams, o tada naudoja rodinį **Derinimas** , kad įsitikintų, jog paskirstymas veikia su rezervavimais.

### <a name="edit-a-resource-requirement"></a>Redaguoti ištekliaus reikalavimą

Sukūręs ištekliaus reikalavimą, projektų vadovas arba išteklių vadovas gali norėti redaguoti išsamią informaciją, kad patikslintų ieškos kriterijus, kai naudojama grafiko lenta. Norėdami redaguoti išteklių reikalavimą, atlikite šiuos veiksmus:

1. Puslapio **Projektai** skirtuke **Komanda** pasirinkite nuorodą bet kuriam reikalavimui, esančiam bendrajame ištekliuje.
2. Pasirodžiusiame puslapyje **Ištekliaus reikalavimas** galite atnaujinti kelis atributus. Štai keli pavyzdžiai:

    - Pavadinimas
    - Pradžios data
    - Pabaigos data
    - Trukmė
    - Išteklių tipas

Puslapyje **Ištekliaus reikalavimas** projektų vadovas arba išteklių vadovas taip pat gali apibrėžti šią informaciją:

- Įgūdžiai
- Vaidmenys
- Ištekliaus nuostatos
- Pageidaujamas organizacijos vienetas

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Atnaujinti išteklių rezervavimus po to, kai jie užrezervuoti projekte

Įtraukę bendrąjį arba įvardytąjį išteklių į projekto komandą, galite pakeisti ištekliaus rezervavimus.

1. Puslapio **Projektai** skirtuke **Komanda** pasirinkite komandos narį, o tada pažymėkite **Išlaikyti rezervavimus**.

    ![Grafiko lentos atidarymas pasirinktam komandos nariui](media/Resource-Management-image40.png)

    Atsiranda grafiko lenta ir rodomi projekto komandos nario rezervavimai. Išplėskite komandos nario įrašą, kad peržiūrėtumėte valandas, užrezervuotas pagal šį projektą, ir kitus projektus, naudojančius komandos nario pajėgumą.

2. Pažymėkite ir tempkite rezervavimą, kad jį išplėstumėte arba sumažintumėte. Atsiras dialogo langas **Kurti ištekliaus rezervavimą** , kuris leidžia koreguoti rezervavimą.

    ![Dialogo langas „Kurti išteklių rezervavimą“](media/Resource-Management-image41.png)

3. Dešiniuoju pelės klavišu spustelėkite rezervavimą. Tada galite naudoti santrumpų meniu, kad užbaigtumėte šiuos veiksmus:

    - Keisti rezervavimo būseną.
    - Redaguoti rezervavimą.
    - Pakeisti projekto komandos išteklių.

### <a name="change-the-booking-status"></a>Pakeisti rezervavimo būseną.

Galite keisti bet kurią numatytąją arba pasirinktinę rezervavimo būseną.

![Komanda „Keisti būseną“](media/Resource-Management-image42.png)

Į PSA įtrauktos šios būsenos:

- **Atšaukta** – ši būsena atšaukia ištekliaus rezervavimą ir atlaisvina ištekliaus pajėgumą.
- **Rezervuoti galutinai** – ši būsena sunaudoja ištekliaus pajėgumą. Paprastai rezervavimas turi šią būseną, kai atidarote parinktį **Išlaikyti rezervavimus** tinklelyje **Visi komandos nariai** puslapyje **Projektai**.
- **Rezervuoti preliminariai** – ši būsena įtraukia išteklių į komandą, tačiau nenaudoja ištekliaus pajėgumo. Ši būsena nurodo, kad išteklius buvo rezervuotas galimam darbui, bet vis tiek turi pajėgumo, jei jo reikia kitoms užduotims. Peržiūrėjus bendro ištekliaus pasiekiamumą, preliminarūs rezervavimai turi skirtingą būseną nei galutiniai rezervavimai.
- **Siūloma** – ši būsena rodo išteklių vadovo arba projekto vadovo pasiūlymą ištekliui. Pasiūlymai nenaudoja ištekliaus pajėgumo, o išteklius neįtraukiamas į projekto komandą. Norėdami galutinai rezervuoti išteklių komandoje, projekto vadomas turi priimti pasiūlymą.

### <a name="submit-resource-requests"></a>Išteklių užklausų teikimas

Išteklių užklausos naudojamos poreikiui, kurį turi įvykdyti išteklių vadovas, vykdyti (ištekliaus reikalavimas). Jei tai bendras išteklius, kuris jau yra komandoje, galite ištekliaus užklausą galite pateikti tiesiogiai. Ištekliaus užklausą galima įvykdyti dviem būdais:

- Išteklių vadovas tiesiogiai įvykdo užklausą. Šiuo atveju bendrasis išteklius pakeičiamas galutiniu rezervavimu, į kurį įeina įvardytasis išteklius.
- Išteklių vadovas siūlo išteklių projektų vadovui, o projektų vadovas patvirtina arba atmeta siūlomą išteklių.

#### <a name="direct-fulfillment-of-resource-requests"></a>Tiesioginis išteklių prašymų vykdymas

Sugeneravus išteklių reikalavimą, projektų vadovas gali pateikti ištekliaus užklausą bendriesiems ištekliams, pažymėdamas išteklių, o tada pasirinkdamas **Pateikti užklausą**.

![Pateikti užklausą](media/Resource-Management-image45.png)

Pastabas apie išteklius galima pateikti išteklių vadovui, kuris vykdo užklausą. Pateikus prašymą, komandos nariui skirtas laukas **Būsena** pakeičiamas į **Pateikta**.

![Įvesti pasirinktinius komentarus](media/Resource-Management-image46.png)

Projektų vadovui įvykdžius užklausą, bendrasis komandos narys pakeičiamas įvardytuoju ištekliumi tinklelyje **Visi komandos nariai**.

![Bendrojo komandos nario keitimas įvardytuoju ištekliumi tinklelyje „Visi komandos nariai“](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Išteklių pasiūlymas išteklių užklausoms

Užuot tiesiogiai rezervuodamas išteklius išteklių užklausoje, išteklių vadovas gali siūlyti išteklių projektų vadovui. Išteklių vadovas gali naudoti šią parinktį, kai nėra tikslaus reikalavimų atitikimo. Išteklių vadovui pasiūlius išteklių, projektų vadovas mato, kad bendrajam komandos nariui skirtas laukas **Būsena** pakeičiamas į **Reikia peržiūrėti**.

![Bendrosios komandos nario būsenos pasikeitimas į „Reikia peržiūrėti“](media/Resource-Management-image48.png)

Norėdami peržiūrėti siūlomą išteklių ir pasiūlymo rezervavimo efekto vizualizavimą, dukart spustelėkite komandos narį, kurio būsena yra **Reikia peržiūrėti**. Tada pasirinkite skirtuką **Siūlomi ištekliai**.

![Siūlomi ištekliai](media/Resource-Management-image49.png)

Pasirinkite **Priimti visus pasiūlymus** , kad priimtumėte visus siūlomus išteklius arba **Atmesti visus pasiūlymus** , kad juos atmestumėte. Jei priimate siūlomus išteklius, jie yra galutinai rezervuojami projekte kaip komandos nariai ir pakeičia bendruosius išteklius.

> [!NOTE]
> Turite priimti arba atmesti visus siūlomus išteklius. Negalite jų priimti arba atmesti iš dalies.

### <a name="substitute-a-resource-on-the-project-team"></a>Pakeiskite išteklių projekto komandoje

Kartais projekto vadovas projekte turi pakeisti rezervuotos komandos narį.

1. Puslapio **Projektai** skirtuke **Komanda** pažymėkite išteklių, kurį reikia pakeisti, o tada pasirinkite **Išlaikyti rezervavimus**.
2. Išplėskite išteklių, kad peržiūrėtumėte projektus, kuriems jis priskirtas.

    ![Išplėstas išteklius priskirtiems projektams rodyti](media/Resource-Management-image50.png)

3. Dešiniuoju pelės mygtuku spustelėkite projektą, o tada pažymėkite **Pakeisti išteklius**.
4. Jei žinote išteklių, kurį norite pakeisti dabartiniu ištekliumi, pažymėkite arba įveskite pavadinimą, o tada pasirinkite **Iš naujo priskirti**.

    ![Pakaitinio ištekliaus nurodymas](media/Resource-Management-image51.png)

    Taip pat galite atlikti šiuos veiksmus, kad ieškotumėte ištekliaus:

    1. Pažymėkite **Rasti pakaitalą**.

        ![Pakaitinio ištekliaus paieška](media/Resource-Management-image52.png)

        Planavimo pagalbinė priemonė pateikia galimų pakaitų sąrašą. Planavimo pagalbinėje priemonėje galite toliau filtruoti galimus išteklius, kad rastumėte tinkamą pakaitą.

        ![Galimų pakaitų sąrašas](media/Resource-Management-image53.png)

    2. Norėdami pakeisti išteklių, pasirinkite norimą išteklių ir pažymėkite **Pakeisti**.

        ![Pakeisti pasirinktus išteklius](media/Resource-Management-image54.png)

    Rezervavimai ir priskyrimai pakeičiami naujais ištekliais.

    ![Rezervavimų ir priskyrimų keitimas naujais ištekliais](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Komandos narių rezervavimų ir priskyrimų derinimas

Komandos nariams rezervavimai ir priskyrimai yra laisvai susiję. Kitaip tariant, ištekliai gali turėti priskyrimų, bet ne rezervavimų, arba jie gali turėti rezervavimų, bet ne priskyrimų. Geriausiu atveju rezervavimai ir priskyrimai turėtų būti suderinti, kad ištekliai turėtų patvirtintą pajėgumą užduočių priskyrimams atlikti. Tačiau rezervavimai gali būti pagrįsti prieinamumu, o užduoties laikas gali keistis projektui tęsiantis. Todėl laisvas rezervavimų ir priskyrimų siejimas suteikia lankstumą.

PSA turi skirtuką **Derinimas** , kuris leidžia projektų vadovams derinti komandos narių rezervavimus ir priskyrimus projekto komandoms.

![Derinimas](media/Resource-Management-image56.png)

Skirtuke **Derinimas** rodomi rezervavimai ir priskyrimai iki atskiro kiekvieno komandos nario užduoties priskyrimo lygio. Skirtuke rodomos langeliuose nurodytos valandos, kurios nurodo laikotarpius nuo mėnesių iki dienų.

Skirtuke taip pat rodoma bendra grynoji projekto suma kartu su stulpeliu „Iš viso“.

Kiekvienam ištekliui skirtukas apskaičiuoja skirtumą tarp komandos narių rezervavimų ir komandos nario užduočių priskyrimo apibendrinamosios reikšmės. Geriausiu atveju šis skirtumas turi būti 0 (nulis). Kitaip tariant, tarp rezervavimų ir priskyrimų neturėtų būti skirtumo. Skirtumai nuspalvinami ir nušešėliuojami, kad atkreiptų dėmesį į dvi sąlygas:

- **Rezervavimo trūkumas** – rezervavimo trūkumas atsiranda, kai išteklius turi daugiau priskyrimų nei rezervavimų. Kadangi šis pajėgumas nebuvo rezervuotas, projektų vadovas gali pataisyti šią sąlygą išplėsdamas ištekliaus rezervavimus, kad padengtų trūkumą.
- **Užsakymų perteklius** – užsakymų perteklius įvyksta, kai ištekliai buvo rezervuoti projektui, tačiau nebuvo priskirti užduotims. Ši sąlyga gali būti priimtina tais atvejais, kai išteklius buvo užrezervuotas projektui prieš užduoties priskyrimą. Tačiau kitais atvejais išteklius neplanuojamas priskirti užduotims. Tokiais atvejais projektų vadovas turėtų apsvarstyti išteklių rezervavimo atšaukimą, kad pajėgumą būtų galima naudoti kitam projektui.

Kai kuriais atvejais, peržiūrint laiką aukštesniame nei dienos lygyje (pavyzdžiui, mėnesio lygyje), galite matyti ištekliaus grynąjį nulio skirtumą (kitaip tariant, rezervavimai = priskyrimai). Tačiau, jei peržiūrite laiką savaitės lygyje, galite matyti nulio valandų priskyrimus ir 40 valandų rezervavimus pirmoje savaitėje, tačiau 40 valandų priskyrimus ir nulio valandų rezervavimus antroje savaitėje. Apskritai rezervavimai ir priskyrimai yra suderinami, tačiau kiekvieną savaitę jie skiriasi.

Peržiūrint laiką aukštesniuose lygiuose, langeliai, esantys skirtuke **Derinimas** , turi indikatorių, kuris praneša, kad žemesniuose lygiuose yra skirtumų. Dukart spustelėję langelį galite priartinti ir peržiūrėti skirtumą. Tada galite spustelėti dešiniuoju pelės mygtuku ir nutolinti. Pažymėdami išteklių, o tada naudodami valdiklį **Kitas skirtumas** , esantį tinklelio įrankių juostoje, galite eiti į kitą skirtumą tarp šio ištekliaus rezervavimų ir priskyrimų. Tada galite naudoti valdiklį **Ankstesnis skirtumas** , kad grįžtumėte atgal. Taip pat galite išjungti skirtumo indikatorių ir naršymą **Parametruose**.

![Skirtumo indikatorius](media/Resource-Management-image57.png)

Jei turite ištekliaus užduoties priskyrimus, bet ne rezervavimus, puslapio **Projektai** skirtuke **Derinimas** pažymėkite rezervavimo trūkumą, o tada pasirinkite **Išplėsti rezervavimą**. Atsiranda dialogo langas **Išplėsti rezervavimą** ir rodomas rezervavimas, reikalingas ištekliaus trūkumui spręsti. Jame taip pat nurodomi esami ištekliaus rezervavimai visuose projektuose arba kituose planiniuose objektuose. Jei pasirinksite **Gerai** , kad sukurtumėte ištekliaus rezervavimą, neatsižvelgiant į ištekliaus pasiekiamumą, galite viršyti rezervavimo limitą.

![Dialogo langas „Išplėsti rezervavimą“](media/Resource-Management-image58.png)

Projektų vadovas arba išteklių vadovas gali naudoti grafiko lentą, kad valdytų situacijas, kai išteklius rezervuojamas per daug nepaisant jo pajėgumo.
