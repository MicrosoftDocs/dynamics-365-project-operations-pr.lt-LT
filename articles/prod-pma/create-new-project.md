---
title: Kurti naują projektą;
description: Šiame straipsnyje pateikiama informacija apie tai, kaip sukurti naują projektą.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbe7ea7d6ee57b3494494a2758dbcb7ded735dc1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919702"
---
# <a name="create-a-new-project"></a>Kurti naują projektą;

[!include [banner](../includes/banner.md)]

Atlikite šiuos veiksmus, kad sukurtumėte naują projektą.

1. Puslapyje **Projektų valdymas** pasirinkite **Naujas projektas** ir įveskite toliau nurodytas reikšmes.

    - **Projekto tipas:** laikas ir medžiagos
    - **Projekto pavadinimas:** XYZ Upgrade Phase 2
    - **Projektų grupė:** TM\_WIP
    - **Projekto sutarties ID:** 00000002

2. Pasirinkite **Kurti projektą**.

## <a name="assign-a-resource-to-a-project"></a>Išteklių priskyrimas projektui

1. Puslapio **Darbuotojai** sąraše **Darbuotojai** pasirinkite darbuotojo, kuriam anksčiau nustatėte kompetencijas, įrašą, ir atidarykite darbuotojo įrašą.
2. Veiksmų srityje, skirtuke **Projektas**, grupėje **Sąranka**, pasirinkite **Priskirti projektus**.
3. Puslapyje **Išteklių tikrinimo projekto priskyrimai**, skirtuke **Projektai**, lauke **Įtraukti projektą į pasirinktus projektus** filtruokite projektą **XYZ Upgrade Phase 2**.
4. Srityje **Likę projektai** pasirinkite projektą, tada pasirinkite rodyklės mygtuką, kad įtrauktumėte jį į sritį **Pasirinkti projektai**.

Jeigu reikia, taip pat galite priskirti ištekliaus kategorijas. Kategorijos tipas yra arba **Išlaidos**, arba **Pajamos**. Kategorijos tipą nustato jūsų organizacija. Jeigu ištekliui nepriskirta jokių kategorijų, „Finance” ieško numatytosios kategorijos pagal išlaidų ir pajamų valandos kainą.

## <a name="set-up-project-resource-and-role-characteristics"></a>Projektų išteklių ir vaidmens ypatybių nustatymas

Projektų vadovas gali naudoti projekto išteklių paskirstymo funkcijas, kad sukurtų projektui reikiamus vaidmenis. Vaidmenys gali būti naudojami, kai rezervuojant išteklius, patvirtinti ištekliai vis dar nėra žinomi. Vaidmenys gali būti laikinai rezervuojami kaip planuojami ištekliai, kad galėtumėte toliau vykdyti projekto planavimo etapus.

