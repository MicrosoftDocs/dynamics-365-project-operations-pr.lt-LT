---
title: Komandos narių įtraukimas iš komandos narių tinklelio
description: Šioje temoje pateikiama informacija apie tai, kaip galite tvarkyti komandos nario išteklius.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c4ff7792a9a99cbbe791a10dbc5157ffd51de285c02f23471532a09e7a55b031
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008416"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Komandos narių įtraukimas iš komandos narių tinklelio

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Į „Dynamics 365 Project Operations“ įeina išteklių vadovo ataskaitų sritis, teikianti vaizdinį išteklių poreikio ir naudojimo visoje organizacijoje apžvalgą. Šioje ataskaitų srityje galite naudoti diagramas, kad galėtumėte vizualizuoti šią informaciją:

- **Išteklių poreikis**: diagramoje **Aktyvių išteklių užklausa** rodomi pateikti ištekliai. Ištekliai yra agreguojami pagal vaidmenį arba projektą.
- **Nepateiktų išteklių poreikis**: diagramoje **Nepriskirtų išteklių poreikis** rodomi visi nepateikti išteklių reikalavimai. Ši diagrama padeda išteklių vadovams peržiūrėti poreikį, kuris nėra patvirtintas ir gali būti pateiktas naudojant išteklių užklausą.
- **Apmokėtinas naudojimas per paskutinę savaitę**: diagramoje **Naudojimas pagal vaidmenį** rodoma organizacijos faktinio apmokamo naudojimo pagal vaidmenį procentinė dalis lyginant su tiksliniu apmokėtinu naudojimu pagal vaidmenį.

    > [!NOTE]
    > Norėdami pasiekti diagramą **Naudojimas pagal vaidmenį**, sukurkite užduotį, kuri vykdo darbo eigą **UpdateRoleUtilization**. Ši pasikartojanti užduotis vykdoma kas septynias dienas, kad apskaičiuotų apmokėtiną realizavimą per ankstesnes septynias dienas. Rezultatai sujungiami pagal vaidmenį.

## <a name="manage-project-team-members"></a>Projekto komandos narių valdymas

Projektų vadovai gali naudoti išteklių vadovo ataskaitų sritį, kad valdytų projektų išteklius. Pavyzdžiui, jie gali įtraukti komandos narį tiesiogiai į projektą ir rezervuoti komandos narį vykdyti išteklių reikalavimus, kurie buvo užfiksuoti bendrųjų išteklių.

### <a name="add-a-team-member-directly-to-a-project"></a>Komandos nario įtraukimas tiesiogiai į projektą

Norėdami įtraukti komandos narį tiesiogiai į projektą, formoje **Projektai**, esančioje skirtuke **Komanda**, pasirinkite **Naujas**. Atsiras dialogo langas **Spartusis kūrimas: projekto komandos narys**. Šiame dialogo lange galite atlikti šias užduotis:

- **Rezervuokite įvardytuosius išteklius**: lauke **Rezervuojami ištekliai** pasirinkite ištekliaus pavadinimą. Tada pažymėkite vaidmenį, nustatykite laikotarpį ir pažymėkite paskirstymo metodą. Jūsų pažymėtas įvardytas išteklius įtraukiamas į projektą naudojant pasirinktą paskirstymo metodą ir išteklių kalendorių.
- **Įtraukite bendrąjį išteklių**: palikite lauką **Rezervuojami ištekliai** tuščią, o tada pažymėkite vaidmenį, nustatykite laikotarpį ir pažymėkite pageidaujamą paskirstymo metodą. Bendrasis išteklius įtraukiamas į komandą kaip vietos rezervavimo ženklas. Vietos rezervavimo ženklas turi poreikio modelį, naudojamą komandos įvardytiesiems ištekliams rezervuoti. Reikalavimas pateikiamas pagal projekto kalendorių.
- **Įtraukite įvardytąjį išteklių į komandą nenaudojant išteklių pajėgumo**: lauke **Rezervuojami ištekliai** pažymėkite išteklių. Pasirinkite laikotarpį, o tada pažymėkite **Nėra** kaip paskirstymo metodą. Išteklius įtraukiamas į komandą, tačiau ištekliaus pajėgumas užsakyme nenaudojamas.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Užsakykite komandos narį, kad būtų galima vykdyti išteklių reikalavimus bendriesiems ištekliams

