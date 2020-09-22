---
title: Projektų ir rezervavimų valdymas jūsų Office 365 kalendoriuje
description: Kaip valdyti projektus ir rezervavimus Office 365 kalendoriuje?
author: ruhercul
manager: kfend
ms.service: dynamics-365-projectservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 92428956-1058-4490-934f-907fbbdc8f25
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5c075e0b63db35c1e189a62a6b5b00f5bcb7ea97
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753612"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Projektų ir rezervavimų valdymas jūsų kalendoriuje („Project Service“)

> [!Note]
> NEBENAUDOJAMA: ši funkcija yra nebenaudojama ir nebepasiekiama.

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Peržiūrėkite asmenines paskyras, projekto darbų rezervacijas ir „Field Service“ darbo užsakymo priskyrimus, naudodami „[!INCLUDE[pn_office_365](../includes/pn-office-365.md)]“ kalendorių.  
  
 Viskas vienoje vietoje, todėl lengviau tvarkyti dienos darbus. Jūsų visi susitikimai, paskyros, rezervacijos ir užduotys pateikiami „[!INCLUDE[pn_office_365](../includes/pn-office-365.md)]“ kalendoriuje.  
  
 Jei naudojate „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“, savo asmenines paskyras taip pat galite įvesti laiko įrašo rodinyje „Project Service“. Tokiu būdu projekto ir išteklių vadovai gali žinoti jūsų projektų užimtumą. Be to, sutaupoma jūsų laiko, nes jums nereikia įvesti informacijos apie asmenines paskyras du kartus. Tiesiog galite importuoti asmenines paskyras iš kalendoriaus į laiko įrašo rodinį „Project Service“.  
  
 Jūsų kalendoriuje bus sinchronizuotos projekto ir darbo užsakymo rezervacijos per ateinančias keturias savaites skaičiuojant nuo šiandien. Šio parametro keisti negalima.  
  
 Palaikomas tik vienos krypties sinchronizavimas – iš PSA į [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] kalendorių. Galite sinchronizuoti atvirkštine tvarka. 
  
 Norėdami sužinoti, kaip naudoti „[!INCLUDE[pn_office_365](../includes/pn-office-365.md)]“ kalendorių, peržiūrėkite puslapį [Verslui skirtas „Outlook“ kalendorius žiniatinklyje](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Sąranka  
 Prieš peržiūrėdami ir tvarkydami rezervacijas „[!INCLUDE[pn_office_365](../includes/pn-office-365.md)]“ kalendoriuje, jums reikia nustatyti keletą parametrų.  
  
- Jums reikės turėti [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] visuotinio administratoriaus arba sistemos administratoriaus kredencialus.  
  
- Jūsų administratorius turės sukonfigūruoti el. pašto serverio profilį ir kiekvienas vartotojas turės sukonfigūruoti savo pašto dėžutę. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [El. pašto apdorojimo nustatymas, atliekant sinchronizavimą serveryje](../admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks.md)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Organizacijos sinchronizavimo įjungimas (administratoriaus užduotis)  
  
1.  Pagrindiniame meniu spustelėkite **Parametrai** > **Administravimas**.  
  
2.  Spustelėkite **Sistemos parametrai**.  
  
3.  Spustelėkite skirtuką **Sinchronizavimas**.  
  
4.  Dalyje **Pasirinkite, ar įgalinti išteklių rezervavimo sinchronizavimą** pasirinkite **Sinchronizuoti išteklių rezervacijas naudojant „Outlook“**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Vartotojo profilio sinchronizavimo įjungimas (vartotojo užduotis)  
  
1.  Spustelėkite viršutiniame dešiniajame ekrano kampe esantį mygtuką **Parametrai** .  
  
2.  Spustelėkite **Veiksmai**.  
  
3.  Spustelėkite skirtuką **Sinchronizavimas**.  
  
4.  Dalyje **Išteklių rezervacijų sinchronizavimas naudojant „Outlook“** pažymėkite **Sinchronizuoti išteklių rezervacijas naudojant „Outlook“**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Asmeninių paskyrų importavimas (vartotojo užduotis)  
 Galite importuoti asmenines paskyras iš kalendoriaus į laiko įrašo rodinį „Project Service Automation“.  
  
1. Atidarykite „[!INCLUDE[pn_office_365](../includes/pn-office-365.md)]“ kalendorių ir spustelėkite **Importuoti duomenis**.  
  
2. Ekrane Filtrai pasirinkite **„Exchange“ paskyros** ir tada spustelėkite **Taikyti**.  
  
3. Sistema perkels paskyras į laiko įrašo rodinį kaip siūlomus dabartinės savaitės įrašus. Norėdami įtraukti kitos savaitės įrašų, spustelėkite **Ankstesnis** arba **Kitas**.  
  
4. Pasirinkite paskyrą, kurią norite įtraukti į laiko įrašo rodinį „Project Service Automation“.  
  
5. Iššokančiajame lange **Laiko įrašas** pasirinkite parinktis, reikalingas paskyrą konvertuojant į laiko įrašo rodinį „Project Service Automation“.  
  
6. Spustelėkite **Įrašyti**.  
  
### <a name="see-also"></a>Taip pat žr.  
 [Laiko, išlaidų ir bendradarbiavimo vadovas](../project-service/time-expense-collaboration-guide.md)
