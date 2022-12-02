---
title: Projekto su sutarties darbuotojais ir subrangos pajėgumo personalas
description: Šiame straipsnyje paaiškinta, kaip projektų reikalavimus gali vykdyti darbuotojai pagal sutartį arba darbo rangos sutarties pajėgumą naudojant „Microsoft Dynamics 365 Project Operations“.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 30e16efeed93ab4568eac57fb3ed46067a08524d
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522446"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Projekto su sutarties darbuotojais ir subrangos pajėgumo personalas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Bendrosios projekto komandos nariai gali būti samdomi su darbuotojais arba sutarčių darbuotojais. Kai dirbate su sutarties darbuotojais, galite apriboti darbuotojų parinktis iki konkrečių sutarties darbuotojų, kurie priskirti tam tikrai subrangos sutarties eilutei. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Ieškoti darbuotojų išteklių reikalavimų su sutarties darbuotojais, priklausančiais konkrečiai subrangos sutarties eilutei

Ieškoti darbuotojų išteklių reikalavimų su sutarties darbuotojais, priklausančiais konkrečiai subrangos sutarties eilutei, vadovaukitės šiais žingsniais:

1. Sukurkite bendrąjį projekto komandos nariį, kuris jau susietas su subrangos sutartimi ir jos eilute.
2. Sugeneruokite šio bendrojo projekto komandos nario išteklių reikalavimą projekto komandos narių tinklelyje naudodami mygtuką **Generuoti reikalavimą**.
3. Pasirinkite komandos nario eilutę, tada tinklelyje pasirinkite mygtuką **Knyga**. 
4. Atidaroma grafiko lenta su reikalavimų kontekstu. Grafiko lentos filtruose kartu su kitais atributais, pvz., datomis, vaidmenimis ir organizacijos vienetų laukais, automatiškai iš ištekliaus reikalavimo įvedami tiekėjo, subrangos sutarties ir jos eilutės laukai.
5. Sistema ieško filtravimo kriterijus atitinkančių išteklių ir juos išvardija. 
6. Pažymėkite vieną iš filtruotų išteklius ir rezervuokite reikalavimo išteklių. 
7. Projekto komandos narys sukurtas ir atnaujntas pagal subrangos sutarties ir jos eilutės šaltinius. Eikite į **Project Estimates** ir pasirinkite **Atnaujinti kainas**, kad pamatytumėte atnaujintas išteklių priskyrimo išlaidas. 

> [!NOTE]
> Atnaujinant projekto komandos narį su subrangos sutartimi ir jos eilute šaltinis gali būti ne visada prieinamas per rezervavimo procecą, jei išteklius priskirtas kelioms subrangos sutarties eilutėms. Jei sistemai nepavyksta atnaujinti projekto komandos narių, su subrangos sutartimi ir sutarties eilute, atidarykite tokio projekto komandos nario įrašą ir rankiniu būdu atnaujinkite šiuos laukus, kad finansinių išlaidų įvertinimas tiksliai atspindėtų subrangovo išlaidas.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Ieškokite bet kurio darbuotojo išteklių reikalavimų su bet kuriuo sutarties darbuotoju

Norėdami ieškoti bet kurio darbuotojo išteklių reikalavimų su bet kuriuo sutarties darbuotoju, vadovaukitės šiais žingsniais:

1. Sukurkite bendrojo projekto komandos narį.
2. Sugeneruokite šio bendrojo projekto komandos nario išteklių reikalavimą projekto komandos narių tinklelyje naudodami mygtuką **Generuoti reikalavimą**.
3. Pasirinkite komandos nario eilutę, tada tinklelyje pasirinkite mygtuką **Knyga**. 
4. Atidaroma grafiko lenta su reikalavimų kontekstu. Grafiko lentos filtruose kartu su kitais atributais, pvz., datomis, vaidmenimis ir organizacijos vienetų laukais, automatiškai iš ištekliaus reikalavimo įvedami tiekėjo, subrangos sutarties ir jos eilutės laukai. Kadangi reikalavimas neturi jokių įvestų subrangos sutarties ar jos eilutės reikšmių, šie atributai filtro srityje bus tušti.
5. Sistema ieško filtravimo kriterijus atitinkančių išteklių ir juos išvardija.
6. Atnaujinkite lauką **Darbuotojo tipas** filtrų srityje į **Sutarties darbuotojas** kad būtų ieškoma tik sutarties darbuotojų. Filtro srityje atnaujinkite **Tiekėją**, kad pasirinktumėte tiekėją, kad būtų ribojama ieška, kad būtų rodomi tik konkrečios pardavėjo įmonės sutarties darbuotojai.
7. Iš sąrašo pažymėkite sutarties darbuotoją ir rezervkite reikalavimo išteklius.
8. Projekto komandos narys sukurtas. Tačiau projekto komandos narys nėra atnaujinamas su bet kokia subrangos sutartimi ar jos eilute, todėl išteklių priskyrimas nebus įkainojamas naudojant subrangos sutarties kainodarą. Rankiniu būdu atnaujinkite projekto komandos narį su subrangos sutartimi ir eikite į **Projekto sąmatos** ir pasirinkite **Atnaujinti kainas**, kad pamatytumėte atnaujintas išteklių priskyrimo išlaidas.

> [!NOTE]
> Projekto komandos nariai, kurių **Darbuotojo tipas** yra **Pagal sutartį dirbantis darbuotojas**, bet jie neturi subrangos sutarties nuorodos, tinklelyje **Projekto komandos nariai** pažymimi kaip **Negalioja**. Jei yra projekto komandos narių, kurių būsena tokia, atidarykite tokio projekto komandos nario įrašą ir rankiniu būdu atnaujinkite subrangos sutarties ir subrangos sutarties eilutės laukus, kad finansinių išlaidų įvertinimas tiksliai atspindėtų subrangovo išlaidas skirtuke **Įvertinimai**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
