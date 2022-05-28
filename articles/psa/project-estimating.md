---
title: Projekto savikaina ir pajamos
description: Šioje temoje pateikiama informacija apie projektų savikainų ir pajamų įvertinimą.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: ecac3a08b2405e697eb260bbab991458dbe69f4e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581892"
---
# <a name="project-costs-and-revenue"></a>Projekto savikaina ir pajamos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekto įvertinimai nurodomi finansiniame rodinyje to darbo, kuris įvertintas ir suplanuotas projektų grafike. Skirtuke **Sąmatos**, esančiame puslapyje **Projektai**, rodomas suplanuotų darbo savikainos ir pajamų poveikis. Taip pat pateikiama informacija apie daugelį iš anksto nustatytų dimensijų. 

> ![Sąmatų skirtukas.](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a>Projekto savikainos ir pardavimo vertės

Kainoraštyje nustatomi projekto vaidmenų savikainos ir atsiskaitymų rodikliai. Galite nustatyti darbo savikainos ir pajamų poveikį pagal vaidmenis, susietus su pareigų pavadinimu ir įvardytuoju užduočiai ištekliumi. Jei yra užduočių, neturinčių jokių priskyrimų (bendrinių arba įvardytųjų), negalite gauti savikainos ar pardavimo sąmatų. Savikainos ir pardavimų reikšmėms apskaičiuoti atsižvelgiama į kainoraščiuose nustatytą datą.

### <a name="default-cost-price"></a>Numatytoji savikaina  

Kiekvienas projektas priklauso organizacijai. Ši organizacija rodoma projekto lauke **Sutarties vienetas**. Kainoraštis, susietas su sutarties vienetu, naudojamas vieneto savikainai nustatyti. Norėdami teisingai nustatyti vaidmenų savikainas nustatytai datai sąmatos eilutėse, ieškokite vaidmens, vieneto ir organizacinio vieneto derinio kainoraštyje. 

Kad jų savikainos galėtų būti apskaičiuojamos, visos užduotys turi būti priskirtos ištekliams. Visos nepriskirtos užduotys turės 0,00 savikainą.

Jei vaidmens, vieneto ir organizacinio vieneto derinys nerodo savikainos iš perkančiojo vieneto kainoraščio, sistema nepaiso vieneto. Užuot ieškomas tik vaidmens ir organizacinio vieneto derinys. Radus savikainą, konversijos koeficientai naudojami konvertuoti ją į vienetą, kurį pažymėjote sąmatos eilutėje.

Jei vaidmens ir organizacinio vieneto derinys nerodo savikainos, sistema nepaiso organizacinio vieneto. Užuot ji ieško vaidmens ir vieneto derinio, kad nustatytų numatytąją kainą (atlikus kiekvieną konversiją).

Jei sistema vaidmens kainos neranda, sąmatos eilutėje savikaina nustatoma į **0,00** numatytąją reikšmę. Visos savikainos sumos projekto savikainos sąmatos eilutėse įrašomos perkančiojo vieneto valiuta.

> [!NOTE]
> Pagal numatytuosius nustatymus „Microsoft Dynamics 365“ saugo savikainos sumas jūsų pagrindine valiuta. Tačiau savikainos sumos, rodomos skirtuke **Sąmatos**, yra perkančiojo vieneto valiuta.  

### <a name="default-sales-price"></a>Numatytasis pardavimo kainoraštis 

Pardavimo kainoraštis nustatomas pardavimo objektu, prie kurio pridedamas projektas, arba projekto kliento. Kai pardavimo objektas, pvz., galimybė, pasiūlymas arba sutartis, susietas su projektu, pardavimo objekto pardavimo savikaina nustatoma pagal kainoraštį, susietą su pasiūlymu ar sutartimi. Jei prie pasiūlymo ar sutarties yra pasirinktinis kainoraštis, jis bus numatytasis projekto sąmatų pardavimo kainoraštis. Jei nėra susiejimo su pardavimo objektais, numatytasis parametruose pardavimo kainoraštis naudojamas kaip numatytojo projekto pardavimo kainoraštis, sutampantis su projekte nustatyta kliento valiuta.

Kiekvienoje įvertinimo eilutėje yra su juo susieti išteklių skyrimo vienetai. Išteklių skyrimo vienetas nurodo organizacinį vienetą, iš kurio ištekliai rezervuojami užduočiai atlikti. Norėdami nustatyti susietųjų vaidmenų pardavimo savikainą, ieškokite vaidmens, vieneto ir išteklių skyrimo vieneto derinio kainoraštyje. Jei užduočiai nėra nurodyti priskyrimai, užduoties pardavimo savikaina yra 0,00.

Jei vaidmens, vieneto ir išteklių skyrimo vieneto derinys nerodo pardavimo savikainos iš pardavimo kainoraščio, sistema nepaiso šio vieneto. Užuot ieškoma tik vaidmens ir išteklių skyrimo vieneto derinio. Radus pardavimo savikainą, konversijos koeficientai naudojami konvertuoti ją į vienetą, kurį pažymėjote pardavimo sąmatų eilutėje. 

Jei vaidmens ir išteklių skyrimo vieneto derinys nerodo pardavimo savikainos iš pardavimo kainoraščio, sistema nepaiso išteklių skyrimo vieneto. Užuot ji ieško vaidmens ir vieneto derinio, kad nustatytų numatytąją kainą (atlikus kiekvieną konversiją).

Jei sistema vaidmens savikainos neranda, sąmatų eilutėje pardavimo savikaina nustatoma į **0,00** numatytąją reikšmę.

Skirtuke **Sąmatos** yra tinklelio rodinys, kuriame rodomos sąmatų eilutės. Tinklelyje yra vienetų, bendrosios savikainos ir bendrosios pardavimo kainos stulpeliai, kaip pavaizduota šioje iliustracijoje. 

> ![Tinklelio rodinys skirtuke Sąmatos.](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a>Laipsniškai laike išdėstytas projekto sąmatų rodinys

Laipsniškai laike išdėstyto projekto sąmatų rodinyje nurodyti sąmatos duomenys iš tinklelio rodinio pagal laiko planavimo juostą, jūsų pasirinkta laiko skale. Pagal numatytuosius nustatymus sąmatos duomenys yra rikiuojami greitojo rikiavimo būdu į dimensiją **Vaidmuo**.

> ![Laipsniškai laike išdėstytas rodinys projekto sąmatoms.](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a>Apskaičiuotų pastangų paskirstymas pagal užduoties režimą

Laipsniškai laike išdėstytame rodinyje visos apskaičiuotos pastangos užduočiai atlikti paskirstomos priskiriant tam tikrą pastangų valandų pasirinktos laiko skalės laikotarpio vienetui skaičių. Užduoties režimu nustatoma, kaip pastangos yra paskirstomos per visą užduoties atlikimo trukmę. Dvi paskirstymo rūšys – tai **Tolygus** ir **Pagal darbo valandas**.

### <a name="work-hours-based-allocation"></a>Paskirstymas pagal darbo valandas
 
Automatinio planavimo užduoties režimu dienos numatytosios užduočių išteklių valandos nustatomos pagal visą darbo valandų skaičių. Tai taip pat taikoma, kai pastangos paskirstomos jas išskaidant per visą užduoties atlikimo trukmę laipsniškai laike išdėstytame rodinyje. Pavyzdžiui, apskaičiavus, kad užduotis bus atlikta pasirinkus vieną išteklių laiko skalėje **Diena**, dienai priskiriamos pastangos neviršys dienos darbo valandų skaičiaus, nurodyto projekto kalendoriuje. Todėl paskirstant pastangas visada užtikrinama, kad ištekliai būtų numatomi naudoti visą dieną.

### <a name="even-allocation"></a>Tolygus paskirstymas

Neautomatiniu būdu suplanuotu užduoties režimu darbo valandos iš projekto kalendoriaus nenaudojamos. Užuot užduočių grafikas paremtas naudotojo įvestimi. Tokių užduočių pastangas paskirstant pasirinktos laiko skalės laikotarpio vienetui, netaikomi jokie ribojantys veiksniai. Visos užduoties pastangos lygiai išskaidomos ir priskiriamos kiekvienam pasirinktos laiko skalės laikotarpio vienetui. Tokiu būdu apibrėžtas užduoties režimas nustato pastangų paskirstymą arba priskyrimą kiekvienam laipsniškai laike išdėstytų sąmatų laikotarpio vienetui.

## <a name="grouping-and-time-phasing-options"></a>Grupavimas ir laipsniško išdėstymo laike parinktys

Laipsniškai laike išdėstytame rodinyje nurodomas pastangų, savikainos ir pardavimo sąmatų paskirstymas dienai, savaitei, mėnesiui ar metams. Pagal numatytuosius nustatymus sąmatos duomenys yra rikiuojami greitojo rikiavimo būdu į dimensiją **Vaidmuo**. Tačiau galite naudoti parinktį **Grupuoti pagal**, skirtą rikiuoti greitojo rikiavimo būdu kitose dviejose dimensijose: **Kategorija** ir **Išteklius**.

Tinklelio ir laipsniškai laike išdėstytame rodiniuose galite pažymėti, kuriuos laukus rodyti. Visų laiko blokų bendrosios sumos rodomos projekto apačioje. Jose rodomi bendrai apskaičiuoti dienos, savaitės, mėnesio arba metų pastangos, savikaina ir pardavimas. Numatytoji savikaina ir pardavimo kaina yra efektyvi pagal datą. Kitaip tariant, ji keičiasi pagal kiekvieną išteklių ir pagal laipsniškai laike išdėstytą rodinį, kurį pažymėjote.

## <a name="expense-estimates"></a>Išlaidų sąmatos

Mygtukas **Įtraukti naują išlaidų sąmatą** tinklelio rodinyje leidžia įrašyti visas projekte patirtas išlaidas, tačiau tai nėra tiesiogiai susiję su darbu. Galite įrašyti specifinės užduoties arba viso projekto išlaidų sąmatas. Pasirinkite išlaidų kategorijas ir preliminarią datą, kai tikitės patirti išlaidų. Jei susietuose savikainos ir pardavimo savikainos kainoraščiuose yra numatytųjų savikainų (ar apibrėžtų išlaidų kategorijų antkainių procentų), susiejant, sąmatų eilutėje jos įvedamos automatiškai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
