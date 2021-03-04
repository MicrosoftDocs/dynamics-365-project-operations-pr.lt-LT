---
title: Peržiūrėti apmokestinamą išteklių naudojimą
description: Šioje temoje pateikiama informacija apie išteklių naudojimo rodinį.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146403"
---
# <a name="view-chargeable-utilization-for-resources"></a>Peržiūrėti apmokestinamą išteklių naudojimą

[!include [banner](../includes/psa-now-project-operations.md)]
 
Puslapyje **„Project Service“ išteklių naudojimas** **Naudojimo rodinys** rodo kiekvieno rezervuojamo ištekliaus apmokestinamą naudojimą. Kadangi rodinys grindžiamas Grafiko lenta, pamatysite, kad yra daug tokių pačių funkcijų.

> ![Naudingumo rodinio ekrano nuotrauka](media/FAQ-utilization-1.png)
 

Apmokestinamo naudojimo skaičiavimas atliekamas taip:

   Apmokestinamas naudojimas = (Apmokestinamos faktinės valandos) / (Išteklių pajėgumas).

Langeliuose pateikiamas suskaičiuotas apmokestinamas naudojimas per pasirinktą laikotarpį (dienas, savaites ar mėnesius).

Spalvos kiekviename langelyje reiškia apmokestinamą išteklio naudojimą, palyginti su tiksliniu apmokestinamu naudojimu. 

Gali būti nustatytas tikslinis numatytojo ištekliaus vaidmens arba atskiro ištekliaus naudojimas. Skaičiuojant pirma atsižvelgiama į atskirą išteklių kaip į tikslą, tada į numatytąjį ištekliaus vaidmenį.

## <a name="set-target-on-a-resource"></a>Išteklių tikslo nustatymas

1. Eikite į **Ištekliai** \> **Ištekliai**. 
2. Pasirinkite išteklius, norėdami atidaryti įrašą. 
3. Skirtuke **Project Service** galite nustatyti ištekliaus tikslinį naudojimą.

> ![Skirtuko „Project Service“ naudojimo, siekiant nustatyti tikslinį naudojimą, ekrano nuotrauka](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Tikslinio naudojimo nustatymas vaidmeniui

1. Eikite į **Ištekliai** \> **Išteklių planavimas**. 
2. Pasirinkite išteklius ir atidarykite įrašą. 
3. Nustatyti tikslinį vaidmens naudojimą.

> ![Dalies „Išteklių vaidmenys“ naudojimo, siekiant nustatyti tikslinį naudojimą, ekrano nuotrauka](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Apmokestinamų išteklių naudojimo skaičiavimas

Norėdami apskaičiuoti apmokestinamą išteklių naudojimą, turite atlikti keletą nustatymų. 

### <a name="set-default-role-for-individual-resource"></a>Nustatykite numatytąjį atskiro ištekliaus vaidmenį

Pirmiausia, tikslinis naudojimas turi būti nustatytas atskiram ištekliui arba išteklių vaidmenims. Jei naudojate išteklių vaidmenis kaip tikslus, kiekvienas atskiras išteklius privalo turėti numatytąjį vaidmenį. 

1. Norėdami atlikti tokius nustatymus, eikite į **Ištekliai** \> **Ištekliai**. 
2. Pažymėkite išteklių, atidarykite įrašą ir pažymėkite skirtuką **Project Service**. 
3. Tinklelyje **Išteklių vaidmuo** įsitikinkite, kad yra vienas išteklių vaidmuo, o **Numatytoji reikšmė** nustatyta į **Taip**.
 
### <a name="change-billing-type-for-resource-role"></a>Pasirinkite atsiskaitymo už šį išteklių vaidmenį tipą.

Išteklių vaidmenys turi būti nustatyti į atsiskaitymo tipą **Apmokestinamas**. 

1. Eikite į **Ištekliai** \> **Išteklių planavimas**. 
2. Atidarykite įrašą, kurį norite atnaujinti, tada nustatykite numatytąjį atsiskaitymo tipą į **Apmokestinamas**.

### <a name="set-working-hours-for-resource-role"></a>Išteklių vaidmenų darbo valandų nustatymas
 
Turi būti nustatytos išteklių darbo valandos, siekiant suskaičiuoti pajėgumą. 

1. Eikite į **Ištekliai** \> **Ištekliai**. 
2. Pasirinkite išteklių, kad atidarytumėte įrašą, tada pasirinkite **Rodyti darbo valandas**. 
3. Galite masiškai atnaujinti išteklių sąrašą, taikydami **Darbo valandų šablonas**, esantį rodinyje **Išteklių sąrašas**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Apmokestinamų faktinių valandų trikčių šalinimas

Apmokestinamos faktinės valandas gaunamos iš objekto **Faktiniai duomenys**. Faktiniai duomenys su atsiskaitymo tipu **Apmokestinamas** yra įtraukti į skaičiavimą, todėl privalote turėti projektus, kurių faktiniai duomenys yra apmokestinami.

Jei nematote apmokestinamo naudojimo, patikrinkite šiuos dalykus:

- Apibrėžtas išteklio darbo valandų pajėgumas.
- Išteklius turi atskirai nustatytą naudojimo tikslą arba turi jam skirtą numatytąjį vaidmenį. Vaidmuo turi jam nustatytą naudojimo tikslą.
- Faktiniai duomenys turi atsiskaitymo tipą **Apmokestinamas** laikotarpiui, kuriam tikitės naudojimo skaičiavimo. Jeigu matote faktinius duomenis su neapmokestinamu atsiskaitymo tipu, patikrinkite šias sąlygas:

  - Faktiniams duomenims naudojamas vaidmuo turi kitokį numatytąjį atsiskaitymo tipą nei apmokestinamas.
  - Projekto sutarties eilutės vaidmuo, kuriuo grindžiamas projektas, buvo nustatytas kaip neapmokestinamas.
  - Projektas neturi susijusios sutarties eilutės.

