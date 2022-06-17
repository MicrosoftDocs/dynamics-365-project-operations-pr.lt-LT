---
title: Pajamų pripažinimo apžvalga
description: Šiame straipsnyje pateikiama informacija apie pajamų atpažinimą projekto operacijose.
author: sigitac
ms.date: 11/16/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 22486693226256f765589b272e6df36aceaf9c1c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926280"
---
# <a name="revenue-recognition-overview"></a>Pajamų pripažinimo apžvalga

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Programoje „Dynamics 365 Project Operations“ pajamų pripažinimo principai skiriasi atsižvelgiant į pasirinktą atsiskaitymo metodą, taikomą projektui arba projekto daliai. Šiame straipsnyje pateikiama informacija apie pajamų atpažinimą projekto operacijose.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Operacijos, įtraukiamos naudojant atsiskaitymo už laiką ir medžiagas metodą

- Išlaidų ir pajamų pripažinimas yra susiję tarpusavyje. Operacijos išlaidos ir pardavimas, už kurį neišrašyta sąskaita, užregistruojami naudojant [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md).
- Projekto išlaidų ir pajamų profilis nustato, ar pardavimo operacijos, už kurias neišrašyta sąskaita, registruojamos didžiojoje knygoje. Pasirinkus parinktį **Kaupti įplaukas**, sistema užregistruoja naudodama sąskaitas **NG – Pardavimo vertė** ir **Sukauptos įplaukos – Pardavimo vertė**. Toliau pateikiamas šio metodo pavyzdys.  

  | Operacijos tipas | Debetas / kreditas | Suma |
  | --- | --- | --- |
  | NG – Pardavimo vertė | Debetas | 100 |
  | Sukauptos įplaukos – Pardavimo vertė | Kreditas | 100 |

- Pajamos pripažįstamos išrašant SF. Sistema užregistruoja naudodama sąskaitą **įplaukos, kurioms išrašyta SF**. Toliau pateikiamas šio metodo pavyzdys.  

  | Operacijos tipas | Debetas / kreditas | Suma |
  | --- | --- | --- |
  | Kliento balansas | Debetas | 120 |
  | Mokėtinas PVM | Kreditas | 20 |
  | įplaukos, kurioms išrašyta SF | Kreditas | 100 |

- Jei įplaukos buvo sukauptos, kai yra užregistruojamas pardavimas, už kurį neišrašyta sąskaita, sistema atšauks sukauptas įplaukas išrašydama SF.

  | Operacijos tipas | Debetas / kreditas | Suma |
  | --- | --- | --- |
  | NG – Pardavimo vertė | Kreditas | 100 |
  | Sukauptos įplaukos – Pardavimo vertė | Debetas | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Operacijos, įtraukiamos naudojant fiksuotos kainos atsiskaitymo metodą

- Išlaidų ir pajamų pripažinimas yra atskiri procesai. Operacijos išlaidos užregistruojamos naudojant [„Project Operations“ integravimo žurnalą](../project-accounting/project-operations-integration-journal.md). Pardavimo, už kurį neišrašyta sąskaita, operacijos nesukuriamos.
- Pajamas galima pripažinti išrašant SF, jei projekto išlaidų ir pajamų profilyje parinktis **Projekto atliko skaičiavimo principas** nustatyta kaip **NG nėra**. Šį metodą taikykite tik trumpalaikiams, paprastiems projektams.
- Pajamas galima pripažinti naudojant fiksuotos kainos pajamų įvertinimus, taikant pajamų pripažinimo metodą **Baigta sutartis** arba **Įvykdymo procentas**.

## <a name="additional-resources"></a>Papildomi ištekliai
[Apmokėtinų projektų apskaitos konfigūravimas](../project-accounting/configure-accounting-billable-projects.md)

[Fiksuotos kainos pajamų vertinimo projektai](rev-rec-percentage-completion-method.md)

[Pajamų įvertinimų valdymas](rev-rec-completed-contract-method.md)

[Užbaigimo išlaidų apskaičiavimo metodai](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]