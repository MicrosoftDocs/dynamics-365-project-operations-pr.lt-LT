---
title: Įrašų žurnalų kūrimas ir patvirtinimas
description: Šiame straipsnyje pateikta informacija apie tai, kaip sukurti ir patvirtinti įrašų žurnalus programoje „Microsoft Dynamics 365 Project Operations“.
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

Įrašų žurnalus naudojate norėdami faktinius duomenis įrašyti tiesiogiai „Microsoft Dynamics 365 Project Operations“. Kai naudojate įrašų žurnalus, programoje „Project Operations“ nereikia įvesti laiko, išlaidų ir medžiagų naudojimo žurnalų.

Naudodami vieną įrašų žurnalą galite kurti kelias žurnalo eilutes. Kai žurnalas patvirtinamas, įrašų žurnalo eilutėje įrašomi faktiniai duomenys pagal toliau nurodytą informaciją.

- Išlaidos arba pajamos, atsižvelgiant į pasirinktą operacijos tipą.
- Pasirinkta operacijos klasė. Galimos klasės: **Laikas**, **Išlaidos**, **Medžiaga**, **Išankstinis apmokėjimas** **Etapas** ir **Mokestis**.
- Projektas ir (arba) užduotis, pasirinkta žurnalo eilutėje.

Norėdami sukurti „Project Operations“ įrašų žurnalą, atlikite toliau nurodytus veiksmus.