[![Vaidmens pavyzdys.](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenarijus:** įmonė „Contoso” buvo pasamdyta užbaigti laiko ir medžiagų projektą, turintį patvirtintą projekto chartiją. Jaunesnysis projekto vadovas vis dar nustato projekto aprėptį. Išteklių vadovas dabar nustato konkrečius išteklius, kurie bus rezervuojami darbui naujame projekte. Projektas yra svarbus, todėl projekto rėmėjas paprašė nustatyti vyresniojo projekto vadovo vaidmenį kaip vieną iš vaidmenų. Išteklių vadovas turi gauti naują išteklių ir apibrėžti vaidmenį sistemoje, nes jaunesniajam projekto vadovui planuojant projektą gali prireikti ištekliaus informacijos.

Toliau pateikiamais veiksmais parodoma, kaip išteklių vadovas gali nustatyti vyresniojo projekto vadovo vaidmenį ir susieti su juo ištekliaus charakteristikas. Vėliau vaidmenį galima naudoti norint ieškoti galimų išteklių, atitinkančių reikiamas išteklių kompetencijas.

1. Puslapyje **Vaidmenų nustatymas** pasirinkite **Naujas** ir įveskite toliau nurodytas reikšmes.

    - **Vaidmens ID:** vyresnysis projekto vadovas
    - **Aprašas:** vyresnysis projekto vadovas

2. Pasirinkite **Kurti**.
3. Pasirinkite vaidmenį **Vyresnysis projekto vadovas**, tada pasirinkite **Konfigūruoti ypatybes**.
4. Lauke **Charakteristikų tipas** pažymėkite **Įgūdis**.
5. Lauke **Galimos charakteristikos** įveskite ieškomą įgūdį.
6. Lauke **Charakteristikų tipas** pažymėkite **Sertifikatas**.
7. Lauke **Galimos charakteristikos** įveskite ieškomą sertifikato tipą.

## <a name="assign-a-project-resource-to-a-project"></a>Projekto išteklių priskyrimas projektui

1. Puslapyje **Visi projektai** pasirinkite projektą **XYZ Upgrade Phase 2**.
2. Skirtuke **Projekto komanda ir planavimas** pasirinkite **įtraukti**.
3. Lauke **Vaidmuo** pasirinkite **Komandos narys**.
4. Pasirinkite **Rezervuoti iš kalendoriaus**.
5. Puslapyje **Išteklių pasiekiamumas** pasirinkite **Peržiūrėti parametrus**.
6. Puslapyje **Koreguoti rodinio parametrus** įveskite toliau nurodytas reikšmes.

    - **Datų diapazono rodinio formatas:** diena
    - **Rodyti pasiekiamumo aprašus:** taip
    - **Rodyti likusį pajėgumą:** taip

7. Išteklių sąraše pasirinkite išteklių.
8. Pasirinkite **Rezervuoti galutinai** ir **Viso pajėgumo metodas**.

## <a name="assign-a-resource-to-a-default-role"></a>Ištekliaus priskyrimas numatytajam vaidmeniui

Norint padėti projekto ar išteklių vadovams, galima toliau detalizuoti projektui rezervuojamus išteklius. Numatytąjį vaidmenį galite susieti su esamais ištekliais arba su naujai gautu ištekliumi. Pavyzdžiui, kai Danielis buvo pasamdytas, jis turėjo patirtį ir įgūdžius, atitinkančius verslo analitiko vaidmenį. Išteklių vadovas priskyrė šį vaidmenį kaip numatytąjį Danieliaus vaidmenį. Todėl išteklių vadovas įtraukė Danielį į verslo analitikų, galinčių dirbti projektuose, telkinį.

Rezervuodami išteklius, projektų vadovai gali filtruoti vaidmens išteklius, galinčius dirbti projektuose. Jie gali naudoti šią informaciją kaip vieną kriterijų, kai atlieka keliais kriterijais grindžiamą sprendimų analizę išteklių panaudojimo metu. Be to, filtruodami jie gali įtraukti kitų išteklių charakteristikų, kad galėtų ieškoti išteklių, turinčių konkrečių įgūdžių, išsilavinimą ir patirtį, kurių reikia dirbant nurodytame projekte.

**Scenarijus:** pradėtas vykdyti patvirtintas projektas, o vyresniojo projekto vadovo vaidmuo buvo rezervuotas kaip planuotas išteklius projekto planavimo etape. Dabar išteklių vadovas gavo išteklių, kuris atitinka vyresniojo projekto vadovo vaidmenį.

1. Puslapyje **Išteklių sąrašas** pasirinkite **Danielis Goldschmidtas**.
2. Puslapyje **Ištekliaus vaidmuo** pasirinkite **Naujas** ir įveskite toliau nurodytas reikšmes.

    - **Įsigaliojimo data:** įveskite šiandienos datą.
    - **Galiojimo pabaigos data:** įveskite **Niekada**.
    - **Vaidmuo:** įveskite **vyresnysis projekto vadovas**.

3. Spustelėkite **Įrašyti** ir uždarykite puslapį.
4. Skirtuke **Kompetencijos** įtraukite įgūdį **ProjectMgmt** ir sertifikatą **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]