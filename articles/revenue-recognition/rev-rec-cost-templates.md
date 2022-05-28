---
title: Sąnaudų šablonų nustatymas
description: Šioje temoje pateikiama informacijos apie tai, kaip kurti ir naudoti sąnaudų šablonus programoje „Project Operations”.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9e163dc3180d2b35ddf9b15aa0577bf51e3b72ce
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594220"
---
# <a name="set-up-cost-templates"></a>Sąnaudų šablonų nustatymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_


Šioje temoje pateikiama informacijos apie tai, kaip kurti ir naudoti sąnaudų šablonus programoje „Project Operations”. Sąnaudų šablonas nustato:

- projekto kategorijas, taikomas prognozuojamoms ir faktinėms operacijoms, kurios bus įtrauktos į projekto atlikimo skaičiavimo procentinę vertę. Tada atlikimo procentais vertė naudojama siekiant apskaičiuoti pajamas;
- ar galima modifikuoti atlikimo procentinę vertę, jei ji apskaičiuojama automatiškai;
- ar atlikimo procentais vertė apskaičiuojama pagal sumas ar vienetus.

## <a name="cost-template-example"></a>Sąnaudų šablono pavyzdys

Dirbate su kliento žiniatinklio svetainės dizaino projektu ir už jį imate fiksuotą 10 000 USD mokestį. Prognozuojate, kad jums reikės 100 valandų (5 000 USD) projektui užbaigti. Taip pat numatote, kad reikės pirkti du lėktuvo bilietus ir užsisakyti keturias nakvynes viešbutyje, nes reikės nuvykti pas klientą (1 800 USD). Taigi bendra prognozuojama savikaina yra 6 800 USD.

Paleidę fiksuotos kainos įplaukų pripažinimo procesą, kad mėnesio pabaigoje sukurtumėte įvertinimą, pamatote, kad projektui skyrėte 35 valandas. Tai dar neapima skrydžių arba viešbučio išlaidų. Jūs taip pat turėjote padėjėją, kuris atliko penkių valandų trukmės tyrimą, susijusį su projektu, kuriam sumokėjote 100 USD, ir šios išlaidos nebuvo suplanuotos.

Norėdami apskaičiuoti šio projekto atlikimo procentais vertę, turite atsakyti į toliau nurodytus klausimus.

- Ar norite įtraukti visas išlaidas (valandas ir išlaidas) ar tik valandas?
- Ar norite įtraukti visas valandas ir tik suplanuotas valandas?
- Ar norite apskaičiuoti atlikimo procentais vertę remdamiesi suplanuotų valandų (5 000 USD) savikaina doleriais ar tik remdamiesi valandų skaičiumi (100)?

Nuo jūsų atsakymų į šiuos klausimus priklauso sąnaudų šablono parinktys, kurias nustatysite, ir kategorijos, kurias pasirinksite sąnaudų šablono eilutėse.

Toliau esančioje lentelėje parodyti skirtingų šio scenarijaus atlikimo procentais vertės apskaičiavimo metodų rezultatai.

| Atlikimo pagrindas | Savikaina doleriais arba vienetai | Atlikimo procentas | Skaičiavimas |
| --- | --- | --- | --- |
| Visos valandos, be išlaidų | Savikaina doleriais | 37 % 35 x 50 USD + 100 USD = 1 850 USD 1 850 USD iš 5 000 USD |
| Visos valandos, be išlaidų | Vienetai | 40 % | 40 valandų iš 100 valandų (įskaitant penkias nesuplanuotas valandas) |
| Suplanuotos valandos, be išlaidų | Savikaina doleriais arba vienetai | 35 % | 35 iš 100 valandų arba 35 x 50 USD / 5 000 USD |
| Visos valandos ir išlaidos | Savikaina doleriais | 27,2 % | 1 850 USD iš 6 800 USD |

Sprendimas, kokį sąnaudų šabloną kurti, priklauso nuo įvairių aspektų.

