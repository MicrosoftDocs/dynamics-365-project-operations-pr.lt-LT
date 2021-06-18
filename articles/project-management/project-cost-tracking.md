---
title: Projekto savikainos sekimas
description: Šioje temoje pateikiama informacija apie tai, kaip „Project Operations“ eiga sekama pagal projekto savikainą ir išlaidas.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cb76987cf15a14639f34cd3b67c1296a020b2e3e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996531"
---
# <a name="labor-cost-tracking-on-projects"></a>Projektų darbo savikainos sekimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ darbo įvertinimus ir išlaidas projekto plane seka mažiausiu reikalaujamu detalumu. Darbo savikainos finansinis įvertinimas pagrįstas planuojamomis pastangomis ir bendraisiais arba įvardytais ištekliais, priskirtais kiekvienai projekto plano lapo mazgo užduočiai. Projektui prasidėjus ir žmonėms pradėjus pranešti įvairių projekto užduočių laiką, sumuojamos faktinės darbo išlaidos, todėl pradedamos skaičiuoti prognozės.

## <a name="labor-cost-tracking-view"></a>Darbo savikainos sekimo rodinys

Puslapio **Projektai** skirtuke **Sekimas** galite pasirinkti **Sekimas** > **Savikaina**, kad atidarytumėte rodinį **Išlaidų sekimas** ir peržiūrėtumėte kiekvienos projekto plano užduoties darbo išlaidų eigą. Šiame rodinyje taip pat palyginama faktinė užduočiai atlikti išleista darbo savikaina su planuojama užduoties darbo savikaina. „Project Operations“ darbo savikainos metrikoms apskaičiuoti naudojamos toliau nurodytos formulės.

- **Planuojama savikaina**: visų išteklių priskyrimo kiekvienoje lapo mazgo užduotyje įvertintos savikainos reikmės
- **Faktinė savikaina**: visų faktinių savikainos duomenų suma pagal užduotyje užregistruotą laiką
- **Savikainos naudojimo procentinė dalis**: faktinė savikaina ÷ savikainos įvertinimas pabaigoje
- **Savikainos likutis**: savikainos įvertinimas pabaigoje – faktinė savikaina
- **Savikaina pabaigoje**: savikainos likutis + faktinė savikaina
- **Savikainos nuokrypis**: planuojama savikaina – savikainos įvertinimas pabaigoje

Kiekvienoje užduotyje rodoma savikainos nuokrypio užduočiai prognozė. Jei išlaidų įvertinimas pabaigoje yra didesnis už planuojamą savikainą, užduotis projektuojama viršijant biudžetą. Jei išlaidų įvertinimas pabaigoje yra mažesnis už planuojamą savikainą, užduotis projektuojama taip, kad pabaigoje biudžetas nebūtų viršytas.

