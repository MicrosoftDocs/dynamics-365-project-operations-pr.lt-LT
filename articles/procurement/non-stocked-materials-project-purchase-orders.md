---
title: Projektui skirtas atsargose nelaikomas medžiagas užsakykite naudodami projekto pirkimo užsakymus
description: Šioje temoje paaiškinama, kaip projektui skirtas atsargose nelaikomas medžiagas užsakyti naudojant projekto pirkimo užsakymus.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563032"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Projektui skirtas atsargose nelaikomas medžiagas užsakykite naudodami projekto pirkimo užsakymus

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Jūsų organizacijos įsigijimo skyrius gali naudoti [pirkimo užsakymus](/dynamics365/supply-chain/procurement/purchase-order-overview) norėdamas sekti prekių ir paslaugų užsakymus. Atsargose nelaikomų medžiagų pirkimo užsakymus galima priskirti projektui. Išrašant šių pirkimo užsakymų sąskaitą savikaina registruojama pagal projektą.

## <a name="prerequisites"></a>Būtinosios sąlygos
Norėdami įjungti projekto pirkimo užsakymų funkcijas atlikite nurodytus veiksmus.

1. Naudodami „Dynamics 365 Finance“ eikite į **Funkcijų valdymo** darbo sritį.
2. Funkcijų sąraše raskite ir pažymėkite funkciją **Įjungti projekto pirkimo užsakymus „Project Operations“ ištekliais pagrįstiems / atsargose nelaikomų prekių scenarijams**.
3. Pasirinkite **Įjungti**.
4. Konfigūruokite atsargose nelaikomas medžiagas ir laukiančias tiekėjo sąskaitas, kaip aprašyta skyriuje [Atsargose nelaikomų medžiagų ir laukiančių tiekėjo sąskaitų konfigūravimas](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Sukurkite projekto pirkimo užsakymą iš projekto pirkimo užsakymų sąrašo

1. Naudodami „Finance“ eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai** ir pasirinkite projektą.
2. Veiksmų srityje, skirtuke **Valdyti**, grupėje **Naujas**, pasirinkite **Prekės užduotis** > **Pirkimo užsakymas**.
3. Puslapyje **Kurti pirkimo užsakymą** pasirinkite tiekėją, kuriam norite pateikti pirkimo užsakymą, įveskite kitą informaciją ir pasirinkite **Gerai**.
4. Puslapyje **Pirkimo užsakymas**, **Pirkimo užsakymo eilučių** tinklelyje, pasirinkite **Įtraukti eilutę**.
5. Įveskite prekės numerį, kiekį, vienetą, vieneto kainą ir kitą atitinkamą informaciją.

    > [!NOTE]
    > Su projekto pirkimo užsakymais galima naudoti tik atsargose nelaikomas prekes ir paslaugas. Atsargose laikomos prekės ir įsigijimo kategorijos nepalaikomos.

6. Toliau įtraukite tiek prekių, kiek reikia, ir patvirtinkite pirkimo užsakymą.

    Prekių ir paslaugų kvitus galima įrašyti sukuriant ir registruojant produkto kvitą.

    > [!NOTE]
    > Produktų kvitai neįrašomi projekto faktiniuose duomenyse „Microsoft Dataverse“ ir neturi įtakos projekto papildomai knygai.

    Kai tiekėjas siunčia pirkimo užsakymo prekių ir paslaugų sąskaitą faktūrą, įsigijimo skyrius gali sugeneruoti pirkimo užsakymo sąskaitą faktūrą veiksmų srityje atsidaręs **Sąskaita faktūra** > **Generuoti** > **Sąskaita faktūra**. Daugiau informacijos apie laukiančias tiekėjo sąskaitas faktūras žr. [Atsargose nelaikomų medžiagų pirkimas naudojant laukiančią tiekėjo sąskaitą faktūrą](pending-vendor-invoices.md).
