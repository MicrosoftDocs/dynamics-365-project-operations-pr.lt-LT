---
title: Įvardytų išteklių rezervavimas iš išteklių reikalavimų
description: Šioje temoje pateikiama informacija apie įvardytų išteklių rezervavimą bendrųjų išteklių reikalavimui.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 20e3a904bc33360b194c0c53e58430c80d1ff55f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081041"
---
# <a name="book-named-resources-from-resource-requirements"></a>Įvardytų išteklių rezervavimas iš išteklių reikalavimų

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Galite rezervuoti įvardytą išteklių, jei norite pakeisti bendrąjį išteklių, kuriam taikomas ištekliaus reikalavimas.

1. Programos „Project Service Automation“ (PSA) puslapyje **Projektai** spustelėkite skirtuką **Komanda**.
2. Sąraše pasirinkite bendrąjį išteklių, kuriam taikomas ištekliaus reikalavimas, ir spustelėkite **Rezervuoti**. Arba atidarykite ištekliaus reikalavimą ir spustelėkite **Rezervuoti**.


![Bendrojo komandos nario rezervavimas](media/RM-how-to-14.png)


3. Puslapyje **Pagalbinė planavimo priemonė** pasirinkite įvardytą išteklių, kurį norite rezervuoti savo projekto komandoje, ir spustelėkite **Rezervuoti**.

![Bendrojo komandos nario rezervavimas naudojant pagalbinę planavimo priemonę](media/RM-how-to-15.png)

Atlikus rezervavimą ir įvardytam ištekliui jį įvykdžius, bendrasis išteklius pakeičiamas įvardytu ištekliumi.

![Įvardyto komandos nario pakeitimas bendruoju komandos nariu](media/RM-how-to-16.png)

Priskyrimus, nurodytus grafike, taip pat galima atnaujinti naudojant įvardytą išteklių.

![Įvardyto komandos nario priskyrimas projekto užduotims](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Bendrojo ištekliaus reikalavimo įvykdymas naudojant kelis įvardytus išteklius
Bendrojo ištekliaus reikalavimas įvykdomas naudojant kelis įvardytus išteklius panašiai, kaip ir priskiriant vieną įvardytą išteklių. Pavyzdžiui, turite penkių dienų trukmės užduotį, kuriai skirta 120 darbo valandų. Šios užduoties per penkių dienų darbo savaitę negali atlikti vienas išteklius, dirbantis įprastą aštuonių valandų trukmės darbo dieną. 

![Užduotis, kurią reikia atlikti per penkias dienas, dirbant 120 valandų](media/RM-how-to-21.png)

120 valandų reikalavimas per penkias dienas skirtas robotų technikai, dirbančiai 24 valandas per parą.

![Dienos reikalavimas](media/RM-how-to-22.png)

Tai yra pavyzdys, kai norint įvykdyti bendrojo ištekliaus užklausą reikia kelių įvardytų išteklių. Norint įvykdyti reikalavimą jums reikės rezervuoti kelis išteklius.

![Kelių išteklių rezervavimas siekiant įvykdyti reikalavimą](media/RM-how-to-23.png)

Šis scenarijus iš esmės skiriasi tuo, kad bendrasis išteklius lieka komandoje priskirtas užduočiai, o rezervuoti įvardytų išteklių komandos nariai nėra priskirti pareigų daliai. Projekto vadovas gali atitinkamai priskirti darbą įvardytiems ištekliams. Išskaidydamas kelis išteklių rezervavimus pagal užduočių priskyrimus, projektų vadovas gali naudotis rodiniu **Suderinimas**. Šis procesas neatliekamas automatiškai, nes bet kokio sudėtingesnio scenarijaus atveju, nei aprašoma ankstesniame paprastame pavyzdyje, kaip antai, kai reikalavimą sudaro užduočių paketas, sistema turėtų numanyti, kaip projekto vadovas ketina priskirti. Kadangi sistema negali suprasti ketinimų, yra tikimybė, kad ji numanys kitaip, nei ketinama, ir gautas rezultatas bus netinkamas arba nenuspėjamas. Nuspėjami rezultatai gaunami, kai bendrieji ištekliai lieka priskirti tol, kol projekto vadovas sąmoningai sukuria priskyrimus naudodamasis rodiniu **Suderinimas**.


