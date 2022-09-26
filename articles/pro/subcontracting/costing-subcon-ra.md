---
title: Subrangos išteklių priskyrimų išlaidų vertinimas
description: Šiame straipsnyje paaiškinama, kaip "Microsoft" Dynamics 365 Project Operations apskaičiuoja subrangos būdu atliktų išteklių priskyrimų išlaidų įvertinimą.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522666"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Subrangos išteklių priskyrimų išlaidų vertinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Subrangovų projekto komandos narių užduočių priskyrimai įkainojami naudojant **pirkimo** kainoraštį, pridėtą prie subrangos sutarties, esantį susijusiame komandos nario įraše. Tai skiriasi nuo to, kaip įkainojami darbuotojų išteklių priskyrimai, kai darbuotojų išteklių užduočių priskyrimai įkainojami naudojant **išlaidų** kainoraštį, pridėtą prie projekto sutartinio vieneto. 

Bendrųjų projekto komandos narių, kurie yra subrangovai, priskyrimai įkainojami naudojant vaidmenimis pagrįstą kainos nustatymą pirkimo kainoraštyje, pridėtame prie subrangos sutarties. Pirkimo kainas taip pat galima nustatyti specialiai kiekvienam ištekliui. Šioms konkretaus ištekliaus kainoms bus teikiama pirmenybė, kai įvardytų projekto komandos narių, pagal sutartis dirbančių darbuotojų, užduočių priskyrimas bus įkainotas. 

Konkretaus vaidmens pirkimo kainos naudojimo prioritetas, palyginti su konkrečiais ištekliais, priklauso nuo kainodaros dimensijos prioriteto nustatymo parametruose **> suma pagrįstų kainodaros aspektų**.

Ši dinamiškai gaunamų kainų funkcija, pagrįsta subrangovų pirkimo kainų matmenų nustatymu, yra panaši į tai, kaip nustatomos visą darbo dieną dirbančių darbuotojų išlaidos ir sąskaitų tarifai. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Užduočių priskyrimų kūrimas subrangovų išteklių išlaidų sąmatoms gauti

Užduočių priskyrimus subrangovams galima sukurti dviem būdais: 
- Skirtuko **Užduotys** naudojimas.
- Skirtuko **Komanda** naudojimas.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Išteklių užduočių kūrimas naudojant skirtuką Užduotys
**Naudodami konkrečios užduoties skirtuke** Užduotys **esantį sąrašą Ištekliai**, galite sukurti įvardyto ištekliaus arba bendrojo ištekliaus užduoties priskyrimą. Jei pasirenkate įvardytą išteklių užduoties **išplečiamajame sąraše Priskirti ištekliai** ir šis išteklius yra sutartininkas, pavadintas išteklius priskiriamas užduočiai ir sukuriamas atitinkamas projekto komandos nario įrašas, kurio darbuotojo tipas nustatytas kaip **Sutartinis darbuotojas**, o **Galiojimas** nustatytas kaip **Neteisingas**. Atlikdami kitą veiksmą, turėsite atidaryti projekto komandos nario įrašą ir pasirinkti subrangos ir subrangos liniją. Tai atnaujins užduoties priskyrimą, kad būtų nuoroda į subrangos ir subrangos liniją, taip pat atnaujins komandos nario būseną į **Galiojanti**.

Jei pasirinksite sukurti bendrąjį komandos narį iš užduoties išplečiamojo sąrašo **Priskirti ištekliai**, **dialogo lange Bendrieji komandos nario kūrimas** galėsite pasirinkti subrangos ir subrangos liniją. Kai užduočiai priskiriamas bendrasis išteklius ir sukuriamas atitinkamas projekto komandos nario įrašas, pastebėsite, kad projekto komandos nario įrašas sukuriamas, kai darbuotojo tipas nustatytas kaip **Sutartinis darbuotojas**, o **Galiojimas** nustatytas kaip **Galiojantis**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projekto komandos narių kūrimas naudojant skirtuką Komanda
Naudodami projekto skirtuką Komanda, galite sukurti bendrinį arba pavadintą komandos narį. Kurdami komandos narį, galite pasirinkti subrangos ir subrangos liniją. Sukūrę komandos narį, turėsite priskirti komandos narį užduočiai naudodami **užduoties išplečiamąjį meniu Priskirti ištekliai**. 

## <a name="updating-estimates"></a>Sąmatų atnaujinimas
Priskyrę projekto komandos narius užduotims, turėsite pereiti į **projekto skirtuką Sąmatos ir pasirinkti** Naujinti kainas **, kad užtikrintumėte, jog subrangovų išteklių priskyrimų išlaidų tarifai būtų atnaujinti pagal pirkimo kainoraštį, pridėtą prie subrangos** sutarties. Įvertinimai negeneruojami nepriskirtoms užduotims programoje "Microsoft"Dynamics 365 Project Operations. Todėl turėsite sukurti užduočių priskyrimus, kad įkainotumėte ir įkainotumėte įvairias projekto užduotis. 

> [PASTABA!] Projekto komandos nariai, kurių darbuotojo tipas **yra** sutarties darbuotojas **,** bet neturi subrangos nuorodos, tinklelyje **"Project" komandos nariai** pažymėti kaip **netinkami**. Jei yra projekto komandos narių, turinčių šią būseną, atidarykite projekto komandos nario įrašą ir rankiniu būdu atnaujinkite subrangos ir subrangos linijos laukus, kad finansinių išlaidų sąmata tiksliai atspindėtų subrangovo išlaidas skirtuke **Sąmatos**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
