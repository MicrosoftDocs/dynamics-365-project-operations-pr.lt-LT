---
title: Projekto savikainos ir pajamų įvertinimų nustatymas
description: Projekto savikainos ir pajamų įvertinimų nustatymas „Project Service“
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 1652b39b6c8a703bf198a990eb9047eff9dc9f4c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080844"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Projekto savikainos ir pajamų įvertinimų nustatymas 

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projekto sąmatos pateikia projekto darbo paskirstymo struktūroje įvertinto ir suplanuoto darbo finansinį vaizdą. Sąmatų rodinyje jūs informuojami apie planuojamo darbo kainos ir pajamų poveikį. Sąmatų rodinys – tai įrankis matyti informaciją apie kelias iš anksto apibrėžtas dimensijas, kad būtumėte kuo geriau informuoti apie finansinį projekto poveikį.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Projekto kaina ir pardavimo vertė  
„[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ kainoraščiuose apibrėžiama projekto naudojamų vaidmenų kaina ir apmokestinimo tarifai. Remdamiesi vaidmenimis, susietais su projekto darbo paskirstymo struktūros užduotimis, galite nustatyti atliekamo darbo kainos ir pajamų poveikį.  
  
## <a name="cost-price-defaulting"></a>Numatytosios savikainos nustatymas  
Kiekvienas projektas priklauso organizacijai (projekte tai nurodoma srityje **Nuosavybės teisę turintis vienetas** ). Vieneto savikaina nustatoma kainoraščiu, susietu su nuosavybės teisę turinčiu organizaciniu vienetu. „[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]“ vaidmenų savikainas nustato savikainų sąraše ieškodama vaidmens, vieneto ir organizacinio vieneto derinio, kad gautų sąmatų eilučių galiojimo datos savikainą.  
  
Jei pagal vaidmens, vieneto ir organizacinio vieneto derinį nuosavybės teisę turinčio organizacinio vieneto kainoraštyje savikainos gauti negalima, vieneto nepaisoma, ir naudojamas vaidmens bei organizacinio vieneto derinys. Jei savikaina yra, ji konvertuojama į vienetą, kurį pasirinkote sąmatų eilutėje.  
  
Jei pagal vaidmens ir organizacinio vieneto derinį savikainos gauti negalima, organizacinio vieneto nepaisoma, ir naudojamas vaidmens ir vieneto derinys, o numatytoji kaina nustatoma ją konvertavus (jei reikia).  
  
 Jei vaidmens kainos nėra, sąmatų eilutėje numatytoji savikaina nustatoma į 0,00.  
  
 Visos išlaidų sumos projekto išlaidų sąmatų eilutėse pateikiamos nuosavybės teisę turinčio organizacinio vieneto valiuta.  
  
## <a name="sales-price-defaulting"></a>Numatytosios pardavimo kainos nustatymas  
Pardavimo kainoraštis paremtas pardavimo objektu, prie kurio projektas pridėtas. Vieneto pardavimo kaina nustatoma pardavimo kainoraščiu, susietu su pasiūlymu ar sutartimi. Jei prie pasiūlymo ar sutarties yra pasirinktinis kainoraštis, jis bus numatytasis projekto sąmatų pardavimo kainoraštis. Jei su pardavimo objektais sąsajų nėra, numatytasis projekto kainoraštis bus parametrų nuostatose sukonfigūruotas numatytasis kainoraštis. Kiekvienoje sąmatų eilutėje yra susietas išteklių organizacinis vienetas, kuris nurodo organizacinį vienetą, iš kurio bus rezervuojami ištekliai atlikti užduočiai. Susietų vaidmenų pardavimo kaina nustatoma pardavimo kainoraštyje ieškant vaidmens, vieneto ir išteklių organizacinio vieneto derinio, kad būtų gauta sąmatų eilučių galiojimo datos pardavimo kaina.  
  
Jei pagal vaidmens, vieneto ir išteklių organizacinio vieneto derinį pardavimo kainoraščio kainos gauti negalima, sistema vieneto nepaisys ir ieškos vaidmens bei išteklių organizacinio vieneto derinio. Jei pardavimo kaina randama, ji bus konvertuojama į vienetą, kurį pasirinkote pardavimo sąmatų eilutėje.  
  
Jei sistema vaidmens kainos neranda, sąmatų eilutėje numatytoji pardavimo kaina turi būti nustatyta į 0,00.  
  
Sąmatų rodinyje yra tinklelio rodinys, kuriame rodomas plokščias sąmatų eilučių su vienetu, visa kaina ir pardavimo kaina tinklelis.  
  
## <a name="time-phased-view-of-project-estimates"></a>Laipsniškai laike išdėstytas projekto sąmatų rodinys  
Laipsniškai laike išdėstytame projekto sąmatų rodinyje sąmatų duomenys iš tinklelio rodinio pagal numatytąsias nuostatas greitai surikiuojami pagal vaidmenį, ir sąmatų duomenys išdėstomi pasirinktos laiko skalės laiko planavimo juostoje.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Pastangų sąmatų paskirstymas pagal užduoties režimą  
Laipsniškai laike išdėstytame rodinyje visos įvertintos užduoties pastangos paskirstomos priskiriant tam tikrą pastangų valandų per pasirinktos laiko skalės laikotarpio vienetų skaičių. „Project Service“ užduoties režimu nustatoma, kaip pastangos paskirstomos per visą užduoties trukmę. Dvi paskirstymo rūšys – tai lygus paskirstymas ir paskirstymas pagal darbo valandas.  
  
## <a name="work-hours-based-allocation"></a>Paskirstymas pagal darbo valandas  
Automatinio planavimo užduoties režimas nustato, kad įvertintą užduoties išteklių skaičių numatoma naudoti visas dienos darbo valandas. Tai taip pat taikoma, kai pastangos paskirstomos jas išskaidant per visą užduočių trukmę laipsniškai laike išdėstytame rodinyje. Pavyzdžiui, „dienos‟ laiko skalėje užduoties, numatomos atlikti naudojant vieną išteklių, per dieną paskirstytos pastangos neviršys dienos darbo valandų, apibrėžtų projekto kalendoriuje. Todėl paskirstant pastangas visada užtikrinama, kad ištekliai būtų numatomi naudoti visą dieną.  
  
## <a name="even-distribution"></a>Lygus paskirstymas  
Rankiniu būdu suplanuotas užduoties režimas neatsižvelgia į darbo valandas, projekto kalendorių ir apibrėžtą užduoties išteklių skaičių. Užduočių grafikas paremtas naudotojo įvestimi. Tokių užduočių pastangas paskirstant pasirinktos laiko skalės laikotarpio vienetui, netaikomi jokie ribojantys veiksniai. Visos užduoties pastangos lygiai išskaidomos ir priskiriamos kiekvienam pasirinktos laiko skalės laikotarpio vienetui.  
  
Tokiu būdu apibrėžtas užduoties režimas nustato pastangų paskirstymą arba priskyrimą vienam laipsniškai laike išdėstytų sąmatų laikotarpio vienetui.  
  
## <a name="grouping-and-time-phasing-options"></a>Grupavimas ir laipsniško išdėstymo laike parinktys  
Šis rodinys padeda suprasti pastangų, išlaidų ir pardavimo sąmatų paskirstymą dienai, savaitei, mėnesiui ar metams. Parinktis Grupuoti pagal leidžia sąmatų duomenis greitai surikiuoti pagal kitas dvi dimensijas: kategorijos ir ištekliaus. Tiek tinklelio rodinyje, tiek laipsniškai laike išdėstytame rodinyje galite pasirinkti rodytinus laukus. Kiekvieno laiko bloko sumos rodomos apačioje; jomis nurodomos visos įvertintos pastangos, išlaidos ir pardavimas per dieną, savaitę, mėnesį ar metus.  
  
Numatytoji kaina ir pardavimo kaina nustatoma pagal galiojimo datą – kai pasikeis vaidmenų tarifai, jie bus skaidresni laipsniškai laike išdėstytame rodinyje, peržiūrint pagal „išteklių‟ greitai surinkiuotus ir laipsniškai pagal savaitę išdėstytus sąmatų duomenis.  
  
## <a name="expense-estimates"></a>Išlaidų sąmatos  
Visas patirtas projekto išlaidas, kurios tiesiogiai nesusijusios su darbo išlaidomis, galima įrašyti į projekto sąmatas, pateiktas tinklelio rodinyje. Tai atlikti galite naudodami tinklelio rodinio parinktį **Pridėti išlaidų sąmatą**. Galima įrašyti konkrečios užduoties arba viso projekto išlaidų sąmatas; šiose eilutėse galite pasirinkti išlaidų kategorijas ir preliminarią datą, kad išlaidas numatoma patirti. Jei susietuose kainos ir pardavimo kainos kainoraščiuose yra numatytųjų kainų ar apibrėžtų išlaidų kategorijų antkainių procentų, susiejant kainoraštis bus pagal numatytąsias nuostatas naudojamas sąmatų eilutėje.  
  
### <a name="see-also"></a>Taip pat žr.  
 [Projekto vadovo vadovas](../psa/project-manager-guide.md)
