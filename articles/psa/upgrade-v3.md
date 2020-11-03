---
title: Atnaujinimo aptarimas – „Microsoft Dynamics 365 Project Service Automation“ 2.x arba 1.x versijos į 3 versiją
description: Šioje temoje pateikta informacija apie dalykus, į kuriuos reikia atsižvelgti atnaujinant iš „Project Service Automation“ 2.x arba 1.x versijos į 3 versiją.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 19d6d312c7cedd2d7b9b5649452b85dd24fae761
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080916"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Atnaujinimo aptarimas - iš PSA 2.x arba 1.x versijos į 3 versiją
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>„Project Service Automation“ ir „Field Service“
Dynamics 365 Project Service Automation ir Dynamics 365 Field Service išteklių planavimui naudoja „Universal Resourcing Scheduling“ sprendimą. Jei egzemplioriuje turite ir „Project Service Automation“ ir „Field Service“, turėtumėte planuoti, kad būtų atnaujinti abu sprendimai į naujausią versiją („Project Service Automation“ 3.x versiją, „Field Service“ 8.x versiją). Atnaujinus „Project Service Automation“ arba „Field Service“ bus įdiegta naujausia URS versija, tai reiškia, kad galimas nesuderinamas veikimas, jei to paties egzemplioriaus „Project Service Automation“ ir „Field Servic“ sprendimai nebus atnaujinti į naujausią versiją.

## <a name="resource-assignments"></a>Išteklių priskyrimai
Naudojant „Project Service Automation“ 2 versiją ir 1 versiją, užduočių priskyrimai buvo saugomi kaip antrinės užduotys (taip pat vadinamos eilutės užduotimis) **Užduoties objekte** , ir buvo netiesiogiai susiję su objektu **Išteklių priskyrimas**. Eilutės užduotis buvo matoma priskyrimo iššokančiajame lange darbo paskirstymo struktūroje (WBS).

![Eilutės užduotys WBS „Project Service Automation“ 2 versijoje ir 1 versijoje](media/upgrade-line-task-01.png)

„Project Service Automation“ 3 versijoje pasikeitė rezervuojamų išteklių priskyrimo užduotims schema. Eilutės užduotis nebenaudojama, o tarp užduoties **Užduoties objekte** ir komandos nario objekte **Išteklių priskyrimas** yra tiesioginis 1:1 ryšys. Projekto komandos nariui priskiriamos užduotys dabar saugomos tiesiogiai išteklių priskyrimo objekte.  

Šie pakeitimai turi įtakos visų esamų projektų, kuriuose yra įvardytų rezervuojamų išteklių ir bendrųjų išteklių projekto komandoje priskyrimų, atnaujinimui. Šioje temoje nurodyti dalykai, į kuriuos reikės atsižvelgti dėl projektų atnaujinant iki 3 versijos. 

### <a name="tasks-assigned-to-named-resources"></a>Įvardytiems ištekliams priskirtos užduotys
Naudojant esamą užduoties objektą, 2 versijos ir 1 versijos užduotys leido komandos nariams atlikti kitą vaidmenį, o ne jų numatytąjį apibrėžtą vaidmenį. Pavyzdžiui, Irena Jankauskienė, kuriai pagal numatytuosius nustatymus priskirtas programų vadovo vaidmuo, galėjo būti priskirta užduočiai, kurios vaidmuo yra kūrėjas. 3 versijoje įvardyto komandos nario vaidmuo visada yra numatytasis, todėl bet kokioje užduotyje, kuriai Irena Jankauskienė priskirta, naudojamas jos numatytasis programų vadovo vaidmuo.

Jei naudodami 2 versiją ir 1 versiją priskyrėte išteklių užduočiai už jo numatytojo vaidmens ribų, atnaujinę, įvardytam ištekliui bus priskirtas numatytasis vaidmuo visuose užduočių priskyrimuose, neatsižvelgiant į vaidmens priskyrimą 2 versijoje. Todėl bus apskaičiuotų įvertinimų iš 2 versijos arba 1 versijos į 3 versiją skirtumų, nes įvertinimai apskaičiuojami atsižvelgiant į išteklių vaidmenį, o ne į eilutės užduoties priskyrimą. Pavyzdžiui, 2 versijoje dvi užduotys priskirtos Brigitai Bortkevičienei. 1 užduoties eilutės užduoties vaidmuo yra kūrėjas, o 2 užduoties programos vadovas. Brigitos Bortkevičienės numatytasis vaidmuo yra programos vadovas.

