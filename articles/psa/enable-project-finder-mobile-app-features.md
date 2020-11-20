---
title: „Project Finder Mobile“ programėlės funkcijų įjungimas
description: „Project Finder Mobile“ programėlės funkcijų įjungimas „Project Service“
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080843"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>„Project Finder Mobile“ programėlės funkcijų įjungimas („Project Service“)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Jūsų ištekliai savo telefone gali naudoti „Project Finder Mobile“ ir „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“, kad rastų naujus projektus, kuriuos jie nori vykdyti, ir naujinti savo įgūdžių rinkinius.  
  
 Programėlę galima naudoti „[!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)]“ ir „[!INCLUDE[tn_android](../includes/tn-android.md)]“ telefonuose bei „[!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)]“.  
  
 Turite nustatyti kelias jūsų organizacijos vieneto parametrų sąrankos parinktis, kad vartotojai galėtų peržiūrėti projektų išteklių reikalavimus ir naujinti savo įgūdžius.  
  
> [!NOTE]
>  „Project Finder Mobile“ programėlę galima naudoti tik su „[!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)]“ (ne su vietine versija).  
  
1. Eikite į **Project Service > Parametrai**.  
  
2. Spustelėkite parametrų nustatymą, kurį norite naudoti, kad įjungtumėte „Project Finder Mobile“ programėlės funkcijas.  
  
3. Srityje **Bendra** parinktį **Išteklių reikalavimai matomi ištekliams** nustatykite į **Taip**.  
  
4. Nustatykite **Leisti naujinti įgūdžius pagal išteklius** į parinktį **Taip**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Tai visuotinis parametras. Projektų vadovai gali nustatyti, ar atskiras projektas bus matomas to projekto puslapyje **Projekto grupė**.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>El. pašto pranešimai  
 „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ siunčia el. laiškus dėl išteklių užklausų toliau pateiktiems gavėjams nurodytu laiku.  
  
|Gavėjas|Įvykis|  
|---------------|-----------|  
|Projekto vadovas|- Kai išteklius užsiregistruoja vykdyti projektą naudodamas „Project Finder Mobile“ programėlę.|  
|Ištekliai|- Kai projekto darbą, kurį atlikti išteklius užsiregistravo, jau atliko kitas išteklius.<br />- Kada jų įgūdžių patvirtinimo užklausa patvirtinama arba atmetama.<br />- Kada jų registracijos vykdyti projektą užklausa patvirtinama arba atmetama.|  
  
## <a name="privacy-notice"></a>Pastaba dėl privatumo  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Taip pat žr.  
 [Rezervuojamų išteklių nustatymas](../psa/set-up-resources.md)