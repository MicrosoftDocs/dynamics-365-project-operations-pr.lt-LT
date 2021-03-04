---
title: Projektų kainoraščių valdymas pasiūlyme
description: Šioje temoje pateikta informacija apie projektų kainoraščio objektą.
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
ms.openlocfilehash: 5fc8691984e22b2fa35e26b1a7d94cc56c25c26d
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177206"
---
# <a name="manage-project-price-lists-on-a-quote"></a>Projektų kainoraščių valdymas pasiūlyme

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ išplėtė kainoraščio objektą programoje „Dynamics 365 Sales“. 

## <a name="key-entities"></a>Pagrindiniai objektai

Kainoraštis apima keturių skirtingų objektų teikiamą informaciją.

- **Kainoraštis** – tai objektas, kuriame saugoma informacija apie laiko kainų kontekstą, valiutą, galiojimo datas ir laiko vienetą. Kontekstas parodo, ar kainoraštyje pateikiami išlaidų ar pardavimo tarifai. 
- **Valiuta** – tai objektas, kuriame saugoma kainoraščio kainų valiuta. 
- **Data** – šis objektas naudojamas, kai sistema bando įvesti numatytąją operacijos kainą. Pasirinktas kainoraštis, turintis galiojimo datą, į kurią įeina operacijos data. Jei randamas daugiau nei vienas kainoraštis, kuris galioja operacijos datai ir yra pridėtas prie susijusio pasiūlymo, sutarties ar organizacinio vieneto, jokia kaina nėra nustatoma kaip numatytoji. 
- **Laikas** – šiame objekte išsaugomas laiko vienetas, pagal kurį nurodomos kainos, pvz., dienos ar valandinis tarifas. 

Objektą Kainoraštis sudaro trys toliau nurodytos susijusios lentelės, kuriose saugomos kainos.

  - **Vaidmenų kaina** – šioje lentelėje saugomi vaidmenų ir organizacijos vienetų reikšmių derinių tarifai. Ji naudojama žmogiškųjų išteklių vaidmenų kainoms nustatyti.
  - **Operacijų kategorijų kaina** – šioje lentelėje kainos nustatomos pagal operacijų kategoriją ir naudojamos išlaidų kategorijų kainoms nustatyti.
  - **Kainoraščio elementai** – šioje lentelėje saugomos katalogo produktų kainos.
 
Kainoraštis – tai tarifų kortelė. Tarifų kortelė – tai objekto Kainoraštis ir susijusių lentelių Vaidmenų kaina, Operacijų kategorijų kaina bei Kainoraščio elementai eilučių derinys.

## <a name="resource-roles"></a>Išteklių vaidmenys

Terminas *išteklių vaidmuo* nurodo įgūdžių, kompetencijų ir sertifikatų rinkinį, kurį turi atlikti asmuo, kad galėtų atlikti konkretų projekto užduočių rinkinį.

Žmogiškųjų išteklių laiko kaina paprastai nustatoma atsižvelgiant į ištekliaus vaidmenį tam tikrame projekte. Nustatant žmogiškųjų išteklių laiką, įkainojimas ir atsiskaitymas vyksta remiantis išteklių vaidmenimi. Laiko kainą galima nustatyti naudojant bet kokį vienetų grupės **Laikas** vienetą.

**Laiko** vienetų grupė sukuriama diegiant „Project Operations“. Jos numatytasis vienetas yra **Valanda**. Vienetų grupės **Laikas** ir vieneto **Valanda** atributų negalima panaikinti, pervardyti arba redaguoti. Tačiau į vienetų grupę **Laikas** galima įtraukti kitų vienetų. Jei bandysite panaikinti vienetų grupę **Laikas** arba vienetą **Valanda**, verslo logika gali sutrikti.
 
## <a name="transaction-categories-and-expense-categories"></a>Operacijų kategorijos ir išlaidų kategorijos

