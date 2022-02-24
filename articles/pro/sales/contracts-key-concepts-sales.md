---
title: Projekto sutartys – pagrindinės sąvokos – „Lite“ versija
description: Šioje temoje pateikiama informacija apie pagrindines projekto sutarčių sąvokas.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75c4b90e47c0b90ed3fea8dce1533057aa6137b9
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663784"
---
# <a name="concepts-unique-to-project-contracts"></a>Unikalios projekto sutarčių sąvokos

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje pateikiamos pagrindinės sąvokos, kurias reikia žinoti prieš pradedant naudoti projektų sutartis programoje „Dynamics 365 Project Operations“:

## <a name="contracting-unit"></a>Sutartį sudarantis vienetas

Sutartį sudarantis vienetas yra padalinys arba praktika, kuriai priklauso projekto pristatymas. Galite nustatyti kiekvieno sutarties vieneto išteklių savikainą. Kai nurodote ištekliaus savikainą, taip pat galėsite nustatyti skirtingus išteklių savikainos tarifus. Šis sutartį sudarantis vienetas skolinasi šiuos išteklius iš kito įmonės padalinio arba praktikos. Išteklių savikainos tarifai yra pervedimų kainos, išteklių skolinimasis arba valiutų kainos. Nustatydami išteklių skolinimosi iš kitų padalinių savikainos tarifus, naudokite skolinimo padalinio valiutą.

## <a name="cost-currency"></a>Savikainos valiuta

Savikainos valiuta yra valiuta, kuria ekrane pateikiama savikaina. Ši valiuta gaunama iš valiutos, susietos su lauku **Sutartį sudarantis vienetas**, esančiu sutartyje ir projekte. Išlaidas galima registruoti bet kuria valiuta projekte. Tačiau tada nurodomas valiutos konvertavimas iš valiutos, kuria užregistruota savikaina, į projekto išlaidų valiutą, kai rodoma ekrane.

Kadangi „Common Data Service“ (CDS) platformos valiutų kursai nėra galiojantys pagal datą, todėl, jei atnaujinate valiutos keitimo kursus, ekrane savikainos sumos gali pasikeisti. Tačiau savikainos, įrašytos į duomenų bazę, lieka nepakitusios, nes sumos saugomos valiuta, kuria jos patirtos.

## <a name="sales-currency"></a>Pardavimo valiuta

Pardavimo valiuta, naudojama „Project Operations“, yra valiuta, kuria yra įrašytos ir rodomos apskaičiuotos bei faktinės pardavimo sumos. Pardavimo valiuta taip pat yra valiuta, kuria klientui išrašyta sąskaita faktūra už sandorį. Projekto sutartyje pardavimo valiuta gaunama iš kliento įrašo ir ją galima pakeisti, kai sukuriama sutartis. Kai sutartis sukuriama uždarant pasiūlymą kaip laimėtą, sutarties valiuta nustatoma pagal pasiūlymo valiutą.

Kai kuriate projekto sutartį nuo nulio, lauko **Pardavimo valiuta** redaguoti negalima. Produkto ir projekto kainoraščiai yra numatytieji sąrašai pagal šią sutarties valiutą.

Kitaip nei savikainos, pardavimo reikšmės gali būti įrašytos tik pardavimo valiuta.

## <a name="billing-method"></a>Atsiskaitymo metodas

Projektuose paprastai yra dviejų tipų sutarties sudarymo modeliai – pagrįsti fiksuotais mokesčiais ir suvartojimu. „Project Operations“ šie modeliai nurodomi kaip atsiskaitymo būdai su dviem galimomis reikšmėmis.

- Laikas ir Medžiaga: suvartojimu pagrįstas sutarties sudarymo modelis, kai kiekvienas patirtas išlaidas kompensuoja atitinkamos pajamos. Kai numatote arba patiriate daugiau išlaidų, atitinkami numatyti ir faktiniai pardavimai taip pat bus padidinti. Nurodykite neviršytinus limitus sutarties eilutėse, naudojančiose šį atsiskaitymo būdą, kuris panaikina faktinių pajamų viršutinę ribą. Numatytų pajamų ribos neviršijimo apribojimas įtakos neturi.
- Fiksuota kaina: fiksuoto mokesčio sutarties sudarymo modelis, nurodantis, kad pardavimo reikšmės bus nepriklausomos nuo patirtų išlaidų. Pardavimo reikšmė yra fiksuota ir ji nekinta, kai numatote arba patiriate daugiau išlaidų.

