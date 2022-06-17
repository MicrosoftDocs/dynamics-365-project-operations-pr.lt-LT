---
title: Projekto su sutarties darbuotojais ir subrangos pajėgumo personalas
description: Šiame straipsnyje paaiškinama, kaip projekto reikalavimai gali būti įdarbinti naudojant sutartininkus arba subrangos pajėgumus programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 173e1c20d2d046ee2120ec178e51d4868b70847d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922094"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekto su sutarties darbuotojais ir subrangos pajėgumo personalas

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Bendrieji projekto komandos nariai gali būti darbuotojai su darbuotojais arba sutartininkais. Dirbdami projekte su sutartininkais, galite apriboti savo personalo galimybes tik konkretiems sutartininkams, priskirtiems subrangos eilutei. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Ieškoti personalo išteklių reikalavimų su sutartininkais, priklausančiais konkrečiai subrangos eilutei

Norėdami ieškoti ir darbuotojų išteklių reikalavimų su sutartininkais, priklausančiais konkrečiai subrangos eilutei, atlikite šiuos veiksmus:

1. Sukurkite bendrąjį projekto komandos narį, kuris nurodo subrangos ir subrangos eilutę.
2. Generuoti išteklių poreikį šiam bendram projekto komandos nariui naudojant **projekto komandos narių potinklio mygtuką Generuoti poreikį**.
3. Pasirinkite komandos nario eilutę, tada apatiniame **tinklelyje pasirinkite mygtuką Užsakyti**. 
4. Taip atidaroma grafiko lenta su reikalavimų kontekstu. Kartu su kitais atributais, pvz., datomis, vaidmeniu ir organizacinių vienetų laukais, grafiko lentos filtrai taip pat automatiškai užpildomi tiekėjo, subrangos ir subrangos eilutės laukais iš išteklių poreikio.
5. Sistema ieško išteklių, atitinkančių filtro kriterijus, ir juos išvardija. 
6. Pasirinkite vieną iš filtruotų išteklių ir užsisakykite reikalavimo išteklius. 
7. Projekto komandos narys sukuriamas ir atnaujinamas subrangos sutarčių ir subrangos eilučių nuorodomis. Eikite į **Projekto įvertinimai** ir pasirinkite **Naujinti kainas**, kad pamatytumėte atnaujintą išteklių priskyrimo kainą. 

> [!NOTE]
> Užsakymo metu ne visada galima atnaujinti projekto komandos narį subrangos ir subrangos eilutės nuoroda, jei išteklius priskiriamas kelioms subrangos eilutėms. Jei sistema negali atnaujinti projekto komandos nario subrangos ir subrangos eilute, atidarykite projekto komandos nario įrašą ir rankiniu būdu atnaujinkite šiuos laukus, kad finansinių išlaidų įvertinimas tiksliai atspindėtų subrangovo savikainą.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Ieškoti ir personalo išteklių reikalavimų su bet kuriuo sutartininku

Norėdami ieškoti ir personalo išteklių reikalavimų su bet kuriuo sutartininku, atlikite šiuos veiksmus:

1. Sukurkite bendrąjį projekto komandos narį.
2. Generuoti išteklių poreikį šiam bendram projekto komandos nariui naudojant **projekto komandos narių potinklio mygtuką Generuoti poreikį**.
3. Pasirinkite komandos nario eilutę, tada apatiniame **tinklelyje pasirinkite mygtuką Užsakyti**. 
4. Taip atidaroma grafiko lenta su reikalavimų kontekstu. Kartu su kitais atributais, pvz., datomis, vaidmeniu ir organizacinių vienetų laukais, grafiko lentos filtrai taip pat automatiškai užpildomi tiekėjo, subrangos ir subrangos eilutės laukais iš išteklių poreikio. Kadangi reikalavimas nebuvo užpildytas jokiomis subrangos ar subrangos eilučių vertėmis, šie atributai filtro srityje bus tušti.
5. Sistema ieško išteklių, atitinkančių filtro kriterijus, ir juos išvardija.
6. **Atnaujinkite filtro srities lauką Darbuotojo tipas** į **Sutartininkas,** kad iešką apribotumėte sutartininkais. Atnaujinti **tiekėją** filtro srityje, kad pasirinktumėte tiekėją, kad apribotumėte iešką, kad būtų rodomi tik sutartininkai, priklausantys konkrečiai tiekėjo įmonei.
7. Iš sąrašo pasirinkite sutarties darbuotoją ir užsisakykite reikalavimo išteklius.
8. Sukuriamas projekto komandos narys. Tačiau projekto komandos narys neatnaujinamas jokia subrangos ar subrangos eilute, todėl išteklių priskyrimas nebus įkainotas naudojant subrangos kainą. Neautomatiniu būdu atnaujinkite projekto komandos narį subrangos eilute ir eikite į **Projekto įvertinimai** ir pasirinkite Atnaujinti kainas **, kad pamatytumėte** atnaujintą išteklių priskyrimo savikainą.

> [!NOTE]
> Projekto komandos nariai, kurių **darbuotojo tipas** **yra Sutartininkas**, bet neturi subrangos nuorodos, projekto komandos narių **tinklelyje pažymėti kaip** Neleistini **·**. Jei yra projekto komandos narių, turinčių šią būseną, atidarykite projekto komandos nario įrašą ir rankiniu būdu atnaujinkite subrangos ir subrangos eilučių laukus, kad finansinių išlaidų įvertinimas tiksliai atspindėtų subrangovo savikainą **skirtuke Įvertinimai**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
