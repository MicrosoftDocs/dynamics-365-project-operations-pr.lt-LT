---
title: Subrangos išteklių priskyrimų išlaidų įvertinimas
description: Šioje temoje paaiškinama, kaip "Microsoft" Dynamics 365 Project Operations apskaičiuoja subrangos išteklių priskyrimų išlaidų įvertinimą.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 09a2a86ea0e97376939d5bff6df9177747818ebb
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903719"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Subrangos išteklių priskyrimų išlaidų įvertinimas

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Subrangos projekto komandos narių užduočių priskyrimai kainuoja naudojant **pirkimo** kainoraštį, pridėtą prie subrangos, pateikto susijusiame komandos nario įraše. Tai skiriasi nuo to, kaip kainuoja darbuotojų išteklių priskyrimai, kai įsodūsi darbuotojų išteklių užduočių priskyrimai naudojant **išlaidų** kainoraštį, pridėtą prie projekto perkančiojo vieneto. 

Subrangos generinių projekto komandos narių užduotys kainuojamos naudojant vaidmenimis pagrįstą kainos nustatymą pirkimo kainoraštyje, pridėtame prie subrangos. Pirkimo kainos taip pat gali būti nustatytos specialiai kiekvienam ištekliui. Šioms ištekliams būdingoms kainoms bus teikiama pirmenybė, kai įvardytų projekto komandos narių įkainotų užduočių priskyrimai yra sutartininkai. 

Prioritetą naudoti konkrečiai vaidmeniui būdingą pirkimo kainą, palyginti su konkrečiais ištekliais, lemia kainodaros dimensijos prioriteto nustatymas **parametruose > suma pagrįstomis kainodaros dimensijomis**.

Ši dinamiškai gaunamų kainų funkcija, pagrįsta subrangovų pirkimo kainų dimensijų nustatymu, yra panaši į tai, kaip visą darbo dieną dirbantiems darbuotojams gaunami išlaidų ir sąskaitų tarifai. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Užduočių priskyrimų kūrimas subrangovo išteklių išlaidų įvertinimams gauti

Subrangovų užduočių priskyrimai gali būti sukurti dviem būdais: 
- Skirtuko **Užduotys** naudojimas.
- Skirtuko **Komanda** naudojimas.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Išteklių priskyrimų kūrimas naudojant skirtuką Užduotys
Naudodami **konkrečios** užduoties skirtuko Užduotys sąrašą **Ištekliai**, galite sukurti pavadinto ištekliaus arba bendrojo ištekliaus užduoties priskyrimą. Jei pavadintą išteklių pasirinksite iš **užduoties išplečiamojo įvado Priskirti ištekliai** ir šis išteklius yra sutarties darbuotojas, nurodytas išteklius bus priskirtas užduočiai ir sukuriamas atitinkamas projekto komandos nario įrašas, kurio darbuotojo tipas nustatytas kaip **Sutarties** darbuotojas, o **galiojimas nustatytas kaip** **neleistinas**. Kaip kitą veiksmą turėsite atidaryti projekto komandos nario įrašą ir pasirinkti subrangos ir subrangos liniją. Tai atnaujins užduoties priskyrimą, kad jis turėtų nuorodą į subrangos ir subrangos eilutę, taip pat atnaujins komandos nario būseną į **Galiojanti**.

Jei pasirinksite kurti bendruosius komandos narius iš **užduoties išplečiamojo įdaryto kategorijoje Priskirti** ištekliai, **dialogo langas Bendrieji komandos nario kūrimas** leis pasirinkti subrangos ir subrangos eilutę. Kai bendram ištekliui priskiriama užduotis ir sukuriamas atitinkamas projekto komandos nario įrašas, pastebėsite, kad projekto komandos nario įrašas sukuriamas darbuotojo tipu, nustatytu **kaip Sutarties** darbuotojas, o **galiojimas nustatytas kaip** **Galiojantis**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projekto komandos narių kūrimas naudojant skirtuką Komanda
Naudodami projekto skirtuką Komanda galite sukurti bendrąjį arba pavadintą komandos narį. Kurdami komandos narį galite pasirinkti subrangos ir subrangos eilutę. Sukūrę komandos narį, turėsite priskirti komandos narį užduočiai naudodami **užduoties** išplečiamąjįmąjį palikusį išteklius. 

## <a name="updating-estimates"></a>Įvertinimų atnaujinimas
Priskynę projekto komandos narius užduotims, turėsite pereiti į **projekto skirtuką Sąmatos** ir pasirinkti **Naujinti** kainas, kad įsitikintumėte, jog subrangovo išteklių priskyrimų savikainos tarifai atnaujinami pagal pirkimo kainoraštį, pridėtą prie subrangos sutarties. Microsoft nepriskirtų užduočių įvertinimai nesukuriami Dynamics 365 Project Operations. Dėl to turėsite sukurti užduočių priskyrimus kainai ir įvairioms projekto užduotims. 

> [PASTABA!] Projekto komandos nariai, kurių **darbuotojo tipas yra sutarties** **darbuotojas**, bet neturi subrangos nuorodos, **projekto komandos narių** **tinklelyje pažymėti kaip** neleistini. Jei yra projekto komandos narių, turinčių šią būseną, atidarykite projekto komandos nario įrašą ir neautomatiniu būdu atnaujinkite subrangos ir subrangos eilučių laukus, kad finansinių išlaidų įvertinimas tiksliai atspindėtų subrangovo išlaidas **skirtuke** Sąmatos. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
