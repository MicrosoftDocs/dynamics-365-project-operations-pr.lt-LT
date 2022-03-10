---
title: Projektu pagrįstos sutarties eilutės įvertinimas – „Lite“ versija
description: Šioje temoje pateikta informacija apie projektu pagrįstos sutarties eilutės įvertinimą.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 747a1abe5630cac3dc074eba3a469d8d858c5ef244b59e26921e35afa61645df
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999101"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Projektu pagrįstos sutarties eilutės įvertinimas – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Naudodami „Dynamics 365 Project Operations“, projektu pagrįstoje sutarties eilutėje pateikiama išsami informacija, kuri padeda įvertinti susijusio darbo savikainą ir potencialias pajamas sutarties eilutei pateikti.

Norėdami įvertinti projektu pagrįstą sutarties eilutę, nueikite į projektu pagrįstos **sutarties eilutės** skirtuką **Sutarties eilutės informacija**.  Yra du tolesni būdai, kaip įvertinti projektu pagrįstą sutarties eilutę.

   - Įvertinimą sukurkite tiesiai sutarties eilutėje, rankiniu būdu įtraukdami sutarties eilutės informaciją.
   - Sukurkite projektą ir projekto planą bei susiekite projektą ir užduotis su projekto sutarties eilute. Tokiu būdu galite importuoti projekto plano sąmatą į sutarties eilutę pagal sutarties eilutėje esančius komponentus.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Sąmatos kūrimas tiesai projektu pagrįstoje sutarties eilutėje

Norėdami įvertinimą sukurti tiesiai projektu pagrįstoje sutarties eilutėje, atlikite toliau nurodytus veiksmus.

1. Nueikite į sutarties eilutę ir pasirinkite skirtuką **Sutarties eilutės informacija**. Šiame skirtuke sukurtos eilutės yra apibendrinamos ir rodomos kaip šios **sutarties eilutės** **sutarties reikšmė**. 
2. Papildomame tinklelyje **Sutarties eilutės informacija** pasirinkite **Nauja sutarties eilutės informacija**. Atidaromas sparčiojo kūrimo slankiklis. Toliau nurodytus laukus galima rasti sutarties puslapyje **Sutarties eilutės išsami informacija**.

| Laukas | Vieta | Aprašymas | Tolesnis poveikis |
| --- | --- | --- | --- |
| **Aprašas** | **Spartusis kūrimas** | Konkretaus įvertinimo aprašymas. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| **Operacijos klasė** | **Spartusis kūrimas** | Tai operacijos klasių sąrašas, įtrauktas į projektu pagrįstos sutarties eilutės skirtuką **Bendra**. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| **Pasirinkti produktą** | **Spartusis kūrimas** | Taikoma, kai operacijos klasė yra **Medžiaga**. Galite nurodyti, ar ši įvertinimo eilutė yra skirta **esamam** (kataloge nurodytam) produktui ar **įtraukiamajam** produktui. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| **Produktas** | **Spartusis kūrimas** | Produkto iš produktų katalogo ID. Šis laukas įjungiamas pasirinkus **Esamas produktas** lauke **Pasirinkti produktą**. ID naudojamas norint gauti pardavimo kainą iš sutarties projekto kainoraščio. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| **Įtraukiamasis produktas** | **Spartusis kūrimas** | Teksto laukas, kuriame reikia įvesti produkto pavadinimą. Šis laukas įjungiamas tik pasirinkus **Įtraukiamasis** lauke **Pasirinkti produktą**.| Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| **Vaidmuo** | **Spartusis kūrimas** | Asmens, kuris atlieka šį darbą arba patiria šias išlaidas, vaidmuo. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai.|
| **Kategorija.** | **Spartusis kūrimas** | Darbo arba išlaidų kategorija. |Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai.|
| **Pradžios data** | **Spartusis kūrimas** | Darbo pradžios data. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| **Pabaigos data** | **Spartusis kūrimas** | Darbo pabaigos data. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| **Išteklių paskirstymo vienetas** | **Spartusis kūrimas** | Išteklių skyrimo vienetas, pagal kurį taikoma ši savikaina ir pateikiami ištekliai dirbti. |Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai ir naudojama savikainai gauti. |
| **Vieneto grafikas** | **Spartusis kūrimas** | Darbo, produkto arba išlaidų vienetų grupė. Vienetai priklauso vienetų grafikui arba vienetų grupei. Pavyzdžiui, *mylios* ir *kilometrai (km)* yra vienetai, priklausantys vienetų grupei, kurioje aprašomas atstumas. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| **Vienetas** | **Spartusis kūrimas** | Darbo, produkto arba išlaidų vienetas. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| **Kiekis** | **Spartusis kūrimas** | Darbo, produkto arba išlaidų kiekis. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi sutarties eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| **Vieneto kaina** | **Spartusis kūrimas** | Darbą atliekančio vaidmens sąskaitų tarifas, produkto vieneto kaina arba produkto ar išlaidų kategorijos pardavimo kaina. Šiam laukui nustatoma numatytoji **laiko** reikšmė, pagrįsta deriniu kainodaros dimensijų reikšmių, esančių vaidmens kainos eilutėje, susijusioje su projekto kainoraščiu, galiojančiu pradžios dieną. **Išlaidų** atveju šio lauko numatytoji reikšmė nustatoma pagal operacijos kategorijos kainų sąranką projekto kainoraštyje, kuris galioja pradžios dieną. Jei operacijos kategorijos kainodaros būdas nėra **kaina už vienetą**, numatytosios reikšmės nėra, o šis laukas paliekamas tuščias. Produktų atveju šio lauko numatytoji reikšmė pagrįsta eilute **Kainų sąrašo elementas**, priklausančia kainoraščiui, kuris galioja pradžios dieną.| Darbą atliekančio vaidmens savikainos tarifas arba išlaidų kategorijos vieneto savikaina arba produkto vieneto savikaina. Šiam laukui nustatoma numatytoji **laiko** reikšmė, pagrįsta deriniu kainodaros dimensijų reikšmių, esančių vaidmens kainos eilutėje, susijusioje su savikainos kainoraščiu, susietu su sutartį sudarančiu vienetu, galiojančiu pradžios dieną. Išlaidų atveju šio lauko numatytoji reikšmė nustatoma pagal kaštų kainoraščio, pridedamo prie sutartį sudarančio vieneto, kuris galioja pradžios dieną, kategorijos kainos eilutę. Jei operacijos kategorijos kainodaros būdas nėra kaina už vienetą, numatytosios reikšmės nėra, o šis laukas paliekamas tuščias. Produktų atveju šio lauko numatytoji reikšmė yra pagrįsta **kainų sąrašo elemento** eilute, priklausančia savikainos kainoraščiui, susietam su sutartį sudarančiu vienetu, galiojančiu pradžios dieną.|
| **Įvertintas mokestis** | **Spartusis kūrimas** | Įvertintas mokestis už šį darbą arba išlaidas. | Įvertintas mokestis už šį darbą arba išlaidas. |
| **Suma** | **Spartusis kūrimas** | Į šį lauką galite įtraukti reikšmę, jei laukai **Kiekis** ir **Kaina** yra tušti. Jei **Kiekis** ir **Kaina** yra užpildyti, laukas **Suma** yra skirtas tik skaityti ir apskaičiuojamas kaip **(kiekis \* vieneto kaina) + mokesčiai**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Sutarties eilutės informacijos kainų naujinimas

