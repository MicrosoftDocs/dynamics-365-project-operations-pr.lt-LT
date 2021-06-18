---
title: Projekto išteklių nustatymas
description: Šioje temoje pateikiama informacija, kaip nustatyti arba prašyti projekto išteklių.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997701"
---
# <a name="set-up-project-resources"></a>Projekto išteklių nustatymas

[!include [banner](../includes/banner.md)]

Turite nustatyti kalendorių ir susieti jį su darbuotoju. Kalendorius naudojamas projekto ir projektui rezervuotų išteklių darbo laiko grafikui sudaryti. Atlikdami kalendoriaus sąranką, projekto vadovai išteklių optimizavimo metu gali koreguoti išteklių paskirstymą. Ištekliams gali būti taikomi apribojimai pagal kalendoriaus grafiką. Kalendorių galite nustatyti puslapyje **Kalendorius**.

Kai nustatote darbuotoją kaip projekto išteklių, galite pasirinkti iš darbuotojų, dirbančių įmonėje, kuriai nustatote išteklius. Arba galite pasirinkti darbuotojus iš kitų jūsų organizacijoje esančių įmonių. Šie darbuotojai vadinami vidinės įmonės ištekliais.

Toliau pateikiamose procedūrose paaiškinama, kaip nustatyti darbuotoją kaip jūsų įmonės projekto išteklių ir kaip nustatyti vidinės įmonės projekto išteklius.

## <a name="set-up-a-worker-as-a-project-resource"></a>Darbuotojo kaip projekto ištekliaus nustatymas

1. Puslapyje **Darbuotojai** sąraše **Darbuotojai** pasirinkite darbuotoją, kurį įtraukiate kaip projekto išteklių, ir atidarykite darbuotojo įrašą.
2. Veiksmų srityje pasirinkite **Projektas** &gt; **Sąranka** &gt; **Projekto sąranka**.
3. Pasirinkite kalendorių, tada uždarykite puslapį.

Taip pat galite nurodyti išteklių numatytuosius projektus kaip išankstinio priskyrimo tipą. Išankstinius priskyrimus galima naudoti, kai išteklių vadovas arba projektų vadovas iš anksto žino, su kuriais projektais dirbs išteklius. Išankstiniai priskyrimai taip pat gali būti grindžiami projekto rėmėjo ar kliento prašymu. Norėdami iš anksto priskirti projektą, puslapio **Projektų priskyrimas** skirtuko **Projektai** sąraše **Likę projektai** pažymėkite atitinkamą projektą.

## <a name="set-up-an-intercompany-resource"></a>Vidinės įmonės išteklių nustatymas

Kai nustatote darbuotoją kaip vidinės įmonės išteklių, turite atlikti sąranką ir nuomojančioje, ir besiskolinančioje įmonėje.

### <a name="in-the-lending-company"></a>Nuomojančioje įmonėje

1. Programoje „Finance” patikrinkite, ar pažymėta nuomojanti įmonė, tada atlikite ankstesniame skyriuje „Darbuotojo kaip projekto ištekliaus nustatymas” pateiktą procedūrą.
2. Puslapyje **Vidinės įmonės apskaita** pasirinkite **Nauja**.
3. Lauke **Juridinio subjekto ID** pažymėkite nuomojančią įmonę. Tinkamai užpildykite likusius laukus ir pasirinkite **Įrašyti**.
4. Puslapyje **Perkėlimo kaina** pasirinkite **Nauja**.
5. Lauke **Besiskolinančio juridinio subjekto ID** pažymėkite tinkamą įmonę.
6. Jeigu norite besiskolinančiai įmonei išnuomoti tik tą išteklių, kurį sukūrėte šio skyriaus pradžioje, lauke **Ištekliai**, pasirinkite sukurto ištekliaus pavadinimą. Jeigu norite, kad besiskolinančioji įmonė galėtų pasiekti visus nuomojančios įmonės išteklius, palikite lauką **Ištekliai** tuščią.
7. Puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **Vidinė įmonė** nustatykite parinktį **Įgalinti vidinės įmonės išteklių planavimą ir grafikų sudarymą** kaip **Taip**.

### <a name="in-the-borrowing-company"></a>Besiskolinančioje įmonėje

- Puslapio **Išteklių sąrašas** ieškos filtre įveskite ištekliaus, kurį sukūrėte nuomojančiai įmonei, pavadinimą, kad patikrintumėte, ar pavadinimas įtrauktas į besiskolinančios įmonės išteklių sąrašą.

## <a name="request-project-resources"></a>Projektų išteklių prašymas
Projektų išteklių planavimo funkcijos leidžia išteklių vadovams tik paskirstyti darbuotojams įtraukimuose ar projektuose priskirtus išteklius. Norėdami įgalinti šias funkcijas, atlikite toliau pateikiamas užduotis arba patikrinkite, ar jos buvo atliktos.

- Nustatykite numerių sekas.
- Nustatykite projektų valdymo ir apskaitos darbo eigas.
- Įgalinkite išteklių užklausos darbo eigas.

Jeigu reikia, atlikę ankstesnes užduotis, galite atlikti toliau pateikiamas užduotis.

- Sukurkite ištekliaus užklausą iš preliminariai rezervuoto darbuotojui priskirto ištekliaus.
- Stebėkite išteklių užklausas.
- Vykdykite išteklių užklausas.
- Prašykite darbuotojui priskirto ištekliaus iš WBS.
- Rezervuokite išteklius projektui, neturėdami darbuotojui priskirto ištekliaus užklausos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]