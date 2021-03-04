---
title: Kas nauja arba pakeista „Project Service Automation“ V3 17 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 17 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143745"
---
# <a name="project-service-automation-update-release-17-v3"></a>„Project Service Automation“ V3 17 naujinimo leidimas

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.  Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti PSA V3 17 atnaujintame leidime. Ši versija turi naują komponavimo versijos numerį V3.10.6.34 ir ją galima pasiekti per 2020 m. kovo mėn. automatinį naujinimą.


## <a name="update-release-17"></a>17 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Bendra**

- Ištaisyta: atnaujinta „Project Service Automation“, kad būtų vykdomos komandos narių licencijos (projekto išteklių telkinys turės 3.x komandos narių tarnybos plano metaduomenis)
 
**Laikas ir išlaidos**

- Ištaisyta: neįmanoma pakeisti išlaidų sąmatos iš nenulinės kainos į nulinę (0). Pakeitimas yra ignoruojamas.

**Projektų valdymas**

- Ištaisyta: nulinių reikšmių tikrinimas įtrauktas į komandos nario pareigų pavadinimą.
- Ištaisyta: laukas **msdyn_userresourceid** objekte **msdyn_resourceassignment** nebenaudojamas.
- Ištaisyta: naujinimas iš versijos 2.x į 3.x dabar tvarko tuščius pastangų kontūrus užduočių priskyrimuose.

**„Sales“**

- Ištaisyta: **Invoice.PreValidateInvoiceUpdate** dabar tinkamai tvarko įrašų savininkų priskyrimo iš naujo scenarijus.
- Ištaisyta: kai operacijos klasė yra **Laikas**, visų objektų **UnitGroup** yra neredaguotina, įskaitant **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** ir **ContractLineDetails**. Tačiau **Vienetas** negalima redaguoti tik **JournalLine** ir **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]