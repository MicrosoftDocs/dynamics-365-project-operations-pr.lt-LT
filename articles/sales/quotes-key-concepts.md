---
title: Pasiūlymai – pagrindinės sąvokos
description: Šioje temoje pateikta informacija apie projektų ir pardavimų pasiūlymus, prieinamus programoje „Project Operations“.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 899279b33f4fe8780d110d7c18a097407bd8d839
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277528"
---
# <a name="quotes---key-concepts"></a>Pasiūlymai – pagrindinės sąvokos

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Programoje „Dynamics 365 Project Operations“ naudojami dviejų tipų pasiūlymai: projekto pasiūlymai ir pardavimo pasiūlymai. Šių pasiūlymų dviejų tipų skirtumai išvardyti toliau.

- **Tinkleliai eilutės elementams**: pardavimo pasiūlymuose yra tik vienas tinklelis eilutės elementams. Projekto pasiūlyme yra du eilučių elementų tinkleliai. Vienas tinklelis skirtas projektų eilutėms, o kitas – produktų eilutėms.
- **Aktyvinimas ir peržiūrėjimas** – pardavimo pasiūlymus galima aktyvuoti ir peržiūrėti. Šie procesai nepalaikomi projekto pasiūlyme.
- **Pridėti užsakymai** – į pardavimo pasiūlymą galima įtraukti keletą užsakymų. Į projekto pasiūlymą galima įtraukti tik vieną projekto sutartį.
- **Pasiūlymo laimėjimas** – kai laimite pardavimo pasiūlymą, susijusi galimybė gali likti atvira. Laimėjus projekto pasiūlymą, susijusi galimybė uždaroma.
- **Laukai ir sąvokos** – pardavimo pasiūlyme nėra kai kurių laukų ir sąvokų, įtrauktų į projekto pasiūlymą. Šie laukai yra **Sutartį pasirašantis vienetas**, **Klientų vadybininkas** ir **Sąskaitų gavėjo kontakto vardas**.  
- **Tipas** – pardavimo pasiūlymai ir projekto pasiūlymai taip pat identifikuojami pagal parinkčių rinkiniu grindžiamą lauką **Tipas**. Pardavimo pasiūlyme šio lauko reikšmė yra **Pagrįstas prekėmis**. Projekto pasiūlyme jo reikšmė yra **Pagrįstas darbais**.

Šioje temoje pagrindinis dėmesys skiriamas projekto pasiūlymų informacijai.

„Project Operations“ projekto pasiūlyme gali būti keli eilučių elementai arba pasiūlymo eilutės. Faktiškai projekto pasiūlyme yra du eilučių elementų tinkleliai. Vienas tinklelis skirtas projektu pagrįstoms eilutėms, kurias galima išsamiai įvertinti. Kitas tinklelis skirtas produktu pagrįstoms eilutėms, kurioms naudojamas tiesiog vieneto kaina ir kiekiu pagrįstas metodas.

- **Pagrįstas projektu** – siūloma vertė nustatoma įvertinus reikiamo darbo kiekį. Galite įvertinti darbo aukštą lygį tiesiogiai kaip eilutės išsamią informaciją po kiekvienos pasiūlymo eilutės arba pagal žemės sąmatą, naudodami projekto ir projekto planą. Projektu pagrįstas pasiūlymo eilutes galima rasti tik projekto pasiūlymuose, sukurtuose naudojant „Project Operations“. Šio tipo pasiūlymo eilutė yra pildomų pasiūlymo eilučių, esančių programoje „Microsoft Dynamics 365 Sales“, tinkinta forma.

- **Pagrįstas produktu** – siūloma vertė nustatoma pagal parduotų vienetų kiekį ir produkto vieneto pardavimo kainą. Produktas, esantis produktu grindžiamoje eilutėje, gali būti produktas iš „Sales“ produktų katalogo arba tai gali būti jūsų nustatytas produktas. Šio tipo pasiūlymo eilutė taip pat galima projektu pagrįstuose pasiūlymuose, sukurtuose naudojant „Project Operations“.