- Jei į sąnaudų šabloną įtrauksite neplanuotas valandas, kyla rizika, kad pasieksite 100 procentų dar nebaigę projekto. Taip bus todėl, kad faktinės valandos viršys suplanuotas valandas. Jei naudosite vieną iš pirmųjų dviejų metodų, pateiktų lentelėje, turėtumėte pakeisti planą (prognozuojamus vienetus), kai yra nuokrypių. Tokiu atveju turėsite pridėti arba atimti valandas remdamiesi savo žiniomis apie tai, ko reikia projektui baigti. Jei projektui užbaigti reikės dar 65 valandų, į planą įtrauksite penkias valandas ir iš viso bus 105 valandos. Jei žinote, kad jūsų padėjėjas atliks dar vieną penkių valandų tyrimą, iš viso bus 110 valandų.
- Jei naudojate trečiąjį lentelėje pateiktą metodą, reikės tik atnaujinti suplanuotas savo laiko valandas, kad užtikrintumėte tikslų atlikimo procentais skaičiavimą. Jūsų pelningumo vertė pasikeis užregistravus neplanuotas valandas, bet žinosite atlikimo procentais vertę.
- Jei naudojate ketvirtąjį lentelėje pateiktą metodą, kyla rizika, kad išlaidos bus nereguliarios ir jos gali neatsispindėti atlikimo eigoje. Todėl, jei bus įtrauktos išlaidos, jūsų atlikimo procentinė dalis gali svyruoti labiau, nei norite. Pavyzdžiui, jūsų skrydžio dar nebuvo, todėl atlikimo procentinė vertė yra 27 proc. vietoj 35 proc. arba 37 proc., jei skaičiavimas grindžiamas tik laiko duomenimis. Jei vieną kartą skridote pas klientą ir dvi naktis praleidote viešbutyje, ir tiksliai numatėte skrydžio ir viešbučio išlaidas, atlikimo procentinė vertė būtų 40,4 proc. (1 850 USD už darbą ir 900 USD išlaidoms = 2 750 USD iš 6 800 USD = 40,4 proc.). Todėl įtraukus tik vienos kelionės lėktuvu išlaidas, atlikimo procentinė vertė pasikeistų iš 27 proc. į 40 proc.

## <a name="create-cost-templates"></a>Sąnaudų šablonų kūrimas
Norėdami sukurti sąnaudų šabloną, atlikite toliau nurodytus veiksmus.

1. Norėdami pasiekti išlaidų šablonus, Dynamics 365 Finance aplinkoje eikite į **Projektų valdymo ir apskaitos** > **nustatymo sąmatų** > **išlaidų šabloną** > **·**.
2. Norėdami sukurti naują sąnaudų šabloną, pasirinkite **Naujas**. Įveskite pavadinimą ir aprašą.
3. Nurodykite kiekvieno tipo operacijos sąnaudų eilutės ID.
4. Pasirinkite numatytąjį atlikimo skaičiavimo metodą:

  - **Automatinis**: projekto atlikimo procentinė vertė apskaičiuojama automatiškai. Gautos vertės pakeisti negalima.
  - **Rankinis**: projekto atlikimo procentinė vertė apskaičiuojama automatiškai. Gautą vertę galima pakeisti.

  > [!NOTE]
  > Atliekant skaičiavimus rankiniu būdu, atlikimo procentinė vertė tvarkoma puslapio **Įvertinimas** skirtuko **Bendra** dalyje **Skaičiavimas rankiniu būdu**.

5. Dalyje **Užbaigimas pagrįstas** pasirinkite vieną iš toliau nurodytų verčių:

  - **Suma**: suma apskaitos valiuta apskaičiuoja atlikimo procentinę vertę.
  - **Vienetas**: kiekis apskaičiuoja atlikimo procentinę vertę.
  - **Tiesiogiai proporcingas metodas**: sistema proporcingai apskaičiuoja atlikimo procentinę vertę naudodama projekto pradžios ir pabaigos datas, kad nustatytų projekto trukmę.

6. Pasirinkite **Sąnaudų eilutės**, kad peržiūrėtumėte sąnaudų šablono sąnaudų eilutes. Kiekvienas operacijos tipas turi turėti bent vieną sąnaudų eilutę. Tačiau galite kurti kelias sąnaudų eilutes tiems patiems operacijos tipams ir nustatyti norimus šių eilučių atributus.
7. Skirtuke **Kategorijos** pasirinkite projekto kategorijas, kurios bus įtrauktos į sąnaudų šablono eilutę.
8. Skirtuke **Bendra** pasirinkite, ar ši eilutė bus įtraukta apskaičiuojant atlikimo procentinę vertę.
9. Pasirinkite užbaigimo išlaidų apskaičiavimo metodą, kuris bus naudojamas atlikimo procentinei vertei apskaičiuoti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]