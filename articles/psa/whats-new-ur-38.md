---
title: Kas nauja arba pakeista „Project Service Automation“ V3 38 atnaujintame leidime
description: Šioje temoje išvardijamos funkcijos ir pataisymai, kuriuos galima rasti Microsoft Dynamics 365 Project Service Automation 38 naujinimo leidime, V3.
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901514"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 38 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Ji suderinama su „Dynamics 365 9.x“. Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardijamos naujos arba pakeistos "Project Service Automation Update Release 38", V3 priemonės ir pataisymai. Šios versijos komponavimo versijos numeris yra V3.10.59.117 ir ji visuotinai pasiekiama įdiegiant savaiminį 2021 m. gruodžio mėn. naujinimą.

## <a name="update-release-38"></a>38 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

Buvo pataisytos tolesnės problemos.

**Laikas ir išlaidos**

- Išimtis atsiranda, kai patvirtinimo rinkinių žurnalų ilgis viršija 100 000 įrašų.
- Vartotojai negali pasiekti **laiko įrašo** tinklelio iš **pagrindinio puslapio Laiko** įrašas.
- **Dialogo lange Laiko įrašo importavimas** nerodomas joks tekstas, kai elementų negalima importuoti.
- Vartotojai gali kurti patvirtinimo rinkinius, kuriuose **laukas Paskirties būsena** nustatytas kaip **Nežinoma**.

**Projektų valdymas**

- Kai prasideda vasaros laikas, išteklių priskyrimuose UTC(+09:30) ir UTC(+10:00) kontūrai rodomi netinkamai.
- **Darbo** suskirstymo struktūrų laukas Papildomas stulpelis yra paslėptas kai kuriose lokalėse.
- Projekto užduočių tinklelio kalendoriaus valdiklio datos parinkiklis **netinkamai** lokalizuotas kinų kalba.

**Pardavimas**

- **Sutarties našumo** ir **projekto faktinės savikainos** vertės nesutampa, kai rezervuojami ištekliai, turintys skirtingus sutarčių vienetus ir valiutas, pateikia laiko įrašus.
- Pasirinktinė darbo eiga, automatiškai patvirtinant SF, nepavyksta, kai SF importuojamos kaip valdomasis sprendimas. Rodomas šis pranešimas: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Netinkama SF būsena".
- Kai **šakninė** parinktis pasirenkama kaip apibendrinimo parinktis, o projektas turi įvertinimų iš operacijų klasių mišinio (pvz., laiko, išlaidų ir medžiagų įvertinimų derinio), sistema apibendrina operacijų klases kaip vieną mokesčio eilutę.
- Tais atvejais, kai išlaidų eilutė pridedama prieš susiedami sutarties eilutę su projektu, lauke Naujinti kainą teisinga kainodara neįveita kaip numatytoji **vertė**.
- Neigiamos pardavimo sumos **neleidžiamos projekto** ir **užduoties** objektuose.