Jei keičiate kainas projekto kainoraštyje, pridėtame prie sutartį sudarančio vieneto sutarties arba kaštų kainoraščio, galite atnaujinti kainas atskiroje sutarties eilutės informacijos dalyje, kad būtų matomas pakeitimas. Puslapyje **Sutartis** pasirinkite **Perskaičiuoti**. Rodomas įspėjimas, kuriame informuojama, kad visų šios sutarties eilučių kainos yra nustatytos iš naujo. Norėdami atnaujinti tiek pardavimo, tiek kaštų sutarties eilučių informaciją, pasirinkite **Taip**.

## <a name="access-contract-line-details-for-cost"></a>Prieiga prie kaštų sutarties eilutės informacijos

Skirtuke **Sutarties eilutės informacija** pažymėkite tinklelio eilutę, kad būtų rodomi veiksmai papildomo tinklelio įrankių juostoje. Pirmasis papildomo tinklelio įrankių juostos veiksmas yra **Atidaryti kaštų informaciją**. Jei norite peržiūrėti šios sutarties eilutės informacijos kaštų tarifą ir sumą, pasirinkite **Atidaryti kaštų informaciją**. 

> [!NOTE]
> **Kaštų** sutarties eilutės informacijoje pakeitus išteklių įmonės, išteklių skyrimo vieneto, kiekio, datų, vaidmens ar kategorijos reikšmes, taip pat pakeičiamos atitinkamos **pardavimo** sutarties eilutės reikšmės.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Kaštų ir pardavimo sutarties eilutės informacijos valiuta

**Pardavimo** sutarties eilutės informacija nustato numatytąją valiutą iš projekto kainoraščio, kuris galioja sutarties eilutės informacijos pradžios dieną.

**Kaštų** sutarties eilutės informacija nustato numatytąją valiutą iš sutartį sudarančio vieneto kainoraščio, kuris galioja sutarties eilutės **kaštų** informacijos pradžios dieną.

Skaičiuojant pelningumą, **kaštų** ir **pardavimo** sutarties eilutės informacijos sumos konvertuojamos į aplinkos pagrindinę valiutą, norint deklaruoti bendrą faktinę ir numatomą sutarties maržą.

> [!NOTE]
> Dėl trūkstamų nuo datos priklausančių valiutos kursų gali įvykti valiutos apvalinimo klaidų ir pasikeisti maržos. Šiuos skaičiavimus naudokite tik projekto sutartyse, nes jie yra apytiksliai ir nėra skirti įstatymų nustatytoms faktinėms arba kitoms ataskaitoms, kuriose reikalaujama tiksliau apvalinti ir pateikti valiutų kursų įsigaliojimo datą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