## <a name="project-price-lists"></a>Projekto kainoraščiai

Projekto kainoraščiai naudojami numatytajai kainai (ne išlaidų tarifams), laikui, išlaidoms ir kitiems su projektu susijusiems komponentams. Gali būti keletas kainoraščių. Kiekviename kainoraštyje nustatoma atskira kiekvienos projekto sutarties įsigaliojimo data. „Project Operations“ nepalaiko persidengiančių projekto kainoraščių galiojimo datų.

Kai projekto sutartis sukuriama laimėjus projekto pasiūlymą, projekto kainoraščiai nukopijuojami nurodant sutarties pavadinimą ir datą. Šios informacijos kopijavimas yra projekto komponentų pasirinktinė kainodara šioje projekto sutartyje.

## <a name="product-price-lists"></a>Produkto kainoraščiai

Produktų kainoraščiai naudojami numatytosioms kainoms (ne išlaidų tarifams) sutarties produktu pagrįstose eilutėse. Vienai sutarčiai skirtas tik vienas produktų kainoraštis.

## <a name="transaction-classes"></a>Operacijų klasės

„Project Operations“ palaiko keturis operacijų klasių tipus:

- Laikas
- Išlaidos
- Medžiaga
- Rinkliava

Išlaidų ir pardavimo reikšmės gali būti numatytos ir patirtos pagal laiko, išlaidų ir medžiagų operacijų klases. Mokestis yra tik pajamų operacijų klasė.

## <a name="work-entities-and-billing-entities"></a>Darbo objektai ir atsiskaitymo objektai

Objektai, nurodantys darbą, yra projektai ir užduotys. Objektai, kurie nurodo atsiskaitymą aspektus, yra sutarties eilutės. Galite susieti skirtingus darbo objektus su atsiskaitymo parinktimis, susiedami juos su sutarties eilutėmis.

## <a name="multi-customer-deals"></a>Kelių klientų sandoriai

Su kelių klientų sandoriais susiduriama, kai sandorį sudaro daugiau nei vienas sąskaitos faktūros klientas. Toliau pateikti tipiniai pavyzdžiai.

- „OEM Enterprises“ ir jos partneriai: partneriai ir pardavėjai parduoda produktą su tam tikromis pridėtinės vertės paslaugomis ir paprastai įtraukia konkretų pasiūlymą klientui. OEM siūlo finansuoti projekto dalį. 

- Viešojo sektoriaus projektai keli vietos valdžios institucijų skyriai sutaria finansuoti projektą ir į sąskaitą faktūrą įtraukiami pagal anksčiau suderintas dalis. Pavyzdžiui, mokyklos skyrius ir vietos valstybinė institucija susitaria finansuoti baseino pastatą.

## <a name="invoice-schedules"></a>Sąskaitos faktūros grafikai

Sąskaitos faktūros grafikai taikomi kiekvienai konkrečiai sutarties eilutei ir jie reikalingi išrašant automatines sąskaita faktūras. Sąskaitų faktūrų grafikai kuriami pagal tam tikras pradžios ir pabaigos datas bei sąskaitų faktūrų dažnumą. Grafikai naudojami sutarties etape, kai konfigūruojamas automatinis sąskaitos faktūros kūrimo procesas. Kai projekto sutartis sukuriama iš pasiūlymo, sąskaitos faktūros grafikas nukopijuojamas į projekto sutartį iš pasiūlymo.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>„Dynamics 365 Sales“ sutarties pakeitimai

„Project Operations“ sutartys kuriamos „Dynamics 365 Sales“ sutartyse. Tačiau yra keletas svarbių funkcijų skirtumų, kuriuos turėtumėte žinoti.

- „Project Operations“ sutartyse yra du skirtingi eilučių tipai, vienas skirtas projektams, o kitas – produktams.
- „Project Operations“ sutartys turi savus formos ir UI elementus, verslo taisykles, verslo logiką papildiniuose ir kliento scenarijus, kuriais jos ir skiriasi nuo „Sales“ sutarčių.

Dėl šių priežasčių „Sales“ sutarties ir projekto sutarties apkeisti vietomis negalima.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
