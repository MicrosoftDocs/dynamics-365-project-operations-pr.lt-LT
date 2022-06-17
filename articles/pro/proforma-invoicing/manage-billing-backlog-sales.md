---
title: Projekto atsiskaitymo nebaigtų užduočių valdymas
description: Šiame straipsnyje pateikiama informacija apie įvairius rodinius, kuriuos galima naudoti valdant projektų atsiskaitymo atsilikimą.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f2e68449a8f1a0da62850454fb8ae56daffbab0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930098"
---
# <a name="manage-project-billing-backlog"></a>Projekto atsiskaitymo nebaigtų užduočių valdymas 

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

„Dynamics 365 Project Operations“ programoje yra specialieji rodiniai, kad būtų lengviau tvarkyti nebaigtas atsiskaitymo užduotis. Norėdami tvarkyti nebaigtas atsiskaitymo užduotis, pasirinkite saitus dalies **Atsiskaitymas** srityje **Pardavimas**. 

Yra tolesni rodiniai.

- Išankstiniai apmokėjimai ir avansai
- Galimi išankstiniai apmokėjimai ir avansai
- Fiksuotos kainos gairės
- Produktų atsiskaitymo nebaigtos užduotys
- Laiko ir medžiagų atsiskaitymo nebaigtos užduotys

## <a name="retainers-and-advances"></a>Išankstiniai apmokėjimai ir avansai

Rodinyje **Išankstiniai apmokėjimai ir avansai** išvardyti visi išankstiniai apmokėjimai ir avansai, esantys visose sistemos projektų sutartyse. Kai išrašoma sąskaita faktūra už išankstinį apmokėjimą ar avansą, avanso suma tampa pasiekiama naudoti.

## <a name="available-retainers-and-advances"></a>Galimi išankstiniai apmokėjimai ir avansai

Rodinyje **Galimi išankstiniai apmokėjimai ir avansai** išvardyti visi galimi išankstiniai apmokėjimai ir avansai, esantys visose sistemos projektų sutartyse. Kai išrašoma sąskaita faktūra už išankstinį apmokėjimą ar avansą, avanso suma tampa pasiekiama naudoti ir yra įtraukiama į sąrašą. Visiškai išnaudojus išankstinio apmokėjimo ar avanso sumą, ji pašalinama iš sąrašo.

## <a name="fixed-price-milestones"></a>Fiksuotos kainos gairės

Rodinyje **Fiksuotos kainos etapai** išvardyti visi fiksuotos kainos etapai, esantys visose sistemos projekto sutarties eilutėse. Vieną ar kelis etapus šiame rodinyje galima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą** arba **Neparengta išrašyti sąskaitos faktūros**. Etapą pažymėjus **Parengta išrašyti sąskaitą faktūrą**, jį galima įdėti į sąskaitos faktūros juodraštį.

Kai kelių klientų sutarties eilutėse taikomas fiksuotos kainos atsiskaitymo metodas, etapas sukuriamas kiekvienam sutarties eilutės klientui. Sukūrus etapą, ji galima išskaidyti į atskirus konkrečiam klientui taikomus etapų įrašus. Šis išskaidymas yra vidinis ir atitinka sąskaitų išrašymo procentinę dalį, apibrėžtą kiekvienam sutarties eilutės klientui. Rodinyje **Fiksuotos kainos etapai** matysite atskirus konkrečiam klientui skirtus etapų įrašus. Kiekvienas iš šių etapų įrašų gali būti pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą** atskirai nuo šio rodinio. Kai vienas ar daugiau susijusių etapų išskaidymų pažymėti kaip **Parengta išrašyti sąskaitą faktūrą**, antraštės būsena iš **Nepradėta** atnaujinama į **Vykdoma**. Kai sąskaita faktūra išrašoma visiems išskaidytiems etapams, antraštės etapo būsena atnaujinama į **Baigta**.

