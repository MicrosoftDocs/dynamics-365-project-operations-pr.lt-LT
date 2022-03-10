---
title: „Project Service Automation“ integravimo parametrai
description: Šioje temoje paaiškinama, kaip konfigūruoti numatytųjų duomenų įvedimą, kai integruojate „Microsoft Dynamics 365 for Project Service Automation“ į „Microsoft Dynamics 365 Finance“.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b58f34cb74be531a98518100158f39d74f136afc34444468d666cd4e9394af6f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005851"
---
# <a name="project-service-automation-integration-parameters"></a>„Project Service Automation“ integravimo parametrai

[!include[banner](../includes/banner.md)]

Puslapyje **„Project Service Automation“ integravimo parametrai** galite konfigūruoti, kaip numatytieji duomenys įvedami, kai integruojate „Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“. Norėdami, kad projektai būtų sėkmingai sinchronizuojami iš „Project Service Automation“ į „Finance“, turite nustatyti toliau pateikiamus laukus.

Norėdami atidaryti puslapį **„Project Service Automation“ integravimo parametrai**, eikite į **Projektų valdymas ir apskaita** \> **Sąranka** \> **„Dynamics 365 for Project Service Automation“ integravimo parametrai**. 

> [!NOTE]
> - Projekto užduočių integravimas, išlaidų operacijų kategorijos, valandų įvertinimas, išlaidų įvertinimas ir funkcijų blokavimas prieinami 8.0 versijoje.
> - Faktinių duomenų integravimas galimas 8.0.1 ir naujesnėse versijoje.


| Tab                    | Laukas                | Aprašo |
|------------------------|----------------------|-------------|
| Bendrasis                | Numatytasis projekto tipas | Pasirinkite numatytąjį projekto tipą. Kai projektai sinchronizuojami iš „Project Service Automation“, ši reikšmė naudojama, jei integravimo šablone nepateikėte numatytosios reikšmės. Sinchronizuojant, naujų projektų lauke **Projekto tipas** nustatoma ši reikšmė. Tačiau reikšmė gali būti atnaujinama, kai projekto sutarties eilutės sinchronizuojamos iš „Project Service Automation“. |
|                        | Laiko kategorija        | Pasirinkite numatytąją laiko kategoriją. Ši reikšmė naudojama, kai valandų įvertinimai sinchronizuojami iš „Project Service Automation“. Kai valandų įvertinimai ir valandų faktiniai duomenys sinchronizuojami iš „Project Service Automation“, „Finance“ naujų projektų valandų prognozių lauke **Kategorija** nustatoma ši reikšmė. |
|                        | Mokesčių kategorija         | Pasirinkite numatytąją mokesčių kategoriją. Ši reikšmė naudojama, kai mokesčių faktiniai duomenys sinchronizuojami iš „Project Service Automation“. Kai mokesčių faktiniai duomenys sinchronizuojami iš „Project Service Automation“, „Finance“ naujų mokesčių operacijų lauke **Kategorija** nustatoma ši reikšmė. |
| Projektų grupės numatytosios reikšmės | Projekto tipas         | Spustelėkite **Nauja**, jei norite įtraukti eilutę, kurioje galite pasirinkti projekto tipą ir nustatyti numatytąją projektų grupę. Konfigūruojant, konkretų projekto tipą galima pasirinkti tik vieną kartą. |
|                        | Projektų grupė        | Pažymėkite pasirinkto projekto tipo numatytąją projektų grupę. Kai nauji projektai sinchronizuojami iš „Project Service Automation“, lauke **Projekto grupė** nustatoma numatytoji projekto tipo reikšmė, jei integravimo šablone nepateikėte numatytosios reikšmės. |
| Atsiskaitymo tipo numatytosios reikšmės  | Atsiskaitymo tipas         | Spustelėkite **Nauja**, jei norite įtraukti eilutę, kurioje galite pasirinkti atsiskaitymo tipą ir nustatyti numatytąją eilutės ypatybę. Konfigūruojant, konkretų atsiskaitymo tipą galima pasirinkti tik vieną kartą. |
|                        | Eilutės ypatybė        | Pažymėkite pasirinkto atsiskaitymo tipo numatytąją eilutės ypatybę. Kai nauji valandų įvertinimai, nauji išlaidų įvertinimai arba nauji faktiniai duomenys sinchronizuojami iš „Project Service Automation“, lauke **Eilutės ypatybė** nustatoma numatytoji atsiskaitymo tipo reikšmė. |
| Funkcijų blokavimas  | Netaikoma       | Pažymėkite funkcijas, kurias norite išjungti „Finance“ projektuose ir sutartyse, kilusiuose iš „Project Service Automation“. Pavyzdžiui, galite išjungti galimybę redaguoti sutartis ir projektus, kurti darbo paskirstymo struktūras ir įvesti laiko grafikus naudojant „Finance“. Su apskaita susiję laukai liks įjungti, net jei jie taptų nepasiekiami dėl nustatyto parametro. Pagal numatytuosius nustatymus įjungtos visos funkcijos. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]