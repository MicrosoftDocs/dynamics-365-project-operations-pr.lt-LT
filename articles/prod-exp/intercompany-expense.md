---
title: Įmonės vidaus išlaidos
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti vidinės įmonės išlaidas darbuotojo išlaidoms priskirti juridiniam subjektui, kuriam buvo atliktas darbas.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005081"
---
# <a name="intercompany-expenses"></a>Vidinės įmonės išlaidos

Darbuotojas, įdarbintas vieno organizacijos juridinio subjekto, gali atlikti darbą, skirtą kitam tos pačios organizacijos juridiniam subjektui. Galite naudoti vidinės įmonės išlaidas darbuotojo išlaidoms priskirti juridiniam subjektui, kuriam buvo atliktas darbas. Juridinis subjektas, įdarbinantis darbuotoją, vadinamas skolinančiu juridiniu subjektu. Juridinis subjektas, kuris už darbuotojo atliktą darbą patiria išlaidų, vadinamas pasiskolinančiu juridiniu subjektu. 

Kad darbuotojas galėtų kurti ir pateikti vidinės įmonės išlaidas, turite įjungti vidinės įmonės išlaidų eilutes. Skolinančiajame juridiniame subjekte, puslapyje **Išlaidų valdymo parametrai**, pasirinkite **Leisti vidinės įmonės išlaidų eilutes**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Vidinės įmonės išlaidų mokesčių registravimas

[!include [banner](../includes/banner.md)]

Kad savo išlaidų ataskaitoje galėtumėte naudoti mokesčių grupes, susietas su skolinančiuoju (šaltinio) juridiniu subjektu, o ne su besiskolinančiu (paskirties) juridiniu subjektu, turite įjungti šią funkciją didžiosios knygos PVM sąrankoje. Kai parametras **Juridinis subjektas mokesčių registracijai tarp įmonių** nustatytas į **Šaltinio**, o **Taikyti PVM apmokestinimo taisykles** nustatytas į **Ne**, naudojamas skolinančiojo juridinio subjekto mokesčių derinys. Kai tas pats parametras nustatytas į parinktį **Paskirtis**, bus naudojamas pasiskolinančio juridinio subjekto mokesčių derinys. Jei juridiniai subjektai Jungtinėse Valstijose, kai parametras nustatytas į parinktį **Šaltinis**, laukas **Gaunamas PVM** turi būti sukonfigūruotas laukas naujame puslapyje **DK registravimo grupės**. Apskaitos modulis naudos šiame lauke esančią informaciją su mokesčiais susijusiam apskaitos įrašui.   
Veikimas atitinka išlaidų eilutes, užregistruotas su projektu ar be jo.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]