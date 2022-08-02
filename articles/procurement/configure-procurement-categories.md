---
title: Įsigijimo kategorijų naudojimas su projekto pirkimo užsakymais ir laukiančiomis tiekėjo SF
description: Šiame straipsnyje aprašoma, kaip konfigūruoti įsigijimo kategorijas, kurias galima naudoti su projekto pirkimo užsakymais ir laukiančiomis tiekėjo SF.
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
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Įsigijimo kategorijų naudojimas su projekto pirkimo užsakymais ir laukiančiomis tiekėjo SF

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Pirkimo profesionalai gali kurti ir tvarkyti prekių ir paslaugų, kurias galima naudoti projekto pirkimo užsakymuose ir laukiančiose tiekėjo SF, katalogus. [Įsigijimo katalogai](/dynamics365/supply-chain/procurement/procurement-catalogs) suteikia paprastą būdą suskirstyti pirkinius į kategorijas nekonfigūruojant ir nenaudojant išleistų produktų katalogo. Kiekvieną įsigijimo kategoriją galima susieti su projekto kategorija laiko, išlaidų ar prekių operacijoms. Užregistravus laukiančią tiekėjo SF, kuri naudoja įsigijimo kategoriją, sistema sukurs laiko, išlaidų arba reikšmingų projekto faktinių duomenų, projekto operacijų ir papildomos knygos įrašų kūrimą.

## <a name="minimum-version-requirements"></a>Minimalūs versijos reikalavimai

Norint naudoti įsigijimo kategorijas su projekto pirkimo užsakymais scenarijams, skirtiems "Microsoft" Dynamics 365 Project Operations ne atsargų / ištekliais pagrįstiems scenarijams, reikalingos šios versijos:

- "Project Operations" Dataverse sprendimo 4.41.0.45 arba naujesnė versija
- Finansų ir operacijų aplinkos 10.0.26 arba naujesnė versija

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Paleiskite dvigubo rašymo žemėlapius įsigijimo kategorijos palaikymui

Įsitikinkite, kad "Project Operations" integravimo projekto tiekėjo SF eilutės eksportavimo objekto msdyn **projectvendorinvoicelines susiejimas \_** naudoja 1.0.0.4 arba naujesnę versiją.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Įgalinkite funkcijų raktą įsigijimo kategorijoms

Atlikite šiuos veiksmus, kad įgalintumėte įsigijimo kategorijų naudojimo su projekto pirkimo užsakymais funkciją.

1. Dynamics 365 Finance atidarykite **darbo sritį Funkcijų valdymas**.
1. Funkcijų sąraše raskite funkciją Naudoti įsigijimo **kategorijas programoje "Project Operations for resource based/ non-stocked scenarios"**, tada pasirinkite **Įgalinti**.

> [!IMPORTANT]
> Kaip būtinąją sąlygą taip pat turite įjungti **funkciją Įgalinti laukiančias tiekėjo sąskaitas faktūras "Project Operations", kad būtų galima pagrįsti ištekliais / be atsargų scenarijų**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projektų kategorijų susiejimas įsigijimo kategorijų hierarchijoje

Norėdami susieti projektų kategorijas su įsigijimo kategorijomis įsigijimo **kategorijų** hierarchijoje, atlikite šiuos veiksmus:

1. Eikite į **Pirkimo ir pirkimo \> kategorijos**.
1. Pasirinkite **Redaguoti kategorijų hierarchiją**.
1. Pasirinkite norimą kategorijų hierarchijos mazgą, tada skirtuke **Priskirti projekto kategorijas** susiekite mazgą su projekto kategorija iš **kategorijos Laikas**, **Išlaidos** arba **Elemento projektas** (t. y. **kategorijos Numatytasis laikas arba Numatytasis laikas** arba **Numatytosios išlaidos**).
1. Pasirinkite **Įrašyti**.
1. Uždarykite puslapį.

> [!NOTE]
> Pirkimo kategorijos susiejimas su projekto kategorija yra neprivalomas. Jei įsigijimo kategorija nesusieta, sistema naudos reikšmę, nustatytą **puslapio Projekto valdymo ir apskaitos parametrai skirtuko** Project Operations on Dynamics **365 Customer engagement (Project Operations on Dynamics 365 Customer engagement)** sekcijos Lauke Prekė **, esančiame** skyriuje **Projekto kategorijos numatytieji nustatymai**.
