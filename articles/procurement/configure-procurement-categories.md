---
title: Naudoti įsigijimo kategorijas su projekto pirkimo užsakymais ir laukiančiomis tiekėjo SF
description: Šioje temoje aprašoma, kaip konfigūruoti įsigijimo kategorijas, kurias galima naudoti su projekto pirkimo užsakymais ir laukiančiomis tiekėjo SF.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613361"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Naudoti įsigijimo kategorijas su projekto pirkimo užsakymais ir laukiančiomis tiekėjo SF

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Pirkimo specialistai gali kurti ir tvarkyti prekių ir paslaugų katalogus, kuriuos galima naudoti projekto pirkimo užsakymuose ir laukiančiose tiekėjo SF. [Įsigijimo katalogai](/dynamics365/supply-chain/procurement/procurement-catalogs) suteikia jums paprastą būdą suskirstyti pirkimus į kategorijas, nereikia konfigūruoti ir naudoti išleistų produktų katalogo. Kiekvieną įsigijimo kategoriją galima susieti su laiko, išlaidų ar prekių operacijų projekto kategorija. Užregistravus laukiančią tiekėjo SF, kuri naudoja įsigijimo kategoriją, sistema sukurs laiko, išlaidų ar medžiagų projekto faktinius duomenis, projekto operacijas ir subklasto įrašus.

## <a name="minimum-version-requirements"></a>Minimalūs versijos reikalavimai

Norint naudoti įsigijimo kategorijas su projekto pirkimo užsakymais, skirtais "Microsoft" Dynamics 365 Project Operations nelaikomiems / ištekliui pagrįstiems scenarijams, reikia naudoti šias versijas:

- "Project Operations" Dataverse sprendimo versija 4.41.0.45 arba naujesnė versija
- Finansų ir operacijų aplinkos versija 10.0.26 arba naujesnė versija

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Vykdyti įsigijimo kategorijos palaikymo dvigubo rašymo žemėlapius

Įsitikinkite, kad "Project Operations" integravimo projekto tiekėjo SF eilutės eksportavimo objekto msdyn **projectvendorinvoicelines\_ susiejimas** naudoja versiją 1.0.0.4 arba vėlesnę versiją.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Įgalinti įsigijimo kategorijų priemonės raktą

Atlikite šiuos veiksmus, kad įgalintumėte įsigijimo kategorijų naudojimo su projekto pirkimo užsakymais funkciją.

1. Dalyje Dynamics 365 Finance atidarykite **darbo sritį Funkcijų valdymas**.
1. Funkcijų sąraše raskite **funkciją Naudoti įsigijimo kategorijas projekto operacijose, skirtą ištekliams pagrįstiems / nelaikomiems scenarijams**, tada pasirinkite **Įgalinti**.

> [!IMPORTANT]
> Kaip būtiną sąlygą taip pat turite įgalinti **laukiančias tiekėjo SF projekto operacijose, skirtą ištekliams pagrįstiems / nelaikomiems scenarijams**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Susieti projektų kategorijas įsigijimo kategorijų hierarchijoje

Norėdami susieti projektų kategorijas su įsigijimo kategorijų hierarchijoje, **atlikite** šiuos veiksmus:

1. Eikite į **viešųjų pirkimų ir pirkimų įsigijimo \> kategorijas**.
1. Pasirinkite **Redaguoti kategorijų hierarchiją**.
1. Pasirinkite norimą kategorijų hierarchijos mazgą, tada skirtuke **Priskirti projekto kategorijas** susiekite mazgą su projekto kategorija iš **kategorijos Laikas**, Išlaidos**arba **Prekės projektas** (t. y. **kategorijoje Numatytasis laikas** arba **Numatytosios išlaidos**).
1. Pasirinkite **Įrašyti**.
1. Uždarykite puslapį.

> [!NOTE]
> Įsigijimo kategorijos susiejimas su projekto kategorija yra neprivalomas. Jei įsigijimo kategorija nesusieta, sistema naudos vertę, nustatytą puslapio Projekto valdymo ir apskaitos parametrų skirtuko Projekto operacijos, esančios "Dynamics 365 Customer Engagement" skirtuko **Projekto operacijos skirtuke "Project Operations on Dynamics 365 Customer Engagement**", esančiame **lauke** Prekė **·**.**·**
