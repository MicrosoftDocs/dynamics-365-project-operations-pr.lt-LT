---
title: Projekto kainodara
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Service Automation“ kainodarą.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: dfbfb59547f295e5fb275264b9222bfa20517f6278144ca013e14a99454b6840
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000586"
---
# <a name="project-pricing"></a>Projekto kainodara 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

„Dynamics 365 Project Service Automation“ išplečia „Dynamics 365 Sales“ objektą Kainoraštis. 

## <a name="key-entities"></a>Pagrindiniai objektai

Kainoraštis apima keturių skirtingų objektų teikiamą informaciją.

- **Kainoraštis** – tai objektas, kuriame saugoma informacija apie laiko kainų kontekstą, valiutą, galiojimo datas ir laiko vienetą. Kontekstas parodo, ar kainoraštyje pateikiami išlaidų ar pardavimo tarifai. 
- **Valiuta** – tai objektas, kuriame saugoma kainoraščio kainų valiuta. 
- Objektas **Data** naudojamas, kai sistema bando įvesti numatytąją operacijos kainą. PSA kainodarai pasirenkamas kainoraštis, kurio galiojimo data apima operacijos datą. Jei PSA kainodara randa daugiau nei vieną prie susijusio pasiūlymo, sutarties ar organizacijos vieneto pridedamą kainoraštį, kuris galioja operacijos datai, jokia kaina nėra nustatoma kaip numatytoji. 
- Objekte **Laikas** išsaugomas laiko vienetas, pagal kurį nurodomos kainos, pvz., dienos ar valandinis tarifas. 

Objektą Kainoraštis sudaro trys toliau nurodytos susijusios lentelės, kuriose saugomos kainos.

  - **Vaidmenų kaina** – šioje lentelėje saugomi vaidmenų ir organizacijos vienetų reikšmių derinių tarifai. Ji naudojama žmogiškųjų išteklių vaidmenų kainoms nustatyti.
  - **Operacijų kategorijų kaina** – šioje lentelėje kainos nustatomos pagal operacijų kategoriją ir naudojamos išlaidų kategorijų kainoms nustatyti.
  - **Kainoraščio elementai** – šioje lentelėje saugomos katalogo produktų kainos.

> ![Kainų konfigūravimas naudojant kainoraštį.](media/basic-guide-12.png)
 
Kainoraštis – tai tarifų kortelė. Tarifų kortelė – tai objekto Kainoraštis ir susijusių lentelių Vaidmenų kaina, Operacijų kategorijų kaina bei Kainoraščio elementai eilučių derinys.

## <a name="resource-roles"></a>Išteklių vaidmenys

Terminas *išteklių vaidmuo* nurodo įgūdžių, kompetencijų ir sertifikatų rinkinį, kurį turi atlikti asmuo, kad galėtų atlikti konkretų projekto užduočių rinkinį.

Žmogiškųjų išteklių laiko kaina paprastai nustatoma atsižvelgiant į ištekliaus vaidmenį tam tikrame projekte. Nustatant žmogiškųjų išteklių laiko kainas PSA programoje naudojamos įkainojimo ir atsiskaitymo pagal ištekliaus vaidmenį funkcijos. Laiko kainą galima nustatyti naudojant bet kokį vienetų grupės **Laikas** vienetą.

Įdiegus PSA, sukuriama vienetų grupė **Laikas**. Jos numatytasis vienetas yra **Valanda**. Vienetų grupės **Laikas** ir vieneto **Valanda** atributų negalima panaikinti, pervardyti arba redaguoti. Tačiau į vienetų grupę **Laikas** galima įtraukti kitų vienetų. Jei bandysite panaikinti vienetų grupę **Laikas** arba vienetą **Valanda**, PSA verslo logika gali sutrikti.

