---
title: Įvardytų rezervuojamų išteklių rezervavimas projekto komandai ir užduočių priskyrimas
description: Šioje temoje pateikiama informacija apie įvardytų išteklių rezervavimą projektų komandoms ir jų priskyrimą užduotims.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: e0f3957936e699fb2a9f570b9789924c55e12cc2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009356"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Įvardytų rezervuojamų išteklių rezervavimas projekto komandai ir užduočių priskyrimas 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Galite įtraukti įvardytąjį išteklių į savo projekto komandą rezervuodami juos tiesiogiai komandoje. Kad tai padarytumėte atlikite toliau nurodytus veiksmus.

1. Programoje „Project Service Automation“ eikite į sritį **Projektai** ir pasirinkite atidaryti projektą, kuriam rezervuojate.
2. Puslapio **Projektas** skirtuke **Komanda** spustelėkite **Naujas**. 

![Komandos nario įtraukimas naudojant komandos skirtuką](media/RM-how-to-1.png)

3. Dialogo lange **Spartusis projekto komandos nario kūrimas** pasirinkite rezervuojamą išteklių. Jei ištekliui yra priskirtas numatytasis ištekliaus vaidmuo, jis bus automatiškai įvestas į lauką **Vaidmuo**. Jei reikia, vaidmenį galite keisti. 
4. Pasirinkite pradžios ir pabaigos datas, kada išteklius bus reikalingas, ir pasirinkite ištekliaus pajėgumo paskirstymo metodą. 
5. Jei norite, kad komandos narys būtų projekto tvirtintojas, lauke **Projekto tvirtintojas** pasirinkite reikšmę **Taip**. Tai reikš, kad komandos narys galės tvirtinti pateiktus šio projekto laiko ir išlaidų įrašus. 
6. Spustelėkite **Įrašyti**.

![Komandos nario įtraukimas į sparčiojo kūrimo formą](media/RM-how-to-2.png)


Dabar galite rezervuotą išteklių priskirti projekto užduotims. Puslapyje **Projektas** spustelėkite skirtuką **Grafikas** ir priskirkite užduotis naujam ištekliui. Išteklių parinkiklis, paleidžiamas naudojant užduočių tinklelio lauką **Ištekliai**, parodys komandos narius, kuriuos galite pasirinkti.

![Komandos nario priskyrimas užduočiai naudojant skirtuką Grafikas](media/RM-how-to-3.png)

Programos „Project Service Automation“ (PSA) 3 versijoje išteklių rezervavimas ir užduočių priskyrimai nėra tvirtai susieti. Tai reiškia, kad naudodamiesi grafike esančiu išteklių parinkikliu komandos nariams galite priskirti daugiau užduočių valandų, nei jiems yra priskirta rezervuotų projekto valandų.
Skirtuke **Komanda** arba **Išteklių suderinimas** galite matyti skirtumus tarp komandos narių rezervavimų ir priskyrimų. Be to, išteklių rezervavimų ir priskyrimų skirtumus galite suderinti išsamesniu lygiu.

![Išteklių suderinimo skirtukas](media/RM-how-to-4.png)

Norėdami ieškoti rezervuojamų išteklių, kurie dar nėra įtraukti į jūsų projekto komandą, ir juos pasirinkti taip pat galite skirtuke **Grafikas** esantį išteklių parinkiklį. Išteklių parinkiklyje jie yra rodomi kaip **Kiti ištekliai**.

![Ne komandos nario ištekliaus priskyrimas užduočiai](media/RM-how-to-5.png)

Kai naudojate šį veiksmą, išteklius įtraukiamas į projekto komandą ir priskiriamas užduočiai, tačiau rezervavimas negeneruojamas.

![Priskyrimai komandos nariams nerezervuojant](media/RM-how-to-6.png)

Norėdami rezervuoti ištekliaus pajėgumą projektui galite naudoti skirtuko **Derinimas** rezervavimo išplėtimo pajėgumą arba **Grafiko lentą**.

![Komandos nario rezervavimų išplėtimas skirtuke Išteklių derinimas](media/RM-how-to-7.png)

Rezervavę komandos narį savo projektui, jo rezervavimus galite tvarkyti naudodami funkciją Prižiūrėti rezervavimus arba tiesiogiai naudodamiesi Grafiko lenta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]