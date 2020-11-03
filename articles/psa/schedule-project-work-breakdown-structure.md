---
title: Projekto planavimas su darbo paskirstymo struktūra
description: Projekto planavimas su darbo paskirstymo struktūra „Project Service“
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081018"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Projekto planavimas su darbo paskirstymo struktūra („Project Service“)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Projekto grafikas nurodo, kokius darbus reikės atlikti, kurie ištekliai darbą atliks ir laiko ribas, per kurias darbą reikės atlikti. Projekto grafikas atspindi visą darbą, susijusį su projekto atlikimu laiku. Vienas iš pirmųjų projekto inicijavimo etapo veiksmų yra projekto grafiko sudarymas. Norint sudaryti projekto grafiką, reikia sukurti darbo paskirstymo struktūrą.  
  
 Sukurkite projekto struktūrą su darbo paskirstymo struktūra, kuri jums padės:  
  
- suskirstyti darbą į įvykdomas užduotis;  
  
- įvertinti, kiek laiko reikės užduočiai atlikti;  
  
- nustatyti užduočių priklausomybes ir užduočių trukmę;  
  
- apibrėžti kiekvienai užduočiai atlikti reikalingus vaidmenis.  
  
  Projekto grafikas darbo paskirstymo struktūroje yra panašus į projekto grafiką interaktyviojoje Ganto diagramoje.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Projekto darbo paskirstymo struktūros kūrimas  
 Sukurkite darbo paskirstymo struktūrą, vaizduojančią projekto užduočių seką. Darbo paskirstymo struktūra apima užduotis, kiekvienos užduoties reikalavimus ir įplaukų bei savikainos informaciją. Į darbo paskirstymo struktūrą galite įtraukti:  
  
-   užduočių seką pagal hierarchiją;  
  
-   kitas užduotis, jei jų yra, kurias būtina atlikti, kad būtų galima pradėti vykdyti užduotį;  
  
-   užduoties pradžios datą, pabaigos datą ir trukmę;  
  
-   užduočiai atlikti reikalingų valandų skaičių;  
  
-   visus reikalingus darbuotojų įgūdžius ir išsilavinimą;  
  
-   užduočiai priskirtus darbuotojus;  
  
-   prognozuojamas įplaukas ir savikainą.  
  
## <a name="task-types"></a>Užduočių tipai  
Kuriant darbo paskirstymo struktūrą, naudojamos šių tipų užduotys:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Projekto šakninis mazgas** | Tai projekto aukščiausio lygio suvestinė užduotis. Joje yra kuriamos visos kitos projekto užduotys. Šakninei užduočiai suteikiamas projekto pavadinimas. Šakninio mazgo pastangos, datos ir trukmė yra pagrįstos žemiau jos esančios hierarchijos reikšmėmis. Negalite nei redaguoti šakninio mazgo ypatybių, nei panaikinti paties šakninio mazgo. | 
| **Suvestinės arba konteinerio užduotys** | Suvestinė užduotis yra užduotis, turinti papildomų užduočių. Pati suvestinė užduotis neturi jokių darbo pastangų nei savikainos. Jos darbo pastangos ir savikaina yra jos papildomų užduočių apibendrinamoji reikšmė. Galite keisti suvestinės užduoties pavadinimą, bet negalite keisti pastangų, datų ar trukmės, nes jos apskaičiuojamos automatiškai. Panaikinus suvestinę užduotį, panaikinama pati užduotis ir visos jos papildomos užduotys.|  
| **Lapo mazgo užduotys** | Lapo mazgo užduotis vaizduoja patį smulkiausią projekto darbą. Ji rodo prognozuojamas pastangas, planuojamą išteklių skaičių, planuojamas pradžios bei pabaigos datas ir trukmę.|

  
## <a name="task-hierarchy"></a>Užduoties hierarchija  
 Kuriant užduoties hierarchiją, naudojamos šios parinktys:  
  
- **Įtraukti užduotį**.   Užduotį galite įtraukti pasirinktoje užduoties hierarchijos vietoje. Jei vietos nepasirinksite, nauja užduotis bus įtraukta į pabaigą.  
  
- **Užduoties įtrauka**.   Pritaikius užduoties įtrauką, užduotis tampa antrine užduotimi tos užduoties, kuri yra virš jos.  
  
- **Atvirkštinė užduoties įtrauka**.   Pasirinkite atvirkštinę įtrauką, jei nebenorite, kad ši užduotis būtų papildoma pirminės užduoties užduotimi.  
  
- **Perkelti aukštyn arba perkelti žemyn**.   Pirminių užduočių hierarchijoje perkelkite užduotis aukštyn arba žemyn. Užduoties perkėlimas aukštyn arba žemyn niekaip nepaveikia jos pastangų, savikainos, datų ar trukmės.  
  
## <a name="task-attributes"></a>Užduoties atributai  
 Užduoties pavadinimas aprašo darbą, kurį reikia atlikti. Įvairūs užduoties atributai naudojami aprašant užduoties grafiką ir reikalingų darbuotojų reikalavimus.  
  
### <a name="schedule-attributes"></a>Grafiko atributai

 - Priskiriant reikšmes laukuose **Pastangų valandos** , **Išteklių skaičius** , **Pradžios data** , **Pabaigos data** ir **Trukmė** , apibrėžiamas užduoties grafikas. 
 - **Pastangos** yra prognozuojamas valandų skaičius, reikalingas užduočiai atlikti.
 - **Išteklių skaičius** yra prognozuojami ištekliai, projekto vadovo skiriami užduočiai, siekiant sudaryti geriausią galimą grafiką. 
 - **Trukmė** (dienomis) rodo užduočiai atlikti reikalingų darbo dienų skaičių.  
  
