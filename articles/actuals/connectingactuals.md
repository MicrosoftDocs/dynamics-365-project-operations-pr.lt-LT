---
title: Operacijų ryšiai – skirtingų operacijų tipų faktinių duomenų susiejimas
description: Šiame straipsnyje paaiškinta, kaip operacijų ryšys naudojamas skirtingų tipų faktiniams duomenims sujungti, kad būtų galima sekti pelningumą, atsiskaitymo nebaigtas užduotis ir pajamų, už kurias išrašyta sąskaita, palyginti su pajamomis, už kurias neišrašyta sąskaita, skaičiavimus.
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

Operacijų ryšio įrašai kuriami norint susieti skirtingų tipų faktinius duomenis, pvz., laiko, išlaidų ar medžiagos naudojimo trukmės pokyčius ciklo metu, nuo pasiūlymo arba etapo prieš pardavimą iki sutarties etapo, patvirtinimų ir (arba) atšaukimų, sąskaitų faktūrų išrašymo ir galimai kredito arba koreguojamųjų sąskaitą faktūrų išrašymo.

Toliau pateiktame pavyzdyje parodytas tipinis „Project Operations“ projekto ciklo laiko įrašų apdorojimas.

> ![Laiko įrašų apdorojimas programoje „Project Operations“.](media/basic-guide-17.png)

Laiko įrašų apdorojimas „Project Operations“ projekto cikle vykdomas atliekant šiuos veiksmus: 

1. Pateikus laiko įrašą sukuriamos dvi žurnalo eilutės: viena išlaidų eilutė ir viena pardavimo, už kurį neišrašyta sąskaita, eilutė. 
2. Galiausiai patvirtinus laiko įrašą, sukuriamos dvi faktinės sumos: viena išlaidų suma ir viena pardavimo, už kurį neišrašyta sąskaita, suma. Šie 2 faktiniai duomenys susiejami naudojant operacijų ryšius.
3. Vartotojui kuriant projekto sąskaitą faktūrą, sąskaitos faktūros eilutės operacija sukuriama naudojant faktinės pardavimo, už kurį neišrašyta sąskaita, sumos duomenis.
4. Patvirtinus sąskaitą faktūrą, sukuriamos dvi naujos faktinės sumos: pardavimo, už kurį neišrašyta sąskaita, atšaukimo suma ir faktinė pardavimo, už kurį išrašyta sąskaita, suma. Pardavimo, už kurį neišrašyta sąskaita, atšaukimo ir pradinio pardavimo, už kurį neišrašyta sąskaita, faktiniai duomenys sujungiami naudojant atšaukimo operacijos ryšius. Pardavimo, už kurį išrašyta sąskaita, ir pradinio pardavimo, už kurį neišrašyta sąskaita, faktiniai duomenys taip pat sujungiami, kad būtų parodyti ryšiai tarp to, kas anksčiau buvo nebaigtų užduočių arba vykdomo darbo (WIP) pajamos ir to, kas dabar yra pajamos, už kurias išrašyta sąskaita faktūra.   

Kiekvienas apdorojimo darbo eigos įvykis inicijuoja įrašų kūrimą lentelėje **Operacijos ryšys**. Tai padeda sukurti ryšių tarp įrašų, sukurtų laiko įrašuose, žurnalo eilutėse, faktiniuose duomenyse ir sąskaitos faktūros eilutės informacijos dalyje, sekimą.

Tolesnėje lentelėje pateikiami ankstesnės darbo eigos objekto **Operacijos ryšys** įrašai.

|Įvykis                   |1 operacija                 |1 operacijos vaidmuo |1 operacijos tipas       |2 operacija          |2 operacijos vaidmuo |2 operacijos tipas |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Laiko įrašo pateikimas   |Žurnalo eilutės (pardavimo) GUID     |Pardavimas, už kurį neišrašyta sąskaita |msdyn_journalline            |Žurnalo eilutės (išlaidų) GUID     |Išlaidos            |msdyn_journalline  |
|Laiko patvirtinimas           |Faktinės sumos, už kurią neišrašyta sąskaita, GUID (pardavimas)  |Pardavimas, už kurį neišrašyta sąskaita |msdyn_actual                 |Faktinių išlaidų GUID (išlaidos)       |Išlaidos            |msdyn_actual       |
|Sąskaitos faktūros kūrimas        |Sąskaitos faktūros eilutės informacijos GUID      |Pardavimas, už kurį išrašyta sąskaita   |msdyn_invoicelinetransaction |Pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID   |Pardavimas, už kurį neišrašyta sąskaita  |msdyn_actual       |
|Sąskaitos faktūros patvirtinimas    |Faktinės sumos atšaukimo GUID         |Atšaukimas      |msdyn_actual                 |Pradinio pardavimo, už kurį neišrašyta sąskaita, GUID |Pradinis        |msdyn_actual       |
|                        |Pardavimo, už kurį išrašyta sąskaita, GUID             |Pardavimas, už kurį išrašyta sąskaita   |msdyn_actual                 |Pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID   |Pardavimas, už kurį neišrašyta sąskaita  |msdyn_actual       |
|Sąskaitos faktūros juodraščio koregavimas |Sąskaitos faktūros eilutės operacijos GUID|Pakeitimas      |msdyn_invoicelinetransaction |Pardavimo, už kurį išrašyta sąskaita, GUID            |Pradinis        |msdyn_actual       |
|Sąskaitos faktūros koregavimo patvirtinimas|Pardavimo, už kurį išrašyta sąskaita, atšaukimo GUID  |Atšaukimas      |msdyn_actual                 |Pardavimo, už kurį išrašyta sąskaita, GUID            |Pradinis        |msdyn_actual       |
|                        |Naujo pardavimo, už kurį neišrašyta sąskaita, GUID |Pakeitimas            |msdyn_actual                 |Pardavimo, už kurį išrašyta sąskaita, GUID            |Pradinis        |msdyn_actual       |


Toliau pateiktoje iliustracijoje pavaizduoti saitai, sukurti tarp skirtingų faktinių duomenų tipų įvairiais, įvykus įvairiems įvykiams, naudojant „Project Operations“ laiko įrašų pavyzdį.

> ![Kaip skirtingų tipų faktiniai duomenys susiejami vieni su kitais programoje „Project Operations“.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
