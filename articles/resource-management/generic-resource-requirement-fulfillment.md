---
title: Bendrųjų išteklių reikalavimų vykdymas
description: Šioje temoje pateikiama informacija apie įvardytų išteklių rezervavimą bendrųjų išteklių reikalavimui.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 92255564e2a1ffa4077ded9b3cf5216dedba0913
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588608"
---
# <a name="generic-resource-requirement-fulfillment"></a>Bendrųjų išteklių reikalavimų vykdymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Galite rezervuoti įvardytą išteklių, jei norite pakeisti bendrąjį išteklių, kuriam taikomas ištekliaus reikalavimas.

1. Puslapyje **Projektai** pasirinkite skirtuką **Komanda**.
2. Sąraše pasirinkite bendrąjį išteklių, kuriam taikomas ištekliaus reikalavimas, ir spustelėkite **Rezervuoti**. Arba atidarykite ištekliaus reikalavimą ir spustelėkite **Rezervuoti**.
3. Puslapyje **Pagalbinė planavimo priemonė** pasirinkite įvardytą išteklių, kurį norite rezervuoti savo projekto komandoje, ir spustelėkite **Rezervuoti**.

Atlikus rezervavimą ir įvardytam ištekliui jį įvykdžius, bendrasis išteklius pakeičiamas įvardytu ištekliumi.

Priskyrimus, nurodytus grafike, taip pat galima atnaujinti naudojant įvardytą išteklių.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Bendrojo ištekliaus reikalavimo įvykdymas naudojant kelis įvardytus išteklius
Bendrojo ištekliaus reikalavimas įvykdomas naudojant kelis įvardytus išteklius panašiai, kaip ir priskiriant vieną įvardytą išteklių. Pavyzdžiui, turite penkių dienų trukmės užduotį, kuriai skirta 120 darbo valandų. Šios užduoties per penkių dienų darbo savaitę negali atlikti vienas išteklius, dirbantis įprastą aštuonių valandų trukmės darbo dieną. 

120 valandų reikalavimas per penkias dienas skirtas robotų technikai, dirbančiai 24 valandas per parą.

Tai yra pavyzdys, kai norint įvykdyti bendrojo ištekliaus užklausą reikia kelių įvardytų išteklių. Norint įvykdyti reikalavimą jums reikės rezervuoti kelis išteklius.

Šis scenarijus iš esmės skiriasi tuo, kad bendrasis išteklius lieka komandoje priskirtas užduočiai, o rezervuoti įvardytų išteklių komandos nariai nėra priskirti pareigų daliai. Projekto vadovas gali atitinkamai priskirti darbą įvardytiems ištekliams. Išskaidydamas kelis išteklių rezervavimus pagal užduočių priskyrimus, projektų vadovas gali naudotis rodiniu **Suderinimas**. Šis procesas neatliekamas automatiškai, nes bet kokio sudėtingesnio scenarijaus atveju, nei aprašoma ankstesniame paprastame pavyzdyje, kaip antai, kai reikalavimą sudaro užduočių paketas, sistema turėtų numanyti, kaip projekto vadovas ketina priskirti. Kadangi sistema negali suprasti ketinimų, prielaidos gali būti kitokios, nei numatyta, ir gaunamas netinkamas arba nenuspėjamas rezultatas. Nuspėjami rezultatai gaunami, kai bendrieji ištekliai lieka priskirti tol, kol projekto vadovas sąmoningai sukuria priskyrimus naudodamasis rodiniu **Suderinimas**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]