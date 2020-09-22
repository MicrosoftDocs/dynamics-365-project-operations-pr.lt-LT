---
title: Bendrųjų rezervuojamų išteklių priskyrimas užduočiai ir projekto komandai
description: Šioje temoje pateikiama informacija apie bendrųjų išteklių rezervavimą užduotims ir projekto komandoms.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f461fbd3-1fce-4aeb-a896-a6d14453a5a4
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 82478e2cf97ab03e80e9f5fbb662b3603d5905b9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753791"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Bendrųjų rezervuojamų išteklių priskyrimas užduočiai ir išteklių reikalavimų generavimas 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Savo projektui galite ne tik rezervuoti ir priskirti įvardytus arba realius išteklius, bet ir priskirti bendruosius išteklius projekto užduotims. Šiuos išteklius galima naudoti kaip įvardytų išteklių vietos rezervavimo ženklus, kol būsite pasirengę juos pakeisti įvardytais projekto ištekliais. 

1. Naudodami „Project Service Automation“ (PSA), atidarykite puslapį **Projektas** ir skirtuko **Grafikas** grafiko langelyje **Išteklius** įveskite bendrojo ištekliaus padėties pavadinimą. Arba spustelėkite langelyje esančią piktogramą **Išteklius** ir atidarykite išteklių parinkiklį, tada įveskite bendrojo ištekliaus, kurį norite sukurti, pavadinimą.

![Bendrojo komandos nario sukūrimas ir priskyrimas](media/RM-how-to-9.png)

Atsidarys sritis **Spartusis kūrimas: projekto komandos narys**. 

2. Įveskite bendrojo išteklių komandos nario vaidmenį ir organizacijos vienetą, tada spustelėkite **Įrašyti**.

![Spartusis bendrojo komandos nario kūrimas](media/RM-how-to-10.png)

3. Sukūrus naują bendrąjį išteklių komandos narį, jis priskiriamas užduočiai. Galite tęsti ir priskirti tą bendrąjį išteklių kitoms užduočių grafiko užduotims.

![Esamo bendrojo komandos nario priskyrimas užduotims](media/RM-how-to-11.png)

4. Priskyrę bendrąjį išteklių, galite generuoti ištekliaus reikalavimą ir jį įvykdyti tiesiogiai rezervuodami arba pateikdami ištekliaus užklausą išteklių vadovui.

![Bendrojo komandos nario reikalavimo generavimas](media/RM-how-to-12.png)

Komandos narių tinklelyje galite naudoti ne tik išteklių parinkiklį, kaip paminėta pirmiau, bet ir tiesiogiai įtraukti bendruosius išteklius. Ištekliai įtraukiami nurodant išteklių reikalavimą, pagrįstą pradžios / pabaigos datomis ir paskirstymo metodu, nurodytu srityje **Spartusis kūrimas: projekto komandos narys**.

Skirtumą galite pamatyti tiesiogiai įtraukę bendrąjį komandos narį ir tada bendrajam ištekliui priskyrę daugiau užduočių, nei yra būtinų valandų, kurias jis turi apimti. Norėdami iš naujo sugeneruoti reikalavimą, atitinkantį reikiamas valandas pagal priskyrimus spustelėkite **Generuoti reikalavimą**.

Taip pat galite spustelėti komandos tinklelyje esantį saitą **Išteklių reikalavimas**, kad atidarytumėte reikalavimą, įtrauktumėte įgūdžių, pageidaujamų išteklių ir pan.

![Išteklių reikalavimas](media/RM-how-to-13.png)

