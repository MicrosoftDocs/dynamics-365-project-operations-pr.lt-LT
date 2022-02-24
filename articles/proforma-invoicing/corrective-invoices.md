---
title: Pakoreguotos sąskaitos faktūros
description: Šioje temoje pateikta informacija apie koreguotų sąskaitų faktūrų išrašymą.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122398"
---
# <a name="corrected-invoices"></a>Pakoreguotos sąskaitos faktūros

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Patvirtintas sąskaitas faktūras galima redaguoti. Pataisius patvirtintą sąskaitą faktūrą, sukuriama juodraštinė pakoreguota sąskaita faktūra. Kadangi daroma prielaida, kad norite atšaukti visas operacijas ir kiekius iš pradinės sąskaitos faktūros, į šią koreguotą sąskaitą faktūrą įeina visos operacijos iš pradinės sąskaitos faktūros, o visi joje esantys kiekiai yra nulis (0).

Kai operacijų taisyti nereikia, galite jas pašalinti iš juodraštinės koreguojamosios sąskaitos faktūros. Jei norite atšaukti arba grąžinti tik dalinį kiekį, galite redaguoti eilutės informacijos lauką „Kiekis“. Jei atidarote sąskaitos faktūros eilutės išsamią informaciją, galite peržiūrėti pradines sąskaitos faktūros kiekį. Tada galite redaguoti dabartinės sąskaitos faktūros kiekį, kad jis būtų mažesnis arba didesnis nei pradinės sąskaitos faktūros kiekis.

Patvirtinus koreguojamąją sąskaitą faktūrą, pradinis faktinis pardavimas, už kurį išrašyta sąskaita, yra atšaukiamas ir sukuriamas naujas faktinis pardavimas, už kurį išrašyta sąskaita. Jei kiekis sumažintas, dėl skirtumo taip pat bus sukuriamas naujas faktinis pardavimas, už kurį neišrašyta sąskaita. Pavyzdžiui, jei pradinio pardavimo, už kurį išrašyta sąskaita, kiekis yra aštuonios valandos, o koreguotos sąskaitos faktūros eilutės išsamioje informacijoje nurodomas sumažintas šešių valandų kiekis, pradinio pardavimo, už kurį išrašyta sąskaita faktūra, eilutė atšaukiama ir sukuriami du nauji faktiniai duomenys:

- Šešių valandų faktinis pardavimas, už kurį išrašyta sąskaita.
- Likusių dviejų valandų faktinis pardavimas, už kurį neišrašyta sąskaita. Šiai operacijai vėliau galima išrašyti sąskaitą arba pažymėti ją kaip neapmokestinamąją, atsižvelgiant į derybas su klientu.
