---
title: Kas nauja arba pakeista „Project Service Automation“ V3 35 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisos, įtrauktos į „Microsoft Dynamics 365 Project Service Automation“ 35 naujinimo leidimo 3 v.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: e210777f1e4d149b700721ac7fb9bd129b1166fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574038"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 35 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Ji suderinama su „Dynamics 365 9.x“. Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos naujos arba pakeistos funkcijos ir pataisos, susijusios su 3 versijos „Project Service Automation“ 35 naujinimo leidimu. Šios komponavimo versijos numeris yra V3.10.56.110 ir ji visuotinai pasiekiama naudojant savaimini naujinimą 2021 m. rugsėjo mėn.

## <a name="update-release-35"></a>35 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

Buvo pataisytos tolesnės problemos.

**Laikas ir išlaidos**

- Projekto tvirtintojui pateikiama skaitymo teisės klaida, kai jis patvirtina išlaidų įrašus naudodamas vaidmenį **Projekto tvirtintojas**.
- Projekto tvirtintojui pateikiama rašymo teisės klaida, susijusi su **msdyn_projectapproval**, kai jis atšaukia patvirtintą laiko įrašą naudodamas vaidmenį **Projekto tvirtintojas**.
- Kai „Dynamics 365“, skirtos telefonams, programėlės Projekto išteklių telkinys modulio laiko įraše pasirenkate **Kopijuoti savaitę**, įvyksta ši klaida: „...\OfficeProductivity_RibbonRules.js.map: HTTP klaida: būsenos kodas 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE.“
- Strategija **Kartoti** automatiškai patvirtina įrašus, kurie anksčiau buvo atmesti.
- Antriniame tinklelyje **Patvirtinimo rinkiniai** rodomi netaikomi juostos veiksmai.
- Objekte **Laiko įrašas** nėra **projekto užduoties** ir **ištekliaus vaidmens** piktogramų.
- Kai importuojate išteklių priskyrimus, importuotuose laiko įrašuose nurodoma neteisinga priskyrimų, sukurtų vykdant neautomatinio režimo užduotis, trukmė.
- Puslapyje **Išplėstinė laiko įrašų ieška** trūksta parinkties **Naikinti**.
- Puslapyje **Laiko įrašų informacija** trūksta parinkties **Įrašyti**. Dėl šios problemos negalima įrašyti pakeitimų uždarant puslapį.

**Projekto planavimas**

- Tinkleliuose **Išteklių priskyrimas** ir **Išteklių suderinimas** sugrupuoti atributai nesurikiuoti abėcėlės tvarka.
- Jei datos funkcija tinkinama kaip **Tik data**, negalima sukurti užduočių.

**Išteklių valdymas**

- Jei įdiegta ir „Dynamics 365 Field Service“, ir „Project Service Automation“, su pagrindiniu puslapiu susiejus **išteklių reikalavimo susietąjį rodinį** kyla sluoksnių pertekliaus problemų.
- Dialogo lange **Spartusis komandos narių kūrimas** dukart spustelėjus **Įrašyti**, negalima sukurti išteklių reikalavimo.

**Pardavimas**

- Jei panaikinsite užduotį, susietą su pasiūlymu, kurio būsena yra **Laimėtas**, bus pateikta išimtis.
