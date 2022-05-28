---
title: Tiekėjo užlaikymo apžvalga
description: Šioje temoje apžvelgiamos tiekėjo užlaikymo galimybės.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f9e4a1e63e47524bb622771f645c04e61c279496
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588470"
---
# <a name="vendor-retention-overview"></a>Tiekėjo užlaikymo apžvalga

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Jūsų organizacija gali norėti užlaikyti dalį mokėjimų tiekėjams, kurie dirba su jūsų organizacijos projektais. Pavyzdžiui, prieš mokėdami tiekėjui galite norėti įsitikinti, kad jų tiekiamos prekės ir paslaugos atitinka jūsų lūkesčius.

Kai su tiekėjais deratės dėl projektų pirkimo, galite nurodyti tiekėjo užlaikymo sąlygas, kuriose įtraukiamas užlaikomos sumos procentinis dydis. Kai tiekėjas pristato prekes ir teikia paslaugas, iš mokėjimo tiekėjui išskaičiuojate nurodytą užlaikymo procentinę dalį arba sumą. Kai projektas įvykdomas arba pasiekia tarpinį etapą, kaip nurodyta tiekėjo sutartyje, išleidžiate užlaikytą sumą ir sukuriate mokėjimą tiekėjui.

## <a name="vendor-retention-example"></a>Tiekėjo užlaikymo pavyzdys

Toliau pateiktame pavyzdyje parodoma, kaip užlaikoma tiekėjo sąskaitos faktūros sumos procentinė dalis, atsižvelgiant į projekto įvykdymo dalį.

„Contoso Robotics USA“ sutarė su tiekėju „Fabrikam“, kad šis dėl įrangos atnaujinimo projekto suteiks 100 mokymo valandų. Bendroji sutarties vertė yra 30 000 USD, o sutarta pirkimo kaina yra 300 USD už valandą.

Mokymas bus teikiamas trimis etapais pagal šį grafiką:

- 1 etapas: 50 valandų arba 50 procentų projekto
- 2 etapas: 30 valandų arba 80 procentų viso projekto
- 3 etapas: 20 valandų arba 100 procentų projekto

Šioje lentelėje išvardytos užlaikymo sąlygos.

| **Pristatytų vienetų procentinė dalis** | **Užlaikoma procentinė dalis** | **Išleidžiama procentinė dalis** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100 % | 0 % | 100 % |

Operacijose pateikiamos šios sumos:

- 1 etapas:
  - Mokėtina suma yra 50 x 300 arba 15 000.
  - 20 procentų sumos arba 3000 užlaikoma ir bus išleista vėlesniame etape.
  - Tiekėjui sumokėta suma yra 12 000.
- 2 etapas:
  - Mokėtina suma yra 30 x 300 arba 9 000.
  - Užlaikoma 10 procentų sumos arba 900.
  - Išleista 10 procentų nuo 3000, kurie buvo užlaikyti 1 etape.
  - Tiekėjui sumokėta suma yra 8 400. Ši suma yra 9000 atėmus 900 užlaikymą ir 300, kurie buvo išleisti iš 1 etapo užlaikymo.
- 3 etapas:
  - Mokėtina suma yra 20 x 300 arba 6000.
  - Neužlaikoma jokia suma.
  - Išleista suma yra 3600. Šią sumą sudaro 3000, kurie buvo užlaikyti 1 etape, atėmus 300 iš 1 etapo, kurie buvo išleisti 2 etape, ir 900, kurie buvo užlaikyti 2 etape.
  - Tiekėjui sumokėta suma yra 9600. Šią sumą sudaro 3600 užlaikyta suma ir 6000 už 3 etapo įvykdymą.

Bendra suma, sumokėta tiekėjui įvykdžius tris etapus, yra 30 000; tai yra bendra pirkimo užsakymo suma (15 000 + 9000 + 6000).
