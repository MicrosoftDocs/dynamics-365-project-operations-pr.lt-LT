---
title: Įmonės vidaus kliento ir tiekėjo sąskaitų faktūrų kūrimas
description: Šioje temoje pateikiama informacija, kaip kurti įmonės vidaus klientų ir tiekėjų sąskaitas faktūras.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 92d08537fe0c2a1deba486974db53e7ebe1ff2d8
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948405"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Įmonės vidaus kliento ir tiekėjo sąskaitų faktūrų kūrimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projekto apskaitininkas skolinimo juridiniame objekte sukuria įmonės vidaus kliento sąskaitą faktūrą, kurioje nurodomos projekto išlaidos, perduodamos skolinimosi juridiniam objektui. Įmonės vidaus kliento sąskaitą faktūrą patvirtinus ir užregistravus, skolinimo juridinis objektas įmonės vidaus sąskaitą faktūrą siunčia skolinimosi juridiniam objektui.

Skolinimo juridinio objekto projekto apskaitininkas gali nustatyti paketinį procesą, kad įmonės vidaus sąskaitos faktūros būtų generuojamos reguliariai. Kad būtų sukurtos paketinės įmonės vidaus sąskaitos faktūros, projekto apskaitininkas nurodo kriterijus, pvz., konkrečius projektus.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Neautomatinis įmonės vidaus klientų sąskaitų faktūrų, skirtų projekto operacijoms, kūrimas 

Šią procedūrą naudokite, jei norite neautomatiškai kurti įmonės vidaus klientų sąskaitas faktūras, skirtas projekto operacijoms. Ieškokite valandų, kurias užregistravo su projektais dirbantys darbuotojai skolinimosi juridiniuose objektuose, ir išlaidų, kurias patyrė jūsų juridinis objektas dėl skolinimosi juridinių objektų. Galite ieškoti pagal juridinio objekto pavadinimą, projekto sutarties numerį, projekto numerį, datos diapazoną arba pagal bet kokį šių parinkčių derinį. Ieškos rezultatuose pasirinkite operacijas, kurias norite įtraukti į įmonės vidaus sąskaitą faktūrą. 

Skolinančiajame juridiniame subjekte reikia atlikti toliau nurodytus veiksmus. 

1. Programoje „Dynamics 365 Finance“ eikite į **Projektų valdymas ir apskaita** > **Projekto sąskaitos faktūros** > **Vidinių įmonių klientų SF**. **Vidinių įmonių klientų SF** sąrašo puslapyje esančioje veiksmų srityje pasirinkite **Naujas.**
2. Puslapyje **Kurti vidinės įmonės SF**, lauke **Juridinis objektas**, pasirinkite skolinimosi juridinį objektą.
3. Pasirinktinai: įveskite konkrečios projekto sutarties ir projekto numerius.
4. Susiaurinkite iešką pasirinkdami datų diapazoną. Laukuose **Pradžios data** ir **Pabaigos data** įveskite konkrečias datas. Ieškos rezultatuose rodomos tik tos įmonės vidaus operacijos, kurios užregistruotos šio datų diapazono ribose.
5. Nustatykite **išplėstinio projekto žurnalo eilutės parametrą** kaip **Taip** ir pasirinkite **Ieškoti**.
6. Ieškos rezultatuose pasirinkite operacijas, kurias norite įtraukti į įmonės vidaus sąskaitos faktūros pasiūlymą, tada pasirinkite **Gerai**.
7. **Vidinių įmonių klientų SF** puslapyje rodomos iš ieškos rezultatų pasirinktos įmonės vidaus projekto operacijos. Jei norite modifikuoti operacijas prieš išsiųsdami sąskaitą faktūrą skolinimosi juridiniam objektui, atlikite toliau nurodytus veiksmus:
  
    1. Puslapyje **Vidinės įmonės kliento sąskaita faktūra** atidarykite sąskaitos faktūros išsamią informaciją ir pasirinkite **Įtraukti eilutę**.
    2. Jei norite eilutę pašalinti, pažymėkite ją, tada pasirinkite **Šalinti**.
    3. Peržiūrėdami sąskaitos faktūros eilutės išsamią informaciją, galite matyti komentarus, priežastis, finansines dimensijas ir kitą informaciją.
    
