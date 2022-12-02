---
title: Užsakymų ir priskyrimų derinimas
description: Šiame straipsnyje pateikta informacija apie faktinius duomenis.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 04c238527006daab4c55f17280ce46b7df2aa649
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920392"
---
# <a name="reconcile-bookings-and-assignments"></a>Užsakymų ir priskyrimų derinimas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekto komandos nario projektų užsakymai ir projekto užduočių priskyrimai yra silpnai susiję. Todėl ištekliams gali būti užduočių priskyrimų, kurie neatitinka užsakymų, o užsakymai, gali neatitikti užduočių priskyrimų. Geriausia, kad projektų užsakymai ir užduotys būtų suderinti, kad ištekliams būtų priskirta pajėgumas atlikti užduočių priskyrimus. Tačiau tikrovė yra tokia, kad užsakymai gali būti atliekami atsižvelgiant į užimtumą, o užduoties laikas gali pasikeisti projekto įgyvendinimo tąsos laikotarpiu. Todėl dėl laisvo siejimo galimas lankstumas.

Dėl projekto užsakymų ir užduočių priskyrimų laisvo siejimo į projekto objektą įtraukiamas skirtukas **Derinimas**. Šis skirtukas padeda projektų vadovams suderinti komandos narių rezervavimą ir jų projekto komandos priskyrimus.

Kiekvieno pavadinto komandos nario skirtuke **Derinimas** rodomi užsakymai ir priskyrimai iki atskiro užduoties priskyrimo. Jame rodomos valandos langeliuose, kurie gali nurodyti laikotarpius nuo mėnesių iki dienų.

Lauke **Laiko skalė** galite pasirinkti **Mėnesis**, **Savaitė** arba **Diena**. **Savaitė** yra numatytoji parinktis. Tačiau numatytąją reikšmę galite pakeisti spustelėję mygtuką **Parametrai**. Kai skirtukas **Derinimas** atidaromas, rodoma dabartinė data, tačiau galite naudoti kalendoriaus valdiklį ir pereiti laike į priekį arba atgal. Kai projekto pradžios data yra ateityje, skirtuke rodoma data, kai jis atidaromas. Kalendoriaus valdiklis taip pat turi parinkčių, leisiančių pereiti prie projekto pradžios ir laiko datų.

Galite naudoti kiekvieno ištekliaus plėstuvo valdiklius, kad būtų rodoma išsami informacija apie išteklių rezervavimą. Taip pat galite išplėsti kiekvieno ištekliaus priskyrimus pagal atskirų užduočių lygį.

Skirtuko **Derinimas** apačioje rodoma bendra bendroji projekto suma bei skirtuke yra bendras stulpelis. Kiekvienam ištekliui skirtuke atsižvelgiama į skirtumus tarp komandos nario projekto užsakymų ir tos komandos narių užduočių priskyrimų. Geriausiu atveju skirtumas turi būti 0 (nulis). Kitaip sakant, išteklių rezervavimai ir jų užduočių priskyrimai neturėtų skirtis. Bet kokius skirtumus nurodo spalva ir atspalvis atkreipti dėmesį į dvi sąlygas:

- **Užsakymų trūkumas** – užsakymo trūkumo įvyksta, kai ištekliai turi daugiau užduočių nei užsakymų. Kadangi šis pajėgumas nebuvo rezervuotas, projektų vadovas šią sąlygą gali pataisyti išplėsdamas išteklių rezervavimą, kad padengtų trūkumą.
- **Užsakymų perteklius** – užsakymų perteklius įvyksta, kai ištekliai buvo rezervuoti projektui, tačiau nebuvo priskirti užduotims. Ši sąlyga gali būti priimtina, jei, pvz., ištekliai buvo rezervuoti iki užduočių priskyrimo. Tačiau kitais atvejais ištekliai gali būti neplanuoti priskirti. Tokiais atvejais projektų vadovas turėtų apsvarstyti išteklių rezervavimo atšaukimą, kad pajėgumą būtų galima naudoti kitam projektui.

> [!NOTE]
> Šių sąlygų legenda gali būti paslėpta, kad liktų daugiau vietos tinkleliui. Šiuo atveju galite padaryti legendą matomą spustelėdami mygtuką **Parametrai**.

Kai kuriais atvejais, kai laukas **Laiko skalė** nustatomas kaip lygis, kuris yra didesnis nei **Diena**, skirtumai gali būti apskaičiuojami kaip 0 (nulis). Pavyzdžiui, lygyje **Mėnesis** grynasis ištekliaus skirtumas gali būti 0 (nulis), kad nurodytų, jog užsakymai yra lygūs priskyrimams. Tačiau, jei peržiūrite lygį **Savaitė**, galite matyti, kad ten yra 0 (nulis) priskyrimų valandų ir rezervuota 40 valandų pirmojoje mėnesio savaitėje bei 40 priskyrimų valandų ir 0 (nulinių) valandų užsakymui antrą mėnesio savaitę. Nors bendras mėnesio užsakymų ir priskyrimų kiekis yra vienodas, jis skiriasi pagal savaitę.

Kai peržiūrite stambesnius laiko lygius, skirtuke **Derinimas** rodomas langelio indikatorius, kuris jums praneš, kad yra skirtumų esant smulkesniems laiko lygiams. Pavyzdžiui, šioje iliustracijoje rodomas langelio indikatorius, esantis 2018 m. spalio mėnesio langelyje, skirtame ištekliams, pavadintame Margarita Ambrazaitytė. Todėl galite matyti, kad net jei išteklių užsakymai ir priskyrimai lygūs lygiu **Mėnesis**, jie nesutampa su smulkesniais lygiais.

![Nesuderinti užsakymai ir prieskyros mėnesio lygiu.](media/reconcile-assignments-01.JPG)

