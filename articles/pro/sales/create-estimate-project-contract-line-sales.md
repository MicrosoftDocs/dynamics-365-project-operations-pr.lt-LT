---
title: Projektu pagrįstos sutarties eilutės įvertinimas – „Lite“ versija
description: Šioje temoje pateikta informacija apie projektu pagrįstos sutarties eilutės įvertinimą.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 186b982ee440576e10cf5b78922848b8877afd51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273547"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Projektu pagrįstos sutarties eilutės įvertinimas – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Naudodami „Dynamics 365 Project Operations“, projektu pagrįstoje sutarties eilutėje pateikiama išsami informacija, kuri padeda įvertinti susijusio darbo savikainą ir potencialias pajamas sutarties eilutei pateikti.

Norėdami įvertinti projektu pagrįstą sutarties eilutę, nueikite į projektu pagrįstos **sutarties eilutės** skirtuką **Sutarties eilutės informacija**.  Yra du tolesni būdai, kaip įvertinti projektu pagrįstą sutarties eilutę.

   - Įvertinimą sukurkite tiesiai sutarties eilutėje, rankiniu būdu įtraukdami sutarties eilutės informaciją.
   - Sukurkite projektą ir projekto planą bei susiekite projektą ir užduotis su projekto sutarties eilute. Tokiu būdu galite importuoti projekto plano sąmatą į sutarties eilutę pagal sutarties eilutėje esančius komponentus.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Sąmatos kūrimas tiesai projektu pagrįstoje sutarties eilutėje

1. Nueikite į sutarties eilutę ir pasirinkite skirtuką **Sutarties eilutės informacija**. Šiame skirtuke sukurtos eilutės yra apibendrinamos ir rodomos kaip šios **sutarties eilutės** **sutarties reikšmė**. 
2. Papildomame tinklelyje **Sutarties eilutės informacija** pasirinkite **+ Nauja sutarties eilutės informacija**. Atidaromas sparčiojo kūrimo slankiklis. Formoje **Sutarties eilutės informacija** pasiekiami toliau nurodyti laukai.

| Laukas | Vieta | Aprašo | Tolesnis poveikis |
| --- | --- | --- | --- |
| **Aprašas** | **Spartusis kūrimas** | Konkretaus įvertinimo aprašymas. | Šio lauko numatytoji reikšmė yra susijusi sutarties eilutės informacija apie automatiškai sukurtus kaštus. |
| **Operacijos klasė** | **Spartusis kūrimas** | Šis išskleidžiamasis sąrašas yra operacijų klasių, įtrauktų į projektu pagrįstos sutarties eilutės skirtuką **Bendra**, sąrašas. | Šio lauko numatytoji reikšmė yra susijusi sutarties eilutės informacija apie automatiškai sukurtus kaštus. |
| **Vaidmuo** | **Spartusis kūrimas** | Asmens, kuris atlieka šį darbą arba patiria šias išlaidas, vaidmuo. | Šio lauko numatytoji reikšmė yra susijusi sutarties eilutės informacija apie automatiškai sukurtus kaštus. |
| **Kategorija** | **Spartusis kūrimas** | Darbo arba išlaidų kategorija. | Šio lauko numatytoji reikšmė yra susijusi sutarties eilutės informacija apie automatiškai sukurtus kaštus. |
| **Pradžios data** | **Spartusis kūrimas** | Darbo pradžios data. | Šio lauko numatytoji reikšmė yra susijusi sutarties eilutės informacija apie automatiškai sukurtus kaštus. |
| **Pabaigos data** | **Spartusis kūrimas** | Darbo pabaigos data. | Šio lauko numatytoji reikšmė yra susijusi sutarties eilutės informacija apie automatiškai sukurtus kaštus. |
| **Išteklių paskirstymo vienetas** | **Spartusis kūrimas** | Išteklių skyrimo vienetas, kuris patiria šias išlaidas ir teikia išteklių darbui su jomis. | Šio lauko numatytoji reikšmė yra susijusi sutarties eilutės informacija apie automatiškai sukurtus kaštus. Šis laukas taip pat naudojamas savikainai gauti. |
| **Vieneto grafikas** | **Spartusis kūrimas** | Darbo arba išlaidų vienetų grupė. Vienetai priklauso vienetų grafikui arba vienetų grupei. Pavyzdžiui, *mylios* ir *kilometrai (km)* yra vienetai, priklausantys vienetų grupei, kuri aprašo atstumą. | Šio lauko numatytoji reikšmė yra susijusi sutarties eilutės informacija apie automatiškai sukurtus kaštus. |
| **Vienetas** | **Spartusis kūrimas** | Darbo arba išlaidų vienetas. | Šio lauko numatytoji reikšmė yra susijusi sutarties eilutės informacija apie automatiškai sukurtus kaštus. |
| **Kiekis** | **Spartusis kūrimas** | Darbo arba išlaidų kiekis. | Šio lauko numatytoji reikšmė yra susijusi sutarties eilutės informacija apie automatiškai sukurtus kaštus. |
| **Vieneto kaina** | **Spartusis kūrimas** | Vaidmens, kuris atlieka darbą, sąskaitos tarifas arba išlaidų kategorijos pardavimo kaina. Šio lauko numatytoji **laiko** reikšmė pagrįsta vaidmens ir išteklių skyrimo vieneto derinu projekto kainoraštyje, kuris galioja pradžios dieną. Išlaidų atveju šio lauko numatytoji reikšmė nustatoma pagal operacijos kategorijos kainų sąranką projekto kainoraštyje, kuris galioja pradžios dieną. Jei operacijos kategorijos kainodaros būdas nėra **kaina už vienetą**, numatytosios reikšmės nėra, o šis laukas paliekamas tuščias. | Vaidmens, kuris atlieka darbą, kaštų tarifas arba išlaidų kategorijos vieneto kaštai. Šio lauko numatytoji reikšmė yra **laiko pagal vaidmenį** ir išteklių skyrimo vieneto derinys kaštų kainoraščio, pridėto prie sutartį sudarančio vieneto, galiojančio pradžios dieną, vaidmens kainų eilutėje. Išlaidų atveju šio lauko numatytoji reikšmė nustatoma pagal kaštų kainoraščio, pridedamo prie sutartį sudarančio vieneto, kuris galioja pradžios dieną, kategorijos kainos eilutę. Jei operacijos kategorijos kainodaros būdas nėra kaina už vienetą, numatytosios reikšmės nėra, o šis laukas paliekamas tuščias. |
| **Įvertintas mokestis** | **Spartusis kūrimas** | Apskaičiuoti šio darbo arba išlaidų mokesčiai, kuriuos įveda vartotojas. | Apskaičiuoti šio darbo arba išlaidų mokesčiai, kuriuos įveda vartotojas. |
| **Suma** | **Spartusis kūrimas** | Jei laukai **Kiekis** ir **Kaina** paliekami tušti, šio lauko reikšmę gali įtraukti vartotojas. Jei **kiekis** ir **kaina** yra užpildyti, laukas **Suma** yra skirtas tik skaityti ir apskaičiuojamas kaip **(kiekis \* vieneto kaina) + mokesčiai**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Sutarties eilutės informacijos kainų naujinimas

