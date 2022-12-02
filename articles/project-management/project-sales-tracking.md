---
title: Projekto pardavimo sekimas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip „Project Operations“ eiga sekama pagal projekto darbo pajamas.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce61acf95ee5e9ac10047406c9d4a5c9b1f92aad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911284"
---
# <a name="project-sales-tracking"></a>Projekto pardavimo sekimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ darbo įvertinimus ir pajamas projekto plane seka mažiausiu reikalaujamu detalumu. Darbo pajamų įvertinimas pagrįstas planuojamomis pastangomis ir bendraisiais arba įvardytais ištekliais, priskirtais kiekvienai projekto plano lapo mazgo užduočiai. Projektui prasidėjus ir žmonėms pradėjus pranešti įvairių projekto užduočių laiką, sumuojamos faktinės darbo pajamos, todėl pradedamos skaičiuoti prognozės.

## <a name="labor-revenue-tracking-view"></a>Projektų darbo pajamų sekimo rodinys

Puslapio **Projektai** skirtuke **Sekimas** galite pasirinkti **Sekimas** > **Savikaina** ir atidaryti rodinį **Savikainos sekimas**. Arba galite pasirinkti **Naudoti** > **Sąskaitos tarifas**, kad atidarytumėte rodinį **Pajamų sekimas**, kuriame pateikiama kiekvienos projekto plano užduoties darbo pajamų eiga. Šiame rodinyje taip pat palyginamos faktinės užduočiai atlikti išleistos darbo pajamos su planuojamomis užduoties darbo pajamomis. „Project Operations“ darbo pajamų metrikoms apskaičiuoti naudojamos toliau nurodytos formulės.

- **Planuojamos pajamos**: visų išteklių priskyrimo kiekvienoje lapo mazgo užduotyje įvertintos pardavimo reikšmės
- **Faktinės pajamos**: viso faktinio pardavimo, už kurį neišrašyta sąskaita faktūra, suma pagal užduotyje užregistruotą laiką
- **Mokėtinos pajamos %**: faktinės pajamos ÷ pajamų įvertinimo pabaigoje
- **Likusios pajamos**: pajamų įvertinimas pabaigoje – faktinės pajamos
- **Įvertintos pajamos pabaigoje**: likusios pajamos + faktinės pajamos
- **Pajamų nuokrypis**: planuojamos pajamos – įvertintos pajamos pabaigoje


> [!NOTE]
> „Project Operations“ darbo pajamos rodomos tik puslapio **Projektas** skirtuke **Sekimas**. Nors medžiagas ir išlaidas galima įvertinti ir sekti, kaip jos naudojamos, šios pajamos neįtraukiamos į pajamas, rodomas skirtuke **Sekimas**. Šis skirtukas skirtas naudoti tik darbo pajamoms pakartotinai prognozuoti, kai pakartotinai suprognozuojamos pastangos.  
> Visos rodomos pajamų sumos konvertuojamos į projekto savikainos valiutą. Projekto savikainos valiuta yra projekto sutarties vieneto valiuta. Fiksuotos kainos projektų atveju, pajamų rodikliai rodinyje **Darbo pajamų sekimas** nėra tinkami, nes faktiniai pardavimo, už kurį neišrašyta sąskaita, duomenys neįrašomi laiko patvirtinimo dalyje.
> Įvertintos pardavimo pagal laiką reikšmės, rodomos projekto skirtuke **Įvertinimas**, gali būti nesumuojamos su planuojamų pajamų reikšme skirtuke **Sekimas**. Šio neatitikimo šaltinis atsiranda dėl dviejų toliau nurodytų priežasčių.
><ol>
   ><li> Skirtuke <b>Įvertinimai</b> įvertintos pajamos rodomos pardavimo valiuta, o skirtuke <b>Sekimas</b> planuojamos pajamos rodomos konvertuotos į savikainos valiutą. </li>
   ><li> Kai įvertintas pardavimas konvertuojamas į sutarties valiutą, kaip parodyta skirtuke <b>Įvertinimai</b>, arba į projekto valiutą, konvertavimas apima veiksmus, dėl kurių gali nukentėti tikslumas. </li>
><ol>
><li> Įvertinta pardavimo suma sutarties valiuta pirmiausia konvertuojama į bazinę valiutą (1 konvertavimas).</li>
><li> Įvertinta pardavimo suma bazine valiuta konvertuojama į projekto savikainos valiutą (2 konvertavimas). </li>
></ol>
></ol>
> Valiutos tikslumas taikomas atliekant abu veiksmus, todėl planuojamos projekto valiuta pajamos nukrypsta nuo planuojamo pardavimo sutarties valiuta.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Pajamų pakartotinė prognozė lapo mazgo užduotims

