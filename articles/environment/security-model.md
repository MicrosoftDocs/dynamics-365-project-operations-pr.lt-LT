---
title: Saugos modelis
description: Šiame straipsnyje pateikiama informacija apie saugos modelį programoje Dynamics 365 Project Operations.
author: stsporen
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2f4992b1ea0c2b93a83c6c2c9a146a7610afc5fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924532"
---
# <a name="security-model"></a>Saugos modelis

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_



„Microsoft Dynamics 365 Project Operations“ naudojamas unikalus saugos modelis, leidžiantis naudoti vaidmenimis pagrįstą veiklos saugos modelį, kuris veikia su „Microsoft Office“ grupėmis. 


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

| Vaidmuo           | Aprašo                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| „Project“ vartotojas   | „Project“ bendradarbiaujantis vartotojas, galintis kurti savo projektus ir peržiūrėti bet kokius su juo bendrintus projektus. | Vartotojas   |
| „Project“ sistema | Vaidmuo, naudojamas programos kontekste. Klientai neturėtų naudoti šio sistemos vaidmens.                                    | Visuotinis |

## <a name="security-enforcement"></a>Saugos užtikrinimas
Projekto lygmeniu atliekami veiksmai atliekami prisijungusio vartotojo kontekste. Tai reiškia, kad norint kurti, atidaryti arba panaikinti projektą, vartotojas privalo turėti prieigą prie CDS. Prieiga prie CDS gali būti suteikta naudojant bet kuriuos galimus į platformą įtrauktus mechanizmus. Pavyzdžiui, vartotojas, turintis didesnės aprėpties teises, gali pasiekti projektą arba jei atliktas aiškus projekto bendrinimo veiksmas, kuris suteikia vartotojui prieigą.

Svarbu tai atsiminti kuriant projektus sistemoje „Project Operations“.

## <a name="modern-group-collaboration-with-project-operations"></a>Bendradarbiavimas naudojant modernias grupes sistemoje „Project Operations“
„Project“ žiniatinkliui ir „Project Operations“ palaiko modernių grupių funkciją, kad būtų galima bendradarbiauti. Vartotojai, įtraukti į projektą per grupę, gali redaguoti projekto planą.

Priskyrus „Project“ žiniatinkliui įtraukia vartotojus į grupę automatiškai.

Naudojant grupes galima bendrai dirbti su projekto teisėmis ir palaikomais bendradarbiavimo artefaktais. Toliau pateiktoje diagramoje pavaizduoti įvykiai ir būsenos pakeitimai, kurie įvyksta vykdant grupės priskyrimo procesą.

„Project Operations“ grupė nesukuriama atliekant netiesioginį veiksmą – grupė sukuriama tiesiogiai paspaudus grupes.

Dialogo lange **Grupės valdymas** galima ieškoti tik grupės narių, kurie nustatyti kaip priklausantys aplinkos saugos grupei. Daugiau informacijos žr. [Vartotojų prieigos prie aplinkos valdymas: saugos grupės ir licencijos](/power-platform/admin/control-user-access).

![Grupės režimas.](./media/groupsmode.png)

1. Projektą sukuria vartotojas ir jis priklauso projektą sukūrusiam vartotojui.
2. Projekto savininkas atnaujinamas komandoje.
3. Savininko komanda susiejama su nurodyta ar sukurta „Office“ grupe.
4. Pirminis projekto savininkas įtraukiamas į „Office“ grupę.

## <a name="deployment-recommendation"></a>Visuotinio diegimo rekomendacija
„Office“ grupių bendradarbiavimo modelis nuolat tobulinamas, todėl laikui bėgant bus įtraukta naujų funkcijų, užtikrinančių tikslesnę kontrolę. Klientai, kurie diegia „Project Operations“ šiandien, skatinami sutelkti dėmesį į įprastą „Microsoft Dynamics 365“ saugos modelį.

Norėdami gauti daugiau informacijos žr. [Sauga sistemoje „Common Data Service“](/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Projekto operacijos ir Microsoft Dynamics 365 finansinis saugumas
„Project Operations“ apima toliau nurodytus vaidmenis:

- Projekto vadovas
- Projekto apskaitininkas

Norėdami gauti daugiau informacijos apie „Finance“ saugą žr. [Vaidmenimis pagrįsta sauga](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).




[!INCLUDE[footer-include](../includes/footer-banner.md)]