Šiame rodinyje rodomas sąskaitos faktūros juodraščio etapas su atsiskaitymo būsena **Kliento sąskaita faktūra sukurta**. Patvirtinus sąskaitos faktūros juodraštį, įrašo sąskaitų išrašymo būsena atnaujinama į **Kliento sąskaita faktūra užregistruota**. Neatnaujinkite šios būsenos reikšmės naudodami pasirinktinį kodą. Kai šios būsenos reikšmės atnaujinamos naudojant pasirinktinį kodą, „Project Operations“ veikia netinkamai.

## <a name="product-billing-backlog"></a>Produktų atsiskaitymo nebaigtos užduotys

Rodinyje **Nebaigtos atsiskaitymo už produktus užduotys** išvardytos visos su produktais susijusios sutarties eilutės, esančios visose sistemos projektų sutartyse. Vieną ar kelias su produktais susijusias sutarčių eilutes šiame rodinyje galima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą** arba **Neparengta išrašyti sąskaitos faktūros**. Su produktais susijusią sutarties eilutę pažymėjus **Parengta išrašyti sąskaitą faktūrą**, ją galima įdėti į sąskaitos faktūros juodraštį.

Su produktais susijusi sutarties eilutė, esanti sąskaitos faktūros juodraštyje, šiame rodinyje rodoma nustačius būseną **Kliento sąskaita faktūra sukurta**. Patvirtinus sąskaitos faktūros juodraštį, šio įrašo atsiskaitymo būsena atnaujinama į **Kliento sąskaita faktūra užregistruota**. Neatnaujinkite šios būsenos reikšmės naudodami pasirinktinį kodą. Kai šios būsenos reikšmės atnaujinamos naudojant pasirinktinį kodą, „Project Operations“ veikia netinkamai.

## <a name="time-and-material-billing-backlog"></a>Laiko ir medžiagų atsiskaitymo nebaigtos užduotys

Rodinyje **Nebaigtos atsiskaitymo už laiką ir medžiagas užduotys** išvardyti visi pardavimų, už kuriuos neatsiskaityta, faktiniai duomenys, esantys visose sistemos projektų sutartyse, kurioms neišrašyta sąskaita faktūra. Vieną ar kelias neapmokestinto pardavimo sumas galima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą** arba **Neparengta išrašyti sąskaitos faktūros** iš šio rodinio. Pažymėjus neapmokestinto pardavimo faktines sumas kaip **Parengta išrašyti sąskaitą faktūrą**, jas galima įtraukti į sąskaitą faktūrą.

Faktinių pardavimo, už kurį neatsiskaityta, duomenų, kurių **Neviršyti** būsena yra **Nepavyko**, negalima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą**. Jei faktinius duomenis reikia pažymėti kaip **Parengta išrašyti sąskaitą faktūrą**, iš naujo nustatykite kitų paskirtų faktinių duomenų būseną sutarties eilutėje. tada iš naujo įvertinkite **Neviršyti** būseną.

Jei kelių klientų sutarčių eilutėse taikomas atsiskaitymo už laiką ir medžiagas metodas, patvirtinant laiką ir išlaidas, kiekvienam sutarties eilutės klientui pagal sutarties atsiskaitymo procento išskaidymą, apibrėžtą kiekvienam klientui, sukuriamas pardavimo, už kurį neatsiskaityta, duomuo. Rodinyje **Nebaigtos atsiskaitymo už laiką ir medžiagas užduotys** matysite šiuos atskirus konkretiems klientams taikomus pardavimo, už kurį neatsiskaityta, faktinius duomenis. Kiekviena iš šių neapmokestinto pardavimo sumų gali būti pažymėta kaip **Parengta išrašyti sąskaitą faktūrą** atskirai nuo šio rodinio.

Pardavimo, už kurį neatsiskaityta, faktinis duomuo, esantis sąskaitos faktūros juodraštyje, šiame rodinyje rodomas nustačius būseną **Kliento sąskaita faktūra sukurta**. Patvirtinus sąskaitos faktūros juodraštį, šio įrašo atsiskaitymo būsena atnaujinama į **Kliento sąskaita faktūra užregistruota**. Neatnaujinkite šios būsenos reikšmės naudodami pasirinktinį kodą. Kai šios būsenos reikšmės atnaujinamos naudojant pasirinktinį kodą, „Project Operations“ veikia netinkamai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