Jei keičiate kainas projekto kainoraštyje, pridėtame prie sutartį sudarančio vieneto sutarties arba kaštų kainoraščio, galite atnaujinti kainas atskiroje sutarties eilutės informacijos dalyje, kad būtų matomas pakeitimas. Puslapyje **Sutartis** pasirinkite **Perskaičiuoti**. Atidaromas įspėjimas, kad visų šios sutarties eilučių kainos nustatomos iš naujo. Norėdami atnaujinti tiek pardavimo, tiek kaštų sutarties eilučių informaciją, pasirinkite **Taip**.

## <a name="access-contract-line-details-for-cost"></a>Prieiga prie kaštų sutarties eilutės informacijos

Skirtuke **Sutarties eilutės informacija** pažymėkite tinklelio eilutę, kad būtų rodomi veiksmai papildomo tinklelio įrankių juostoje. Pirmasis papildomo tinklelio įrankių juostos veiksmas yra **Atidaryti kaštų informaciją**. Jei norite peržiūrėti šios sutarties eilutės informacijos kaštų tarifą ir sumą, pasirinkite **Atidaryti kaštų informaciją**. 

> [!NOTE]
> **Kaštų** sutarties eilutės informacijoje pakeitus išteklių įmonės, išteklių skyrimo vieneto, kiekio, datų, vaidmens ar kategorijos reikšmes, taip pat pakeičiamos atitinkamos **pardavimo** sutarties eilutės reikšmės.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Kaštų ir pardavimo sutarties eilutės informacijos valiuta

**Pardavimo** sutarties eilutės informacija nustato numatytąją valiutą iš projekto kainoraščio, kuris galioja sutarties eilutės informacijos pradžios dieną.

**Kaštų** sutarties eilutės informacija nustato numatytąją valiutą iš sutartį sudarančio vieneto kainoraščio, kuris galioja sutarties eilutės **kaštų** informacijos pradžios dieną.

Skaičiuojant pelningumą, **kaštų** ir **pardavimo** sutarties eilutės informacijos sumos konvertuojamos į aplinkos pagrindinę valiutą, norint deklaruoti bendrą faktinę ir numatomą sutarties maržą.

> [!NOTE]
> Dėl trūkstamų nuo datos priklausančių valiutos kursų gali įvykti valiutos apvalinimo klaidų ir pasikeisti maržos. Šiuos skaičiavimus atlikite tik su projekto sutartimis kaip apytikrį įvertinimą, o ne kaip faktinį norminį ar kitokį deklaravimą, kuriam reikia didesnio apvalinimo tikslumo ir žinoti valiutos kursų galiojimo datas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]