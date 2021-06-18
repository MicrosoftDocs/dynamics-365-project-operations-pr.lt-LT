---
title: Pasiūlymai – pagrindinės sąvokos – „Lite“ versija
description: Šioje temoje pateikta informacija apie „Project Operations“ projektų pasiūlymų naudojimą.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bd225bfea6e04839b57dfcc9436315fe1cd6a204
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994282"
---
# <a name="concepts-unique-to-project-quotes"></a>Unikalios projekto pasiūlymų sąvokos

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_


Toliau pateikiamos pagrindinės sąvokos, kurias reikia žinoti prieš pradedant naudoti projektų pasiūlymus programoje „Dynamics 365 Project Operations“:

## <a name="contracting-unit"></a>Sutartį sudarantis vienetas

Sutartį sudarantis vienetas yra padalinys arba praktika, kuriai priklauso projekto pristatymas. Galite nustatyti kiekvieno sutarties vieneto išteklių savikainą. Kai nurodysite ištekliaus išteklių savikainą sutarties vienete, taip pat turėsite galimybę nustatyti skirtingus išlaidų tarifus ištekliams, iš kurių šis sutartį sudarantis vienetas skolinasi arba kitą įmonės padalinį arba cechą. Tai yra pervedimų kainomis, išteklių skolinimasis arba valiutų kainos. Nustatydami išteklių skolinimosi iš kitų padalinių išlaidas taip pat galite nustatyti tas išlaidų normas skolinimo padalinio valiuta.

## <a name="cost-currency"></a>Savikainos valiuta

Išlaidų valiuta „Project Operations“ yra valiuta, kuria pateikiamos išlaidos. Ši valiuta gaunama iš valiutos, susietos su lauku **Sutartį sudarantis vienetas**, esančiu pasiūlyme, sutartyje ir projekte. Išlaidas galima registruoti bet kuria valiuta projekte. Tačiau tada nurodomas valiutos konvertavimas iš valiutos, kuria užregistruotos išlaidos, į projekto išlaidų valiutą.

Kadangi CDS platformos valiutų kursai nėra galiojantys pagal datą, todėl, jei atnaujinate valiutos keitimo kursus, išlaidų ekrane sumos gali pasikeisti. Tačiau išlaidos, įrašytos į duomenų bazę, lieka nepakitusios, nes sumos saugomos valiuta, kuria jos patirtos.

## <a name="sales-currency"></a>Pardavimo valiuta

Pardavimo valiuta, naudojama „Project Operations“, yra valiuta, kuria yra įrašytos ir rodomos apskaičiuotos bei faktinės pardavimo sumos. Tai taip pat valiuta, kuria klientui išrašyta sąskaita faktūra už sandorį. Projekto pasiūlyme pardavimo valiuta gaunama iš kliento įrašo ir ją galima pakeisti, kai sukuriamas pasiūlymas. Po pasiūlymo įrašymo pardavimo valiutos pakeisti negalima. Produkto ir projekto kainų sąrašai yra numatytieji sąrašai pagal pasiūlymo pardavimo valiutą.

Kitaip nei išlaidos, pardavimo reikšmės gali būti įrašytos tik pardavimo valiuta.

## <a name="billing-method"></a>Atsiskaitymo metodas

Projektuose paprastai yra fiksuotais mokesčiais ir suvartojimu pagrįsti sutarčių modeliai. „Project Operations“ tai atitinka **Atsiskaitymo metodas** ir turi dvi reikšmes: laiką ir medžiagą bei fiksuotą kainą.

- **Laikas ir medžiaga** tai yra suvartojimu pagrįstas sutarties modelis, kai kiekvienas patirtas išlaidas kompensuoja atitinkamos pajamos. Kai numatote arba patiriate daugiau išlaidų, atitinkami numatyti ir faktiniai pardavimai taip pat bus padidinti. Galite nurodyti neviršyti pasiūlymo eilučių, turinčių šį atsiskaitymo būdą, limitų. Taip panaikinsite faktinių pajamų viršutinę ribą. Numatytų pajamų ribos neviršijimo apribojimas įtakos neturi.
- **Fiksuota kaina** tai fiksuoto mokesčio sutarties modelis, nurodantis, kad pardavimo reikšmės bus nepriklausomos nuo patirtų išlaidų. Pardavimo reikšmė yra fiksuota ir ji nekinta, kai numatote arba patiriate daugiau išlaidų.

