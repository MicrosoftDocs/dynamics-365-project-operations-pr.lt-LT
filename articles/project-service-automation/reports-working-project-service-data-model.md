---
title: Darbas su „Project Service Automation“ duomenų modeliu
description: Šioje temoje pateikiama informacija apie tai, kaip dirbti su duomenų modeliu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: e1a177a8-cd16-4ac4-acb8-a8f1a8f9e4bf
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: b909099af2493c4010103189c2add6175eea8add
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753750"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Darbas su „Project Service Automation“ duomenų modeliu

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation išplečia kitus programos objektus ir įveda nuosavus objektus į Common Data Service duomenų modelį. Šioje temoje aprašomi keli objektai, su kuriais susidursite įprastuose PSA ataskaitų scenarijuose.

## <a name="reporting-on-opportunities"></a>Ataskaitų apie galimybes teikimas

„Project Service Automation“ išplečia „Dynamics 365 Sales“ **Opportunity** objektą įtraukdamas laukus, kurie įgalina projektais pagrįstus scenarijus. Šie laukai identifikuojami pagal schemos pavadinimą, kuris yra su prefiksu **msdyn\_**. Vienas naujas laukas, svarbus norint pateikti ataskaitą apie PSA galimybes, yra **Užsakymo tipas**. Šiame lauke **Pagrįsta darbu** reikšmė nurodo, kad galimybė yra PSA galimybė. Kiti laukai, kurie buvo įtraukti į objektą, yra **Susijusi įmonė**, kuris fiksuoja organizaciją, turinčią galimybę, ir **Klientų vadybininkas**, kuris fiksuoja klientų vadybininko, atsakingo už galimybę, vardą.

Objekte **Galimybės eilutė** taip pat yra laukų, susijusių su „Project Service“. **Sąskaitų išrašymo** metodas nurodo, ar galimybės eilutė turėtų būti išrašyta pagal laiką ir medžiagas, ar pagal fiksuotos kainos principą, o **Projektas** užfiksuoja projekto, kuris kuria galimybės atsarginę kopiją, pavadinimą. Kituose laukuose, kuriuos galite įtraukti į ataskaitą, fiksuojama eilutės elemento savikaina ir kliento biudžeto sumos.

## <a name="reporting-on-quotes"></a>Ataskaitų apie pasiūlymus teikimas

PSA išplečia pardavimo **pasiūlymo** objektą įtraukdama su projektu susijusius laukus. **Užsakymo tipas** atskiria PSA pasiūlymus iš ne PSA pasiūlymų. Šio lauko **Darbu pagrįsta** reikšmė nurodo, kad pasiūlymas yra PSA pasiūlymas. Kiti laukai, kurie gali būti susiję su PSA pasiūlymų ataskaitų teikimu yra **Apmokestinama savikaina**, **Neapmokestinama savikaina**, **Bruto marža**, **Įvertinimai** ir **Biudžetas**. Kiti naudingi laukai nurodo, ar savikaina yra pelninga, ar ji bus užbaigta laiku ir ar ji atitinka kliento biudžeto lūkesčius.

PSA taip pat išplečia Pardavimų **pasiūlymo eilutės** objektą. Vienas laukas, kurį PSA įtraukia, yra **Atsiskaitymo metodas**, kuris nurodo, kaip pasiūlymo eilutė bus apmokestinta (laikas ir medžiagos arba fiksuota kaina). Kiti laukai, kurie buvo įtraukti į objektą, fiksuoja susijusį projektą, kuris kuria pasiūlymo eilutės, sąskaitos faktūros, savikainos ir biudžeto atsargines kopijas.

PSA į „Dynamics 365“ duomenų modelį taip pat įtraukia naujus su pasiūlymu susijusius objektus. Štai keli pavyzdžiai:

- **Pasiūlymo eilutės informacija** – šį objektą sudaro pasiūlymo eilutės projekto įvertinta informacija. Kiekvienoje pasiūlymo eilutėje yra du įrašai. Viename įraše saugoma pasiūlymo eilutės savikaina ir savikainos informacija, o kitame – pasiūlymo eilutės pardavimo suma ir pardavimo informacija.
- **Pasiūlymo eilutės sąskaitos faktūros grafikas** – šiame objekte yra pasiūlymo eilutės atsiskaitymo grafikas. Šis grafikas sukuriamas pagal sąskaitų faktūrų išrašymo dažnumą, priskirtą pasiūlymo eilutei.
- **Pasiūlymo eilutės etapas** – šiame objekte yra fiksuotos kainos pasiūlymo eilučių atsiskaitymo etapai.
- **Pasiūlymo eilutės analizės paskirstymas** – šiame objekte yra pasiūlymo eilutės finansinė informacija. Ši informacija gali būti naudinga teikiant ataskaitas apie pasiūlytus pardavimus ir įvertintas savikainos sumas įvairiais matmenimis.

Kiti objektai, kuriuo PSA įtraukia į pasiūlymus, yra **Pasiūlymo eilutės projekto kainoraštis**, **Pasiūlymo eilutės išteklių kategorija** ir **Pasiūlymo eilutės operacijų kategorija**.

