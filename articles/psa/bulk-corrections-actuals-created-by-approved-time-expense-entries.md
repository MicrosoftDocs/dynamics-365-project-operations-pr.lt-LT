---
title: Faktinių duomenų masiniai pataisymai pagal patvirtintus laiko ir išlaidų įrašus
description: Šiame straipsnyje paaiškinama, kaip administratorius gali atlikti vienkartinius arba masinius anksčiau patvirtintų laiko ar išlaidų įrašų taisymus, jei atsiskaitymas nebaigtas.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 82c9b38e4c79511fe3b6abfcb973fff8b56f1522
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916299"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Faktinių duomenų masiniai pataisymai pagal patvirtintus laiko ir išlaidų įrašus

[!include [banner](../includes/psa-now-project-operations.md)]

Kartais laiko arba išlaidų įrašas gali būti įvestas neteisingai. Pavyzdžiui, konsultantas gali pasirinkti neteisingą laiko įrašo sukūrimo datą arba gali perkelti skaičius įvesdamas išlaidas. Jei konsultantas negali atnaujinti pateiktų įrašų, administratorius gali tiesiogiai pataisyti projekto įrašą.

Norėdami užbaigti šiame straipsnyje pateiktas procedūras, jums reikės administratoriaus teisių.

## <a name="correct-approved-time-entries"></a>Teisingi patvirtinti laiko įrašai     

Atlikite toliau nurodytus veiksmus norėdami pataisyti vieną ar kelis projekto laiko įrašus.

1. Srityje **Pardavimas** pasirinkite **Operacijos**, tada pasirinkite **Patvirtintas laikas**. 

2. Sąraše **Patvirtintas laikas** raskite ir pasirinkite vieną ar kelis taisytinus patvirtintus laiko įrašus. Galite naudoti filtrą susijusiems įrašams rasti. Pavyzdžiui, galite filtruoti pagal projekto ID ir pasirinkti visus patvirtintus laiko įrašus su tuo projekto ID.

3. Pasirinkite **Teisingi įrašai**. Automatiškai sukuriamas naujas pataisymų žurnalas su priskirtu tipu **Laiko koregavimas**. Į šį žurnalą įtraukiami jūsų pasirinkti įrašai. 

4. Puslapyje **Naujas žurnalas** įveskite pataisymų žurnalo **Aprašas**, tada pasirinkite skirtuką **Laiko koregavimas**.  
5. Dalyje **Naujos laiko įrašų reikšmės** atnaujinkite laukus įvesdami teisingą informaciją, jei reikia. Pavyzdžiui, galite keisti priskirtą projektą arba rezervuotiną išteklių.

6. Pasirinkite **Peržiūra**. Dialogo lange pasirinkite **Gerai**. Skirtuke **Žurnalo eilutės** galite peržiūrėti pirminių faktinių duomenų, kurie yra susieti su pasirinktais laiko įrašais, kurie buvo anuliuoti, ir pataisytomis eilutėmis, kurios buvo sukurtos, sąrašą. Jei reikia atlikti papildomų pataisymų, pakartokite 5 ir 6 veiksmus. 

> [!NOTE]
> Visos pataisytos faktinių duomenų reikšmės turės tas pačias reikšmes, kurias pasirinkote skyriuje **Laiko įrašų naujos reikšmės**.

7. Jei pataisymai rodomi taip, kaip tikėjotės, pasirinkite **Patvirtinti**. Dialogo lange pasirinkite **Gerai**.

8. Grįžkite į sritį **Pardavimas**, pasirinkite **Projektai**, tada atidarykite projektą, kuriame ką tik atnaujinote laiko įrašus. 

9. Puslapio **Projektai** skirtuke **Faktiniai duomenys** peržiūrėkite atliktus pakeitimus. 

> [!NOTE]
> Jei skirtuko **Faktiniai duomenys** nesimato, pasirinkite **Susijęs** > **Faktiniai duomenys**.  

10. Sąraše **Faktinis susietasis rodinys** galite matyti, kad vis dar rodomi anuliuoti pradiniai laiko įrašai ir atitinkami pataisyti laiko įrašai. 


## <a name="correct-approved-expense-entries"></a>Patvirtintų išlaidų įrašų taisymas

Atlikite toliau nurodytus veiksmus norėdami pataisyti vieną ar daugiau išlaidų įrašų. 

1. Srityje **Pardavimas** kairiojoje naršymo srityje pasirinkite **Operacijos**, tada pasirinkite **Patvirtintos išlaidos**.

2. Sąraše **Patvirtintos išlaidos** pasirinkite taisytiną projektą, tada pasirinkite **Teisingi įrašai**. Automatiškai bus sukurtas naujas pataisymų žurnalas su priskirtu tipu **Išlaidų koregavimas**. 

3. Puslapyje **Naujas žurnalas** įveskite pataisymo **Aprašas**, o skirtuke **Išlaidų koregavimas** skyriuje **Naujos išlaidų reikšmės** pasirinkite duomenų lauką, kurį norite pataisyti pasirinktoms išlaidų eilutėms. Pavyzdžiui, galite priskirti išlaidas kitam **Projektas** arba pataisyti **Išlaidų kategorija**, **Išlaidų data** arba **Rezervuotini ištekliai**.

4. Pasirinkite **Peržiūra**. Dialogo lange pasirinkite **Gerai**. 

5. Skirtuke **Žurnalo eilutės** patvirtinkite pataisymus. Galite peržiūrėti pirminių faktinių duomenų, kurie yra susieti su pasirinktais išlaidų įrašais, kurie buvo anuliuoti, ir pataisytomis eilutėmis, kurios buvo sukurtos, sąrašą.

6. Jei pataisytos reikšmės rodomos taip, kaip tikėjotės, pasirinkite **Patvirtinti**. Dialogo lange pasirinkite **Gerai.** Jei rodomos ne tos reikšmės, kurių tikėjotės, pasirinkite **Atšaukti**, kas grįžtumėte į sąrašą **Patvirtintos išlaidos**. Pakartokite 2–5 veiksmus. 

> [!NOTE]
> Pataisytos faktinių duomenų reikšmės turės tas pačias reikšmes, kurias pasirinkote skyriuje **Išlaidų įrašų naujos reikšmės**.

7. Patvirtinę pataisymų žurnalą, grįžkite prie atnaujintų projekto arba projektų ir peržiūrėkite savo pakeitimus.  

8. Projekto puslapyje skirtuke **Faktiniai duomenys** peržiūrėkite **Faktinis susietasis rodinys**. Rodomi pradiniai įrašai ir pataisyti įrašai. Šiame grafike rodomos pradinės išlaidų įrašų sumos ir atitinkamos pataisytų išlaidų įrašų sumos. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
