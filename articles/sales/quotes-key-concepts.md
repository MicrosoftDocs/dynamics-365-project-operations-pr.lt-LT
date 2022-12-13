---
title: Unikalios sąvokos projektu pagrįstiems pasiūlymams
description: Šiame straipsnyje pateikiama informacija apie projektų pasiūlymus "Microsoft" Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824338"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Unikalios sąvokos projektu pagrįstiems pasiūlymams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Prieš pradėdami naudoti projekto pasiūlymus "Microsoft", Dynamics 365 Project Operations turėtumėte žinoti šias pagrindines sąvokas.

## <a name="owning-company"></a>Valdančioji įmonė

Nuosavybės įmonė atstovauja juridiniam asmeniui, kuriam priklauso projekto pristatymas. Pasiūlyme nurodytas klientas turi būti galiojantis klientas tame "finance and operations" programų juridiniame subjekte. Turi sutapti valdančios įmonės valiuta ir sutarties vieneto valiuta, pasirinkta pagal projektu pagrįstą pasiūlymą.

## <a name="contracting-unit"></a>Sutartį sudarantis vienetas

Sutarties vienetas atstovauja padaliniui ar praktikai, kuriai priklauso projekto pristatymas. Galite nustatyti kiekvieno sutarties vieneto išteklių savikainą. Kai nurodote išteklių išlaidas sutarties vienete, galite nustatyti skirtingus išlaidų tarifus ištekliams, iš kurių sutarties vienetas skolinasi, arba kitiems įmonės padaliniams ar praktikai. Šios išlaidų normos vadinamos sandorių kainomis, išteklių skolinimusi arba valiutų kainomis. Kai nustatote išteklių skolinimosi iš kitų padalinių kainą, galite nustatyti išlaidų normas skolinimo skyriaus valiuta.

## <a name="cost-currency"></a>Savikainos valiuta

"Project Operations" savikainos valiuta yra valiuta, kuria išlaidos ataskaitos. Ši valiuta gaunama iš valiutos, kuri pridėta prie **pasiūlymo pasiūlymo, sutarties ir projekto lauko Sutarties vienetas** . Projekto išlaidos gali būti registruojamos bet kuria valiuta. Tačiau valiuta konvertuojama iš valiutos, kuria buvo įrašytos išlaidos, į projekto išlaidų valiutą.

Kadangi valiutų kursai Dataverse platformoje negali būti galiojantys pagal datą, ekrane rodomos bendros išlaidų sumos laikui bėgant gali keistis, jei atnaujinsite valiutos keitimo kursus. Tačiau į duomenų bazę įrašytos išlaidos lieka nepakitusios, nes sumos saugomos ta valiuta, kuria jos buvo patirtos.

## <a name="sales-currency"></a>Pardavimo valiuta

"Project Operations" pardavimo valiuta yra valiuta, kuria įrašomos ir rodomos apskaičiuotos ir faktinės pardavimo sumos. Tai taip pat valiuta, kuria klientui išrašoma sąskaita faktūra už sandorį. Projekto pasiūlyme numatytoji pardavimo valiuta nustatoma iš kliento arba kliento įrašo ir ją galima keisti sukūrus pasiūlymą. Tačiau įrašius pasiūlymą, pardavimo valiutos keisti negalima. Numatytieji produktų ir projektų kainoraščiai nustatomi pagal pasiūlymo pardavimo valiutą.

Skirtingai nuo išlaidų, pardavimo vertės gali būti įrašomos **tik** pardavimo valiuta.

## <a name="billing-method"></a>Atsiskaitymo metodas

Projektai paprastai turi fiksuoto mokesčio ir vartojimo pagrindu sudarytus sutarčių sudarymo modelius. Programoje "Project Operations" projekto sutarčių sudarymo modelis pateikiamas atsiskaitymo metodu. Atsiskaitymo metodas turi dvi vertes: laiką ir medžiagą bei fiksuotą kainą.

- **Laikas ir medžiaga**  – vartojimu pagrįstas sutarčių sudarymo modelis, kai kiekviena patirta kaina yra pagrįsta atitinkamomis pajamomis. Kai numatote arba patiriate daugiau išlaidų, atitinkami numatyti ir faktiniai pardavimai taip pat bus padidinti. Galite nurodyti neviršyti pasiūlymo eilučių, turinčių šį atsiskaitymo būdą, limitų. Tokiu būdu galite apriboti faktines pajamas. Apskaičiuotoms pajamoms neturi įtakos ribos, kurių negalima viršyti.
- **Fiksuota kaina** - Fiksuoto mokesčio sutarčių sudarymo modelis, kai pardavimo vertės nepriklauso nuo patirtų išlaidų. Pardavimo reikšmė yra fiksuota ir ji nekinta, kai numatote arba patiriate daugiau išlaidų.

## <a name="project-price-lists"></a>Projekto kainoraščiai