8. Jei įmonės vidaus kliento sąskaitą faktūrą norite užregistruoti, veiksmų srityje pasirinkite **Registruoti**.

> [!NOTE]
> Jei jūsų organizacija reikalauja, kad prieš užregistruojant įmonės vidaus sąskaitos faktūros turi būti peržiūrėtos, sistemos administratorius gali nustatyti įmonės vidaus sąskaitų faktūrų darbo eigą. Jei įmonės vidaus sąskaitų faktūrų darbo eiga nenustatyta, įmonės vidaus sąskaitą faktūrą galite užregistruoti.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Įmonės vidaus sąskaitų faktūrų paketinės užduoties kūrimas

Vienu metu galite sukurti keletą įmonės vidaus sąskaitų faktūrų visiems skolinimosi juridiniams objektams. Naudodami ieškos funkcijas galite ieškoti, pvz., visų operacijų, kurias užregistravo pasiskolinti darbuotojai, ir susijusių su projektais, kuriuos valdo kiti juridiniai objektai. Tada kiekvienam skolinimosi juridiniam objektui galite sukurti įmonės vidaus sąskaitą faktūrą, skirtą operacijoms, kurios nurodytos ieškos rezultatuose.

1. Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Projekto sąskaitos faktūros** > **Kurti vidinių įmonių klientų SF**.
2. Puslapyje **Kurti vidinių įmonių klientų SF**, lauke **Įmonė**, pasirinkite juridinį objektą, kuriam kurti sąskaitą faktūrą. Jei nepasirinksite įmonės, bus rodomos visų skolinimosi juridinių objektų visos operacijos, atitinkančios ieškos kriterijus.
3. Dalyje **Kurti po vieną SF** pasirinkite, ar kurti įmonės vidaus operacijų sąskaitą faktūrą pagal projektą ar pagal skolinimosi juridinį objektą.
4. Pasirinktinai: jei norite pasirinkti konkretų projektą ir projekto sutartį, kad būtų sukurtos įmonės vidaus sąskaitos faktūros, spustelėkite **Pasirinkti**. Puslapyje **Užklausa**, lauke **Kriterijai**, pasirinkite projekto sutartį, projekto numerį (arba abu), o tada pasirinkite **Gerai**.
5. Skirtuke **Paketas** nustatykite paketinį procesą, kad įmonės vidaus sąskaitos faktūros būtų kuriamos reguliariai. Daugiau informacijos žr. [Paketinio apdorojimo užduoties pateikimas naudojant formą](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Jei įmonės vidaus sąskaitas faktūras norite užregistruoti, veiksmų srityje pasirinkite **Registruoti**.

> [!NOTE]
> Jei jūsų organizacija reikalauja prieš užregistruojant įmonės vidaus sąskaitas faktūras peržiūrėti, sistemos administratorius gali nustatyti įmonės vidaus sąskaitų faktūrų darbo eigą. Jei įmonės vidaus sąskaitų faktūrų darbo eiga nenustatyta, įmonės vidaus sąskaitas faktūras galite užregistruoti.

## <a name="post-the-intercompany-vendor-invoice"></a>Įmonės vidaus tiekėjo sąskaitos faktūros registravimas

Užregistravus atitinkamą įmonės vidaus kliento sąskaitą faktūrą, skolinimosi juridinio objekto projekto apskaitininkas gali peržiūrėti laukiančias įmonės vidaus tiekėjo sąskaitas faktūras. Finansų srityje, skolinimosi juridiniame objekte, eikite į **Mokėtinos sumos** > **Sąskaitos faktūros** > **Laukianti tiekėjo SF**. Laukiančios sąskaitos faktūros numeris sutaps su įmonės vidaus kliento sąskaitos faktūros numeriu. Patikrinkite, ar sąskaita faktūra teisinga, o tada ją užregistruokite. Įmonės vidaus tiekėjo sąskaitą faktūrą užregistravus, sukuriama projekto antrinės knygos ir didžiosios knygos operacija, atspindinti operacijos išlaidas skolinimosi juridiniame objekte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
