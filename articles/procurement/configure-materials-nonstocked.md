---
title: Atsargose nelaikomų medžiagų ir laukiančių tiekėjo sąskaitų faktūrų konfigūravimas
description: Šioje temoje paaiškinta, kaip įjungti atsargose nelaikomų medžiagų ir laukiančių tiekėjo sąskaitų faktūrų naudojimo galimybę.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 24418f3aad8356bd209eef7487a47a3870bce10f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993921"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Atsargose nelaikomų medžiagų ir laukiančių tiekėjo sąskaitų faktūrų konfigūravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

## <a name="minimum-version-requirement"></a>Minimali būtina versija

Norint „Dynamics 365 Project Operations“ atsargose nelaikomų medžiagų / išteklių scenarijuose naudoti atsargose nelaikomas medžiagas ir laukiančias tiekėjų sąskaitas faktūras, reikalingos toliau nurodytos versijos.

„Dynamics 365 Dataverse“ sprendimai.

- „Project Operations“ – 4.9.0.221 arba naujesnė
- Dvigubo rašymo programų tvarkymo sprendimas – 2.2.2.23 arba naujesnė

„Dynamics 365 Finance“:
- 10.0.18 (10.0.793.52) arba naujesnė. Siekdami atitikti minimalių versijų reikalavimus, įsitikinkite, kad jūsų „Finance“ aplinka yra naujausia ir kad pritaikyti visi kokybės naujinimai.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Atsargose nelaikomų medžiagų dvigubo rašymo schemų vykdymas ir tiekėjų sąskaitų faktūrų integravimas

Šiame skyriuje pateikiama informacija apie konkrečias schemas, kurias reikia naudoti su atsargose nelaikomomis medžiagomis ir tiekėjų sąskaitomis faktūromis. Patikrinkite, ar jūsų aplinkoje veikia būtinosios schemos, išvardytos temoje [Naujos aplinkos konfigūravimas](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps).

1. Nueikite į „Lifecycle Services“ (LCS), pereikite prie savo LCS projekto ir nueikite į puslapį **Išsami aplinkos informacija**.
2. Skyriuje **„Common Data Service“ aplinkos informacija** pasirinkite **Susieti su CDS programoms**. Pasirinkus saitą būsite nukreipti į susiejimų objektų sąrašą.
3. Įsitikinkite, kad veikia toliau nurodytos schemos. Jei schemos neveikia, jas paleiskite ir būtinai įtraukite visas susijusias lentelių schemas.

    - CDS išleisti išskirtieji produktai (produktai)
    - Tiekėjai v2 (msdyn_vendors)
    - „Project Operations“ lentelė, skirta medžiagų įvertinimams (msdyn_estimatelines)
    - „Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eksportavimo objektas (msdyn_projectvendorinvoices)
    - „Project Operations“ integravimo projekto tiekėjų sąskaitų eilučių eksportavimo objektas (msdyn_projectvendorinvoicelines)
    - „Project Operations“ integravimo faktiniai duomenys (msdyn_actuals). Įsitikinkite, kad naudojate 1.0.0.14 arba naujesnę schemų versiją. Aktyvią schemos versiją galite matyti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versija** ir pasirinktą versiją įrašydami.

Jei naudojate standartinius demonstracinius duomenis, taip pat gali reikėti sustabdyti ir iš naujo paleisti toliau nurodytas objektų schemas, iš pradžių jas sinchronizuojant.
  - Mokėjimo dienos CDS V2 (msdyn_paymentdays)
  - Mokėjimo grafikas (msdyn_paymentschedules)
  - Mokėjimo sąlygos (msdyn_paymentterms)
  - Tiekėjų grupės (msdyn_vendorgroups)
  - Vienetai (uom)

> [!NOTE]
> Pradinio tiekėjų grupių ir vienetų, esančių keliuose esamo demonstracinių duomenų rinkinio įrašuose, sinchronizavimo gali nepavykti atlikti. Šių trikčių galite nepaisyti, nes jos netrukdys naudoti demonstracinių duomenų su „Project Operations“.

