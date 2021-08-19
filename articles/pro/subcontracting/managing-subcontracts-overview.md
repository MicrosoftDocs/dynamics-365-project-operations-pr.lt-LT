---
title: „Project Operations“ valdymas pagal subrangos sutartį
description: Šioje temoje pateikta tiesioginio subrangos valdymo proceso programoje „Microsoft Dynamics 365 Project Operations” apžvalga.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994241"
---
# <a name="subcontract-management-in-project-operations"></a>„Project Operations“ valdymas pagal subrangos sutartį

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Subrangos sutarties sudarymas programoje „Microsoft Dynamics 365 Project Operations“ palaiko toliau nurodytą veiklos procesų seką.

![Subrangos procesų seka](../media/SubcontractingProcessFlow.png)

Čia pateikiamas nuoseklus subrangos proceso aprašymas.

1. Projekto vadovas sudaro subrangos sutartį su tiekėju. Pagal numatytuosius nustatymus prie tiekėjo įrašo pridėti kainoraščiai yra naudojami sudarant subrangos sutartį. Tiekėjo kliento ryšio tipas yra **Tiekėjas** arba **Pristatytojas**.
2. Projekto vadovas gali detalizuoti visus pirkimus kaip subrangos sutarties eilutės elementus. Gali būti laiko, išlaidų arba produktų subrangos sutarties eilutės. Kiekvienoje subrangos sutarties eilutėje pasirinkta operacijos klasė nurodo, kam skirta eilutė.
3. Tiekėjo kliento vadovas ir projekto vadovas gali kartoti subrangos sutartį. Įkainius galima koreguoti pirkimo kainoraščiuose, pridedamuose prie subrangos sutarties.
4. Šiame etape arba vėliau, jei subrangos sutarties eilutė yra skirta laikui, tiekėjo kliento vadovas susieja kontaktus su kiekviena subrangos kliento eilute. Šis susiejimas teikia informaciją projekto vadovui, dirbančiam su subrangos sutartimi. Susiejus kontaktą su subrangos sutarties eilute, sistema automatiškai sukuria rezervuojamą išteklių iš šio kontakto, jei rezervuojamo ištekliaus dar nėra.
5. Kiekvienos subrangos sutarties eilutės atsiskaitymo metodas gali būti **Fiksuota kaina** arba **Laikas ir medžiagos**. Fiksuotos kainos subrangos sutarties eilutėms galite nustatyti etapais pagrįstą sąskaitos faktūros grafiką.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
