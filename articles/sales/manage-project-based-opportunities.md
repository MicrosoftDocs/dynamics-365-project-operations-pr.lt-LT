---
title: Projektais pagrįstų galimybių valdymas
description: Šioje temoje pateikta informacija apie tai, kaip naudoti su projektais susijusias galimybes.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 39ce52d5da4c7027ee2f2fa44579c0d4bf74925e
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088019"
---
# <a name="manage-project-based-opportunities"></a>Projektais pagrįstų galimybių valdymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projektų pagrindu dirbančios įmonės paprastai savo pristatymo operacijas vykdo keliose šalyse ir vietovėse. Projekto vykdymo ir pristatymo kaina gali skirtis atsižvelgiant į tai, kuri vietovė arba padalinys vykdo pristatymą. Savo ruožtu tai gali paveikti sandorio maržas. Projektais pagrįstų paslaugų pristatymas paprastai apima didelius personalo laiko kiekius, dideles kelionių išlaidas, materialines išlaidas ir kitas išlaidas.

Projektais pagrįstos „Dynamics 365 Project Operations" galimybės yra sukurtos su „Dynamics 365 Sales“ plėtiniais. Šioje temoje pateikta išsami informacija apie įvairius laukus ir verslo logiką, kuri įtraukta į papildomas funkcijas, kurių reikalauja projektais pagrįstose įmonėse, kad būtų galima valdyti projektais pagrįstas galimybes.

## <a name="view-all-project-based-opportunities"></a>Visų projektais pagrįstų galimybių peržiūra

Visų projektais pagrįstų galimybių sąrašą galima peržiūrėti sąrašo puslapyje **Galimybės**. 

1. Eikite į **Pardavimas** > **Galimybės**.
2. Naudodami **rodinių perjungiklį** pasirinkite kitus filtruotuosius galimybių rodinius. Galite sukurti savo rodinius su pasirinktiniais filtravimo kriterijais ir sukonfigūruoti šiuos rodinius bei naršymo parinktis.

Projekto galimybes galima kurti arba naikinti iš šio sąrašo puslapio arba išsamios informacijos puslapio.

## <a name="business-process-flow-for-project-based-deals"></a>Projektu pagrįstų sandorių veiklos procesų seka

„Project Operations“ palaikomos tokios projektu pagrįstų sandorių veiklos procesų sekos:

- Galimas klientas į galimybės veiklos procesą
- Galimybės pardavimo procesas

### <a name="lead-to-opportunity-business-process"></a>Veiklos procesas nuo galimo kliento iki galimybės 
Veiklos procesas nuo galimo kliento iki galimybės palaiko šiuos etapus.

| Etapas | Susietas objektas | Funkcija |
| --- | --- | --- |
| Patvirtinti tinkamumą | Galimas klientas | Galimo kliento patvirtinimas, kad būtų sukurtas klientas, kontaktass ir galimybė. |
| Kurti | Galimybė | Sukurkite galimybę, kad būtų įtraukta daugiau informacijos apie susijusį darbą, svarbiausias suinteresuotąsias šalis ir konkurenciją. |
| Siūlyti | Galimybė | Sukurkite pasiūlymą ir gaukite vidinės peržiūros komandos patvirtinimą. |
| Uždaryti objektą  | Galimybė | Laimėkite galimybę, kad uždarytumėte sandorį. |

### <a name="opportunity-sales-process"></a>Galimybės pardavimo procesas
„Project Operations“ galimybės pardavimo procesas yra galimybės pardavimo proceso veiklos srauto plėtinys „Sales“ programoje. Šis veiklos procesas sukurtas parengtas naudoti, kad būtų palaikomi toliau nurodyti projektais pagrįstos galimybės etapai.

| Etapas | Susietas objektas | Funkcija |
| --- | --- | --- |
| Patvirtinti tinkamumą | Galimybė | Galimo kliento patvirtinimas, kad būtų sukurtas klientas, kontaktass ir galimybė. |
| Siūlyti | Pasiūlymas | Sukurkite pasiūlymą naudodami projektų pasiūlymus ir gaukite vidinės peržiūros komandos patvirtinimą. |
| Sutartis | Projekto sutartis | Laimėkite pasiūlymą ir sukurkite sutartį bei pradėkite projekto vykdymą ir pristatymą. |
| Uždaryti objektą  | Projekto sutartis | Sėkmingai baikite darbą ir uždarykite projekto sutartį. |

> [!NOTE]
> Jei jūsų projektais pagrįstas sandoris pradėtas su klientu, pirmenybė teikiama veiklos procesui nuo galimo kliento iki galimybės.
>
> Jei jūsų projektais pagrįstas sandoris pradėtas su galimybe, pirmenybė teikiama galimybės pardavimo procesui.

Norėdami pagal poreikį sekti pardavimo procesą, galite redaguoti produkto veiklos procesų seką arba kurti savo verslo procesų sekas. Daugiau informacijos apie veiklos procesų seką žr. [Veiklos procesų sekų apžvalga](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).
