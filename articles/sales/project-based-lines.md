---
title: Projektu pagrįstos galimybių eilutės
description: Šioje temoje pateikta informacija, kaip dirbti su projektu pagrįstomis galimybių eilutėmis.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b255d607ac8180c249a9b9831db6f8d0cd3937b
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898406"
---
# <a name="project-based-opportunity-lines"></a>Projektu pagrįstos galimybių eilutės

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_


Projektu pagrįstos galimybės eilutės pasiekiamos tik projektu pagrįstose galimybėse. Projektu pagrįsta galimybė, kurios lauko **Tipas** reikšmė nustatyta į **Pagrįstas darbu**.

Projektu pagrįstos galimybės eilutės yra eilutės elementai, kurie bus pristatomi klientui naudojant projektą. Tačiau projekto negalima susieti su projektu pagrįstos galimybės eilute. Projektai gali būti susieti su eilučių elementais iš etapo **Pasiūlymas**, nes paprastai galimybė vyksta ankstyvuoju sandorio etapu. Nustatymas, kiek projektų bus naudojama darbui klientui suteikti, yra sprendimas, padarytas vėliau pardavimo etape. Naudokite galimybės etapą, kad nustatytumėte atskirus kliento pristatymo komponentus. Sprendimus, susijusius su faktiniu šių komponentų pristatymo projektų skaičiumi, galima perkelti į priekį tol, kol bus žinoma daugiau informacijos apie patį darbą.

Žemiau yra laukai, esantys projektu pagrįstos galimybės eilutėje:

| **Laukas** | **Vieta** | **Atitiktis, tikslas ir gairės** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Produkto tipas | Bendros informacijos skirtukas (paslėptas) | Tai yra parinkčių rinkinio laukas. Jei turite įsidiegę „Dynamics 365 Operations", viena iš galimų parinkčių yra **Projektu pagrįsta paslauga**.  | Šio lauko reikšmė nustatoma kaip **Projektu pagrįsta paslauga**, kai galimybėje kuriate projektu pagrįstos galimybės eilutę pagal projektu pagrįstų eilučių tinklelį. <br> Jei šią reikšmę pakeisite arba perrašysite, projekto funkcijos nebus įjungtos jūsų projektu pagrįstų eilučių elementuose. |
| Galimybė | Bendros informacijos skirtukas | Šis laukas yra skirtas tik skaityti ir nurodo pirminį galimybės įrašą, kuriam priklauso šis eilutės elementas. | Nėra jokio tolesnio šio lauko poveikio. |
| Pavadinimas / vardas, pavardė | Bendros informacijos skirtukas | Tai yra redaguojamas teksto laukas, kurį galima naudoti norint pateikti trumpą šio eilutės elemento identifikaciją. | Ši reikšmė perkeliama į pasiūlymo eilutę, kai kuriate pasiūlymą iš šios galimybės |
| Kliento biudžetas | Bendros informacijos skirtukas | Šis redaguojamas valiutos laukas gali būti naudojamas norint sekti sumą, kurią klientas nori išleisti šiam eilutės elementui. | Ši reikšmė perkeliama į atitinkamą pasiūlymo lauką, kai kuriate pasiūlymą iš šios galimybės |
| Atsiskaitymo metodas | Bendros informacijos skirtukas | Šis redaguojamas laukas gali turėti tokias reikšmes:</br>- Laikas ir medžiaga</br>- Fiksuota kaina | Ši reikšmė perkeliama į atitinkamą pasiūlymo lauką, kai kuriate pasiūlymą iš šios galimybės. Sukūrus pasiūlymo eilutę laukas užrakinamas ir jo negalima keisti. Šiam laukui reikšmę priskirkite kaip įmanoma tiksliau. Jei norite pakeisti šio lauko reikšmę pasiūlymo eilutėje, panaikinkite ir iš naujo sukurkite pasiūlymo eilutę. |