Pasiūlymo suma – tai bendra produktu pagrįstų eilučių ir projektu pagrįstų eilučių suma.

> [!NOTE]
> Pasiūlymai ir pasiūlymo eilutės nėra būtini naudojant „Project Operations“. Projekto procesą galite pradėti nuo projekto sutarties (parduodamas projektas). Tačiau galimybė yra visada būtina, nepaisant to, ar pradedate nuo pasiūlymo ar projekto sutarties.

## <a name="project-based-quote-lines"></a>Projektu pagrįstos pasiūlymo eilutės

„Project Operations“ projektu pagrįstoje pasiūlymo eilutėje galimi toliau nurodyti atsiskaitymo būdai:

- Laikas ir medžiagos
- Fiksuota kaina

### <a name="time-and-material"></a>Laikas ir medžiagos

Laiko ir medžiagų atsiskaitymo metodas grindžiamas suvartojimu. Pasirinkus šį atsiskaitymo metodą, klientui išrašoma sąskaita faktūra, kai patiriamos projekto išlaidos. Kuriamos periodinės, data grindžiamos sąskaitos faktūros. Pardavimo proceso metu siūloma laiko ir medžiagų komponentų vertė klientui nurodo tik apytikrę galutinių išlaidų vertę. Tiekėjas neįsipareigoja užbaigti projekto tiksliai už pasiūlytą vertę. Naudojant atsiskaitymą už laiko ir medžiagų komponentus didėja kliento rizika. Klientai gali norėti susitarti dėl papildomų vertės, kurios negalima viršyti, sąlygų, kad sumažintų savo riziką. Naudojant „Project Operations“, vertės, kurios negalima viršyti, sąlygų nustatymas nepalaikomas.

### <a name="fixed-price"></a>Fiksuota kaina

Naudojant fiksuotos kainos atsiskaitymo metodą, tiekėjas įsipareigoja klientui įvykdyti projektą už fiksuotą kainą. Klientui išrašoma pasiūlytos vertės sąskaita pagal fiksuotos kainos pasiūlymo eilutę, neatsižvelgiant į tiekėjo vykdant šią pasiūlymo eilutę patirtas išlaidas. Sąskaita pagal fiksuotos kainos pasiūlymo eilutės vertę išrašoma naudojant vieną iš toliau nurodytų būdų. 

- Mokant vienkartinę sumą projekto pradžioje arba pabaigoje, arba užbaigus projekto etapą. 
- Mokant periodines fiksuotos pasiūlymo eilutės kainos įmokas lygiomis dalimis nustatytomis datomis. Šios įmokos vadinamos kaip periodiniu sąskaitų pateikimu etapais.
- Mokant dalimis, kurių piniginė išraiška atitinka darbų eigą arba įvykdytus projekto etapus. Šiuo atveju kiekvienos įmokos vertė gali skirtis, tačiau jų suma turi atitikti fiksuotą pasiūlymo eilutės kainą.

„Project Operations“ palaiko visų trijų tipų fiksuotos kainos pasiūlymo eilučių sąskaitų faktūrų pateikimo grafikus.

## <a name="transaction-classification"></a>Operacijų klasifikacija

Profesionalių paslaugų organizacijos paprastai teikia klientams pasiūlymus ir išrašo sąskaitas faktūras pagal išlaidų klasifikaciją. Išlaidos nurodomos pagal toliau pateiktas operacijų klasifikacijas.

