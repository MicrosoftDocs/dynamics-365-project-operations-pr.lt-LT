---
title: Sinchronizuokite projekto būseną, kad neleistumėte patekti į uždarus projektus
description: Šiame straipsnyje paaiškinta, kaip sinchronizuoti projekto būseną, kad nebūtų galima įvesti projektų su neaktyviais arba uždarytais projektais.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348111"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sinchronizuokite projekto būseną, kad neleistumėte patekti į uždarus projektus

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

## <a name="scenario"></a>Scenarijus

„Contoso“ paleidžiama naudojant „Microsoft Dynamics 365 Project Operations“, skirtą išteklių / nelaikomų medžiagų scenarijams. Kaip įprasta verslo veikla, projektai gali būti užbaigti arba sulaikyti. Galite išjungti projektą ir įsitikinti, kad negeneruojama jokių išlaidų arba sąskaitų faktūrų.

## <a name="solution"></a>Sprendimas

### <a name="prerequisites"></a>Būtinosios sąlygos

-   Turi būti įdiegta „Microsoft Dynamics 365 Finance“ 10.0.29 arba naujesnė versija.
-   Dviguba rašymo struktūra 1.0.0.3, skirtas V2 projektams (msdyn\_projektams), turi būti įdiegta arba rankiniu būdu sukonfigūruota, kaip nurodyta toliau.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Atnaujintos „Project Operations integration Projects V2" dvigubo rašymo struktūros versijos kūrimas

„Project Operations Projects V2“ dvigubo rašymo schemų naujinimai:

1. Eikite į arbo sritį **Duomenų valdymas** ir pasirinkite **Dvigubas rašymas**.
2. Pažymėkite **Dvigubo rašymo** plytelę.
3. Stulpelyje T **Lentelės struktūra** raskite ir pažymėkite **Project V2" (msdyn\_projects)** ir pažymėkite Sustabdyti.
4. Pažymėkite struktūros pavadinimą, kad atidarytumėte struktūrą, tada pažymėkite **[Nėra]**.
5. Dialogo lange Stulpelio pasirinkimas pasirinkite **būsenos kodą \[Projekto būsena\]**, tada pasirinkite Gerai. Filtro reikšmę **galite** įvesti taip, kad susiaurintumėte sąrašą.
6.  Norėdami redaguoti transformaciją, pasirinkite **Įtraukti arba redaguoti transformaciją** **struktūros tipo** stulpelyje.
7.  Iš **Transformacijos tipo** pasirinkite **VertėsStruktūra**.
8.  Pažymėkite **Įtraukti reikšmių susiejimą**, tada įtraukite šiuos **Raktus** ir **Reikšmes**:

   Klavišas       | Vertė 
   ----------|-------
   Apdorojama | 0     
   baigta | 1     

![Dvigubo rašymo susiejimo ekrano kopija](media/projectstage-dw-mapping.png)

9. Pasirinkite **Įrašyti**.
10. Puslapio **Dvigubas rašymas viršuje > „Projects V2" (msdyn_projects)** pasirinkite **Įrašyti kaip**.
11. Iš srities **Įtraukti lentelę** lauke **Leidėjas** pasirinkite **CDS Numatytasis leidėjas**.
12. Nustatykite **Versija** laukelį į 1.0.0.3.
13. Įveskite **Aprašą** ir pasirinkite **Įrašyti**.
14. Puslapio **Dvigubas rašymas viršuje > „Projects V2 msdyn_projects"** pasirinkite **Vykdyti**, kad paleistumėte struktūrą, tada pasirinkite **Taip**, jei prieš paleisdami būsite prašomi patvirtinti. 

### <a name="close-a-newly-completed-project"></a>Naujai užbaigto projekto uždarymas

„Dynamics 365 Finance" naudoja **projekto etapo** lauką, kad būtų atskirti **vykdomi** arba **baigti** projektai. **Baigti** projektai negali sukelti išlaidų arba klientams išrašyti jų sąskaitų faktūrų.

1. Atidarykite projektą, kurį norite išjungti.
2. Juostelėje pasirinkite **Išjungti**.

> [!NOTE]
> Projektą galima išjungti arba uždaryti, nes jie abu elgsis taip pat, kaip ir finansų kontekste.

3. Finansų srityje atidarykite **Visų projektų sąrašo** puslapį.
4. Patikrinkite, ar išjungto projekto nėra sąraše.
5. **Rodomų projektų** filtre virš sąrašo reikšmę pakeiskite iš **Aktyvūs** į **Visi**.
6. Dabar matysite išjungtą projektą.

Jei bandote registruoti laiką ar išlaidas pagal šį projektą finansų srityje, projekto pasirinkti negalite. Jei išlaidų projekto numerį įvesite rankiniu būdu, matysite pranešimą, pvz., „Projekto etapas baigtas, neleidžiama įrašyti projekto". Sąskaitų faktūrų išrašymo ir kitos sąskaitų siuntimo funkcijos turėtų būti išjungtos, nes jos bus uždaryto projekto kontekste.

