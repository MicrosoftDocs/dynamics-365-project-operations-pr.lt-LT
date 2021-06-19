---
title: Projektų kainoraščių valdymas projekto sutartyse
description: Šioje temoje pateikiama informacija apie projekto kainoraščius projekto sutartyse.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3313eef74b5e7a0624b32d2a336cd986dfdda839
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010391"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Projektų kainoraščių valdymas projekto sutartyse

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projekto sutartys programoje „Dynamics 365 Project Operations“ sukurtos siekiant palaikyti kelis nuo datos priklausančius sutarties pardavimo kainoraščius. Programoje „Project Operations“ yra naujas susietasis objektas, vadinamas **projekto kainoraščiais**. Šis objektas su projekto sutartimi yra susijęs ryšiu „vienas su daugeliu“.

Projekto kainoraščiai naudojami norint nustatyti kainą už laiką, medžiagą ir išlaidų operacijas. Kai sutartyje yra vienas ar keli projekto kainoraščiai, šie kainoraščiai naudojami norint nustatyti kainą už laiką, medžiagą, išlaidų sąmatas ir faktinius duomenis, priklausančius projektams, susietiems su sutartimi sutarties eilutėje.

Kai projekto sutartyje projekto kainoraščių nėra, matysite įspėjamąjį pranešimą, kad nėra projekto kainoraščių, o jūsų užregistruotoms sąmatos, faktiniams projekto darbams, medžiagai ir išlaidoms kaina nebus nustatyta. Nebus nustatyta pardavimo verčių kaina.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Projekto sutarties kainoraščio susiejimas arba atsiejimas

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Konkretaus kainoraščio kūrimas arba susiejimas norint įvertinti projektu pagrįstą darbą, medžiagą ir išlaidas

1. Projekto sutartyje pasirinkite skirtuką **Projekto kainoraščiai**.
2. Papildomame tinklelyje pasirinkite **+ Įtraukti naują projekto kainoraštį**.
3. Slankiklyje **Spartusis kūrimas** pažymėkite kainoraštį. 

  Išplečiamajame sąraše rodomi visi kainoraščiai, kuriuose kontekstas nustatytas kaip **Pardavimas**, o kainoraščio valiuta atitinka sutarties valiutą.
  
4. Įveskite projekto kainoraščio susiejimo aprašą, pasirinkite **Įrašyti**, tada uždarykite slankiklį **Spartusis kūrimas**.

   Sukuriamas projekto kainoraščio susiejimas.
   
5. Pakartokite 1–4 veiksmus, kad susietumėte daugiau nei vieną projekto kainoraštį su projekto sutartimi. Kelis projekto kainoraščius kurkite, tik jei kiekvienas susietas projekto kainoraštis galioja skirtingomis datomis.

> [!NOTE]
> „Project Operations“ nepalaiko projekto kainoraščių galiojimo datų persidengimo. Jei konkrečią dieną operacijai galioja keli projekto kainoraščiai, tai operacijai nustatoma numatytoji nulinė kaina.

### <a name="remove-a-project-price-list-association"></a>Projekto kainoraščio susiejimo pašalinimas

- Pasirinkite projekto kainoraštį, tada papildomame tinklelyje pasirinkite **Naikinti sutarties projekto kainoraštį**. 

  Kainoraštis pašalinamas iš sutarties projekto kainoraščių. Pats kainoraštis nebus panaikintas. Panaikinamas tik susiejimas su sutartimi.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Projekto kainoraščių automatinio nustatymo numatytaisiais sąranka

Projekto kainoraštį galima nustatyti kaip numatytąjį projekto kainoraštį. Ši sąranka užtikrina, kad visos jūsų organizacijos sutartys visada būtų pradedamos nuo standartinio tam kainų laikotarpiui taikomo kainoraščio.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Projekto numatytojo kainoraščio organizacijoje nustatymas

1. Nueikite į **Parametrai** > **Bendra**, tada pasirinkite **Parametrai**.
2. Sąrašo puslapyje **Aktyvieji parametrai** pažymėkite ir dukart spustelėkite įrašą, kad jį atidarytumėte. Dukart spustelėdami, įsitikinkite, kad nespustelėjote lauko reikšmės, kuri yra hipersaitas. 
3. Puslapyje **Aktyvieji parametrai** pažymėkite skirtuką **Kainoraštis**. Papildomame tinklelyje rodomas numatytųjų kainoraščių sąrašas. Tai yra standartinių kaštų ir pardavimo kainoraščių sąrašas. Jei čia **pardavimo** kainoraštis susietas su kiekviena valiuta, kuria parduodate, užtikrinama, kad šis pardavimo kainoraštis būtų numatytasis bet kurioje sutartyje, kurią kuriate klientams, prekiaujantiems šia valiuta.

### <a name="set-up-a-customer-specific-project-price-list"></a>Konkrečiam klientui taikomui projekto kainoraščio nustatymas

Konkretiems klientams taikomus kainoraščius taip pat galite nustatyti, kai su klientais susiderėjote dėl pagrindinės kainų sutarties.

1. Eikite į **Pardavimas** > **Klientai**.
2. Aktyvių klientų sąraše pažymėkite klientą, kuriam turite specialų kainoraštį.
3. Pažymėkite kliento įrašą, kad jį atidarytumėte, ir pasirinkite skirtuką **Projekto kainoraščiai**. Papildomame tinklelyje rodomas konkrečiai šiam klientui taikomų projekto kainoraščių sąrašas. 
4. Čia sukurkite naują kainoraščio susiejimą, kad turėtumėte konkrečiai šiam klientui skirtą projekto kainoraštį.

## <a name="custom-pricing-on-a-project-contract"></a>Pasirinktinė kainodara projekto sutartyje

Kai turite organizacinius ir konkretiems klientams taikomus projekto kainoraščius, jūsų projekto sutartys bus sukurtos automatiškai susiejant šiuos projekto kainoraščius. Tačiau projekto kainoraščiai projekto sutartyje visada kopijuojami prie jų nurodant datą ir sutarties pavadinimą. Tada klientų ir projektų vadovai gali pradėti redaguoti šių kopijų kainas. Šios pakeistos kainos bus taikomos tik šiai projekto sutarčiai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
