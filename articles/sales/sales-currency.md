---
title: Valiuta
description: Šioje temoje pateikta informacija apie tai, kaip įtraukti ir pašalinti valiutos tipus programoje „Project Operations“.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1db7e76dbb220954b9f9088b2168eed1a1902abc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080868"
---
# <a name="currency"></a>Valiuta

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Pagal valiutas produktų kataloge nustatomos produktų kainos ir transakcijų, pvz., pardavimo užsakymų, išlaidos. Jei jūsų klientai yra skirtingose geografinėse vietovėse, įtraukite jų valiutas ir valdykite savo operacijas. Įtraukite valiutas, kurios labiausiai tinka jūsų dabartiniams ir būsimiems verslo poreikiams.  

> [!NOTE]
> Jei jūsų aplinka yra „Common Data Service“ aplinka, jūs esate „Power Platform“ administravimo centre ir pasirenkate puslapį **Valiutos** ( **Aplinkos** > [pasirinkti aplinką] > **Parametrai** > **Verslas** > **Valiutos** ), puslapis bus tuščias. Taip yra todėl, kad aplinkose „Common Data Service“ valiutos nustatymas nepalaikomas.

## <a name="add-a-currency"></a>Valiutos įtraukimas  
Prieš pradėdami šią procedūrą patikrinkite, ar jūsų saugos vaidmuo yra sistemos administratoriaus teisės. 

1. Power Platform administravimo centre pasirinkite aplinką. 
2. Pasirinkite **Parametrai** > **Verslas**.
3. Pasirinkite **Valiutos**.  
4. Pasirinkite **Naujas**.  
5. Užpildykite informaciją, kaip nurodyta.  


   |          Laukas          |                                                                                                                                                                                                                                                                                                                                                                            Aprašas                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Valiutos tipas**    | - **Sistema** – pasirinkite šią parinktį, jei norite naudoti „Dynamics 365“ modeliu pagrįstose programose pateikiamas valiutas. Norėdami ieškoti valiutos, pasirinkite **Peržvalga**. Kai pasirenkate valiutos kodą, automatiškai įtraukiami pasirinktos **Valiutos pavadinimas** ir **Valiutos simbolis**.<br />- **Pasirinktinis** – pasirinkite šią parinktį, jei norite įtraukti „Dynamics 365“ modeliu pagrįstose programose nepateikiamą valiutą. Tokiu atveju turite patys įvesti reikšmes laukuose **Valiutos kodas** , **Valiutos tikslumas** , **Valiutos pavadinimas** , **Valiutos simbolis** ir **Valiutos konvertavimas**. |
   |    **Valiutos kodas**    |                                                                                                                                                                                                                                                                                                                                            Sutrumpinta valiutos pavadinimo forma. Pavyzdys: **USD** yra JAV doleris.                                                                                                                                                                                                                                                                                                                                            |
   | **Valiutos tikslumas**  |                                                                                                                                                                                  Įveskite norimą valiutos dešimtainių dalių skaičių.  Galite nurodyti reikšmę nuo 0 iki 4. **Pastaba.** Jei tikslumo reikšmę nustatote dialogo lange **Sistemos parametrai** , čia bus rodoma ta reikšmė.                                                                                                                                                                                  |
   |    **Valiutos pavadinimas**    |                                                                                                                                                                                                                                         Jei valiutos kodą pasirinkote iš „Dynamics 365“ modeliu pagrįstose programose esančio valiutų sąrašo, čia bus rodomas valiutos pavadinimas pagal pasirinktą kodą. Jei pasirinkote valiutos tipą **Pasirinktinis** , įveskite valiutos pavadinimą.                                                                                                                                                                                                                                          |
   |   **Valiutos simbolis**   |                                                                                                                                                                                                                                                                      Jei valiutos kodą pasirinkote iš galimų valiutų sąrašo, čia bus rodomas pasirinktos valiutos simbolis. Jei pasirinkote valiutos tipą **Pasirinktinis** , įveskite naujos valiutos simbolį.                                                                                                                                                                                                                                                                       |
   | **Valiutos konvertavimas** |                                                                                                                                                                                                                                     Įveskite pasirinktos valiutos vertę lyginant su vienu JAV doleriu. Ši suma nurodo, kiek pasirinktos valiutos vienetų kainuoja vienas pagrindinės valiutos vienetas. **Svarbu.** Būtinai naujinkite šią reikšmę taip dažnai, kaip reikia, kad operacijose nebūtų jokių netikslių skaičiavimų.                                                                                                                                                                                                                                      |


6. Pabaigę keitimus, komandų juostoje pasirinkite **Įrašyti** arba **Įrašyti ir uždaryti**.  

   > [!TIP]
   >  Norėdami redaguoti valiutą, pasirinkite valiutą ir tada įveskite arba pasirinkite naujas reikšmes.  

## <a name="delete-a-currency"></a>Valiutos naikinimas  

1. Power Platform administravimo centre pasirinkite aplinką. 
2. Pasirinkite **Parametrai** > **Verslas**.
3. Pasirinkite **Valiutos**.  
4. Rodomame valiutų sąraše pasirinkite valiutą, kurią norite naikinti.  
5. Pasirinkite **Naikinti**.  
6. Patvirtinkite naikinimą.  

> [!IMPORTANT]
>  Kitų įrašų naudojamų valiutų panaikinti negalima, bet jas galima išjungti. Išjungus valiutos įrašus, valiutos informacija iš esamų įrašų, pvz., galimybių arba užsakymų, nepašalinama. Tačiau jūs naujose operacijose nebegalėsite pasirinkti išjungtos valiutos.  
