---
title: Finansinės dimensijos numatytosios reikšmės
description: Šioje temoje pateikta informacija apie tai, kaip nustatyti finansinių dimensijų numatytąsias reikšmes.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c1eb71d13ca7fc59118d15fef7ac914577b3b0e
ms.sourcegitcommit: fe5610464fdb5be756aa6a6a5b3c9a991dea0ed8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922948"
---
# <a name="financial-dimension-defaults"></a>Finansinės dimensijos numatytosios reikšmės

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

„Dynamics 365 Project Operations“ naudoja [finansinių dimensijų](/dynamics365/finance/general-ledger/financial-dimensions) sistemą programoje „Dynamics 365 Finance“, kad teiktų papildomų įžvalgų apie projekto papildomos knygos ir DK operacijas.

Numatytąsias finansines dimensijas galima nustatyti klientui, projekto finansavimo šaltiniui, etapui, projekto sutarties eilutei arba projektui.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Numatytųjų finansinių dimensijų apibrėžimas klientui

Kliento dimensijų numatytosios reikšmės nurodomos programoje „Finance“. Norėdami nustatyti numatytąsias dimensijų reikšmes, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Gautinos sumos** > **Klientai** > **Visi klientai**.
2. Puslapio **Klientai** skirtuke **Finansinės dimensijos** nustatykite konkretaus kliento finansinių dimensijų reikšmes.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Numatytųjų finansinių dimensijų apibrėžimas projekto sutartims

Projekto sutartys kuriamos ir tvarkomos naudojant „Common Data Service“ (CDS). Projekto sutarčių apskaitos atributai nustatyti „Finance“ modulyje **Projektų valdymas ir apskaita**.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Finansinių dimensijų nustatymas projekto finansavimo šaltiniui

1. Eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Projektų sutartys**.
2. Pažymėkite įrašą, kurį norite atnaujinti, ir skirtuke **Projekto sutartis** pasirinkite **Rodyti numatytąją apskaitą**.
3. Išplėskite **Susijusi informacija** ir pasirinkite skirtuką **Finansavimo šaltiniai**.
4. Nustatykite numatytąsias finansinių dimensijų reikšmes. Atkreipkite dėmesį, kad numatytosios finansinių dimensijų reikšmės gaunamos iš kliento paskyros.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Finansinių dimensijų nustatymas projekto sutarties eilutei

1. Eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Projektų sutartys**.
2. Pažymėkite įrašą, kurį norite atnaujinti, ir skirtuke **Projekto sutartis** pasirinkite **Rodyti numatytąją apskaitą**.
3. Išplėskite **Susijusi informacija** ir pasirinkite skirtuką **Sutarties eilutės**.
4. Nustatykite numatytąsias finansinių dimensijų reikšmes. Numatytosios finansinių dimensijų reikšmės taikytinos ir jas galima naudoti tik su fiksuotos kainos (etapų) sutarties eilutėmis.

Šios numatytosios reikšmės naudojamos susijusių projektų klientų operacijose ir sąskaitų faktūrų eilutėse.

## <a name="define-default-financial-dimensions-for-projects"></a>Numatytųjų finansinių dimensijų apibrėžimas projektams

Projektai kuriami ir tvarkomi naudojant (CDS). Projektų apskaitos atributai nustatyti „Finance“ modulyje **Projektų valdymas ir apskaita**.

1. Eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai**.
2. Pažymėkite įrašą, kurį norite atnaujinti, ir skirtuke **Projektas** pasirinkite **Rodyti numatytąją apskaitą**.
3. Išplėskite **Susijusi informacija** ir pasirinkite skirtuką **Sąranka**.
4. Nustatykite numatytąsias finansinių dimensijų reikšmes. Atkreipkite dėmesį, kad numatytosios finansinių dimensijų reikšmės gaunamos iš kliento paskyros. Jei projektas yra susietas su sutarties eilute, turinčia kelis projektų sutarčių klientus, numatytosioms finansinių dimensijų reikšmėms nustatyti naudojamas pirminis klientas.

Projekto numatytosios finansinės dimensijos naudojamos norint nustatyti laiko, išlaidų ir mokesčių operacijų žurnalų eilučių numatytąsias reikšmes **„Project Operations“ integravimo žurnale** ir susijusiose projekto sąskaitų faktūrų eilutėse.

## <a name="apply-financial-dimensions-for-project-time-entries"></a>Gretinti projekto laiko įrašų finansines dimensijas
Norėdami gretinti finansines dimensijas projekto laiko įrašams, atkreipkite dėmesį, kad numatytoji dimensijos vertė yra pagrįsta šiuo užsakymu:

1. Išteklius
2. Project
3. Finansavimo šaltinis

Pavyzdžiui, jei numatytoji dimensija nurodyta ištekliuje, ji bus taikoma pagal projekte nurodytą numatytąjį. Panašiai numatytoji projekto dimensija bus taikoma pagal numatytąjį, nurodytą finansavimo šaltinyje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
