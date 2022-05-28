---
title: Subrangos projekto komandos narių parinktys
description: Šioje temoje paaiškinamos projekto komandos narių subrangos parinktys programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: aacd2f97d3120a854c78fe87e512fad1c43b9651
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600200"
---
# <a name="subcontracting-options-for-project-team-members"></a>Subrangos projekto komandos narių parinktys

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Programoje "Microsoft" Dynamics 365 Project Operations galite įvertinti subrangos parinktis, prieinamas vienam ar keliems projekto komandos nariams. Galimos subrangos parinktys leidžia:

- Sukurkite naują subrangos sutartį ir (arba) sukurkite naujas eilutes esamoje pasirinkto projekto komandos narių subrangos sutartyje. 
- Rezervuokite pagal jau esamą subrangos ir subrangos liniją. 

Galite pasirinkti iš galimų bendrosios projekto komandos narių subrangos parinkčių arba pasirinkti iš projekto komandos narių, kuriuose dirbo įvardytas išteklius, kuris yra sutartininkas. 

Subrangos parinkčių nėra:

- Projekto komandos nariai, kuriuose dirbo darbuotojas. 
- Projekto komandos nariai, kurie jau susieti su subrangos ir subrangos eilute. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Subrangos sutartis su nekvalifikuotu projekto komandos nariu

Norėdami peržiūrėti ir pasirinkti iš galimų bendrosios arba neturinčios darbuotojų projekto komandos nario subrangos parinkčių, atlikite šiuos veiksmus:

1. Pasirinkite vieną ar daugiau projekto komandos narių įrašų, kuriuose išteklius yra bendrasis išteklius.
2. Įsitikinkite, kad nė vienas iš pasirinktų projekto komandos narių įrašų dar nėra sudaręs subrangos sutarčių. 
3. Projekto komandos narių potinklyje pasirinkite **subrangos parinktis**. Atidaromas **dialogo langas Subrangos parinktys**. 
4. Jei atlikdami 1 veiksmą pasirinkote tik vieną projekto komandos nario įrašą, bus galimos šios parinktys:
    - Kurti naujas subrangos eilutes. 
    - Rezervuoti pagal esamą subrangos sutartį Jei atlikdami 1 veiksmą pasirinkote kelis projekto komandos narių įrašus, vienintelė galima pasirinktis yra sukurti naujas subrangos eilutes.
5. Galimybė rezervuoti pagal esamą subrangos eilutę leidžia pasirinkti subrangos ir subrangos eilutę, pagal kurią norite rezervuoti. Pasirinkdami subrangos eilutę pajėgumams rezervuoti, turėtumėte įsitikinti, kad pasirinkta subrangos eilutė yra skirta laikui ir kad projekto komandos nariui reikalingas vaidmuo atitinka subrangos eilutėje įsigytą vaidmenį.
6. Kai pasirenkate kurti naujas subrangos eilutes projekto komandos nariams, sistema leis pasirinkti subrangos sutartį, kurią norite sukurti šioms eilutėms. Subrangos sutartis, kurią pasirinkote naujoms eilutėms kurti, turi būti **juodraščio** būsena. Pasirinkus šią parinktį sukurti naujas subrangos eilutes pasirinktiems projekto komandos nariams, sistema sukurs vieną subrangos eilutę kiekvienam projekto komandos nariui. Vaidmuo, valandos ir datos bus nukopijuotos iš projekto komandos nario į kiekvieną sukurtą subrangos eilutę. 
7. Kai generinis komandos narys yra susietas su subrangos ir subrangos eilute, **bendrosios komandos nario eilutės laukas Darbuotojo tipas** bus atnaujintas į **Sutartininkas**, o **antrinės sutarties galiojimo** vertė bus nustatyta kaip **Galiojanti**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Subrangos sutartis su personalo projekto komandos nariu

Kaip ir bendriniai arba nedirbantys komandos nariai, taip pat galite peržiūrėti personalo projekto komandos nario subrangos galimybes, jei personalo komandos narys yra sutartininkas. Norėdami peržiūrėti ir pasirinkti iš galimų darbuotojų arba įvardyto projekto komandos nario subrangos parinkčių, atlikite šiuos veiksmus:

1. Pasirinkite vieną ar daugiau projekto komandos narių įrašų, kuriuose išteklius yra pavadintas sutartininkas.
2. Įsitikinkite, kad nė vienas iš pasirinktų projekto komandos narių įrašų dar nėra sudaręs subrangos sutarčių. 
3. Projekto komandos narių potinklyje pasirinkite **subrangos parinktis**. Atidaromas **dialogo langas Subrangos parinktys**. 
4. Jei atlikdami 1 veiksmą pasirinkote tik vieną projekto komandos nario įrašą, bus galimos šios parinktys:
      - Kurti naujas subrangos eilutes.
      - Rezervuokite pagal esamą subrangos sutartį.
  Jei atlikdami 1 veiksmą pasirinkote kelis projekto komandos narių įrašus, vienintelė galima pasirinktis yra sukurti naujas subrangos eilutes.
5. Galimybė rezervuoti pagal esamą subrangos eilutę leidžia pasirinkti subrangos ir subrangos eilutę, pagal kurią norite rezervuoti. Pasirinkdami subrangos eilutę pajėgumams rezervuoti, turėtumėte užtikrinti:
      - Pasirinkta subrangos eilutė skirta laikui. 
      - Projekto komandos nariui reikalingas vaidmuo atitinka vaidmenį, įsigytą subrangos eilutėje. 
      - Tiekėjas, su kuriuo susietas sutarties darbuotojas, yra toks pat kaip subrangos sutarties tiekėjas.
6. Kai pasirenkate kurti naujas subrangos eilutes projekto komandos nariams, sistema leis pasirinkti subrangos sutartį, kurią norite sukurti šioms eilutėms. Naudodami šią pasirinktį turėtumėte užtikrinti, kad tiekėjas, kuriam priklauso sutartininkas, būtų toks pat kaip ir subrangos sutarties tiekėjas. 
7. Subrangos sutartis, kurią pasirinkote naujoms eilutėms kurti, turi būti **juodraščio** būsena. Pasirinkus šią parinktį sukurti naujas subrangos eilutes pasirinktiems projekto komandos nariams, sistema sukurs vieną subrangos eilutę kiekvienam projekto komandos nariui. Vaidmuo, valandos ir datos bus nukopijuotos iš projekto komandos nario į kiekvieną sukurtą subrangos eilutę.  
8. Kai įvardytas komandos narys yra susietas su subrangos ir subrangos eilute, **įvardytos komandos nario eilutės laukas Darbuotojo tipas** bus atnaujintas į **Sutartininkas**, o **antrinės sutarties galiojimo** vertė bus nustatyta kaip **Galiojanti**.

## <a name="re-costing-subcontractor-assignments"></a>Subrangovų priskyrimų perskaičiavimas

Kai projekto komandos narys (bendrasis arba pavadintasis) yra susietas su subrangos eilutėmis naudodamas dialogo langą **Subrangos parinktys**, bet kokie priskyrimai užduotims, kurias turi komandos narys, bus perskaičiuoti pagal pirkimo kainoraštį, pridėtą prie subrangos sutarties. **Puslapio Išsami projekto informacija** skirtuke **Įvertinimai** pasirinkite mygtuką Atnaujinti kainas **, kad pamatytumėte** atnaujintą kainodarą ir (arba) įkainojimą, atsirandančius dėl sprendimo sudaryti subrangos sutartis.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
