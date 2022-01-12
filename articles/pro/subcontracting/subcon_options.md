---
title: Projekto komandos narių subrangos parinktys
description: Šioje temoje paaiškinamos "Microsoft" projekto komandos narių subrangos parinktys Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4db283db728b50ccf76eafabfd643313620bbce2
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903062"
---
# <a name="subcontracting-options-for-project-team-members"></a>Projekto komandos narių subrangos parinktys

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Programoje Microsoft Dynamics 365 Project Operations galite įvertinti subrangos parinktis, prieinamas vienam ar daugiau projekto komandos narių. Galimos subrangos parinktys leidžia:

- Sukurkite naują subrangą ir (arba) sukurkite naujas eilutes esamoje pasirinktų projekto komandos narių subrangoje. 
- Rezervuoti jau egzistuojančiai subrangos ir subrangos linijai. 

Galite pasirinkti iš galimų generinių projekto komandos narių subrangos parinkčių arba pasirinkti iš projekto komandos narių, kuriuose dirbo įvardytas išteklius, kuris yra sutartininkas. 

Nėra subrangos parinkčių, skirtų:

- Projekto komandos nariai, kuriuose dirbo darbuotojas. 
- Projekto komandos nariai, kurie jau susieti su subrangos ir subrangos linija. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subrangos sutartis su neįjungtu projekto komandos nariu

Norėdami peržiūrėti ir pasirinkti iš galimų bendrosios arba neprijungto projekto komandos nario subrangos parinkčių, atlikite šiuos veiksmus:

1. Pasirinkite vieną ar daugiau projekto komandos narių įrašų, kuriuose išteklius yra bendrasis išteklius.
2. Įsitikinkite, kad nė vienas iš pasirinktų projekto komandos narių įrašų dar nėra subrangos sutartis. 
3. Projekto komandos narių sublyte pasirinkite **Subrangos** pasirinktys. **Atidaromas dialogo langas Subrangos** pasirinktys. 
4. Jei 1 veiksme pasirinkote tik vieną projekto komandos nario įrašą, bus galimos šios parinktys:
    - Kurti naujas subrangos eilutes. 
    - Rezervuoti esamoje subrangovoje Jei 1 žingsnyje pasirinkote kelis projekto komandos narių įrašus, vienintelė galima pasirinkti yra sukurti naujas subrangos eilutes.
5. Galimybė rezervuoti pagal esamą subrangos eilutę leidžia pasirinkti subrangos ir subrangos liniją, pagal kurią norite rezervuoti. Pasirinkdami subrangos eilutę pajėgumams rezervuoti, turėtumėte užtikrinti, kad pasirinkta subrangos eilutė būtų skirta laikui ir kad projekto komandos nariui reikalingas vaidmuo atitiktų subrangos eilutėje įsigytą vaidmenį.
6. Kai pasirinksite kurti naujas projekto komandos narių subrangos eilutes, sistema leis pasirinkti subrangą, kurią norite sukurti šias eilutes. Subrangos sutartis, kurią pasirinkote naujoms eilutėms kurti, turi būti **juodraščio** būsenoje. Pasirinkus šią parinktį sukurti naujas subrangos eilutes pasirinktiems projekto komandos nariams, sistema kiekvienam projekto komandos nariui sukurs vieną subrangos eilutę. Vaidmuo, valandos ir datos bus nukopijuotos iš projekto komandos nario į kiekvieną sukurtą subrangos eilutę. 
7. Kai bendrosios komandos narys susietas su subrangos ir subrangos eilute, **bendrosios komandos nario eilutės laukas Darbuotojo tipas bus** atnaujintas į Sutarties **darbuotojas**, o **subrangos galiojimo** vertė bus nustatyta kaip **Galiojanti**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subrangos sutartis su projekto komandos nariu

Kaip ir bendrieji arba neprijungti komandos nariai, taip pat galite peržiūrėti projekto komandos nario subrangos parinktis, jei darbuotojas yra sutartininkas. Norėdami peržiūrėti ir pasirinkti iš galimų darbuotojų arba įvardyto projekto komandos nario subrangos parinkčių, atlikite šiuos veiksmus:

1. Pasirinkite vieną ar daugiau projekto komandos narių įrašų, kuriuose išteklius yra pavadintas sutarties darbuotojas.
2. Įsitikinkite, kad nė vienas iš pasirinktų projekto komandos narių įrašų jau nėra subrangos sutartis. 
3. Projekto komandos narių sublyte pasirinkite **Subrangos** pasirinktys. **Atidaromas dialogo langas Subrangos** pasirinktys. 
4. Jei 1 veiksme pasirinkote tik vieną projekto komandos nario įrašą, bus galimos šios parinktys:
      - Kurti naujas subrangos eilutes.
      - Rezervas esamai subrangai.
  Jei 1 žingsnyje pasirinkote kelis projekto komandos narių įrašus, vienintelė galima pasirinkti yra sukurti naujas subrangos eilutes.
5. Galimybė rezervuoti pagal esamą subrangos eilutę leidžia pasirinkti subrangos ir subrangos liniją, pagal kurią norite rezervuoti. Renkantis subrangos liniją pajėgumams rezervuoti, turėtumėte užtikrinti:
      - Pasirinkta subrangos eilutė skirta laikui. 
      - Projekto komandos nariui reikalingas vaidmuo atitinka vaidmenį, įsigytą subrangos eilutėje. 
      - Tiekėjas, su kuriuo susietas sutarties darbuotojas, yra toks pat kaip ir subrangos tiekėjas.
6. Kai pasirinksite kurti naujas projekto komandos narių subrangos eilutes, sistema leis pasirinkti subrangą, kurią norite sukurti šias eilutes. Naudodami šią pasirinktį turėtumėte užtikrinti, kad tiekėjas, kuriam priklauso sutarties darbuotojas, būtų toks pat kaip ir subrangos tiekėjas. 
7. Subrangos sutartis, kurią pasirinkote naujoms eilutėms kurti, turi būti **juodraščio** būsenoje. Pasirinkus šią parinktį sukurti naujas subrangos eilutes pasirinktiems projekto komandos nariams, sistema kiekvienam projekto komandos nariui sukurs vieną subrangos eilutę. Vaidmuo, valandos ir datos bus nukopijuotos iš projekto komandos nario į kiekvieną sukurtą subrangos eilutę.  
8. Kai nurodytas komandos narys susietas su subrangos ir subrangos eilute, **nurodytas komandos nario eilutės laukas Darbuotojo tipas bus** atnaujintas į Sutarties **darbuotojas**, o **subrangos galiojimo** reikšmė bus nustatyta kaip **Galiojanti**.

## <a name="re-costing-subcontractor-assignments"></a>Pakartotiniai subrangovo priskyrimai

Kai projekto komandos narys (bendrinis arba pavadintas) yra susietas su subrangos eilutėmis, naudojant **antrinėsrangos parinkčių** dialogą, visi komandos nario užduočių priskyrimai bus iš naujo įkainoti pagal pirkimo kainoraštį, pridėtą prie subrangos. Puslapio **Išsami projekto informacija skirtuke Sąmatos** **pasirinkite** **mygtuką Naujinti kainas,** kad pamatytumėte atnaujintą kainodarą ir (arba) įkainojimas, atsirandančius dėl sprendimo subrangos sutartis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
