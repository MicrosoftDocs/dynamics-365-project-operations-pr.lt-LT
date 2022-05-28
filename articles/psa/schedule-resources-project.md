---
title: Projekto išteklių planavimas
description: Projekto išteklių planavimas „Project Service“
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: f3b7ea1a2b81b86bedc85b77689145ba5afb579d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583134"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Projekto išteklių planavimas („Project Service“)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Galite patikrinti išteklių užimtumą, kad turėtumėte apie jį bendrą vaizdą, arba galite rodinį filtruoti pagal įgūdžius, komandą, vietą ir kitas parinktis.  
  
Grafiko lentoje rodomas išteklių sąrašas ir jų pasiekiamumas. Pasirinkite peržiūros režimą, kas būtų rodomas pasiekiamumas pagal **Valandas**, **Dieną**, **Savaitę** arba **Mėnesį**.  
  
Prieš pradedant naudotis grafiko lenta, svarbu ją nustatyti. Daugiau informacijos žr. [Grafiko lentos konfigūravimas („Field Service” arba „Project Service Automation”)](/dynamics365/field-service/configure-schedule-board).
  
Jei jūs naudojate senesnę versiją, dėl išteklių pasiekiamumo, žr. [Išteklių pasiekiamumo peržiūra](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Norint naudoti grafiko lentos rezervacijos funkcines galimybes, geokodavimo ir vietos nustatymo paslaugas, jums reikia įjungti žemėlapius.  
> 
> 1. Pagrindiniame meniu pasirinkite **Išteklių planavimas** > **Administravimas**.  
> 2. Spustelėkite **Planavimo parametrai**.  
> 3. Atidarykite įrašą ir slinkite žemyn iki srities **Resource Scheduling Optimization**.  
> 4. Lauke **Prisijungimas prie žemėlapių** pasirinkite **Taip**.  
> 5. Sutikite su sąlygomis ir įrašykite įrašą.  
> 6. Pagrindiniame meniu pasirinkite **Project Service** > **Grafiko lenta**. Tada suplanuoti rezervacijos reikalavimą neautomatiniu būdu galima keliais būdais. Pasirinkite jums tinkantį būdą.
  
## <a name="find-available-resources"></a>Pasiekiamų išteklių radimas

1.  Sąraše **Rezervacijos reikalavimas** dešiniuoju pelės klavišu spustelėkite ant nesuplanuotos rezervacijos ir pasirinkite vieną iš tolesnių parinkčių.  
  
- Pasirinkite **Rasti pasiekiamus – dabartiniai ištekliai**, kad rastumėte pasiekiamų išteklių iš grafiko lentoje pateikto sąrašo.  
- Pasirinkite **Rasti pasiekiamus – visi ištekliai**, kad rastumėte pasiekiamų išteklių sistemos šaltiniuose  
   > [!NOTE]
   >  Tai atlikus, filtrai parodys pasirinkto rezervacijos reikalavimo parinktis.  
  
2. Kai pamatysite laisvą atkarpą, dešiniuoju pelės klavišu spustelėkite ant laisvos atkarpos grafiko lentoje ir pasirinkite **Rezervuoti čia**. Arba nuvilkite rezervacijos reikalavimą į laisvą laiko tarpą.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Rezervuokite išteklių dienos rodinyje ir raskite, kas nėra rezervuotas
  
1.  Grafiko lentoje pasirinkite **Peržiūros režimas** ir pasirinkite **Dienos**.  
  
    Rodomas tinklelio rodinys, kiek ištekliaus valandų yra rezervuota per dieną ir kokiomis dienomis jie laisvi.  
  
2.  Spustelėkite ištekliaus, kurį norite rezervuoti, vardą, tada pasirinkite **Rezervuoti**.  
  
3.  Dialogo lange **Išteklių rezervavimas (sukurti)** pasirinkite projektą, kuriam norite rezervuoti išteklių, taip pat rezervavimo būdą, pradžios ir pabaigos laiką.  
  
4.  Baigę pasirinkite **Rezervuoti**.  
  
## <a name="view-to-the-schedule-board"></a>Grafiko lentos peržiūra
  
1.  Pasirinkite nesuplanuotą rezervacijos reikalavimą iš sąrašo apačioje.  
  
2.  Nuvilkite rezervacijos reikalavimą į laisvų išteklių / laiko atkarpą grafiko lentoje.  
  
3.  Baigę pasirinkite **Rezervuoti**.  
  
### <a name="additional-resources"></a>Papildomi ištekliai  
 [Išteklių vadovo vadovas](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
