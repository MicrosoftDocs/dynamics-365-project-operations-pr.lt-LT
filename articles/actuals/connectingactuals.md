---
title: Operacijų ryšiai – skirtingų operacijų tipų faktinių duomenų susiejimas
description: Šiame straipsnyje paaiškinama, kaip operacijos ryšys naudojamas skirtingų tipų faktams susieti, kad būtų galima stebėti pelningumą, atsiskaitymo atsilikimą ir sąskaitų faktūrų, palyginti su neapmokėtais pajamų skaičiavimais.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926096"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Operacijų ryšiai – skirtingų operacijų tipų faktinių duomenų susiejimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Operacijos ryšio įrašai sukuriami siekiant susieti skirtingų tipų faktinius duomenis, nes laikas, išlaidos ar medžiagų naudojimas perkelia jo gyvavimo ciklą iš pasiūlymo arba išankstinio pardavimo etapo į sutarties etapą, patvirtinimus ir (arba) atšaukimus, SF išrašymą ir galimą kredito ar taisomosios SF išrašymą.

Toliau pateiktame pavyzdyje parodytas tipinis „Project Operations“ projekto ciklo laiko įrašų apdorojimas.

> ![Apdorojami laiko įrašai projekto operacijose.](media/basic-guide-17.png)

Projekto operacijų projekto gyvavimo ciklo laiko įrašų apdorojimas atliekamas šiais veiksmais: 

1. Pateikus laiko įrašą, sukuriamos dvi žurnalo eilutės: viena savikainai ir viena neapmokėtiems pardavimams. 
2. Patvirtinus laiko įrašą, sukuriami du faktiniai duomenys: vienas savikainai ir vienas neapmokėtiems pardavimams. Šie 2 faktiniai duomenys yra susieti naudojant operacijų ryšius.
3. Vartotojui kuriant projekto sąskaitą faktūrą, sąskaitos faktūros eilutės operacija sukuriama naudojant faktinės pardavimo, už kurį neišrašyta sąskaita, sumos duomenis.
4. Patvirtinus SF, sukuriami du nauji faktiniai duomenys: neapdorotas pardavimo atšaukimas ir faktinis pardavimas, kuriam išrašyta sf. Neapdorotas pardavimo atšaukimas ir pradinis neįregistruotas pardavimas faktinis yra prijungti naudojant atšaukiamus operacijų ryšius. Pardavimai, už kuriuos išrašytos sąskaitos, ir pradiniai neapmokėti pardavimo faktiniai duomenys taip pat yra susieti, kad būtų rodomi ryšiai tarp to, kas kažkada buvo neįvykdyta arba nebaigta darbo (NG) pajamų su tuo, kas dabar apmokestinama pajamomis.   

Kiekvienas apdorojimo darbo eigos įvykis suaktyvina įrašų kūrimą lentelėje **Operacijos ryšys**. Tai padeda sukurti ryšių tarp įrašų, sukurtų pagal laiko įrašą, žurnalo eilutę, faktinę ir SF eilutės informaciją, sekimą.

Šioje lentelėje rodomi ankstesnės darbo eigos objekto **Operacijos ryšio** įrašai.

|Įvykis                   |1 operacija                 |1 operacijos vaidmuo |1 operacijos tipas       |2 operacija          |2 operacijos vaidmuo |2 operacijos tipas |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Laiko įrašo pateikimas   |Žurnalo eilutės (pardavimo) GUID     |Pardavimas, už kurį neišrašyta sąskaita |msdyn_journalline            |Žurnalo eilutės (išlaidų) GUID     |Išlaidos            |msdyn_journalline  |
|Laiko patvirtinimas           |Faktinės sumos, už kurią neišrašyta sąskaita, GUID (pardavimas)  |Pardavimas, už kurį neišrašyta sąskaita |msdyn_actual                 |Faktinių išlaidų GUID (išlaidos)       |Išlaidos            |msdyn_actual       |
|Sąskaitos faktūros kūrimas        |Sąskaitos faktūros eilutės informacijos GUID      |Pardavimas, už kurį išrašyta sąskaita   |msdyn_invoicelinetransaction |Pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID   |Pardavimas, už kurį neišrašyta sąskaita  |msdyn_actual       |
|Sąskaitos faktūros patvirtinimas    |Faktinės sumos atšaukimo GUID         |Atšaukimas      |msdyn_actual                 |Pradinio pardavimo, už kurį neišrašyta sąskaita, GUID |Pradinis        |msdyn_actual       |
|                        |Pardavimo, už kurį išrašyta sąskaita, GUID             |Pardavimas, už kurį išrašyta sąskaita   |msdyn_actual                 |Pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID   |Pardavimas, už kurį neišrašyta sąskaita  |msdyn_actual       |
|Sąskaitos faktūros juodraščio koregavimas |Sąskaitos faktūros eilutės operacijos GUID|Pakeitimas      |msdyn_invoicelinetransaction |Pardavimo, už kurį išrašyta sąskaita, GUID            |Pradinis        |msdyn_actual       |
|Sąskaitos faktūros koregavimo patvirtinimas|Pardavimo, už kurį išrašyta sąskaita, atšaukimo GUID  |Atšaukimas      |msdyn_actual                 |Pardavimo, už kurį išrašyta sąskaita, GUID            |Pradinis        |msdyn_actual       |
|                        |Naujas neapmokėtas pardavimo GUID |Pakeitimas            |msdyn_actual                 |Pardavimo, už kurį išrašyta sąskaita, GUID            |Pradinis        |msdyn_actual       |


Toliau pateiktoje iliustracijoje rodomi saitai, sukurti tarp skirtingų tipų faktinių duomenų įvairiuose renginiuose, naudojant laiko įrašų pavyzdį projekto operacijose.

> ![Kaip skirtingų tipų aktualijos yra tarpusavyje susietos projekto operacijose.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