## <a name="project-price-lists"></a>Projekto kainoraščiai

Projektų kainoraščiai yra kainoraščiai, naudojami numatytajai kainai (ne išlaidų tarifams), laikui, išlaidoms ir kitiems su projektu susijusiems komponentams. Gali būti keletas kainoraščių, o kiekvienas sąrašas gali galioti pagal datą kiekvienam projekto pasiūlymui. „Project Operations“ nepalaiko persidengiančių projekto kainoraščių galiojimo datų.

## <a name="product-price-lists"></a>Produkto kainoraščiai

Produktų kainoraščiai yra kainoraščiai, naudojami numatytosioms kainoms (ne išlaidų tarifams) pasiūlymo produktu pagrįstose eilutėse. Vienam pasiūlymui skirtas tik vienas produktų kainoraštis.

## <a name="transaction-classes"></a>Operacijos klasės

„Project Operations“ palaiko keturis operacijų klasių tipus:

- Laikas
- Išlaidos
- Medžiaga
- Rinkliava

Išlaidų ir pardavimo reikšmės gali būti numatytos ir patirtos pagal laiko, išlaidų ir medžiagų operacijų klases. Mokestis yra tik pajamų operacijų klasė.

## <a name="work-entities-and-billing-entities"></a>Darbo objektai ir atsiskaitymo objektai

Objektai, nurodantys darbą, yra projektai ir užduotys. Objektai, kurie nurodo atsiskaitymą, yra pasiūlymo eilutės ir sutarties eilutės. Galite susieti skirtingus darbo objektus su atsiskaitymo parinktimis, susiedami juos su pasiūlymo arba sutarties eilutėmis.

## <a name="multi-customer-deals"></a>Kelių klientų sandoriai

Su kelių klientų sandoriais susiduriama, kai yra daugiau nei vienas sąskaitos faktūros klientas. Įprasti pavyzdžiai gali būti:

- **OĮG įmonės ir jų partneriai** partneriai ir pardavėjai, parduodantys produktą su pridėtinės vertės paslaugomis. Paprastai tai būna scenarijus, kai per tam tikrą sandorį su klientu OĮG siūlo finansuoti projekto dalį. 

- **Viešojo sektoriaus projektai** keli vietos valdžios institucijų skyriai sutaria finansuoti projektą ir į sąskaitą faktūrą įtraukiami pagal anksčiau suderintas dalis. Pavyzdžiui, mokyklos skyrius ir miesto arba vietos valstybinės institucijos departamentas susitaria finansuoti baseino pastatą.

## <a name="invoice-schedules"></a>Sąskaitos faktūros grafikai

Sąskaitos faktūros grafikas būdingas kiekvienai pasiūlymo eilutei ir yra pasirinktinis. Sąskaitų faktūrų grafikai kuriami pagal tam tikras pradžios ir pabaigos datas bei sąskaitų faktūrų dažnumą. Sąskaitų faktūrų grafikai naudojami sutarties etape, kai konfigūruojamas automatinis sąskaitos faktūros kūrimo procesas. Pasiūlymo etape grafikai yra pasirinktiniai. Kai etape **Pasiūlymas** sukuriami sąskaitų faktūrų grafikai, jie nukopijuojami į projekto sutartį, sukurtą laimėjus projekto pasiūlymą.

## <a name="changes-from-dynamics-365-sales-quote"></a>Pasikeitimai iš „Dynamics 365 Sales“ pasiūlymo:

„Project Operations“ pasiūlymai kuriami „Dynamics 365 Sales“ pasiūlymuose. Tačiau yra keletas svarbių funkcijų skirtumų, kuriuos turėtumėte žinoti:

- Veiksmai **Peržiūrėti** ir **Aktyvinti**.
- „Project Operations“ pasiūlymuose yra dviejų skirtingų tipų eilutės. Viena yra projektams, o kita – produktams.
- „Project Operations“ pasiūlymai turi savus formos ir UI elementus, verslo taisykles, verslo logiką papildiniuose ir kliento scenarijus, kuriais jie ir skiriasi nuo „Sales“ pasiūlymų.

Dėl šių priežasčių nerekomenduojama naudoti „Sales“ pasiūlymo ir „Project Operations“ pasiūlymų keičiant juos vietomis.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
