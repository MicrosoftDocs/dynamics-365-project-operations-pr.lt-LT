---
title: Subrangos išteklių priskyrimų išlaidų vertinimas
description: Šioje temoje paaiškinama, kaip "Microsoft" Dynamics 365 Project Operations apskaičiuoja subrangovų išteklių priskyrimų išlaidų įvertinimą.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f276e12713261538d1e7520dac17243e578db433
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596704"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Subrangos išteklių priskyrimų išlaidų vertinimas

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Subrangos projekto komandos narių užduočių priskyrimai įkainojami naudojant pirkimo **kainoraštį**, pridėtą prie susijusio komandos nario įrašo subrangos sutarties. Tai skiriasi nuo to, kaip įkainojami darbuotojų išteklių priskyrimai, kai darbuotojų išteklių užduočių priskyrimai įkainojami naudojant **išlaidų** kainoraštį, pridėtą prie projekto perkančiojo vieneto. 

Bendriesiems projekto komandos nariams, sudariusiems subrangos sutartis, priskyrimai įkainojami naudojant vaidmenimis pagrįstą kainos nustatymą pirkimo kainoraštyje, pridėtame prie subrangos sutarties. Pirkimo kainos taip pat gali būti nustatytos specialiai kiekvienam ištekliui. Šioms su ištekliais susijusioms kainoms bus teikiamas prioritetas, kai įvardytų projekto komandos narių užduočių užduotys yra sutartininkai. 

Konkretaus vaidmens pirkimo kainos, palyginti su konkrečiais ištekliais, naudojimo prioritetą lemia kainodaros dimensijos prioriteto nustatymas parametruose **> suma pagrįstų kainodaros dimensijų**.

Ši dinamiškai gaunamų kainų funkcija, pagrįsta subrangovų pirkimo kainų dimensijų nustatymu, yra panaši į tai, kaip gaunami visą darbo dieną dirbančių darbuotojų išlaidų ir sąskaitų tarifai. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Užduočių priskyrimų kūrimas subrangovo išteklių išlaidų sąmatoms gauti

Užduočių priskyrimus subrangovams galima sukurti dviem būdais: 
- Skirtuko **Užduotys** naudojimas.
- Skirtuko **Komanda** naudojimas.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Išteklių priskyrimų kūrimas naudojant skirtuką Užduotys
**Naudodami konkrečios užduoties skirtuko** Užduotys **sąrašą Ištekliai**, galite sukurti įvardyto ištekliaus arba bendrojo ištekliaus užduoties priskyrimą. Jei pasirinksite įvardytą išteklių iš **užduoties išplečiamojo sąrašo Priskirti ištekliai** ir šis išteklius bus sutartininkas, įvardytas išteklius bus priskirtas užduočiai ir bus sukurtas atitinkamas projekto komandos nario įrašas, kurio darbuotojo tipas nustatytas kaip **Sutartininkas**, o **galiojimas** nustatytas kaip **Neleistinas**. Atlikdami kitą veiksmą turėsite atidaryti projekto komandos nario įrašą ir pasirinkti subrangos ir subrangos eilutę. Tai atnaujins užduoties priskyrimą, kad būtų nuoroda į subrangos ir subrangos eilutę, taip pat atnaujins komandos nario būseną į **Galiojanti**.

Jei pasirinksite sukurti bendrąjį komandos narį iš **užduoties išplečiamojo sąrašo Priskirti ištekliai**, **dialogo langas Bendrieji komandos narių kūrimas** leis pasirinkti subrangos ir subrangos eilutę. Kai bendrasis išteklius priskiriamas užduočiai ir sukuriamas atitinkamas projekto komandos nario įrašas, pastebėsite, kad projekto komandos nario įrašas sukuriamas, kai darbuotojo tipas nustatytas kaip **Sutartininkas** ir **galiojimas**, nustatytas kaip **Galiojantis**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projekto komandos narių kūrimas naudojant skirtuką Komanda
Naudodami projekto skirtuką Komanda, galite sukurti bendrąjį arba įvardytą komandos narį. Kurdami komandos narį, galite pasirinkti subrangos ir subrangos eilutę. Sukūrę komandos narį, turėsite priskirti komandos narį užduočiai naudodami **užduoties išplečiamąjį sąrašą Priskirti ištekliai**. 

## <a name="updating-estimates"></a>Įvertinimų naujinimas
Priskyrę projekto komandos narius užduotims, turėsite pereiti į **projekto skirtuką Įvertinimai** ir pasirinkti **Naujinti kainas**, kad užtikrintumėte, jog subrangovo išteklių priskyrimų išlaidų tarifai atnaujinami pagal pirkimo kainoraštį, pridėtą prie subrangos sutarties. Programoje Microsoft Dynamics 365 Project Operations nesugeneruojami nepriskirtų užduočių įvertinimai. Dėl to turėsite sukurti užduočių priskyrimus, kad galėtumėte įkainoti ir kainuoti įvairias projekto užduotis. 

> [PASTABA!] Projekto komandos nariai, kurių **darbuotojo tipas** **yra Sutartininkas**, bet neturi subrangos nuorodos, projekto komandos narių **tinklelyje pažymėti kaip** Neleistini **·**. Jei yra projekto komandos narių, turinčių šią būseną, atidarykite projekto komandos nario įrašą ir rankiniu būdu atnaujinkite subrangos ir subrangos eilučių laukus, kad finansinių išlaidų įvertinimas tiksliai atspindėtų subrangovo savikainą **skirtuke Įvertinimai**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
