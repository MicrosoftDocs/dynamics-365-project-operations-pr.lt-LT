---
title: Projektu pagrįstos pasiūlymo eilutės įvertinimas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip sukurti įvertinimą pagal projektą pagrįstoje pasiūlymo eilutėje.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2a8aa2971431cd1f2082c8fc80db1438be185f5b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914366"
---
# <a name="estimating-a-project-based-quote-line"></a>Projektu pagrįstos pasiūlymo eilutės įvertinimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projektu pagrįstoje pasiūlymo eilutėje pateikta išsami informacija, padedanti įvertinti darbo išlaidas ir potencialias pajamas, kad būtų sukurta pasiūlymo eilutė.

Norėdami įvertinti projektu pagrįstą pasiūlymo eilutę, projektu pagrįstoje pasiūlymo eilutėje pažymėkite skirtuką **Pasiūlymo eilutės informacija**. Yra du būdai apskaičiuoti projektu pagrįstos pasiūlymo eilutės įvertinimą:

- Rankiniu būdu sukurti įvertinimą tiesiogiai pasiūlymo eilutėje naudojant pasiūlymo eilutės išsamią informaciją. 
- Sukurti projektą ir projekto planą, o tada susieti projektą ir projekto užduotis su pasiūlymo eilute. Procesas, skirtas projekto plano įvertinimų importavimui į pasiūlymo eilutę pagal jūsų pateiktą informaciją, bus įjungtas.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Įvertinimų kūrimas tiesiogiai projektu pagrįstoje pasiūlymo eilutėje

Jei norite kurti įvertinimą projektu pagrįstoje pasiūlymo eilutėje, pažymėkite skirtuką **Pasiūlymo eilutės informacija**. Šiame skirtuke sukurtas eilutės elementas apibendrins šios pasiūlymo eilutės pasiūlytą reikšmę. 

Norėdami sukurti pasiūlymo eilutės išsamią informaciją, papildomame tinklelyje **Pasiūlymo eilutės informacija** pasirinkite **Nauja pasiūlymo eilutės informacija**. Atsidarys sparčiojo kūrimo slankiklis. Toliau pateiktoje lentelėje nurodyta išsami informacija apie puslapio **Pasiūlymo eilutės informacija** laukus ir tai, kaip reikšmės turi įtakos funkcijoms.

| **Laukas** | **Vieta** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Aprašymas | Spartusis kūrimas | Konkretaus įvertinimo aprašymas. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Operacijos klasė | Spartusis kūrimas | Šiame išplečiamajame sąraše pateikiamos operacijos klasės, įtrauktos į projektu pagrįstos pasiūlymo eilutės skirtuką **Bendra**.  | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Pasirinkti produktą | Spartusis kūrimas | Taikoma, kai operacijos klasė yra **Medžiaga**. Galite pasirinkti nurodyti, kad ši įvertinimo eilutė būtų skirta **esamam** (kataloge nurodytam) produktui arba **įtraukiamajam** produktui. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Produktas | Spartusis kūrimas | Produkto iš produktų katalogo ID. Šis laukas įjungiamas tik pasirinkus **Esamas** lauke **Pasirinkti produktą**. ID naudojamas norint gauti pardavimo kainą iš pasiūlymo projekto kainoraščio. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Įtraukiamasis produktas | Spartusis kūrimas | Teksto laukas, kuriame reikia įrašyti produkto pavadinimą. Šis laukas įjungiamas tik pasirinkus **Įtraukiamasis** lauke **Pasirinkti produktą**.| Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Vaidmuo | Spartusis kūrimas | Asmens, kuris atliks šį darbą arba patirs šias išlaidas, vaidmuo. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Kategorija. | Spartusis kūrimas | Darbo arba išlaidų kategorija. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Pradžios data | Spartusis kūrimas | Darbo pradžios data. | Šiam laukui pagal numatytuosius parametrus nustatoma pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Pabaigos data | Spartusis kūrimas | Darbo pabaigos data. | Šiam laukui pagal numatytuosius parametrus nustatoma pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Išteklių paskirstymo vienetas | Spartusis kūrimas | Išteklių skyrimo vienetas, pagal kurį bus taikoma ši savikaina ir pateikti ištekliai dirbti. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai ir naudojama savikainai gauti. |
| Vieneto grafikas | Spartusis kūrimas | Darbo, produkto arba išlaidų vienetų grupė. Vienetai priklauso vienetų grafikui arba vienetų grupei. Pavyzdžiui, mylios ir kilometrai yra vienetai, priklausantys vienetų grupei, kurioje aprašomas atstumas. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Vienetas | Spartusis kūrimas | Darbo, produkto arba išlaidų vienetas. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Kiekis | Spartusis kūrimas | Darbo, produkto arba išlaidų kiekis. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Vieneto kaina | Spartusis kūrimas |Darbą atliekančio vaidmens sąskaitų tarifas, produkto vieneto kaina arba produkto ar išlaidų kategorijos pardavimo kaina. Šiam laukui taikoma numatytoji **laiko** reikšmė, pagrįsta deriniu kainodaros dimensijų reikšmių, esančių vaidmens kainos eilutėje, susijusioje su projekto kainoraščiu, galiojančiu pradžios dieną. **Išlaidų** atveju numatytoji reikšmė nustatoma pagal operacijos kategorijos kainų sąranką projekto kainoraštyje, kuris galioja pradžios dieną. Jei operacijos kategorijos kainodaros būdas nėra vieneto kaina, numatytosios reikšmės nėra ir šis laukas lieka tuščias. Produktų atveju numatytasis parametras pagrįstas eilute **Kainų sąrašo elementas**, priklausančioje kainoraščiui, kuris galioja pradžios dieną.| Darbą atliekančio vaidmens savikainos tarifas, išlaidų kategorijos vieneto savikaina arba produkto vieneto savikaina. Šiam laukui taikoma numatytoji **laiko** reikšmė, pagrįsta deriniu kainodaros dimensijų reikšmių, esančių vaidmens kainos eilutėje, susijusioje su projekto kainoraščiu, galiojančiu pradžios dieną. **Išlaidų** atveju numatytoji reikšmė nustatoma pagal operacijos kategorijos kainų sąranką projekto kainoraštyje, kuris galioja pradžios dieną. Jei operacijos kategorijos kainodaros būdas nėra vieneto kaina, numatytosios reikšmės nėra ir šis laukas lieka tuščias. Produktų atveju numatytasis parametras pagrįstas eilute **Kainų sąrašo elementas**, priklausančioje kainoraščiui, kuris galioja pradžios dieną.|
| Įvertintas mokestis | Spartusis kūrimas | Galite rankiniu būdu įvesti numatomą šio darbo arba išlaidų mokestį. | Nėra jokio tolesnio šio lauko poveikio. |
| Suma | Spartusis kūrimas | Galite rankiniu būdu įvesti informaciją į šį lauką, jei laukai **Kiekis** ir **Kaina** paliekami tušti. Jei šie laukai nėra tušti, šis laukas tampa tik skaitomu ir apskaičiuojamas kaip (Kiekis \* Vieneto kaina) + mokestis. | Nėra jokio tolesnio šio lauko poveikio. |