Naudodami „Project Operations“ galite užsakyti bendrąjį išteklių projekto komandai. Taip pat galite nurodyti vaidmenį, reikalingą pajėgumą ir tai, kaip tas pajėgumas platinamas. Išteklių reikalavimams galite nurodyti su bendruoju ištekliumi susietus atributus. Į šiuos atributus įtraukti būtini įgūdžiai, pageidaujamas organizacijos vienetas ir pageidautini ištekliai.

Atlikite šiuos veiksmus, kad nustatytumėte bendrųjų išteklių kūrėjams būtinus įgūdžius.

1. Formoje **Projektai**, esančioje skirtuke **Komanda**, pažymėkite **Naujas**, kad rezervuotumėte bendrąjį išteklių.
2. Rodinyje **Viso komandos nariai**, stulpelyje **Ištekliaus reikalavimas** pažymėkite nuorodą, kad įtrauktumėte bendriesiems ištekliams būtinus įgūdžius.
3. Formoje **Ištekliaus reikalavimas**, esančioje tinklelyje **Įgūdžiai**, pasirinkite elipsę (**...**), o tada pažymėkite **Įtraukti naują reikalavimo charakteristiką**, kad įtrauktumėte kūrėjui būtinus įgūdžius.
4. Dialogo lange **Spartusis kūrimas: reikalavimo charakteristika**, esančiame lauke **Charakteristika**, pasirinkite būtiną įgūdį.
5. Lauke **Įvertinimo reikšmė** pažymėkite šio įgūdžio kompetencijos lygį. 
6. Lauke **Ištekliaus reikalavimas** nustatykite reikalavimą šaltinio ištekliams iš organizacijos vienetų arba net įvardytų išteklių. Baigę pasirinkite **Įrašyti**.
7. Formoje **Ištekliaus reikalavimas** pažymėkite **Rezervuoti**, kad būtų įvykdyti ištekliaus reikalavimai. Bendrąjį išteklių taip pat galite pasirinkti tinklelyje **Visi komandos nariai**, o tada pažymėti **Rezervuoti**.

    > [!NOTE]
    > Šiame pavyzdyje yra 40 reikiamų valandų, tačiau nėra faktinių rezervuotų valandų, nes bendrieji ištekliai neturi užsakymų. Be to, nėra priskirtų valandų, nes bendrasis išteklius buvo įtrauktas tiesiogiai į komandą, o ne įtrauktas naudojant užduoties priskyrimą.

    Formoje **Planavimo pagalbinė priemonė** galite filtruoti prieinamus išteklius pagal reikalavimus, nurodytus ištekliaus reikalavime. Ištekliai rūšiuojami pagal rūšiavimo parametrus, apibrėžtus grafiko lentoje.

   Kai kurie dažniausiai naudojami filtrai:

    - **Charakteristikos kartu su įvertinimu**: filtruokite pagal įgūdžius, sertifikatus ir kitas išteklių ypatybes bei pateikite kompetencijos įvertinimus.
    - **Vaidmenys**: filtruokite pagal rezervuojamiems ištekliams priskirtus numatytuosius vaidmenis.
    - **Organizacijos vienetai**: filtruokite rezervuojamus išteklius pagal organizacijos vienetus, kuriems jie yra priskirti.

8. Jei netenkina pradinio reikalavimo ieškos rezultatai, galite pakeisti filtro kriterijus. Kairėje pusėje išplėskite skydą **Filtro rodinys**, o tada pažymėkite **Ieškoti**, kad rastumėte papildomų išteklių. Norėdami pakeisti rezultatų rikiavimą, pažymėkite **Rūšiuoti**.
9. Pasirinkite išteklius pagal reikalavime nurodytą poreikį, kaip nurodyta tinklelio viršuje. Galite išvalyti tinklelio langelių žymėjimą ir palikti tą išteklių pajėgumą atvirą. Vienu metu tik vieną išteklių galima pažymėti kaip rezervuotą.
10. Pasirinkite **Rezervuoti**, kad rezervuotumėte pažymėtą išteklių ir palikite grafiko lentą atvirą, kad galėtumėte pažymėti papildomus išteklius. Arba pažymėkite **Rezervuoti ir išeiti**, kad rezervuotumėte pasirinktą išteklių ir uždarytumėte grafiko lentą.
11. Grįžkite į rodinį **Visi komandos nariai**. Atkreipkite dėmesį, kad tinklelyje bendrasis išteklius pakeistas į įvardytąjį išteklių, o 40 valandos įvardytos kaip rezervuotos tam ištekliui.

    > [!NOTE]
    > Nerodomos paskirtos valandos, nes jos buvo rezervuotos tiesiogiai komandoje. Jos nebuvo rezervuotos naudojant užduočių priskyrimą.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Bendrųjų išteklių priskyrimas užduotims atlikti ir išteklių reikalavimams generuoti

