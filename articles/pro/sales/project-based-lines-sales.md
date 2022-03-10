---
title: Projektu pagrįstos galimybių eilutės – „Lite“ versija
description: Šioje temoje pateikta informacija apie projektu pagrįstos galimybės eilutes. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1978b452b84486cabd5b6b4e550261e2c8f76cd89a140709b137ac184c8967c1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999011"
---
# <a name="project-based-opportunity-lines---lite"></a>Projektu pagrįstos galimybių eilutės – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projektu pagrįstos galimybės eilutės pasiekiamos tik projektu pagrįstose galimybėse. Projektu pagrįsta galimybė, kurios lauko **Tipas** reikšmė nustatyta į **Pagrįstas darbu**.

Projektu pagrįstos galimybės eilutės yra eilutės elementai, kurie bus pristatomi klientui naudojant projektą. Tačiau projekto negalima susieti su projektu pagrįstos galimybės eilute. Projektai gali būti susieti su eilučių elementais iš etapo **Pasiūlymas**, nes paprastai galimybė vyksta ankstyvuoju sandorio ciklo etapu. Nustatymas, kiek projektų bus naudojama darbui klientui suteikti, yra sprendimas, padarytas vėliau pardavimo etape. Galite naudoti galimybės etapą, kad nustatytumėte atskirus kliento pristatymo komponentus. Sprendimus, susijusius su faktiniu šių komponentų pristatymo projektų skaičiumi, galima perkelti į priekį tol, kol bus žinoma daugiau informacijos apie patį darbą.

Žemiau yra laukai, esantys projektu pagrįstos galimybės eilutėje:

| **Laukas** | **Vieta** | **Aprašas** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Produkto tipas | Bendros informacijos skirtukas (paslėptas) | Galite pasirinkti vieną iš šių parinkčių:</br>– Projektais pagrįsta paslauga (galima tik įdiegus „Dynamics 365 Project Operations“)</br>- Produktas (yra tik jei turite įsidiegę „Project Operations“ ir „Dynamics 365 Sales") | Šio lauko reikšmė nustatoma kaip **Projektu pagrįsta paslauga**, kai galimybėje kuriate projektu pagrįstos galimybės eilutę pagal projektu pagrįstų eilučių tinklelį. <br> Jei šią reikšmę pakeisite arba perrašysite, projekto funkcijos nebus įjungtos jūsų projektu pagrįstų eilučių elementuose. |
| Galimybė | Bendros informacijos skirtukas | Šis laukas yra skirtas tik skaityti ir nurodo pirminį galimybės įrašą, kuriam priklauso šis eilutės elementas. | Nėra jokio tolesnio šio lauko poveikio. |
| Pavadinimas / vardas, pavardė | Bendros informacijos skirtukas | Tai yra redaguojamas teksto laukas, kurį galima naudoti norint pateikti trumpą šio eilutės elemento identifikaciją. | Ši reikšmė perkeliama į pasiūlymo eilutę, kai kuriate pasiūlymą iš šios galimybės. |
| Kliento biudžetas | Bendros informacijos skirtukas | Šis redaguojamas valiutos laukas gali būti naudojamas norint sekti sumą, kurią klientas nori išleisti šiam eilutės elementui. | Ši reikšmė perkeliama į atitinkamą pasiūlymo lauką, kai kuriate pasiūlymą iš šios galimybės. |
| Atsiskaitymo metodas | Bendros informacijos skirtukas | Šis redaguojamas laukas gali turėti tokias reikšmes:</br>- Laikas ir medžiaga</br>- Fiksuota kaina | Ši reikšmė perkeliama į atitinkamą pasiūlymo lauką, kai kuriate pasiūlymą iš šios galimybės. Sukūrus pasiūlymo eilutę laukas užrakinamas ir jo negalima keisti. Šiam laukui reikšmę priskirkite kaip įmanoma tiksliau. Jei norite pakeisti šio lauko reikšmę pasiūlymo eilutėje, panaikinkite ir iš naujo sukurkite pasiūlymo eilutę. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]