- **Laikas** – ši klasifikacija apima žmogiškųjų išteklių darbo su projektu laiko sąnaudas.
- **Išlaidos** – ši klasifikacija apima visų kitų tipų su projektu susijusias išlaidas. Kadangi išlaidas iš esmės galima klasifikuoti labai įvairiai, dauguma organizacijų kuria papildomų kategorijų, pvz., kelionių, automobilių nuomos, viešbučių arba raštinės reikmenų išlaidos.
- **Mokestis** – ši klasifikacija apima įvairias papildomas išlaidas, baudas ir kitus kliento mokamus elementus. 
- **Mokesčiai** – ši klasifikacija apima mokesčių sumas, kurias vartotojai įtraukia įvesdami išlaidas.
- **Medžiagų operacija** – ši klasifikacija apima faktines produktų eilučių sumas patvirtintoje projekto sąskaitoje faktūroje.
- **Etapas** – ši klasifikacija naudojama fiksuotos kainos atsiskaitymo logikai.

Su kiekviena pasiūlymo eilute galima susieti vieną arba kelias iš šių operacijų klasifikacijų. Laimėjus pasiūlymą, operacijų klasifikacijos susiejimas ir pasiūlymo eilutė perkeliami į sutarties eilutę.
  
Pavyzdžiui, pasiūlyme gali būti šios dvi pasiūlymo eilutės: 

- konsultavimo darbas, už kurį atsiskaitoma naudojant laiko ir medžiagų atsiskaitymo metodą, taikant operacijų klasifikacijas Laikas ir Mokestis. Pavyzdžiui, klientui išrašoma sąskaita faktūra už visas pavyzdinio projekto **Visuotinis „Dynamics AX“ diegimas** laiko ir mokesčio klasifikacijų operacijas, atsižvelgiant į laiko ir medžiagų sąnaudas; 
- susijusios kelionių išlaidos, kurioms taikomas fiksuotos kainos atsiskaitymo metodas. Pavyzdžiui, sąskaita už visas pavyzdinio projekto **Visuotinis „Dynamics AX“ diegimas** kelionių išlaidas išrašoma naudojant fiksuotą piniginę vertę.

> [!NOTE]
> Su pasiūlymo eilute arba sutarties eilute susietų operacijų klasifikacijų **Laikas**, **Išlaidos** ir **Mokestis** derinys turi būti unikalus. Jei tas pats projekto ir operacijų klasių derinys susiejamas su daugiau nei viena sutarties eilute arba pasiūlymo eilute, „Project Operations“ veiks netinkamai.

## <a name="billing-types"></a>Atsiskaitymo tipai

Lauke **Atsiskaitymo tipas** nustatoma apmokestinimo sąvoka. Tai – parinkčių rinkinys, galintis apimti toliau nurodytas reikšmes.

- **Apmokestinamos** – šiame vaidmenyje / kategorijoje kaupiamos išlaidos laikomos tiesioginėmis su projekto vykdymu susijusiomis išlaidomis ir klientas sumokės už šį darbą. Mokėjimas gali būti administruojamas kaip laiko ir medžiagų arba fiksuotos kainos susitarimas. Tačiau šiam darbui laiką skyrusiam darbuotojui bus išmokėtas atitinkamas kreditas už apmokėtiną efektyvumą.
- **Neapmokestinamos** – šiame vaidmenyje / kategorijoje kaupiamos išlaidos laikomos tiesioginėmis su projekto vykdymu susijusiomis išlaidomis, net jei klientas nepripažįsta šio fakto ir už šį darbą nemokės. Laiką skyrusiam darbuotojui nebus mokama už apmokėtiną efektyvumą.
- **Nemokamos** – šiame vaidmenyje / kategorijoje kaupiamos išlaidos laikomos tiesioginėmis su projekto vykdymu susijusiomis išlaidomis ir klientas pripažįsta šį faktą. Laiką skyrusiam darbuotojui bus sumokėta už apmokėtiną efektyvumą. Tačiau šios išlaidos nebus priskirtos klientui.
- **Nėra** – naudojant šią parinktį sekamos su vidaus projektais, kurių pajamų nereikia sekti, susijusios išlaidos.

