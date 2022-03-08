---
title: Įmonės vidaus išlaidos
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti vidinės įmonės išlaidas darbuotojo išlaidoms priskirti juridiniam subjektui, kuriam buvo atliktas darbas.
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001216"
---
# <a name="intercompany-expenses"></a>Vidinės įmonės išlaidos

Darbuotojas, įdarbintas vieno organizacijos juridinio subjekto, gali atlikti darbą, skirtą kitam tos pačios organizacijos juridiniam subjektui. Galite naudoti vidinės įmonės išlaidas darbuotojo išlaidoms priskirti juridiniam subjektui, kuriam buvo atliktas darbas. Juridinis subjektas, įdarbinantis darbuotoją, vadinamas skolinančiu juridiniu subjektu. Juridinis subjektas, kuris už darbuotojo atliktą darbą patiria išlaidų, vadinamas pasiskolinančiu juridiniu subjektu. 

Kad darbuotojas galėtų kurti ir pateikti vidinės įmonės išlaidas, turite įjungti vidinės įmonės išlaidų eilutes. Skolinančiajame juridiniame subjekte, puslapyje **Išlaidų valdymo parametrai**, pasirinkite **Leisti vidinės įmonės išlaidų eilutes**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Vidinės įmonės išlaidų mokesčių registravimas

[!include [banner](../includes/banner.md)]

Kad savo išlaidų ataskaitoje galėtumėte naudoti mokesčių grupes, susietas su skolinančiuoju (šaltinio) juridiniu subjektu, o ne su besiskolinančiu (paskirties) juridiniu subjektu, turite įjungti šią funkciją didžiosios knygos PVM sąrankoje. Kai parametras **Juridinis subjektas mokesčių registracijai tarp įmonių** nustatytas į **Šaltinio**, o **Taikyti PVM apmokestinimo taisykles** nustatytas į **Ne**, naudojamas skolinančiojo juridinio subjekto mokesčių derinys. Kai tas pats parametras nustatytas į parinktį **Paskirtis**, bus naudojamas pasiskolinančio juridinio subjekto mokesčių derinys. Jei juridiniai subjektai Jungtinėse Valstijose, kai parametras nustatytas į parinktį **Šaltinis**, laukas **Gaunamas PVM** turi būti sukonfigūruotas laukas naujame puslapyje **DK registravimo grupės**. Apskaitos modulis naudos šiame lauke esančią informaciją su mokesčiais susijusiam apskaitos įrašui.   
Veikimas atitinka išlaidų eilutes, užregistruotas su projektu ar be jo.  

## <a name="new-expense-expression-builder"></a>Nauja išlaidų reiškinio daryklė

Naudojant naują išlaidų reiškinio daryklę sprendžiamos problemos, susijusios su vidinės įmonės išlaidų scenarijais, kuriuose naudojami projektai. Šia funkcija užtikrinama, kad sukūrus vidinės įmonės išlaidas, išlaidų strategija būtų tinkamai patikrinama pagal projektą, pasirinktą išlaidų eilutėje, ir kad išlaidų ataskaita galėtų būti sėkmingai pateikta.

Norint, kad išlaidų reiškinio daryklės funkcija veiktų, ją reikia įjungti. Be to, turi būti nustatyta išlaidų strategija, kurioje nurodytas projekto ID.

Jei jau sukonfigūravote strategijas, kuriomis patvirtinamas išlaidų eilutėje esantis ID, šias strategijas reikia nurašyti. Tada galite įjungti funkciją ir iš naujo sukonfigūruoti strategijas.

Norėdami įjungti šią funkciją, atlikite toliau nurodytus veiksmus.

1. Eikite į **Darbo sritys**\>**Funkcijų tvarkymas**.
2. Sąraše pasirinkite **Nauja išlaidų reiškinio daryklė, kurią naudojant sprendžiamos problemos, susijusios su vidinės įmonės išlaidų scenarijais, kuriuose naudojami projektai**. Tada pasirinkite **Įjungti dabar**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
