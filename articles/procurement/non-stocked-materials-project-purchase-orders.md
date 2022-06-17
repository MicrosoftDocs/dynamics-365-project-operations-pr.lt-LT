---
title: Projektui skirtas atsargose nelaikomas medžiagas užsakykite naudodami projekto pirkimo užsakymus
description: Šiame straipsnyje paaiškinama, kaip galite užsisakyti nekauptas medžiagas projektui naudodami projekto pirkimo užsakymus.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929822"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Užsakyti projekto įsigijimo kategorijas arba nekauptas medžiagas naudojant projekto pirkimo užsakymus

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Jūsų organizacijos įsigijimo skyrius gali naudoti [pirkimo užsakymus](/dynamics365/supply-chain/procurement/purchase-order-overview) norėdamas sekti prekių ir paslaugų užsakymus. Pirkimo užsakymus pirkimo kategorijoms arba ne atsargų medžiagoms galima priskirti projektui. Išrašant šių pirkimo užsakymų sąskaitą savikaina registruojama pagal projektą.

## <a name="prerequisites"></a>Būtinosios sąlygos
Norėdami įjungti projekto pirkimo užsakymų funkcijas atlikite nurodytus veiksmus.

1. Dalyje Dynamics 365 Finance eikite į **darbo sritį Funkcijų valdymas**.
2. Funkcijų sąraše raskite ir pažymėkite funkciją **Įjungti projekto pirkimo užsakymus „Project Operations“ ištekliais pagrįstiems / atsargose nelaikomų prekių scenarijams**.
3. Pasirinkite **Įjungti**.
4. Konfigūruokite atsargose nelaikomas medžiagas ir laukiančias tiekėjo sąskaitas, kaip aprašyta skyriuje [Atsargose nelaikomų medžiagų ir laukiančių tiekėjo sąskaitų konfigūravimas](configure-materials-nonstocked.md).
5. Konfigūruokite įsigijimo kategorijas, kaip aprašyta dalyje [Naudoti įsigijimo kategorijas su projekto pirkimo užsakymais ir laukiančiomis tiekėjo SF](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Sukurkite projekto pirkimo užsakymą iš projekto pirkimo užsakymų sąrašo

1. Naudodami „Finance“ eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai** ir pasirinkite projektą.
2. Veiksmų srityje, skirtuke **Valdyti**, grupėje **Naujas**, pasirinkite **Prekės užduotis** > **Pirkimo užsakymas**.
3. Puslapyje **Kurti pirkimo užsakymą** pasirinkite tiekėją, kuriam norite pateikti pirkimo užsakymą, įveskite kitą informaciją ir pasirinkite **Gerai**.
4. Puslapyje **Pirkimo užsakymas**, **Pirkimo užsakymo eilučių** tinklelyje, pasirinkite **Įtraukti eilutę**.
5. Įveskite prekės numerį arba įsigijimo kategoriją, kiekį, vienetą, vieneto kainą ir kitą informaciją.

    > [!NOTE]
    > Su projekto pirkimo užsakymais galima naudoti tik įsigijimo kategorijas, nelaikomas prekes ir paslaugas. Sandėliuojamos prekės nepalaikomos.

6. Jei reikia, toliau įtraukite prekes arba įsigijimo kategorijas ir patvirtinkite pirkimo užsakymą.

    Prekių ir paslaugų kvitus galima įrašyti sukuriant ir registruojant produkto kvitą.

    > [!NOTE]
    > Produktų kvitai neįrašomi projekto faktiniuose duomenyse „Microsoft Dataverse“ ir neturi įtakos projekto papildomai knygai.

    Kai tiekėjas siunčia pirkimo užsakymo prekių ir paslaugų sąskaitą faktūrą, įsigijimo skyrius gali sugeneruoti pirkimo užsakymo sąskaitą faktūrą veiksmų srityje atsidaręs **Sąskaita faktūra** > **Generuoti** > **Sąskaita faktūra**. Daugiau informacijos apie laukiančias tiekėjo sąskaitas faktūras žr. [Atsargose nelaikomų medžiagų pirkimas naudojant laukiančią tiekėjo sąskaitą faktūrą](pending-vendor-invoices.md).
