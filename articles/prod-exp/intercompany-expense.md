---
title: Įmonės vidaus išlaidos
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti vidinės įmonės išlaidas darbuotojo išlaidoms priskirti juridiniam subjektui, kuriam buvo atliktas darbas.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960842"
---
# <a name="intercompany-expenses"></a>Vidinės įmonės išlaidos

Darbuotojas, įdarbintas vieno organizacijos juridinio subjekto, gali atlikti darbą, skirtą kitam tos pačios organizacijos juridiniam subjektui. Galite naudoti vidinės įmonės išlaidas darbuotojo išlaidoms priskirti juridiniam subjektui, kuriam buvo atliktas darbas. Juridinis subjektas, įdarbinantis darbuotoją, vadinamas skolinančiu juridiniu subjektu. Juridinis subjektas, kuris už darbuotojo atliktą darbą patiria išlaidų, vadinamas pasiskolinančiu juridiniu subjektu. 

Kad darbuotojas galėtų kurti ir pateikti vidinės įmonės išlaidas, turite įjungti vidinės įmonės išlaidų eilutes. Skolinančiajame juridiniame subjekte, puslapyje **Išlaidų valdymo parametrai**, pasirinkite **Leisti vidinės įmonės išlaidų eilutes**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Vidinės įmonės išlaidų mokesčių registravimas

[!include [banner](../includes/banner.md)]

Kad savo išlaidų ataskaitoje galėtumėte naudoti mokesčių grupes, susietas su skolinančiuoju (šaltinio) juridiniu subjektu, o ne su besiskolinančiu (paskirties) juridiniu subjektu, turite įjungti šią funkciją didžiosios knygos PVM sąrankoje. Kai parametras **Juridinis subjektas mokesčių registracijai tarp įmonių** nustatytas į **Šaltinio**, o **Taikyti PVM apmokestinimo taisykles** nustatytas į **Ne**, naudojamas skolinančiojo juridinio subjekto mokesčių derinys. Kai tas pats parametras nustatytas į parinktį **Paskirtis**, bus naudojamas pasiskolinančio juridinio subjekto mokesčių derinys. Jei juridiniai subjektai Jungtinėse Valstijose, kai parametras nustatytas į parinktį **Šaltinis**, laukas **Gaunamas PVM** turi būti sukonfigūruotas laukas naujame puslapyje **DK registravimo grupės**. Apskaitos modulis naudos šiame lauke esančią informaciją su mokesčiais susijusiam apskaitos įrašui.   
Veikimas atitinka išlaidų eilutes, užregistruotas su projektu ar be jo.  
