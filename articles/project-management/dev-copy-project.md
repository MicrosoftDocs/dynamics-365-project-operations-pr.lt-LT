---
title: Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą
description: Šioje temoje pateikta informacija apie tai, kaip kurti projektų šablonus naudojant pasirinktinį veiksmą Kopijuoti projektą.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080776"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ palaiko galimybę kopijuoti projektą ir atkurti bet kokius priskyrimus į bendruosius išteklius, nurodančius vaidmenį. Naudodami šią funkciją klientai gali kurti pagrindinių projektų šablonus.

Pasirinkus **Kopijuoti projektą** , tikslinio projekto būsena atnaujinama. Naudokite **būsenos tipą** , kad nustatytumėte, kada kopijavimo veiksmas yra baigtas. Pasirinkus **Kopijuoti projektą** taip pat projekto pradžios data atnaujinama į dabartinę pradžios datą, jei tikslinio projekto objekte neaptikta tikslinė data.

## <a name="copy-project-custom-action"></a>Pasirinktinis veiksmas Kopijuoti projektą 

### <a name="name"></a>Pavadinimas / vardas, pavardė 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Įvesties parametrai
Yra trys įvesties parametrai.

| Parametras          | Tipas   | Reikšmės                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** arba **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Objekto nuoroda | Šaltinio projektas |
| Tikslinis objektas             | Objekto nuoroda | Tikslinis projektas |


- **{"clearTeamsAndAssignments":true}** : numatytas „Project“, skirto žiniatinkliui, veikimas, bus pašalinti visi priskyrimai ir komandos nariai.
- **{"removeNamedResources":true}** : numatytasis „Project Operations“ veikimas, priskyrimai bus atkurti į bendruosius išteklius.

Daugiau informacijos apie veiksmus žr. [Žiniatinklio API veiksmai](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions).

## <a name="specify-fields-to-copy"></a>Kopijuotinų laukų nurodymas 
Kai veiksmas iškviečiamas, funkcija **Kopijuoti projektą** ieškos projekto rodinyje **Kopijuoti projekto stulpelius** ir nustatys, kuriuos laukus kopijuoti, kai projektas kopijuojamas.
