---
title: Kas nauja arba pakeista „Project Service Automation“ V3 38 atnaujintame leidime
description: Šiame straipsnyje išvardytos funkcijos ir pataisos, įtrauktos į „Microsoft Dynamics 365 Project Service Automation“ V3 38 atnaujintą leidimą.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915195"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 38 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Ji suderinama su „Dynamics 365 9.x“. Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šiame straipsnyje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 38 atnaujintame leidime. Šios versijos komponavimo versijos numeris yra V3.10.59.117 ir ji visuotinai pasiekiama įdiegiant savaiminį 2021 m. gruodžio mėn. naujinimą.

## <a name="update-release-38"></a>38 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

Buvo pataisytos tolesnės problemos.

**Laikas ir išlaidos**

- Išimtis atsiranda, kai patvirtinimo rinkinio žurnalų ilgis viršija 100 000 įrašų.
- Vartotojai negali pasiekti laiko įvedimo **tinklelio iš** laiko **įvesties pagrindinio** puslapio.
- Laiko **įvesties importavimo** dialogo lange nerodo jokio teksto, kai jokių elementų importuoti negalima.
- Vartotojai gali sukurti patvirtinimo rinkinius, kurių **tikslinės būsenos** laukas nustatytas kaip **nežinomas**.

**Projektų valdymas**

- Kai pradedamas vasaros laikas, kai išteklių priskyrimai UTC (+09:30) ir UTC (+10:00) ištekliai yra netinkamai rodomi.
- Kai **kuriose lokalėse** paslėptas darbo struktūros papildomų stulpelių laukas.
- Kalendoriaus valdiklio datos parinkėjas projekto užduoties **tinklelyje** nėra tinkamai lokalizuotas kinų kalba.

**Pardavimas**

- **Sutarties vykdymo** ir projekto **faktinių** išlaidų reikšmės nesutampa, kai rezervuojami ištekliai, kurių skirtingi sutarties vienetai ir valiutos pateikia laiko įrašus.
- Pasirinktinė darbo eiga, automatiškai patvirtindama sąskaitas faktūras, neįvyksta, kai sąskaitos faktūros importuojamos valdomasis sprendimas. Rodomas šis pranešimas: „Microsoft.Xrm.Sdk.InvalidPluginExecutionException“ pranešimas: netinkama sąskaitos faktūros būsena“.
- Kai **šaknis** yra pažymėta kaip suvestinės parinktis ir projektą sudaro transakcijų susiejimo (pvz., laiko, išlaidų ir materialinių verčių derinys), sistema susumuojamas pagal transakcijų susiejimo funkciją kaip vieną mokesčio eilutę.
- Tais atvejais, kai išlaidų eilutė įtraukiama prieš su projektu susietą sutarties eilutę, **tinkama** kaina nėra įvesta kaip numatytoji reikšmė lauke Naujinti kainą.
- Projektų ir užduočių objektuose neleidžiama naudoti **neigiamų** pardavimo **sumų**.