Programoje „Project Operations“ galite kurti užduotis, o tada joms priskirti bendruosius išteklius. Išteklių poreikį galite pavaizduoti vietos rezervavimo ženklais, kol įvertinate savo grafiką ir finansinius skaičius. Tada galite generuoti išteklių reikalavimus, skirtus bendriesiems ištekliams ir juos vykdyti.

1. Formoje **Projektai**, esančioje skirtuke **Grafikas**, pasirinkite **Įtraukti**, kad sukurtumėte užduotį.
2. Lauke **Ištekliai** pažymėkite simbolį **Išteklių parinkiklis**. Atsiras išteklių parinkiklis ir bus rodomi esami projekto komandos nariai.
3. Įveskite naujo bendrojo ištekliaus pavadinimą, o tada pasirinkite **Kurti**.
4. Dialogo lange **Spartusis kūrimas: projekto komandos narys**, esančiame lauke **Vaidmuo**, pažymėkite bendrajam ištekliui skirtą vaidmenį. 
5. Lauke **Išteklių paskirstymo vienetas** pažymėkite bendrajam ištekliui skirtą organizacijos vienetą. Tada pasirinkite **Įrašyti**. Dabar užduotis priskirta bendrajam komandos nariui.

   Skirtuke **Komanda** matysite naują bendrąjį komandos narį. Atkreipkite dėmesį, kad jam priskirtos tik valandos. Šios valandos yra visų užduočių, priskirtų bendrajam komandos nariui, suma. Bendrasis komandos narys neturi reikiamų valandų arba ištekliaus reikalavimo.

6. Dabar galite priskirti bendrąjį komandos narį kitoms užduotims naudodami išteklių parinkiklį.

   Baigę priskirti bendrąjį išteklių užduotims, galite generuoti bendrajam ištekliui skirtą išteklio reikalavimą.

7. Skirtuke **Komanda** pasirinkite bendrąjį išteklių, o tada pasirinkite **Generuoti reikalavimą**. Sugeneravus reikalavimą, bendrasis komandos narys turės reikiamas valandas ir nuorodą į ištekliaus reikalavimą.

  Rezervavus įvardytąjį išteklių, bendrasis išteklius pašalinamas iš komandos ir pakeičiamas įvardytuoju ištekliumi. Skirtuke **Grafikas** bendrojo ištekliaus užduotys pašalinamos ir pakeičiamos įvardytuoju ištekliumi.

  > [!NOTE]
  > Taip nutinka tik tada, kai nurodytas įvardytasis išteklius yra visiškai rezervuotas bendrojo ištekliaus reikalavimui. Kai įvardytasis išteklius iš dalies pakeičia bendrojo ištekliaus reikalavimą arba kai keli įvardytieji ištekliai pakeičia bendrojo ištekliaus reikalavimą, bendrasis išteklius išlieka priskirtas užduočiai.

„Project Operations“ nepriskiria abiejų išteklių užduočiai, nes tai lemtų mažiau nuspėjamą grafiką. Šiame paprastame pavyzdyje nesunku po lygiai padalinti valandas tarp dviejų išteklių. Tačiau sudėtingesniais atvejais, į kuriuos įeina kelios užduotys ar keli ištekliai, PSA turėtų daryti prielaidas apie tai, kaip reikėtų paskirstyti rezervavimus, kurie gaunami keliems ištekliams keliose užduotyse.

Todėl šiais atvejais projektų vadovas yra atsakingas už kelių rezervavimų analizavimą ir jų priskyrimą pagal poreikį. Norėdamas priskirti rezervavimus, projektų vadovas priskiria užduotis iš bendrųjų išteklių įvardytiems ištekliams, o tada naudoja rodinį **Derinimas**, kad įsitikintų, jog paskirstymas veikia su rezervavimais.

