---
title: Subrangos projekto komandos nariai
description: Šioje temoje paaiškinama, kaip sudaryti subrangos sutartis su projekto komandos nariais programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f43f817e59ef83fbf4dda6267327080f7c56e0f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587856"
---
# <a name="subcontracting-project-team-members"></a>Subrangos projekto komandos nariai

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Programoje "Microsoft" Dynamics 365 Project Operations galite pasirinkti sudaryti subrangos sutartis su darbuotojais arba projekto komandos nariais, kuriuose nėra darbuotojų.

- Nekvalifikuotiems projekto komandos nariams priskirtas bendrasis išteklius.
- Personalo komandos nariams priskirtas pavadintas išteklius.

Kai susiejate projekto komandos narį su subrangos eilute, visi priskyrimai užduotims, kurias turi komandos narys, bus perskaičiuoti pagal pirkimo kainoraštį, pridėtą prie subrangos sutarties.  **Puslapio Išsami projekto informacija** skirtuke **Įvertinimai** pasirinkite mygtuką Atnaujinti kainas **, kad pamatytumėte** atnaujintą kainodarą ir (arba) įkainojimą, atsirandančius dėl sprendimo sudaryti subrangos sutartis. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subrangos sutartis su nekvalifikuotu projekto komandos nariu
Puslapyje **Komandos nario išsami informacija** yra subrangos ir subrangos eilučių laukai, leidžiantys projekto vadovui išreikšti, kaip jie norėtų pasinaudoti pajėgumais, reikalingais iš subrangos sutarties. Norėdami sudaryti subrangos sutartį su projekto komandos nariu kaip bendruoju ištekliumi, atlikite šiuos veiksmus:

1.  Puslapyje Komandos nario išsami informacija **pasirinkite subrangos** sutartį.

2.  Galite pasirinkti tik subrangos sutartis, kurių **būsena Yra Juodraštis** arba **Patvirtinta**. **Negalima pasirinkti uždarytų** arba **atšauktų** subrangos sutarčių. 

3.  Antrinės sutarties eilutės **laukas** tampa matomas pasirinkus subrangos sutartį.

4.  Lauke **Subrangos eilutė** galite pasirinkti tik laiko subrangos eilutes. Negalite pasirinkti išlaidų ar medžiagų subrangos eilučių.

5.  Projekto komandos nario įrašo vaidmuo turi atitikti subrangos eilutės vaidmenį. Tai užtikrina, kad laikas vaidmeniui, kuris vertinamas projekte, yra tas pats vaidmuo, kuris perkamas subrangos eilutėje. 

Kai generinis komandos narys yra susietas su subrangos ir subrangos eilute, **bendrosios komandos nario eilutės laukas Darbuotojo tipas** bus atnaujintas į **Sutartininkas**, o **subrangos galiojimas** bus nustatytas kaip **Galiojantis**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subrangos sutartis su personalo projekto komandos nariu
Kaip ir bendrieji ar ne darbuotojai komandos nariai, projekte reikalingi personalo komandos narių pajėgumai taip pat gali būti susieti su subrangos sutartimi. Norėdami sudaryti subrangos sutartis su įvardytu projekto komandos nariu, atlikite šiuos veiksmus:

1.  Įsitikinkite, kad įvardytas išteklius nustatytas kaip užsakomųjų ištekliaus darbuotojo pagal sutartį tipas. Be to, įsitikinkite, kad **rezervuoto ištekliaus laukas Tiekėjas** atitinka pasirinktą subrangos sutarties tiekėją. 

2.  Subrangos sutartis galite pasirinkti tik būsenos Juodraštis **arba** **Patvirtinta** būsena. **Negalima pasirinkti uždarytų** arba **atšauktų** subrangos sutarčių. 

3.  Antrinės sutarties eilutės **laukas** tampa matomas pasirinkus subrangos sutartį.

4.  Lauke **Subrangos eilutė** galite pasirinkti tik laiko subrangos eilutes. Negalite pasirinkti išlaidų ar medžiagų subrangos eilučių.

5.  Projekto komandos nario įrašo vaidmuo turi atitikti subrangos eilutės vaidmenį. Tai užtikrina, kad laikas vaidmeniui, kuris vertinamas projekte, yra tas pats vaidmuo, kuris perkamas subrangos eilutėje. 

Pavadinti projekto komandos nariai, nustatyti kaip užsakomųjų išteklių **sutartininko** tipas, bus rodomi su subrangos galiojimo būsena Neleistina, **jei** jie nėra susieti su subrangos sutartimi. Kai įvardytas projekto komandos narys yra susietas su subrangos ir subrangos eilute, **komandos nario eilutės laukas Darbuotojo tipas** bus atnaujintas į **Sutartininkas**, o **subrangos galiojimas** bus nustatytas kaip **Galiojantis**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
