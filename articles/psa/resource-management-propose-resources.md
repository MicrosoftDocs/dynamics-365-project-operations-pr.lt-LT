---
title: Projektų išteklių siūlymas
description: Šioje temoje pateikiama informacija apie siūlomus projekto išteklius.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 2003f6f06912b0c47eb942aae17e509b00e19487
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283018"
---
# <a name="propose-project-resources"></a>Projektų išteklių siūlymas

[!include [banner](../includes/psa-now-project-operations.md)]

Išteklių valdytojai projektų vadovui gali pasiūlyti išteklius naudodami išteklių užklausą.

1. Išteklių užklausos tinklelyje pažymėkite **Rasti išteklius**.
2. Puslapyje **Planavimo pagalbinė priemonė** pažymėkite išteklius, tada skyde **Kurti išteklių rezervaciją** lauke **Rezervacijos būsena** pažymėkite **Rezervuoti**.

    ![Pasirinktas pasiūlytas išteklius](media/Resource-Management-image62.png)

Galimi šie būsenos naujinimai:

- Puslapyje **Planavimo pagalbinė priemonė** būsenos indikatoriai atnaujinami, kad rodytų, kad rezervacija yra pasiūlyta, o ne galutinai rezervuota.

    ![Pasiūlytos rezervacijos būsenos indikatoriai planavimo pagalbinės priemonės puslapyje](media/Resource-Management-image63.png)

- Išteklių užklausoje būsena pakeičiama į **Reikia peržiūrėti**.

    ![Išteklių užklausos būsena pakeista į „Reikia peržiūrėti“](media/Resource-Management-image64.png)

- Projekto skirtuke **Komanda** bendrosios komandos nario reikšmė **Pageidauti būsenos** pakeičiama į **Reikia peržiūrėti**.

    ![Bendrosios komandos nario užklausos būsena komandos skirtuke pakeičiama į „Reikia peržiūrėti“](media/Resource-Management-image48.png)

Projekto vadovas gali priimti arba atmesti pasiūlymą.

Kai išteklių valdytojas apdoroja išteklių užklausas, jis gali naudoti bet kurį iš toliau nurodytų metodų.

- Pasiūlyti kelis išteklius, kad patenkintų poreikį, jei nėra nei vieno atskiro ištekliaus, kuris užpildytų pageidaujamas valandas. Tada pasiūlytos valandos padalinamos keliams ištekliams, kurie gali patenkinti pageidaujamas valandas. Tokiu atveju valandos negali persidengti.
- Pasiūlyti mažiau išteklių, nei pageidaujama. Tokiu atveju pasiūlytas išteklių pajėgumas yra mažesnis nei pageidaujamos valandos, kurias nurodė pageidaujantis asmuo. Todėl, kai pageidaujantis asmuo sutinka su pasiūlytais ištekliais, sukuriamas neįvykdytas išteklių reikalavimas, kuris fiksuoja likusią poreikio dalį.
- Rezervuoti kelis išteklius, kad patenkintų poreikį, jei nėra nei vieno atskiro ištekliaus, kuris užbaigtų darbą.
- Rezervuoti mažiau išteklių, nei pageidaujama. Tokiu atveju rezervuotų valandų yra mažiau nei pageidautų valandų. Sistema parodys, kaip pasiūlyti išteklius, o ne rezervacijas, kad pageidaujantis asmuo galėtų patikrinti ir stebėti likusią poreikio dalį.

## <a name="billable-utilization"></a>Apmokėtinas naudojimas

Ištekliai gali turėti tikslinį apmokėtiną naudojimą. Šis tikslinis naudojimas apibrėžiamas kaip atributas išteklių numatytame vaidmenyje arba nustatomas atskiro rezervuojamo ištekliaus įraše. Naudojimo skaičiavimai pagrįsti faktinėmis valandomis, apie kurias ištekliai pranešė naudodami patvirtintus laiko įrašus.

Naudojimo skaičiavimui naudojamos toliau nurodytos formulės.

- Apmokėtinas naudojimas = apmokestinamos faktinės valandos ÷ išteklių pajėgumas
- Neapmokėtinas naudojimas = faktinis laikas su apmokėtino tipo ID = neapmokestinamas, papildomas arba negalimas ÷ išteklių pajėgumas
- Vidinis = faktinis laikas be pardavimo sutarties ÷ išteklių pajėgumas
- Išteklių pajėgumas = išteklių darbo valandos – išvykęs – ne darbo dienos