![Diagrama, parodanti pasiūlymą, pasiūlymo eilutę ir projektų ryšius](media/PS-Reporting-image2.png "Diagrama, parodanti pasiūlymą, pasiūlymo eilutę ir projektų ryšius")

## <a name="reporting-on-project-contracts"></a>Ataskaitų teikimas apie projektų sutartis

PSA išplečia Pardavimo **užsakymo** objektą, kuris naudojamas, kai įrašomos projekto sutartys. Jis įtraukia svarbų naują lauką **Užsakymo tipas**, kuris identifikuoja sutartį kaip PSA projekto sutartį, o ne pardavimo užsakymą. Šio lauko **Darbu pagrįsta** reikšmė nurodo, kad užsakymas yra PSA projekto sutartis. Kituose naujuose laukuose, kurie įtraukti į **Užsakymo** objektą, fiksuojama informacija apie savikainą, PSA sutarties būseną ir organizaciją, kurai priklauso sutartis.

PSA taip pat išplečia **Pardavimo užsakymo eilutės** objektą. Tarp įtrauktinų laukų yra laukai, kuriuose fiksuojamas atsiskaitymo metodas (laikas ir medžiagos arba fiksuota kaina), kliento biudžeto sumos ir pagrindinis projektas.

PSA taip pat įtraukia naujus objektus, kurie sukurti projekto sutartims. Štai keli pavyzdžiai:

- **Projekto sutarties eilutės informacija** – šiame objekte yra eilutės lygio informacija, kuri išskleidžiama į sutarties eilutės sumą. Jos gali būti tokios pat išsamios kaip ir eilutės elementai, kurie sukuriami iš projekto grafiko užduoties lygmenyje.
- **Sutarties eilutės sąskaitų faktūrų grafikas** – šiame objekte yra sąskaitų faktūrų išrašymo grafikas, sugeneruotas pagal sąskaitų faktūrų išrašymo dažnumą, priskirtą sutarties eilutei.
- **Sutarties etapas** – objekte yra sutarties eilučių, kurios turi fiksuotos kainos atsiskaitymo terminą, atsiskaitymo etapai.

Kiti objektai, kuriuos PSA įtraukia į sutartis yra **Projekto sutarties eilutės projekto kainoraštis**, **Projekto sutarties eilutės išteklių kategorija** ir **Projektų sutarties eilutės operacijų kategorija**.

![Diagrama, parodanti užsakymą, užsakymo eilutę ir projektų ryšius](media/PS-Reporting-image3.png "Diagrama, parodanti užsakymą, užsakymo eilutę ir projektų ryšius")

## <a name="reporting-on-projects"></a>Ataskaitų apie projektus teikimas

Objektas **Projektai** ir jo susiję objektai priklauso tik PSA. **Projektas** yra aukščiausiojo lygio objektas, naudojamas operacijoms ir operacijų savikainai fiksuoti. Toliau pateikiamas susijusių objektų sąrašas.

- **Projekto komandos narys** – šiame objekte pateikta informacija apie rezervuojamus išteklius, kurie priskirti projektui. Šie ištekliai gali būti bendrojo pobūdžio rezervuojami ištekliai arba pavadinimus turintys rezervuojami ištekliai, kuriuos įvedė arba projektų vadovas, arba kurie buvo sukurti iš projekto grafiko.
- **Projekto užduotis** – šiame objekte yra užduočių, kurios sudaro projekto planą arba grafiką.
- **Išteklių priskyrimas** – šiame objekte yra užduotis, priskirtina rezervuojamiems ištekliams.
- **Išteklių reikalavimas** – šiame objekte yra bendrųjų išteklių komandos nariams skirti reikalavimai.
- **Įvertinimas** ir **Įvertinimo eilutė** – šie objektai turi antraštės / eilutės ryšį ir projektui apskaičiuotas išlaidas. Užduočių įvertinimai saugomi objekte **Išteklių įvertinimas**.

![Diagrama, parodanti išteklių reikalavimą ir projektų ryšius](media/PS-Reporting-image4.png "Diagrama, parodanti išteklių reikalavimą ir projektų ryšius")

## <a name="reporting-on-resources"></a>Ataskaitų teikimas apie išteklius

Projekto ištekliai naudoja **Rezervuojamų išteklių** objektus iš Universal Resource Scheduling (URS), kurie bendrinami su kitomis programomis, pavyzdžiui, „Microsoft Dynamics 365 Field Service“. Toliau pateikiamas objektų, kuriuos gali reikėti naudoti, kai teikiate ataskaitas apie projekto išteklius, sąrašas.

