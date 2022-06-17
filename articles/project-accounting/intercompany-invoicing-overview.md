---
title: Vidinės įmonės sąskaitų faktūrų išrašymo apžvalga
description: Šiame straipsnyje pateikiama informacija ir pavyzdžiai apie projektų vidinės įmonės SF išrašymą.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd17f6542558bae9d4b97d0a92aefae52571cfa8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913584"
---
# <a name="intercompany-invoicing-overview"></a>Vidinės įmonės sąskaitų faktūrų išrašymo apžvalga

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Jūsų organizaciją gali sudaryti keli skyriai, filialai ir kiti juridiniai subjektai, kurie, vykdydami projektus, keičiasi produktais ir paslaugomis. Juridinis subjektas, kuris teikia paslaugą arba produktą, vadinamas *skolinančiu juridiniu subjektu*. Juridinis subjektas, kuris gauna paslaugą arba produktą, vadinamas *besiskolinančiu juridiniu subjektu*.

Toliau pateikiamas tipiško scenarijaus pavyzdys: du juridiniai subjektai „Contoso Robotics USA“ (besiskolinantis juridinis subjektas) ir „Contoso Robotics UK“ (skolinantis juridinis subjektas) dalijasi ištekliais, kad pateiktų projektą klientui „Adventure Works“. Šiuo atveju su „Contoso Robotics USA“ sudaryta sutartis, pagal kurią ji turi pateikti darbą įmonei „Adventure Works“.

![Vidinės įmonės sąskaitų faktūrų išrašymas.](./media/IntercompanyScenario.png) 

„Dynamics 365 Project Operations“ naudoja toliau pateiktą srautą, kad apdorotų vidinės įmonės operacijas.

1. Skolinančio juridinio subjekto ištekliai įrašo vidinės įmonės laiko arba išlaidų operacijas rezervuodami laiką ir išlaidas besiskolinančio juridinio subjekto projektams.
2. Laiko ir išlaidų kaštai įrašomi skolinančioje įmonėje naudojant besiskolinančios įmonės vieneto savikainos kainoraštį.
3. Vidinės įmonės pardavimo, už kurį neišrašyta sąskaita, operacijos įrašomos skolinančioje įmonėje naudojant besiskolinančios įmonės vieneto savikainos kainoraštį.
4. Pajamos, už kurias neišrašyta sąskaita, įrašomos besiskolinančioje įmonėje naudojant projekto sutarties pardavimo kainoraštį. Klientui galima išrašyti sąskaitą, kai įrašomos pajamos, už kurias neišrašyta sąskaita. Klientas neturi laukti, kol bus baigtas vidinės įmonės sąskaitos faktūros apdorojimas.
5. Vidinės įmonės kliento sąskaitos faktūros sukuriamos periodiškai skolinančioje įmonėje. Sąskaitos faktūros sukuriamos rankiniu būdu arba naudojant periodinį automatinį procesą. Galima kurti vieną sąskaitą faktūrą kiekvienam besiskolinančiam juridiniam subjektui arba atskiras sąskaitas faktūras pagal projektą.
6. Kai vidinės įmonės kliento sąskaita faktūra užregistruojama skolinančiame juridiniame subjekte, atitinkama laukianti tiekėjo sąskaita faktūra sukuriama besiskolinančiame juridiniame subjekte. Laukiančioje tiekėjo sąskaitoje faktūroje esančios išlaidos bus įrašytos į projekto papildomą knygą, kai bus užregistruota sąskaita faktūra.

Toliau pateiktoje diagramoje vaizduojamas vidinės įmonės sąskaitų faktūrų išrašymas, kaip jis susijęs su apskaitos įvykiais ir numatomais registravimais didžiojoje knygoje.

![Vidinės įmonės srautas.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Vidinės įmonės SF išrašymo konfigūravimas](configure-intercompany-invoicing.md)
- [Vidinės įmonės operacijų įrašymas](create-intercompany-transactions.md)
- [Vidinės įmonės kliento ir tiekėjo sąskaitų faktūrų kūrimas](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]