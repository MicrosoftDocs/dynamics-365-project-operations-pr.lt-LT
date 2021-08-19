---
title: Projekto pasiūlymo eilutės įvertinimas
description: Šioje temoje pateikiama informacija apie tai, kaip sukurti įvertinimą projekto pasiūlymo eilutėje.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 84283ac055aea802fadbd6814ea65a6d3dc01d29e1e3c6290ef11f72f6a75692
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003961"
---
# <a name="estimate-a-project-quote-line"></a>Projekto pasiūlymo eilutės įvertinimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projektu pagrįstoje pasiūlymo eilutėje pateikta išsami informacija, padedanti įvertinti darbo išlaidas ir potencialias pajamas, kad būtų sukurta pasiūlymo eilutė.

Norėdami įvertinti projektu pagrįstą pasiūlymo eilutę, pasiūlymo eilutėje pasirinkite skirtuką **Pasiūlymo eilutės informacija**. Sukurti įvertinimą projektu pagrįstoje pasiūlymo eilutėje galima dviem toliau nurodytais būdais.

   - Rankiniu būdu sukurti įvertinimą tiesiogiai pasiūlymo eilutėje naudojant pasiūlymo eilutės išsamią informaciją. 
   - Sukurti projektą ir projekto planą, o tada susieti projektą ir projekto užduotis su pasiūlymo eilute. Procesas, skirtas projekto plano įvertinimų importavimui į pasiūlymo eilutę pagal jūsų pateiktą informaciją, bus įjungtas.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Įvertinimų kūrimas tiesiogiai projektu pagrįstoje pasiūlymo eilutėje

Norėdami įvertinimus sukurti tiesiai projektu pagrįsto pasiūlymo eilutėje, atlikite toliau nurodytus veiksmus.

1. Jei norite kurti įvertinimą projektu pagrįstoje pasiūlymo eilutėje, pažymėkite skirtuką **Pasiūlymo eilutės informacija**. Šiame skirtuke sukurtas eilutės elementas apibendrins šios pasiūlymo eilutės pasiūlytą reikšmę. 
2. Norėdami sukurti pasiūlymo eilutės išsamią informaciją, papildomame tinklelyje **Pasiūlymo eilutės informacija** pasirinkite **Nauja pasiūlymo eilutės informacija**. Atsidarys sparčiojo kūrimo slankiklis. Toliau nurodyti puslapio **Pasiūlymo eilutė** laukai.

| **Laukas** | **Vieta** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Aprašymas | Spartusis kūrimas | Konkretaus įvertinimo aprašymas. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Operacijos klasė | Spartusis kūrimas | Šiame išplečiamajame sąraše pateikiamos operacijų klasės, įtrauktos į projektu pagrįstos pasiūlymo eilutės skirtuke **Bendra**.  | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Pasirinkti produktą | Spartusis kūrimas | Taikoma, kai operacijos klasė yra **Medžiaga**. Galite pasirinkti nurodyti, kad ši įvertinimo eilutė būtų skirta **esamam** (kataloge nurodytam) produktui arba **įtraukiamajam** produktui. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Produktas | Spartusis kūrimas | Produkto iš produktų katalogo ID. Šis laukas įjungiamas tik pasirinkus **Esamas** lauke **Pasirinkti produktą**. ID naudojamas norint gauti pardavimo kainą iš pasiūlymo projekto kainoraščio. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Įtraukiamasis produktas | Spartusis kūrimas | Teksto laukas, kuriame reikia įrašyti produkto pavadinimą. Šis laukas įjungiamas tik pasirinkus **Įtraukiamasis** lauke **Pasirinkti produktą**.| Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Vaidmuo | Spartusis kūrimas | Asmens, kuris atliks šį darbą arba patirs šias išlaidas, vaidmuo. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Kategorija. | Spartusis kūrimas | Darbo arba išlaidų kategorija. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Pradžios data | Spartusis kūrimas | Darbo pradžios data. | Šiam laukui pagal numatytuosius parametrus nustatoma pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Pabaigos data | Spartusis kūrimas | Darbo pabaigos data. | Šiam laukui pagal numatytuosius parametrus nustatoma pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Išteklių paskirstymo įmonė | Spartusis kūrimas | Išteklių paskirstymo įmonė arba juridinis subjektas, kuriam bus taikoma ši savikaina, ir kuris pateikia išteklių dirbti. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai, yra naudojama savikainai gauti. |
| Išteklių paskirstymo vienetas | Spartusis kūrimas | Išteklių skyrimo vienetas, pagal kurį taikoma ši savikaina ir pateikiami ištekliai dirbti. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai, yra naudojama savikainai gauti. |
| Vieneto grafikas | Spartusis kūrimas | Darbo, produkto arba išlaidų vienetų grupė. Vienetai priklauso vienetų grafikui arba vienetų grupei. Pavyzdžiui, mylios ir kilometrai yra vienetai, priklausantys vienetų grupei, kurioje aprašomas atstumas. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Vienetas | Spartusis kūrimas | Darbo, produkto arba išlaidų vienetas. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Kiekis | Spartusis kūrimas | Darbo, produkto arba išlaidų kiekis. | Šiai reikšmei pagal numatytuosius parametrus nustatoma susijusi pasiūlymo eilutės išsami informacija, taikoma automatiškai sukuriamai savikainai. |
| Vieneto kaina | Spartusis kūrimas |Darbą atliekančio vaidmens sąskaitų tarifas, produkto vieneto kaina arba produkto ar išlaidų kategorijos pardavimo kaina. Numatytoji **laiko** reikšmė pagrįsta deriniu kainodaros dimensijų reikšmių, esančių vaidmens kainos eilutėje, susijusioje su projekto kainoraščiu, galiojančiu pradžios dieną. **Išlaidų** atveju numatytoji reikšmė nustatoma pagal operacijos kategorijos kainų sąranką projekto kainoraštyje, kuris galioja pradžios dieną. Jei operacijos kategorijos kainodaros būdas nėra kaina už vienetą, numatytosios reikšmės nėra, o šis laukas paliekamas tuščias. Produktų atveju šio lauko numatytoji reikšmė pagrįsta eilute **Kainų sąrašo elementas**, priklausančia kainoraščiui, kuris galioja pradžios dieną.| Darbą atliekančio vaidmens savikainos tarifas, išlaidų kategorijos vieneto savikaina arba produkto vieneto savikaina. Numatytoji **laiko** reikšmė pagrįsta deriniu kainodaros dimensijų reikšmių, esančių vaidmens kainos eilutėje, susijusioje su savikainos kainoraščiu, susietu su sutartį sudarančiu vienetu, galiojančiu pradžios dieną. Išlaidų atveju numatytoji reikšmė yra pagrįsta kategorijos kainos eilute, priklausančia savikainos kainoraščiui, susietam su sutartį sudarančiu vienetu, galiojančiu pradžios dieną. Jei operacijos kategorijos kainodaros būdas nėra vieneto kaina, numatytosios reikšmės nėra ir šis laukas lieka tuščias. Produktų atveju šio lauko numatytoji reikšmė yra pagrįsta **kainų sąrašo elemento** eilute, priklausančia savikainos kainoraščiui, susietam su sutartį sudarančiu vienetu, galiojančiu pradžios dieną.|
| Įvertintas mokestis | Spartusis kūrimas | Galite rankiniu būdu įvesti numatomą šio darbo arba išlaidų mokestį. | Nėra jokio tolesnio šio lauko poveikio. |
| Suma | Spartusis kūrimas | Galite rankiniu būdu įvesti informaciją į šį lauką, jei laukai **Kiekis** ir **Kaina** paliekami tušti. Jei šie laukai nėra tušti, šis laukas tampa tik skaitomu ir apskaičiuojamas kaip (Kiekis \* Vieneto kaina) + mokestis. | Nėra jokio tolesnio šio lauko poveikio. |

