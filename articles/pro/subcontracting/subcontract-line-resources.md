---
title: Subrangos sutarties eilutės ištekliai
description: Šioje temoje paaiškinta, kaip nurodyti išteklius, kuriuos tiekėjas priskiria konkrečiai subrangos sutarties laiko eilutei.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323381"
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
4. Puslapyje **Naujas subrangos sutarties eilutės etapas** įveskite reikiamą informaciją ir pasirinkite **Įrašyti ir uždaryti**.

Toliau esančioje lentelėje paaiškinami subrangos sutarties eilutės ištekliaus laukai.

| Laukas |  Aprašymas |
| ----- | ------------ |
| Rezervuotini ištekliai | Pasirinkite tipo Sutarties darbuotojas rezervuojamąjį išteklių, kurį norite naudoti kaip išteklių subrangos sutarties eilutėje. Jei dar nesukūrėte sutarties darbuotojo rezervuojamojo ištekliaus, šį lauką palikite tuščią. Rezervuojamasis išteklius sukuriamas įrašant įrašą.  |
| Susisiekite | Jei laukas **Rezervuojamasis išteklius** yra tuščias, subrangos sutarties eilutės išteklių galite sukurti iš esamo kontakto. Naudodami peržvalgą, sistemoje galite peržiūrėti aktyvių kontaktų sąrašą. Pasirinkite šios subrangos sutarties tiekėjo kontaktą. Jūsų pasirinktas kontaktas patikrinamas įrašant įrašą. Jei jūsų pasirinktas kontaktas nėra tinkamas. įrašas nebus įrašytas. Jei pasirinkto kontakto rezervuojamųjų išteklių nėra, sistema pasirinktam kontaktui rezervuojamąjį išteklių sukuria prieš sukurdama subrangos eilutės išteklių. |
| Vartotojas | Jei laukas **Rezervuojamasis išteklius** yra tuščias, subrangos sutarties eilutės išteklių galite sukurti pasirinkdami aktyvų vartotoją. Naudodami peržvalgą, sistemoje galite peržiūrėti aktyvių vartotojų sąrašą. Jei pasirinkto vartotojo rezervuojamųjų išteklių nėra, sistema pasirinktam vartotojui rezervuojamąjį išteklių sukuria prieš sukurdama subrangos eilutės išteklių. |
| Pradžios data | Data, kai prasidės subrangos sutarties darbuotojo priskyrimas. Jei šis išteklius rezervuojamas laikotarpiui iki šio datų intervalo, bus pateiktas įspėjimas. |
| Pabaigos data | Data, kai baigiasi subrangos sutarties darbuotojo priskyrimas. Jei šis išteklius rezervuojamas laikotarpiui po šio datų intervalo, bus pateiktas įspėjimas. |
| Pastangos | Bendrasis pastangų valandų, kurias subrangos sutarties darbuotojas praleis šioje subrangos sutarties eilutėje nurodytiems darbams atlikti, skaičius. Jei rezervuojama daugiau šio ištekliaus pastangų nei priskirta šioje subrangos sutartyje, bus pateiktas įspėjimas. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
