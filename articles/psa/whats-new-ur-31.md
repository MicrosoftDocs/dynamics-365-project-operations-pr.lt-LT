---
title: Kas nauja arba pakeista „Project Service Automation“ V3 31 atnaujintame leidime
description: Šiame straipsnyje išvardijamos funkcijos ir taisymai, galimi "Project Service Automation Update Release 31", V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d62b12a5363637e46b29c2e9edf4e1f17da729f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925038"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 31 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šiame straipsnyje išvardijamos naujos arba pakeistos "Project Service Automation V3", "Update Release 31" funkcijos ir taisymai. Šios versijos komponavimo versijos numeris yra V3.10.52.77 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2021 m. gegužės mėn.

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







