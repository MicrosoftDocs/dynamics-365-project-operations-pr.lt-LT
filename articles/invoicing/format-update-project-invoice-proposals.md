---
title: Projekto sąskaitos faktūros pasiūlymų valdymas
description: Šioje temoje pateikiama išsami informacija apie klientų sąskaitų faktūrų apdorojimą naudojant „Project Operations“, skirtą išteklių / nelaikomų medžiagų scenarijams.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 83e5af60d0a3baf0b59da2a97c6b156ef5b2b7ed
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089275"
---
# <a name="manage-project-invoice-proposals"></a>Projekto sąskaitos faktūros pasiūlymų valdymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projektų sąskaitų faktūrų pasiūlymus gali apdoroti sąskaitų pateikimo skyrius, jei atitinka šios dvi sąlygos:

  - Projektų vadovas patvirtina išankstinę sąskaitą faktūrą programoje „Microsoft Dataverse“.
  - Visos laiko ir medžiagų pardavimo operacijos, už kurias neišrašyta sąskaita, įtrauktos į išankstinę sąskaitą faktūrą, registruojamos naudojant „Dynamics 365 **Project Operations“ integravimo** žurnalą.

Norėdami užbaigti projekto sąskaitos faktūros pasiūlymą programoje „Dynamics 365 Finance“, atlikite toliau nurodytus veiksmus.

1. Peržiūrėkite laiko ir medžiagų operacijų sąskaitų išrašymo informaciją ir registruokite **„Project Operations“ integravimo** žurnalą.
2. Peržiūrėkite fiksuotos kainos atsiskaitymo etapų sąskaitų išrašymo informaciją.
3. Peržiūrėkite ir formatuokite projekto sąskaitos faktūros pasiūlymą.
4. Registruokite ir spausdinkite projekto sąskaitas faktūras.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Sąskaitų išrašymo informacijos valdymas „Project Operations“ integravimo žurnale

Projekto faktinius duomenis programoje „Dataverse“ peržiūri ir skiltyje „Finansai“ užregistruoja projekto apskaitininkas. Daugiau informacijos apie tai, kaip dirbti su integravimo žurnalu, ieškokite [„Project Operations“ integravimo žurnalas](../project-accounting/project-operations-integration-journal.md).

Išlaidų faktiniai duomenys ir pardavimo, už kurį neišrašyta sąskaita, faktiniai duomenys į integravimo žurnalą įtraukiami kaip atskiros eilutės:

  - Vieneto savikainos ir išlaidų suma faktinėse išlaidose yra nustatoma pagal projekto faktinių išlaidų operaciją programoje „Dataverse“.
  - Vieneto pardavimo kaina ir pardavimo suma pardavimų, už kuriuos neišrašyta sąskaita, operacijose yra nustatoma iš projekto faktinių pardavimo, už kurį neišrašyta sąskaita, operacijų programoje „Dataverse“.

### <a name="billing-sales-tax"></a>Atsiskaitymo PVM

Atsiskaitymo PVM apskaičiuojamas pagal laukų **Atsiskaitymo PVM grupė** ir **Atsiskaitymo elemento PVM grupė** derinį pardavimo, už kurį neišrašyta sąskaita, įraše, kuris yra eilutėje **„Project Operations“ integravimo** žurnalas. Sistema nustato šiuos laukus pagal parametrus skirtuke **Finansai**, esančiame puslapyje **Projekto vadymo ir apskaitos parametrai**.

- **PVM grupės būdas** nustato atsiskaitymo PVM grupės numatytąją logiką:
  
  - **Projektas**: pagal numatytuosius nustatymus visada nustatys atsiskaitymo PVM grupę iš projekto. Galite peržiūrėti arba pakeisti projekto numatytąją atsiskaitymo PVM grupę puslapyje **Visi projektai** pasirinkdami **Rodyti numatytąją apskaitą**.
  - **Projekto sutartis**: pagal numatytuosius nustatymus visada nustatys atsiskaitymo PVM grupę iš projekto sutarties. Galite peržiūrėti arba pakeisti projekto sutarties numatytąją atsiskaitymo PVM grupę puslapyje **Projekto sutartys** pasirinkdami **Rodyti numatytąją apskaitą**.
  - **Klientas**: pagal numatytuosius nustatymus visada nustatys atsiskaitymo PVM grupę iš kliento.
  - **Ieška**: ieškos tarp visų aukščiau nurodytų objektų ir pažymės pirmą prieinamą reikšmę. Ieška pradedama nuo objekto **Projektas**, tada seka objektas **Projekto sutartis** ir galiausiai – objektas **Klientas**.

