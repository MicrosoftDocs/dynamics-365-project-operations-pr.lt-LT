---
title: Pajamų įvertinimų valdymas
description: Šiame straipsnyje pateikiama informacijos, kaip tvarkyti projektų pajamų įvertinimus.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 051535ce8dd4997a923b1511d242638361076979
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928488"
---
# <a name="manage-revenue-estimates"></a>Pajamų įvertinimų valdymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Galite kurti, apskaičiuoti, užregistruoti, atšaukti arba pašalinti pajamų įvertinimus. Tai galite padaryti rankiniu būdu arba naudodami periodinį procesą. Šiame straipsnyje pateikiama informacijos, kaip tvarkyti projektų pajamų įvertinimus.

### <a name="manage-revenue-estimates-manually"></a>Pajamų įvertinimų valdymas rankiniu būdu

Fiksuotos kainos pajamų įvertinimo projekte arba puslapyje **Įvertinimo užklausa** (**Projektų valdymas ir apskaita** > **Ataskaitos ir užklausos** > **Įvertinimų užklausos ir ataskaitos**) pasirinkite **Įvertinimai**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Pajamų įvertinimų tvarkymas naudojant periodinį procesą

Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Įvertinimai** ir pasirinkite atitinkamą procesą.

## <a name="create-a-revenue-estimate"></a>Pajamų įvertinimo kūrimas

Norėdami sukurti pajamų įvertinimą, atlikite toliau nurodytus veiksmus. 

1. Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Įvertinimai**.
2. Pasirinkite **Naujas**. Puslapyje **Įvertinimo kūrimas** pasirinkite toliau nurodytus parametrus.

   - **Laikotarpio kodas**: šis kodas apibrėžia, kaip dažnai užregistruojami įvertinimai.
   - **Įvertinimo data**: įvertinimo apdorojimo data.
   - **Ištisinis**: pažymėkite šį žymės langelį, kad įvertinimai būtų kuriami tik tada, jei įvertinimai buvo užregistruoti ankstesniame laikotarpyje arba jei įvertinimas yra pirmasis įvertinimas, kuris buvo sukurtas. Jei šis žymės langelis nepažymėtas, įvertinimai kuriami net ir tada, jei įvertinimai nebuvo užregistruoti ankstesniame laikotarpyje.
   - **Užbaigimo išlaidų apskaičiavimo metodas**: apibrėžia, kaip įvertinti likusį projekto darbą. Norėdami gauti daugiau informacijos žr. [Užbaigimo išlaidų apskaičiavimo metodai](cost-complete-methods.md).
   - **Užbaigimo metodas**: pasirinkite užbaigimo metodą iš toliau nurodytų parinkčių.
     - **Automatinis**: įvykdymo procentinė vertė apskaičiuojama automatiškai ir remiantis į skaičiavimą įtrauktomis sąnaudų eilutėmis. Sąnaudų šablonas apibrėžia sąnaudų eilutes, kurios yra įtraukiamos.
     - **Rankinis**: įvykdymo procentinė vertė yra lygi įvykdymo procentinei vertei, nustatytai atliekant paskutinį įvertinimą. Sukūrę įvertinimą galite pakeisti **Skaičiavimas rankiniu būdu** puslapyje **Įvertinimai**.
     - **Iš sąnaudų šablono**: automatinio ir rankinio metodų derinys. Ši parinktis nustatoma automatiškai arba rankiniu būdu, atsižvelgiant į numatytąją sąnaudų šablono reikšmę.
   - **Prognozės modelis**: pasirinkite įvertinimo prognozės modelį.
   - **Spausdinti įvertinimo sąrašą**: sukurkite ir peržiūrėkite įvertinimo sąrašą. Sąraše pateikiama esamos funkcijos būsena. Galite išspausdinti bet kokius įspėjimus, susijusios su ataskaitoje esančiu įvertinimu. Toliau nurodytais atvejais įvertinimo sąraše rodomas įspėjimas.
     - Įvykdymo procentinė vertė viršija 100 proc.
     - Įvykdymo procentinė vertė yra mažesnė už nulį.
     - Stulpelyje **Iki baigimo** yra neigiama reikšmė.
     - Įvertinime nenurodyta atitinkama sutarties suma.
     - Įvertinimas neturi pridėto išlaido įvertinimo.
   - **Rodyti sistemos pranešimą**: pasirinkite šią parinktį, kad gautumėte pranešimą, kuriame pateikiama informacija apie įvertinimo projektus, kurie buvo apdoroti vykdant užduotį.


## <a name="post-wip-or-accruals"></a>NG arba sukauptų sumų užregistravimas

Atlikus įvertinimus, jų vertės išlaikomos, mažėja arba didėja. Tada galite užregistruoti NG, kai naudojamas vertinimo principas **Baigta sutartis**, arba užregistruoti kaupimus, kai naudojamas vertinimo principas **Baigimo procentas**.
  
Įvertinimo laikotarpio būsena pakeičiama iš **Sukurta** į **Užregistruota**.

## <a name="reverse-wip-or-accruals"></a>NG arba sukauptų sumų atšaukimas

Naudokite atšaukimo parinktį, jei norite įtraukti jau užregistruotą NG ar sukauptas sumas į kreditą, ir tada sukurkite laikotarpio įvertinimus.

> [!NOTE]
> Norėdami atšaukti tarp kitų laikotarpių esantį laikotarpį, atšaukite reikiamus įvertinimo laikotarpius ir iš naujo juos užregistruokite. Kadangi visi paskesni laikotarpiai priklauso nuo ankstesnio laikotarpio įvertinimų, nepraleiskite jokių laikotarpių.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Vertinamo projekto pašalinimas ir projekto užbaigimas

Galutinis įvertinimo proceso veiksmas yra pašalinti vertinamą projektą ir užbaigti fiksuotos kainos projektą, kai įvykdymo procentas pasiekia 100 proc.

Vykdant pašalinimo veiksmą atliekami toliau nurodyti veiksmai.

- Fiksuotos kainos projektas su baigta sutartimi: NG vertės išvalomos iš balanso sąskaitų ir užregistruojamos pelno ir nuostolio sąskaitose.
- Fiksuotos kainos projektas su baigimo procentu: sukauptos sumos pašalinamos iš pelno ir nuostolio sąskaitų.

Įvertinimo būsena pakeičiama į **Pašalinta**.

> [!NOTE]
> Tam tikrais atvejais procentinė vertė gali būti didesnė nei 100 proc. Tokiu atveju sumažinkite atlikimo procentinę vertę naudodami metodą **Nustatyti nulinę užbaigimo išlaidų vertę**, kad pasiektumėte 100 proc.

## <a name="reverse-elimination"></a>Pašalinimo atšaukimas

1. Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Įvertinimai** > **Atšaukti pašalinimą**. 
2. Veiksmų srities skirtuko **Procesas** grupėje **Tvarkyti** pasirinkite **Įvertinimas**. 
3. Pasirinkite **Atšaukti pašalinimą**.

Naudodami šį puslapį, galite atšaukti visus pašalinimus su nurodyta įvertinimo data ir įvertinimo būsena **Pašalinta**. Operacijos būsena pasikeičia pasirinkus atitinkamus laukus.

Taip pat automatiškai pakeičiama projekto būsena į **Apdorojama**, jei projekto etapas nustatytas kaip baigtas. Projekto laikotarpio įvertinimo būsena pakeičiama į **Užregistruota**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]