---
title: Subrangos išteklių priskyrimų išlaidų vertinimas
description: Šiame straipsnyje paaiškinta, kaip „Microsoft Dynamics 365 Project Operations“ apskaičiuoja subrangos išteklių priskyrimų išlaidų vertinimą.
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

Subrangos projekto komandos narių užduočių priskyrimai įkainojami naudojant **Pirkimo** kainoraštį, pridėtą prie subrangos sutarties, esančios atitinkamame komandos nario įraše. Tai skiriasi nuo to, kaip įkainojami darbuotojų išteklių priskyrimai, kai darbuotojų išteklių užduočių priskyrimai įkainojami naudojant **Savikainos** kainoraštį, pridėtą prie projekto sutartį sudarančio vieneto. 

Subrangos bendrųjų komandos narių priskyrimai įkainojami naudojant vaidmenimis pagrįstą kainą, nustatytą pirkimo kainoraštyje, pridėtame prie subrangos sutarties. Taip pat galima nustatyti kiekvieno konkretaus ištekliaus pirkimo kainas. Šioms konkrečių išteklių kainoms bus teikiama pirmenybė, kai bus įkainojami nurodytų projekto komandos narių, kurie yra pagal sutartis dirbantys darbuotojai, užduočių priskyrimai. 

Pirmenybė naudoti konkrečių vaidmenų pirkimo kainą arba konkrečių išteklių suteikiama pagal įkainių dimensijos prioritetą, nustatytą **Parametrai >Suma pagrįstos kainodaros dimensijos**.

Ši dinamiškai gaunamų kainų funkcija, kai kainos gaunamos remiantis subrangovų pirkimo kainų dimensijos nustatymu, yra panaši į tai, kaip gaunami visą dieną dirbančių darbuotojų savikainos ir sąskaitų tarifai. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Užduočių priskyrimų kūrimas, norint gauti subrangovų išteklių savikainos įvertinimus

Rangovų užduočių priskyrimus galima sukurti dviem būdais: 
- Naudojant skirtuką **Užduotys**.
- Naudojant skirtuką **Komanda**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Išteklių priskyrimų kūrimas naudojant skirtuką Užduotys
Konkrečiai užduočiai naudodami sąrašą **Ištekliai**, esantį skirtuke **Užduotys**, galite sukurti užduoties priskyrimą įvardytajam ištekliui arba bendrajam ištekliui. Jei užduoties išplečiamajame sąraše **Priskirti ištekliai** pasirinksite įvardytąjį išteklių ir jis bus pagal sutartį dirbantis darbuotojas, tas įvardytasis išteklius bus priskirtas užduočiai ir bus sukurtas atitinkamas projekto komandos nario įrašas, kuriame darbuotojo tipas bus nustatytas kaip **Pagal sutartį dirbantis darbuotojas**, o **Galiojimas** – kaip **Negalioja**. Kitas veiksmas – turėsite atidaryti projekto komandos nario įrašą ir pasirinkti subrangos sutartį ir subrangos sutarties eilutę. Tokiu atveju bus atnaujintas užduoties priskyrimas, kad būtų nuoroda į subrangos sutartį ir subrangos sutarties eilutę, o komandos nario būseną bus atnaujinta į **Galioja**.

Jei užduoties išplečiamajame sąraše **Priskirti ištekliai** pasirinksite kurti bendrąjį komandos narį, dialogo lange **Bendrojo komandos nario kūrimas** galėsite pasirinkti subrangos sutartį ir subrangos sutarties eilutę. Kai užduočiai bus priskirtas bendrasis išteklius ir sukurtas atitinkamas projekto komandos nario įrašas, pastebėsite, kad projekto komandos nario įrašas sukuriamas nustatant darbuotojo tipą kaip **Pagal sutartį dirbantis darbuotojas**, o **Galiojimas** nustatant kaip **Galioja**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projekto komandos narių kūrimas naudojant skirtuką Komanda
Projekto skirtuke Komanda galite sukurti bendrąjį arba įvardintąjį komandos narį. Kurdami komandos narį, galite pasirinkti subrangos sutartį ir subrangos sutarties eilutę. Kai komandos narys bus sukurtas, turėsite jį priskirti užduočiai naudodami išplečiamąjį sąrašą **Priskirti ištekliai**. 

## <a name="updating-estimates"></a>Įvertinimų atnaujinimas
Kai projekto komandos narius priskirsite užduotims, turėsite pereiti į projekto skirtuką **Įvertinimai** ir pasirinkti **Atnaujinti kainas**, kad užtikrintumėte, jog subrangovo išteklių priskyrimų savikainos tarifai būtų atnaujinti pagal pirkimo kainoraštį, pridėtą prie subrangos sutarties. Programoje „Microsoft Dynamics 365 Project Operations“ nepriskirtų užduočių įvertinimai negeneruojami. Todėl turėsite sukurti užduočių priskyrimus, kad būtų nustatyta įvairių projekto užduočių kainai ir savikaina. 

> [PASTABA!] Projekto komandos nariai, kurių **Darbuotojo tipas** yra **Pagal sutartį dirbantis darbuotojas**, bet jie neturi subrangos sutarties nuorodos, tinklelyje **Projekto komandos nariai** pažymimi kaip **Negalioja**. Jei yra projekto komandos narių, kurių būsena tokia, atidarykite tokio projekto komandos nario įrašą ir rankiniu būdu atnaujinkite subrangos sutarties ir subrangos sutarties eilutės laukus, kad finansinių išlaidų įvertinimas tiksliai atspindėtų subrangovo išlaidas skirtuke **Įvertinimai**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
