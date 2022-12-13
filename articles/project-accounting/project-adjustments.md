---
title: Projekto korekcijos
description: Šiame straipsnyje pateikiama informacija apie projekto koregavimus.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788370"
---
# <a name="project-adjustments"></a>Projekto korekcijos

_**Taikoma (kam):**„Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_

## <a name="adjustments-overview"></a>Koregavimų apžvalga

Galite konfigūruoti "Microsoft", Dynamics 365 Project Operations kad vartotojai galėtų keisti paskelbtas operacijas. Galite koreguoti projekto operacijas atskirai arba visų projekto operacijų sąraše vienu metu pasirinkti kelias operacijas. Projekto koregavimai naudojami, pvz., norint masiškai atnaujinti atsiskaitymo būseną, perskaičiuoti išlaidas pakeitus konfigūraciją arba atnaujinti finansavimo šaltinius.

Vartotojai gali pasiekti projekto koregavimo funkciją keliais būdais:

- Naudodami **puslapį Koreguoti operacijas**, kurį galima pasiekti iš **projektų valdymo ir apskaitos** \> **sąrankos**.
- Naudodami **mygtuką Koregavimas**, esantį puslapyje Užregistruotos projekto operacijos **,** kurį galima pasiekti iš **projektų valdymo ir apskaitos** \> **operacijų**.
- Naudodami **mygtuką Koregavimas**, **esantį puslapyje Užregistruotos projekto operacijos** projekto kontekste. Šį puslapį galima pasiekti iš **Projektų valdymas ir apskaita** \> **Visi projektai**.

Norėdami leisti koregavimus, turite įjungti vieną ar daugiau operacijų būsenų iš **projektų valdymo ir apskaitos projektų valdymo ir apskaitos** \> **formuotojų**, **esančių skirtuko** Bendra **skyriuje Leisti koreguoti operacijos būseną**. Operacijų būsenų pavyzdžiai apima užregistruotas operacijas, operacijas, kurioms išrašyta SF, arba eliminuotas operacijas. Bet kurioje operacijos būsenoje, kuri nustatyta kaip Ne **, bus tos būsenos operacijų, kurios nebus rodomos koregavimo procese kaip** pasirenkamos koreguoti.

Konfigūravimo parinktis, pavadinta **Visada kurti koregavimo operaciją**, šiuo metu pasiekiama projektų valdymo ir apskaitos parametruose. Šią parinktį galite išjungti, jei norite atnaujinti pradinę operaciją, o ne kurti naujas operacijas koreguojant scenarijų poaibyje. Paskelbta, kad šis parametras bus nebenaudojamas iki 2023 m. kovo 1 d. Po 1 m. kovo 2023 d. sistema visada elgsis taip, lyg parinktis būtų įjungta.

## <a name="adjustments-process-flow"></a>Koregavimo proceso eiga

Šie veiksmai rodo tipinį koregavimų apdorojimo srautą.

1.  **Atidarykite puslapį Projekto koregavimai** .
2. Pasirinkite **Pasirinkti**, jei norite ieškoti operacijų, kurios atitinka numatomus koregavimo kriterijus.
3. Operacijų sąraše pasirinkite visas koreguojamas operacijas arba operacijų poaibį.
4. Pasirinkite **Koreguoti** ir modifikuokite eilutės atributus. Arba, jei reikšmės buvo rankiniu būdu nurodytos įvedant operaciją, galite pasirinkti įvesti numatytąsias sistemos reikšmes.
5. Operacijų sąrašas grąžinamas, o stulpelyje Laukiamas koregavimas **pasirodo** varnelė, nurodanti, kur buvo atlikti pakeitimai. Visi koregavimai, kurių laukiantys pakeitimai yra laukiami, rodomi apatinėje puslapio dalyje. Čia galite atlikti papildomų išsamių pakeitimų, be to, kas buvo parodyta ankstesniame puslapyje.
6. Pasirinkite **Registruoti**, kad registruotumėte koregavimo operacijas.

Atsižvelgiant į konfigūraciją, koregavimui paprastai sukuriamos naujos operacijos.

- Pradinės **operacijos laukas Sąskaitos faktūros būsena** nustatytas kaip **Koreguota**.
- Norint atšaukti pradinę operaciją, sukuriama atšaukimo operacija, o **laukas Būsena** nustatomas kaip **Koreguotas**.
- Sukuriama nauja operacija su pakeitimais, kurie buvo atlikti koregavimo proceso metu.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Kelių užregistruotų projekto operacijų pasirinkimas vienu metu koregavimams ir kredito pažymoms

