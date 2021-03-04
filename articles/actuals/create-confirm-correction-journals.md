---
title: Koregavimo žurnalų kūrimas ir patvirtinimas
description: Šioje temoje pateikta informacija apie tai, kaip sukurti ir patvirtinti koregavimo žurnalą.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127771"
---
# <a name="create-and-confirm-correction-journals"></a>Koregavimo žurnalų kūrimas ir patvirtinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Kartais laiko arba išlaidų įrašas gali būti įvestas neteisingai. Pavyzdžiui, konsultantas gali pasirinkti neteisingą laiko įrašo sukūrimo datą arba gali perkelti skaičius įvesdamas išlaidas. Jei konsultantas negali atnaujinti pateiktų įrašų, administratorius gali tiesiogiai pataisyti projekto įrašą.

Norėdami atlikti procedūras šioje temoje, turite turėti administratoriaus teises.

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

Pavyzdžiui, šiame grafiniame elemente yra du eilutės elementai, kurių kiekis yra 8,00 ir kurių debetai išvardinti stulpelyje „Suma“. Be to, yra du eilutės elementai, kurių kiekis yra -8,00 ir kurių kredito sumos rodomos stulpelyje „Suma“. Šie pataisymai suteikia kiekiui nulinę reikšmę.

 
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