Rodinį **Išteklių naudojimas** galite rasti skyde **Ištekliai**.

![Išteklių naudojimo rodinys](media/Resource-Management-image65.png)

Kiekvienas tinklelio langelis nurodo išteklių apmokėtiną naudojimą pagal laiką, pavyzdžiui, dieną, savaitę arba mėnesį. Langeliams naudojamos toliau nurodytos spalvos.

- **Žalia:** apmokėtinas naudojimas \>= išteklių tikslinis naudojimas
- **Geltona:** tikslinis naudojimas – 20 \<= apmokėtinas naudojimas \< tikslinis naudojimas
- **Raudona:** apmokėtinas naudojimas \< tikslinis naudojimas – 20

Kadangi rodinys **Išteklių naudojimas** pagrįstas grafiko lenta, galite naudoti grafiko lentos filtravimo galimybes, kad filtruotumėte rezultatus.

Reikia, kad tinkleliui nustatytumėte tikslinį naudojimą arba pagal vaidmenį, arba individualų išteklių. Norėdami atlikti tokius nustatymus, eikite į **Ištekliai** \> **Išteklių vaidmenys**.

Be to, kiekvienam rezervuojamam ištekliui reikia priskirti numatytąjį vaidmenį. Eikite į **Ištekliai** \> **Ištekliai**. Skirtuke **Project Service** patikrinkite, kad nustatytas išteklių vaidmuo ir kad laukas **Yra numatytasis** nustatytas kaip **Taip**. Galite įtraukti papildomų vaidmenų, kai **Kaip numatytasis = ne**. Vaidmuo, kai **Yra numatytasis = taip**, naudojamas išteklių naudojimui įvertinti pagal to vaidmens tikslą.

![Numatytojo vaidmens nustatymas](media/Resource-Management-image67.png)

Skirtuke **Project Service** taip pat galite ištekliui nustatyti individualų tikslinį naudojimą. Tada naudojimo skaičiavimui naudojamas šis tikslinis naudojamas, kad būtų įvertintas išteklių tikslas, o ne išteklių numatytojo vaidmens tikslas.

Išteklių naudojimas rodomas, tik jei šis išteklius turi patvirtintą ir apmokestinamą laiką periode, kuris rodomas tinklelyje.

## <a name="resource-availability"></a>Išteklių pasiekiamumą

Labai svarbu, kad išteklių valdytojai galėtų peržiūrėti išteklių pasiekiamumą ir naujinti rezervacijas. Kai kuriais atvejais nėra formalaus poreikio (išteklių užklausos), tačiau išteklių valdytojas turi reaguoti į neplanuotą poreikį, kurį gauna per tokius kanalus kaip el. paštas, telefono skambutis ar tiesioginis pranešimas. Išteklių valdytojai naudoja grafiko lentą, kad naujintų išteklius ir rezervacijas.

Išteklių darbo valandos naudojamos kaip išteklių pasiekiamumo skaičiavimo pagrindas. Išteklių rezervacijos naudoja išteklių pajėgumą.

![Grafiko lenta](media/Resource-Management-image68.png)

Grafiko lentoje naudojamos spalvos ir atspalviai, kurie rodo rezervacijas, pasiekiamumą ir per daug rezervacijų, taip pat rezervacijų būseną. Grafiko lentos parametrai leidžia rodyti legendą.

Jei grafiko lentoje šalia atskiro rezervuojamo ištekliaus atsiranda į dešinę rodanti rodyklė, išteklių galima išplėsti, kad būtų rodoma darbo, kuriam rezervuotas išteklius, informacija.

![Rezervuojamas išteklius, išplėstas grafiko lentoje](media/Resource-Management-image69.png)

Kadangi Dynamics 365 Project Service Automation naudoja Universal Resource Scheduling variklį, jei taip pat įdiegėte Dynamics 365 Field Service, galite peržiūrėti projektams, darbo užsakymams ir objektams, kuriuos išplėtėte planavimui, išteklių rezervacijų informaciją.

![Išteklių rezervacijų projektams ir darbo užsakymams informacija](media/Resource-Management-image70.png)

Norėdami peržiūrėti daugiau informacijos apie atskirą išteklių, spustelėkite dešiniu pelės klavišu, kad atidarytumėte išteklių kortelę.

![Išteklių kortelė](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]