![Vienam ištekliui priskirti keli vaidmenys](media/upgrade-multiple-roles-02.png)

Kadangi kūrėjo ir programų vadovo vaidmenys skiriasi, savikainos ir pardavimo įvertinimai yra tokie:

![Išteklių vaidmenų savikainos įvertinimai](media/upggrade-cost-estimates-03.png)

![Išteklių vaidmenų pardavimo įvertinimai](media/upgrade-sales-estimates-04.png)

Atnaujinus į 3 versiją, eilutės užduotys pakeičiamos išteklių priskyrimais rezervuojamų išteklių komandos nario užduočiai. Priskyrimas naudos numatytąjį rezervuojamų išteklių vaidmenį. Šioje iliustracijoje Brigita Bortkevičienė, kurios vaidmuo yra programos vadovas, yra išteklius.

![Išteklių priskyrimai](media/resource-assignment-v2-05.png)

Kadangi įvertinimai apskaičiuojami pagal numatytąjį išteklių vaidmenį, pardavimo ir savikainos įvertinimai gali pasikeisti. Atkreipkite dėmesį, kad toliau pateiktoje iliustracijoje neberodomas vaidmuo **Kūrėjas** , nes vaidmuo dabar gaunamas iš rezervuojamų išteklių numatytojo vaidmens.

![Numatytųjų vaidmenų savikainos įvertinimai](media/resource-assignment-cost-estimate-06.png)
![Numatytųjų vaidmenų pardavimo įvertinimai](media/resource-assignment-sales-estimate-07.png)

Kai naujinimas bus baigtas, galėsite redaguoti komandos nario vaidmenį, kad jis būtų kitoks nei priskirtasis numatytasis vaidmuo. Tačiau, jei pakeisite komandos nario vaidmenį, jis bus pakeistas visose jam priskirtose užduotyse, nes 3 versijoje komandos nariams nebeleidžiama priskirti kelių vaidmenų.

![Išteklių vaidmens naujinimas](media/resource-role-assignment-08.png)

Tai taikoma ir eilutės užduotims, kurios buvo priskirtos įvardytiems ištekliams, kai pakeičiate išteklių organizacijos vienetą iš numatytojo į kitą organizacijos vienetą. Baigus naujinimą į 3 versiją, priskyrimas naudos išteklių numatytąjį organizacijos vienetą, o ne tą, kuris nustatytas eilutės užduotyje.

### <a name="tasks-assigned-to-generic-resources"></a>Bendriesiems ištekliams priskirtos užduotys
2 versijoje ir 1 versijoje galite nustatyti vaidmenį ir organizacijos vienetą užduotyje, o tada naudoti funkciją **Generuoti komandą** , kad būtų sugeneruoti bendrieji ištekliai pagal nustatytus užduoties atributus. 3 versijoje sukuriate bendruosius komandos narius su vaidmeniu ir organizacijos vienetu, tada komandos narius priskiriate užduotims.

2 versijoje ir 1 versijoje projektai su bendraisiais ištekliais gali būti dviejų būsenų arba abiejų būsenų deriniu užduočių lygiu. Pvz., galimi šie scenarijai:

- Užduotys su nustatytais vaidmenimis ir organizacijos vienetais, tačiau nesugeneruotas joks susijęs išteklių priskyrimas.
- Užduotys su bendraisiais komandos narių išteklių priskyrimais, kurie buvo priskirti sukuriant bendruosius išteklius naudojant funkciją **Generuoti komandą**.

Prieš pradedant naujinti, rekomenduojame iš naujo sugeneruoti kiekvieno projekto, kuriame yra bendriesiems ištekliams priskirtų užduočių, arba kuriuose dar reikia įvykdyti komandos generavimo procesą, komandą.

