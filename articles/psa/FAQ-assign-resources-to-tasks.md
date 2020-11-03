---
title: Išteklių priskyrimas užduočiai
description: Šioje temoje pateikiama informacija apie tai, kaip priskirti išteklius užduotims.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081025"
---
# <a name="assign-a-resource-to-a-task"></a>Išteklių priskyrimas užduočiai

Ištekliui priskirti užduotį programoje Microsoft Dynamics 365 Project Service Automation galima trimis būdais.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervuokite išteklius kaip komandos narys, o tada priskirkite išteklių užduočiai

Galite pridėti išteklių prie projekto komandos, o tada projekto grafike juos priskirti užduotims.

1. Skirtuke **„Komandos narys“** pridėkite naują komandos narį, pasirinkdami **„Naujas“**. 

2. Atidaroma sritis **„Spartusis komandos nario kūrimas“** , kuriame galima pasirinkti rezervuojamą išteklių pavadinimą ir nustatyti vaidmenį. 

    Pasirinkite vieną iš pateiktų išteklių rezervavimo paskirstymo metodų:

    - **Visas pajėgumo metodas**  – rezervuojamas visas išteklių pajėgumas tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.
    - **Pajėgumo procentinės dalies rezervavimo metodas**  – rezervuojama išteklių pajėgumo dalis procentais tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.
    - **Tolygiai paskirstomų valandų metodas**  – ištekliai rezervuojami nurodytam valandų skaičiui, kiekvienai dienai skirtą laiką tolygiai paskirstant nuo nurodyto laikotarpio pradžios ir pabaigos.
    - **Pirminės apkrovos metodas**  – ištekliai rezervuojami į išteklių naudojimo pradžios dieną keliant didžiausią dienos valandų skaičių tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.
    - **Joks**  – ištekliai pridedami prie komandos, tačiau rezervavimai, kurie sunaudoja išteklių pajėgumą, nesukuriami.

3. Užduoties tinklelyje **„Grafikas“** pasirinkite išteklių langelyje esančią piktogramą **„Ištekliai“** , o tada skirtuke **„Komandos nariai“** pasirinkite ką tik pridėtą komandos narį. 

> [!NOTE]
> Skirtukuose **„Komandos narys“** ir **„Derinimas“** matomos rezervuotos ir priskirtos išteklių valandos. Jų valandos turėtų būti vienodos, tačiau tai nėra privaloma, nes rezervavimas ir priskyrimai nėra tvirtai susieti. Skirtuke **„Derinimas“** galite rasti informaciją apie tai, kada jie skiriasi, pavyzdžiui, kada ištekliams priskiriate daugiau valandų nei rezervavote. Tuomet, jeigu reikia, galite taisyti informaciją – prailginti išteklių rezervavimą arba pakeisti priskyrimą.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Bendrojo komandos nario kūrimas priskiriant užduotį

Kai sukuriate bendrąjį komandos narį priskirdami jam užduotį, taip pat sukuriate vietos rezervavimo ženklą arba bendrąjį išteklių, kuriuo būtų nurodoma įvardyto ištekliaus, su kuriuo norite atlikti užduotis, charakteristika. Tada galite generuoti reikalavimą (arba pateikti užklausą naudojant reikalavimą), kuris yra naudojamas įvardytų išteklių paieškai ir rezervavimui atlikti.

1. Užduoties tinklelyje **„Grafikas“** pasirinkite išteklių langelyje esančią piktogramą **„Ištekliai“**.

2. Įveskite pavadinimą, kuris bus vietos rezervavimo ženklo išteklių pavadinimas. Pavyzdžiui, „Programos vadovas“.

3. Pasirinkite **„Kurti“** , o tada lauke **„Spartusis projekto komandos nario kūrimas“** nustatykite bendrųjų išteklių vaidmenį.

4. Užduoties **„Išteklių išrinkiklyje“** pasirinkę išteklius galite toliau priskirti užduotis šiems vietos rezervavimo ženklo ištekliams. Jie išvardyti skirtuke **„Komandos nariai“**.

5. Priskyrę bendruosius išteklius, skirtuke **„Komanda“** pasirinkite bendruosius išteklius, tada pasirinkite **„Generuoti reikalavimą“** ir sukurkite išteklių reikalavimą bendriesiems ištekliams.

6. Bendriesiems ištekliams pasirinkite **„Rezervuoti“**. Tada, norėdami rasti tikrus išteklius, pasinaudokite Grafiko lenta. Taip pat galite išteklių vadovui pateikti reikalavimą, kad jis būtų įvykdytas.

7. Kai bendrieji ištekliai pakeičiami įvardytais ištekliais, bendrieji ištekliai yra pašalinami iš komandos, o jiems paskirtos užduotys paskiriamos įvardytiems ištekliams, kuriais pakeičiami bendrųjų išteklių išteklių reikalavimai.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Įvardytų išteklių priskyrimas iš visų rezervuojamų išteklių sąrašo

Jei norite ieškoti rezervuojamų išteklių ir juos priskirti užduočiai, galite pasinaudoti **„Išteklių išrinkiklio“** ieškos lauku.

Tokiu būdu priskirti ištekliai įtraukiami į komandą neatliekant jokių rezervacijų. Taip pat galima įtraukti komandos narį ir vietoj paskirstymo metodo pažymėti „Nėra“. Ištekliai yra rodomi skirtukuose **„Komanda“** ir **„Derinimas“** kaip ištekliai, turintys tik priskyrimus ir rezervavimo deficitus. Jei norite pasinaudoti jų prieinamumu, juos rezervuokite.

1. Užduoties tinklelyje **„Grafikas“** pasirinkite išteklių langelyje esančią piktogramą **„Ištekliai“**.

2. Pradėkite rašyti pavadinimą. Pavadinimo ieškos rezultatai pateikiami **„Išteklių išrinkiklis“** , parinktyje **„Kiti ištekliai“**.

3. Pažymėkite išteklių, kurį norite priskirti prie užduoties.

