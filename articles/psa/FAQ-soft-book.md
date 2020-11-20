---
title: Preliminarus išteklių rezervavimas
description: Šioje temoje pateikiama informacija apie tai, kaip preliminariai planuoti arba preliminariai rezervuoti projekto komandos narius.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.openlocfilehash: af71ff9d60e237a9d1379b3ccd4c0d5ffce411e4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122218"
---
# <a name="soft-book-a-resource"></a>Preliminarus išteklių rezervavimas

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Galite preliminariai planuoti arba preliminariai rezervuoti išteklius projekto komandai norėdami parodyti, kad planuojate tuos išteklius priskirti projektui. Preliminarūs rezervavimai nenaudoja galimo išteklių pajėgumo, be to, preliminariai rezervuotus komandos narius galite priskirti prie projekto užduočių. Tačiau, kadangi preliminarus rezervavimas nenaudoja išteklių pajėgumo, vis vien galite galutinai rezervuoti išteklius kitoms užduotims tam pačiam laikotarpiui. Bendrieji ištekliai negali būti rezervuojami preliminariai, o preliminarūs rezervavimai negali įvykdyti bendrųjų išteklių užklausos.

Preliminariai rezervuoti projekto komandos nariai surašyti puslapio **„Projektas“** skirtuke **„Komanda”**, o jų preliminariai rezervuotos valandos rodomos stulpelyje **„Preliminariai rezervuotos valandos”**, rodinyje **„Įvardytieji komandos nariai”**. Preliminariai rezervuoti komandos nariai taip pat surašyti Grafiko lentoje. Kadangi jie yra rezervuoti preliminariai, Grafiko lentoje nerodomas joks tų išteklių pajėgumo sunaudojimas. Preliminariai rezervuotas laikas nėra rodomas nei Grafiko lentos skirtuke **„Derinimas”**, nei lauke **„Išplėsti rezervavimus”** esančiame skirtuke **„Derinimas”**. 

Yra du būdai preliminariai rezervuoti komandos narį projektui: tiesiogiai Grafiko lentoje arba pridedant komandos narį skirtuke **„Komanda”**. 

## <a name="soft-book-from-the-schedule-board"></a>Preliminarus rezervavimas Grafiko lentoje
Atlikite šiuos veiksmus norėdami preliminariai rezervuoti Grafiko lentoje esančius išteklius. 

1. Atidarykite Grafiko lentą, tada srityje **„Rezervavimo reikalavimai“** pasirinkite skirtuką **„Projektas“**.
2. Suraskite projektą, kuriam norite preliminariai rezervuoti išteklius. Jei sąraše yra didelis projektų skaičius, pasirinkite stulpelio antraštę **„Projektas“** ir, naudodami filtrą, ieškokite vieno ar daugiau projektų.
3. Pasirinkite projektą, tada nuvilkite jį ant išteklių laiko tinklelio.
5. Srityje **„Kurti išteklių rezervavimą”** koreguokite pradžios ir pabaigos datas, nustatykite **„Rezervavimo būseną“** į **„Preliminari“** ir tada nustatykite valandas. 
6. Spustelėkite **„Rezervuoti”**. Ištekliai bus matomi skirtuke **„Komanda”** kaip projekto ištekliai. Rodinio **„Įvardytieji komandos nariai”** stulpelyje **„Preliminariai rezervuotos valandos”** bus nurodytos preliminariai rezervuotos valandos.

> [!NOTE]
> Dabar skirtuke **„Grafikas”** galėsite priskirti preliminariai rezervuotus išteklius užduotims. Skirtuke **„Derinimas”** rodomas išteklių rezervavimo deficitas, susijęs su jų užduočių priskyrimu, kadangi skirtuke **„Derinimas”** atsižvelgiama tik į galutinius rezervavimus. Norėdami galutinai rezervuoti išteklius ir taip pašalinti galutinių rezervavimų deficitą išteklių priskyrimo atžvilgiu, galite pasinaudoti funkcija **„Išplėsti rezervavimus”**. Turėsite rankiniu būdu atšaukti preliminarų išteklių rezervavimą, naudodami funkciją **„Išlaikyti rezervavimus”**.