### <a name="edit-a-resource-requirement"></a>Redaguoti ištekliaus reikalavimą

Sukūręs ištekliaus reikalavimą, projektų vadovas arba išteklių vadovas gali redaguoti išsamią informaciją, kad patikslintų ieškos kriterijus, kai naudojama grafiko lenta. Norėdami redaguoti išteklių reikalavimą, atlikite šiuos veiksmus:

1. Formoj **Projektai**, esančioje skirtuke **Komanda** pasirinkite nuorodą bet kuriam reikalavimui, esančiam bendrajame ištekliuje.
2. Atsiradusioje formoje **Išteklių reikalavimas** įveskite reikiamą lauko informaciją

   Formoje **Išteklių reikalavimas** projektų vadovas arba išteklių vadovas taip pat gali apibrėžti įgūdžius, vaidmenis, išteklių prioritetus ir pageidaujamą organizacijos vienetą.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Atnaujinti išteklių rezervavimus po to, kai jie užrezervuoti projekte

Įtraukę bendrąjį arba įvardytąjį išteklių į projekto komandą, galite pakeisti ištekliaus rezervavimus.

1. Formoje **Projektai**, esančioje skirtuke **Komanda**, pasirinkite komandos narį, o tada pažymėkite **Išlaikyti rezervavimus**.
 
   Atsiranda grafiko lenta ir rodomi projekto komandos nario rezervavimai. Išplėskite komandos nario įrašą, kad peržiūrėtumėte valandas, užrezervuotas pagal šį projektą, ir kitus projektus, naudojančius komandos nario pajėgumą.

2. Pažymėkite ir tempkite rezervavimą, kad jį išplėstumėte arba sumažintumėte. Atsiras dialogo langas **Kurti ištekliaus rezervavimą**, kuris leidžia koreguoti rezervavimą.
3. Dešiniuoju pelės klavišu spustelėkite rezervavimą. Tada galite naudoti santrumpų meniu, kad užbaigtumėte šiuos veiksmus:

    - Pakeisti rezervavimo būseną.
    - Rezervavimo redagavimas
    - Pakeiskite išteklių projekto komandoje

### <a name="change-the-booking-status"></a>Pakeisti rezervavimo būseną.

Galite keisti bet kurią numatytąją arba pasirinktinę rezervavimo būseną.

Į „Project Operations“ įtrauktos šios būsenos:

- **Atšaukta**: ši būsena atšaukia ištekliaus rezervavimą ir atlaisvina ištekliaus pajėgumą.
- **Galutinė rezervacija**: sunaudoja ištekliaus pajėgumą. Paprastai rezervavimas turi šią būseną, kai atidarote parinktį **Išlaikyti rezervavimus** tinklelyje **Visi komandos nariai**, esančiame formoje **Projektai**.
- **Preliminari rezervacija**: įtraukia išteklių į komandą, tačiau nenaudoja ištekliaus pajėgumo. Ši būsena nurodo, kad išteklius buvo rezervuotas galimam darbui, bet vis tiek turi pajėgumo, jei jo reikia kitoms užduotims. Peržiūrėjus bendro ištekliaus pasiekiamumą, preliminarūs rezervavimai turi skirtingą būseną nei galutiniai rezervavimai.
- **Siūloma**: ši būsena rodo išteklių vadovo arba projekto vadovo pasiūlymą ištekliui. Pasiūlymai nenaudoja ištekliaus pajėgumo, o išteklius neįtraukiamas į projekto komandą. Norėdami galutinai rezervuoti išteklių komandoje, projekto vadovas turi priimti pasiūlymą.

### <a name="submit-resource-requests"></a>Išteklių užklausų pateikimas

Išteklių užklausos naudojamos poreikiui ar ištekliaus reikalavimui, kurį turi atlikti išteklių vadovas, vykdyti. Jei tai bendras išteklius, kuris jau yra komandoje, galite ištekliaus užklausą galite pateikti tiesiogiai. Ištekliaus užklausą galima įvykdyti dviem būdais:

