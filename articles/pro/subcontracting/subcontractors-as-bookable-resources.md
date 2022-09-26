---
title: Nustatyti subrangovus kaip rezervuotinus išteklius
description: Šiame straipsnyje paaiškinama, kaip nustatyti ir prižiūrėti subrangovų išteklius, sukurtus iš sistemos vartotojų ir kontaktų, kad juos būtų galima susieti su subrangos sutartimis programoje "Microsoft" Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 727508c41c190c3703e9cd1420066fa0e551f147
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522712"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Nustatyti subrangovus kaip rezervuotinus išteklius

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

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
