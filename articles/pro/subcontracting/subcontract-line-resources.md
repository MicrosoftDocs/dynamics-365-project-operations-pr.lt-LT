---
title: Subrangos sutarties eilutės ištekliai
description: Šioje temoje paaiškinta, kaip nurodyti išteklius, kuriuos tiekėjas priskiria konkrečiai subrangos sutarties laiko eilutei.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 96bce2d6797c124331ce0174b16804ff8dfec993
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576096"
---
# <a name="subcontract-line-resources"></a>Subrangos sutarties eilutės ištekliai

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

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
