---
title: Projekto su sutarties darbuotojais ir subrangos pajėgumo personalas
description: Šiame straipsnyje paaiškinama, kaip projekto reikalavimus galima įdarbinti naudojant sutartininkus arba subrangovų pajėgumus programoje "Microsoft"Dynamics 365 Project Operations.
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

Bendrieji projekto komandos nariai gali turėti darbuotojų arba pagal sutartis dirbančių darbuotojų. Kai projekte dirbama su sutartininkais, galite apriboti savo personalo galimybes iki konkrečių pagal sutartį dirbančių darbuotojų, priskirtų subrangos linijai. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Ieškokite darbuotojų išteklių reikalavimų su sutartininkais, priklausančiais konkrečiai subrangos linijai

Norėdami ieškoti darbuotojų, pagal kuriuos sudarytos sutartys ir kurie priklauso konkrečiai subrangos linijai, ir darbuotojų išteklių reikalavimų, atlikite šiuos veiksmus:

1. Sukurkite bendrąjį projekto komandos narį, nurodantį subrangos ir subrangos liniją.
2. Generuokite išteklių reikalavimą šiam bendram projekto komandos nariui naudodami **projekto komandos narių subtinklatinklyje esantį mygtuką Generuoti reikalavimą**.
3. Pasirinkite komandos nario eilutę, tada antriniame **tinklelyje pasirinkite mygtuką Rezervuoti**. 
4. Taip atidaroma tvarkaraščio valdyba su reikalavimų kontekstu. Kartu su kitais atributais, pvz., datų, vaidmens ir organizacijos vieneto laukais, sąrašo lentos filtrai taip pat automatiškai užpildomi tiekėjo, subrangos ir subrangos eilučių laukais iš išteklių poreikio.
5. Sistema ieško išteklių, kurie atitinka filtro kriterijus, ir juos išvardija. 
6. Pasirinkite vieną iš filtruotų išteklių ir rezervuokite reikalavimo šaltinį. 
7. Projekto komandos narys sukuriamas ir atnaujinamas naudojant subrangos ir subrangos linijų nuorodas. Eikite į **Projekto įvertinimai** ir pasirinkite **Naujinti kainas**, kad pamatytumėte atnaujintas išteklių priskyrimo išlaidas. 

> [!NOTE]
> Projekto komandos nario atnaujinimas naudojant subrangos sutartį ir subrangos linijos nuorodą ne visada gali būti įmanomas užsakymo metu, jei ištekliai priskiriami kelioms subrangos linijoms. Jei sistema negali atnaujinti projekto komandos nario subrangos ir subrangos linija, atidarykite projekto komandos nario įrašą ir rankiniu būdu atnaujinkite šiuos laukus, kad finansinių išlaidų sąmata tiksliai atspindėtų subrangovo išlaidas.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Ieškokite ir personalo išteklių reikalavimų su bet kuriuo pagal sutartį dirbančiu darbuotoju

Norėdami ieškoti darbuotojų ir darbuotojų išteklių reikalavimų pas bet kurį sutartininką, atlikite šiuos veiksmus:

1. Sukurkite bendrą projekto komandos narį.
2. Generuokite išteklių reikalavimą šiam bendram projekto komandos nariui naudodami **projekto komandos narių subtinklatinklyje esantį mygtuką Generuoti reikalavimą**.
3. Pasirinkite komandos nario eilutę, tada antriniame **tinklelyje pasirinkite mygtuką Rezervuoti**. 
4. Taip atidaroma tvarkaraščio valdyba su reikalavimų kontekstu. Kartu su kitais atributais, pvz., datų, vaidmens ir organizacijos vieneto laukais, sąrašo lentos filtrai taip pat automatiškai užpildomi tiekėjo, subrangos ir subrangos eilučių laukais iš išteklių poreikio. Kadangi reikalavimas nebuvo užpildytas jokiomis subrangos arba subrangos linijų reikšmėmis, šie atributai filtro srityje bus tušti.
5. Sistema ieško išteklių, kurie atitinka filtro kriterijus, ir juos išvardija.
6. Atnaujinkite filtro srities lauką **Darbuotojo tipas** į **Sutartinis darbuotojas**, kad apribotumėte paiešką iki sutartininkų. Atnaujinkite **tiekėją** filtro srityje, kad pasirinktumėte tiekėją, kuris apribotų iešką, kad būtų rodomi tik sutartininkai, priklausantys konkrečiai tiekėjo įmonei.
7. Iš sąrašo pasirinkite pagal sutartį dirbantį darbuotoją ir rezervuokite reikalavimo išteklius.
8. Sukuriamas projekto komandos narys. Tačiau projekto komandos narys nėra atnaujinamas jokia subrangos ar subrangos linija, todėl išteklių priskyrimas nebus įkainotas naudojant subrangos kainodarą. Rankiniu būdu atnaujinkite projekto komandos narį naudodami subrangos eilutę, eikite į **Projekto sąmatos** ir pasirinkite **Naujinti kainas**, kad pamatytumėte atnaujintas išteklių priskyrimo išlaidas.

> [!NOTE]
> Projekto komandos nariai, kurių darbuotojo tipas **yra** sutarties darbuotojas **,** bet neturi subrangos nuorodos, tinklelyje **"Project" komandos nariai** pažymėti kaip **netinkami**. Jei yra projekto komandos narių, turinčių šią būseną, atidarykite projekto komandos nario įrašą ir rankiniu būdu atnaujinkite subrangos ir subrangos linijos laukus, kad finansinių išlaidų sąmata tiksliai atspindėtų subrangovo išlaidas skirtuke **Sąmatos**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
