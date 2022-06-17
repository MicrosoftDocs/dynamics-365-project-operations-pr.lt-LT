---
title: Produktu pagrįsto pasiūlymo eilučių sudėtinių vienetų valdymas, pvz., pagal vartotoją ar pagal mėnesį – „Lite“ versija
description: Šiame straipsnyje pateikiama informacija apie sudėtingų produktų pasiūlymų eilučių vienetų valdymą.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88173468cd2e898331c4aa0a398792d9a0f3df10
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929914"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Produktu pagrįsto pasiūlymo eilučių sudėtinių vienetų valdymas, pvz., pagal vartotoją ar pagal mėnesį – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

„Dynamics 365 Project Operations“ programoje naudojami kiekio koeficientai, kad būtų palaikomas prenumerata pagrįstų produktų pardavimas. Prenumerata pagrįstiems produktams pasiūlymo arba projekto sutarties eilutėje kiekis išreiškiamas kaip vartotojo mėnesių skaičius.

Paprastai prenumeratos programinės įrangos kaina kataloge yra kaina vienam vartotojui per mėnesį. Per pardavimo procesą pasiūlymo eilutėje nurodyta kaina paprastai yra vienam vartotojui per mėnesį, dėl kurios susitarė ir nuolaidą pritaikė IT pardavimo agentas. Kiekvienas sandoris turi skirtingą vartotojų skaičių ir skirtingą prenumeratos mėnesių skaičių. Kiekis, naudojamas pasiūlymo eilutei apskaičiuoti, yra vartotojų skaičiaus ir prenumeratos mėnesių skaičiaus produktas.

Norėdami paremti šį pardavimo tipą, „Project Operations“ pristatė kiekio koeficientų koncepciją. Kiekio koeficientai priklauso nuo „Dynamics 365“ produkto atributų. Konfigūruojant konkrečias produkto ypatybes, „Project Operations“ leidžia žymėti pogrupį arba visas ypatybes kaip kiekio koeficientus.

„Project Operations“ tikrina, kad tik skaitinės ypatybės arba produkto, turinčio skaitinių duomenų tipą, ypatybės būtų žymimos kaip kiekio koeficientai. Kai į pasiūlymo eilutę įtraukiate produktą su kiekio faktoriais, laukas **Kiekis** tampa tik skaitomu. Įvedus produktų ypatybių reikšmes, kurios yra kiekio koeficientai, „Project Operations“ apskaičiuoja pasiūlymo eilutės kiekį.

Pavyzdžiui, „Dynamics 365 Sales“ gali turėti šias ypatybes:

- **Vartotojų skaičius** – vartotojų skaičius
- **Mėnesių skaičius** – prenumeratos mėnesių skaičius
- **Produkto SKU**

Galite vėliavėle pažymėti ypatybes **Vartotojų skaičius** ir **Mėnesių skaičius** kaip kiekio koeficientus redaguodami produkto eilutės ypatybes.

Norėdami kurti produkto ypatybių kiekio koeficientus, atlikite šiuos veiksmus:

1. Kairiojoje „Project Operations“ naršymo srityje eikite į **Pardavimas** > **Produktai**.
2. Atidarykite produktą, kuriam reikia konfigūruoti kiekio koeficientus. Patikrinkite, ar produkto ypatybės jau sukonfigūruotos.
3. Produkto puslapyje **Projekto informacija** pažymėkite skirtuką **Kiekio koeficientai**.
4. Antriniame tinklelyje pasirinkite **+ Naujo lauko apskaičiavimas**.
5. Įveskite kiekio koeficiento pavadinimą ir pasirinkite ypatybės reikšmę, kuri susieja ją su lauko apskaičiavimu.
6. Įrašykite ir uždarykite formą. Pakartokite šiuos veiksmus su visomis ypatybėmis, kurias reikia naudoti produktu pagrįsto pasiūlymo eilutės kiekiui apskaičiuoti.

Kai kuriate produkto produktu pagrįsto pasiūlymo eilutę, pasiūlymo eilutės kiekis bus užrakintas. Kiekis bus skaičiuojamas kaip ypatybių reikšmių, kurias įvedate tai pasiūlymo eilutei, produktas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]