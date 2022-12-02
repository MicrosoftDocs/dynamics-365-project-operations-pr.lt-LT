---
title: Medžiagų naudojimo projektuose ir projekto užduotyse įrašymas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip užregistruoti medžiagos naudojimą projektuose ir projekto užduotyse.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: eeb8303821bc4c246e37333ddbcb77ca798d2e8f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920070"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Medžiagų naudojimo projektuose ir projekto užduotyse įrašymas

_**Taikoma kam:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniam diegimui – išankstinėms sąskaitoms faktūroms išrašyti_

Projekto komandai dirbant su projekto užduotimis, komandos nariai naudoja medžiagas. Medžiagos naudojimo žurnalas suteikia galimybę įrašyti šį naudojimą, kad jį galėtų patvirtinti projekto vadovas ir, galiausiai, klientui būtų galima išrašyti sąskaitą faktūrą. 

Norėdami įrašyti katalogo arba įtraukiamųjų medžiagų naudojimą ir pateikti šiuos duomenis tvirtintojui, atlikite toliau nurodytus veiksmus. 

1. Naršymo srityje pasirinkite **Medžiagos naudojimas**, tada – **Naujas**.
2. Puslapyje **Naujas medžiagos naudojimas** įveskite reikiamą medžiagos naudojimo informaciją ir pasirinkite **Įrašyti**.

Šioje lentelėje pateikiama informacija apie laukus puslapyje **Medžiagos naudojimo žurnalas**. 

| **Laukas** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- |
| Aprašymas | Konkrečios medžiagos naudojimo aprašas. | Nėra jokio tolesnio šio lauko poveikio. |
| Data | Data, kada planuojama naudoti medžiagą. | Nėra jokio tolesnio šio lauko poveikio. |
| Project | Aktyvių projektų sąrašas. | Pasirinkus medžiagos naudojimo žurnalo projektą, paveikiamas laukas **Užduotis** ir jame rodomos tik į projektą įtrauktos užduotys. |
| Užduotis | Projekto užduočių sąrašas, įskaitant suvestines ir lapo mazgo užduotis. | Pasirinkus medžiagos naudojimo žurnalo užduotį, paveikiama faktinė užduoties medžiagos savikaina ir faktinis pardavimas. Jei šis laukas bus paliktas tuščias, atitinkama medžiagos naudojimo savikaina ir pardavimas bus sekami ir apibendrinami tik projekto lygiu. |
| Pasirinkti produktą | Nurodykite, ar šis medžiagos naudojimas skirtas **esamam** (kataloge nurodytam) produktui, ar **įtraukiamajam** produktui. | Šiuo lauku apibrėžiamas produkto tipas. |
| Produktas | Produkto iš produktų katalogo ID. Pasirinkus produkto ID, lauko **Pasirinkti produktą** reikšmė automatiškai atnaujinama į **Esamas produktas**. ID naudojamas norint gauti kainoraščio savikainą ir pardavimo kainas. | Nėra jokio tolesnio šio lauko poveikio. |
| Įtraukiamojo produkto aprašas | Teksto laukas, kuriame reikia įrašyti produkto pavadinimą. Šis laukas pasiekiamas pasirinkus **Įtraukiamąjį** produktą lauke **Pasirinkti produktą**.| Nėra jokio tolesnio šio lauko poveikio. |
| Rezervuotini ištekliai| Ištekliai, naudoję šią medžiagą projekte. Šio lauko numatytoji reikšmė yra rezervuojami prisijungusio vartotojo ištekliai, tačiau galima pakeisti, kad naudojimas būtų įrašytas kitų projekto komandos narių vardu. | Nėra jokio tolesnio šio lauko poveikio. |
| Vienetų grupė | Numatytoji šio lauko reikšmė gaunama iš vienetų grupės, katalogo produktui nustatytos kaip numatytoji. Šį lauką galite atnaujinti, kad būtų galima pasirinkti kitą vienetų grupę. | Nėra jokio tolesnio šio lauko poveikio. |
| Vienetas | Šio lauko numatytoji reikšmė yra pasirinkto produkto numatytasis vienetas. Šį lauką galite atnaujinti, kad būtų galima pasirinkti kitą vienetą. | Pakeitus vienetą, nustatoma kita numatytoji vieneto kaina ir savikaina. |
| Kiekis | Produkto, kuris naudojamas projektui arba projekto užduočiai, kiekis. | Nėra jokio tolesnio šio lauko poveikio. |
| Vieneto savikaina | Pasirinkto produkto vieneto savikainos ir vieneto derinys, nustatytas taikomame savikainos kainoraštyje. | Vieneto savikaina visada rodoma projekto savikainos valiuta. Jei kainoraštyje produkto ir vieneto deriniui nustatyto vieneto savikainos nėra, vieneto savikainai bus nustatyta numatytoji reikšmė – 0,00. |
| Bendroji savikaina | Savikainos suma, apskaičiuojama kaip vieneto \* kiekio savikaina.| Savikainos suma visada rodoma projekto savikainos valiuta. |


## <a name="submit-material-usage-for-review-and-approval"></a>Medžiagos naudojimo pateikimas peržiūros ir patvirtinimo tikslais 
Užfiksavę visą medžiagos naudojimą ir būdami pasirengę jį patvirtinti, naudojimo informaciją turite pateikti peržiūrai.

1. Eikite į **Medžiagos naudojimo žurnalas** ir pasirinkite vieną ar kelis įrašus. Arba pasirinkite visus medžiagos naudojimo įrašus pažymėdami žymės langelį antraštėje.
2. Pasirinkite **Pateikti**. Sistema apdoroja pasirinktus įrašus, tada sukuria medžiagos naudojimo patvirtinimo užklausas.

## <a name="recall-a-material-usage-log"></a>Medžiagos naudojimo žurnalo atšaukimas

Prireikus pateiktą medžiagos naudojimo informaciją galite atšaukti. Laikas, kurio reikia medžiagos naudojimo įrašui atšaukti, priklauso nuo patvirtinimo etapo.  Jei tvirtintojas dar nepatvirtino įrašo, jis gali būti nedelsiant atšauktas. Tačiau, jei įrašas jau buvo patvirtintas, tvirtintoją prašoma patvirtinti atšaukimą ir atšaukti operacijas.

1. Eikite į **Medžiagos naudojimas** ir, medžiagos naudojimo žurnalų sąraše, pasirinkite medžiagą, kurią norite atšaukti.
2. Pažymėkite **Atšaukti**. Jei medžiagos naudojimo įrašas dar nebuvo patvirtintas, sistema nedelsiant jį atšauks. Jei medžiagos įrašas jau buvo patvirtintas, sukuriama atšaukimo užklausa, kuria tvirtintojui pranešama, kad medžiagos naudojimą norite atšaukti. Tvirtintojas patvirtina, kad galima atšaukti, o įrašas bus grąžintas.

## <a name="delete-a-material-usage-log"></a>Medžiagos naudojimo žurnalo naikinimas

Panaikinti galite nepateiktus medžiagos naudojimo žurnalus. Norėdami panaikinti jau pateiktą medžiagos naudojimo žurnalą, pirmiausia jį turite atšaukti.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