Lapo mazgo užduoties darbo pajamų negalima tiesiogiai pakartotinai prognozuoti skirtuke **Sekimas**, esančiame puslapyje **Projektas**. Tačiau galite pasinaudoti rodiniu **Pastangų sekimas** ir atlikti pakartotinę užduoties pastangų likučio prognozę. Dėl to perskaičiuojamos likusios užduoties pajamos. Toliau pateikiamas aprašas, kuriame paaiškinama, kaip tai atliekama.

1. Projekto vadovas užduotims pakartotinę prognozę gali atlikti atnaujinęs numatytąją reikšmę lauke **Pastangų likutis**, užduotyje įvesdamas naują pastangų likučio įvertinimą. Dėl pakartotinės prognozės atlikimo perskaičiuojamas užduoties pastangos įvertinimas pabaigoje (EAC), eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis. Taip pat perskaičiuojamos suvestinių užduočių EAC, įvertinimas užbaigti (ETC) bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.
2. Remdamasi nauja likusių užduoties pastangų reikšme, sistema likusias pajamas apskaičiuoja rodinyje **Pajamų sekimas**. Kad likusias pajamas galėtų apskaičiuoti pagal likusias pastangas, sistema pirmiausia vienos valandos pastangų vidutines pajamas apskaičiuoja kaip planuojamas pajamas arba planuojamas pastangas. Planuojamos pajamos yra visų užduoties išteklių priskyrimų pajamų suma. Vidutinių valandos pajamų reikšmė naudojama norint apskaičiuoti naujai išprognozuotų užduoties pastangų likutį pagal pajamų likutį.
3. Perskaičiuojamos lapo mazgo užduoties įvertintos pajamos pabaigoje ir pajamų panaudojimo procentas.
4. Atliekamas suvestinių užduočių pajamų žinant pabaigos reikšmę perskaičiavimas iki pat šaknies mazgo.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Pajamų pakartotinė prognozė suvestinėms užduotims

Galite atlikti pakartotinę suvestinės arba talpyklės užduočių darbo pajamų prognozę. Tačiau tiesiogiai atlikti pakartotinės darbo pajamų prognozės suvestinės užduoties skirtuke **Sekimas**, esančiame puslapyje **Projektas**, negalite. Panašiai kaip ir lapo mazgo užduočių atveju, galima pakartotinai prognozuoti suvestinės ir talpyklės užduotis naudojant rodinį **Pastangų sekimas**. Šiame rodinyje galite atlikti pakartotinę suvestinės užduoties pastangų prognozę, dėl kurios reikės perskaičiuoti likusias suvestinės užduoties pajamas. Toliau pateikiamas aprašas, kuriame paaiškinama, kaip tai atliekama.

1. Projekto vadovas užduotims pakartotinę prognozę gali atlikti atnaujinęs numatytąją reikšmę lauke **Pastangų likutis**, užduotyje įvesdamas naują **Pastangų likutis** įvertinimą. Dėl pakartotinės prognozės atlikimo perskaičiuojamas užduoties įvertinimas pabaigoje (EAC), eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis. Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.
2. Remdamasi nauja užduoties lauko **Pastangų likutis** reikšme, sistema likusias pajamas apskaičiuoja rodinyje **Pajamų sekimas**. Kad likusias pajamas galėtų apskaičiuoti pagal likusias pastangas, sistema pirmiausia vienos valandos pastangų vidutines pajamas apskaičiuoja kaip planuojamas pajamas arba planuojamas pastangas. Planuojamos pajamos yra visų užduoties išteklių priskyrimų pajamų suma. Tada vidutinių valandos pajamų reikšmė naudojama norint apskaičiuoti pajamas pagal naujai išprognozuotų užduoties pastangų likutį.
3. Perskaičiuojamos suvestinės užduoties įvertintos pajamos pabaigoje ir pajamų panaudojimo procentinės dalys.
4. Nauja įvertintų pajamų reikšmė pabaigoje antrinėms užduotims paskirstoma tokiomis pat dalimis, kaip ir pradinės užduoties suplanuotos pajamos.
5. Apskaičiuojamos naujos kiekvienos individualios užduoties įvertintos pajamos pabaigoje iki pat lapo mazgo užduočių. Remiantis šia reikšme, paveiktų antrinių užduočių iki pat iki lapo mazgų pajamų likutis ir pajamų naudojimo procentinė dalis bus perskaičiuota remiantis pajamų kiekiu esant užbaigimo reikšmei. Taip sukuriama nauja pajamų užduočiai nuokrypio prognozė. 
6. Atliekamas suvestinių užduočių pajamų žinant pabaigos reikšmę perskaičiavimas iki pat šaknies mazgo.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

