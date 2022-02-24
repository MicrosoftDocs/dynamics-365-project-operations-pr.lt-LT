---
title: Automatinio sąskaitų faktūrų kūrimo konfigūravimas – „Lite“ versija
description: Šioje temoje pateikta informacija, kaip konfigūruoti automatinį išankstinių sąskaitų faktūrų kūrimą.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ce9cb9090c44762f370bf8d574d179077b6a821
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176576"
---
# <a name="configure-automatic-invoice-creation---lite"></a>Automatinio sąskaitų faktūrų kūrimo konfigūravimas – „Lite“ versija
 
_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Galite konfigūruoti automatinį sąskaitų faktūrų kūrimą naudodami „Dynamics 365 Project Operations“. Sistema sukuria išankstinės sąskaitos faktūros juodraštį pagal kiekvienos projekto sutarties ir sutarties eilutės sąskaitos faktūros grafiką. Sąskaitų faktūrų grafikai konfigūruojami sutarties eilutės lygyje. Kiekvienoje sutarties eilutėje gali būti atskiras sąskaitų faktūrų grafikas arba tą patį sąskaitos faktūros grafiką galima nurodyti kiekvienoje sutarties eilutėje.

Sukūrus sąskaitą faktūrą, sistema visada sukuria bent vieną sąskaitą faktūrą vienai projekto sutarčiai. Kai kuriais atvejais gali būti sukurtos kelios sąskaitos faktūros.

Pavyzdžiui, jei sutartyje yra keli klientai, bus sukurta tiek sąskaitų faktūrų, kiek yra klientų, kurie turi apmokėtinų operacijų tame projekte.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Supraskite, kaip sąskaitoje faktūroje įtraukiamos operacijos 

Kartais kiekviena projektais pagrįstos sutarties eilutė nurodo atskirą sąskaitos faktūros grafiką. Pavyzdžiui, „Adatum“ sutarties diegimo paslaugos yra tokios sutarties eilutės.

- Prototipas, kuris yra fiksuota kaina su dviem neautomatiškai sukurtais etapais.
- Diegimo užduotis, kuri apima laiką ir bus išrašyta du kartus per savaitę pirmadieniais.
- Patirtos išlaidos, kurias reikia apskaityti kas mėnesį kiekvieną mėnesio pirmą pirmadienį.

Kiekvieno iš šių dviejų eilučių elementuose nustatytas sąskaitų faktūrų grafikas panašus į šią lentelę.

| Sutarties eilutė | Sąskaitos faktūros vykdymo data | Operacijos nutraukimo data | Etapo data | Etapo suma |
| --- | --- | --- | --- | --- |
| Prototipas | Pirmadienis, spalio 5 d. | - | Pirmadienis, spalio 5 d. | 5000 USD |
| - | Antradienis, lapkričio 3 d. | - | Antradienis, lapkričio 3 d. | 12,000 USD |
| Diegimas | Pirmadienis, spalio 5 d. | Sekmadienis, spalio 4 d. | - | - |
| - | Pirmadienis, spalio 19 d. | Sekmadienis, spalio 18 d. | - | - |
| - | Pirmadienis, lapkričio 2 d. | Sekmadienis, lapkričio 1 d. | - | - |
| - | Pirmadienis, lapkričio 16 d. | Sekmadienis, lapkričio 15 d. | - | - |
| Patirtos išlaidos | Pirmadienis, spalio 5 d. | Sekmadienis, spalio 4 d. | - | - |
| - | Pirmadienis, lapkričio 2 d. | Sekmadienis, lapkričio 1 d. | - | - |

Šiame pavyzdyje, kai sąskaitos faktūros automatiškai išrašomos

- **Spalio 4 d. arba bet kurią datą prieš tai**: šiai sutarčiai sugeneruojama sąskaita faktūra, nes kiekvienos sutarties eilutės lentelė **Sąskaitų faktūrų tvarkaraštis** neiškviečia spalio 4 d., sekmadienio, kaip sąskaitos faktūros vykdymo datos.
- **Antradienis, spalio 5 d.**: viena sąskaita faktūra sugeneruojama:

    - Prototipas, apimantis etapą, jei pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą**.
    - Diegimas, apimantis visas laiko operacijas, sukurtas prieš operacijų pabaigos datą spalio 4 d., sekmadienį, pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą**.
    - Patirtos išlaidos, apimančios visas išlaidų operacijas, sukurtas prieš operacijų pabaigos datą spalio 4 d., sekmadienį, pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą**.
  
