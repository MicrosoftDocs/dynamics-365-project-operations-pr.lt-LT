---
title: Kas naujo 2021 m. gruodžio mėn.
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. gruodžio mėn.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942987"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Kas naujo 2021 m. gruodžio mėn.

_Taikoma (kam): „Lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros kūrimą_

Ši tema taikoma toliau pateiktiems Microsoft komponentams ir versijoms Dynamics 365 Project Operations:

- Projekto operacijos Dataverse aplinkos versijoje 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

### <a name="subcontract-management"></a>Subrangos valdymas 

- [Subrangos projekto komandos nariai](../subcontracting/subcontracting-project-team-members.md) : Projekto vadovas gali sukurti įvardytus arba bendruosius komandos narius su subrangos ir subrangos linijomis, kad paveiktų personalą ir įvertinimą.
- [Projekto komandos narių subrangos parinktys](../subcontracting/subcon-options.md) : rinkdamas darbuotojų pasirinkimus įvardytiems ar bendriems projekto komandos nariams, projekto vadovas gali peržiūrėti esamas subrangovas arba sukurti naujų subrangų vienam ar daugiau projekto komandos narių. 
- [Subrangos išteklių priskyrimų išlaidų įvertinimas](../subcontracting/costing-subcon-ra.md) : Projekto išlaidų įvertinimas atsižvelgs į subrangos išteklių priskyrimus ir kainuos juos naudodamas pirkimo kainoraščius, susietus su subrangovais. 
- [Konfigūruoti grafiko lentą, kad būtų rodomi sutartininkai ir subrangos pajėgumai](../subcontracting/configure-sb-subcon.md) : projekto operacijų grafiko lenta dabar gali būti sukonfigūruota ieškoti ir siūlyti sutarties darbuotojo turimus rezervuojamų išteklių tipą ir subrangos pajėgumus kartu su darbuotojais. Ši konfigūracija gali būti taikoma ieškant išteklių konkretaus projekto poreikio personalo kontekste arba ieškant ne projekto poreikio kontekste.
- [Projekto personalas su sutartininkais ir subrangos](../subcontracting/staffing-cw.md) pajėgumais : Sutartininkai dabar gali būti rezervuoti projektams, kuriuose pasinaudojama tvarkaraščio valdybos patirtimi.
- [Laiko, išlaidų ir medžiagų naudojimo įrašant subrangos komponentų](../subcontracting/recording-subcon-actuals.md) projektuose: sutartininkai gali įrašyti laiką ir išlaidas, o projekto komandos nariai taip pat gali įrašyti medžiagų, įsigytų naudojant subrangovą projekte, naudojimą. Tai leis įrašyti tikslias išlaidas projektams, kuriuose naudojami įsigyti pajėgumai ar medžiagos.
- [Valstybės perėjimai subrangos](../subcontracting/subcon-states.md) sutartimi: Subrangos sutartys gali būti patvirtintos užbaigti derybas su tiekėju, uždarytos, kad būtų nurodytas pristatymo užbaigimas, arba atšauktos, kad būtų nurodyta sutarties su pardavėju nutraukimas prieš baigiant pristatymą.

### <a name="task-planning"></a>Užduočių planavimas
- Patobulinta sistemos administratorių trikčių diagnostika. Kai vartotojas negali atidaryti projekto, administratorius gali peržiūrėti su licencija nesusijusias klaidas, sugeneruotas iš projekto žiniatinklyje [projekto planavimo žurnaluose](../../project-management/schedule-api-logs.md).
- [Naudokite užduočių kontrolinius sąrašus programai Microsoft Project žiniatinklyje](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Programoje "Microsoft Project for the web" galite įtraukti kontrolinį sąrašą prie užduoties, kad galėtumėte sekti konkrečius elementus.

## <a name="quality-updates"></a>Kokybės naujinimai

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Planavimas ir stebėjimas | 2392596 | Planuoti API dabar leidžia atnaujinti **likusius laukus Pastangos**, Pastangos ir % **·** **Baigti**. |
| Planavimas ir stebėjimas | 2478497 | Suvestinės API **veiklos numeris ir užduoties ID** **laukai** įvesties metu gali būti tušti, nes sistema juos apgyvendins naudodama automatinį numeravimą.|
| Laikas ir išlaidos | 2468135 | Patvirtinimo pakartojimų skaičius sumažinamas nuo penkių iki trijų. |
| Laikas ir išlaidos | 2468188 | Išsprendė problemą, kai žurnalo tekstas viršija **maksimalų** komentaro objekto pastabų atributo **ilgį.** |