## <a name="invoice-schedule"></a>Sąskaitų faktūrų grafikas

Sąskaitų faktūrų grafikas – tai su projektų susijusių sąskaitų faktūrų išrašymo datų seka. Galite pasirinktinai sukurti sąskaitų faktūrų grafiką pasiūlymo eilutėje. Kiekvienai pasiūlymo eilutei galima sukurti atskirą sąskaitų faktūrų grafiką. Norėdami sukurti sąskaitų faktūrų grafiką, turite nurodyti šias atributų reikšmes:

- atsiskaitymo pradžios data; 
- pristatymo data, nurodanti projekto pabaigos datą;
- sąskaitų faktūrų išrašymo dažnis;

Šios trys atributų reikšmės naudojamos, kad būtų sukurtas preliminarų sąskaitų faktūrų išrašymo datų rinkinį.

## <a name="invoice-frequency"></a>SF išrašymo dažnis

Sąskaitų faktūrų išrašymo dažnis – tai objektas, apimantis atributų reikšmės, padedančias išreikšti sąskaitų faktūrų kūrimo dažnį. Šie atributai išreiškia arba nustato sąskaitų faktūrų išrašymo dažnio objektą:

- **Laikotarpis** – palaikomi laikotarpiai: kas mėnesį, kas dvi savaites ir kas savaitę. 
- **Vykdymų skaičius per laikotarpį** – laikotarpiams kas savaitę ir kas dvi savaites galima nustatyti tik vieną vykdymą per laikotarpį. Laikotarpiams kas mėnesį galima nustatyti nuo vieno iki keturių vykdymų per laikotarpį; 
- **Vykdymo dienos** – sąskaitų faktūrų išrašymo dienos. Šį atributą galima sukonfigūruoti dviem būdais:
  - **Savaitės dienos** – pavyzdžiui, galite nurodyti, kad sąskaitos faktūros būtų išrašomos kiekvieną pirmadienį arba kas antrą pirmadienį. Klientai, kuriems reikia nustatyti sąskaitų faktūrų išrašymo dieną kaip darbo dieną, gali pageidauti šio tipo konfigūracijos; 
  - **Kalendorinės dienos** – pavyzdžiui, galite nurodyti, kad sąskaitos faktūros būtų išrašomos kiekvieno mėnesio septintą ir dvidešimt pirmą dienomis. Kai kurios organizacijos gali teikti pirmenybę šio tipo konfigūracijai, nes ji padeda užtikrinti, kad sąskaitos faktūros būtų išrašomos kas mėnesį pagal fiksuotą grafiką.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Fiksuotos kainos pasiūlymo eilutės sąskaitų faktūrų grafikas

Fiksuotos kainos pasiūlymo eilutėms galite naudoti tinklelį **Sąskaitų faktūrų grafikas** ir sukurti atsiskaitymo etapus, atitinkančius pasiūlymo eilutės vertę.

- Jei norite sukurti lygiai padalytus sąskaitų išrašymo etapus, pasirinkite sąskaitų faktūrų išrašymo dažnį, į pasiūlymo eilutę įveskite atsiskaitymo pradžios datą ir pasiūlymo antraštės srityje **Suvestinė** pasirinkite pasiūlymo **Pageidaujamą užbaigimo datą**. Tada pasirinkite **Generuoti periodinį sąskaitų pateikimą etapais** ir sukurkite lygiai padalytus etapus pagal pasirinktą sąskaitų faktūrų išrašymo dažnį. 
- Norėdami sukurti atsiskaitymo vienkartine suma etapą, sukurkite etapą ir tada kaip etapo sumą įveskite pasiūlymo eilutės vertę.
- Norėdami sukurti konkrečiomis projekto plano užduotimis pagrįstus sąskaitų išrašymo etapus, sukurkite etapą ir atsiskaitymo etapo UI susiekite jį su projekto grafiko elementu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]