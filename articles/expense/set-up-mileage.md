---
title: Kilometražo nustatymas naudojant kilometražo tarifo pakopas
description: Šiame straipsnyje pateikiama informacija apie ridos tarifus ir ridos greičio pakopas.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 03ca18c8fef6228f2ba553ebe50447beda5a857c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930144"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Kilometražo nustatymas naudojant kilometražo tarifo pakopas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Kai pranešama apie išlaidas, o pažymėta išlaidų kategorija yra **Kilometražas**, tos išlaidų eilutės suma apskaičiuojama pagal sumą *kilometražo tarifas*. Ši suma nustatoma naudojant apibrėžtas kilometražo pakopas arba, jei nėra nustatytų pakopų, pagal standartinį kilometražo tarifą. 

Kilometražo tarifo pakopas galima nustatyti įėjus į **Išlaidų valdymas** > **Sąranka** > **Bendra** > **Išlaidų kategorijos** > **Kilometražas** > **Kategorijų sąranka**.

Jei jūsų organizacija naudoja kilometražo išlaidų kategoriją, atnaujinę į 10.0.18, galite įjungti kilometražo funkciją peržiūrėję toliau nurodytus dizaino pakeitimus. 

Naujasis kilometražo tarifo pakopų dizainas lemia, kaip apdorojama lauko **Kiekis** reikšmė. Prieš išleidžiant 10.0.18, lauko **Kiekis** reikšmė buvo laikoma mažesne riba. Viršijus šią reikšmę, buvo naudojamas atitinkamas tarifas.  10.0.18 versijoje lauko **Kiekis** reikšmė laikoma didesne riba. Atitinkamas tarifas naudojamas, kai kilometražo suma yra mažesnė nei lauko **Kiekis** reikšmė.  Naujasis kilometražo pakopų modelis padeda nuosekliai taikyti pakopas ir geriau jas panaudoti.   

Visos patvirtintos išlaidų ataskaitos registravimo metu bus perskaičiuojamos pagal naują dizainą.

## <a name="example"></a>Pavyzdžiui
 
### <a name="before-version-10018"></a>Prieš 10.0.18 versiją
Naudojant dvi kilometražo tarifų pakopas, kiekvienos jų laukas **Kiekis** reiškia žemesnę kilometražo ribą. Šiuo metu vienos pakopos reikšmė yra nulinė (0), o tarifas 0,45 – o antrojo pakopos vertė – 1 000, o tarifas 0,25. Jei mylių ar kilometrų suma viršija lauko reikšmę, naudojamas susijęs tarifas. Jei nėra eilutės, kurios kiekis nulinis, sistema naudoja kilometražo tarifą, apibrėžtą išlaidų valdymo dalyje. 
 
Jei darbuotojas pateikia išlaidų ataskaitą su 1 500 myliomis, dvi kilometražo eilutės užregistruotoje išlaidų ataskaitoje bus: 1000 (tarifas 0,45) + 500 (tarifas 0,25) = 575,00.

### <a name="after-version-10018"></a>Po 10.0.18 versijos
10.0.18 versijoje kiekvienos pakopos laukas **Kiekis** atitinka viršutinę pakopos ribą. Šiuo metu vienos pakopos reikšmė yra 999, o tarifas 0,45 – o antrojo pakopos vertė – 999 999 999,00, o tarifas 0,25. Jei mylių ar kilometrų suma viršija lauko **Kiekis** reikšmę, naudojamas susijęs tarifas. Jei viršijamos visos viršutinės ribos, sistema naudoja kilometražo tarifą, apibrėžtą išlaidų valdymo dalyje. 
 
Norint tinkamai apskaičiuoti tą patį scenarijų, reikia pakeisti nustatytą pakopą. Pirmos pakopos lauko **Kiekis** reikšmė yra 999,00, o antros pakopos – 999 999 999,00. Jei darbuotojas viršija bendrą imylių ar kilometrų kiekį pirmoje pakopoje, sistema naudoja kilometražo tarifą, apibrėžtą išlaidų valdymo dalyje. 
  
Jei darbuotojas pateikia išlaidų ataskaitą su 1 500 myliomis, dvi kilometražo eilutės užregistruotoje išlaidų ataskaitoje bus: 1000 (tarifas 0,45) + 500 (tarifas 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Įjunkite kelių kilometražo pakopų, kurių tarifo funkcija yra ta pati, kilometražo sumos skaičiavimą

Funkcija **Kelių kilometražo pakopų, kurių tarifo funkcija yra ta pati** pagerina kilometražo tarifo skaičiavimą. Norėdami įjungti šią funkciją, atlikite šiuos veiksmus.

1. Eikite į **Darbo sritys** > **Funkcijų tvarkymas**. 
2. Sąraše raskite ir pasirinkite **Kelių kilometražo pakopų, kurių tarifo funkcija yra ta pati**, tada pasirinkite **Įjungti dabar**.

Įjungę funkciją, iš naujo nustatykite kilometražo pakopas, kad jos tinkamai atspindėtų lauko **Kiekis** reikšmę. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
