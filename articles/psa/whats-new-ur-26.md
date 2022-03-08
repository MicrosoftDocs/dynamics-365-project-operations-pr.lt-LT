---
title: Kas nauja arba pakeista „Project Service Automation“ V3 26 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 26 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: fa526e97a366c01dae2547d79d0eda2fb204e07d0f6383b991165b9eecd836e9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004276"
---
# <a name="project-service-automation-update-release-26-v3"></a>„Project Service Automation“ V3 26 naujinimo leidimas

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos naujos arba pakeistos funkcijos ir pataisos, susijusios su 3 versijos „Project Service Automation“ 26 atnaujintu leidimu. Šios versijos komponavimo versijos numeris yra V3.10.44.59 ir ji visuotinai pasiekiama įdiegiant savaiminį 2020 m. gruodžio mėn. naujinimą.

## <a name="update-release-26"></a>26 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

Buvo pataisytos šios problemos:

- Vartotojai gali pakeisti užduotį laiko įraše, kuris buvo patvirtintas / pateiktas.
- Įrašant laiko įrašą pateikiama klaida Objekto nuoroda nenustatyta.
- Importuojant laiko įrašus iš išteklių priskyrimo sukuriami laiko įrašai su netinkamomis DateTime reikšmėmis.
- Įdiegus „Project Service Automation“ ir „Field Service“ programą, mygtukas **Naujas** rodomas du kartus „Field Service“ programos laiko įrašų komandų juostoje.
- Langelių **Leisti vienetą** ir **Vienetų grupė** atnaujinimai nuo šiol veikia tinklelyje **Išlaidų sąmatos**.
- Į formą **Laiko įrašo redagavimas** įtraukta **Laiko planavimo juosta**.
- Patvirtinus ne projekto laiko įrašų laiką užblokuojama sistema, kai ieškoma projekto tvirtintojo vaidmens.

**Išteklių valdymas**

Buvo pataisytos šios problemos:

- Prie priedo **PostProjectCreate** pridėta patikra, tikrinanti pirminį reikalavimą prieš jį sukuriant.
- Sparčiojo kūrimo forma **Projekto komandos narys** pateikia „null“ nuorodos išimtį, kai iš formos pašalinami laukai.
- Nepavyks generuoti 12 valandų reikalavimų 1 metų laikotarpiu.
- Patobulintas klaidos pranešimas dėl „null“ nuorodos išimties, pateikiamos kuriant išteklių reikalavimą.

**Projektų valdymas**

Buvo pataisytos šios problemos:

- Patobulinta patikra, siekiant išspręsti „null“ nuorodos išimties problemą, kylančią priede **PreProjectUpdate**.
- Projektai, kuriuos paskelbė „Microsoft Project“ kompiuterio papildinys, panaikina nepriskirtus priskyrimus.
- Pridėta nauja patikra, kai užduoties projekto nuoroda yra netinkama dėl „null“ nuorodos išimties, pateikiamos priede **PreValidateProjectTaskUpdate**.
- Komandos narių tinklelyje nerodomi atskiri priskyrimai komandos nario įraše.
- Pridėta nauja patikra ir klaidos pranešimai dėl „null“ nuorodos išimties, pateikiamos priede **PreProjectTaskDelete**.

**„Sales“**

Buvo pataisytos šios problemos:

- Pasiūlyme arba sutartyje pasirinkus projektu pagrįstą eilutę, mygtukas **Pasiūlymas** turėtų būti rodomas tik tada, kai pasirenkam produktu pagrįsta eilutė, susieta su esamu produktu.
- Teisė **Create_Product** atskirta nuo teisės **Create_ProjectContract**.
- Panaikinus sąskaitos faktūros eilutę pateikiama „null“ nuorodos klaida dėl **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]