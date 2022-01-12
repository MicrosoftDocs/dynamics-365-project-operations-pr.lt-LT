---
title: Projekto personalas su sutartininkais ir subrangos pajėgumais
description: Šioje temoje paaiškinama, kaip projekto reikalavimai gali būti įdarbinti naudojant sutartinius darbuotojus arba subrangos pajėgumus Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 7e9a0ca08f472999138589f31ca820b733b6303e
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903728"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekto personalas su sutartininkais ir subrangos pajėgumais

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Bendrieji projekto komandos nariai gali būti įdarbinti su darbuotojais arba sutartininkais. Įdarbindami projektą su sutartininkais, galite apriboti savo personalo parinktis tik konkretiems sutartininkams, priskirtiems subrangos linijai. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Ieškoti personalo išteklių reikalavimų su sutartininkais, priklausančius konkrečiai subrangos eilutei

Norėdami ieškoti ir personalo išteklių poreikių su sutartininkais, priklausančius konkrečiai subrangos linijai, atlikite šiuos veiksmus:

1. Sukurkite generinį projekto komandos narį, nurodantį subrangos ir subrangos eilutę.
2. Generuoti šio bendrojo projekto komandos nario išteklių poreikį naudojant **projekto** komandos narių antrinio tinklelio mygtuką Generuoti poreikį.
3. Pasirinkite komandos nario eilutę, tada **antrinio** tinklelio mygtuką Užsakyti. 
4. Taip atidaroma grafiko lenta su poreikio kontekstu. Kartu su kitais atributais, pvz., datų, vaidmenų ir organizacinių vienetų laukais, grafiko lentos filtrai taip pat automatiškai užpildomi tiekėjo, subrangos ir subrangos eilutės laukais iš išteklių poreikio.
5. Sistema ieško filtro kriterijus atitinkančių išteklių ir juos išvardija. 
6. Pasirinkite vieną iš filtruotų išteklių ir rezervuokite poreikio išteklius. 
7. Projekto komandos narys sukuriamas ir atnaujinamas naudojant subrangos ir subrangos eilučių nuorodas. Eikite į **Projekto įvertinimai** ir pasirinkite **Naujinti** kainas, kad pamatytumėte atnaujintą išteklių priskyrimo savikainą. 

> [!NOTE]
> Projekto komandos nario atnaujinimas su subrangos ir subrangos eilutės nuoroda ne visada gali būti įmanomas rezervuojant, jei išteklius priskiriamas kelioms subrangos eilutėms. Jei sistema negali atnaujinti projekto komandos nario subrangos ir subrangos eilute, atidarykite projekto komandos nario įrašą ir neautomatiniu būdu atnaujinkite šiuos laukus, kad finansinių išlaidų įvertinimas tiksliai atspindėtų subrangovo išlaidas.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Ieškoti ir personalo išteklių reikalavimų su bet kuriuo sutartiniu darbuotoju

Norėdami ieškoti ir personalo išteklių reikalavimų su bet kuriuo sutartiniu darbuotoju, atlikite šiuos veiksmus:

1. Sukurkite generinį projekto komandos narį.
2. Generuoti šio bendrojo projekto komandos nario išteklių poreikį naudojant **projekto** komandos narių antrinio tinklelio mygtuką Generuoti poreikį.
3. Pasirinkite komandos nario eilutę, tada **antrinio** tinklelio mygtuką Užsakyti. 
4. Taip atidaroma grafiko lenta su poreikio kontekstu. Kartu su kitais atributais, pvz., datų, vaidmenų ir organizacinių vienetų laukais, grafiko lentos filtrai taip pat automatiškai užpildomi tiekėjo, subrangos ir subrangos eilutės laukais iš išteklių poreikio. Kadangi reikalavimas neturėjo užpildytų subrangos ar subrangos eilučių verčių, filtro srityje šie atributai bus tušti.
5. Sistema ieško filtro kriterijus atitinkančių išteklių ir juos išvardija.
6. Atnaujinti **filtro srities lauką Darbuotojo tipas** į **Sutarties** darbuotojas, kad ieška būtų apribota iki sutartininkų. Atnaujinti **tiekėją** filtravimo srityje, kad pasirinktumėte tiekėją, kuris apribotų iešką, kad būtų rodomi tik sutartiniai darbuotojai, priklausantys konkrečiai tiekėjo įmonei.
7. Sąraše pasirinkite sutarties darbuotoją ir rezervuokite poreikio išteklius.
8. Sukuriamas projekto komandos narys. Tačiau projekto komandos narys neatnaujinamas jokia subrangos ar subrangos linija, todėl išteklių priskyrimas nebus įkainotas naudojant subrangos kainodarą. Neautomatiniu būdu atnaujinkite projekto komandos narį subrangos eilute ir eikite į **Projekto įvertinimus** ir pasirinkite **Naujinti** kainas, kad pamatytumėte atnaujintą išteklių priskyrimo kainą.

> [!NOTE]
> Projekto komandos nariai, kurių **darbuotojo tipas yra sutarties** **darbuotojas**, bet neturi subrangos nuorodos, **projekto komandos narių** **tinklelyje pažymėti kaip** neleistini. Jei yra projekto komandos narių, turinčių šią būseną, atidarykite projekto komandos nario įrašą ir neautomatiniu būdu atnaujinkite subrangos ir subrangos eilučių laukus, kad finansinių išlaidų įvertinimas tiksliai atspindėtų subrangovo išlaidas **skirtuke** Sąmatos. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