## <a name="update-prices-on-quote-line-details"></a>Kainų atnaujinimas pasiūlymo eilutės informacijoje

Jei keitėte prie pasiūlymo pridėto projekto kainoraščio kainas arba sutartį sudarančio vieneto kainoraščio kainas, galite pasirinkti funkciją **Perskaičiuoti**, esančią puslapyje **Pasiūlymas**, kad atnaujintumėte kainas atskiros pasiūlymo eilutės išsamios informacijos dalyje, ir šis keitimas būtų pritaikytas. Pasirinkus **Perskaičiuoti** rodomas įspėjimas, kuriame informuojama, kad bus iš naujo nustatytos pasiūlymo eilutės informacijos kainos, susijusios su visomis pasiūlymo eilutėmis, pateikiamomis šiame pasiūlyme. Norėdami atnaujinti pardavimų ir išlaidų pasiūlymo eilutės išsamią informaciją, pasirinkite **Taip**.

## <a name="access-quote-line-details-for-cost"></a>Prieiga prie išlaidų pasiūlymo eilutės išsamios informacijos

Skirtuke **Pasiūlymo eilutės informacija** pažymėkite tinklelio eilutę, kad būtų įjungta keletas veiksmų papildomo tinklelio įrankių juostoje. Pirmasis veiksmas papildomo tinklelio įrankių juostoje, kai yra pasirinkta pasiūlymo eilutės informacija, yra **Atidaryti kaštų informaciją**. Pasirinkite **Atidaryti išlaidų informaciją**, kad matytumėte šios pasiūlymo eilutės išlaidų tarifą ir sumą.

> [!NOTE]
> Išteklių paskirstymo vieneto, kiekybės, datos, vaidmens arba kategorijos reikšmių keitimas išlaidų pasiūlymo eilutės išsamiojoje informacijoje pakeis atitinkamas reikšmes pardavimų pasiūlymo eilutės išsamiojoje informacijoje.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Išlaidų ir pardavimų pasiūlymo eilutės išsamios informacijos valiuta

Išlaidų ir pardavimų pasiūlymo eilutės išsamios informacijos valiuta pagal numatytąsias reikšmes perimama iš projekto kainoraščio, kuris galioja nuo pasiūlymo eilutės išsamios informacijos pradžios.

Išlaidų pasiūlymo eilutės išsamios informacijos valiuta pagal numatytąsias reikšmes perimama iš pasiūlymo sutartį sudarančio vieneto kainoraščio, kuris galioja nuo išlaidų pasiūlymo eilutės išsamios informacijos pradžios.

Pelningumo skaičiavimas konvertuoja išlaidų ir pardavimų pasiūlymo eilutės išsamią informaciją į pagrindinę aplinkos valiutą, kad praneštų apie bendrą numatomą pasiūlymo maržą.

> [!PASTABA
> > Dėl trūkstamų nuo datos priklausančių valiutos kursų gali įvykti valiutos apvalinimo klaidų ir pasikeisti maržos. Šiuos skaičiavimus naudokite tik projekto sutartyse, nes jie yra apytiksliai ir nėra skirti įstatymų nustatytoms faktinėms arba kitoms ataskaitoms, kuriose reikalaujama tiksliau apvalinti ir pateikti valiutų kursų įsigaliojimo datą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