- Išteklių vadovas tiesiogiai įvykdo užklausą. Šiuo atveju bendrasis išteklius pakeičiamas galutiniu rezervavimu, į kurį įeina įvardytasis išteklius.
- Išteklių vadovas siūlo išteklių projektų vadovui, o projektų vadovas patvirtina arba atmeta siūlomą išteklių.

#### <a name="direct-fulfillment-of-resource-requests"></a>Tiesioginis išteklių prašymų vykdymas

Sugeneravus išteklių reikalavimą, projektų vadovas gali pateikti ištekliaus užklausą bendriesiems ištekliams, pažymėdamas išteklių, o tada pasirinkdamas **Pateikti užklausą**. Pastabas apie išteklius galima pateikti išteklių vadovui, kuris vykdo užklausą. Pateikus prašymą, komandos nariui skirtas laukas **Būsena** pakeičiamas į **Pateikta**. Projektų vadovui įvykdžius užklausą, bendrasis komandos narys pakeičiamas įvardytuoju ištekliumi tinklelyje **Visi komandos nariai**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Išteklių pasiūlymas išteklių užklausoms

Užuot tiesiogiai rezervuodamas išteklius išteklių užklausoje, išteklių vadovas gali siūlyti išteklių projektų vadovui. Išteklių vadovas gali naudoti šią parinktį, kai nėra tikslaus reikalavimų atitikimo. Išteklių vadovui pasiūlius išteklių, projektų vadovas mato, kad bendrajam komandos nariui skirtas laukas **Būsena** pakeičiamas į **Reikia peržiūrėti**.

Galite peržiūrėti siūlomą išteklių ir pasiūlymo rezervavimo poveikio vizualizavimą. 

1. Du kartus spustelėkite komandos narį, kurio būsena yra **Reikia peržiūrėti**. 
2. Pasirinkite skirtuką **Siūlomi ištekliai**.
3. Pasirinkite **Priimti visus pasiūlymus**, kad priimtumėte visus siūlomus išteklius arba **Atmesti visus pasiūlymus**, kad juos atmestumėte. Jei priimate siūlomus išteklius, jie yra galutinai rezervuojami projekte kaip komandos nariai ir pakeičia bendruosius išteklius.

> [!NOTE]
> Turite priimti arba atmesti visus siūlomus išteklius. Negalite jų priimti arba atmesti iš dalies.

### <a name="substitute-a-resource-on-the-project-team"></a>Pakeiskite išteklių projekto komandoje

Kartais projekto vadovas projekte turi pakeisti rezervuotos komandos narį.

1. Formoje **Projektai**, esančioje skirtuke **Komanda**, pažymėkite išteklių, kurį reikia pakeisti, o tada pasirinkite **Išlaikyti rezervavimus**.
2. Išplėskite išteklių, kad peržiūrėtumėte projektus, kuriems jis priskirtas.
3. Dešiniuoju pelės mygtuku spustelėkite projektą, o tada pažymėkite **Pakeisti išteklius**.
4. Jei žinote išteklių, kuriuo norite pakeisti dabartinį išteklių, pažymėkite arba įveskite pavadinimą, o tada pasirinkite **Iš naujo priskirti**.

Arba jei norite ieškoti ištekliaus, atlikite toliau nurodytus veiksmus.

1. Pažymėkite **Rasti pakaitalą**.

   Planavimo pagalbinė priemonė pateikia galimų pakaitų sąrašą. Planavimo pagalbinėje priemonėje galite toliau filtruoti galimus išteklius, kad rastumėte tinkamą pakaitą.

2. Norėdami pakeisti išteklių, pasirinkite norimą išteklių ir pažymėkite **Pakeisti**.   

   Rezervavimai ir priskyrimai pakeičiami naujais ištekliais.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Komandos narių rezervavimų ir priskyrimų derinimas

Komandos nariams rezervavimai ir priskyrimai yra laisvai susiję. Kitaip tariant, ištekliai gali turėti priskyrimų, bet ne rezervavimų, arba jie gali turėti rezervavimų, bet ne priskyrimų. Geriausiu atveju rezervavimai ir priskyrimai turėtų būti suderinti, kad ištekliai turėtų patvirtintą pajėgumą užduočių priskyrimams atlikti. Tačiau rezervavimai gali būti pagrįsti prieinamumu, o užduoties laikas gali keistis projektui tęsiantis. Todėl laisvas rezervavimų ir priskyrimų siejimas suteikia lankstumą.

