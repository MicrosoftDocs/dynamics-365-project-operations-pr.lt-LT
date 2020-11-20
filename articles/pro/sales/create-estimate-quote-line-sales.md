---
title: Projektu pagrįstos pasiūlymo eilutės įvertinimas
description: Šioje temoje pateikta informacija apie tai, kaip sukurti įvertinimą projektu pagrįstai pasiūlymo eilutei.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 56892a134c0c739958f7f939214930631dea7420
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180382"
---
# <a name="estimating-a-project-based-quote-line"></a>Projektu pagrįstos pasiūlymo eilutės įvertinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projektu pagrįstoje pasiūlymo eilutėje pateikta išsami informacija, padedanti įvertinti darbo išlaidas ir potencialias pajamas, kad būtų sukurta pasiūlymo eilutė.

Norėdami įvertinti projektu pagrįstą pasiūlymo eilutę, projektu pagrįstoje pasiūlymo eilutėje pažymėkite skirtuką **Pasiūlymo eilutės informacija**. Yra du būdai apskaičiuoti projektu pagrįstos pasiūlymo eilutės įvertinimą:

- Rankiniu būdu sukurti įvertinimą tiesiogiai pasiūlymo eilutėje naudojant pasiūlymo eilutės išsamią informaciją 
- Sukurti projektą ir projekto planą, o tada susieti projektą ir projekto užduotis su pasiūlymo eilute. Procesas, skirtas projekto plano įvertinimų importavimui į pasiūlymo eilutę pagal jūsų pateiktą informaciją, bus įjungtas.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Įvertinimų kūrimas tiesiogiai projektu pagrįstoje pasiūlymo eilutėje

Jei norite kurti įvertinimą projektu pagrįstoje pasiūlymo eilutėje, pažymėkite skirtuką **Pasiūlymo eilutės informacija**. Šiame skirtuke sukurtas eilutės elementas apibendrins šios pasiūlymo eilutės pasiūlytą reikšmę. 

Norėdami sukurti pasiūlymo eilutės išsamią informaciją, papildomame tinklelyje **Pasiūlymo eilutės informacija** pasirinkite **+ Nauja pasiūlymo eilutės informacija**. Atsidarys sparčiojo kūrimo slankiklis. Toliau nurodyti laukai, esantys formoje **Pasiūlymo eilutė**:

| **Laukas** | **Vieta** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Aprašo | Spartusis kūrimas | Konkretaus įvertinimo aprašymas. | Šio lauko numatytosios reikšmės nurodytos automatiškai sukurtoje susijusios pasiūlymo eilutės savikainos išsamioje informacijoje. |
| Operacijos klasė | Spartusis kūrimas | Šiame išplečiamajame sąraše pateikiamos operacijų klasės, įtrauktos į projektu pagrįstos pasiūlymo eilutės skirtuke **Bendra**.  | Šio lauko numatytosios reikšmės nurodytos automatiškai sukurtoje susijusios pasiūlymo eilutės savikainos išsamioje informacijoje. |
| Vaidmuo | Spartusis kūrimas | Asmuo, kuris atliks šį darbą arba patiriantis šias išlaidas. | Šio lauko numatytosios reikšmės nurodytos automatiškai sukurtoje susijusios pasiūlymo eilutės savikainos išsamioje informacijoje. |
| Kategorija. | Spartusis kūrimas | Darbo arba išlaidų kategorija | Šio lauko numatytosios reikšmės nurodytos automatiškai sukurtoje susijusios pasiūlymo eilutės savikainos išsamioje informacijoje. |
| Pradžios data | Spartusis kūrimas | Darbo pradžios data. | Šio lauko numatytosios reikšmės nurodytos automatiškai sukurtoje susijusios pasiūlymo eilutės savikainos išsamioje informacijoje. |
| Pabaigos data | Spartusis kūrimas | Darbo pabaigos data. | Šio lauko numatytosios reikšmės nurodytos automatiškai sukurtoje susijusios pasiūlymo eilutės savikainos išsamioje informacijoje. |
| Išteklių paskirstymo vienetas | Spartusis kūrimas | Išteklių skyrimo vienetas, kuris patirs šias išlaidas ir pateiks išteklius darbui. | Šio lauko numatytosios reikšmės nurodytos automatiškai sukurtoje susijusios pasiūlymo eilutės savikainos išsamioje informacijoje. Šis laukas taip pat naudojamas savikainai gauti. |
| Vieneto grafikas | Spartusis kūrimas | Darbo arba išlaidų vienetų grupė. Vienetai priklauso vienetų grafikui arba vienetų grupei. Pavyzdžiui, „Miles“ ir „KMs“ yra vienetai, priklausantys vienetų grupei, kuri aprašo atstumą. | Šio lauko numatytosios reikšmės nurodytos automatiškai sukurtoje susijusios pasiūlymo eilutės savikainos išsamioje informacijoje. |
| Vienetas | Spartusis kūrimas | Darbo arba išlaidų vienetai. | Šio lauko numatytosios reikšmės nurodytos automatiškai sukurtoje susijusios pasiūlymo eilutės savikainos išsamioje informacijoje. |
| Kiekis | Spartusis kūrimas | Darbo arba išlaidų kiekis. | Šio lauko numatytosios reikšmės nurodytos automatiškai sukurtoje susijusios pasiūlymo eilutės savikainos išsamioje informacijoje. |
| Vieneto kaina | Spartusis kūrimas | Darbą atliekančio vaidmens sąskaitos tarifas arba išlaidų kategorijos pardavimų kaina. Šio lauko numatytosios reikšmės laikas pagal vaidmenį ir išteklių vieneto derinį projekto kainoraštyje, kuris galioja pradžios datą. Išlaidų srityje šio lauko numatytosios reikšmės nustatytos kaip operacijos kategorijos projekto kainų sąraše, kuris galioja pradžios datą. Jei operacijos kategorijos kainodaros būdas nėra kaina už vienetą, numatytosios reikšmės nėra, o šis laukas paliekamas tuščias. | Darbą atliekančio vaidmens savikainos tarifas arba išlaidų kategorijos kainą per vienetą. Šio lauko numatytosios reikšmės laikas pagal vaidmenį ir išteklių vieneto derinį sutartį sudarančio vieneto kainos pasiūlymo kainoraštyje, kuris galioja pradžios datą. Išlaidų srityje šio lauko numatytosios reikšmės nustatytos kaip operacijos kategorijos sutartį sudarančio vieneto savikainos kainų sąraše, kuris galioja pradžios datą. Jei operacijos kategorijos kainodaros būdas nėra kaina už vienetą, numatytosios reikšmės nėra, o šis laukas paliekamas tuščias. |
| Įvertintas mokestis | Spartusis kūrimas | Galite rankiniu būdu įvesti numatomą šio darbo arba išlaidų mokestį. | Nėra jokio tolesnio šio lauko poveikio. |
| Suma | Spartusis kūrimas | Galite rankiniu būdu įvesti informaciją į šį lauką, jei laukai **Kiekis** ir **Kaina** paliekami tušti. Jei šie laukai nėra tušti, šis laukas tampa tik skaitomu ir apskaičiuojamas kaip (Kiekis\*Vieneto kaina) + mokestis. | Nėra jokio tolesnio šio lauko poveikio. |

