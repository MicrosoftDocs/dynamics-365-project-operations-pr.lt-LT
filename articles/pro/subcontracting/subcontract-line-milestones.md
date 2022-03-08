---
title: Subrangos sutarties eilutės etapai
description: Šioje temoje aiškinama, kaip sukurti ir prižiūrėti etapais pagrįstą subrangos sutarties sąskaitos faktūros grafiką su tiekėju.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7f99853f5f649f96225b7d72580db97bb92de7c5
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558512"
---
# <a name="subcontract-line-milestones"></a>Subrangos sutarties eilutės etapai

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

„Dynamics 365 Project Operations“ naudojant subrangos sutarties eilutę su fiksuotos kainos atsiskaitymo metodu, galima nurodyti etapais pagrįstą subrangos sutarties sąskaitos faktūros grafiką su tiekėju.

Tiekėjo sąskaitų faktūrų išrašymo etapus galima generuoti automatiškai naudojant nustatytą dažnumą arba jų sukurti galite rankiniu būdu.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Automatinis etapais pagrįsto sąskaitos faktūros grafiko kūrimas subrangos sutarties eilutei

Atlikite toliau nurodytus veiksmus ir automatiškai sugeneruokite vienodai paskirstytų etapų fiksuoto rinkinio etapais pagrįstų sąskaitų faktūrų grafiką.

1. Eikite **Parametrai** > **Sąskaitų faktūrų dažnumas** ir nustatykite subrangos sutarties eilučių sąskaitų faktūrų dažnumą.
2. Atidarykite puslapį **Subrango sutartys**, atidarykite subrangos sutartį su kuria norite dirbti, tada atidarykite fiksuotos kainos subrangos sutarties eilutę, kuriai ketinate sukurti etapo grafiką.
3. Skirtuke **Subrangos sutarties eiilutės etapai** pasirinkite **Generuoti periodinius etapus**.
4. Dialogo lange įveskite arba pasirinkite datų intervalą, etapų skaičių ir sąskaitos faktūros dažnumą. Galite pasirinkti pradžios datą arba etapų skaičių ir sąskaitos faktūros dažnumą arba pradžios datą arba galite pasirinkti pabaigos datą ir sąskaitos faktūros dažnumą. Pasirinkti pabaigos datos ir etapų skaičiaus negalite.
Pasinaudodama šia informacija, sistema sugeneruoja etapus ir įrašus, kurie rodomi tinklelyje **Etapai**.

   - **Etapo pavadinimas** – etapo pavadinimas nustatomas pagal etapo datą remiantis sąskaitos faktūros dažnumu.
   - **Etapo data** – data, pagrįsta sąskaitos faktūros dažnumu.
   - **Etapo suma** – apskaičiuojama subrangos sutarties eilutės tarpinę sumą padalijus iš etapų skaičiaus.

Jei subrangos sutarties eilutės vertė yra lauke **Įvertintos mokesčių sumos**, generuojant periodinius etapus ši vertė į kiekvieną etapą įtraukiama po lygiai.

Subrangos sutarties eilutės etatpo suma turi būti lygi subrangos sutarties eilutės vertei. Jei jie nėra lygūs, įvyksta klaida. Ištaisyti klaidą ir patikrinti, ar bendra etapo suma lygi subrangos sutarties eilutės vertei galite sukurdami, redaguodami arba panaikindami etapą ir mokesčių sumas. Atlikę keitimų, puslapį įrašykite ir atnaujinkite, kad įsitikintumėte, jog daugiau klaidų nėra.

## <a name="manually-create-subcontract-line-milestones"></a>Subrangos sutarties eilutės etapų kūrimas rankiniu būdu

Fiksuotos kainos etapus subrangos sutarties eilutėje rankiniu būdu galima sugeneruoti tada, kai jie nėra periodiškai skaidomi. Norėdami subrangos sutarties eilutės etapą sukurti rankiniu būdu, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje pasirinkite **Subrangos sutartys** ir atidarykite subrangos sutartį, su kuria norite dirbti.
2. Atidarykite fiksuotos kainos subrangos eilutę, kuriai norite sukurti etapą.
3. Skirtuko **Subrangos sutarties eilutės etapai** antriniame tinklelyje pasirinkite **+ Naujas subrangos sutarties eilutės etapas**.
4. Puslapyje **Naujas subrangos sutarties eilutės etapas** įveskite reikiamą informaciją remdamiesi toliau pateikta lentele.

    | Laukas | Aprašymas |Funkcinis poveikis|
    | --- | --- |----------------------|
    | Etapo pavadinimas | Etapo pavadinimas. |Jis bus rodomas kaip pirmasis visų peržvalgų stulpelis, remiantis subrangos sutarties eilučių etapais. Pagal šį etapą sukurta tiekėjo sąskaitos faktūros eilutė taip pat kaip numatytąjį tiekėjo sąskaitos faktūros eilutės pavadinimą naudos subrangos sutarties eilutės etapo pavadinimą.|
    | Aprašymas | Etapo aprašas. |Pagal šį etapą sukurta tiekėjo sąskaitos faktūros eilutė taip pat kaip numatytąjį tiekėjo sąskaitos faktūros eilutės aprašą naudos subrangos sutarties eilutės etapo aprašą.|
    | Gairės data | Data, kai automatinio sąskaitų faktūrų kūrimo procesas turi ieškoti šio etapo būsenos ir nustatyti, ar jį įtraukti išrašant sąskaitą faktūrą.| Ši reikšmė bus naudojama kaip numatytoji tiekėjo sąskaitos faktūros eilutės data išrašant šios subrangos sutarties eilutės sąskaitą faktūrą. |
    | Suma | Etapo suma ar vertė, kuriai bus išrašyta klientui skirta sąskaita faktūra. |Ši reikšmė naudojama kaip numatytoji tiekėjo sąskaitos faktūros eilutės suma išrašant šios subrangos sutarties eilutės sąskaitą faktūrą. |
    | Mokestis | Etapui taikoma mokesčių suma.| Ši reikšmė naudojama kaip numatytoji tiekėjo sąskaitos faktūros eilutės mokesčių suma išrašant šios subrangos sutarties eilutės sąskaitą faktūrą. |
    | Suma atskaičius mokestį | Šis tik skaitomas laukas apskaičiuojamas kaip Suma + Mokestis.|Ši reikšmė naudojama kaip numatytoji tiekėjo sąskaitos faktūros eilutės reikšmė išrašant šios subrangos sutarties eilutės sąskaitą faktūrą. |
    | Sąskaitos faktūros būsena | Sukūrus etapą, ši būsena visada nustatoma kaip **Neparengta išrašyti sąskaitos faktūros**.|  Kai būsena yra **Parengta išrašyti sąskaitą faktūrą**, tiekėjo sąskaitos faktūros kūrimo procesas šį etapą įtrauka į tiekėjo sąskaitą faktūrą. |

5. Pasirinkite **Įrašyti ir uždaryti**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