„Project Operations“ turi skirtuką **Derinimas**, kuris leidžia projektų vadovams derinti komandos narių rezervavimus ir priskyrimus projekto komandoms.

Skirtuke **Derinimas** rodomi rezervavimai ir priskyrimai iki atskiro kiekvieno komandos nario užduoties priskyrimo lygio. Skirtuke rodomos langeliuose nurodytos valandos, kurios nurodo laikotarpius nuo mėnesių iki dienų.

Skirtuke taip pat rodoma bendra grynoji projekto suma kartu su stulpeliu „Iš viso“.

Kiekvienam ištekliui skirtukas apskaičiuoja skirtumą tarp komandos narių rezervavimų ir komandos nario užduočių priskyrimo apibendrinamosios reikšmės. Geriausiu atveju šis skirtumas turi būti 0 (nulis). Kitaip tariant, tarp rezervavimų ir priskyrimų neturėtų būti skirtumo. Skirtumai nuspalvinami ir nušešėliuojami, kad atkreiptų dėmesį į dvi sąlygas:

- **Rezervavimo trūkumas**: atsiranda tada, kai išteklius turi daugiau priskyrimų nei rezervavimų. Kadangi šis pajėgumas nebuvo rezervuotas, projektų vadovas gali pataisyti šią sąlygą išplėsdamas ištekliaus rezervavimus, kad padengtų trūkumą.
- **Užsakymų perteklius**: įvyksta, kai ištekliai buvo rezervuoti projektui, tačiau nebuvo priskirti užduotims. Ši sąlyga gali būti priimtina tais atvejais, kai išteklius buvo užrezervuotas projektui prieš užduoties priskyrimą. Tačiau kitais atvejais išteklius neplanuojamas priskirti užduotims. Tokiais atvejais projektų vadovas turėtų apsvarstyti išteklių rezervavimo atšaukimą, kad pajėgumą būtų galima naudoti kitam projektui.

Kai kuriais atvejais, peržiūrint laiką aukštesniame nei dienos lygyje, pavyzdžiui, mėnesio lygyje, galite matyti ištekliaus grynąjį nulio skirtumą. Kitaip tariant, užsakymai = priskyrimai. Tačiau, jei peržiūrite laiką savaitės lygyje, galite matyti nulio valandų priskyrimus ir 40 valandų rezervavimus pirmoje savaitėje, tačiau 40 valandų priskyrimus ir nulio valandų rezervavimus antroje savaitėje. Apskritai rezervavimai ir priskyrimai yra suderinami, tačiau kiekvieną savaitę jie skiriasi.

Peržiūrint laiką aukštesniuose lygiuose, langeliai, esantys skirtuke **Derinimas**, turi indikatorių, kuris praneša, kad žemesniuose lygiuose yra skirtumų. Dukart spustelėkite langelį, kad priartintumėte ir peržiūrėtumėte skirtumą. Tada galite spustelėti dešiniuoju pelės mygtuku ir nutolinti. Pažymėdami išteklių, o tada pasirinkdami tinklelio įrankių juostoje esantį valdiklį **Kitas skirtumas**, galite eiti į kitą skirtumą tarp šio ištekliaus rezervavimų ir priskyrimų. Pažymėkite **Ankstesnis skirtumas** ir grįžkite atgal. Taip pat galite išjungti skirtumo indikatorių ir naršymą **Parametruose**.

Jei turite ištekliaus užduoties priskyrimus, bet ne rezervavimus, formoje **Projektai**, esančioje skirtuke **Derinimas**, pažymėkite rezervavimo trūkumą, o tada pasirinkite **Išplėsti rezervavimą**. Atsiranda dialogo langas **Išplėsti rezervavimą** ir rodomas rezervavimas, reikalingas ištekliaus trūkumui spręsti. Dialogo lange taip pat nurodomi esami ištekliaus rezervavimai visuose projektuose arba kituose planiniuose objektuose. Jei pasirinksite **Gerai**, kad sukurtumėte ištekliaus rezervavimą, neatsižvelgiant į ištekliaus pasiekiamumą, galite viršyti rezervavimo limitą.

Projektų vadovas arba išteklių vadovas gali naudoti grafiko lentą, kad valdytų situacijas, kai išteklius rezervuojamas per daug nepaisant jo pajėgumo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]