- **Prekės PVM grupės būdas** nustato atsiskaitymo prekės PVM grupės numatytąją logiką:
  
  - Naudojant laiko, išlaidų ir mokesčių operacijų tipus, atsiskaitymo prekės PVM grupė pagal numatytuosius nustatymus visada bus nustatoma iš objekto **Projekto kategorija**.
  - Naudojant medžiagų operacijų tipus, atsiskaitymo prekės PVM grupė pagal numatytuosius nustatymus nustatoma pagal parametrą **Prekės PVM grupės būdas**, esantį dalyje **Projekto valdymo ir apskaitos parametrai**. Prekės numeris pagal numatytuosius nustatymus nustatomas pagal prekės PVM grupę iš objekto **Patvirtintas produktas**. Kategorija pagal numatytuosius nustatymus nustatoma pagal prekės PVM grupę iš objekto **Projekto kategorija**.

### <a name="financial-dimensions"></a>Finansinės dimensijos

Finansinės dimensijos, skirtos pardavimo, už kurį neišrašyta sąskaita, įrašui **„Project Operations“ integravimo** žurnale, pagal numatytuosius nustatymas nustatomos iš objekto **Projektas**. Finansines dimensijas galima peržiūrėti ir koreguoti pasirinkus parinktį **Paskirstyti sumą**. Jei reikia pakeisti pardavimo, už kurį neišrašyta sąskaita, įrašo finansines dimensijas po to, kai užregistruotas integravimo žurnalus, bet prieš patvirtinant išankstinę sąskaitą faktūrą, eikite į **Visi prijektai** > **Valdyti** > **Užregistruotos operacijos**, pasirinkite operaciją, o tada pasirinkite **Procesas** > **Koreguoti apskaitą**.

### <a name="exchange-rates"></a>Valiutos kursai

Operacijos, už kurią neišrašyta sąskaita, valiuta programoje „Dataverse“ naudojama kaip operacijų valiuta skiltyje „Finansai“, ir konvertuojama į įmonės apskaitos valiutą naudojant valiutos kursus, apibrėžtus skiltyje „Finansai“.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Atsiskaitymo etapų finansinių atributų valdymas 

