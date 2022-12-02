---
title: Mobiliųjų įrenginių programėlė „Project Timesheet“
description: Šiame straipsnyje pateikiama informacija apie mobiliųjų įrenginių programėlę „Microsoft Dynamics 365 Project Timesheet“. Mobiliųjų įrenginių programėlė „Project Timesheet“ leidžia vartotojams pateikti ir tvirtinti projektų grafikus mobiliuosiuose įrenginiuose.
author: abruer
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 730ed36841d07df60e8a8f343126209f0edcc593
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110985"
---
# <a name="project-timesheet-mobile-application"></a>Mobiliųjų įrenginių programėlė „Project Timesheet“

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Apžvalga

Mobiliųjų įrenginių programėlė „Microsoft Dynamics 365 Project Timesheet“ leidžia vartotojams pateikti ir tvirtinti projektų grafikus mobiliuosiuose įrenginiuose („iPhone“ arba „Android“). Ši mobiliųjų įrenginių programėlė apima grafiko funkcionalumą, esantį „Dynamics 365 Finance“ projektų valdymo ir apskaitos srityje. Ji padeda gerinti vartotojų produktyvumą ir efektyvumą, taip pat leidžia laiku teikti ir tvirtinti projektų grafikus.

## <a name="download-and-install-the-mobile-app"></a>Mobiliųjų įrenginių programėlės atsisiuntimas ir įdiegimas

Atsisiųskite ir įdiekite mobiliųjų įrenginių programėlę „Microsoft Dynamics 365 Project Timesheet“, skirtą „Android“ arba „iPhone“, iš jūsų įrenginio mobiliosios parduotuvės.

## <a name="enable-the-app"></a>Programėlės įgalinimas 

Programoje „Finance“ turi būti įgalinta Mobiliųjų įrenginių programėlė „Project Timesheet“. Norėdami įjungti šias funkcijas, pereikite į **Projektų valdymo ir apskaitos parametrai \> Grafikas** ir pažymėkite parametrą **Įgalinti „Microsoft Dynamics 365 Project Timesheet“**.

### <a name="resolve-sign-in-issues"></a>Prisijungimo problemų sprendimas

**Problema:** prisijungę prie „Project Timesheet" mobiliųjų įrenginių programėlės, vartotojai gauna klaidos pranešimą, kuriame nurodyta, kad jie „negali pasiekti šio nuomotojo programėlės „2bc50526-cdc3-4e36-a970-c284c34cbd6e“.

**Problema:** vartotojui prisijungiant prie „Project Timesheet" mobiliųjų įrenginių programėlės įvyksta klaida, panaši į vieną iš šių pavyzdžių:

- „AADSTS50020: vartotojo abonemento „[vartotojo vardas]“ iš tapatybės tiekėjo „https://sts.windows.net/[programos ID]“ nėra nuomotojuje „[nuomotojo ID]“ ir negali pasiekti šio nuomotojo programos [programos ID]".
- „Pasirinktos vartotojo paskyros nėra nuomotojuje „[nuomotojo id]“ ir negalima pasiekti programos „[programos id]“ šiame nuomotojuje“?

**Paaiškinimas:** šių problemų priežastis yra „Azure Active Directory (Azure AD)“ 2022 m. gegužės m. atliktas pakeitimas, susijęs su išoriniais vartotojais. Kadangi šis pakeitimas nebuvo atliktas finansavimo ir operacijų programose, jis gali turėti įtakos klientams bet kurioje platformos ar programos versijoje.

**Sprendimas:** visi išoriniai vartotojai turi būti pakviesti į nuomotoją naudojant „Azure AD“. Daugiau informacijos rasite: [Kviesti vartotojus su „Azure Active Directory“ B2B kolaboracijai](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration).

## <a name="sign-in-to-the-app"></a>Prisijungimas prie programėlės

1.  Mobiliajame įrenginyje paleiskite mobiliųjų įrenginių programėlę.

2.  Įveskite savo „Finance“ URL.

3.  Pirmą kartą prisijungdami, būsite paraginti įvesti vartotojo vardą ir slaptažodį. Įveskite savo kredencialus.

4. Prisijungsite prie numatytosios įmonės.

## <a name="submit-a-project-timesheet"></a>Projekto grafiko pateikimas

Programėlėje galite sukurti ir pateikti projekto grafiką. Naują grafiką galite sukurti, remdamiesi ankstesnio grafiko, įrašytų eilučių arba projektų priskyrimų informacija. Jei esate paskirtas atstovu, taip pat galite įvesti kito darbuotojo grafiką. Norėdami sukurti grafiką kaip atstovas, pasirinkite mygtuką **Meniu**, tada pasirinkite ištekliaus pavadinimą.