## <a name="update-prices-on-quote-line-details"></a>Kainų atnaujinimas pasiūlymo eilutės informacijoje

Jei pakeitėte kainas projekto kainoraštyje, kuris pridėtas prie pasiūlymo, arba sutartį sudarančio vieneto savikainos kainoraštyje, galite pažymėti parinktį **Perskaičiuoti**, esančią puslapyje **Pasiūlymas**, kad atnaujintumėte kainas individualios pasiūlymo eilutės išsamiojoje informacijoje. Pasirinkus **Perskaičiuoti** rodomas įspėjimas, kuriame informuojama, kad bus iš naujo nustatytos pasiūlymo eilutės informacijos kainos, susijusios su visomis pasiūlymo eilutėmis, pateikiamomis šiame pasiūlyme. Norėdami atnaujinti pardavimų ir išlaidų pasiūlymo eilutės išsamią informaciją, pasirinkite **Taip**.

## <a name="access-quote-line-details-for-cost"></a>Prieiga prie išlaidų pasiūlymo eilutės išsamios informacijos

Norėdami gauti prieigą prie pasiūlymo eilutės išlaidų informacijos, skirtos savikainai, atlikite toliau nurodytus veiksmus.

1. Skirtuke **Pasiūlymo eilutės informacija** pasirinkite tinklelio eilutę ir įjunkite veiksmus papildomo tinklelio įrankių juostoje. 
2. Pasirinkite **Atidaryti išlaidų informaciją**, kad matytumėte šios pasiūlymo eilutės išlaidų tarifą ir sumą.

> [!NOTE]
> Išteklių paskirstymo vieneto, kiekybės, datos, vaidmens arba kategorijos reikšmių keitimas išlaidų pasiūlymo eilutės išsamiojoje informacijoje pakeis atitinkamas reikšmes pardavimų pasiūlymo eilutės išsamiojoje informacijoje.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Išlaidų ir pardavimų pasiūlymo eilutės išsamios informacijos valiuta

Pardavimo pasiūlymo eilutės informacijos valiutai numatytoji reikšmė nustatoma pagal projekto kainoraštį, kuris galioja pasiūlymo eilutės informacijos pradžios dieną.

Savikainos pasiūlymo eilutės informacijos valiutai numatytoji reikšmė nustatoma pagal pasiūlymo sutartį sudarančio vieneto kainoraštį, kuris galioja savikainos pasiūlymo eilutės informacijos pradžios dieną.

> [!NOTE]
> Pelningumo skaičiavimas konvertuoja išlaidų ir pardavimų pasiūlymo eilutės išsamią informaciją į pagrindinę aplinkos valiutą, kad praneštų apie bendrą numatomą pasiūlymo maržą. Dėl trūkstamų nuo datos priklausančių valiutos kursų gali įvykti valiutos apvalinimo klaidų ir pasikeisti maržos. Šiuos skaičiavimus naudokite tik projekto pasiūlymuose, nes jie yra apytiksliai ir nėra skirti įstatymų nustatytoms faktinėms arba kitoms ataskaitoms, kuriose reikalaujama tiksliau apvalinti ir pateikti valiutų kursų įsigaliojimo datą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