Projekto sutarties eilutėms, kurios naudoja fiksuotos kainos atsiskaitymo būdą, sąskaitos faktūros išrašomos naudojant [Fiksuotos kainos etapus](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Projekto apskaitininkas gali peržiūrėti atsiskaitymo etapus skiltyje „Finansai“ nueidamas į **Projekto valdymas ir apskaita** > **Visi projektai** > **Valdyti** > **Laisvos formos sąskaitos operacija**.

### <a name="billing-sales-tax"></a>Atsiskaitymo PVM

Reikšmės **PVM grupė** ir **Prekės PVM grupė** nustatomos iš parametrų, kai „Dataverse“ programoje sukuriamas naujas atsiskaitymo etapas. Sistema šiems laukams nustato reikšmes pagal parametrus skirtuke **Finansai**, esančiame puslapyje **Projekto valdymo ir apskaitos parametrai**.

- **PVM grupės būdas** nustato numatytąją **Atsiskaitymo PVM grupės** logiką:

    - **Projektas** pagal numatytuosius nustatymus visada nustatys atsiskaitymo PVM grupę iš projekto. Galite peržiūrėti arba pakeisti projekto numatytąją atsiskaitymo PVM grupę puslapyje **Visi projektai** pasirinkdami **Rodyti numatytąją apskaitą**.
    - **Projekto sutartis** pagal numatytuosius nustatymus visada nustatys atsiskaitymo PVM grupę iš projekto sutarties. Galite peržiūrėti arba pakeisti projekto sutarties numatytąją atsiskaitymo PVM grupę puslapyje **Projekto sutartys** pasirinkdami **Rodyti numatytąją apskaitą**.
    - **Klientas** pagal numatytuosius nustatymus visada nustatys atsiskaitymo PVM grupę iš kliento.
    - **Ieška** ieškos tarp visų šiame sąraše esančių objektų ir pažymės pirmą prieinamą reikšmę. Ieška pradedama nuo objekto **Projektas**, tada seka objektas **Projekto sutartis**, o tada – objektas **Klientas**.

- **Fiksuotos kainos etapo prekės PVM grupė** naudojama nustatyti reikšmę laukui **Prekės PVM grupė**.

### <a name="financial-dimensions"></a>Finansinės dimensijos

Fiksuotos kainos atsiskaitymo etapų numatytosios finansinės dimensijos yra nustatytos projekto sutarties eilutėse. Eikite į **Projekto sutartys** > **Rodyti numatytąją apskaitą** ir skirtuke **Sutarties eilutės** pasirinkite **kainos sutarties eilutę**, o tada nustatykite finansinių dimensijų reikšmes, kurias norite naudoti kaip numatytąsias.

Projekto apskaitininkas gali redaguoti PVM ir finansinių dimensijų informaciją sąskaitų faktūrų etapuose iki tol, kol sukuriamas projekto sąskaitos faktūros pasiūlymas.


## <a name="create-project-invoice-proposals"></a>Projekto sąskaitos faktūros pasiūlymų kūrimas

Projekto sąskaitų faktūrų pasiūlymus galima peržiūrėti modulyje **Projekto valdymas ir apskaita** nueinant į **Projekto sąskaitos faktūros** > **Projekto sąskaitų faktūrų pasiūlymai**.

Projekto sąskaitos faktūros pasiūlymo antraštė sukuriama skiltyje „Finansai“, kai patvirtinama išankstinė sąskaita faktūra programoje „Dataverse.“ Kad būtų lengviau derinti, sistema projekto sąskaitos faktūros pasiūlymo numerį skiltyje „Finansai“ nustato tokį patį skaičių, kaip ir išankstinės sąskaitos faktūros ID programoje „Dataverse“. Kadangi išankstinės sąskaitos faktūros ne visada patvirtinamos ta pačia tvarka, kuria jos kuriamos, projektų sąskaitų faktūrų pasiūlymo numeracija skiltyje „Finansai“ turėtų leisti keisti į mažesnius ir didesnius skaičius. Konfigūruokite numeraciją naudodami šiuos veiksmus:

1. Skiltyje „Finansai“ eikite į **Organizacijos administravimas** > **Numeracijos** > **Numeracijos**.
2. Filtre **Sritis** pasirinkite **Projektai**.
3. Filtre **Nuoroda** pasirinkite **Sąskaitos faktūros pasiūlymas**.
4. Naudokite lauką **Įmonė**, kad filtruotumėte kiekvieną juridinį objektą įjungę „Project Operations Dataverse“ integravimą.
5. Atidarykite **Išsami numeracijos informacija** ir skirtuke **Bendra** nustatykite:

    - **Leisti vartotojo pakeitimus: mažesniu numeriu** = **Taip**
    - **Leisti vartotojo pakeitimus: didesniu numeriu** = **Taip**

Sistem projektų sąskaitų faktūrų pasiūlymo eilutes prideda naudojant periodinį apdorojimą **Importuoti iš išdėstymo lentelės** (**Projekto valdymas ir apskaita** > **Periodinis** > **„Project Operations“ integravimas** > **Importuoti iš išdėstymo lentelės**). Šį procesą galima vykdyti rankiniu būdu arba naudojant periodinį grafiką. Sistema nepridės eilučių į sąskaitos faktūros pasiūlymo dokumentą, kol visos eilutės nebus paruoštos sąskaitai faktūrai išrašyti. Laiko ir medžiagų operacijos yra paruoštos sąskaitos faktūros išrašymui tik tada, kai jos užregistruojamos naudojant **„Project Operations“ integravimo** žurnalą.

## <a name="format-and-print-invoice-proposals"></a>Sąskaitų faktūrų pasiūlymų formatavimas ir spausdinimas

Projekto apskaitininkas gali tinkinti projekto sąskaitos faktūros spaudinį naudodamas puslapį **Formatuoti SF pasiūlymą** ir spausdinimo valdymo galimybes.

### <a name="format-invoice-proposals"></a>Sąskaitų faktūrų pasiūlymų formatavimas

Puslapyje **Formatuoti SF pasiūlymus** pasirinktinio grupavimo operacijas galima rodyti kliento projekto sąskaitoje faktūroje.

1. Puslapyje **Projekto SF pasiūlymas** pasirinkite **Spausdinti** > **Formatuoti SF pasiūlymą**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują projekto sąskaitos faktūros spaudinio grupavimą.
3. Lauke **Išsami informacija / suvestinė** pasirinkite šio grupavimo parinktis:

    - Norėdami spausdinti kliento sąskaitos faktūros operacijos išsamią informaciją, pasirinkite **Išsami informacija**.
    - Norėdami spausdinti kliento sąskaitos faktūros operacijos suvestinę, pasirinkite **Suvestinė**.

> [!NOTE]
> Pasirinkimas lauke **Išsami informacija / suvestinė**, esančiame puslapyje **Formatuoti SF pasiūlymą** perrašo parinktį, pasirinktą lauke **SF formatas**, esančiame puslapyje **SF pasiūlymai**, spausdinti išsamią SF ar apibendrintą SF.

- Skirtuke **Galimos operacijos** pasirinkite operacijų eilutes, kurias norite įtraukti į šį skyrių, ir pasirinkite **Įtraukti operacijas**, kad perkeltumėte jas į skirtuką **Pasirinktos operacijos**.
- Norėdami keisti skyrių tvarką, pasirinkite **Perkelti aukštyn** ir **Perkelti žemyn**.
- Norėdami peržiūrėti formatuotą SF, pasirinkite **Spausdinimo peržiūra**.

### <a name="print-management"></a>Spausdinimo valdymas

Spausdinimo valdymas naudoja skirtingus ataskaitų failus sąskaitoms faktūroms spausdinti, paskirties vietai nurodyti ir poraštės tekstui tinkinti. Spausdinimo valdymą galima nustatyti modulio lygiu, tačiau šiuos parametrus galima perrašyti konkrečiam klientui, sutarčiai arba sąskaitos faktūros pasiūlymui. Norėdami pasiekti šią funkciją, puslapyje **Projekto SF pasiūlymas** pasirinkite **Spausdinti** > **Spausdinimo valdymas**.

Spausdinimo valdymo sąranka rodoma kaip medžio rodinys, kuriame kiekviename mazgo lygyje rodomi galimi koreguoti dokumentai. Pasirinktinius spaudinius galite priskirti modulio, kliento, sutarties arba sąskaitos faktūros dokumentų lygiu. Norėdami modifikuoti originalaus dokumento spaudinį, išplėskite norimą mazgą ir pasirinkite **Pradinis elementas**. Lauke **Ataskaitos formatas** pažymėkite ataskaitos formatą, kurį norite naudoti spausdinant. Pasirinktinius ataskaitų formatus galite naudoti naudodami [Verslo dokumentų valdymo sistemą](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Sąskaitų faktūrų pasiūlymų registravimas

Po to, kai sąskaita faktūra peržiūrima ir suredaguojama, o sąskaitų faktūrų pasiūlymo eilutės yra tinkamos, patikrinkite sąskaitų faktūrų sumas ir PVM. Grupėje **Išsami informacija** pasirinkite **Bendros sumos**, o tada pasirinkite **Registruoti**, kad užregistruotumėte sąskaitą faktūrą.

Norėdami peržiūrėti sąskaitą faktūrą prieš registravimą, išvalykite žymės langelį **Registravimas**. **„Pro forma“** bus spausdinama sąskaitoje faktūroje, kad būtų nurodyta, jog tai sąskaitos faktūros pavyzdys. Norėdami atspausdinti sąskaitą faktūrą, pasirinkite žymės langelį **Spausdinti SF**.

Be puslapio **SF pasiūlymas**, sąskaitų faktūrų pasiūlymai taip pat gali būti registruojami vykdant periodinę užduotį **Registruoti SF pasiūlymus**. Norėdami rasti šią užduotį, eikite į **Projekto valdymas ir apskaita** > **Periodinis** > **Projekto SF** > **Registruoti SF pasiūlymus**.

Šiame puslapyje pateikiami visi sąskaitų faktūrų, kurios yra paruoštos registruoti, pasiūlymai. Galite planuoti sąskaitų faktūrų registravimą pažymėdami **Paketas**. Nustatykite **Paketo apdorojimo parametrą** į **Taip** ir nustatykite paketo apdorojimo pasikartojimą pasirinkdami **Pasikartojimas**.
