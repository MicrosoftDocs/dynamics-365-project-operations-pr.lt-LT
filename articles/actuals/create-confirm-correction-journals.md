---
title: Koregavimo žurnalų kūrimas ir patvirtinimas
description: Šiame straipsnyje pateikta informacija apie tai, kaip sukurti ir patvirtinti koregavimo žurnalą.
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
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928074"
---
# <a name="create-and-confirm-correction-journals"></a>Koregavimo žurnalų kūrimas ir patvirtinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Kartais laiko arba išlaidų įrašas gali būti įvestas neteisingai. Pavyzdžiui, konsultantas gali pasirinkti neteisingą laiko įrašo sukūrimo datą arba gali pasirinkti netinkamą projektą įvesdamas išlaidas. Jei konsultantas negali atnaujinti pateiktų įrašų, vidinis administratorius gali tiesiogiai pataisyti projekto faktinius duomenis.

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

7. Patvirtinę koregavimo žurnalą, grįžkite prie atnaujintų projekto arba projektų ir peržiūrėkite savo pakeitimus.

8. Projekto puslapio skirtuke **Faktiniai duomenys** peržiūrėkite sąrašą **Faktinių duomenų susietasis rodinys**. Rodomi pradiniai įrašai ir pataisyti įrašai.


## <a name="correct-approved-material-usage-logs"></a>Patvirtintų medžiagos naudojimo žurnalų koregavimas

Atlikite toliau nurodytus veiksmus norėdami pataisyti vieną ar daugiau medžiagos naudojimo įrašų.

1. Srities **Pardavimas** kairiojoje naršymo srityje pasirinkite **Operacijos**, tada pasirinkite **Faktiniai duomenys**.

2. Sąraše **Faktiniai duomenys** naudodami stulpelių filtrus pasirinkite operacijų klasę **Medžiaga**, kad būtų rodomi tik medžiagos faktiniai duomenys. Norėdami labiau apriboti rodomus faktinius duomenis, naudokite kitus stulpelių filtrus. Radę norimą faktinių duomenų rinkinį, pasirinkite tuos faktinius įrašus, tada pasirinkite **Tinkami įrašai** . Automatiškai sukuriamas naujas koregavimo žurnalas ir priskiriamas tipas **Medžiagos koregavimas**.

3. Puslapio **Naujas žurnalas** lauke **Aprašas** įveskite koregavimo aprašą. Tada skyriaus **Naujos medžiagos reikšmės** skirtuke **Medžiagos koregavimas** pasirinkite pasirinktų medžiagos eilučių koreguotinus duomenų laukus. Pavyzdžiui, medžiagą galite priskirti kitam projektui arba pataisyti produktą, medžiagos datą arba subrangos sutartį.

4. Pasirinkite **Peržiūra**. Tada kitame dialogo lange pasirinkite **Gerai**.

5. Skirtuke **Žurnalo eilutės** patikrinkite pataisymus. Galite peržiūrėti pirminių faktinių duomenų, susietų su pasirinktais medžiagos įrašais, kurie buvo anuliuoti, ir pataisytomis atitinkamomis eilutėmis, kurios buvo sukurtos, sąrašą.

6. Jei pataisytos reikšmės rodomos taip, kaip tikėjotės, pasirinkite **Patvirtinti**. Tada kitame dialogo lange pasirinkite **Gerai**. Jei reikšmės ne tokios, kurių tikėjotės, pasirinkite **Atšaukti**, kad grįžtumėte į sąrašą **Faktiniai duomenys**. Tada pakartokite 2–5 veiksmus.

7. Patvirtinę koregavimo žurnalą, grįžkite prie atnaujintų projekto arba projektų ir peržiūrėkite savo pakeitimus.

8. Projekto puslapio skirtuke **Faktiniai duomenys** peržiūrėkite sąrašą **Faktinių duomenų susietasis rodinys**. Rodomi pradiniai įrašai ir pataisyti įrašai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