## <a name="soft-book-on-the-team-tab"></a>Preliminarus rezervavimas skirtuke „Komanda”

Galite pridėti komandos narius tiesiogiai skirtuke **„Komanda”** ir tada pakeisti jų rezervavimo būseną iš **„Galutinė”** į **„Preliminari”**, naudodami funkciją **„Išlaikyti rezervavimus”**. Kai tokiu būdu pridedate komandos narį, visada bus atliekamas galutinis rezervavimas, nebent pasirinktumėte paskirstymo metodą **„Nėra“**.

Kad tai padarytumėte atlikite toliau nurodytus veiksmus.

1. Puslapio **Projektas** skirtuke **Komanda** spustelėkite **Naujas**.
2. Pasirinkite rezervuojamus išteklius, vaidmenį bei pradžios ir pabaigos datas.
3. Pasirinkite paskirstymo metodą, išskyrus **„Nėra”**.
4. Pasirinkite **Įrašyti**. Išteklius matysite tinklelyje, o jų valandas – stulpelyje **„Galutinai rezervuotos valandos”**.
5. Išlaikykite išteklių rezervavimus naudodami funkciją **„Išlaikyti rezervavimus“**.
6. Atsidarius Grafiko lentai, išplėskite išteklius, kad būtų matomi jų rezervavimai. Bus rodoma **„Galutinė”** išteklių būsena.
7. Dešiniuoju pelės mygtuku spustelėti **Keisti būseną** ir pasirinkite **Preliminarios rezervacijos** \> **Preliminari**. Dabar rezervavimo būsena yra **„Preliminari”**.
8. Uždarę Grafiko lentą pamatysite, kad informacija apie išteklių naudojimo valandas buvo perkelta iš stulpelio **„Galutinai rezervuotos valandos“** į stulpelį **„Preliminariai rezervuotos valandos“**, esantį skirtuko tinklelyje **„Komanda“**, kai žiūrėsite į rodinį **„Įvardytieji komandos nariai”**.

> [!NOTE]
> Galutinai rezervavus išteklius komandai ir tada jiems priskyrus užduotis, naudojant funkciją **„Išlaikyti rezervavimus“** būsenos pakeitimui iš **„Galutinė”** į **„Preliminari”**, išlaikomos tiems ištekliams priskirtos užduotys. Tačiau, skirtuke **„Derinimas”** ištekliai turės rezervavimo trūkumą, nes, derinant rezervavimus su užduotimis, paisomi tik galutiniai rezervavimai. Norėdami galutinai rezervuoti ir taip pašalinti galutinių rezervavimų deficitą išteklių priskyrimo atžvilgiu, galite pasinaudoti funkcija **„Išplėsti rezervavimus”**, esančia skirtuke **„Derinimas”**. Turėsite atšaukti preliminarų išteklių rezervavimą, naudodami funkciją **„Išlaikyti rezervavimus”**.

Kai būsite pasiruošę pakeisti preliminariai rezervuotus komandos nario išteklius į galutinai rezervuotą komandos narį, atlikite šiuos veiksmus:

1. Grafiko lentoje išplėskite išteklius, kad būtų matomi jų rezervavimai. Bus rodoma **„Preliminari”** išteklių būsena.
2. Dešiniuoju pelės mygtuku spustelėti **Keisti būseną** ir pasirinkite **Galutinės rezervacijos** \> **Galutinė**. Dabar rezervavimo būsena yra **„Galutinė”**.
3. Uždarę Grafiko lentą, grįžę į projektą ir atidarę skirtuką **„Komanda”**, pamatysite, kad išteklių naudojimo valandos buvo perkeltos iš stulpelio **„Preliminariai rezervuotos valandos”**, į stulpelį **„Galutinai rezervuotos valandos”**, esantį skirtuke **„Komanda”**, kai žiūrėsite į rodinį **„Įvardytieji komandos nariai”**. Jei ištekliams buvo priskirtos užduotys, išteklių skirtuke **„Derinimas“** nebebus matomas rezervavimo deficitas, nes rezervavimai jau yra galutiniai.

