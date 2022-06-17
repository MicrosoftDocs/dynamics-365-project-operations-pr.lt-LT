---
title: Įrašų žurnalų kūrimas ir patvirtinimas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip kurti ir patvirtinti įrašų žurnalus programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912342"
---
# <a name="create-and-confirm-entry-journals"></a>Įrašų žurnalų kūrimas ir patvirtinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Įrašų žurnalai naudojami faktams įrašyti tiesiogiai programoje Microsoft Dynamics 365 Project Operations. Kai naudojate įrašų žurnalus, projekto operacijose nereikia įvesti Laiko, Išlaidų ir Medžiagų naudojimo žurnalų.

Vienas įrašų žurnalas leidžia kurti kelias žurnalo eilutes. Patvirtinus žurnalą, įrašo žurnalo eilutė įrašo faktinę informaciją apie šią informaciją:

- Savikaina arba įplaukos, atsižvelgiant į pasirinktą operacijos tipą.
- Pasirinkta operacijos klasė. Galimos klasės yra **laikas**, išlaidos **,** medžiaga **,** **laikiklis**, **orientyras** ir **mokesčiai**.
- Žurnalo eilutėje pasirinktas projektas ir (arba) užduotis.

Atlikite šiuos veiksmus, kad sukurtumėte įrašų žurnalą programoje "Project Operations".