1. Eikite į **Pardavimas** \> **Operacijos** \> **Žurnalai**.
2. Sąrašo puslapio **Įrašų žurnalai** veiksmų srityje pasirinkite **Naujas**, kad sukurtumėte žurnalą.
3. Puslapio **Naujas žurnalas** lauke **Aprašas** įveskite žurnalo aprašą.
4. Įsitikinkite, kad lauko **Žurnalo tipas** reikšmė nustatyta kaip **Įrašas**, tada pasirinkite **Įrašyti**. Įrašius naują įrašų žurnalą, žurnalų puslapyje turi būti rodomas skirtukas **Žurnalo eilutės**.
5. Skirtuke **Žurnalo eilutės**, virš tinklelio esančioje įrankių juostoje, pasirinkite **Naujas**, kad sukurtumėte įrašų žurnalo eilutę.
6. Dialogo lange **Spartusis kūrimas**, skirtame įvesties žurnalo eilutėms kurti, nustatykite laukus, kaip aprašyta toliau pateiktoje lentelėje.

    | Laukas | Aprašą | Funkcinis poveikis |
    | --- | --- | --- |
    | Operacijos klasė | Žurnalo eilutė gali būti priskirta vienai iš šešių operacijų klasių: **Laikas**, **Išlaidos**, **Medžiaga**, **Išankstinis apmokėjimas**, **Etapas** arba **Mokestis**. | Operacijų klasė **Mokestis** programoje „Project Operations“ nebenaudojama. <br> Jei sukursite operacijų klasę **Mokestis**, ji nebus apdorojama išrašant sąskaitą faktūrą arba skaičiuojant išlaidas arba pajamas. **Etapas** yra tik pajamų operacijų klasė. <br>Operacijų klasė **Išankstinis apmokėjimas** nurodo avansą, gautą iš kliento. Jis visada turėtų būti kuriamas kaip pardavimo, už kurį išrašyta sąskaita, ir pardavimo, už kurį neišrašyta sąskaita, žurnalo eilučių pora. |
    | Operacijos tipas | Operacijų tipai **Savikaina**, **Pardavimas tarp organizacijų** ir **Išteklių paskirstymo vieneto savikaina** turi būti naudojami įrašant išlaidas.<br> Operacijų tipai **Pardavimas, už kurį neišrašyta sąskaita** ir **Pardavimas, už kurį išrašyta sąskaita** turi būti naudojami įrašant pajamas. | Operacijų klasė **Išankstinis apmokėjimas** veikia tik su operacijų tipais **Pardavimas, už kurį išrašyta sąskaita** ir **Pardavimas, už kurį neišrašyta sąskaita**.<br> Operacijų klasė **Etapas** veikia tik su operacijos tipu **Pardavimas, už kurį išrašyta sąskaita**. <br>Operacijų tipai **Pardavimas tarp organizacijų** ir **Išteklių paskirstymo vieneto savikaina** taikomi tik operacijų klasei **Laikas** ir jie yra tik įrašų žurnaluose „Lite“ visuotinio diegimo scenarijuje, bet jų nėra diegiant „Project Operations“ išteklių / nelaikomų medžiagų scenarijuose. |
    | Pasirinkti produktą | Kai pasirinkta operacijų klasė **Medžiaga**, šiame lauke galite nurodyti, ar medžiagos operacija, kuriai kuriate žurnalo eilutę, yra esamas produktas ar įtraukiamasis produktas. | Jei pasirinksite **Įtraukiamasis produktas**, galėsite įvesti produkto pavadinimą. |
    | Produktas | Nuoroda į produktą iš katalogo. | |
    | Aprašą | Žurnalo eilutės aprašas, kad būtų lengviau ją identifikuoti. | Pardavimo, už kurį neišrašyta sąskaita, žurnalo eilutėms ši reikšmė bus naudojama kaip aprašas, kai bus kuriama sąskaitos faktūros eilutės išsami informacija. |
    | Išorinis aprašas | Žurnalo eilutės aprašas, kurį galima naudoti bendrinant su išorine suinteresuotąja šalimi. | Pardavimo, už kurį neišrašyta sąskaita, žurnalo eilutėms ši reikšmė bus naudojama kaip išorinis aprašas, kai bus kuriama sąskaitos faktūros eilutės išsami informacija. Jis taip pat gali būti rodomas klientui išsiųstoje sąskaitoje faktūroje. |
    | Atsiskaitymo tipas | Reikšmė, nurodanti, ar žurnalo eilutė projekte bus skaičiuojama kaip apmokestinamas, nemokamas arba neapmokestinamas komponentas. | Įprastame sraute atsiskaitymo tipas išvedamas pagal sutartyje nustatytas sutartas sąlygas. Tačiau į šį lauką galite įvesti reikšmę, kai įrašote žurnalo eilutę. |
    | Dokumento data | Naudokite datą, kai įvyko operacija. | |
    | Pradžios data | Naudokite datą, kai įvyko operacija. | Šis laukas naudojamas palyginimui su sąskaitos faktūros sukūrimo data, kai operacijos tipas yra **Pardavimas, už kurį neišrašyta sąskaita**. Šis palyginimas padės nuspręsti, ar operacijos data ateityje ar praeityje. Į sąskaitą faktūrą bus pridėtos tik operacijos su data praeityje. |
    | Pabaigos data | Naudokite datą, kai įvyko operacija. | |
    | Apskaitos data | Naudokite šią datą, kai bus įrašomas apskaitos poveikis. | |
    | Sutarties eilutės klientas | Pagal numatytuosius nustatymus, jei sutarties eilutėje yra tik vienas klientas, įrašant žurnalo eilutę šis laukas nustatomas klientui, esančiam sutarties eilutėje. Jei sutarties eilutėje yra keli klientai, sutarties eilutėje pasirinkite tinkamą klientą. | Jei sistema žurnalo eilutėje negali nustatyti sutarties eilutės kliento ir, jei jis būna tuščias tipo **Pardavimas, už kurį neišrašyta sąskaita** faktiniuose duomenyse, kurie kuriami iš žurnalo eilutės, šie faktiniai duomenys nebus įtraukti į sąskaitą faktūrą. |
    | Project | Pasirinkite projektą, į kurį norite įrašyti faktinius duomenis. | Pagal pasirinktą projektą, operacijų klasę ir užduotį sistema bandys nustatyti sutartį, sutarties eilutę ir sutarties eilutės klientą. |
    | Užduotis | Pasirinkite užduotį, į kurį norite įrašyti faktinius duomenis. | Jei sutarties nustatymo metu susiejote užduotis su sutarties eilutėmis, sistema naudos pasirinktą užduotį kartu su projektu ir operacijų klase norėdama nustatyti sutartį, sutarties eilutę ir sutarties eilutės klientą. |
    | Operacijos kategorija | Pasirinkite operacijos kategoriją, į kurią norite įrašyti faktinius duomenis. | Dėl išlaidų pasirinkta operacijos kategorija nustato numatytąją kainą, kuri įrašant bus įvesta į žurnalo eilutę. |
    | Vaidmuo | Šis laukas yra susijęs su laiko žurnalo eilutėmis. Pasirinkite ištekliaus, kuris skyrė laiką projektui ir (arba) užduočiai, vaidmenį. | Dėl laiko žurnalo eilučių: jei naudojate iš anksto parengtą konfigūraciją numatytųjų išteklių išlaidoms ir sąskaitų tarifams įvesti, pažymėtas vaidmuo naudojamas kartu su išteklių paskirstymo vienetu, kad būtų nustatyta numatytoji kaina, kuri įrašant bus įvesta į žurnalo eilutę. Jei naudojate pasirinktinę numatytųjų kainų įvedimo konfigūraciją, turite peržiūrėti šią konfigūraciją ir nustatyti, ar laukas **Vaidmuo** naudojamas numatytosios kainos reikšmėms įvesti. |
    | Subrangos sutartis | Jei žurnalo eilutė nurodo subrangos sutarties pajėgumą arba subrangos sutarties išlaidas ar medžiagas, pasirinkite atitinkamą subrangos sutartį. | Kai išlaidų žurnalo sąrašo eilutės bus įrašomos, pasirinkta subrangos sutartis nustatys kainoraštį, naudojamą numatytajai vieneto savikainai įvesti. |
    | Subrangos sutarties eilutė | Jei žurnalo eilutė nurodo subrangos sutarties pajėgumą arba subrangos sutarties išlaidas ar medžiagas, pasirinkite atitinkamą subrangos sutarties eilutę. | Įrašius išlaidų žurnalo eilutes, pasirinkta subrangos sutarties eilutė užtikrins, kad būtų tinkamai atlikti galimo pajėgumo skaičiavimai pagal subrangos sutarties eilutę. |
    | Sumos metodas | Pagal numatytuosius nustatymus šio lauko reikšmė nustatyta kaip **Dauginti kiekį iš kainos**. Kai naudojamas šis metodas, suma bus apskaičiuojama kaip *Kiekis* × *Kaina*. Kitas palaikomas metodas yra **Fiksuota kaina**. Kai naudojamas šis metodas, kaina nustatoma kaip suma, o kiekis skaičiuojant naudojamas. | |
    | Vieneto grafikas ir vienetas | Kartu vieneto grafikas ir vienetas identifikuoja kiekio vienetą. | Vieneto ir operacijos kategorijos derinys naudojamas numatytosioms kainoms pagal išlaidas įvesti. Numatytojoje „Project Operations“ konfigūracijoje vieneto, vaidmens ir išteklių paskirstymo vieneto derinys naudojamas numatytosioms kainoms pagal laiką įvesti. Jei turite pasirinktinę numatytųjų kainų įvedimo konfigūraciją, ji bus naudojama kartu su vienetu. Produkto ir vieneto derinys naudojamas medžiagos numatytųjų kainų įvedimui. |
    | Kiekis | Įveskite kiekį. | |
    | Kainos | Jei kuriant žurnalo eilutę kaina paliekama tuščia, įvedant numatytąsias kainas bus naudojamos atitinkamos reikšmės, atsižvelgiant į operacijos klasę. Jei kuriant žurnalo eilutę kaina įvedama, bus naudojama ta kaina. | |
    | Mokesčiai | Įveskite bet kokią mokesčių sumą. | Atsižvelgiant į įvestą mokesčio sumą, bus apskaičiuota išplėstinė suma kaip *Suma* + *Mokestis*. |

