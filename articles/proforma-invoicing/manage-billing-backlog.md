---
title: Atsiskaitymo nebaigtų užduočių tvarkymas
description: Šioje temoje pateikta informacija, kaip peržiūrėti ir tvarkyti atsiskaitymo nebaigtas užduotis naudojant „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bec6afe04a705d4f55ac3a7de93a64b47021fbb4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122353"
---
# <a name="manage-the-billing-backlog"></a>Atsiskaitymo nebaigtų užduočių tvarkymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ yra du skirtieji rodiniai, padėsiantys jums tvarkyti ir valdyti atsiskaitymo nebaigtas užduotis. Jos yra **Fiksuoti kainų etapai** ir **Bebaigtos laiko ir medžiagų sąskaitų užduotys** Norėdami pasirinkti rodinį, „Project Operations“ srityje **Sales**, kairiajame naršymo puslapyje pasirinkite **Atsiskaitymas**. Čia saugomi nebaigtų atsiskaitymo užduočių saitai.

## <a name="fixed-price-milestones"></a>Fiksuotos kainos gairės

Šiame rodinyje išvardyti visi fiksuotos kainos etapai visose sistemos projekto sutarties eilutėse. Vieną ar kelis etapus galima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą** arba **Neparengta išrašyti sąskaitos faktūros** iš šio rodinio. Kai pažymite etapą kaip **Parengta išrašyti sąskaitą faktūrą**, etapas tampa pasiekiamu sąskaitos faktūros juodraštyje.

Kai kelių klientų sutarties eilutėse yra fiksuotos kainos atsiskaitymo metodas, kiekvienam klientui sukuriama po vieną etapą sutarties eilutėje. Vartotojas sukuria etapą ir tas etapas suskaidomas į konkretaus kliento etapų vidinius įrašus, atsižvelgiant į atsiskaitymo procentinį suskaidymą, apibrėžtą kiekvienam klientui sutarties eilutėje. Rodinyje **Fiksuotos kainos etapai** matysite individualius konkrečiam klientui skirtus etapų įrašus. Kiekvienas iš šių etapų įrašų gali būti pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą** atskirai nuo šio rodinio. Kai vienas ar daugiau susijusių etapo suskaitymų yra pažymėti kaip **Parengta išrašyti sąskaitą faktūrą**, antraštės būsena pasikeičia iš **Vykdoma** į **Nepradėta**. Kai į sąskaitą faktūrą įtraukiami visi etapo suskaitymai, antraštės etapo būsena tampa **Baigta**.

Šiame rodinyje rodomas sąskaitos faktūros juodraščio etapas su atsiskaitymo būsena **Kliento sąskaita faktūra sukurta**. Patvirtinus sąskaitos faktūros juodraštį, šio įrašo atsiskaitymo būsena atnaujinama į **Sąskaita faktūra užregistruota**. Atnaujinant šią būsenos reikšmę nerekomenduojame naudoti pasirinktinio kodo. Jei šios būsenos reikšmės bus atnaujintos naudojant pasirinktinį kodą, „Project Operations“ neveiks tinkamai.

## <a name="time-and-material-billing-backlog"></a>Laiko ir medžiagų atsiskaitymo nebaigtos užduotys

Šiame rodinyje pateikiamas visų neapmokestintų pardavimo faktinių sumų, kurių sąskaita faktūra neišrašyta pagal visas sistemos projekto sutartis, sąrašas. Vieną ar kelias neapmokestinto pardavimo sumas galima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą** arba **Neparengta išrašyti sąskaitos faktūros** iš šio rodinio. Pažymėjus neapmokestinto pardavimo faktines sumas kaip **Parengta išrašyti sąskaitą faktūrą**, jas galima įtraukti į sąskaitą faktūrą.

Neapmokestinto pardavimo faktinių sumų, kurių **Neviršytina** būsena yra **Nepavyko**, negalima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą**. Jei šias faktines sumas reikia pažymėti kaip tokias, iš naujo nustatykite kitų patvirtintų faktinių sumų būseną sutarties eilutėje, tada įvertinkite **neviršytiną** būseną.

Jei yra kelių klientų sutarties eilučių, kuriose yra laiko ir medžiagų atsiskaitymo būdas, kai laikas ir išlaidos patvirtinami, kiekvienam klientui pagal sutarties eilutę sukuriamos neapmokestinto pardavimo faktinės sumos pagal sąskaitų išrašymo procentą, nustatytą kiekvienam klientui sutarties eilutėje. Rodinyje **Laiko ir medžiagų atsiskaitymo nebaigtos užduotys** matysite šiuos individualius klientui būdingus neapmokestinto pardavimo faktines sumas. Kiekviena iš šių neapmokestinto pardavimo sumų gali būti pažymėta kaip **Parengta išrašyti sąskaitą faktūrą** atskirai nuo šio rodinio.

Šiame rodinyje rodomos sąskaitos faktūros juodraščio neapmokestinto pardavimo faktinės sumos su **atsiskaitymo būsena** **Kliento sąskaita faktūra sukurta**. Patvirtinus sąskaitos faktūros juodraštį, šio įrašo atsiskaitymo būsena atnaujinama į **Kliento sąskaita faktūra užregistruota**. Atnaujinant šią būsenos reikšmę, kai ji yra šiame etape, nerekomenduojame naudoti pasirinktinio kodo. Jei šios būsenos reikšmės bus atnaujintos naudojant pasirinktinį kodą, „Project Operations“ neveiks tinkamai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]