### <a name="staffing-attributes"></a>Darbuotojų atributai

 - **Vaidmuo** , **Išteklių organizacinis vienetas** , **Išteklių skaičius** ir **Ištekliai** aprašo užduoties darbuotojų reikalavimus. 
 - **Vaidmuo** aprašo užduočiai atlikti reikalingų išteklių tipą. 
 - **Išteklių organizacinis vienetas** nurodo organizacinį vienetą, iš kurio šiai užduočiai turi būti skiriami ištekliai; šis atributas paveikia užduoties savikainą ir pardavimo sąmatą, kadangi į jį atsižvelgiama nustatant ištekliaus vieneto pardavimo kainą. 
 - **Ištekliai** – tai bendrojo ištekliaus pavadinimas arba įvardyto ištekliaus, kai toks surandamas, pavadinimas.  
  
## <a name="task-dependencies"></a>Užduoties priklausomybės  
 Darbo paskirstymo struktūroje galima sukurti ankstesnės užduoties ryšius su viena ar daugiau užduočių. Užduotyse galima nustatyti vieną ar daugiau ankstesnės užduoties lauko reikšmių, nurodančių nuo jų priklausančias užduotis. Užduočiai priskyrus ankstesnės užduoties reikšmę, užduotį pradėti galima tik atlikus visas ankstesnės užduoties užduotis. Nustačius užduočiai šią priklausomybę, planuojama užduoties pradžios data bus perskaičiuota į vėliausią visų jos ankstesnių užduočių atlikimo pabaigos datą. Ankstesnių užduočių poveikis grafikui neapsiriboja užduočiai apibrėžtu užduoties režimu.  
  
## <a name="task-mode"></a>Užduoties režimas  
 Užduoties režimas yra vienas iš svarbių veiksnių, lemiančių lapo mazgo užduočių planavimą. Yra du galimi kiekvienos užduoties režimai: automatinio planavimo režimas ir rankinio planavimo režimas.  
  
-   **Automatinis planavimas**.   nustačius automatinio planavimo užduoties režimą, užduoties planavimo modulis, nustatydamas užduoties grafiką, planavimo taisykles taiko šiems užduoties atributams.  
  
    -   Ankstesnės užduotys  
  
    -   Pastangos  
  
    -   Išteklių skaičius  
  
    -   pradžios ir pabaigos datos;  
  
-   **Planavimo taisyklės**.   Lapo mazgo užduoties, neturinčios ankstesnių užduočių, pradžios data pagal numatytąją reikšmę yra projekto grafiko pradžios data. Lapo mazgo užduoties trukmė visada apskaičiuojama kaip darbo dienų skaičius nuo jos pradžios datos iki pabaigos datos. Planuojant užduotį automatiškai, planavimo modulis taiko šias taisykles:  
  
    -   užduoties pradžios ir pabaigos datos, suplanuotos projekto planavimo kalendoriuje, visada turi būti darbo dienos;  
  
    -   užduoties, kuri turi ankstesnių užduočių, pradžios data pagal numatytąją reikšmę yra vėliausia jos ankstesnių užduočių atlikimo pabaigos data;  
  
    -   pastangos = darbuotojų skaičius * trukmė * valandomis per įprastą darbo dieną projekto kalendoriuje.  
  
-   **Neautomatinis planavimas**.   Kai kuriais atvejais galite norėti nukrypti nuo šių taisyklių. Tokiais atvejais galite nustatyti, kad užduoties režimas užduočiai būtų planuojamas rankomis. Taip planavimo modulis sustabdomas ir nebeskaičiuoja kitų planavimo atributų reikšmių. Užduotyse nustačius ankstesnes užduotis, tai visada paveikia priklausančios užduoties pradžios datą.  
  
## <a name="create-a-work-breakdown-structure"></a>Darbo paskirstymo struktūros kūrimas  
  
1.  Pasirinkite **Project Service > Projektai**.  
  
2.  Spustelėkite projektą, su kuriuo norite dirbti.  
  
3.  Juostoje ekrano viršuje pasirinkite žemyn nukreiptą rodyklę prie projekto pavadinimo, o tada spustelėkite Darbo paskirstymo struktūra.  
  
4.  Jei norite pridėti užduotį, spustelėkite **Įtraukti užduotį**. Užpildykite užduoties laukus, o tada spustelėkite **Įrašyti**.  
  
5.  Tęskite įtraukdami užduotis, kol užbaigsite darbo paskirstymo struktūrą. Kurdami darbo paskirstymo struktūrą, tvarkyti užduotis galite atlikdami šiuos veiksmus:  
  
    -   pasirinkite užduotį ir spustelėkite **Įtrauka** , jei užduotį norite perkelti žemiau kitos užduoties,„Atvirkštinė įtrauka, jei užduotį norite pakelti vienu lygiu;  
  
    -   pasirinkite užduotį ir spustelėkite **Perkelti aukštyn** arba **Perkelti žemyn** ; jei užduotį norite perkelti sąraše aukštyn arba žemyn;  
  
    -   spustelėkite **Slėpti Ganto diagramą** , jei Ganto diagramą norite paslėpti, arba spustelėkite **Rodyti Ganto diagramą** , jei norite, kad Ganto diagrama vėl būtų rodoma;  
  
    -   lauke **Laiko skalė** pasirinkite kitą Ganto diagramos laikotarpį.  
  
6.  Norėdami projekto komandos nariams pridėti vaidmenis, kuriuos nurodėte darbo paskirstymo struktūroje, spustelėkite **Kurti projekto komandą**.  
  
7.  Atlikę pakeitimus, spustelėkite mygtuką **Įrašyti** , esantį ekrano apatiniame dešiniame kampe.  
  
### <a name="see-also"></a>Taip pat žr.  
 [Projekto vadovo vadovas](../psa/project-manager-guide.md)