Nauja funkcija, kuri buvo pristatyta 10.0.30 leidime, leidžia pasirinkti kelias koreguojamas operacijas vienu metu puslapyje Paskelbtos **projekto operacijos** .

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Administratoriai gali naudoti **funkcijų valdymo** darbo sritį, kad patikrintų funkcijos būseną ir, jei reikia, ją įjungtų.  **Darbo srityje Funkcijų valdymas** ieškokite ir pasirinkite Kelis kartus pasirinkite paskelbtas projekto operacijas, kad gautumėte koregavimus ir kredito pažymas **, tada pasirinkite** **Įgalinti dabar**.

Ši funkcija įgalina šias pagrindines funkcijas:

- Jį galima pasiekti iš paskelbto projekto operacijų puslapio naudojant esamą **mygtuką Koregavimas** .
- Jis įgalina kelių eilučių pasirinkimo valdiklį puslapyje Paskelbtos **projekto operacijos** . Galite taikyti filtrus sąrašo puslapiui ir pasirinkti įrašus prieš pradėdami koregavimus.
- Jis išjungia **mygtuką Koregavimas**, jei negalima koreguoti kurios nors vienos operacijos arba jei pasirenkate kredito pažymų ir žurnalų derinį kartu, o ne atskirai.
- Įtraukus kelių eilučių pasirinkimo valdiklį, juostelėje esantis saitas Fiksuotos išlaidos **nebeišjungiamas,** jei pažymėtos kelios eilutės.
- Jis prideda tokį įspėjamąjį pranešimą: "Koregavimui pasirinkote daugiau nei (pasirinktas skaičius) įrašų. Šio veiksmo tęsimas gali užtrukti. Ar tikrai norėtumėte tęsti šį veiksmą?"

Ši funkcija taip pat pašalina 2 veiksmą iš proceso eigos, kuri buvo aprašyta anksčiau šiame straipsnyje. Todėl visos operacijos, kurios buvo pasirinktos **prieš atidarant puslapį Koreguoti operacijas**, bus įtrauktos į koreguojamų operacijų sąrašą. Jums nereikia naudoti mygtuko Pasirinkti **,** kad jų ieškotumėte.

> [!NOTE] 
> Net jei ši funkcija išjungta, vis tiek galite pasirinkti kelis įrašus koreguoti. Tačiau tik vienas įrašas liks *pažymėtas*, o **dialogo langas Pasirinkti operacijas** pasirodys iškart po to, kai pasirinksite atidaryti koregavimus.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Koregavimo operacijų būsenos, kurias galima įjungti arba išjungti atliekant koregavimus

Šias būsenas galima įjungti arba išjungti **puslapio Projektų valdymo ir apskaitos parametrai** skirtuke **Bendra** :

- Užregistruota
- Sąskaitos faktūros pasiūlymas
- Išrašyta sąskaita faktūra
- Numatoma
- Pašalinti
- Pradžios balansas (valanda)

## <a name="adjustment-parameters"></a>Reguliavimo parametrai

Šie parametrai išvardyti **puslapio Projektų valdymo ir apskaitos parametrai**, esančio skirtuko **Bendra** grupėje Koregavimas **,** ir pakeis koregavimų apdorojimo elgseną. 

| Parametro pavadinimas | Aprašą |
|----------------|-------------
| Visada sukurkite koregavimo operaciją | Jei šis parametras įjungtas, koregavimo procesas visada sukurs naują atvirkštinę operaciją ir naują pakoreguotą operaciją, kai bus padarytas finansinis poveikis arba ataskaitos. Jei parametras išjungtas, koregavimo procesas atnaujins pradinę operaciją, o ne sukurs atšaukimą ir naują operaciją scenarijui, pvz., operacijos teksto atnaujinimui. |
| Laukas Autoupdate | Jei šis parametras įjungtas, sistema perskaičiuos savikainą ir pardavimo kainą. |
| Naudokite koregavimo datą kaip naują projektą | Šis parametras naudojamas operacijoms perkelti į būsimą ataskaitinis laikotarpis prieš sistemai palaikant šią funkciją. Nerekomenduojame jo naudoti, nes jis pakeičia operacijos verslo datą ir bus nebenaudojamas būsimame leidime. |
| Leisti uždarą veiklą | Paprastai uždaroms veikloms operacijų kurti negalima. Jei šis parametras įjungtas, to veikimo būdo nepaisoma. Todėl galima sukurti uždaros veiklos koregavimus. |
