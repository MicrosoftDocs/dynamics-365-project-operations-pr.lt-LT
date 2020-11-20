---
title: Kas nauja arba pakeista „Project Service Automation“ V3 22 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 22 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: badd87a276d68d9959e9cca4220daf61ed570638
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080784"
---
# <a name="project-service-automation-update-release-22-v3"></a>„Project Service Automation“ V3 22 naujinimo leidimas

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 22 atnaujintame leidime. Šios versijos komponavimo versijos numeris yra V 3.10.33.48 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. birželio mėn.

## <a name="update-release-22"></a>22 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos



**Laikas ir išlaidos**

Buvo pataisytos šios problemos:

- **Laiko įrašai** po importavimo nėra automatiškai įtraukiami į laiko įrašų grafiką.
- **Laiko įrašo** tinklelio datos parinkiklis neatpažįsta vartotojo regioninių parametrų.

**Išteklių valdymas**

Buvo pataisytos šios problemos:

- Veikiant rankiniam režimui, pakeitimai į **Išteklių priskyrimo** kontūrus nepripažįstami, kai generuojami **Išteklių reikalavimai**.
- **Išteklių užklausos** nepalaiko pasirinktinių užklausų būsenų.

**Projektų valdymas**

Buvo pataisytos šios problemos:

- Du kartus spustelėjus „EstimateGridControl“, olandiško formato skaičiai nebus tinkamai išanalizuoti.
- Priskirtos valandos nėra tinkamai atnaujinamos, kai priskyrimai pakeičiami naudojant „Microsoft Project“ stalinio kompiuterio papildinį.
- Projektų stebėjimo ir įvertinimo tinkleliuose rodomas neteisingas pardavimo valiutos kodas, kai sutarties valiuta skiriasi nuo kliento valiutos ir organizacija sukonfigūruota taip, kad būtų rodomi valiutos kodai, o ne valiutos simboliai.
- Prie komandos nario pabaigos datos bus pridėta viena diena, jei darbo valandų grafikas yra 24 valandos per dieną.
- Projekto grafike įtraukus operacijų kategoriją į užduotį, automatinis įrašymas nėra aktyvuojamas.
- Į projekto šabloną įtraukiant komandos narį, parodoma ši klaida: „Išteklių reikalavimų negalima susieti su projekto šablonais“. 
- Juostelės taisyklės scenarijus „msdyn.Approval.CanApproveOrReject“ parodo skirtojo laiko klaidą.

**„Sales“**

Buvo pataisytos šios problemos:

- Tikrinimo klaidos pranešimas nerodomas, kai formos / objekto „Naujo pasiūlymo projektų kainoraštis“ kainoraščio peržvalgoje pasirenkamas savikainos kainoraštis.
- Uždarius pasiūlymą kaip laimėtą, nėra pereinama į sukurtą sutartį, jei prie pasiūlymo pridėtas BPF yra galutiniame etape.
- Atšaukiant **Pardavimą, už kurį neišrašyta sąskaita** susiejama su originalia savikaina, kai laiko įrašas atšaukiamas.
- Paspaudus mygtuką **Patvirtinti** , sąskaitos faktūros būsena nepakeičiama į **Patvirtinta** , nebent sąskaita faktūra yra atnaujinama.