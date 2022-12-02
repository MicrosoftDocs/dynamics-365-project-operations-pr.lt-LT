---
title: Pagrindinės sąvokos
description: Šiame straipsnyje pateikta informacija apie pagrindines išteklių valdymo sąvokas, minimas „Project Service Automation“.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 41b13000ca17ec3a5d86fdb17885f09692d6f0c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921726"
---
# <a name="key-concepts"></a>Pagrindinės sąvokos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Šioje lentelėje apibrėžiamos svarbiausios programoje „Dynamics 365 Project Service Automation“ naudojamos sąvokos.

| Sąvoka                    | Aprašas |
|----------------------------|------------|
| Projekto komandos narys        | Kaip projekto komandos dalis, projekto komandos narys gali būti pavadintas išteklius, turintis užsakymų, pavadintas išteklius, neturintis užsakymų arba bendrasis išteklius. Bendrieji ištekliai neturi užsakymų, yra vietiniai projektui ir projektuose neturi pajėgumo apribojimų. |
| Projekto bendrieji ištekliai   | Išteklių vietos rezervavimo ženklas, leidžiantis suformuoti komandą ir personalą projekto plane, nežinant įvardytojo ištekliaus. Projekto kalendorius naudojamas kaip bendrasis ištekliaus kalendorius. Bendruosius išteklius galima įtraukti į projekto komandą ir priskirti užduotims. |
| Rezervuotos valandos               | Išteklių valandos yra tiksliai suplanuotos skirti projektui ir padeda užtikrinti, kad projekto veikla būtų baigta. Rezervuotos valandos naudojamos iš bendro išteklių pajėgumo. Užsakymai yra su įvardytais ištekliais, o ne su bendraisiais ištekliais. |
| Priskirtos valandos             | Išteklių valandos priskiriamos projekto grafiko užduotims. Priskyrimai gali būti su įvardytais ištekliais arba bendraisiais ištekliais. Priskyrimai gali būti nepriklausomi nuo užsakymų. |
| Reikalingos valandos             | Būtinas pajėgumas, bet dar nevykdomas pagal įvardytąjį išteklių. Reikiamos valandos tinka tik bendriniams komandos nariams, kurių išteklių reikalavimai sugeneruoti. |
| Poreikis                     | Dabartinis ir gaunamas darbo krūvis. Programoje „Project Service Automation“ poreikis rodomas kaip išteklių reikalavimai arba išteklių užklausos. |
| Išteklių reikalavimas       | Objektas, naudojamas reikiamam valandų skaičiui fiksuoti, pradžios ir pabaigos datas, įgūdžius, geografiją ir kitas įkainių reikiamų išteklių dimensijas. Išteklių reikalavimai sukuriami pagal projekto komandos narius arba sukuriami individualiai. |
| Išteklių užklausa           | Objektas, naudojamas kaip „paketas“, kuriame yra išteklių reikalavimai, kuriuos turi įvykdyti išteklių vadovas. |
| Išteklių numatytasis vaidmuo      | Vaidmuo, kuriam ištekliai grupuojami pagal naudojimo skaičiavimą. Manoma, kad ištekliai turi reikiamų vaidmeniui įgūdžių ir atitinka panaudojimo tikslą, priskirtą vaidmeniui. |
| Išteklių organizacinis vienetas | Organizacinis vienetas, kuriam priskirti ištekliai. |
| Kontūras                    | Užduotis, reikalavimas arba priskyrimo valandos, kai jos suskirstytos į dienos paskirstymą. Pavyzdžiui, penkių dienų 40 valandų užduotį galima kontūru paskirstyti į aštuonias valandas per dieną per penkias dienas. |
| Derinimo rodinys        | Rodinys, rodantis kiekvieno projekto komandos nario užsakymus ir priskyrimus. Šis rodinys leidžia projektų vadovui ieškoti neatitikimo tarp užsakymų ir priskyrimų ir atlikti korekcinius veiksmus, jei yra neatitikimas. |
| Darbo valandos                 | Objektas, naudojamas išteklių pajėgumui bei darbo ir ne darbo valandoms identifikuoti. Šis objektas taip pat vadinamas išteklių kalendoriumi. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
