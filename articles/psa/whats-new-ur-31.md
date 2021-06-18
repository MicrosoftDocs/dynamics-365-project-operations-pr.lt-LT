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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999141"
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







