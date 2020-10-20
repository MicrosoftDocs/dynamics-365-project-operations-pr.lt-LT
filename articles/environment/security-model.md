---
title: Saugos modelis
description: Šioje temoje pateikiama informacija apie saugos modelį programoje „Dynamics 365 Project Operations“.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ffcfa8a9c8e31c5665acd3c3919fa90d36a3f3ca
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896741"
---
# <a name="security-model"></a>Saugos modelis

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Microsoft Dynamics 365 Project Operations“ turi unikalų saugos modelį, leidžiantį naudoti vaidmenis pagrįstą verslo saugos modelį, suderintą su „Microsoft Office“ grupėmis. 


## <a name="security-roles"></a>Saugos vaidmenys
„Project Operations“ sąsajos galimybės apima šiuos vaidmenis:

| Vaidmuo                          | Aprašo                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Praktikos vadovas              | Teikia su projektais susijusias ataskaitas.                                                                                                            | Verslo vienetas              |
| Projekto tvirtintojas              | Patvirtina projekto laiką ir išlaidas.                                                                                                                              | Verslo vienetas |
| Projekto atsiskaitymo administratorius | Kuria sąskaitos faktūros pasiūlymą.                                                                                                                                                 | Verslo vienetas |
| Projekto vadovas               | Kuria projekto planą ir prašo išteklių.                                                                                                                              | Verslo vienetas |
| Projekto išteklius              | Komandos nariai, kuriuos galima rezervuoti ir nurodyti laiko sąnaudas.                                                                                                          | Verslo vienetas|
| Išteklių vadovas              | Visos išteklių valdymo funkcijos, pvz., vykdyti išteklių užklausas ir rezervavimus; atskirtas vaidmuo, palaikantis projekto vadovo ir išteklių vadovo konfigūraciją, ir vienas centralizuotas išteklių vadovo vaidmuo. | Verslo vienetas |


„Microsoft Project“ žiniatinkliui komponentas apima toliau nurodytus vaidmenis:
| Vaidmuo                          | Aprašo                                                                                                          | Scope |                                                       
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| „Project“ vartotojas | „Project“ bendradarbiaujantis vartotojas, galintis kurti savo projektus ir peržiūrėti bet kokius su juo bendrintus projektus.| Vartotojas|
| „Project“ sistema | Vaidmuo, naudojamas programos kontekste. Klientai neturėtų naudoti šio sistemos vaidmens. | Visuotinis|

## <a name="security-enforcement"></a>Saugos užtikrinimas
Projekto lygmeniu atliekami veiksmai atliekami prisijungusio vartotojo kontekste. Tai reiškia, kad norint kurti, atidaryti arba panaikinti projektą, vartotojas privalo turėti prieigą prie CDS. Prieiga prie CDS gali būti suteikta naudojant bet kuriuos galimus į platformą įtrauktus mechanizmus. Pavyzdžiui, vartotojas, turintis didesnės aprėpties teises, gali pasiekti projektą arba jei atliktas aiškus projekto bendrinimo veiksmas, kuris suteikia vartotojui prieigą.

Svarbu tai atsiminti kuriant projektus sistemoje „Project Operations“.

## <a name="modern-group-collaboration-with-project-operations"></a>Bendradarbiavimas naudojant modernias grupes sistemoje „Project Operations“
„Project“ žiniatinkliui ir „Project Operations“ palaiko modernių grupių funkciją, kad būtų galima bendradarbiauti. Vartotojai, įtraukti į projektą per grupę, gali redaguoti projekto planą.

Priskyrus „Project“ žiniatinkliui įtraukia vartotojus į grupę automatiškai.

Naudojant grupes galima bendrai dirbti su projekto teisėmis ir palaikomais bendradarbiavimo artefaktais. Toliau pateiktoje diagramoje pavaizduoti įvykiai ir būsenos pakeitimai, kurie įvyksta vykdant grupės priskyrimo procesą.

„Project Operations“ grupė nesukuriama atliekant netiesioginį veiksmą – grupė sukuriama tiesiogiai paspaudus grupes.

Dialogo lange **Grupės valdymas** galima ieškoti tik grupės narių, kurie nustatyti kaip priklausantys aplinkos saugos grupei. Daugiau informacijos žr. [Vartotojų prieigos prie aplinkos valdymas: saugos grupės ir licencijos](https://docs.microsoft.com/power-platform/admin/control-user-access).

1. Projektą sukuria vartotojas ir jis priklauso projektą sukūrusiam vartotojui.
2. Projekto savininkas atnaujinamas komandoje.
3. Savininko komanda susiejama su nurodyta ar sukurta „Office“ grupe.
4. Pirminis projekto savininkas įtraukiamas į „Office“ grupę.

## <a name="deployment-recommendation"></a>Visuotinio diegimo rekomendacija
„Office“ grupių bendradarbiavimo modelis nuolat tobulinamas, todėl laikui bėgant bus įtraukta naujų funkcijų, užtikrinančių tikslesnę kontrolę. Klientai, kurie diegia „Project Operations“ šiandien, skatinami sutelkti dėmesį į įprastą „Microsoft Dynamics 365“ saugos modelį.

Norėdami gauti daugiau informacijos žr. [Sauga sistemoje „Common Data Service“](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>„Project Operations“ ir „Microsoft Dynamics 365 Finance“ sauga
„Project Operations“ apima toliau nurodytus vaidmenis:

- Projekto vadovas
- Projekto apskaitininkas

Norėdami gauti daugiau informacijos apie „Finance“ saugą žr. [Vaidmenimis pagrįsta sauga](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