Sąskaitos už projekto konsultantų keliones ir kitas išlaidas paprastai išrašomos klientui. Išlaidų kategorijų kainodara užbaigiama naudojant kainoraščius. Pavyzdžiui, galimos išlaidų kategorijos yra lėktuvų bilietų, viešbučių ir automobilių nuomos išlaidos. Kiekvienoje kainoraščio išlaidų eilutėje nurodoma konkrečios išlaidų kategorijos kaina. Toliau nurodyti trys būdai naudojami kainų išlaidų kategorijoms:

- **Pagal savikainą** – klientui išrašoma sąskaita pagal išlaidų savikainą, netaikant jokio antkainio.
- **Antkainio procentas** – klientui išrašoma sąskaita prie faktinių išlaidų pridedant procentinę dalį. 
- **Vieneto kaina** – nustatoma kiekvienos išlaidų kategorijos atsiskaitymo vieneto kaina. Klientui išrašomos sąskaitos suma apskaičiuojama pagal konsultanto praneštų išlaidų vienetų skaičių. Kilometražui naudojamas kainos už vienetą kainodaros metodas. Pavyzdžiui, kilometražo išlaidų kategoriją galima sukonfigūruoti nustatant 30 JAV dolerių (USD) už dieną arba 2 USD už mylią. Kai konsultantas praneša projekto kilometražą, sąskaitos suma apskaičiuojama pagal konsultanto praneštą mylių skaičių.
 
## <a name="project-sales-pricing-and-overrides"></a>Projekto pardavimo kainodara ir keitimai

Projekto pasiūlymams ir sutartims taikomas kitoks projekto kainoraščio kainų keitimo modelis nei produktų kainoraščiui. Produktų katalogu pagrįstoje pasiūlymo eilutėje galite pakeisti vaidmenų ir kategorijų kainas tiesiog pasiūlymo eilutėje, nes kiekviena pasiūlymo eilutė nurodo tik vieną katalogo prekę. Tačiau projektu pagrįstoje pasiūlymo eilutėje negalima keisti vaidmenų ir kategorijų kainų tiesiog pasiūlymo eilutėje. Naudokite projekto kainoraštį dviem skirtingais perrašymo modeliams palaikyti.

> [!NOTE]
> Rekomenduojame turėti atskirą projekto išteklių kainoraštį ir katalogo prekių kainoraštį, nes keičiant kainas jie veikia skirtingai.

Kiekvienam iš toliau nurodytų objektų galima sudaryti vieną arba kelis susijusius projekto kainodaros pardavimo kainoraščius.

- Klientas (kodas) 
- Galimybė 
- Pasiūlymas 
- Projekto sutartis

Šių objektų susiejimą su kainoraščiu nurodo projekto kainoraščiai. Su pardavimo objektais Klientas, Galimybė, Pasiūlymas ir Projekto sutartis galite susieti vieną arba kelis kainoraščius.

Numatytasis projekto kainoraštis nėra automatiškai pridedamas prie kliento įrašo. Tačiau projekto kainoraštį prie kliento įrašo galite pridėti patys. Vis dėlto projekto kainoraštį pridėti patys turėtumėte, tik jei su klientu esate sudarę pasirinktinės kainodaros sutartį. 

Kai projekto kainoraštis pridedamas prie pardavimo objekto, tikrinama toliau nurodyta informacija:

- Kainoraščio kontekstas yra **Pardavimas**. 
- Kainoraščio valiuta atitinka kliento valiutą. 

Automatiškai nustatant susijusius projekto kainoraščius projekto sutartyje naudojama toliau nurodytą pirmumo seka:

1. Pasiūlymas
2. Galimybė
3. Klientas 
4. Visuotiniai parametrai 

Kai projekto kainoraštis įvedamas pagal numatytuosius parametrus, sistema tikrina, ar valiuta atitinka kliento valiutą, ir įvestų numatytųjų kainoraščių kontekstas yra **Pardavimai**.

