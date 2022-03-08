---
title: Subrangos projekto komandos nariai
description: Šioje temoje paaiškinama, kaip subrangos projekto komandos narius Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 846de9afab5bf9ebc13670abd6ce735801796f0e
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903061"
---
# <a name="subcontracting-project-team-members"></a>Subrangos projekto komandos nariai

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Programoje Microsoft Dynamics 365 Project Operations galite pasirinkti subrangos sutartis su neįjungus arba darbuotojų komanda.

- Nepriskirti projekto komandos nariai turi priskirtą bendrąjį išteklių.
- Darbuotojai komandos nariai turi priskirtą pavadintą išteklių.

Kai susiejate projekto komandos narį su subrangos eilute, visi komandos nario priskyrimai užduotims bus iš naujo įkainoti pagal pirkimo kainoraštį, pridėtą prie subrangos.  Puslapio **Išsami projekto informacija skirtuke Sąmatos** **pasirinkite** **mygtuką Naujinti kainas,** kad pamatytumėte atnaujintą kainodarą ir (arba) įkainojimas, atsirandančius dėl sprendimo subrangos sutartis. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subrangos sutartis su neįjungtu projekto komandos nariu
**Komandos nario išsamios informacijos puslapyje yra** subrangos ir subrangos eilučių laukai, leidžiantys projekto vadovui išreikšti, kaip jie norėtų pasinaudoti subrangos pajėgumais. Norėdami subrangos sutartis projekto komandos narį laikyti bendruoju ištekliumi, atlikite šiuos veiksmus:

1.  Komandos nario išsamios informacijos puslapyje pasirinkite **subrangą.**

2.  Galite pasirinkti tik subrangovus, kurių **būsena Juodraštis** arba **Patvirtinta**. **Negalima** **pasirinkti uždarytų arba atšauktų** subrangovų. 

3.  **Subrangos eilutės** laukas tampa matomas pasirinkus subrangos sutartis.

4.  Lauke **Subrangos** eilutėje galite pasirinkti tik laiko subrangos eilutes. Negalite pasirinkti išlaidų ar medžiagų subrangos eilučių.

5.  Projekto komandos nario įrašo vaidmuo turi atitikti subrangos eilutės vaidmenį. Tai užtikrina, kad projekto metu atliekamas vaidmuo yra tas pats vaidmuo, kuris perkamas subrangos linijoje. 

Kai bendrosios komandos narys susietas su subrangos ir subrangos eilute, **bendrosios komandos nario eilutės laukas Darbuotojo tipas bus** atnaujintas į Sutarties darbuotojo **ir** **subrangos galiojimas** bus nustatytas kaip **Galiojantis**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subrangos sutartis su projekto komandos nariu
Kaip ir bendrieji ar ne darbuotojai, projekte reikalingi komandos narių gebėjimai taip pat gali būti susieti su subrangos sutartis. Norėdami subrangos sutartis su įvardytu projekto komandos nariu, atlikite šiuos veiksmus:

1.  Įsitikinkite, kad nurodytas išteklius nustatytas kaip rezervuojamų išteklių sutarties darbuotojo tipas. Be to, įsitikinkite, kad **rezervuojamo** ištekliaus laukas Tiekėjas atitinka pasirinktinos subrangos tiekėją. 

2.  Subrangos sutartis galite pasirinkti tik **būsenoje Juodraštis** arba **Patvirtinta**. **Negalima** **pasirinkti uždarytų arba atšauktų** subrangovų. 

3.  **Subrangos eilutės** laukas tampa matomas pasirinkus subrangos sutartis.

4.  Lauke **Subrangos** eilutėje galite pasirinkti tik laiko subrangos eilutes. Negalite pasirinkti išlaidų ar medžiagų subrangos eilučių.

5.  Projekto komandos nario įrašo vaidmuo turi atitikti subrangos eilutės vaidmenį. Tai užtikrina, kad projekto metu atliekamas vaidmuo yra tas pats vaidmuo, kuris perkamas subrangos linijoje. 

Įvardyti projekto komandos nariai, nustatyti kaip užsakytų išteklių sutarties darbuotojo **tipas**, bus rodomi su subrangos galiojimo būsena, kuri **negalioja**, jei jie nėra susieti su subrangos sutartimi. Kai nurodytas projekto komandos narys susietas su subrangos ir subrangos eilute, **komandos nario eilutės laukas Darbuotojo tipas bus** atnaujintas į Sutarties darbuotojas **ir** **subrangos galiojimas** bus nustatytas kaip **Galiojantis**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
