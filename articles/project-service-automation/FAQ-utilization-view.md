---
title: Peržiūrėti apmokestinamą išteklių naudojimą
description: Šioje temoje pateikiama informacija apie išteklių naudojimo rodinį.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753644"
---
# <a name="view-chargeable-utilization-for-resources"></a>Peržiūrėti apmokestinamą išteklių naudojimą
 
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

