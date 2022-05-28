---
title: Kas naujo 2021 m. gruodžio mėn.
description: Šioje temoje pateikiama informacija apie kokybės atnaujinimus, kuriuos galima rasti 2021 m. gruodžio mėn.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585388"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Kas naujo 2021 m. gruodžio mėn.

_Taikoma (kam): „Lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros kūrimą_

Ši tema taikoma šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- Projekto operacijos aplinkos versijoje Dataverse 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

### <a name="subcontract-management"></a>Subrangos sutarčių valdymas 

- [Subrangos projekto komandos nariai](../subcontracting/subcontracting-project-team-members.md): projekto vadovas gali sukurti įvardytus arba bendruosius komandos narius su subrangos sutartimis ir subrangos linijomis, kad paveiktų personalą ir vertinimą.
- [Subrangos parinktys projekto komandos nariams](../subcontracting/subcon-options.md): pasirinkdamas darbuotojų skaičių vardiniams arba bendriesiems projekto komandos nariams, projekto vadovas gali peržiūrėti esamas subrangos sutartis arba sukurti naujas subrangos sutartis vienam ar keliems projekto komandos nariams. 
- [Subrangos išteklių priskyrimų savikainos įvertinimas: projekto savikainos](../subcontracting/costing-subcon-ra.md) įvertinimas atsižvelgs į subrangos pagrindu sudarytų išteklių priskyrimus ir kainuos jiems naudojant pirkimo kainoraščius, susietus su subrangos sutartimis. 
- [Konfigūruokite grafiko lentą, kad būtų rodomi sutartininkai ir subrangos pajėgumai](../subcontracting/configure-sb-subcon.md): "Project Operations" grafiko lentą dabar galima sukonfigūruoti taip, kad kartu su darbuotojais būtų ieškoma ir siūloma sutartininko rezervuotų išteklių ir subrangos pajėgumų tipas. Ši konfigūracija gali būti taikoma ieškant išteklių, susijusių su konkretaus projekto reikalavimo personalu, arba ieškant už projekto reikalavimo ribų.
- [Projekto, kuriame dirba sutartininkai ir subrangovų pajėgumai](../subcontracting/staffing-cw.md), įdarbinimas: sutartininkai dabar gali būti įtraukti į projektus, kuriuose naudojama tvarkaraščio valdybos patirtis.
- [Laiko, išlaidų ir medžiagų naudojimo registravimas subrangos komponentų projektuose: sutartininkai](../subcontracting/recording-subcon-actuals.md) gali įrašyti laiką ir išlaidas, o projekto komandos nariai taip pat gali įrašyti medžiagų, įsigytų naudojant subrangos sutartį, naudojimą projekte. Dėl to bus registruojamos tikslios projektų, kuriuose naudojami įsigyti pajėgumai ar medžiagos, išlaidos.
- [Būsenos perėjimai pagal subrangos sutartį](../subcontracting/subcon-states.md): subrangos sutartys gali būti patvirtintos kaip baigtos derybos su tiekėju, uždarytos, kad būtų nurodytas pristatymo užbaigimas, arba atšauktos, kad būtų nurodyta sutarties su tiekėju nutraukimas prieš užbaigiant pristatymą.

### <a name="task-planning"></a>Užduočių planavimas
- Patobulintas sistemos administratorių trikčių šalinimas. Kai vartotojas negali atidaryti projekto, administratorius gali peržiūrėti su licencija nesusijusias klaidas, sugeneruotas iš "Project for the web" "Project" planavimo [žurnaluose](../../project-management/schedule-api-logs.md).
- [Naudokite užduočių kontrolinius sąrašus programoje "Microsoft Project" žiniatinklyje](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Programoje "Microsoft Project", skirtoje žiniatinkliui, galite įtraukti kontrolinį sąrašą į užduotį, kad galėtumėte sekti konkrečius elementus.

## <a name="quality-updates"></a>Kokybės naujinimai

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Planavimas ir stebėjimas | 2392596 | Planuoti API dabar leidžia atnaujinti **laukus Pastangos likusios**, **Atliktos** pastangos ir **% Baigta**. |
| Planavimas ir stebėjimas | 2478497 | Planavimo API **veiklos numeris** ir **užduoties ID** laukai gali būti tušti įvedant, nes sistema juos užpildys naudodama automatinį numeravimą.|
| Laikas ir išlaidos | 2468135 | Pakartotinių patvirtinimų skaičius sumažinamas nuo penkių iki trijų. |
| Laikas ir išlaidos | 2468188 | Išsprendė problemą, kai žurnalo tekstas viršijo maksimalų komentaro objekto pastabų teksto **atributo** **ilgį**. |
