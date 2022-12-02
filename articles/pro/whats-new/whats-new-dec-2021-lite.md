---
title: Kas nauja 2021 m. gruodžio mėn. – „Project Operations lite“ visuotinis diegimas
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. gruodžio „Project Operations lite“ visuotinio diegimo leidime.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914090"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Kas nauja 2021 m. gruodžio mėn. – „Project Operations lite“ visuotinis diegimas

_Taikoma (kam): „Lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros kūrimą_

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.27.0.195, 4.27.0.242, 4.27.0.244 versijos „Dataverse“ aplinkoje


## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

### <a name="subcontract-management"></a>Subrangos sutarties valdymas 

- [Projekto komandos narių vertinimas: projekto](../subcontracting/subcontracting-project-team-members.md) vadovas gali kurti įvardytuosius arba bendrosios komandos narius su nedinga ir sustabdant linijas, kad galėtų paveikti darbuotojų skaičių ir vertinimą.
- [Projekto komandos narių](../subcontracting/subcon-options.md) pasirinkimo galimybių sprendimas: kai projekto vadovas renka įvardytuosius arba bendrosios projekto komandos narius, jis gali peržiūrėti esamus sprendimus arba sukurti naujus sprendimus vienam ar daugiau projekto komandos narių. 
- [Išlaidų vertinimas, kai](../subcontracting/costing-subcon-ra.md) ištekliai yra nenaudingi: projekto išlaidų vertinimas bus atliekamas atsižvelgiant į nenaudotus išteklių priskyrimus ir kainoraščius, susietus su papildomais ištekliais, jie kainuos. 
- [Sukonfigūruokite](../subcontracting/configure-sb-subcon.md) grafiko lentą, kad būtų rodomi sutarties darbuotojai ir reastruotas pajėgumas: dabar "Project Operations" grafiko lenta gali būti sukonfigūruota taip, kad būtų ieškoma ir siūloma rezervuotimų išteklių tipo sutarties darbuotojo ir kartu su darbuotojais persodintas pajėgumas. Šią konfigūraciją galima pritaikyti ieškant išteklių personalo pagal konkretų projekto reikalavimą arba ieškant ne projekto reikalavimo kontekste.
- [Projekto, kurį įgyvendinant dirba sutarčių darbuotojai, ir](../subcontracting/staffing-cw.md) darbuotojų, dirbančių su darbo rezultatais, skaičius: sutarčių darbuotojus dabar galima rezervuoti projektais, svertus grafiko lentos patiems.
- [Laiko, išlaidų ir medžiagos](../subcontracting/recording-subcon-actuals.md) naudojimo su projektais, skirtais išsaktyvūs komponentai, įrašymas: sutarčių darbuotojai gali įrašyti laiką ir išlaidas, o projekto komandos nariai taip pat gali įrašyti įsigytų medžiagos naudojimą projekto metu. Taip galėsite įrašyti tikslias projektų, kurių pajėgumas arba medžiaga yra įsigyti, išlaidas.
- [Būsenos perėjimai prie prisodinant: insvera esantys duomenys gali būti patvirtinti, kad pardavėjas](../subcontracting/subcon-states.md) užbaigė šią būseną, neįrašo pristatymo nurodymo arba atšauktas, kad prieš pristatant sutartį su pardavėju būtų nurodyta, jog ji yra užbaigta.

### <a name="task-planning"></a>Užduočių planavimas
- Pagerintas trikčių šalinimas sistemos administratoriams. Kai vartotojas negali atidaryti projekto, administratorius gali peržiūrėti „Project for the Web“ sugeneruotas ne su licencija susijusias klaidas [projektų planavimo žurnaluose](../../project-management/schedule-api-logs.md).
- [Naudokite „Microsoft Project for the Web“ užduočių kontrolinius sąrašus](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Programoje „Microsoft Project for the Web“ į užduotį galite įtraukti kontrolinį sąrašą ir sekti konkrečius elementus.

## <a name="quality-updates"></a>Kokybės naujinimai

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Planavimas ir stebėjimas | 2392596 | Planuoti API dabar leidžia naujinti likusių pastangų **užbaigtų** pastangų ir **užbaigtų** pastangų **laukus**. |
| Planavimas ir stebėjimas | 2478497 | Planuojant API veiklos **numerį** ir **užduoties ID** laukus įvesties duomenyse gali būti tušti, nes sistema juos užpildys naudodama automatinį numeravimą.|
| Laikas ir išlaidos | 2468135 | Patvirtinimo skaičius sumažinamas nuo penkių iki trijų. |
| Laikas ir išlaidos | 2468188 | Išspręsta problema, kylanti dėl to, kad žurnalo tekstas viršija maksimalų **anotacijų objekto** notetext **atributo** ilgį. |
