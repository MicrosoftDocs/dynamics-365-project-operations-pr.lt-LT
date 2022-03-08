---
title: Kas nauja arba pakeista „Project Service Automation“ V3 31 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 31 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 2e5fce003c25f9c5911e5a01fb4ec3e19c06c078e00b054472699a522b9cd070
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002161"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 31 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 31 atnaujintame leidime. Šios versijos komponavimo versijos numeris yra V3.10.52.77 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2021 m. gegužės mėn.

## <a name="update-release-31"></a>31 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

Buvo pataisytos šios problemos:

- Buvo painūs laiko įrašų valdymo komandų mygtukai puslapyje **Rezervuojamasis išteklius**.
- Tvirtinant laiko įrašą, dalyje **Project.SetTrackingFields** buvo generuojama neapibrėžtos nuorodos išimtis.

**Išteklių valdymas**

Buvo pataisytos šios problemos:

- Pasirinkus **Kurti komandos narį**, netinkamai rodomas elemento **Numatytoji patvirtinto rezervavimo būsena** rezervavimo sąrankos metaduomenų parametras.
- PSA 1.X versiją naujinant į 3.X, įvyksta versijos naujinimo proceso triktis etape **UpgradeResourceRequirements**.


**Pardavimas**

Buvo pataisytos šios problemos:

- Sekimo tinklelyje faktinės pajamos sumas konvertuoja į projekto valiutą.
- Kai organizacijos pagrindinė valiuta skiriasi nuo projekto valiutos, numatytoji valiuta yra neaiški kuriant žurnalų eilutes, pasiūlymų eilutes ir sutarčių eilutes.
- Užklausa **Laukiamo taisymo žurnalo tikrinimas** nefiltruojama pagal projektą.
- Likęs projekto pardavimas neteisingai apskaičiuojamas.
- Pasiūlymai, pagrįsti kontaktu, neįvykdomi, kai jie sukuriami be kainoraščio.
- Pasirinkus **Patvirtinti sąskaitą faktūrą** nerodomas joks apdorojimo suktukas.
- Pasirinkus **Kurti sąskaitą faktūrą** nerodomas joks apdorojimo suktukas.
- Jei pasiūlymą uždarysite kaip pralaimėtą, rezervavimai nebus atšaukti.







