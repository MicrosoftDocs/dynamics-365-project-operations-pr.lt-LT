---
title: Darbo paskirstymo struktūros atnaujinimo aptarimas
description: Šioje temoje pateikta informacija, kaip atnaujinti darbo paskirstymo struktūrą pereinant iš „Project Service Automation“ 2.x versijos į 3.x versiją.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x
author: ruhercul
ms.assetid: 9e43d5b5-ca5d-41f5-9012-c48f8e3080f9
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9aa35dd8784bfa55737b0836e653afd0442b80c2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753732"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Darbo paskirstymo struktūros atnaujinimo aptarimas
Šioje temoje pateikta informacija, kaip atnaujinti darbo paskirstymo struktūrą pereinant iš „Project Service Automation“ 2.x versijos į 3.x versiją. Šioje temoje apibūdinta tinkama „Project Service Automation“ (PSA) projekto būsena, kurios reikia norint sėkmingai atnaujinti. Taip pat pateikiama informacija apie įprastas blokavimo sąlygas, dėl kurių nepavyks atnaujinti. Daugiau informacijos apie projekto užduočių nustatymą ir jų funkcijas projekto grafike žr [Projekto grafikai](project-creating.md).

## <a name="key-entities"></a>Pagrindiniai objektai
Tiksliai darbo paskirstymo struktūrai, į kurią jau įkelta išteklių, reikia toliau nurodytų objektų:

- [Projektas](../developer/entities/msdyn_project.md)
- [Projekto komanda](../developer/entities/msdyn_projectteam.md)
- [Projekto užduotis](../developer/entities/msdyn_projecttask.md)
- [Išteklių priskyrimai](../developer/entities/msdyn_resourceassignment.md)
- [Projekto užduoties priklausomybė](../developer/entities/msdyn_projecttaskdependency.md)
- [Rezervuojami ištekliai](../developer/entities/bookableresource.md)

Jei norite nustatyti darbo paskirstymo struktūrą, į kurią įkelti ištekliai, turite atlikti šiuos veiksmus:

1. Kurti naują projektą Daugiau informacijos apie tai, kaip sukurti naują projektą, žr. [msdyn_project](../developer/entities/msdyn_project.md).
2. Sukurkite vieną ar kelias užduotis. Daugiau informacijos apie tai, kaip sukurti užduotį, žr. [msdyn_projecttask](../developer/entities/msdyn_projecttask.md).
3. Nustatykite užduočių priklausomybes. Daugiau informacijos žr. [Projekto užduoties priklausomybė](../developer/entities/msdyn_projecttaskdependency.md).
4. Priskirkite projekto komandos narius prie projekto. Daugiau informacijos žr. [msdyn_projectteam](../developer/entities/msdyn_projectteam.md).
5. Priskirkite projekto komandos narius užduotims. Daugiau informacijos žr. [msdyn_resourceassignment](../developer/entities/msdyn_resourceassignment.md).

## <a name="project-team-relationships"></a>Projekto komandos ryšiai

Norint užtikrinti sėkmingą atnaujinimą, reikia tinkamai išlaikyti šiuos ryšius:
- Visi projekto komandos nariai turi būti susieti su rezervuojamu ištekliumi.
- Visi projekto komandos nariai turi būti susieti su tuo pačiu projektu. 

## <a name="project-task-relationships"></a>Projekto užduočių ryšiai
Norint užtikrinti sėkmingą atnaujinimą, reikia tinkamai išlaikyti šiuos ryšius:

- Bet kokios susijusios užduotys turi būti susietos su tuo pačiu projektu.
- Kiekviena eilutės užduotis turi turėti pirminę užduotį.
- Kiekviena užduotis turi turėti pirminį projektą.

### <a name="valid-conditions"></a>Galiojimo sąlygos

- Visų užduočių trukmė turi būti didesnė arba lygi (>=) vienai valandai ir mažesnė nei 1 800 000 minučių (1 250 dienų).*
- Visų užduočių pradžios data turi būti ne ankstesnė nei 2000/01/01.*
- Visų užduočių pradžios data turi būti ne vėliau kaip 17 metų nuo dabartinės dienos.*
- Visų užduočių pradžios data turi būti ankstesnė nei pabaigos data arba jai lygi.
- Visų klasifikacijų operacijų tipai (išlaidos, medžiagos, mokestis ir laikas) turi turėti **Numatytojo vieneto** ir **Vienetų grupės** reikšmes.
- Reikia vengti datos formatų su raidėmis.

### <a name="potential-mitigation-steps"></a>Potencialūs sumažinimo veiksmai
- Naudodami išplėstinę iešką galite identifikuoti projekto užduotis, kurios neturi projekto ID.
- Naudodami išplėstinę iešką galite identifikuoti projekto užduotis, kurių suplanuota trukmė yra ilgesnė nei >1 800 000.
- Prieš keisdami duomenis, turite išanalizuoti visus tinkinimus, susijusius su objektu, dėl kurio gali suprastėti duomenų būsena. Šie tinkinimai turėtų būti išanalizuoti prieš pradedant bet kokius su duomenimis susijusius naujinimus.
- Jei identifikuotos užduotys yra pavienės, apsvarstykite šių užduočių panaikinimą, jei jų nereikia, arba ar jas reikia susieti su tinkamu pirminiu projektu.
- Jei užduočių trukmė yra ilgesnė nei 1250 dienos, apsvarstykite įtraukti kelias užduotis, kad būtų atspindėta bendra trukmė, jei įmanoma.

> [!NOTE]
> Elementai, pažymėti žvaigždute (\*), turi apribojimus, nes ryšių su klientais valdymas (CRM) palaiko tik 7 320 pasikartojimų išplėtimus. Negalima viršyti šio apribojimo.

## <a name="resource-assignment-relationships"></a>Išteklių priskyrimo ryšiai
Norint užtikrinti sėkmingą atnaujinimą, reikia tinkamai išlaikyti šiuos ryšius:

- Visi išteklių priskyrimai darbo paskirstymo struktūroje turi būti susiję su tuo pačiu projektu.
- Visi išteklių priskyrimai darbo paskirstymo struktūroje turi būti susieti su projekto komandos nariais tame pačiame projekte.

### <a name="potential-mitigation-steps"></a>Potencialūs sumažinimo veiksmai
- Identifikuokite visas užduotis, kurios nepatenkina pirmiau aprašytų sąlygų.  
- Reikia panaikinti visus išteklių priskyrimus, kurie nebegalioja.

## <a name="project-task-dependency-relationships"></a>Projekto užduoties priklausomybės ryšiai
Norint užtikrinti sėkmingą atnaujinimą, reikia tinkamai išlaikyti šiuos ryšius:

- Visos projekto užduočių priklausomybės turi būti susijusios su tuo pačiu projektu.
- Užduotyje ta pati priklausomybė negali būti nurodyta daugiau nei vieną kartą.
