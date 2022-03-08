---
title: Nustatyti subrangovus kaip rezervuotinus išteklius
description: Šioje temoje paaiškinta, kaip nustatyti ir tvarkyti subrangovo išteklius, kurie sukuriami sistemoje iš vartotojų ir sutarčių, siekiant juos susieti su subrangos sutartimis programoje „Microsoft Dynamics 365 Project Operations”.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994196"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Nustatyti subrangovus kaip rezervuotinus išteklius

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Norėdami nustatyti subrangovus kaip rezervuojamus išteklius programoje „Microsoft Dynamics 365 Project Operations”, atlikite toliau nurodytus veiksmus.

1. Eikite į **Projektas**\>**Ištekliai** ir pasirinkite **Naujas**.
2. Puslapio **Naujas rezervuojamas išteklius** lauke **Išteklių tipas** pasirinkite vieną iš toliau nurodytų parinkčių.

    - **Vartotojas** – pasirinkite šį išteklių tipą, jei subrangovas turi pasiekti „Project Operations”, kad įvestų laiką ar išlaidas. Jei pasirinksite **Vartotojas**, subrangovui reikia galiojančios licencijos, kad galėtų pasiekti sistemą.
    - **Kontaktas** arba **Klientas** – pasirinkite vieną iš šių išteklių tipų, jei subrangovui nereikia prieigos prie „Project Operations”, bet jis turi būti pasiekiamas, norint priskirti projekto užduotis arba rezervavimus. Nė vienas iš šių išteklių tipų nesuteikia prieigos prie sistemos. Pasirinkite **Klientas**, jei norite rodyti tiekėjo įmonę kaip rezervuojamą išteklių. Pasirinkite **Kontaktas**, jei norite rodyti atskirus tiekėjo darbuotojus.

3. Atsižvelgiant į pasirinktą išteklių tipą, būsite paraginti pasirinkti atitinkamą vartotojo, kliento arba kontakto įrašą.
4. Lauke **Darbuotojo tipas** pasirinkite „Sutarties darbuotojas”, kad nustatytumėte subrangovą kaip rezervuojamą išteklių.

    > [!NOTE]
    > Jei lauką **Darbuotojo tipas** paliksite tuščią, rezervuojamas išteklius bus laikomas darbuotoju.

5. Jei pasirinkote darbuotojo tipą **Sutarties darbuotojas**, pasirinkite tiekėją, kuriam dirba šis išteklius.
6. Pasirinkite ištekliaus laiko juostą, tada pasirinkite **Įrašyti**. Norėdami rezervuojamam ištekliui priskirti darbo valandų šabloną, sąrašo **Rezervuojamas išteklius** puslapyje galite pasirinkti **Nustatyti kalendorių**.

Rezervuojamas išteklius turi atitikti toliau nurodytas sąlygas, kad būtų susietas su subrangos sutarties eilutę.

- Rezervuojamas išteklius turi būti sutarties darbuotojas.
- Išteklių tipo **Kontaktas** rezervuojamas išteklius turi būti susietas su tiekėjo klientu kaip kontaktas. Išteklių tipo **Vartotojas** rezervuojamas išteklius neturi būti susietas su tiekėjo klientu kaip kontaktas.
- Rezervuojamo ištekliaus lauko **Tiekėjas** reikšmė turi sutapti su subrangos sutarties lauko **Tiekėjas** reikšme.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Atnaujinti rezervuojamų išteklių darbuotojo ir tiekėjo susiejimo tipą

Rezervuojamo ištekliaus lauke **Darbuotojo tipas** nustatoma, ar rezervuojamas išteklius yra sutarties darbuotojas, ar darbuotojas. Lauku **Tiekėjas** nustatomas tiekėjo klientas, su kuriuo siejamas rezervuojamas išteklius. Susiedami rezervuojamą išteklių su tiekėju kaip kontaktu, nurodote, kad kontaktas yra tiekėjo įmonės darbuotojas.

Jei rezervuojamo ištekliaus laukai **Darbuotojo tipas** ir **Tiekėjas** keičiami, šie pakeitimai turi įtakos visiems būsimiems rezervuojamo ištekliaus kuriamiems naujų įrašų patikrinimams, pvz., laiko įrašams. Tačiau dėl šių pakeitimų esami įrašai nenustos galioti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