- **Spalio 6 d. arba bet kurią datą prieš spalio 19 d.**: šiai sutarčiai sugeneruojama sąskaita faktūra, nes kiekvienos sutarties eilutės lentelė **Sąskaitų faktūrų tvarkaraštis** neiškviečia spalio 6 d. ar bet kurios kitos datos prieš spalio 19 d. kaip sąskaitos faktūros vykdymo datos.
- **Pirmadienis, spalio 19 d.**: viena sąskaita faktūra sugeneruojama diegimui, kuris apima visas laiko operacijas, sukurtas prieš operacijų pabaigos datą spalio 18 d., sekmadienį, pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą**.
- **Antradienis, lapkričio 2 d.**: viena sąskaita faktūra sugeneruojama:

    - Diegimas, apimantis visas laiko operacijas, sukurtas prieš operacijų pabaigos datą lapkričio 1 d., sekmadienį, pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą**.
    - Patirtos išlaidos, apimančios visas išlaidų operacijas, sukurtas prieš operacijų pabaigos datą lapkričio 1 d., sekmadienį, pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą**.

- **Antradienis, lapkričio 3 d.**: viena sąskaita faktūra sugeneruojama prototipui, kuris apima 12 000 USD etapą, jei pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą**.

## <a name="configure-automatic-invoicing"></a>Automatinio sąskaitų faktūrų išrašymo konfigūravimas

Norėdami konfigūruoti automatinį sąskaitos faktūros vykdymą, atlikite šiuos veiksmus.

1. **Project Operations** pasirinkite **Parametrai** > **Pasikartojančių sąskaitų faktūrų sąranka**.
2. Sukurkite paketinę užduotį ir pavadinkite ją **„Project Operations“ sąskaitų faktūrų kūrimas**. Paketinės užduoties pavadinime turi būti terminas „Kurti sąskaitas faktūras“.
3. Lauke **Užduoties tipas** pasirinkite **Nėra**. Pagal numatytuosius nustatymus, laukai **Dažnumas: kasdien** ir **Aktyvus** nustatytos į **Taip**.
4. Pasirinkite **Vykdyti darbo eigą**. Dialogo lange **ieškoti įrašo** matysite tris darbo eigas:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Pasirinkite **ProcessRunCaller**, o tada pažymėkite **Įtraukti**.
6. Kitame dialogo lange pasirinkite **Gerai**. Po darbo eigos **Miego režimas** seka darbo eiga **Procesas**. 

> [!NOTE]
> Taip pat galite pasirinkti **ProcessRunner** 5 veiksme. Pažymėję **Gerai**, po darbo eigos **Procesas** seka darbo eiga **Miego režimas**.

Darbo eigos **ProcessRunCaller** ir **ProcessRunner** sukuria sąskaitas faktūras. **ProcessRunCaller** iškviečia **ProcessRunner**. **ProcessRunner** yra darbo eiga, kuri iš tikrųjų sukuria sąskaitas faktūras. Darbo eiga taikoma visoms sutarties eilutėms, kurioms reikia sukurti SF, ir sukuria tų eilučių sąskaitas faktūras. Norint nustatyti sutarties eilutes, kurioms reikia sukurti SF, užduotis atsižvelgia į projekto eilutėms skirtos sąskaitos faktūros vykdymo datas. Jei vienam projektui priklausančių projekto eilučių sąskaitos faktūros buvo vykdytos tuo pačiu metu, operacijos įtraukiamos į vieną sąskaitą faktūrą, kurioje yra dvi sąskaitos faktūros eilutės. Jei nėra operacijų, skirtų išrašyti sąskaitas faktūras, užduotis nesukuria sąskaitos faktūros.

Kai **ProcessRunner** baigia vykdymą, iškviečiamas **ProcessRunCaller**, pateikiamas pabaigos laikas ir yra uždaromas. Tada **ProcessRunCaller** paleidžia laikmatį, kuris trunka 24 valandas nuo nurodyto pabaigos laiko. Baigiantis laikmačio laikui, **ProcessRunCaller** uždaromas.

Paketinė proceso užduotis, skirta sąskaitoms faktūroms kurti, yra pasikartojanti užduotis. Jei šis paketinis procesas vykdomas daug kartų, sukuriami keli užduoties egzemplioriai ir sukeliamos klaidos. Todėl paketinį procesą reikia pradėti tik vieną kartą, o jį paleisti iš naujo reikia tik tuo atveju, jei jis sustos.

> [!NOTE]
> „Project Operations“ paketinių sąskaitų faktūrų išrašymas vykdomas tik projekto sutarties eilutėse, sukonfigūruotose sąskaitų faktūrų grafike. Sutarties eilutė su fiksuotos kainos atsiskaitymų metodu turi turėti sukonfigūruotus etapus. Norint naudoti projekto sutarties eilutę su laiko ir medžiagų atsiskaitymo metodu, reikės nustatyti data pagrįstą sąskaitos faktūros grafiką.
