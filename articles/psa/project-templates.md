---
title: Projekto šablonai
description: Šioje temoje pateikta informacija apie tai, kaip naudoti projektų šablonus, skirtus greitam projektų nustatymui.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: db42c9ea7280274cdc9cc90f1487f27e08f892e5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148068"
---
# <a name="project-templates"></a>Projekto šablonai 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekto šablonas yra iš anksto nustatyta sistema, padedanti greitai ir paprastai pradėti projektą. Galite naudoti iš anksto nustatytą šabloną ir sukurti naują projektą vienu spustelėjimu. Kalbant apie projektus, turite apibrėžti būtinąsias projektų šablonų sąlygas. Turite apibrėžti kiekvieno projekto šablono projekto kalendorių, o vaidmenis ir kainoraščius reikia iš anksto nustatyti organizacijoje, kad šablono komponentuose būtų naudingų duomenų.

Projekto šabloną sudaro trys komponentai: grafikas, projektų sąmatos ir projekto komandos nariai.

## <a name="schedule"></a>Tvarkaraštis

Projekto šablono grafikas turi tą patį elementų rinkinį kaip ir projekto grafikas. Galite kurti užduočių hierarchiją, susieti vaidmenis su užduotimis, nustatyti grafiko atributus, nustatyti priklausomybes. Projekto šablono grafikas taip pat palaiko užduočių režimus kiekvienai užduočiai. Todėl jis palaiko planavimo modulį. Projekto kalendorių turite susieti su projektu. Kuriant darbo grafiką, skirtumų tarp projekto šablono ir projekto nėra.

## <a name="project-estimates"></a>Projekto įvertinimai

Projekto sąmatos projekto šablone veikia taip pat kaip projekto sąmatos projekte. Tačiau savikaina ir pardavimo kainos yra gaunamos iš numatytųjų savikainos ir pardavimo kainoraščių, apibrėžtų parametruose.

## <a name="creating-a-project-from-a-template"></a>Projekto kūrimas pagal šabloną
 
Yra keli būdai kurti projektą iš projekto šablono:

- Kurdami projektą pagal pasiūlymą, projekto šabloną galite pasirinkti dialogo lange **Spartusis kūrimas: Projektas**.

> ![Dialogo langas „Spartusis kūrimas: Projektas“](media/project-11.png)

- Kai kuriate projektą pasirinkdami **Naujas projektas**, puslapis **Projektas** bus rodomas prieš įrašant įrašą. Lauke **išrinkti šabloną** pasirinkite vieną iš anksto nustatytų projekto šablonų organizacijoje.
- Naudokite **Kurti projektą pagal šabloną** puslapyje **Šablono objektas**.

## <a name="copying-components-of-template-to-project"></a>Šablono komponentų kopijavimas į projektą

Kai į projektą kopijuojate projekto šablono komponentus, gali atsirasti kelių perrašymų, atsižvelgiant į projekto parametrus.

### <a name="copying-the-schedule"></a>Grafiko kopijavimas

Kai kopijuojate grafiką iš projekto šablono, jei projekte nurodytas kitas projekto kalendorius nei šablone, projekto kalendoriaus darbo valandos taikomos užduočių grafikui. Tokiu būdu grafikas yra pakoreguojamas pagal atsarginį projekto kalendorių. Panašiai pirmoji užduotis grafike perima projekto pradžios datą, todėl likusios užduočių hierarchijos grafikas yra atnaujinamas pagal trukmę ir priklausomybes, nurodytas šablone. 

### <a name="copying-project-estimates"></a>Projekto įvertinimų kopijavimas 

Kai kopijuojate projekto įvertinimo eilutes, kainoraščiai naujinami. Kalbant apie savikainos kainoraštį, šie naujinimai priklauso nuo projektą valdančio vieneto. O kalbant apie pardavimo kainoraštį, jie priklauso nuo kliento. Galiausiai, kalbant apie projektus, susietus su pardavimo objektu, vieneto savikaina ir pardavimo kainomis, jie nustatomi pagal minėtus kainoraščius.

### <a name="copying-a-project-team"></a>Projekto komandos kopijavimas

Kopijuojant projekto komandą iš šablono į projektą, nukopijuojami bendrieji ištekliai bei jos įgūdžiai ir kvalifikacija, nurodyti šablone. Bendrųjų išteklių priskyrimai taip pat tvarkomi kaip ir projekto šablone. Įvardyti ištekliai nepalaikomi projektų šablonuose.


[!INCLUDE[footer-include](../includes/footer-banner.md)]