## <a name="update-prices-on-quote-line-details"></a>Kainų atnaujinimas pasiūlymo eilutės informacijoje

Jei pakeitėte kainas projekto kainoraštyje, kuris pridėtas prie pasiūlymo, arba sutartį sudarančio vieneto savikainos kainoraštyje, galite pažymėti parinktį **Perskaičiuoti**, esančią puslapyje **Pasiūlymas**, kad atnaujintumėte kainas individualios pasiūlymo eilutės išsamiojoje informacijoje. Kai pasirenkate **Perskaičiuoti**, atsiranda įspėjimas, kuris informuoja, kad kainos pasiūlymo eilutės išsamiojoje informacijoje apie visas pasiūlymo eilutes šiame pasiūlyme bus nustatyta iš naujo. Norėdami atnaujinti pardavimų ir išlaidų pasiūlymo eilutės išsamią informaciją, pasirinkite **Taip**.

## <a name="access-quote-line-details-for-cost"></a>Prieiga prie išlaidų pasiūlymo eilutės išsamios informacijos

Skirtuke **Pasiūlymo eilutės informacija** pažymėkite tinklelio eilutę, kad būtų įjungta keletas veiksmų papildomo tinklelio įrankių juostoje. Pirmasis veiksmas papildomo tinklelio įrankių juostoje, kai yra pasirinkta pasiūlymo eilutės informacija, yra **Atidaryti kaštų informaciją**. Pasirinkite **Atidaryti išlaidų informaciją**, kad matytumėte šios pasiūlymo eilutės išlaidų tarifą ir sumą.

> [!NOTE]
> Išteklių paskirstymo vieneto, kiekybės, datos, vaidmens arba kategorijos reikšmių keitimas išlaidų pasiūlymo eilutės išsamiojoje informacijoje pakeis atitinkamas reikšmes pardavimų pasiūlymo eilutės išsamiojoje informacijoje.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Išlaidų ir pardavimų pasiūlymo eilutės išsamios informacijos valiuta

Išlaidų ir pardavimų pasiūlymo eilutės išsamios informacijos valiuta pagal numatytąsias reikšmes perimama iš projekto kainoraščio, kuris galioja nuo pasiūlymo eilutės išsamios informacijos pradžios.

Išlaidų pasiūlymo eilutės išsamios informacijos valiuta pagal numatytąsias reikšmes perimama iš pasiūlymo sutartį sudarančio vieneto kainoraščio, kuris galioja nuo išlaidų pasiūlymo eilutės išsamios informacijos pradžios.

Pelningumo skaičiavimas konvertuoja išlaidų ir pardavimų pasiūlymo eilutės išsamią informaciją į pagrindinę aplinkos valiutą, kad praneštų apie bendrą numatomą pasiūlymo maržą.

Dėl šios priežasties gali atsirasti valiutos apvalinimo klaidų ir maržos pokyčių dėl datų efektyvumo keitimo kursų stokos. Šiuos skaičiavimus naudokite tik su projekto pasiūlymais kaip suderinimus, o ne faktines teisės aktų nustatytas arba kitokias ataskaitas, kurioms reikia tikslesnio apvalinimo ir didesnio datos efektyvumo valiutos kursams.
