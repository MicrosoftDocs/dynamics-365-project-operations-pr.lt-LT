---
title: Kas nauja arba pakeista „Project Service Automation“ V3 38 atnaujintame leidime
description: Šiame straipsnyje išvardijamos funkcijos ir taisymai, kuriuos galima rasti 38 naujinimo leidime Microsoft Dynamics 365 Project Service Automation, V3.
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

Šiame straipsnyje išvardijamos funkcijos ir pataisymai, kurie yra nauji arba pakeisti "Project Service Automation Update Release 38" V3. Šios versijos komponavimo versijos numeris yra V3.10.59.117 ir ji visuotinai pasiekiama įdiegiant savaiminį 2021 m. gruodžio mėn. naujinimą.

## <a name="update-release-38"></a>38 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

Buvo pataisytos tolesnės problemos.

**Laikas ir išlaidos**

- Išimtis įvyksta, kai patvirtinimo rinkinio žurnalų ilgis viršija 100 000 įrašų.
- Vartotojai negali pasiekti tinklelio **Laiko įrašas** iš pagrindinio puslapio Laiko **įrašas**.
- Dialogo **lange Laiko įrašo importavimas** nerodomas joks tekstas, kai jokie elementai negali būti importuoti.
- Vartotojai gali kurti patvirtinimo rinkinius, kuriuose laukas **Paskirties būsena** nustatytas kaip **Nežinomas**.

**Projektų valdymas**

- Kontūrai netinkamai rodomi išteklių priskyrimuose UTC (+09:30) ir UTC (+10:00), kai prasideda vasaros laikas.
- Kai kuriose vietovėse paslėptas laukas **Papildomas stulpelis** darbo paskirstymo struktūroms.
- Kalendoriaus valdiklio **datos parinkiklis projekto užduočių** tinklelyje nėra tinkamai lokalizuotas kinų kalba.

**Pardavimas**

- **Sutarties vykdymo** ir **projekto faktinių savikainų** vertės nesutampa, kai rezervuojami ištekliai, turintys skirtingus perkančiuosius vienetus ir valiutas, pateikia laiko įrašus.
- Pasirinktinė darbo eiga, skirta automatiškai patvirtinti SĄSKAITAS faktūras, nepavyksta, kai SF importuojamos kaip valdomasis sprendimas. Rodomas šis pranešimas: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Neleistina SF būsena".
- Kai **"Root"** pasirenkama kaip sumavimo parinktis, o projektas turi įvertinimus iš operacijų klasių mišinio (pvz., laiko, išlaidų ir medžiagų įvertinimų derinio), sistema apibendrina visas operacijų klases kaip vieną mokesčio eilutę.
- Tais atvejais, kai išlaidų eilutė įtraukiama prieš susiejant sutarties eilutę su projektu, teisinga kainodara lauke Naujinti kainą **neįvesta kaip numatytoji** vertė.
- Neigiamos pardavimo sumos projekto **ir** užduoties **objektuose** neleidžiamos.
