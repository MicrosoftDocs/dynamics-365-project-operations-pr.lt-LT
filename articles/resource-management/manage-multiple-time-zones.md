---
title: Laiko juostų valdymas
description: Sukūrus projektą, jo laiko juosta yra pagrįsta laiko juosta, nurodyta taikomame darbo valandų šablone.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119833"
---
# <a name="manage-time-zones"></a>Laiko juostų valdymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


## <a name="projects"></a>Projektai

Sukūrus projektą, laiko juosta yra pagrįsta laiko juosta, nurodyta taikomame darbo valandų šablone. **Projektuose** datos visada yra santykinai susijusios su vartotojo, prisijungusio prie kiekvieno skirtuko, laiko zona, išskyrus skirtuką **Užduotis**. Kai peržiūrite darbo paskirstymo struktūrą, datos visada bus rodomos projekto laiko juostoje.

## <a name="tasks"></a>Užduotys

Sukūrus užduotį, pradžios laiką, pabaigo laiką ir valandas / dienas valdo projekto darbo valandos. Pavyzdžiui, jei užduotis sukuriama su projektu, kurio laiko juosta yra -8 PST ir turi tokias darbo valandas: 9:00 iki 17:00, nuo pirmadienio iki penktadienio, bet kokia užduotis, sukurta be priskyrimo, laikysis projekto kalendoriaus pradžios ir pabaigos laiko.

## <a name="manage-resources-with-time-zones"></a>Išteklių valdymas naudojant laiko zonas

Norint gauti tikslius ir nuspėjamus rezultatus naudojant parinktį **Išplėsti rezervavimą**, reikia atlikti dvi pagrindines būtinąsias sąlygas:  

- Vartotojas turi sukonfigūruoti savo įrenginio laiko juostą, kad ji atitiktų laiko juostą, apibrėžtą sistemos **tinkinimo parametruose**.
 
  ![Laiko juostos parametrai „Windows 10“](media/reconcile-assignments-03.png)

  ![Laiko juostos parametrai personalizavimo parametruose](media/reconcile-assignments-04.png)
 
- Rezervuojami ištekliai turi turėti bent vieną minutę darbo laiko, kuri sutampa su kontūrais, kurie naudojami pageidaujamo išplėtimo apibrėžimui. Pavyzdžiui, šie ištekliai su darbo valandomis, kurie patenka nuo 9:00 iki 19:00. 

  ![Išteklių kontūrų palyginimas](media/reconcile-assignments-05.png)

Toliau esančioje lentelėje pateikiama:

- A projekto kalendoriaus šablonas
- A išteklius: šis išteklius turi tą patį kalendorių ir yra toje pačioje laiko juostoje kaip ir projektas. Rezervavimo pradžios laikas bus 9.00.
- Išteklius B: šis išteklius yra kitoje laiko juostoje nei projektas ir prasideda 7:00 val. jų laiko juostoje. Tačiau rezervavimai prasidės 9.00, nes tai yra anksčiausias priskyrimo kontūro pradžios laikas.
- Ištekliai C ir D: ištekliai yra skirtingose laiko juostose ir skiriasi nuo projekto ir vienas kito, o jų rezervavimai prasideda ne anksčiau nei atitinkamas jų pradžios laikas.

|Objektas  |Kalendorius  |
|-|-|
|Projekto kalendoriaus šablonas   | ![Projekto kalendorius](media/reconcile-assignments-06.png) |
|A išteklius  | ![A ištekliaus kalendorius](media/reconcile-assignments-06.png) |
|B išteklius  |  ![B ištekliaus kalendorius](media/reconcile-assignments-07.png) |
|C išteklius  |  ![C ištekliaus kalendorius](media/reconcile-assignments-08.png) |
|D išteklius  | ![D ištekliaus kalendorius](media/reconcile-assignments-09.png)  |
 
Kai pereisite į rodinį **Suderinimas**, rodomi išteklių priskyrimai ir susiję rezervavimo trūkumai.

![Suderinimo rodinys prieš išplėtimą](media/reconcile-assignments-10.png)

Po to, kai kiekvienam ištekliui buvo panaudota rezervavimo išplėtimo funkcija, rezervavimai sėkmingai pratęsiami kiekvienam ištekliui, nes kiekvieno ištekliaus darbo valandos sutapo su trūkumo kontūrais.

![Suderinimo rodinys po rezervavimo išplėtimo](media/reconcile-assignments-11.png) 

Atkreipkite dėmesį, kad išsamiau pažvelgus į rezervavimo detales, skiriasi rezervavimo pradžios laikas. Rezervavimai pradedami ne anksčiau, nei priskyrimo kontūro pradžios laikas, bet ne anksčiau nei galimas ištekliaus pradžios laikas.

![Naujos išteklių rezervacijos grafiko lentoje](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]