Užduotims, priskirtoms bendriesiems komandos nariams, kurie buvo sugeneruoti naudojant funkciją **Generuoti komandą** , atnaujinus bendrasis išteklius bus paliktas komandoje, o priskyrimas bus paliktas tam bendrajam komandos nariui. Rekomenduojame sugeneruoti bendrojo komandos nario išteklių reikalavimą po atnaujinimo, bet prieš rezervuojant arba pateikiant išteklių užklausą. Taip bus išsaugoti bet kokie organizacijos vienetų priskyrimai bendriesiems komandos nariams, kurie skiriasi nuo projekto sutartį sudarančios organizacijos vieneto.

Pavyzdžiui, projekte „Projektas Z“ sutartį sudarančios organizacijos vienetas yra „Danys US“. Projekto plane testavimo užduotims diegimo fazėje buvo priskirtas vaidmuo „techninis konsultantas“, o priskirtas organizacijos vienetas yra „Danys India“.

![Diegimo etapo organizacijos priskyrimas](media/org-unit-assignment-09.png)

Po diegimo etapo integravimo testavimo užduotis priskiriama vaidmeniui „techninis konsultantas“, tačiau organizacija nustatoma į „Danys US“.  

![Integravimo testavimo užduočių organizacijos priskyrimas](media/org-unit-generate-team-10.png)

Generuojant projekto komandą sukuriami du bendrieji komandos nariai dėl skirtingų organizacijos vienetų užduotyse. „Techninis konsultantas 1“ bus priskirtas „Danys India“ užduotims, o „techninis konsultantas 2“ turės „Danys US“ užduotis  

![Sugeneruoti bendrieji komandos nariai](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> „Project Service Automation“ 2 versijoje ir 1 versijoje komandos narys neturi organizacijos vieneto, jis laikomas eilutės užduotyje.

![2 versijos ir 1 versijos eilutės užduotys „Project Service Automation“](media/line-tasks-12.png)

Organizacijos vienetą galite matyti įvertinimų rodinyje. 

![Organizacijos vieneto įvertinimai](media/org-unit-estimates-view-13.png)
 
Baigus naujinti, organizacijos vienetas eilutės užduotyje, atitinkantis bendrąjį komandos narį, įtraukiamas prie bendrojo komandos nario, o eilutės užduotis pašalinama. Todėl rekomenduojame prieš naujinant sugeneruoti arba iš naujo generuoti kiekvieno projekto, kuriame yra bendrųjų išteklių, komandą.

Dėl užduočių, kurioms priskirtas vaidmuo su organizacijos vienetu, kuris skiriasi nuo sutarties sudarymo projekto organizacijos vieneto, o komanda nebuvo sugeneruota, atnaujinus vaidmeniui bus sukurtas bendrasis komandos narys, tačiau kaip komandos nario organizacijos vienetas bus naudojamas projekto sutartį sudarantis vienetas. Grįžtant prie „Projekto Z“ pavyzdžio, tai reiškia, kad sutartį sudarančios organizacijos vienetui „Danys US“ ir projekto plano testavimo užduotims diegimo fazėje buvo priskirtas vaidmuo „Techninis konsultantas“, kurio organizacijos vienetas priskirtas „Danys India“. Integravimo testavimo užduočiai, kuri buvo baigta po diegimo etapo, buvo priskirtas vaidmuo „Techninis konsultantas“. Organizacijos vienetas yra „Danys US“, o komanda nebuvo sugeneruota. Atnaujinus bus sukurtas vienas bendrasis komandos narys, techninis konsultantas, kuriam priskirtos visų trijų užduočių valandos ir organizacijos vienetas „Danys US“, projekto sutartį sudarančios organizacijos vienetas.   
 
Nesugeneruotų komandos narių skirtingų išteklių paskyrimo organizacijos vienetų numatytosios reikšmės pakeitimas yra priežasties, dėl kurios rekomenduojame prieš atnaujinant sugeneruoti arba iš naujo generuoti kiekvieno projekto, kuriame yra bendrųjų išteklių, komandą, kad nebūtų prarasti organizacijos vienetų priskyrimai.

