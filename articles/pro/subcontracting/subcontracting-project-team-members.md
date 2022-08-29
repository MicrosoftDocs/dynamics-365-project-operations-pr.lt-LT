---
title: Subrangos projekto komandos nariai
description: Šiame straipsnyje paaiškinama, kaip sudaryti subrangos sutartis su projekto komandos nariais programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 14abd82cbbd256770105d4272f686590737e2648
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261381"
---
# <a name="subcontracting-project-team-members"></a>Subrangos projekto komandos nariai

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Naršyklėje "Microsoft" Dynamics 365 Project Operations galite pasirinkti sudaryti subrangos sutartis su darbuotojais arba projekto komandos nariais, kuriuose dirba darbuotojai.

- Nedirbantiems projekto komandos nariams priskirtas bendrasis išteklius.
- Komandos nariai, kuriuose dirba darbuotojai, turi priskirtą įvardytą išteklių sąrašą.

Kai susiejate projekto komandos narį su subrangos linija, visos užduotys, kurias turi komandos narys, bus perrašytos pagal pirkimo kainoraštį, pridėtą prie subrangos sutarties.  Puslapio Projekto informacija **skirtuke** **Sąmatos** pasirinkite mygtuką **Naujinti kainas**, kad pamatytumėte atnaujintas kainas ir (arba) įkainojimą, atsirandantį dėl sprendimo sudaryti subrangos sutartį. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Projekto komandos nario, kuriam nedirba darbuotojų, subrangos sutarčių sudarymas
Puslapyje Išsami **komandos nario informacija** yra subrangos ir subrangos linijų laukai, kuriuose projekto vadovas gali išreikšti, kaip jis norėtų panaudoti reikiamą pajėgumą iš subrangos sutarties. Norėdami projekto komandos narį pavesti naudoti kaip bendrąjį išteklių, atlikite šiuos veiksmus:

1.  Pasirinkite subrangos sutartį **puslapyje Komandos nario informacija**.

2.  Subrangos sutartis galite pasirinkti tik naudodami **būseną Juodraštis** arba **Patvirtinta**. **Uždarytų** arba **atšauktų** subrangos sutarčių pasirinkti negalima. 

3.  Laukas Subrangos **linija** tampa matomas pasirinkus subrangos sutartį.

4.  Lauke Subrangos **eilutė** galite pasirinkti tik tam laikui skirtas subrangos eilutes. Negalite pasirinkti išlaidų ar medžiagų subrangos eilučių.

5.  Projekto komandos nario įrašo vaidmuo turi atitikti subrangos linijos vaidmenį. Taip užtikrinama, kad laikas vaidmeniui, kuris numatomas projekte, būtų tas pats vaidmuo, kuris perkamas subrangos linijoje. 

Kai bendrasis komandos narys yra susietas su subrangos ir subrangos linija, **bendrojo komandos nario eilutės laukas Darbuotojo tipas** bus atnaujintas į **Sutartinis darbuotojas**, o **Subrangos galiojimas** bus nustatytas kaip **Galiojantis**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subrangovas projekto komandos nariui, kuriame dirba darbuotojai
Kaip ir bendrieji arba nedirbantys komandos nariai, projektui reikalingi komandos narių pajėgumai taip pat gali būti susieti su subrangos sutartimi. Norėdami sudaryti subrangos sutartį su įvardytu projekto komandos nariu, atlikite šiuos veiksmus:

1.  Įsitikinkite, kad įvardytas išteklius yra nustatytas kaip samdomo darbuotojo rezervuojamų išteklių tipas. Be to, įsitikinkite **, kad rezervuojamo ištekliaus laukas Tiekėjas** atitinka tiekėją pasirinktoje subrangos sutartyje. 

2.  Subrangos sutartis galite pasirinkti tik būsenoje **Juodraštis** arba **Patvirtinta**. **Uždarytų** arba **atšauktų** subrangos sutarčių pasirinkti negalima. 

3.  Laukas Subrangos **linija** tampa matomas pasirinkus subrangos sutartį.

4.  Lauke Subrangos **eilutė** galite pasirinkti tik tam laikui skirtas subrangos eilutes. Negalite pasirinkti išlaidų ar medžiagų subrangos eilučių.

5.  Projekto komandos nario įrašo vaidmuo turi atitikti subrangos linijos vaidmenį. Taip užtikrinama, kad laikas vaidmeniui, kuris numatomas projekte, būtų tas pats vaidmuo, kuris perkamas subrangos linijoje. 

Įvardinti projekto komandos nariai, kurie yra nustatyti kaip rezervuojamo ištekliaus **tipas** pagal sutartį, bus rodomi su subrangos sutarties galiojimo būsena Negaliojanti **,** jei jie nėra susieti su subrangos sutartimi. Kai įvardytas projekto komandos narys yra susietas su subrangos ir subrangos linija, **komandos nario eilutės laukas Darbuotojo tipas** bus atnaujintas į **Sutartinis darbuotojas**, o **Subrangos galiojimas** bus nustatytas kaip **Galiojantis**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
