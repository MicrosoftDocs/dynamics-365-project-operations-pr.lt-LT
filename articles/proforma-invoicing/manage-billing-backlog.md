---
title: Atsiskaitymo nebaigtų užduočių tvarkymas
description: Šioje temoje pateikta informacija, kaip peržiūrėti ir tvarkyti atsiskaitymo nebaigtas užduotis naudojant „Project Operations“.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7c242937cd9dd277f8d92b7a29333c1fa272e5f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011921"
---
# <a name="manage-billing-backlog"></a>Atsiskaitymo nebaigtų užduočių tvarkymas

_ **Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

„Dynamics 365 Project Operations“ programoje yra specialieji rodiniai, kad būtų lengviau tvarkyti nebaigtas atsiskaitymo užduotis. Norėdami tvarkyti nebaigtas atsiskaitymo užduotis, pasirinkite saitus dalies **Atsiskaitymas** srityje **Pardavimas**. 

Yra tolesni rodiniai.

- Išankstiniai apmokėjimai ir avansai
- Galimi išankstiniai apmokėjimai ir avansai
- Fiksuotos kainos gairės
- Laiko ir medžiagų atsiskaitymo nebaigtos užduotys

## <a name="retainers-and-advances"></a>Išankstiniai apmokėjimai ir avansai

Rodinyje **Išankstiniai apmokėjimai ir avansai** pateikiami visų projekto sutarčių išankstiniai apmokėjimai ir avansai. Kai išrašoma sąskaita faktūra už išankstinį apmokėjimą ar avansą, avanso suma tampa pasiekiama naudoti.

## <a name="available-retainers-and-advances"></a>Galimi išankstiniai apmokėjimai ir avansai

Rodinyje **Galimi išankstiniai apmokėjimai ir avansai** pateikiami visų projekto sutarčių visi galimi išankstiniai apmokėjimai ir avansai. Kai išrašoma sąskaita faktūra už išankstinį apmokėjimą ar avansą, avanso suma tampa pasiekiama naudoti ir yra įtraukiama į sąrašą. Visiškai išnaudojus išankstinio apmokėjimo arba avanso kiekį, jis pašalinamas iš sąrašo.

## <a name="fixed-price-milestones"></a>Fiksuotos kainos gairės

Rodinyje **Fiksuotos kainos gairės** pateikiami visų projekto sutarčių eilutėse nurodytos fiksuotos kainos gairės. Šiame rodinyje vieną arba kelis etapus galima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą** arba **Neparengta išrašyti sąskaitą faktūrą**. Etapą pažymėjus **Parengta išrašyti sąskaitą faktūrą**, jį galima įdėti į sąskaitos faktūros juodraštį.

Kai kelių klientų sutarties eilutėse taikomas fiksuotos kainos atsiskaitymo metodas, etapas sukuriamas kiekvienam sutarties eilutės klientui. Sukūrus etapą, ji galima išskaidyti į atskirus konkrečiam klientui taikomus etapų įrašus. Šis išskaidymas yra vidinis ir atitinka sąskaitų išrašymo procentinę dalį, apibrėžtą kiekvienam sutarties eilutės klientui. Rodinyje **Fiksuotos kainos etapai** matysite atskirus konkrečiam klientui skirtus etapų įrašus. Kiekvienas iš šių etapų įrašų gali būti pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą** atskirai nuo šio rodinio. Vieno ar kelių susijusių etapų skaidymus pažymėjus kaip **Parengta išrašyti sąskaitą faktūrą**, antraštės būsena iš **Nepradėta** atnaujinama į **Vykdoma**. Išrašius sąskaitas faktūras už visus etapo skaidymus, antraštės etapo būsena atnaujinama į **Atlikta**.

Šiame rodinyje rodomas sąskaitos faktūros juodraščio etapas su atsiskaitymo būsena **Kliento sąskaita faktūra sukurta**. Patvirtinus sąskaitos faktūros juodraštį, įrašo sąskaitų išrašymo būsena atnaujinama į **Kliento sąskaita faktūra užregistruota**. 

> [!NOTE] 
> Neatnaujinkite šios būsenos reikšmės naudodami pasirinktinį kodą. Kai šios būsenos reikšmės atnaujinamos naudojant pasirinktinį kodą, „Project Operations“ veikia netinkamai.

## <a name="time-and-material-billing-backlog"></a>Laiko ir medžiagų atsiskaitymo nebaigtos užduotys

Rodinyje **Nebaigtos atsiskaitymo už laiką ir medžiagas užduotys** išvardyti visi pardavimų, už kuriuos neatsiskaityta, faktiniai duomenys, esantys visose sistemos projektų sutartyse, kurioms neišrašyta sąskaita faktūra. Vieną ar kelias neapmokestinto pardavimo sumas galima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą** arba **Neparengta išrašyti sąskaitos faktūros** iš šio rodinio. Pažymėjus neapmokestinto pardavimo faktines sumas kaip **Parengta išrašyti sąskaitą faktūrą**, jas galima įtraukti į sąskaitą faktūrą.

Faktinių pardavimo, už kurį neatsiskaityta, duomenų, kurių **Neviršyti** būsena yra **Nepavyko**, negalima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą**. Jei faktinius duomenis reikia pažymėti kaip **Parengta išrašyti sąskaitą faktūrą**, iš naujo nustatykite kitų sutarties eilutėje nurodytų faktinių duomenų, kurie jau pateikti, būseną, tada iš naujo įvertinkite būseną **Neviršyti**.

Jei kelių klientų sutarčių eilutėse taikomas atsiskaitymo už laiką ir medžiagas metodas, patvirtinant laiką ir išlaidas, kiekvienam sutarties eilutės klientui pagal sutarties atsiskaitymo procento išskaidymą, apibrėžtą kiekvienam klientui, sukuriamas pardavimo, už kurį neatsiskaityta, duomuo. Rodinyje **Nebaigtos atsiskaitymo už laiką ir medžiagas užduotys** matysite šiuos atskirus konkretiems klientams taikomus pardavimo, už kurį neatsiskaityta, faktinius duomenis. Kiekviena iš šių neapmokestinto pardavimo sumų gali būti pažymėta kaip **Parengta išrašyti sąskaitą faktūrą** atskirai nuo šio rodinio.

Šiame rodinyje į juodraštinę sąskaitą faktūrą įtrauktas faktinis pardavimas, už kurį neišrašyta sąskaita, rodomas taikant būseną **Kliento sąskaita faktūra sukurta**. Patvirtinus sąskaitos faktūros juodraštį, šio įrašo atsiskaitymo būsena atnaujinama į **Kliento sąskaita faktūra užregistruota**. 

> [!NOTE] 
> Neatnaujinkite šios būsenos reikšmės naudodami pasirinktinį kodą. Kai šios būsenos reikšmės atnaujinamos naudojant pasirinktinį kodą, „Project Operations“ veikia netinkamai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