- **Rezervuojami ištekliai** – objektas nurodo naudotoją, kontaktą, bendruosius išteklius, klientą, grupę arba įrangą, kurią naudoja projekto komanda.
- **Rezervuojamų išteklių charakteristikos** – šį objektą sudaro išteklių įgūdžiai, sertifikatai arba išsilavinimas. Charakteristikos gali turėti įvertinimo reikšmes, kurios apibrėžiamos pagal įvertinimo modelį.
- **Rezervuojamų išteklių kategorija** – šis objektas nurodo rezervuojamų išteklių vaidmenį.
- **Rezervuoti išteklių rezervacijos** – šis objektas nurodo laiką, kuris rezervuotas projektų ištekliams. Kiekviena rezervacija turi antraštės objektą ir eilutės objektus, o kiekviena eilutė turi būseną, kuri rodo rezervacijos būseną.

![Diagrama, parodanti rezervuojamų išteklių charakteristikų ryšius](media/PS-Reporting-image5.png "Diagrama, parodanti rezervuojamų išteklių charakteristikų ryšius")

## <a name="reporting-on-actual-transactions"></a>Ataskaitų teikimas apie faktines operacijas

Kai patvirtinate tabelį arba išlaidas, sąskaitą faktūrą arba sutartį PSA, verslo operacija užfiksuojama objekte **Faktinis**. Šį objektą PSA galima naudoti kaip beveik visų su finansais susijusių ataskaitų pagrindą. Objektas **Faktinis** fiksuoja verslo įvykio savikainą ir pardavimo operacijas. Jame taip pat užfiksuojama daug susijusių atributų.

Kai dirbate su objektu **Faktinis**, svarbu, kad suprastumėte, kokia operacija ar operacijos įrašomos objekte, ir kada operacijos įrašomos. Toliau pateiktas įprastas srautas, kai dirbate su laiko įrašais (išlaidų įrašų srautas yra panašus).

1. Kai laiko įrašas įrašytas, objekte **Faktinis** nesukuriama jokių įrašų.
2. Kai laiko įrašas pateiktas, objekte **Faktinis** nesukuriama jokių įrašų.
3. Kai laiko įrašas patvirtintas, objekte **Faktinis** sukuriamas vienas įrašas, taip pat galima sukurti antrą įrašą. Pirmame įraše saugoma laiko įrašo savikaina. Antrame įraše saugoma laiko įrašo pardavimo suma, kuri dar nėra atsiskaityta. Antras įrašas priklauso nuo to, ar projektui priskirtas klientas, pasiūlymas ar sutarties eilutė.

    | Dokumento data | Operacijos tipas | Operacijos klasė | Klientas         | Sutartis   | Ištekliai     | Išteklių vaidmuo | Atsiskaitymo tipas | Kiekis | Vieneto kaina | Kiekis |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2018-03-02        | Išlaidos             | Time              | „Alpine ski house“ | „Alpine CRM“ | Brigita Bortkevičienė | Projekto vadovė   | Apmokestinama   | 8.0      | 50.00      | 400.00 |
    | 2018-03-02        | Pardavimas, už kurį neišrašyta sąskaita   | Time              | „Alpine ski house“ | „Alpine CRM“ | Brigita Bortkevičienė | Projekto vadovė   | Apmokestinama   | 8.0      | 100.00     | 800.00 |

    Šie du įrašai yra atskiri, bet susiję. Jie nėra nei debetai, nei kreditai.

4. Jei sutartis susijusi su projektu, kai laiko įrašui išrašoma sąskaita faktūra, objekte **Faktinis** sukuriami dar du įrašai. Pirmiausia, sukuriama pardavimo, už kurį neišrašyta sąskaita, neigiama suma. Šis įrašas iš esmės anuliuoja pardavimą, už kurį neišrašyta sąskaita. Antra, sukuriama pardavimo, už kurį išrašyta sąskaita, operacija. Tai yra atskiri, bet susiję įrašai, jie nėra nei debetai, nei kreditai.

    | Dokumento data | Operacijos tipas | Operacijos klasė | Klientas         | Sutartis   | Ištekliai     | Išteklių vaidmuo | Atsiskaitymo tipas | Kiekis | Vieneto kaina | Kiekis   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2018-04-02        | Pardavimas, už kurį neišrašyta sąskaita   | Time              | „Alpine ski house“ | „Alpine CRM“ | Brigita Bortkevičienė | Projekto vadovė   | Apmokestinama   | - 8.0    | 100.00     | - 800.00 |
    | 2018-04-02        | Pardavimas, už kurį išrašyta sąskaita     | Time              | „Alpine ski house“ | „Alpine CRM“ | Brigita Bortkevičienė | Projekto vadovė   | Apmokestinama   | 8.0      | 100.00     | 800.00   |

Objekte **Operacijos kilmė** įrašomas **Faktinis** įrašas, o objekte **Operacijos ryšis** įrašomi susiję objekto **Faktinis** įrašo įrašai. Be to, objekto **Faktinis** įraše yra nuoroda į projektą, projekto sutartį (užsakymą), rezervuojamus išteklius ir klientą.

![Diagrama, parodanti operacijų ryšį, kilmę ir faktinius ryšius](media/PS-Reporting-image6.png "Diagrama, parodanti operacijų ryšį, kilmę ir faktinius ryšius")
