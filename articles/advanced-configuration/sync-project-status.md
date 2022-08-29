---
title: Sinchronizuoti projekto būseną, kad būtų išvengta įėjimo į uždarytus projektus
description: Šiame straipsnyje paaiškinama, kaip sinchronizuoti projekto būseną, kad būtų išvengta įėjimo į neaktyvius arba uždarytus projektus.
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sinchronizuoti projekto būseną, kad būtų išvengta įėjimo į uždarytus projektus

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

## <a name="scenario"></a>Scenarijus

Contoso yra tiesioginis su "Microsoft" Dynamics 365 Project Operations išteklių / ne atsargų scenarijams. Vykdant įprastą verslo veiklą, projektai gali būti užbaigti arba sustabdyti. Galite inaktyvuoti projektą, kad užtikrintumėte, jog nebūtų generuojamos jokios išlaidos ar sąskaitos faktūros.

## <a name="solution"></a>Sprendimas

### <a name="prerequisites"></a>Būtinosios sąlygos

-   Microsoft Dynamics 365 Finansai 10.0.29 arba naujesnė versija turi būti įdiegta.
-   "Dual Write" žemėlapio 1.0.0.3 projektams V2 (msdyn\_ projektams) turi būti įdiegtas arba sukonfigūruotas rankiniu būdu, kaip aprašyta toliau.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Sukurkite atnaujintą "Project Operations" integravimo projektų V2 dvigubo rašymo žemėlapio versiją

Norėdami atnaujinti "Project Operations Projects V2" dvigubo rašymo žemėlapį:

1. Eikite į **duomenų valdymo** darbo sritį ir pasirinkite **Dvigubas rašymas**.
2. Pasirinkite plytelę Dvigubas **rašymas**.
3. Stulpelyje T **lentelės žemėlapis** raskite ir pasirinkite **Project V2 (msdyn\_ projektai)**, tada pasirinkite Stabdyti.
4. Pasirinkite žemėlapio pavadinimą, kad atidarytumėte žemėlapį, tada pasirinkite **[Nėra]**.
5. Dialogo lange Pasirinkti stulpelį pasirinkite **statecode \[projekto būsena\]**, tada pasirinkite Gerai. Norėdami susiaurinti sąrašą, filtro reikšmėje galite įvesti **būseną**.
6.  Pasirinkite **Įtraukti arba redaguoti transformaciją** žemėlapio tipo **stulpelyje,** kad redaguotumėte transformaciją.
7.  Iš **Transformavimo tipas** pasirinkite **ValueMap**.
8.  Pasirinkite **Įtraukti reikšmių susiejimą**, tada įtraukite šiuos **raktus** ir **reikšmes**:

   Klavišas       | Vertė 
   ----------|-------
   "InProcess" | 0     
   baigta | 1     

![Ekrano kopija, kurioje rodomas dvigubo rašymo susiejimas](media/projectstage-dw-mapping.png)

9. Pasirinkite **Įrašyti**.
10. Puslapio Dvigubo rašymo **> projektai V2 (msdyn_projects)** viršuje pasirinkite **Įrašyti kaip**.
11. Lauke **Leidėjas esančiame** sąraše Pridėti lentelę **pasirinkite** CDS numatytasis **leidėjas**.
12. Nustatykite lauką **Versija** į 1.0.0.3.
13. Įveskite **aprašą**, tada pasirinkite **Įrašyti**.
14. Puslapio Dvigubo rašymo **> projektai V2 (msdyn_projects)** viršuje pasirinkite **Vykdyti**, kad paleistumėte žemėlapį, tada sekect **Taip**, jei prašoma patvirtinti prieš paleidžiant. 

### <a name="close-a-newly-completed-project"></a>Uždarykite naujai užbaigtą projektą

Dynamics 365 Finance naudoja projekto etapo **lauką**, kad atskirtų vykdomus **arba** užbaigtus **projektus**. **Iš užbaigtų** projektų negalima patirti išlaidų ar išrašyti sąskaitų faktūrų klientams.

1. Atidarykite projektą, kurį norite išjungti.
2. Juostelėje pasirinkite **Išjungti**.

> [!NOTE]
> Galite išaktyvinti arba uždaryti projektą, nes jie abu veiks taip pat finansų kontekste.

3. Programoje "Finance" atidarykite sąrašo **puslapį** Visi projektai.
4. Patvirtinkite, kad išjungtas projektas nerodomas sąraše.
5. Virš sąrašo **esančiame rodymo projektų** filtre pakeiskite reikšmę iš **Aktyvus** į **Visi**.
6. Dabar pamatysite išjungtą projektą.

Jei bandote registruoti laiką ar išlaidas pagal šį projektą programoje "Finance", neturėtumėte matyti projekto, kad galėtumėte jį pasirinkti. Jei rankiniu būdu įvesite projekto numerį į išlaidas, matysite pranešimą, pvz., "Užbaigtas projekto etapas neleidžia įrašyti į projektą". Sąskaitų faktūrų išrašymo ir kitos atsiskaitymo funkcijos turėtų būti išjungtos, nes jos bus įtrauktos į uždarą projektą.