Grafikų puslapyje bus sukurtas naujas grafiko laikotarpio, pagrįsto šiandienos data, grafikas. Bus rodoma darbo savaitė. Jei grafiko laikotarpis apima kelias savaites, galite pasirinkti kitą darbo savaitę iš darbo savaičių skirtukų.
Jei šiandienos datos grafikas jau yra, jis bus rodomas. Jei norite sukurti naują grafiką kitu grafiko laikotarpiu, pažymėkite mygtuką **Meniu**, paskui pažymėkite **Naujas grafikas**.

Įveskite projekto informaciją, spustelėję veiksmą **Įtraukti laiką** arba veiksmą **Kopijuoti laiką iš**. Pasirinkus veiksmą **Kopijuoti laiką iš**, bus kopijuojama projekto eilutės informacija, bet ne valandos. Meniu **Kopijuoti laiką iš** yra toliau pateikiamos parinktys.

- **Kopijuoti iš esamo grafiko** – kopijuoti grafiko eilutes iš esamo grafiko.

- **Kopijuoti iš parankinių** – kurti naujas grafiko eilutes naudojant grafiko parametrus, pažymėtus kaip parankinius.

- **Kopijuoti iš priskyrimo** – kurti naujas grafiko eilutes pagal priskirtus projektus.

Rodoma projekto informacija priklauso nuo mobiliųjų parametrų, kuriuos nustatėte puslapyje **Projektų valdymo ir apskaitos parametrai**.

Lauke **Juridinis subjektas** pasirinkite juridinį subjektą, kuriam atlikote projekto darbą. Lauką **Juridinis subjektas** galima naudoti tik tuo atveju, jei įjungtas juridinio subjekto įmonių tarpusavio grafikų palaikymas.

Pasirinkite klientą, susietą su grafiko projektu. Pradiniame leidime sistemoje „Android“ klientų įrašai nepalaikomi, nes pirmiausia turite pasirinkti projektą. Jei pirmiausia pasirinkote projektą, laukas **Klientas** užpildomas automatiškai.

Laukelyje **Projektas** pasirinkite projektą, kurio laiką įvedate. Laukas **Klientas** užpildomas automatiškai.

Klientų ir projektų peržvalgos leidžia ieškoti ir tarp klientų, ir tarp projektų.

Jei reikia, pažymėkite informaciją laukuose **Kategorija**, **Veikla**, **Eilutės ypatybė**, **PVM grupė** ir **Prekės PVM grupė**. Šiuos laukus galima perrašyti.

Lauke **Eilutės ypatybė** bus nustatyta numatytoji reikšmė pagal projektų valdymo ir apskaitos parametrus. Įjungus projekto / kategorijos ir kategorijos / ištekliaus parametrus, bus nustatyta numatytoji reikšmė **Eilutės ypatybė**, apibrėžta šiame tikrinime. Kai projekto / kategorijos ir kategorijos / ištekliaus parametrai nėra įjungti, numatytoji reikšmė **Eilutės ypatybė** bus nustatoma pagal lauką **Įgalinti numatytąją eilutės ypatybę** puslapyje **Projektų valdymo ir apskaitos parametrai**. Reikšmę **Eilutės ypatybė** galima perrašyti.

Pasirinkite dieną ir įtraukite laiką. Įveskite valandų, kurias dirbote kiekvieną dieną, skaičių.

Norėdami įtraukti komentarų apie įvedamas valandas, spustelėkite **Įtraukti komentarų**, tada įveskite komentarus, skirtus naudoti įmonės viduje, skirtus klientams, arba skirtus abiems auditorijoms.
Vidaus naudojimui skirtus komentarus gali peržiūrėti projektų vadovai. Komentarai klientams įtraukiami į sąskaitas faktūras.

Norėdami įrašyti eilutę kaip parankinę, pažymėkite žymės langelį, tada spustelėkite **Įrašyti kaip parankinę**.

Finansinių dimensijų ir priedų palaikymas mobiliųjų įrenginių programėlėje nesuteikiamas.

Pagal poreikį įtraukite daugiau projekto eilučių, kad grafikas būtų užbaigtas.

Spustelėkite **Pateikti** ir siųskite grafiką į patvirtinimo darbo eigą.

## <a name="review-timesheets"></a>Grafikų peržiūra

Grafikų, kuriuos reikia peržiūrėti, sąrašas pateikiamas meniu. Ši parinktis galima tik tada, jei buvote paskirtas darbo eigos tvirtintoju. Palaikomas ir antraštės, ir eilutės patvirtinimas. Eilutės lygio patvirtinimas siūlo galimybę pažymėti vieną ar keletą tvirtinamų eilučių. Peržiūrėję grafiko informaciją, spustelėkite **Patvirtinti**, **Paskirti atstovą** arba **Grįžti** ir tęskite darbo eigą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
