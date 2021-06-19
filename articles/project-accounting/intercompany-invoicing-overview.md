---
title: Vidinės įmonės sąskaitų faktūrų išrašymo apžvalga
description: Šioje temoje pateikiama informacijos ir pavyzdžių apie vidinės įmonės SF išrašymą už projektus.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42af89105f8325f1c94df6d2133d2c329facf2b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002651"
---
# <a name="intercompany-invoicing-overview"></a>Vidinės įmonės sąskaitų faktūrų išrašymo apžvalga

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Jūsų organizaciją gali sudaryti keli skyriai, filialai ir kiti juridiniai subjektai, kurie, vykdydami projektus, keičiasi produktais ir paslaugomis. Juridinis subjektas, kuris teikia paslaugą arba produktą, vadinamas *skolinančiu juridiniu subjektu*. Juridinis subjektas, kuris gauna paslaugą arba produktą, vadinamas *besiskolinančiu juridiniu subjektu*.

Šioje iliustracijoje pavaizduotas įprastas scenarijus, kai du juridiniai objektai Contoso Robotics USA (besiskolinantis juridinis subjektas) ir Contoso Robotics UK (skolinantis juridinis subjektas) bendrina išteklius, kad klientui „Adventure works“ būtų galima vykdyti projektą. Pagal šį scenarijų Contoso Robotics USA sudarė sutartį teikti darbus „Adventure Works“.

![Vidinės įmonės sąskaitų faktūrų išrašymas](./media/IntercompanyScenario.png) 

„Dynamics 365 Project Operations“ naudoja toliau pateiktą srautą, kad apdorotų vidinės įmonės operacijas.

1. Skolinančio juridinio subjekto ištekliai įrašo vidinės įmonės laiko arba išlaidų operacijas rezervuodami laiką ir išlaidas besiskolinančio juridinio subjekto projektams.
2. Laiko ir išlaidų kaštai įrašomi skolinančioje įmonėje naudojant besiskolinančios įmonės vieneto savikainos kainoraštį.
3. Vidinės įmonės pardavimo, už kurį neišrašyta sąskaita, operacijos įrašomos skolinančioje įmonėje naudojant besiskolinančios įmonės vieneto savikainos kainoraštį.
4. Pajamos, už kurias neišrašyta sąskaita, įrašomos besiskolinančioje įmonėje naudojant projekto sutarties pardavimo kainoraštį. Klientui galima išrašyti sąskaitą, kai įrašomos pajamos, už kurias neišrašyta sąskaita. Klientas neturi laukti, kol bus baigtas vidinės įmonės sąskaitos faktūros apdorojimas.
5. Vidinės įmonės kliento sąskaitos faktūros sukuriamos periodiškai skolinančioje įmonėje. Sąskaitos faktūros sukuriamos rankiniu būdu arba naudojant periodinį automatinį procesą. Galima kurti vieną sąskaitą faktūrą kiekvienam besiskolinančiam juridiniam subjektui arba atskiras sąskaitas faktūras pagal projektą.
6. Kai vidinės įmonės kliento sąskaita faktūra užregistruojama skolinančiame juridiniame subjekte, atitinkama laukianti tiekėjo sąskaita faktūra sukuriama besiskolinančiame juridiniame subjekte. Laukiančioje tiekėjo sąskaitoje faktūroje esančios išlaidos bus įrašytos į projekto papildomą knygą, kai bus užregistruota sąskaita faktūra.

Toliau pateiktoje diagramoje vaizduojamas vidinės įmonės sąskaitų faktūrų išrašymas, kaip jis susijęs su apskaitos įvykiais ir numatomais registravimais didžiojoje knygoje.

![Vidinės įmonės srautas](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Papildomi ištekliai

- [Vidinės įmonės SF išrašymo konfigūravimas](configure-intercompany-invoicing.md)
- [Vidinės įmonės operacijų įrašymas](create-intercompany-transactions.md)
- [Vidinės įmonės kliento ir tiekėjo sąskaitų faktūrų kūrimas](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]