---
title: 2022 m. vasario mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacijos apie kokybinius naujinimus, pasiekiamus 2022 m. vasario mėn. „Project Operations”, skirtos ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, leidime.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932996"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 m. vasario mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

*Taikoma: „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams*

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.28.0.120 versijos „Dataverse“ aplinkoje
- Projektų valdymas ir apskaita „Dynamics 365 Finance“ aplinkos 10.0.24 versijoje

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

- Šiame leidime į vieną projektą galite įtraukti iki 300 komandos narių. Anksčiau komandos narių skaičiaus apribojimas buvo 150. Daugiau informacijos ieškokite skyriuje [Projekto apribojimai](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Toliau pateiktame sąraše parodytos dvigubo rašymo schemos, modifikuotos arba įtrauktos „Project Operations“ 2022 m. vassario mėn. leidime.

| Objekto schema | Atnaujinta versija | Komentarai |
| --- | --- | --- |
| „Project Operations“ integravimo projekto išlaidų eksportavimo objektas (msdyn\_expenses) | 1.0.0.3 | Išplėstinis projekto veiklos sinchronizavimui su Dataverse. |

Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų siuntimas ir kainodara | 2415109 | Numatytoji reikšmė lauke Operacijos **mokėjimo sąlygos** turi būti projekto sutarties kliento įrašas ir formos sąskaitos faktūros įrašas. |
| Sąskaitų siuntimas ir kainodara | 2497369 | Pataisos parametrai turi atitikti **datos** reikšmę. |
| Sąskaitų siuntimas ir kainodara | 2498697 | Patobulintos laiko įvesties išsamūs **saugos konfigūracijos parametrai**. |
| Sąskaitų siuntimas ir kainodara | 2513824 | Išteklių pagrįstų scenarijų operacijų kategorijos ID neturi būti didesnis nei 28 simbolių "Project Operations". |
| Sąskaitų siuntimas ir kainodara | 2517455 | Atnaujinti **sąskaitos faktūros eilutės operacijų veiksmo** negalima paleisti kelis tos pačios sąskaitos faktūros kartus. |
| Sąskaitų siuntimas ir kainodara | 2517465 | Sąskaitos **faktūros eilutės išsamios informacijos išjungimo** veiksmas yra užblokuotas, nes jis nepalaikomas. |
| Sąskaitų siuntimas ir kainodara | 2556660 | Fiksuota datos poveikio kontrolė, atlikta kainotrašte, pridėtame prie projekto parametrų įrašo. |
|  Galimybių valdymas | 2369202 | Ištaisyti verslo logiką, kuri tikrina, kad kainoraščius, kurie turi persidengiančias poveikio datas, galima pridėti prie tos pačios projekto sutarties. |
|  Galimybių valdymas | 2385965 | Kai pasirenkate Įrašyti ir **uždaryti** projekto sutarties puslapio **skirtuke** Klientai **taisė elgseną**. |
| Laikas ir išlaidos | 2538503 | Projekto užduotis turi būti prieinama projekto faktinių **duomenų objektui** užregistrus išlaidų ataskaitą. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektų valdymas ir apskaita „Dynamics 365 Finance” programos aplinkose

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Importuojant tiekėjo kredito pastabas įvyksta klaida. Klaidos pranešime nurodyta, kad "Neišsilaikoma suma negali būti didesnė nei likusi neto suma". |
| Projektų valdymas ir apskaita | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Jei į sąskaitą faktūrą įtraukta nulinės sumos mokesčio operacijų, kurios yra neišrašomos pardavimo faktinės vertės, sąskaitų faktūrų išrašyti negalima. |
| Projektų valdymas ir apskaita | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Atnaujinus pirkimo kainą ir įjungus aktyvinti pakeitimų valdymą, užregistruotos **išlaidos nėra** teisingos.|
| Projektų valdymas ir apskaita | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Fiksuotos kainos projekto registravimo sąmatoje naudojama netinkama valiuta ir suma, naudojama sąmatų išsamūs duomenys, **net** įgalinus projekto sutarties valiutą įvertinimo skaičiavimo funkcijai. |
| Projektų valdymas ir apskaita | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **"ProjDMFDataPopulation\_" plėtinys** neturėtų paskambinti, kad galėtų įjungti keitimų sekimą negaudami objektų, kurių konfigūracijos klavišai neįjungti, išsaugant išimtis. |
| Projektų valdymas ir apskaita | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Paketo užduotis yra fiksuota, kai užregistruojami keli išplėstiniai žurnalai ir įvyksta klaida. |
| Kelionės ir išlaidos | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Dėl atsiskaitymo problemos, susijusios su išlaidų ataskaitų advances pinigais, mokesčių suma nėra apdrausta kaip advance pinigais dalis. |
| Kelionės ir išlaidos | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Į išlaidų – užregistruotų operacijų ataskaitą neįtraukiama **pardavimo mokesčių** informacija. |
| Kelionės ir išlaidos | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Pajamos **kurių reikia išlaidų** strategijai, netinkamai rodo įspėjimą apie išlaidų ataskaitas. |
| Kelionės ir išlaidos | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Į projekto operaciją nepastemami pardavimo mokestis nėra įtraukiamas į bendrą pardavimo sumą, kai operacija atsiranda dėl išlaidų. |
| Kelionės ir išlaidos | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Kai elementas yra eilutėje yra mokesčių, negalite pakeisti išklaidavimo eilutės datos ir įvyksta šaltinio dokumento būsenos klaida. |

## <a name="removed-and-deprecated-features"></a>Pašalintos ir nerekomenduojamos funkcijos

Straipsnyje ["Project Operations" pašalintos arba nebenaudojamos](removed-depreciated-features-project.md) funkcijos aprašomos funkcijos, kurios buvo pašalintos arba nebenaudojamos Dynamics 365 Project Operations.

- Pašalinta funkcija nebepasiekiama naudojantis šiuo produktu.
- Nerekomenduojama funkcija nėra aktyviai programuojama ir gali būti pašalinta būsimuose atnaujinimuose.

Nebenaudojamas skelbimas bus rodomas ["Project Operations](removed-depreciated-features-project.md) " straipsnyje, po 12 mėnesių iki funkcijos išėmimo iš produkto, iš jo bus rodomas nebenaudojamas arba nebenaudojamas funkcijas.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, šie pakeitimai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.
