---
title: Kas nauja arba pakeista „Project Service Automation“ V3 21 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 21 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 69b592db7456bf11c2e933256569d726056d1a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280633"
---
# <a name="project-service-automation-update-release-21-v3"></a>„Project Service Automation“ V3 21 naujinimo leidimas

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 21 atnaujintame leidime. Šios versijos komponavimo versijos numeris yra V 3.10.32.50 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. birželio mėn.

## <a name="update-release-21"></a>21 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

Buvo pataisytos šios problemos:

- Kai ataskaitų srityje veikia **Laiko įrašo tinklelio valdymas**, tinklelis nenaudoja viso ataskaitų srities tinklelio talpyklės pločio.
- Tam tikroms laiko juostoms **Laiko įrašo** tinklelio valdiklis nerodo įrašų.
- Laiko įrašai, vėlesni nei 21:00, rodomi netinkamą parą.
- Vartotojai negali pateikti išlaidų, jei išlaidų kategorijai **Būtinas išlaidų kvitas** nėra nustatytos reikšmės.

**Išteklių valdymas**

Buvo pataisytos šios problemos:

- Nesuaktyvinti užsakymai rodomi rodinyje **Suderinimas**.
- Bendrojo ištekliaus užpildymas nebuvo patikrintas siekiant užtikrinti, kad egzistuotų tinkama rezervavimo būsena.

**Projektų valdymas**

Buvo pataisytos šios problemos:

- **Projekto** formos tinklelius (rodiniai **Išteklių priskyrimas**, **Užduotis**, **Suderinimas**, **Išlaidų sąmatos**) galima redaguoti net tada, kai projektas nėra aktyvus.
- Dubliuotų klientų negalima sulieti su klientais, susijusiais su patvirtintomis projekto sutartimis.
- Kai pridedamas išteklius, neturintis galiojančio kalendoriaus, sistema neparodo vartotojui patogaus klaidos pranešimo.
- Mygtukas **Pridėti užduotį** įjungiamas užduočių tinklelyje tada, kai projektas susiejamas su **„Microsoft Project“ papildiniu**.
- Pastangos didėja nevaldomai, kai užduotis su kategorija yra priskiriama ištekliui su vaidmeniu, kuriam yra nustatyta savikaina.

**„Sales“**

Buvo atlikti šie patobulinimai:

- **Sąskaitos faktūros dažnumas** ir **Atsiskaitymo pradžia** perkelti į skirtuką **Sąskaitų faktūrų grafikas**.

Buvo pataisytos šios problemos:

- **Kategorijoje** **Bendroji pardavimo kaina** yra nulis (0) , nors vertė **Vaidmuo** turi bendrą pardavimo kainą, nelygią nuliui.
- Klientai negali pakeisti lauko **Sąskaitos faktūros būsenos** reikšmės į **Parengta išrašyti sąskaitą faktūrą**, kai kitas tinkinamas procesas naujina papildomą lauką.
- Mygtuku **Atnaujinti sąskaitų faktūrų eilutes** galima sukurti kelias dubliuotas eilutes, jei jis yra pakartotinai paspaudžiamas.
- Mygtukas **Naujinti kainas** neveikia papildomame tinklelyje **Vaidmens kainos** formoje **Sparčioji peržiūra**.
- **Pardavimo kainoraščio aprašo** algoritmas netinkamai apdoroja laiko juostas, todėl gaunamas netinkamas kainoraščių pasirinkimas.
- Patvirtinus vieno laiko įrašą, projekto **Faktinių išlaidų suma** gali turėti nežymią paklaidą.
- **Kainų aprašo** algoritmas nepateikia vartotojui patogaus pranešimo, jei **Gauta vaidmenų kaina** neturi reikšmių laukuose **Pagrindinis vienetas** ir **Kaina pagrindiniu vienetu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]