Galite susieti kelis kainoraščius su objektais Klientas, Galimybė, Pasiūlymas ir Projekto sutartis. Jei sudarant ilgalaikių projektų sutartis jums gali prireikti daugiau nei vieno kainoraščio, siekiant įtraukti dėl infliacijos atnaujintas kainas, šis pajėgumas palaiko konkrečiai datai nustatomas kainas. Tačiau jei su objektais Klientas, Galimybė, Pasiūlymas arba Projekto sutartis susietų kainoraščių galiojimo datos persidengia, numatytosios kainos gali būti netinkamos. Todėl reikia užtikrinti, kad projekto kainoraščiai, kurių galiojimo datos persidengia, nebūtų susieti su šiais objektais.

### <a name="deal-specific-price-overrides"></a>Konkrečių sandorių kainų keitimas

Galite pakeisti tam tikrų projekto kainoraščių pasirinktas kainas, kurios į pasiūlymą arba projekto sutartį buvo įvestos pagal numatytuosius parametrus.

Pagal numatytuosius parametrus į projekto sutartį visada įtraukiama pagrindinio pardavimo kainoraščio kopija, o ne tiesioginis jo saitas. Tai leidžia užtikrinti, kad pakeitus pagrindinį kainoraštį su klientu suderinti susitarimai dėl darbų sąrašo (SOW) nesikeis.

Tačiau pasiūlyme galite naudoti pagrindinį kainoraštį. Taip pat galite nukopijuoti pagrindinį kainoraštį ir jį redaguoti, kad sukurtumėte pasirinktinį kainoraštį, taikomą tik tam pasiūlymui. Jei norite sukurti naują konkretaus pasiūlymo kainoraštį, puslapyje **Pasiūlymas** pasirinkite **Kurti pasirinktines kainas**. Iš pasiūlymo galite pasiekti tik konkretaus sandorio projekto kainoraštį. 

Kai kuriate pasirinktinį projekto kainoraštį, iš kainoraščio nukopijuojami tik projekto komponentai. Kitaip tariant, naujas kainoraštis sukuriamas kaip esamo projekto kainoraščio, kuris pridedamas prie pasiūlymo, kopija ir šiame naujame kainoraštyje pateikiamos tik su vaidmenimis susijusios kainos ir operacijų kategorijų kainos.
  
## <a name="tracking-costs"></a>Išlaidų sekimas

„Project Operations“ seka su projektais susijusių žmogiškųjų išteklių laiko sąnaudas. Ji taip pat seka kitų išlaidas, patirtas projekto metu, pvz., kelionės išlaidas.

Kaip ir sąskaitų tarifai, žmogiškųjų išteklių išlaidų tarifai nustatomi naudojant kainoraščius. Toliau nurodyti pagrindiniai išlaidų tarifų sąrašo ir pardavimo kainoraščio skirtumai.

- Konkretaus projekto, sutarties arba pasiūlymo išteklių išlaidų tarifų negalima keisti. Tačiau konkretaus sandorio sąskaitų tarifus galima keisti, jei atlikti pakeitimai atitinka sandorio pobūdį. 

- Toliau aprašytas užsakymas naudojamas siekiant pašalinti išlaidų kainoraščio konfliktą.

    1. Išlaidų kainoraštis, susietas su organizacijos vienetu.
    2. Išlaidų kainoraštis, susietas su „Project Operations“ parametrais. Kadangi su parametrais galima susieti išlaidų kainoraščius keliomis skirtingomis valiutomis, valiutos pritaikymas vyksta tarp projektą, sutartį ar pasiūlymą pasirašiusios organizacijos vieneto ir savikainos kainoraščio valiutos.
    3. Išlaidų kainoraščiams netaikomi kainodaros pagal savikainą ir savikainos antkainio metodai. Net jei šie kainodaros metodai naudojami išlaidų kainoraščio eilutėse siekiant nustatyti operacijų kategorijų išlaidas, sistema juos ignoruoja ir neįveda jokių numatytųjų savikainų.


[!INCLUDE[footer-include](../includes/footer-banner.md)]