---
title: Apibrėžti išlaidų strategijas
description: Galite apibrėžti išlaidų strategijas, kurias turi atlikti darbuotojai, įvesdami ir pateikdami išlaidų ataskaitas ir kelionės paraiškas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 863d1e44dad9fa0d2174cf77582a1d820988e92d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276088"
---
# <a name="define-expense-policies"></a>Apibrėžti išlaidų strategijas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Galite apibrėžti išlaidų strategijas, kurias turi atlikti darbuotojai, įvesdami ir pateikdami išlaidų ataskaitas ir kelionės paraiškas.         
Įgyvendinus išlaidų politiką gali būti lengviau veiksmingai valdyti išlaidas.         

Pavyzdžiui, galite nustatyti Niujorke esančio viešbučio išlaidų strategijas, kuriose nurodoma, kad kaina už naktį negali būti didesnė nei USD 250.       
Jei darbuotojas pateikia išlaidų ataskaitą arba kelionių paraiškas, kai kambario kaina viršija šią sumą, sistema praneš         
darbuotojui, kad strategijoje nurodyta išlaidų suma buvo viršyta. Galite konfigūruoti pranešimą, kurį darbuotojas, kai jūs        
apibrėžite strategiją.      
        
Galite apibrėžti trijų tipų strategijas:         
        
- **Įspėjimas** – leidžia darbuotojui pateikti išlaidų ataskaitą arba kelionių rekvizavimą, tačiau sąskaita bus pažymėta visiems tvirtintojams ir         
  vėlesnei ataskaitai.        

- **Klaida** – reikalaujama, kad darbuotojas peržiūrės išlaidas, kad įvykdytų šią strategiją prieš pateikdama išlaidų ataskaitą arba kelionės paraišką.        
 
 - **Pagrindimas** – reikalaujama, kad darbuotojas arba vadovas pateiktų paaiškinimą, kad viršytų politikos sumą prieš pateikdami išlaidų ataskaitą arba kelionės paraišką.        

## <a name="policy-tips"></a>Strategijos patarimai
Pateikiame kelis pasiūlymus, kurie gali padėti jums kuriant naujas išlaidų valdymo strategijas: 

- Strategijos yra datos efektyvios, o tai reiškia, kad strategija neįsigalios, jei ji bus sukurta naudojant datą, kai sąskaita įvyko. Pavyzdžiui, šiuo metu kuriate naują strategiją, kad būtų užtikrintas maksimalus $50. Visos iš vakar įvedamos išlaidos nebus tikrinamos pagal šią strategiją.
- Kurdami išlaidų kategorijos, kurią galima detaliai, strategiją, galite įtraukti sąlygą dėl išlaidų eilutės tipo. Kai kurios strategijos, pvz., gavimo reikalavimas, gali būti neprašomos detaliam detalizavimui. Tokiu atveju strategija taikoma tik antraštės eilutei arba nedetalizuotai eilutei. 
- Pagal numatytuosius nustatymus išlaidų valdymo strategijos yra vertinamos pagal šaltinio objektą. Jei naudojate vidinės įmonės scenarijus, galite nustatyti, kad strategija būtų vertinama pagal paskirties objektą (skolinimosi objektas). Norėdami vykdyti strategijas pagal paskirties objektą, įjunkite **Vertinti išlaidų strategiją prieš skolindami juridinį objektą** funkciją **Funkcijų valdymo** darbo srityje.

## <a name="when-to-evaluate-policies"></a>Kada vertinti strategijas

Išlaidų valdymo parametruose galite pažymėti, kad, įrašius eilutę arba pateikus išlaidų ataskaitą, išlaidų valdymo strategijos būtų įvertintos. Jei pasirinksite įvertinti, kada eilutė bus įrašyta, vartotojai galės anksčiau matyti, ką reikia daryti norint iš karto užbaigti savo išlaidų ataskaitą. Kitu atveju galite atidėti strategijos įvertinimą ir sutaupyti laiko, kol jis nepasibaigs pateikimo darbo eigos metu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]