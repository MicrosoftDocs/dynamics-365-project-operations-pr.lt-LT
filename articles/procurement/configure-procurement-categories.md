---
title: Įsigijimo kategorijų naudojimas projekto pirkimo užsakymuose ir laukiančiose tiekėjo sąskaitose faktūrose
description: Šiame straipsnyje aprašoma, kaip konfigūruoti įsigijimo kategorijas, kurias galima naudoti su projekto pirkimo užsakymais ir laukiančiomis tiekėjo sąskaitomis faktūromis.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028620"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Įsigijimo kategorijų naudojimas projekto pirkimo užsakymuose ir laukiančiose tiekėjo sąskaitose faktūrose

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Pirkimo specialistai gali kurti ir tvarkyti prekių ir paslaugų, kurias galima naudoti pirkimo užsakymuose ir laukiančiose tiekėjo sąskaitose faktūrose, katalogus. [Įsigijimo katalogai](/dynamics365/supply-chain/procurement/procurement-catalogs) suteikia paprastą būdą suskirstyti pirkinius į kategorijas, nekonfigūruojant ir nenaudojant išleistų produktų katalogo. Kiekvieną įsigijimo kategoriją galima susieti su projekto kategorija pagal laiką, išlaidas ar elementų operacijas. Kai užregistruojama laukianti tiekėjo sąskaita faktūra, kurioje naudojama įsigijimo kategorija, sistema sukuria laiko, išlaidų arba medžiagos projekto faktinius duomenis, projekto operacijas ir papildomos knygos įrašus.

## <a name="minimum-version-requirements"></a>Minimalios būtinos versijos

Toliau nurodytos versijos yra būtinos norint įsigijimo kategorijas naudoti su projektų pirkimo užsakymais „Microsoft Dynamics 365 Project Operations“ atsargose nelaikomų medžiagų / išteklių scenarijuose:

- „Project Operations Dataverse“ sprendimo 4.41.0.45 arba naujesnė versija
- Finansų ir operacijų aplinkos 10.0.26 arba naujesnės versija

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Dvigubo rašymo schemų vykdymas norint palaikyti įsigijimo kategorijas

Įsitikinkite, kad **„Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eilučių eksportavimo objektas msdyn\_projectvendorinvoicelines** susiejimas naudoja 1.0.0.4 arba naujesnę versiją.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Funkcijų rakto įjungimas norint naudoti įsigijimo kategorijoms

Atlikite toliau nurodytus veiksmus, kad įjungtumėte įsigijimo kategorijų naudojimo su projekto pirkimo užsakymais funkciją.

1. Programoje „Dynamics 365 Finance“ atidarykite darbo sritį **Funkcijų valdymas**.
1. Funkcijų sąraše raskite funkciją **Naudoti įsigijimo kategorijas „Project Operations“ išteklių / atsargose nelaikomų medžiagų scenarijuose**, tada pasirinkite **Įjungti**.

> [!IMPORTANT]
> Taip pat būtina įjungti funkciją **Leisti „Project Operations“ išteklių / atsargose nelaikomų medžiagų scenarijuose naudoti laukiančias tiekėjų sąskaitas faktūras**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projekto kategorijų susiejimas įsigijimo kategorijų hierarchijoje

Atlikite šiuos veiksmus, kad susietumėte projekto kategorijas su įsigijimo kategorijomis, esančiomis **Įsigijimo kategorijų** hierarchijoje:

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas \> Įsigijimo kategorijos**.
1. Pasirinkite **Redaguoti kategorijų hierarchiją**.
1. Pasirinkite norimą kategorijų hierarchijos mazgą, tada skirtuke **Priskirti projekto kategorijas** susiekite mazgą su projekto kategorija iš kategorijos **Laikas**, **Išlaidos** arba **Projekto elementas** (t. y. kategorija **Numatytasis laikas** arba **Numatytosios išlaidos**).
1. Pasirinkite **Įrašyti**.
1. Uždarykite puslapį.

> [!NOTE]
> Įsigijimo kategorijos susiejimas su projekto kategorija yra pasirinktinis. Jei įsigijimo kategorija nebus nesusieta, sistema naudos reikšmę, nustatytą lauke **Elementas**, esančiame skyriuje **Projekto kategorijos numatytieji nustatymai**, kuris yra skirtuke **“Project Operations“ programoje „Dynamics 365 Customer Engagement“**, esančiame puslapyje **Projektų valdymo ir apskaitos parametrai**.