1. Eikite į **pardavimo** \> **operacijų** \> **žurnalus**.
2. **Sąrašo sąrašo puslapio Įrašai žurnalai** veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte žurnalą.
3. **Puslapio Naujas žurnalas** lauke Aprašas **įveskite** žurnalo aprašymą.
4. Įsitikinkite, kad laukas Žurnalo **tipas** nustatytas kaip **Įrašas**, tada pasirinkite **Įrašyti**. Įrašius naują įrašų žurnalą, žurnalo puslapyje turėtų būti rodomas skirtukas **Žurnalo eilutės**.
5. Skirtuko Žurnalo **eilutės** įrankių juostoje virš tinklelio pasirinkite **Naujas**, kad sukurtumėte įrašo žurnalo eilutę.
6. **Dialogo lange Greitas kūrimas**, skirtame įrašo žurnalo eilutei kurti, nustatykite laukus, kaip aprašyta šioje lentelėje.

    | Laukas | Aprašą | Funkcinis poveikis |
    | --- | --- | --- |
    | Operacijos klasė | Žurnalo eilutę galima suskirstyti į vieną iš šešių operacijų klasių: **laikas**, išlaidos **,** medžiaga **,** **laikiklis**, **orientyras** arba **mokesčiai**. | Mokesčių **operacijų** klasė buvo nebenaudojama projekto operacijose. <br> Jei sukursite **mokesčių** operacijų klasę, ji nebus apdorojama išrašant SF arba skaičiuojant išlaidas ar pajamas. **Orientyras** yra tik pajamų operacijų klasė. <br>Išlaikymo **operacijos** klasė nurodo avansą, gautą iš kliento. Jis visada turėtų būti sukurtas kaip pardavimų, už kuriuos išrašyta sąskaita, ir neapmokėtų pardavimo žurnalo eilučių pora. |
    | Operacijos tipas | Išlaidų **·**, **tarpinių pardavimų** ir **išteklių paskirstymo vieneto savikainos** operacijų tipai turėtų būti naudojami savikainai įrašyti.<br> Operacijų tipai Neįrašyti **pardavimai** ir **pardavimai** išrašytoje sąskaitoje turi būti naudojami įplaukoms įrašyti. | Užlaikytojo **operacijos** klasė veikia tik su operacijų tipais **Nemokėti pardavimai** ir **pardavimai**, kuriems išrašyta sąskaita.<br> Etapo **operacijų** klasė veikia tik su operacijos, **už kurią išrašyta sf,** tipu. <br>" **Interorg" pardavimo** ir **išteklių paskirstymo vieneto savikainos** operacijų tipai taikomi tik **laiko** operacijų klasei ir juos galima naudoti tik "Lite" diegimo scneario įrašų žurnaluose, o ne diegiant "Project Operations" išteklių / nekauptų scenarijų scenarijuose. |
    | Pasirinkti produktą | **Pasirinkus Medžiagų** operacijų klasę, šiame lauke galite nurodyti, ar medžiagų operacija, kuriai kuriate žurnalo eilutę, yra esamas produktas, ar įrašymo produktas. | Jei pasirinksite **Įrašyti produktą**, galėsite įvesti produkto pavadinimą. |
    | Produktas | Nuoroda į produktą iš katalogo. | |
    | Aprašą | Žurnalo eilutės aprašymas, padedantis lengvai identifikuoti. | Neįrašytų pardavimo žurnalo eilučių vertė bus naudojama kaip aprašymas, kai bus sukurta SF eilutės informacija. |
    | Išorinis aprašas | Žurnalo eilutės, kurią galima naudoti dalijantis su išorės suinteresuotosiomis šalimis, aprašymas. | Nerašytų pardavimo žurnalo eilučių vertė bus naudojama kaip išorinis aprašas, kai bus sukurta SF eilutės informacija. Jis taip pat gali būti rodomas klientui siunčiamoje sąskaitoje faktūroje. |
    | Atsiskaitymo tipas | Reikšmė, nurodanti, ar žurnalo eilutė bus skaičiuojama kaip apmokestinamas, nemokamas ar neapmokestinamas projekto komponentas. | Tipiniame sraute atsiskaitymo tipas gaunamas iš sutartyje nustatytų sutartų sąlygų. Tačiau įrašydami žurnalo eilutę, šiame lauke galite įvesti vertę. |
    | Dokumento data | Naudokite operacijos datą. | |
    | Pradžios data | Naudokite operacijos datą. | Šis laukas naudojamas palyginti su SF sukūrimo data operacijoms, **kurių tipas Unbilled Sales**. Šis palyginimas padės jums nuspręsti, ar sandoris yra būsimas, ar ankstesnis. Į SF bus įtrauktos tik ankstesnės datos operacijos. |
    | Pabaigos data | Naudokite operacijos datą. | |
    | Apskaitos data | Naudokite apskaitos poveikio registravimo datą. | |
    | Sutarties eilutės klientas | Pagal numatytuosius nustatymus, jei sutarties eilutėje yra tik vienas pirkėjas, šis laukas nustatomas kaip pirkėjas sutarties eilutėje, kai įrašoma žurnalo eilutė. Jei sutarties eilutėje yra keli klientai, sutarties eilutėje pasirinkite tinkamą klientą. | Jei sistema negali nustatyti sutarties eilutės pirkėjo žurnalo eilutėje ir jei jis tuščias pagal žurnalo eilutės sukurto neįskaitytų pardavimų **tipo** faktinį faktinį faktą, faktiniam nebus išrašyta SF. |
    | Project | Pasirinkite projektą, kuriame bus įrašytas faktinis. | Pagal pasirinktą projektą, operacijų klasę ir užduotį sistema bandys nustatyti sutartį, sutarties eilutę ir sutarties eilutės klientą. |
    | Užduotis | Pasirinkite užduotį, į kurią norite įrašyti faktinį. | Jei nustatydami sutartį užduotis susiejote su sutarties eilutėmis, sistema naudos pasirinktą užduotį kartu su projekto ir operacijų klase, kad nustatytų sutartį, sutarties eilutę ir sutarties eilutės pirkėją. |
    | Operacijos kategorija | Pasirinkite operacijos kategoriją, kurioje norite įrašyti faktinį. | Išlaidų atveju pasirinkta operacijų kategorija nustato numatytąją kainą, kuri bus įvesta į žurnalo eilutę, kai ji bus įrašyta. |
    | Vaidmuo | Šis laukas susijęs su laiko žurnalo eilutėmis. Pasirinkite ištekliaus, kuris praleido laiką projektui ir (arba) užduočiai, vaidmenį. | Laiko žurnalo eilutėse, jei numatytąją išteklių savikainą ir sąskaitų kursus įvesti naudojate lauko konfigūraciją, pasirinktas vaidmuo bus naudojamas kartu su išteklių paskirstymo vienetu, kad būtų galima nustatyti numatytąją kainą, kuri bus įvesta į žurnalo eilutę, kai ji bus įrašyta. Jei numatytųjų kainų įvedimui naudojate pasirinktinę konfigūraciją, turėtumėte peržiūrėti tą konfigūraciją, kad nustatytumėte, ar **laukas Vaidmuo** naudojamas numatytojims kainų vertėms įvesti. |
    | Subrangos sutartis | Jei žurnalo eilutėje nurodytas subrangos pajėgumas arba subrangos išlaidos ar medžiagos, pasirinkite atitinkamą subrangos sutartį. | Kai įrašomos išlaidų žurnalo eilutės, pasirinkta subrangos sutartis nustatys kainoraštį, kuris naudojamas numatytąjai vieneto savikainai įvesti. |
    | Subrangos eilutė | Jei žurnalo eilutėje nurodytas subrangos pajėgumas arba subrangos išlaidos ar medžiagos, pasirinkite atitinkamą subrangos eilutę. | Įrašius išlaidų žurnalo eilutes, pasirinkta subrangos eilutė užtikrins, kad galimi pajėgumų skaičiavimai subrangos eilutėje būtų teisingai apskaičiuoti. |
    | Sumos metodas | Pagal numatytuosius nustatymus šis laukas nustatytas dauginti **kiekį iš kainos**. Kai naudojamas šis metodas, suma bus apskaičiuojama kaip *Kiekis* × *Kaina*. Kitas palaikomas metodas yra **fiksuota kaina**. Kai naudojamas šis metodas, kaina bus nustatyta į sumą, o kiekis skaičiavime nebus naudojamas. | |
    | Vieneto grafikas ir vienetas | Kartu vieneto grafikas ir vienetas identifikuoja kiekio vienetą. | Vieneto ir operacijos kategorijos derinys naudojamas įvesti numatytąsias išlaidų kainas. Numatytoje projekto operacijų konfigūracijoje vieneto, vaidmens ir išteklių paskirstymo vieneto derinys naudojamas numatytoms laiko kainoms įvesti. Jei turite pasirinktinę numatytųjų kainų įvedimo konfigūraciją, ji bus naudojama kartu su vienetu. Produkto ir vieneto derinys naudojamas įvesti numatytąsias medžiagų kainas. |
    | Kiekis | Įveskite kiekį. | |
    | Kainos | Jei kuriant žurnalo eilutę kaina paliekama tuščia, atitinkamos vertės bus naudojamos nustatant numatytąsias kainas, atsižvelgiant į operacijos klasę. Jei kuriant žurnalo eilutę įvedama kaina, ta kaina bus naudojama. | |
    | Mokesčiai | Įveskite bet kokią mokesčio sumą. | Atsižvelgiant į įvestą mokesčio sumą, išplėsta suma bus skaičiuojama kaip *Sumos* + *mokestis*. |

