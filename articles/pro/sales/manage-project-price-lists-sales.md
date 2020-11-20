---
title: Projektų kainoraščių valdymas projekto pasiūlymuose – „Lite“ versija
description: Šioje temoje pateikta informacija, kaip dirbti su projektų kainoraščiais pasiūlymuose. („Sales“)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ff830c63f7acf4cc23ac75d44afa9c3553b8724
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175991"
---
# <a name="manage-project-price-lists-on-project-quotes---lite"></a>Projektų kainoraščių valdymas projekto pasiūlymuose – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projektų pasiūlymai yra skirti kelių datų pardavimo kainoraščiams palaikyti. Naudojant „Dynamics 365 Project Operations“, įtraukiamas naujas susietas objektas, vadinamas **Projekto kainoraštis**. Šis objektas su projekto pasiūlymu turi ryšį nuo 1 iki daugelio.

Projektų kainoraščiai naudojami projekto laikui ir išlaidų operacijoms įkainoti. Kai pasiūlyme yra vienas ar daugiau projekto kainoraščių, šie kainoraščiai naudojami laikui ir išlaidų įvertinimams bei projekto faktiniams duomenims, susietiems su pasiūlymu per pasiūlymo eilutę, įkainoti.

Kai projekto pasiūlyme nėra projektų kainoraščių, gausite įspėjamąjį pranešimą. Pranešime nurodoma, kad dėl to, kad nėra projektų kainoraščių, įvertintas ir faktinis projekto darbas ir išlaidos nebus įkainotos. Vietoje to, jos turės nulinę (0) pardavimo reikšmių kainą.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Projekto kainoraščio susiejimas arba atsiejimas su projekto pasiūlymu

Norėdami sukurti arba pažymėti tam tikrą kainoraštį, skirtą projektu pagrįstam darbui ir išlaidoms įvertinti, atlikite toliau nurodytus veiksmus.

1. Pasiūlyme pasirinkite skirtuką **Projekto kaina**, o papildomame tinklelyje pasirinkite **+ Įtraukti naują projekto kainoraštį**.
2. Sparčiojo kūrimo puslapyje pažymėkite kainoraštį. Išplečiamajame sąraše rodomi visi kainoraščiai, kurių kontekstas nustatytas į **Pardavimai**, o valiuta atitinka pasiūlymo valiutą.
4. Įveskite projekto kainoraščio susiejimo aprašą ir pasirinkite **Įrašyti ir uždaryti**.

Sukuriamas projekto kainoraščio susiejimas.

Šį procesą galite pakartoti, jei į projekto pasiūlymą norite susieti daugiau nei vieną projekto kainoraštį. Jei kiekviename susietame projekto kainoraštyje yra skirtingos veiksmingos datos, sukurkite kelis projekto kainoraščius.

> [!NOTE]
> „Project Operations“ nepalaiko persidengiančių projekto kainoraščių datų efektyvumo. Jei yra keli projekto kainoraščiai operacijai su nurodyta data, šios operacijos kaina bus nustatyta kaip nulis (0).
Norėdami pašalinti projekto kainoraščio susiejimą, pažymėkite projekto kainoraštį ir pasirinkite **Naikinti pasiūlymo projekto kainoraštį**. Kainoraštis pašalinamas iš pasiūlymo projekto kainoraščio, tačiau pats kainoraštis nebus panaikintas. Panaikinamas tik susiejimas su pasiūlymu.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Numatytųjų projekto kainoraščių nustatymas pasiūlyme

Projektų kainoraščiai gali būti nustatyti pagal numatytuosius projekto pasiūlymus. Šis nustatymas užtikrina, kad visi jūsų organizacijos pasiūlymai visada prasidėtų su standartiniu kainoraščiu tam kainos laikotarpiui.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Organizacinių numatytųjų nustatymų nustatymas projekto kainoraščiams

1. Eikite į **Parametrai** > **Bendra** > **Parametrai**.
2. Sąrašo puslapyje **Aktyvieji parametrai** raskite įrašą ir dukart spustelėkite, kad jį atidarytumėte. 
3. Puslapyje **Parametrai** pažymėkite skirtuką **Kainoraštis**. Rodomas numatytųjų kainoraščių sąrašas. Tai yra standartinės kainos ir pardavimo kainoraščių sąrašai. Jei turite pardavimo kainoraštį, susietą su kiekviena valiuta, kurią parduodate, užtikrinsite, kad šis pardavimo kainoraštis būtų nustatytas pagal numatytuosius nustatymus kiekviename pasiūlyme, kurį sukuriate klientams, kurie prekiauja šia valiuta.

### <a name="set-up-customer-specific-project-price-lists"></a>Konkrečių klientų projektų kainoraščių nustatymas

Kai susiderėjote dėl pagrindinės kainodaros susitarimo su klientais, taip pat galite nustatyti konkrečių klientų projekto kainoraščius.

Norėdami nustatyti konkretaus kliento projekto kainoraštį, atlikite šiuos veiksmus.

1. Srityje **Pardavimai** pažymėkite **Klientai**.
2. Aktyvių klientų sąraše pažymėkite ir atidarykite kliento įrašą, kuriam turite specialų kainoraštį.
3. Skirtuke **Projektų kainoraščiai** galite sukurti naują kainoraščio susiejimą ir turėti projekto kainoraštį, būdingą klientui.

## <a name="create-custom-pricing-on-a-project-quote"></a>Projekto pasiūlymo pasirinktinių kainų kūrimas

Jei turite organizacinių ir klientui būdingų numatytųjų projektų kainoraščių, jūsų projekto pasiūlymai bus automatiškai sukurti naudojant šiuos projektų kainoraščio susiejimus. Tačiau tam tikrais atvejais gali prireikti sukurti tam tikro projekto pasiūlymo pasirinktines kainas. 

1. **Projekto pasiūlyme**, skirtuke **Projekto kainoraštis** patikrinkite papildomame tinklelyje, kad nepažymėtas konkretus kainoraščio įrašas.
2. Pasirinkite **Kurti pasirinktinę kainodarą**. Taip galėsite padaryti visų standartinių kainoraščių, kurie šiuo metu susieti su pasiūlymu, kopijas ir susieti jas su pasiūlymu. Esami susiejimai su standartiniais kainoraščiais bus pašalinti. Tada pardavėjas gali pradėti redaguoti šių kopijų kainas. Šios pakeistos kainos bus taikomos tik šiam projekto pasiūlymui.
