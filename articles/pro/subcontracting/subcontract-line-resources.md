---
title: Subrangos sutarties eilutės ištekliai
description: Šiame straipsnyje paaiškinta, kaip nurodyti išteklius, kuriuos tiekėjas priskiria konkrečiai subrangos sutarties laiko eilutei.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522383"
---
# <a name="subcontract-line-resources"></a>Subrangos sutarties eilutės ištekliai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Programoje „Dynamics 365 Project Operations“ tiekėjas gali nurodyti išteklius, kurie bus naudojami teikiant išteklių pajėgumą, kuris perkamas subrangos sutarties laiko eilutėje.

## <a name="create-subcontract-line-resources"></a>Subrangos sutarties eilučių išteklių kūrimas

Norėdami sukurti subrangos sutarties eilutės išteklių, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje pasirinkite **Subrangos sutartys** ir atidarykite subrangos sutartį, su kuria norite dirbti.
2. Atidarykite subrangos sutarties laiko eilutę, kurioje norite nurodyti tiekėjo išteklius.
3. Skirtuko **Subrangos sutarties eilutės ištekliai** antriniame tinklelyje pasirinkite **+ Naujas subrangos sutarties eilutės išteklius**.
4. Puslapyje **Naujos subrangos sutarties eilutės ištekliai** įveskite reikiamą informaciją ir pasirinkite **Įrašyti ir uždaryti**.

Toliau esančioje lentelėje paaiškinami subrangos sutarties eilutės ištekliaus laukai.

| Laukas | Aprašymas | Funkcinis poveikis |
| ----- | ----------- | ----------------- |
| Rezervuotini ištekliai | Pasirinkite tipo **Sutarties darbuotojas** rezervuojamąjį išteklių, kurį norite naudoti kaip išteklių subrangos sutarties eilutėje.| Jei nesukūrėte sutarties darbuotojo rezervuojamojo ištekliaus, šį lauką palikite tuščią. Rezervuojamasis išteklius bus sukurtas įrašant įrašą.  |
| Prisijungti | Naudodami esamą kontaktą galite sukurti subrangos sutarties eilutės išteklių. Naudodami peržvalgą, sistemoje galite peržiūrėti aktyvių kontaktų sąrašą. Pasirinkite šios subrangos sutarties tiekėjo kontaktą. Jei pasirinktas kontaktas nėra tinkamas subrangos sutarties tiekėjo kontaktas, subrangos sutarties eilutės ištekliaus įrašas nebus įrašytas.| Jei pasirinkto kontakto rezervuojamųjų išteklių nėra, sistema pasirinktam kontaktui rezervuojamąjį išteklių sukuria prieš sukurdama subrangos eilutės išteklių. |
| Vartotojas | Pažymėdami aktyvų vartotoją galite sukurti subrangos sutarties eilutės išteklių. Naudodami peržvalgą, sistemoje galite peržiūrėti aktyvių vartotojų sąrašą.| Jei pasirinkto vartotojo rezervuojamųjų išteklių nėra, sistema pasirinktam vartotojui rezervuojamąjį išteklių sukuria prieš sukurdama subrangos eilutės išteklių. |
| Pradžios data | Data, kai prasidės subrangos sutarties darbuotojo priskyrimas.| Jei šis išteklius rezervuojamas laikotarpiui iki šio datų intervalo, bus pateiktas įspėjimas. |
| Pabaigos data | Data, kai baigiasi subrangos sutarties darbuotojo priskyrimas.| Jei šis išteklius rezervuojamas laikotarpiui po šio datų intervalo, bus pateiktas įspėjimas. |
| Pastangos | Bendras pastangų valandų skaičius, kurį sutarties darbuotojas sugaiš šiai subrangos sutarties eilutei.| Jei šie ištekliai rezervuojami ne tik pastangoms, paskirtoms šiai subrangos sutarčiai, pasirodys įspėjimas. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