> ![Kainų konfigūravimas pagal vaidmenį.](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Operacijų kategorijos ir išlaidų kategorijos

Sąskaitos už projekto konsultantų keliones ir kitas išlaidas paprastai išrašomos klientui. PSA palaiko išlaidų kategorijų kainodarą naudodama kainoraščius. Pavyzdžiui, galimos išlaidų kategorijos yra lėktuvų bilietų, viešbučių ir automobilių nuomos išlaidos. Kiekvienoje kainoraščio išlaidų eilutėje nurodoma konkrečios išlaidų kategorijos kaina. Nustatant išlaidų kategorijų kainas PSA palaiko tris toliau nurodytus kainodaros metodus.

- **Pagal savikainą** – klientui išrašoma sąskaita pagal išlaidų savikainą, netaikant jokio antkainio.
- **Antkainio procentas** – klientui išrašoma sąskaita prie faktinių išlaidų pridedant procentinę dalį. 
- **Vieneto kaina** – nustatoma kiekvienos išlaidų kategorijos atsiskaitymo vieneto kaina. Klientui išrašomos sąskaitos suma apskaičiuojama pagal konsultanto praneštų išlaidų vienetų skaičių. Kilometražui naudojamas kainos už vienetą kainodaros metodas. Pavyzdžiui, kilometražo išlaidų kategoriją galima sukonfigūruoti nustatant 30 JAV dolerių (USD) už dieną arba 2 USD už mylią. Kai konsultantas praneša projekto kilometražą, sąskaitos suma apskaičiuojama pagal konsultanto praneštą mylių skaičių.

> ![Išlaidų kategorijų kainos konfigūravimas.](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Projekto pardavimo kainodara ir keitimai

Projekto pasiūlymams ir sutartims taikomas kitoks projekto kainoraščio kainų keitimo modelis nei produktų kainoraščiui. Produktų katalogu pagrįstoje pasiūlymo eilutėje galite pakeisti vaidmenų ir kategorijų kainas tiesiog pasiūlymo eilutėje, nes kiekviena pasiūlymo eilutė nurodo tik vieną katalogo prekę. Tačiau projektu pagrįstoje pasiūlymo eilutėje negalima keisti vaidmenų ir kategorijų kainų tiesiog pasiūlymo eilutėje. Siekiant palaikyti du atskirus keitimo modelius PSA pristatomas naujas kainoraščių susiejimas – projekto kainoraštis.

> [!NOTE]
> Rekomenduojame turėti atskirą projekto išteklių kainoraštį ir katalogo prekių kainoraštį, nes keičiant kainas jie veikia skirtingai.

Kiekvienam iš toliau nurodytų objektų galima sudaryti vieną arba kelis susijusius projekto kainodaros pardavimo kainoraščius.

- Klientas (kodas) 
- Galimybė 
- Pasiūlymas 
- Projekto sutartis

Šių objektų susiejimą su kainoraščiu nurodo projekto kainoraščiai. Su pardavimo objektais Klientas, Galimybė, Pasiūlymas ir Projekto sutartis galite susieti vieną arba kelis kainoraščius.

Numatytasis projekto kainoraštis nėra automatiškai pridedamas prie kliento įrašo. Tačiau projekto kainoraštį prie kliento įrašo galite pridėti patys. Vis dėlto projekto kainoraštį pridėti patys turėtumėte, tik jei su klientu esate sudarę pasirinktinės kainodaros sutartį. 

Kai projekto kainoraštis pridedamas prie pardavimo objekto, PSA tikrina toliau nurodytą informaciją.

- Kainoraščio kontekstas yra **Pardavimas**. 
- Kainoraščio valiuta atitinka kliento valiutą. 

Automatiškai nustatydama susijusius projekto kainoraščius projekto sutartyje PSA naudoja toliau nurodytą pirmumo seką.

1. Pasiūlymas
2. Galimybė
3. Klientas 
4. Visuotiniai PSA parametrai

Kai projekto kainoraštis įvedamas pagal numatytuosius parametrus, PSA tikrina, ar valiuta atitinka kliento valiutą, ir įvestų numatytųjų kainoraščių kontekstas yra **Pardavimas**.

Galite susieti kelis kainoraščius su objektais Klientas, Galimybė, Pasiūlymas ir Projekto sutartis. Jei sudarant ilgalaikių projektų sutartis jums gali prireikti daugiau nei vieno kainoraščio, siekiant įtraukti dėl infliacijos atnaujintas kainas, šis pajėgumas palaiko konkrečiai datai nustatomas kainas. Tačiau jei su objektais Klientas, Galimybė, Pasiūlymas arba Projekto sutartis susietų kainoraščių galiojimo datos persidengia, numatytosios kainos gali būti netinkamos. Todėl reikia užtikrinti, kad projekto kainoraščiai, kurių galiojimo datos persidengia, nebūtų susieti su šiais objektais.

### <a name="deal-specific-price-overrides"></a>Konkrečių sandorių kainų keitimas

Naudodami PSA galite pakeisti tam tikrų projekto kainoraščių pasirinktas kainas, kurios į pasiūlymą arba projekto sutartį buvo įvestos pagal numatytuosius parametrus.

Pagal numatytuosius parametrus į projekto sutartį visada įtraukiama pagrindinio pardavimo kainoraščio kopija, o ne tiesioginis jo saitas. Tai leidžia užtikrinti, kad pakeitus pagrindinį kainoraštį su klientu suderinti susitarimai dėl darbų sąrašo (SOW) nesikeis.

Tačiau pasiūlyme galite naudoti pagrindinį kainoraštį. Taip pat galite nukopijuoti pagrindinį kainoraštį ir jį redaguoti, kad sukurtumėte pasirinktinį kainoraštį, taikomą tik tam pasiūlymui. Jei norite sukurti naują konkretaus pasiūlymo kainoraštį, puslapyje **Pasiūlymas** pasirinkite **Kurti pasirinktines kainas**. Iš pasiūlymo galite pasiekti tik konkretaus sandorio projekto kainoraštį. 

Kai kuriate pasirinktinį projekto kainoraštį, iš kainoraščio nukopijuojami tik projekto komponentai. Kitaip tariant, naujas kainoraštis sukuriamas kaip esamo projekto kainoraščio, kuris pridedamas prie pasiūlymo, kopija ir šiame naujame kainoraštyje pateikiamos tik su vaidmenimis susijusios kainos ir operacijų kategorijų kainos.

> ![Projekto sutarties pasirinktinių kainų peržiūra ir konfigūravimas.](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Išlaidų sekimas

PSA seka su projektais susijusių žmogiškųjų išteklių laiko sąnaudas. Ji taip pat seka kitų išlaidas, patirtas projekto metu, pvz., kelionės išlaidas.

Kaip ir sąskaitų tarifai, žmogiškųjų išteklių išlaidų tarifai nustatomi naudojant kainoraščius. Toliau nurodyti pagrindiniai išlaidų tarifų sąrašo ir pardavimo kainoraščio skirtumai.

- Konkretaus projekto, sutarties arba pasiūlymo išteklių išlaidų tarifų negalima keisti. Tačiau konkretaus sandorio sąskaitų tarifus galima keisti, jei atlikti pakeitimai atitinka sandorio pobūdį. 

- Toliau aprašytas užsakymas naudojamas siekiant pašalinti išlaidų kainoraščio konfliktą.

    1. Išlaidų kainoraštis, susietas su organizacijos vienetu.
    2. Išlaidų kainoraštis, susietas su „Project Service“ parametrais. Kadangi su „Project Service“ parametrais galima susieti išlaidų kainoraščius keliomis skirtingomis valiutomis, PSA pritaiko sutartį dėl projekto, sutarties ar pasiūlymo pasirašiusios organizacijos vieneto valiutą pagal išlaidų kainoraščio valiutą.
    3. Išlaidų kainoraščiams netaikomi kainodaros pagal savikainą ir savikainos antkainio metodai. Net jei šie kainodaros metodai naudojami išlaidų kainoraščio eilutėse siekiant nustatyti operacijų kategorijų išlaidas, sistema juos ignoruoja ir neįveda jokių numatytųjų savikainų.


[!INCLUDE[footer-include](../includes/footer-banner.md)]