>[!NOTE]
> „Project Operations“ darbo savikainos rodomos tik puslapio **Projektas** skirtuke **Sekimas**. Nors medžiagas ir išlaidas galima įvertinti ir sekti, kaip jos naudojamos, šios savikainos neįtraukiamos į savikainas, rodomas skirtuke **Sekimas**. Šis skirtukas skirtas naudoti tik darbo savikainoms pakartotinai prognozuoti, kai pakartotinai suprognozuojamos pastangos.
Visos rodomos savikainos sumos konvertuojamos į projekto savikainos valiutą pagal projekto savikainos valiutą, naudojamą savikainos tarifui nustatyti. Projekto savikainos valiuta yra projekto sutarties vieneto valiuta. Įvertintos laiko savikainos reikšmės, rodomos skirtuke **Įvertinimai**, esančiame puslapyje **Projektas**, gali būti nesumuojamos prie savikainos skirtuke **Sekimas**. Šio neatitikimo priežastis – skirtumas, kaip įvertinta savikaina apibendrinama tinklelyje **Įvertinimai**, ir kaip planuojama savikaina apskaičiuojama tinklelyje **Sekimas**. 
>
> - **Skirtuke Įvertinimai** įvertinta savikaina apskaičiuojama taikant tą pačią savikainos tarifo valiutą, kaip ir kainoraštyje. Tada įvertinta savikaina kainoraščio valiuta konvertuojama į įvertintą savikainą projekto savikainos valiuta. Įvertinta savikaina projekto valiuta rodoma suapvalinta iki 2 skaičių po kablelio. Atliekant šį konvertavimą, valiutos tikslumas nėra taikomas. 
> - Skirtuke **Sekimas** planuojamas savikainos apskaičiavimas atliekamas pagal šiek tiek kitokią skaičiavimo tvarką, pagal kurią valiutos tikslumas taikomas dviem toliau nurodytais etapais. 
   ><ol>
   ><li>Įvertinta savikainos suma kainoraščio valiuta konvertuojama į bazinę valiutą (1 konvertavimas).</li>
   ><li>Įvertinta savikainos suma bazine valiuta konvertuojama į projekto savikainos valiutą (2 konvertavimas). </li>
   ></ol>
   >Valiutos tikslumas taikomas atliekant abu veiksmus, kad būtų gauta nustatyti suplanuotą savikainą (skirtuke **Sekimas**), kuri šiek tiek skiriasi nuo įvertintos savikainos (rodinys **Laipsniškai laike**, skirtuke **Įvertinimai**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Pakartotinė savikainos prognozė lapo mazgo užduotims

Lapo mazgo užduoties darbo savikainos negalima tiesiogiai pakartotinai prognozuoti skirtuke **Sekimas**, esančiame **puslapyje Projektas**. Tačiau galite pasinaudoti rodiniu **Pastangų sekimas** ir atlikti pakartotinę užduoties pastangų likučio prognozę. Dėl to perskaičiuojama likusi užduoties savikaina. Toliau pateikiamas aprašas, kuriame paaiškinama, kaip tai atliekama.

1. Projekto vadovas užduotims pakartotinę prognozę gali atlikti atnaujinęs numatytąją reikšmę lauke **Pastangų likutis**, užduotyje įvesdamas naują pastangų likučio įvertinimą. Dėl pakartotinės prognozės atlikimo perskaičiuojamas užduoties pastangos įvertinimas pabaigoje (EAC), eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis. Taip pat perskaičiuojamos suvestinių užduočių EAC, įvertinimas užbaigti (ETC) bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.
2. Remdamasi nauja likusių užduoties pastangų reikšme, sistema likusią savikainą apskaičiuoja rodinyje **Savikainos sekimas**. Kad likusią savikainą galėtų apskaičiuoti pagal likusias pastangas, sistema pirmiausia vienos valandos užduoties pastangų vidutinę savikainą apskaičiuoja kaip planuojamą savikainą arba planuojamas pastangas. Planuojama savikaina yra visų užduoties išteklių priskyrimų savikainos suma. Vidutinės valandos savikainos reikšmė naudojama norint apskaičiuoti naujai išprognozuotų užduoties pastangų likutį pagal savikainos likutį.
3. Perskaičiuojama savikaina lapo mazgo užduoties savikainos pabaigoje ir savikainos panaudojimo procentas.
4. Atliekamas suvestinių užduočių savikainos žinant pabaigos reikšmę perskaičiavimas iki pat šaknies mazgo.

## <a name="reprojecting-costs-on-summary-tasks"></a>Savikainų pakartotinė prognozė suvestinėms užduotims

Galite atlikti pakartotinę suvestinės arba talpyklės užduočių darbo savikainų prognozę. Tačiau tiesiogiai atlikti pakartotinės darbo savikainos prognozės suvestinės užduoties skirtuke **Sekimas**, esančiame puslapyje **Projektas**, negalite. Panašiai kaip ir lapo mazgo užduočių atveju, galima pakartotinai prognozuoti suvestinės ir talpyklės užduotis naudojant rodinį **Pastangų sekimas**. Šiame rodinyje galite atlikti pakartotinę suvestinės užduoties pastangų prognozę, dėl kurios reikės perskaičiuoti likusią suvestinės užduoties savikainą. Toliau pateikiamas aprašas, kuriame paaiškinama, kaip tai atliekama.

1. Projekto vadovas suvestinėms užduotims pakartotinę prognozę gali atlikti atnaujinęs pastangų likučio numatytąją reikšmę, įvesdamas naują užduoties įvertinimą. Dėl šio naujinimo perskaičiuojamas suvestinės užduoties įvertinimas pabaigoje (EAC), eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis. Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.
2. Remdamasi nauja likusių suvestinės užduoties pastangų reikšme, sistema likusią savikainą apskaičiuoja rodinyje **Savikainos sekimas**. Kad likusią savikainą galėtų apskaičiuoti pagal likusias pastangas, sistema pirmiausia vienos valandos suvestinės užduoties pastangų vidutinę savikainą apskaičiuoja kaip planuojamą savikainą arba planuojamas pastangas. Vidutinės valandos savikainos reikšmė naudojama norint apskaičiuoti naujai išprognozuotų savikainos užduoties pastangų likučio savikainą.
3. Perskaičiuojama savikaina suvestinės užduoties savikainos pabaigoje ir savikainos panaudojimo procentas.
4. Nauja savikaina pabaigoje antrinėms užduotims paskirstoma tokiomis pat dalimis, kaip ir pradinės užduoties suplanuota savikaina.
5. Apskaičiuojama nauja kiekvienos individualios užduoties savikainos reikšmė pabaigoje iki pat lapo mazgo užduočių. Remiantis šia reikšme, paveiktų antrinių užduočių iki pat iki lapo mazgų savikainos likutis ir savikainos naudojimo procentinė dalis bus perskaičiuota remiantis pajamų kiekiu esant užbaigimo reikšmei. Šį reikšmė tampa nauja savikainos užduočiai nuokrypio prognoze. 


Lauką **Savikainos efektyvumas** galima nustatyti pagal sekimo duomenis. Kai rodinio **Savikainos sekimas** šakninio mazgo savikainos nuokrypis yra neigiamas, šį lauką galite nustatyti kaip **Nesiekia biudžeto**. Kai šakninio mazgo išlaidų nuokrypis yra teigiamas, reikšmę galite nustatyti kaip **Viršija biudžetą**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
