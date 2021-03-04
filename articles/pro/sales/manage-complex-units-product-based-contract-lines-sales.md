---
title: Produktu pagrįstų sutarties eilučių sudėtinių vienetų valdymas – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip palaikomas prenumeruojamų produktų pardavimas.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177386"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Produktu pagrįstų sutarties eilučių sudėtinių vienetų valdymas – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Programoje „Dynamics 365 Project Operations“ naudojami kiekio koeficientai, kad būtų palaikomas prenumerata pagrįstų produktų pardavimas. Prenumerata pagrįstiems produktams sutarties arba projekto sutarties eilutėje kiekis išreiškiamas kaip vartotojo mėnesių skaičius.

Prenumeruojamos programinės įrangos kaina kataloge saugoma kaip kaina vienam vartotojui per mėnesį. Pardavimo proceso metu sutarties eilutėje nurodyta kaina paprastai yra vienam vartotojui per mėnesį, dėl kurios susitarė ir kuriai nuolaidą pritaikė pardavimo agentas. Kiekvienas sandoris turi skirtingą vartotojų skaičių ir skirtingą prenumeratos mėnesių skaičių. Kiekis, naudojamas sutarties eilutės sumai apskaičiuoti, yra vartotojų skaičiaus ir prenumeratos mėnesių skaičiaus sandauga.

Kad būtų palaikomas šis pardavimo tipas, „Project Operations“ palaiko *kiekio koeficientų* koncepciją. Kiekio koeficientai priklauso nuo produkto atributų. Konfigūruojant konkrečias produkto ypatybes, galite žymėti tų ypatybių pogrupį arba visas ypatybes kaip kiekio koeficientus.

„Project Operations“ tikrina, kad tik skaitinės ypatybės arba produkto, turinčio skaitinių duomenų tipą, ypatybės būtų žymimos kaip kiekio koeficientai. Kai į sutarties eilutę įtraukiamas produktas su sukonfigūruotais kiekio koeficientais, laukas **Kiekis** tampa tik skaitomas. Įvedus produktų ypatybių reikšmes, kurios yra kiekio koeficientai, „Project Operations“ apskaičiuoja sutarties eilutės kiekį.

Pavyzdžiui, „Dynamics 365 Sales“ gali turėti šias ypatybes:

- **Vartotojų skaičius** – vartotojų skaičius.
- **Mėnesių skaičius** – prenumeratos mėnesių skaičius.
- **Produkto SKU**: produkto sandėliavimo vienetas (SKU).

Ypatybės **Vartotojų skaičius** ir **Mėnesių skaičius** gali būti pažymėtos kaip kiekio koeficientai redaguojant produkto eilutės ypatybes.

Norėdami kiekio koeficientus kurti pagal produktų ypatybes, atlikite toliau nurodytus veiksmus.

1. Programoje **„Project Operations“** pasirinkite **Pardavimo produktai**.
2. Atidarykite produktą, kuriam reikia nustatyti kiekio koeficientus. Įsitikinkite, kad produkto ypatybės jau nustatytos.
3. Puslapyje **Projekto informacija** pasirinkite skirtuką **Kiekio koeficientai**.
4. Antriniame tinklelyje pasirinkite **+ Naujo lauko apskaičiavimas**.
5. Įveskite **kiekio koeficiento** pavadinimą ir pasirinkite ypatybės reikšmę, kuri susieja ją su lauko apskaičiavimu.
6. Įrašykite ir uždarykite formą.
7. Pakartokite 2–6 veiksmus su visomis ypatybėmis, kurios kartu sudarys su produktais susijusios sutarties eilutės kiekį.

Kai, nustatęs kiekio koeficientus, vartotojas sukuria šio produkto sutarties eilutę, jos kiekis yra užrakinamas. Tada kiekis apskaičiuojamas kaip tos sutarties eilutės ypatybių reikšmių sandauga.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]