## <a name="configure-prerequisites-in-dataverse"></a>Būtinųjų „Dataverse“ komponentų konfigūravimas

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Darbo eigos suaktyvinimas norint kurti klientus pagal tiekėjo objektą

Sprendimas Dvigubo rašymo tvarkymas suteikia [pagrindinio tiekėjų integravimo funkciją](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping.md). Norint naudoti šią funkciją, objekte **Klientai** būtina sukurti klientų duomenų. Suaktyvinkite šablono darbo eigos procesą, kad lentelėje **Klientai** būtų sukurti tiekėjai, kaip aprašyta dalyje [Vieno tiekėjo dizaino perjungimas į kitą](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch.md#use-the-extended-vendor-design-for-vendors-of-the-organization-type).

### <a name="set-products-to-be-created-as-active"></a>Nustatymas, kad produktai būtų kuriami kaip aktyvūs

Atsargose nelaikomos medžiagos sprendime „Finance“ turi būti sukonfigūruotos kaip **Išleisti produktai**. Sprendimas Dvigubo rašymo tvarkymas suteikia parengtą naudoti [išleistų produktų integravimo į „Dataverse“ produktų katalogą funkciją](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping.md). Numatyta, kad „Finance“ produktai su „Dataverse“ sinchronizuojami juodraščio būsenos. Norėdami produktą sinchronizuoti aktyvios būsenos, kad jį būtų galima tiesiogiai naudoti medžiagų naudojimo dokumentuose arba laukiančiose tiekėjų sąskaitose faktūrose, nueikite į **Sistema** > **Administravimas** > **Sistemos administravimas** > **Sistemos parametrai** ir skirtuke **Pardavimas** parinktį **Kurti aktyvios būsenos produktus** nustatykite kaip **Taip**.

## <a name="configure-prerequisites-in-finance"></a>Būtinųjų „Finance“ komponentų konfigūravimas

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Laukiančių tiekėjų sąskaitų faktūrų funkcijų rakto įjungimas

Norėdami įjungti funkcijas, leidžiančias į laukiančių tiekėjų sąskaitų faktūrų eilutes įtraukti projekto informacijos, atlikite toliau nurodytus veiksmus.

1. Sprendime „Finance“ nueikite į darbo sritį **Funkcijų tvarkymas**.
2. Funkcijų sąraše raskite funkciją **Leisti „Project Operations“ išteklių / atsargose nelaikomų medžiagų scenarijuose naudoti laukiančias tiekėjų sąskaitas faktūras** ir pasirinkite **Įjungti**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Prekių kategorijų grupių ir projektų kategorijų apibrėžimas

Sukonfigūruokite bent vieną operacijos tipo **Prekė** kategorijų grupę, o naudodami šią grupę – bent vieną projektų kategoriją. Norėdami sužinoti daugiau, žr. [Projektų kategorijų konfigūravimas](../project-accounting/configure-project-categories.md#category-groups).

Peržiūrėkite projektų kaštų ir pajamų profilius bei sukonfigūruokite prekių operacijų registravimą didžiojoje knygoje. Norėdami sužinoti daugiau, žr. [Apmokėtinų projektų apskaitos konfigūravimas](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Įtraukiamojo produkto nustatymas

Naudodami „Project Operations“, galite įrašyti išleistame produktų kataloge sukonfigūruotų ir įtraukiamųjų produktų medžiagų įvertinimus bei naudojimą. Norint naudoti įtraukiamuosius produktus, reikalingas vienas išleistas produktas, šiam tikslui sukonfigūruotas sprendime „Finance“. Norėdami sukonfigūruoti įtraukiamąjį produktą, atlikite toliau nurodytus veiksmus. Šiuos veiksmus pakartokite su kiekvienu juridiniu objektu, kuris išteklių / atsargose nelaikomų medžiagų scenarijams naudoja „Project Operations“.

1. Sprendime „Finance“ nueikite į **Produktų informacijos tvarkymas** > **Produktai** > **Išleisti produktai** ir pasirinkite **Naujas**.
2. Lauke **Produkto tipas** pasirinkite **Prekė**, o lauke **Produkto potipis** – **Produktas**.
3. Įveskite produkto numerį (WRITEIN) ir produkto pavadinimą (Įtraukiamasis produktas).
4. Pasirinkite prekės modelių grupę. Įsitikinkite, kad jūsų pasirinktos prekės modelių grupės laukas **Atsargų strategija, atsargose laikomas produktas** nustatytas kaip **Klaidinga**.
5. Pasirinkite reikšmes laukuose **Prekių grupė**, **Saugyklos dimensijų grupė** ir **Sekimo dimensijų grupė**. **Saugyklos dimensiją** naudokite tik su **vieta** ir nenustatykite jokių sekimo dimensijų.
6. Pasirinkite reikšmes laukuose **Atsargų vienetas**, **Pirkimo vienetas** ir **Pardavimo vienetas**, tada įrašykite pakeitimus.
7. Skirtuke **Planas** nustatykite numatytuosius užsakymų parametrus, o skirtuke **Atsargos** – numatytąją vietą ir sandėlį.
8. Nueikite į **Projektų tvarkymas ir apskaita** > **Sąranka** > **Projektų tvarkymo ir apskaitos parametrai** bei atidarykite **„Project Operations“ naudojant „Dynamics 365 Dataverse“**. 
9. Skirtuko **Medžiagos** lauke **Įtraukiamasis produktas** pasirinkite sukurtą produktą.
10. Savo „Dataverse“ aplinkos svetainės struktūroje atidarykite objektą **Produktai** ir suraskite įtraukiamojo produkto įrašą. 
11. Atidarykite įrašo išsamią informaciją ir produkto būseną nustatykite kaip **Nurašytas**. Ši produkto būsena niekam neleidžia netyčia šio įrašo naudoti tiesiogiai medžiagų įvertinimuose ir naudojimo dokumentuose.

### <a name="set-up-a-procurement-integration-account"></a>Viešųjų pirkimų integravimo sąskaitos nustatymas

Viešųjų pirkimų integravimo sąskaita naudojama kaip tarpuskaitos sąskaita registruojant laukiančią tiekėjo sąskaitą faktūrą, kurios eilutės yra priskirtos projektui.

Kai sistema užregistruoja laukiančią tiekėjo sąskaitą faktūrą, ši sąskaita naudojama projekto kaštų sumai. Išsami informacija apie tiekėjo sąskaitą faktūrą apdorojama naudojant „Dataverse“ ir sukuriami atitinkami projekto faktiniai duomenys. Faktinė projekto informacija įtraukiama į „Project Operations“ integravimo žurnalą. Kai registruojate integravimo žurnalą, suma pašalinama iš viešųjų pirkimų integravimo sąskaitos ir įrašoma į projekto kaštus.

1. Norėdami nustatyti viešųjų pirkimų integravimo sąskaitą, nueikite į **Projektų tvarkymas ir apskaita** > **Sąranka** > **Projektų tvarkymo ir apskaitos parametrai** bei atidarykite **„Project Operations“ naudojant „Dynamics 365 Dataverse“**. 
2. Pasirinkite skirtuką **Medžiagos**, tada lauke **Viešųjų pirkimų integravimo sąskaita** pasirinkite kokią nors reikšmę.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Prekės projektų kategorijų numatytųjų parametrų nustatymas

1. Sprendime „Finance“ nueikite į **Projektų tvarkymas ir apskaita** > **Sąranka** > **Projektų tvarkymo ir apskaitos parametrai** bei atidarykite **„Project Operations“ naudojant „Dynamics 365 Dataverse“**. 
2. Skirtuko **Numatytieji projektų kategorijų parametrai** lauke **Prekė** pasirinkite kokią nors reikšmę. Jei projektų kategorija nebuvo nustatyta projekto faktinių duomenų įraše, ši projektų kategorija naudojama medžiagų operacijoms.
