---
title: Darbo paskirstymo struktūros šablonų vaidmenų nustatymas
description: Šioje temoje pateikta informacija apie vaidmens informacijos nustatymą darbo paskirstymo struktūros šablonuose.
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
ms.openlocfilehash: 35ab88d61c9b1e9d9aebeb776d6a7783b96c62f6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682858"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Darbo paskirstymo struktūros šablonų vaidmenų nustatymas

[!include [banner](../includes/banner.md)]

Projektų vadovai gali nustatyti darbo paskirstymo struktūros (WBS) šablonus, kuriuos gali taikyti kurdami naujų projektų WBS. Kurdami šabloną projektų vadovai gali įtraukti vaidmenis. Naudokite toliau pateikiamą procedūrą, kad priskirtumėte vaidmeniui WBS šabloną.

1. Pasirinkite **Projektų valdymas ir apskaita** > **Sąranka** > **Projektai** > **Darbo paskirstymo struktūros šablonai**.
2. Pasirinkite **Išsami informacija** pasirinktam WBS šablonui.
3. Sąraše pažymėkite užduotį, tada lauke **Vaidmuo** pasirinkite vaidmenį, kurį priskirsite užduočiai.

## <a name="work-with-a-wbs"></a>Darbas su WBS

Galite kurti naują WBS arba kopijuoti WBS iš esamo WBS šablono. Projekto vadovas gali lengvai tvarkyti išteklius, priskirdamas vaidmenis naujoms užduotims WBS. Vaidmenis galima keisti arba gavus išteklių, arba nustačius patvirtintą išteklių, kuris atliks užduotį. Šis lankstumas leidžia projektų vadovams atlikti toliau nurodytas užduotis užduotis.

- Nustatykite išteklių, reikalingų WBS darbo paketams, skaičių.
- Įvertinti projekto išlaidas.
- Nustatyti preliminarų biudžetą.
- Pagal vaidmenis ir išteklius įvertinti veiklos trukmę.
- Kurti projektų valdymo planus remiantis turima projekto informacija.

Į WBS buvo įtrauktos papildomos parinktys, skirtos geriau išnaudoti išteklių paskirstymo funkcijas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parinktis</th>
<th>Aprašo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Išteklių priskyrimai</td>
<td>Priskirtų išteklių, datų, valandų skaičiaus ir rezervavimo tipo, skirtų WBS užduotims, peržiūra.</td>
</tr>
<tr class="even">
<td>Automatinis komandos generavimas</td>
<td>Automatinis suplanuotų išteklių įtraukimas, naudojant su užduotimi susietus vaidmenis. Programa „Finance” automatiškai pasiūlo suplanuotus išteklius, naudodama vaidmenimis grindžiamą kelių kriterijų sprendimų analizę. Kai bus nustatyti WBS esančių užduočių vaidmenys ir pastangos (valandos) ir išleista struktūra, pasirinkite <strong>Automatinis komandos generavimas</strong>. Reikiamas suplanuotų išteklių skaičius įtraukiamas į WBS ir skirtuką <strong>Projekto ir komandos planavimas</strong>.</td>
</tr>
<tr class="odd">
<td>Ištekliai (išplečiamasis sąrašas)</td>
<td>Puslapyje <strong>Išteklių priskyrimo paleidimas</strong> galite pasirinkti išteklius ir, remdamiesi nustatyta trukme, priskirti juos prie galutinai rezervuojamų ir preliminariai rezervuojamų. Galite koreguoti rodinio parametrus, kad peržiūrėtumėte ir nustatytumėte išteklių veiklos trukmę. Naudodami toliau pateikiamas parinktis galite pasirinkti ir priskirti išteklius darbo paketo lygyje.
<ul>
<li><strong>Priimti</strong> – patvirtinti užduočiai priskirto ištekliaus pakeitimus.</li>
<li><strong>Atšaukti</strong> – atšaukti užduočiai priskirto ištekliaus pakeitimus.</li>
<li><strong>Priskirti automatiškai</strong> – pasiekiamas darbuotojams priskirtas išteklius, turintis atitinkantį vaidmenį, automatiškai pasirenkamas ir priskiriamas pasirinktai užduočiai.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Puslapyje **Visi projektai** pasirinkite projektą **XYZ Upgrade Phase 2**.
2. Pasirinkite **Planas** > **Veiklos rūšys** > **Darbo paskirstymo struktūra**.
3. Pasirinkite **Naujas**, kad įtrauktumėte toliau nurodytas veiklas į WBS.

    - Inicijavimas
    - Planavimas
    - Vykdoma
    - Stebėjimas ir valdymas
    - Uždaryti objektą

4. Nustatykite datas ir pastangas (valandas), kaip pavaizduota tolesnėje iliustracijoje.

    [![Datų ir pastangų nustatymas.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Pasirinkite užduoties eilutę **Inicijavimas**, tada lauke **Vaidmuo** pasirinkite **Vyresnysis projekto vadovas**.
6. Pasirinkite **Publikuoti**.
7. Toje pačioje eilutėje, lauke **Ištekliai** pasirinkite **Danielis Goldschmidtas**, tada pasirinkite **Priimti**.
8. Pasirinkite užduoties eilutę **Planavimas**, tada lauke **Vaidmuo** pasirinkite **Verslo analitikas**.
9. Pasirinkite **Publikuoti**, tada pasirinkite **Automatiškai generuoti komandą**.
10. Pasirodžiusiame pranešimo langelyje pasirinkite **Taip**.
11. Lauke **Ištekliai** patikrinkite, ar reikšmė yra **1-as verslo analitikas**.
12. Atidarykite ištekliaus **1-as verslo analitikas** peržvalgą ir pasirinkite **Išteklių priskyrimo paleidimas**. Tada pasirinkite užduočiai priskiriamą darbuotoją.
13. Pasirinkite **Preliminariai priskirti** &gt; **Viso pajėgumo metodas**.

    > [!NOTE] 
    > Negaunate įspėjimo, kad nurodytas išteklius dabar yra 2-as, nes išteklių skaičius lieka 1.

14. Puslapyje **Darbo paskirstymo struktūra** patikrinkite ištekliaus priskyrimą WBS, tada pasirinkite **Įrašyti**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]