## <a name="confirm-an-entry-journal"></a>Įrašų žurnalo patvirtinimas

Įrašę visas žurnalo eilutes į įrašų žurnalą, galite patvirtinti žurnalą. Šis procesas įrašys kiekvieną žurnalo eilutę kaip faktinius atitinkamų projektų įvykius.

Patvirtinus žurnalą, nebegalite jo ar jo eilučių redaguoti.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Faktiniai duomenys, sukurti įrašų žurnalo patvirtinimo

Yra keletas pagrindinių skirtumų tarp faktinių duomenų, kuriuos sukuria įrašo žurnalo patvirtinimas, ir faktinių duomenų, sukurtų tvirtinant laiko, išlaidų ir medžiagų naudojimo žurnalus bei SF patvirtinimą projekto operacijose:

- Įrašų žurnalai nenaudoja operacijų ryšių, kad susietų faktinę savikainą su faktiniais neapmokėtais pardavimais. Faktiniai duomenys, sukurti patvirtinus laiko, išlaidų ir medžiagų naudojimo žurnalus, visada naudoja operacijų ryšius, kad susietų savikainą ir neapmokėtus pardavimo faktinius duomenis.
- Įrašų žurnalai nenaudoja operacijų kilmės, kad susietų faktines išlaidas ir neapmokėtus pardavimo faktinius duomenis su bet kuriuo pradiniu įrašu. Faktinės aplinkybės, sukurtos patvirtinus laiko, išlaidų ir medžiagų naudojimo žurnalus, visada naudoja operacijos kilmę, kad susietų savikainą ir neapmokėtus pardavimo faktinius duomenis su pradiniu laiko įrašu.
- Kai įrašo žurnalo patvirtinimui sukuriamiems neapmokėtiems pardavimo faktams išrašoma SF, sf patvirtinimo metu sukurti pardavimo faktinės sumos, kurioms išrašyta SF, yra susietos su neapmokėtais pardavimo faktiniais duomenimis, panašiai kaip ir neapmokėti pardavimo faktiniai duomenys, kurie sukuriami tvirtinant laiko, išlaidų ir medžiagų naudojimo žurnalus.
- Įrašų žurnalo eilutės, sukurtos laikui, kurį įveda tarporganizaciniai ištekliai, automatiškai nesukuria išteklių vieneto savikainos **ir** **"Interorg Sales" tipų faktinių** duomenų. Šie faktiniai duomenys turi būti sukurti neautomatiniu būdu. Šis elgesys skiriasi nuo laiko įrašų, kuriuos įrašo tarporganizaciniai ištekliai, elgesio. Tokiu atveju, kai laikas patvirtinamas, programa automatiškai sukuria projekto savikainos **tipo** faktinius duomenis ir darbuotojo valdomo padalinio išteklių savikainos **bei**"Interorg Sales" tipų **faktinius** duomenis. Tada ji naudoja operacijų ryšius, kad susietų tuos faktinius duomenis ir sandorio kilmę, kad susietų juos su pradiniu laiko įrašu.
- Kai įrašų žurnalai patvirtinami, jie sukuria faktinius duomenis. Tačiau taisymo žurnalų negalima naudoti šiems faktams ištaisyti. Šis veikimo būdas skiriasi nuo faktinių duomenų, sukurtų patvirtinus laiko, išlaidų ir medžiagų naudojimo žurnalus, elgsenos. Tokiu atveju programa leidžia naudoti taisymo žurnalus faktams ištaisyti, kad ištaisytumėte klaidas, su sąlyga, kad šiems faktams dar neišrašyta SF. Jei jiems jau išrašyta SF, vis tiek galite ištaisyti faktinį dokumentą, jei apdorosite klientui visą faktinį kreditą.

> [!NOTE]
> Įvedimo žurnalai netaiko griežtų numatytųjų taisyklių. Todėl naudokite šiuos įrašų žurnalus kuo mažiau ir būkite atsargūs bei atsargūs, kad įsitikintumėte, jog savo sistemoje nesukuriate sugadintų finansinių duomenų. Kai tik galite, naudokite laiko, išlaidų ir medžiagų naudojimo žurnalus, projekto sutarčių etapo ir užlaikytojo nustatymą ir projekto SF patvirtinimo procesą, o ne įrašų žurnalus, kad sukurtumėte faktinius duomenis.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
