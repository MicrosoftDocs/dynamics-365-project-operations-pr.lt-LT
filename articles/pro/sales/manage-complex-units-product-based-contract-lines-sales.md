---
title: Produktu pagrįstų sutarties eilučių sudėtinių vienetų valdymas – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip palaikomas prenumeruojamų produktų pardavimas.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6bd4e11bf96d9f7d77c77fe081fde02b421c3139915150480a8d1a4d812887f6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003376"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Produktu pagrįstų sutarties eilučių sudėtinių vienetų valdymas – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

„Dynamics 365 Project Operations“ programoje naudojami kiekio koeficientai, kad būtų palaikomas prenumerata pagrįstų produktų pardavimas. Prenumerata pagrįstiems produktams sutarties arba projekto sutarties eilutėje kiekis išreiškiamas kaip vartotojo mėnesių skaičius.

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