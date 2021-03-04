---
title: Išlaidų strategijų nustatymas
description: Galite nustatyti išlaidų strategijas, kurių darbuotojai turi laikytis įvesdami ir pateikdami išlaidų ataskaitas bei kelionių paraiškas „Microsoft Dynamics 365 Finance“.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab99c0ec769eb2e0914fc7d993f83d20e2c327f6
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960707"
---
# <a name="set-up-expense-policies"></a>Išlaidų strategijų nustatymas

Galite apibrėžti išlaidų strategijas, kurias turi atlikti darbuotojai, įvesdami ir pateikdami išlaidų ataskaitas ir kelionės paraiškas.         
Įgyvendinus išlaidų politiką gali būti lengviau veiksmingai valdyti išlaidas.         

Pavyzdžiui, galite nustatyti Niujorke esančio viešbučio išlaidų strategijas, kuriose nurodoma, kad kaina už naktį negali būti didesnė nei USD 250.       
Jei darbuotojas pateikia išlaidų ataskaitą arba kelionės paraišką, kai kambario kaina viršija šią sumą, sistema praneš        
darbuotojui, kad strategijoje nurodyta išlaidų suma buvo viršyta. Galite konfigūruoti pranešimą, kurį darbuotojas, kai jūs        
apibrėžite strategiją.      
        
Galite apibrėžti trijų tipų strategijas:         
        
- Įspėjimas – leidžia darbuotojui pateikti išlaidų ataskaitą arba kelionės paraišką, tačiau išlaidos bus pažymėtos visiems tvirtintojams ir        
  vėlesnei ataskaitai.        

- Klaida – reikalaujama, kad darbuotojas peržiūrėtų išlaidas, kad įvykdytų šią strategiją prieš pateikdamas išlaidų ataskaitą arba kelionės paraišką.       
 
 - Pagrindimas – reikalaujama, kad darbuotojas arba vadovas pateiktų paaiškinimą, kodėl viršijama strategijoje nustatyta suma, prieš pateikdamas išlaidų ataskaitą arba kelionės paraišką.        

## <a name="policy-tips"></a>Strategijos patarimai
Pateikiame kelis pasiūlymus, kurie gali padėti jums kuriant naujas išlaidų valdymo strategijas. 
* Strategijos galioja nustatytą laikotarpį ir negalios, jei bus sukurtos po to, kai patiriamos išlaidos. Pavyzdžiui, jei šiandien kuriate naują strategiją, kad būtų galima maksimaliai padidinti maisto kainą 50 USD, tada bet kokios esamos išlaidos, įrašytos kaip vakarykštės, nebus tikrinamos pagal šią strategiją.
* Kurdami išlaidų kategorijos, kurią galima detaliai, strategiją, galite įtraukti sąlygą dėl išlaidų eilutės tipo. Kai kurios strategijos, pvz., kvito reikalavimas, gali būti beprasmės detalizuotose eilutėse ir turėtų būti taikomos tik antraštės eilutei arba nedetalizuotai eilutei. 
* Pagal numatytuosius nustatymus išlaidų valdymo strategijos yra vertinamos pagal šaltinio objektą. Jei naudojate vidinės įmonės scenarijus, galite nustatyti, kad strategija būtų vertinama pagal paskirties objektą (skolinimosi objektas). Norėdami vykdyti strategijas pagal paskirties objektą, įjunkite funkciją „Vertinti išlaidų strategiją skolinant juridiniam subjektui“ **Funkcijų valdymo** darbo srityje.

## <a name="when-to-evaluate-policies"></a>Kada vertinti strategijas

Išlaidų valdymo parametruose yra parinktis įvertinti išlaidų valdymo strategijas įrašius eilutę arba pateikus išlaidų ataskaitą. Jei pasirinksite įvertinti įrašius eilutę, tai užtikrins, kad naudotojai galės anksčiau matyti, ką reikia daryti norint iš karto užbaigti savo išlaidų ataskaitą. Kitu atveju galite atidėti strategijos įvertinimą ir sutaupyti laiko tvirtindami pabaigoje, kai pateikiama į darbo eigą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]