## <a name="confirm-an-entry-journal"></a>Įrašų žurnalo patvirtinimas

Kai į įrašų žurnalą įvesite visas žurnalo eilutes, galėsite žurnalą patvirtinti. Šis procesas įrašys kiekvieną žurnalo eilutę kaip faktinius atitinkamų projektų duomenis.

Kai žurnalas bus patvirtintas, nebegalėsite redaguoti jo ir jokių jo eilučių.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Faktiniai duomenys, sukurti patvirtinant įrašų žurnalą

Yra keli pagrindiniai skirtumai tarp faktinių duomenų, kurie sukuriami patvirtinant įrašų žurnalą, ir faktinių duomenų, kurie sukuriami patvirtinant laiko, išlaidų ir medžiagos naudojimo žurnalus bei sąskaitą faktūrą programoje „Project Operations“:

- Įrašų žurnalai nenaudoja operacijų ryšių, kad susietų išlaidų faktinius duomenis su pardavimo, už kurį neišrašyta sąskaita, faktiniais duomenimis. Faktiniai duomenys, kurie sukuriami patvirtinus laiko, išlaidų ir medžiagos naudojimo žurnalus, visada naudoja operacijų ryšius, kad susietų išlaidas ir pardavimo, už kurį neišrašyta sąskaita, faktinius duomenis.
- Įrašų žurnalai nenaudoja operacijų kilmės, kad susietų išlaidų faktinius duomenis ir pardavimo, už kurį neišrašyta sąskaita, faktinius duomenis su jokiu pradiniu įrašu. Faktiniai duomenys, kurie sukuriami patvirtinus laiko, išlaidų ir medžiagos naudojimo žurnalus, visada naudoja operacijų kilmę , kad susietų išlaidas ir pardavimo, už kurį neišrašyta sąskaita, faktinius duomenis su pradiniu laiko įrašu.
- Kai pardavimo, už kurį neišrašyta sąskaita, faktiniai duomenys, sukurti patvirtinant įrašų žurnalą, įtraukiami į sąskaitą faktūrą, pardavimo, už kurį išrašyta sąskaita, faktiniai duomenys, sukurti patvirtinant sąskaitą faktūrą, susiejami su pardavimo, už kurį neišrašyta sąskaita, faktiniais duomenimis, panašiai kaip ir su pardavimo, už kurį neišrašyta sąskaita, faktiniais duomenimis, sukurtais patvirtinant laiko, išlaidų ir medžiagos naudojimo žurnalus.
- Įrašų žurnalo eilutės, sukurtos pagal laiką, įvedamą organizacijų išteklių, automatiškai nesukuria faktinių duomenų, kurių tipas **Išteklių paskirstymo vieneto savikaina** ir **Pardavimas tarp organizacijų**. Šiuos faktinius duomenis reikia sukurti rankiniu būdu. Šis veikimo būdas skiriasi nuo laiko įrašų, kuriuos įrašo organizacijų ištekliai, veikimo būdo. Tokiu atveju, kai laikas patvirtinamas, programa automatiškai sukuria projekto faktinius duomenis, kurių tipas **Savikaina**, ir darbuotojo padalinio faktinius duomenis, kurių tipas **Išteklių paskirstymo vieneto savikaina** ir **Pardavimas tarp organizacijų**. Tada programa naudoja operacijos ryšius, kad susietų tuos faktinius duomenis ir operacijų kilmę, o tada juos susietų su pradiniu laiko įrašu.
- Kai patvirtinami įrašų žurnalai, jie sukuria faktinius duomenis. Tačiau tiems faktiniams duomenims taisyti negalima naudoti koregavimo žurnalų. Šis veikimo būdas skiriasi nuo faktinių duomenų, kurie sukuriami patvirtinant laiko, išlaidų ir medžiagos naudojimo žurnalus, veikimo būdo. Tokiu atveju programa leidžia naudoti koregavimo žurnalus, kad pakoreguotumėte faktinius duomenis norėdami ištaisyti klaidas tais atvejais, kai tie faktiniai duomenys dar nebuvo įtraukti į sąskaitą faktūrą. Jei jie jau buvo įtraukti į sąskaitą faktūrą, faktinius duomenis vis tiek galite pataisyti, jei klientui apdorojate visą tų faktinių duomenų kreditą.

> [!NOTE]
> Įrašų žurnalai nereikalauja griežtų numatytojo vykdymo taisyklių. Todėl naudokite šiuos įrašų žurnalus kuo rečiau ir būkite atsargūs, kad savo sistemoje nesukurtumėte iškraipytų finansinių duomenų. Visada, kai galite, naudokite laiko, išlaidų ir medžiagos naudojimo žurnalus, projekto sutarčių etapų ir išankstinio apmokėjimo sąranką ir projekto sąskaitos faktūros patvirtinimo procesą, o ne įrašų žurnalus, kad sukurtumėte faktinius duomenis.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
