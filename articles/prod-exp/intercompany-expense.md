---
title: Vidinės įmonės išlaidos
description: Darbuotojas, įdarbintas vieno organizacijos juridinio subjekto, gali atlikti darbą, skirtą kitam tos pačios organizacijos juridiniam subjektui. Esant tokiai situacijai, galite naudoti vidinės įmonės išlaidų funkciją, kad priskirtumėte darbuotojo išlaidas juridiniam subjektui, kuriam buvo skirtas atliktas darbas.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080987"
---
# <a name="intercompany-expenses"></a>Vidinės įmonės išlaidos

[!include [banner](../includes/banner.md)]

Darbuotojas, įdarbintas vieno organizacijos juridinio subjekto, gali atlikti darbą, skirtą kitam tos pačios organizacijos juridiniam subjektui. Esant tokiai situacijai, galite naudoti vidinės įmonės išlaidų funkciją, kad priskirtumėte darbuotojo išlaidas juridiniam subjektui, kuriam buvo skirtas atliktas darbas. Juridinis subjektas, įdarbinantis darbuotoją, vadinamas skolinančiu juridiniu subjektu. Juridinis subjektas, kuris už darbuotojo atliktą darbą patiria išlaidų, vadinamas pasiskolinančiu juridiniu subjektu. 

Kad darbuotojas galėtų kurti ir pateikti kitame juridiniame subjekte atlikto darbo išlaidas, skolinančio juridinio subjekto puslapyje **Išlaidų valdymo parametrai** pasirinkite parinktį **Leisti vidinės įmonės išlaidų eilutes**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Vidinės įmonės išlaidų mokesčių registravimas

[!include [banner](../includes/banner.md)]

Jei savo išlaidų ataskaitoje norite naudoti mokesčių grupes, susietas su skolinančiu (šaltinio) juridiniu subjektu, o ne pasiskolinančiu (paskirties) juridiniu subjektu, turėsite tai sukonfigūruoti DK PVM rinkinyje. Kai DK parametras **Vidinės įmonės mokesčių registravimo juridinis subjektas** nustatomas į parinktį **Šaltinis** , o parametras **Taikyti PVM apmokestinimo taisykles** nustatytas į parinktį **Ne** , bus naudojamas skolinančio juridinio subjekto mokesčių derinys. Kai tas pats parametras nustatytas į parinktį **Paskirtis** , bus naudojamas pasiskolinančio juridinio subjekto mokesčių derinys. Jei juridiniai subjektai Jungtinėse Valstijose, kai parametras nustatytas į parinktį **Šaltinis** , laukas **Gaunamas PVM** turi būti sukonfigūruotas laukas naujame puslapyje **DK registravimo grupės**. Apskaitos sistema naudos šiame lauke esančią informaciją rašydama su mokesčiais susijusį apskaitos įrašą.   
Veikimas atitinka išlaidų eilutes, užregistruotas su projektu ar be jo.  
