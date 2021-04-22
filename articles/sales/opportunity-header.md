---
title: Galimybės antraštė / suvestinė
description: Šioje temoje pateikta informacija apie projektu pagrįstų sandorių ir projektu pagrįstų galimybių eilutes.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ab8016014c0af60d1c0dfd37fdd457f279fb8059
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664099"
---
# <a name="header-details-for-project-based-opportunities"></a>Projektu pagrįstų galimybių antraštės išsami informacija

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_


Galimybės antraštėje arba suvestinėje užfiksuojama bendra informacija apie projektu pagrįstą sandorį, taikoma visoms projektu pagrįstos galimybės eilutėms.

„Dynamics 365 Project Operations“ projektu pagrįstos galimybės yra „Dynamics 365 Sales“ galimybių plėtiniai. Šie plėtiniai suteikia papildomų funkcijų, būdingų ir būtinų projektu pagrįstoms galimybėms. Šiuose plėtiniuose gali būti naujų laukų ir juostelės veiksmų, galimų naudojant projektu pagrįstas galimybes. Galite rasti kelis laukus, funkcijas ir numatytą logiką, kurie yra „Sales“, bet kurių nėra „Project Operations“.

Toliau pateiktoje lentelėje yra projektu pagrįstų galimybių laukai, kurie yra unikalūs „Project Operations“ arba kuriuose gali būti kai kurių svarbių pakeitimų, atsižvelgiant į „Sales“ galimybes.

| **Laukas** | **Vieta** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Tipas | Bendros informacijos skirtukas (paslėptas) | Šis parinkčių rinkinio laukas turi šias parinktis:</br>- Darbu pagrįsta (veikia tik su „Project Operations“)</br>- Elementu pagrįsta (yra tik jei turite įsidiegę „Project Operations“ ir „Sales")</br>- Pagrįstas aptarnavimo priežiūra (yra, kai įdiegta „Field Service“) | Kai naudojate „Project Operations“, ši lauko reikšmė automatiškai nustatoma kaip **Darbu pagrįsta**, kuri galimybę suklasifikuoja kaip projektu pagrįstą. Galimybė turi būti pagrįsta projektu, kad būtų galima įjungti visus su projektu susijusius išplėtimus ir funkcijas tolesniuose šio sandorio procesuose. |
| Įmonė, kuriai priklauso | Bendros informacijos skirtukas | Tai yra įmonė arba juridinis asmuo, kuris teiks klientui projektą. | Ši lauko informacija bus nukopijuota į atitinkamą projekto pasiūlymo lauką, sukurtą pagal šią galimybę. |
| Susisiekite | Bendros informacijos skirtukas | Nuoroda į kliento pirminį šio sandorio kontaktą. | |
| Abonementas | Bendros informacijos skirtukas | Nurodo į kliento įmonę arba kliento įrašą. | |
| Klientų tvarkytuvas | Bendros informacijos skirtukas | Šios projektu pagrįstos galimybės klientų vadybininko vardas. | Klientų vadybininkas yra atsakingas už ryšių su klientu viso projekto metu valdymą. Remiantis rezervuojamų išteklių įrašo susiejimu su klientų vadybininku, sutartį sudarantis vienetas laikomas numatytuoju. |
| Sutartį sudarantis vienetas | Bendros informacijos skirtukas | Organizacijos vienetas, atsakingas už su šiuo sandoriu susijusio projekto arba projektų pristatymą. | Sutartį sudarantis vienetas yra įmonės padalinys, kuris vykdys projektus po to, kai sandoris bus uždarytas. Kiekvienas sutartį sudarantis vienetas turi valiutą, o ši valiuta naudojama projekto metu padarytoms sąmatinėms ir faktinėms išlaidoms. |

Jei naudojate visus kitus galimybės skirtuko **Suvestinė** laukus ir skyrius, žr. [Galimybių kūrimas arba redagavimas („Sales“ ir „Sales“ telkinys)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