Projekto kainoraščiai yra kainoraščiai, naudojami norint įvesti laiko, išlaidų ir kitų su projektu susijusių komponentų numatytąsias kainas, o ne išlaidų tarifus. Gali būti keletas kainoraščių, o kiekvienas sąrašas gali galioti pagal datą kiekvienam projekto pasiūlymui. "Project Operations" nepalaiko projekto kainoraščių datų persidengimo.

## <a name="product-price-lists"></a>Produkto kainoraščiai

Produktų kainoraščiai yra kainoraščiai, naudojami norint įvesti pasiūlymo produktų eilučių numatytąsias kainas, o ne išlaidų tarifus. Yra tik vienas produkto kainoraštis vienai citatai.

## <a name="transaction-classes"></a>Operacijos klasės

„Project Operations“ palaiko keturis operacijų klasių tipus:

- Laikas
- Išlaidos
- Medžiaga
- Rinkliava

Savikainos ir pardavimo vertės gali būti įvertintos ir patirtos **laiko**, išlaidų **ir** medžiagų **operacijų klasėse** . **Mokestis** yra tik pajamų operacijų klasė.

## <a name="work-entities-and-billing-entities"></a>Darbo objektai ir atsiskaitymo objektai

Projektai ir užduotys yra objektai, atspindintys darbą. Pasiūlymo eilutės ir Sutarties eilutės yra objektai, nurodantys atsiskaitymą. Galite susieti skirtingus darbo objektus su atsiskaitymo parinktimis, susiedami juos su pasiūlymo eilutėmis arba sutarties eilutėmis.

## <a name="multi-customer-deals"></a>Kelių klientų sandoriai

Pasiūlymai keliems klientams sudaromi, kai vienoje sąskaitoje faktūroje yra daugiau nei vienas klientas. Štai keletas tipiškų pavyzdžių:

- **Originalios įrangos gamintojų (OĮG) įmonės ir jų partneriai** – Partneriai ir perpardavėjai parduoda produktą, kuris apima pridėtinės vertės paslaugas. Sandorio su klientu metu OEM paprastai siūlo finansuoti dalį projekto.
- **Viešojo sektoriaus projektai** - Keli savivaldybės departamentai sutinka finansuoti projektą ir jiems sąskaitos faktūros išrašomos pagal anksčiau sutartą padalijimą. Pavyzdžiui, mokyklos skyrius ir miesto arba vietos valstybinės institucijos departamentas susitaria finansuoti baseino pastatą.

## <a name="invoice-schedules"></a>Sąskaitos faktūros grafikai

Sąskaitų faktūrų tvarkaraščiai yra būdingi kiekvienai pasiūlymo eilutei ir yra pasirinktiniai. Sąskaitų faktūrų tvarkaraščiai kuriami pagal konkrečias pradžios ir pabaigos datas bei sąskaitų faktūrų dažnumą. Jie naudojami sutarties etape, kai sukonfigūruojamas automatinis sąskaitų faktūrų kūrimo procesas. Pasiūlymo etape sąskaitų faktūrų tvarkaraščiai yra neprivalomi. Jei jie sukuriami pasiūlymo etape, jie nukopijuojami į projekto sutartį, kuri sukuriama laimėjus projekto pasiūlymą.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Skirtumai nuo "Dynamics 365 Sales" pasiūlymų

"Project Operations" pasiūlymai sukurti naudojant "Dynamics 365 Sales" pasiūlymus. Tačiau yra keletas svarbių funkcijų skirtumų, kuriuos turėtumėte žinoti:

- "Project Operations" pasiūlymuose yra dviejų skirtingų tipų eilutės: viena skirta projektams, kita – produktams.
- "Project Operations" pasiūlymai turi savo puslapio ir vartotojo sąsajos (UI) elementus, verslo taisykles, verslo logiką papildiniuose ir kliento scenarijus, dėl kurių jie skiriasi nuo pardavimo pasiūlymų.
- Dalyje "Sales" prie vieno pardavimo pasiūlymo galite pridėti kelis užsakymus. Programoje "Project Operations" prie projekto pasiūlymo galite pridėti tik vieną projekto sutartį.
- Kai laimite pardavimo pasiūlymą, susijusi galimybė gali likti atvira. Laimėjus projekto pasiūlymą, susijusi galimybė uždaroma.
- Pardavimo pasiūlyme nėra kai kurių laukų ir sąvokų, kurios įtraukiamos į projekto pasiūlymą. Šie laukai yra **Sutartį pasirašantis vienetas**, **Klientų vadybininkas** ir **Sąskaitų gavėjo kontakto vardas**.
- Pardavimo pasiūlymai ir projekto pasiūlymai identifikuojami pagal lauką parinkčių rinkinys pagrįstas **tipas** . Pardavimo pasiūlymo šio lauko reikšmė yra **Pagrįsta** elementu. Projekto pasiūlymo reikšmė yra **Pagrįsta** darbu.

Dėl šių skirtumų nerekomenduojame naudoti pardavimo pasiūlymų ir "Project Operations" pasiūlymų pakaitomis.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