Dukart spustelėkite langelį, jei norite priartinti kitą apatinį lygį ir peržiūrėti skirtumą. Pavyzdžiui, jei dukart spustelėjate 2018 m. spalio mėnesio skirtumą, langelyje Margarita Ambrazaitytė, galite detalizuoti lygį **Savaitė**. Tada galite matyti, kad ištekliai yra rezervuoti 16 valandų, bet jokių priskyrimų, esančių pirmąsias dvi spalio mėnesio savaites, ir 16 valandų priskyrimų, tačiau jokių užsakymų trečią spalio savaitę.

![Nesuderinti užsakymai ir prieskyros savaitės lygiu.](media/reconcile-assignments-02.JPG)

Galite dešiniuoju pelės mygtuku spustelėti langelį ir sumažinti tolimesnį stambesnį lygį. Taip pat galite išjungti langelio indikatorių pažymėdami mygtuką **Parametrai**. 

Taip pat galite naudoti mygtukus **Ankstesnis** ir **Kitas**, esančius virš tinklelio, ir peržvelgti visus projekto skirtumus. Norėdami naudoti šiuos mygtukus, pirmiausia turite pažymėti išteklių. Pasirinkite **Kitas**, kad pereitumėte prie kito skirtumo tarp to ištekliaus užsakymų ir priskyrimų. Pasirinkite **Ankstesnis**, kad pereitumėte prie ankstesnio skirtumo.

Situacijose, kai ištekliams yra užduočių priskyrimų, bet nėra užsakymų, galite pažymėti rezervavimo trūkumą ir pažymėti **Pratęsti rezervavimą**. Tada galite peržiūrėti rezervavimą, reikalingą norint spręsti išteklių trūkumą. Taip pat galite peržiūrėti išteklių užsakymus dabartiniame projekte ir kituose projektuose. Pasirinkite **Gerai**, kad sukurtumėte išteklių rezervavimą neatsižvelgdami į dabartinį pasiekiamumą. Tada projektų vadovas arba išteklių vadovas gali naudoti grafiko lentą valdyti situacijas, kai ištekliams priskirta per daug užsakymų lyginant su pajėgumu dėl to, kad užsakymai buvo pratęsti.

## <a name="managing-with-time-zones"></a>Laiko juostų valdymas
Norint užtikrinti tikslius ir prognozuojamus rezultatus naudojat rezervavimo išplėtimą, reikia atitikti dvi pagrindines sąlygas:  

- Naudotojas turi nustatyti savo įrenginio laiko juostą, kad ji atitiktų laiko juostą, apibrėžtą sistemos personalizavimo parametruose.
 
  ![Laiko juostos parametrai „Windows 10“.](media/reconcile-assignments-03.png)

  ![Laiko juostos parametrai personalizavimo parametruose.](media/reconcile-assignments-04.png)
 
- Rezervuojami ištekliai turi turėti bent vieną minutę darbo laiko, kuri sutampa su kontūrais, kurie naudojami pageidaujamo išplėtimo apibrėžimui. Pavyzdžiui, toliau pateiktame pavyzdyje rodomi peržiūros ištekliai su darbo valandomis, kurios yra intervale nuo 9.00 iki 19.00. 

  ![Išteklių kontūrų palyginimas.](media/reconcile-assignments-05.png)

Toliau esančioje lentelėje pateikiama:

- A projekto kalendoriaus šablonas.
- A išteklius: šis išteklius turi tą patį kalendorių ir yra toje pačioje laiko juostoje kaip ir projektas. Rezervavimo pradžios laikas bus 9.00.
- B išteklius: šis išteklius yra kitoje nei projektas laiko zonoje, todėl jo pradžia yra 7.00 jo laiko juostoje. Tačiau rezervavimai prasidės 9.00, nes tai yra anksčiausias priskyrimo kontūro pradžios laikas.
- C ir D ištekliai: šie ištekliai taip pat yra skirtingose laiko juostose, kurios abi skiriasi tarpusavyje ir nuo projekto, todėl jų rezervavimai prasidės ne anksčiau nei atitinkami galimi pradžios laikai.

|Entity  |Kalendorius  |
|-|-|
|Projekto kalendoriaus šablonas   | ![Projekto kalendorius.](media/reconcile-assignments-06.png) |
|A išteklius  | ![A ištekliaus kalendorius.](media/reconcile-assignments-06.png) |
|B išteklius  |  ![B ištekliaus kalendorius.](media/reconcile-assignments-07.png) |
|C išteklius  |  ![C ištekliaus kalendorius.](media/reconcile-assignments-08.png) |
|D išteklius  | ![D ištekliaus kalendorius.](media/reconcile-assignments-09.png)  |
 
Kai pereisite į suderinimo rodinį, bus rodomi išteklių priskyrimai ir susiję rezervavimo trūkumai.
 ![Suderinimo rodinys prieš išplėtimą.](media/reconcile-assignments-10.png)

Po to, kai buvo įvykdyta kiekvieno ištekliaus rezervavimo pratęsimo funkcija, sėkmingai pratęsiamos kiekvieno ištekliaus rezervacijos. Taip yra todėl, kad kiekvieno ištekliaus darbo valandos sutapo su trūkumo kontūrais.
 ![Suderinimo rodinys po rezervavimo išplėtimo.](media/reconcile-assignments-11.png) 

Tačiau atidžiau apžvelgus rezervacijų išsamią informacija, matomi rezervacijų laiko pradžios skirtumai. Rezervavimai prasidės ne anksčiau nei priskyrimo kontūro pradžios laikas ir ne anksčiau nei galimas ištekliaus pradžios laikas.
 ![Naujos išteklių rezervacijos grafiko lentoje.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
