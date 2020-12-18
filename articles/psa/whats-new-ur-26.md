---
title: Kas nauja arba pakeista „Project Service Automation“ V3 26 atnaujintame leidime
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643273"
---
<a name="project-service-automation-update-release-26-v3"></a>„Project Service Automation“ V3 26 naujinimo leidimas
================================================

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos naujos arba pakeistos funkcijos ir pataisos, susijusios su 3 versijos „Project Service Automation“ 26 atnaujintu leidimu. Šios versijos komponavimo versijos numeris yra V3.10.44.59 ir ji visuotinai pasiekiama įdiegiant savaiminį 2020 m. gruodžio mėn. naujinimą.

<a name="update-release-26"></a>26 atnaujintas leidimas
-----------------

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

Buvo pataisytos šios problemos:

-   Vartotojai gali pakeisti užduotį laiko įraše, kuris buvo patvirtintas / pateiktas.

-   Įrašant laiko įrašą pateikiama klaida Objekto nuoroda nenustatyta.

-   Importuojant laiko įrašus iš išteklių priskyrimo sukuriami laiko įrašai su netinkamomis DateTime reikšmėmis.

-   Įdiegus „Project Service Automation“ ir „Field Service“ programą, mygtukas **Naujas** rodomas du kartus „Field Service“ programos laiko įrašų komandų juostoje.

-   Langelių **Leisti vienetą** ir **Vienetų grupė** atnaujinimai nuo šiol veikia tinklelyje **Išlaidų sąmatos**.

-   Į formą **Laiko įrašo redagavimas** įtraukta **Laiko planavimo juosta**.

-   Patvirtinus ne projekto laiko įrašų laiką užblokuojama sistema, kai ieškoma projekto tvirtintojo vaidmens.

**Išteklių valdymas**

Buvo pataisytos šios problemos:

-   Prie priedo **PostProjectCreate** pridėta patikra, tikrinanti pirminį reikalavimą prieš jį sukuriant.

-   Sparčiojo kūrimo forma **Projekto komandos narys** pateikia „null“ nuorodos išimtį, kai iš formos pašalinami laukai.

-   Nepavyks generuoti 12 valandų reikalavimų 1 metų laikotarpiu.

-   Patobulintas klaidos pranešimas dėl „null“ nuorodos išimties, pateikiamos kuriant išteklių reikalavimą.

**Projektų valdymas**

Buvo pataisytos šios problemos:

-   Patobulinta patikra, siekiant išspręsti „null“ nuorodos išimties problemą, kylančią priede **PreProjectUpdate**.

-   Projektai, kuriuos paskelbė „Microsoft Project“ kompiuterio papildinys, panaikina nepriskirtus priskyrimus.

-   Pridėta nauja patikra, kai užduoties projekto nuoroda yra netinkama dėl „null“ nuorodos išimties, pateikiamos priede **PreValidateProjectTaskUpdate**.

-   Komandos narių tinklelyje nerodomi atskiri priskyrimai komandos nario įraše.

-   Pridėta nauja patikra ir klaidos pranešimai dėl „null“ nuorodos išimties, pateikiamos priede **PreProjectTaskDelete**.

**„Sales“**

Buvo pataisytos šios problemos:

-   Pasiūlyme arba sutartyje pasirinkus projektu pagrįstą eilutę, mygtukas **Pasiūlymas** turėtų būti rodomas tik tada, kai pasirenkam produktu pagrįsta eilutė, susieta su esamu produktu.

-   Teisė **Create_Product** atskirta nuo teisės **Create_ProjectContract**.

-   Panaikinus sąskaitos faktūros eilutę pateikiama „null“ nuorodos klaida dėl **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.
