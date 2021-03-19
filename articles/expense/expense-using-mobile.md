---
title: Mobilioji išlaidų programėlė
description: Šioje temoje pateikiama informacija apie išlaidų valdymą mobiliojoje darbo srityje.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 01df30bf48fa9118771b87363d0418eb6b49ecea
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499906"
---
# <a name="mobile-expense-app"></a>Mobilioji išlaidų programėlė

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Šioje temoje pateikiama informacija apie **išlaidų valdymą** mobiliojoje darbo srityje. Ši darbo sritis leidžia vartotojams fiksuoti ir nusiųsti kvitą, kad ją vėliau galėtų pridėti prie išlaidų ataskaitos. Vartotojai taip pat gali greitai sukurti išlaidų eilutę naudodami pridėtą kvitą ir kurti bei valdyti savo išlaidų ataskaitas. Be to, tvirtintojai gali naudoti **išlaidų valdymo** mobiliąją darbo sritį, kad galėtų peržiūrėti jiems priskirtas išlaidų ataskaitas ir patvirtinti arba atmesti tas išlaidų ataskaitas.

Ši mobilioji darbo sritis skirta naudoti su „Dynamics 365“ bendrųjų operacijų mobiliųjų įrenginių programėle.

Daugeliui organizacijų reikia pridėti kvito kopiją prie su kelionėmis susijusios arba su verslu susijusios išlaidų ataskaitos, kurią darbuotojas pateikia dėl išlaidų kompensavimo. **Išlaidų valdymo** mobilioji darbo sritis leidžia vartotojams greitai sukurti naujas išlaidų eilutes pasirinktoje mobiliajame įrenginyje pagal pridėtą kvito nuotrauką. Arba vartotojai gali užfiksuoti kvito nuotrauką, tada pridėti ją prie išlaidų ataskaitos vėliau. Darbuotojai taip pat gali kurti ir valdyti savo išlaidų ataskaitas, o tada juos patvirtinti ir kompensuoti savo mobiliuoju prietaisu.

Tiksliau sakant, **išlaidų valdymo** mobilioji darbo sritis leidžia vartotojams atlikti šias užduotis:

- Nufotografuokite kvitą. Nusiųskite kvito nuotrauką ir pridėkite ją prie išlaidų ataskaitos vėliau.
- Įkelkite failą kaip užfiksuotą kvitą. Tada galite pridėti tą failą prie išlaidų ataskaitos vėliau.
- Sukurkite naują išlaidų eilutę naudodami pridėtą kvitą. Tada galite įtraukti eilutės elementą į išlaidų ataskaitą vėliau ir pateikti jį tvirtinti ir kompensuoti.

Taip pat galite naudoti šias funkcijas:

- Sukurkite naują išlaidų ataskaitą.
- Kredito kortelių operacijas ir kitas anksčiau sukurtas išlaidas pridėkite prie išlaidų ataskaitos.
- Sukurkite naujas išlaidų ataskaitos išlaidas.
- Pridėkite kvitą bet kuriai išlaidų ataskaitos sąskaita, atsižvelgiant į kvito nuotrauką arba įkeliant failą kaip užfiksuotą kvitą.
- Atsižvelgdami į įmonės išlaidų strategiją, įtraukite svečių sąrašą į išlaidas.
- Atsižvelgdami į įmonės išlaidų strategiją, detaliai detalizuoja išlaidas.
- Pateikite patvirtinimo ir kompensavimo išlaidų ataskaitą.
- Patvirtinkite arba atmeskite išlaidų ataskaitas, kurioms esate priskirtas tvirtintojas.

## <a name="prerequisites"></a>Būtinosios sąlygos
Būtinosios sąlygos skiriasi atsižvelgiant į versiją, įdiegtą organizacijoje.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Būtinosios sąlygos, jei naudojama „Dynamics 365 Finance“ 
Jei organizacijoje įdiegta „Finance“, sistemos administratorius turi publikuoti mobiliąją darbo sritį **Išlaidų valdymas**. 

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Būtinosios sąlygos, jei naudojama 1611 versija su 3 arba naujesnės versijos platforma
Jei organizacijoje įdiegta 1611 versija su 3 arba naujesnės versijos platforma, sistemos administratorius turi įvykdyti toliau pateikiamas būtinąsias sąlygas. 

<table>
<thead>
<tr class="header">
<th>Būtinoji sąlyga</th>
<th>Vaidmuo</th>
<th>Aprašo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Įdiegti KB 4019015.</td>
<td>Sistemos administratorius</td>
<td>KB 4019015 yra X++ naujinimas arba metaduomenų karštosios pataisos, kuriose yra <strong>Išlaidš valdymas</strong> mobilioji darbo sritis. Norėdamas įdiegti KB 4019015, sistemos administratorius turi atlikti toliau pateikiamus veiksmus.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Atsisiųsti atnaujinimus iš „Lifecycle Services“</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Įdiegti metaduomenų karštąsias pataisas</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Sukurkite įdiegiamą paketą,</a> kuriame yra modeliai <strong>„ApplicationSuite“</strong> ir <strong>„ExpenseMobile“</strong>, ir įkelkite įdiegiamą paketą į LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Pritaikyti įdiegiamą paketą</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publikuokite <strong>Išlaidų valdymo</strong> mobiliąja darbo sritį.</td>
<td>Sistemos administratorius</td>
<td>Žr. <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiliosios darbo srities publikavimas</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Atsisiųskite ir įdiekite „Dynamics 365 Unified Ops“ mobiliųjų įrenginių programėlę
Atsisiųskite ir įdiekite „Dynamics 365 Unified Ops“ mobiliųjų įrenginių programėlę:

- [Skirta telefonams „Android“](https://go.microsoft.com/fwlink/?linkid=850662)
- [Skirta telefonams „iPhone“](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prisijungimas prie mobiliųjų įrenginių programėlės
1. Mobiliajame įrenginyje paleiskite mobiliųjų įrenginių programėlę.
2. Įveskite savo „Dynamics 365“ URL.
4. Pirmą kartą prisijungdami, būsite paraginti įvesti vartotojo vardą ir slaptažodį. Įveskite savo kredencialus.
5. Kai prisijungsite, bus rodomos galimos jūsų įmonės darbo sritys. Jei jūsų sistemos administratorius vėliau publikuos naują darbo sritį, turėsite atnaujinti mobiliųjų darbo sričių sąrašą.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Fiksuoti kvitą naudojant mobiliąsias išlaidų valdymo darbo sritis

1. Mobiliajame įrenginyje atidarykite **išlaidų valdymo** darbo sritį.
2. Pasirinkite **Fiksuoti kvitą**.
3. Pasirinkite **Fotografuoti** arba **Pasirinkti vaizdą**.
4. Atlikite vieną iš šių veiksmų:

   - Jei pažymėjote **Fotografuoti**, atlikite šiuos veiksmus:

      1. Mobiliajame įrenginyje atsidarys kamera, kad galėtumėte nufotografuoti kvito nuotrauką. 
      2. Nufotografavę pasirinkite **Gerai**, kad patvirtintumėte nuotrauką.
      3. Pasirinktinai: įveskite nuotraukos pavadinimą ir įveskite visas pastabas.

    - Jei pažymėjote **Pasirinkti vaizdą**, atlikite šiuos veiksmus:

        1. Sąraše pasirinkite vaizdą.
        2. Pasirinktinai: įveskite vaizdo pavadinimą ir įveskite visas pastabas.

5. Pasirinkite **Atlikta**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Sparčiai įveskite išlaidas naudojant mobiliąsias išlaidų valdymo darbo sritis

1. Mobiliajame įrenginyje atidarykite **išlaidų valdymo** darbo sritį.
2. Pasirinkite **Spartus išlaidų įvedimas**.
3. Pažymėkite išlaidų kategoriją. Matysite išlaidų kategorijų, kurios įkeltos į programėlę ir skirtos naudoti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 elementų, bet kūrėjas gali šį skaičių pakeisti. Daugiau informacijos kūrėjai gali rasti skyriuje [Mobilioji platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jei jūsų kategorijos sąraše nėra, pasirinkite **Ieskoti**, kad atliktumėte iešką internete. Ieškokite pagal išlaidų kategoriją arba pereikite prie ieškos pagal išlaidų tipą.
4. Įveskite išlaidų operacijos datą.
5. Pasirinktinai: įveskite prekybininko sąskaitą.
6. Įveskite išlaidos sumą.
7. Pasirinkite išlaidų valiutą. Matysite valiutos kodų, kurie įkelti į programėlę ir skirti naudoti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 400 valiutų, bet kūrėjas gali šį skaičių pakeisti. Daugiau informacijos kūrėjai gali rasti skyriuje [Mobilioji platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jei jūsų valiutos sąraše nėra, pasirinkite **Ieskoti**, kad atliktumėte iešką internete. Ieškokite pagal valiutą arba pereikite prie ieškos pagal pavadinimą.
8. Pasirinkite **Fotografuoti** arba **Pasirinkti vaizdą**.
9. Atlikite vieną iš šių veiksmų:

    - Jei pasirinkote **Nufotografuoti**, mobiliajame įrenginyje atsidarys kamera, kad galėtumėte nufotografuoti kvito nuotrauką. Nufotografavę pasirinkite **Gerai**, kad patvirtintumėte nuotrauką.
    - Jei pažymėjote **Pasirinkti vaizdą**, sąraše pasirinkite vaizdą.

10. Pasirinkite **Atlikta**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Išlaidų ataskaitos patvirtinimas naudojant išlaidų valdymo mobiliąją darbo sritį (jei naudojate liepos 2017 naujinimą)

1. Mobiliajame įrenginyje atidarykite **išlaidų valdymo** darbo sritį.
2. **Išlaidų patvirtinimuose** pateikiamas jums priskirtų išlaidų ataskaitų skaičius patvirtinimui. Numeris atnaujinamas maždaug kas 30 minučių. Pažymėkite **išlaidų patvirtinimai**.

    Rodomas išlaidų ataskaitų, kurios priskirtos jums patvirtinimui, sąrašas.
    
3. Pažymėkite išlaidų ataskaitą ir peržiūrėkite jos išsamią informaciją.
4. Pažymėkite išlaidas ir peržiūrėkite jų išsamią informaciją. Informacijoje, kuri rodoma kaip sąskaita, yra bet koks kvitas, svečias ir išsami informacija.
5. Puslapio **Išlaidų ataskaita** gale pažymėkite, kad patvirtintumėte arba atmestumėte išlaidų ataskaitą.
6. Įveskite visus patvirtinimo veiksmo komentarus.
7. Pasirinkite **Atlikta**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Naujos išlaidų ataskaitos kūrimas ir jos pateikimas patvirtinimui naudojant išlaidų valdymo mobiliąją darbo sritį (jei naudojate liepos 2017 naujinimą)

1. Mobiliajame įrenginyje atidarykite **išlaidų valdymo** darbo sritį.
2. Pasirinkite **Išlaidų įvedimas**.
3. Pasirinkite **Naują ataskaitą** arba sąraše pažymėkite esamą išlaidų ataskaitą.
4. Norėdami gauti naujų išlaidų ataskaitų, įveskite tikslą ir bet kokią turimą papildomą informaciją. Ši informacija skiriasi atsižvelgiant į tai, kaip jūsų įmonei sukonfigūruotas išlaidų valdymas.
5. Pasirinkite **Atlikta**.
6. Norėdami įtraukti esamas išlaidas, pvz., kredito kortelių operacijas, į išlaidų ataskaitą, pažymėkite **Pridėti**.
7. Sąraše pažymėkite vieną arba kelias išlaidas.
8. Pasirinkite **Atlikta**.
9. Jei norite įtraukti naują išlaidų ataskaitą, pažymėkite **Naujos išlaidos**.
10. Pažymėkite išlaidų kategoriją. Matysite išlaidų kategorijų, kurios įkeltos į programėlę ir skirtos naudoti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 elementų, bet kūrėjas gali šį skaičių pakeisti. Daugiau informacijos kūrėjai gali rasti skyriuje [Mobilioji platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jei jūsų kategorijos sąraše nėra, pasirinkite **Ieskoti**, kad atliktumėte iešką internete. Ieškokite pagal išlaidų kategoriją arba pereikite prie ieškos pagal išlaidų tipą.
11. Pasirinktinai: įveskite prekybininko sąskaitą.
12. Įveskite išlaidų operacijos datą.
13. Įveskite išlaidos sumą.
14. Pasirinkite išlaidų valiutą. Matysite valiutos kodų, kurie įkelti į programėlę ir skirti naudoti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 400 valiutų, bet kūrėjas gali šį skaičių pakeisti. Daugiau informacijos kūrėjai gali rasti skyriuje [Mobilioji platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jei jūsų valiutos sąraše nėra, pasirinkite **Ieskoti**, kad atliktumėte iešką internete. Ieškokite pagal valiutą arba pereikite prie ieškos pagal pavadinimą.
15. Pasirinkite **Atlikta**.
16. Norėdami įtraukti daugiau informacijos į išlaidas, pažymėkite **Įtraukti daugiau informacijos**. Galimi laukai priklauso nuo jūsų įmonės išlaidų valdymo konfigūracijos.
17. Jei įmonės strategijoje reikia išlaidų gavimo, pasirinkite **Kvitai** ir atlikite šiuos veiksmus:

    1. Pasirinkite **Fiksuoti kvitą** arba **Pridėti kvitą**.
    2. Atlikite vieną iš šių veiksmų:

        - Jei pažymėjote **Pasirinkti kvitą**, atlikite šiuos veiksmus:

            1. Pasirinkite **Fotografuoti** arba **Pasirinkti vaizdą**.
            2. Atlikite vieną iš šių veiksmų:

                - Jei pažymėjote **Fotografuoti**, atlikite šiuos veiksmus:

                    1. Mobiliajame įrenginyje atsidarys kamera, kad galėtumėte nufotografuoti kvito nuotrauką. Nufotografavę pasirinkite **Gerai**, kad patvirtintumėte nuotrauką.
                    2. Pasirinktinai: įveskite nuotraukos pavadinimą ir įveskite visas pastabas.

                - Jei pažymėjote **Pasirinkti vaizdą**, atlikite šiuos veiksmus:

                    1. Sąraše pasirinkite vaizdą.
                    2. Pasirinktinai: įveskite vaizdo pavadinimą ir įveskite visas pastabas.

            3.  Pasirinkite **Atlikta**.

        - Jei pažymėjote **Pridėti kvitą**, atlikite šiuos veiksmus:

            1.  Sąraše pažymėkite vieną arba kelis vaizdus.
            2.  Pasirinkite **Atlikta**.

    3. Norėdami grįžti prie išlaidų išsamios informacijos, spustelėkite mygtuką **Atgal**.

18. Jei įmonės strategijoje reikia išlaidoms reikia svečių, pasirinkite **Svečiai** ir atlikite šiuos veiksmus:

    1. Pažymėkite **Svečiai**, **Ankstesni svečiai** arba **Bendradarbiai**.
    2. Atlikite vieną iš šių veiksmų:

        - Jei pažymėjote **Svečiai**, atlikite šiuos veiksmus:

            1. Įveskite svečio pavadinimą.
            2. Pasirinktinis: įveskite svečio organizaciją ir (arba) šalį.
            3. Pasirinktinis: Įveskite svečio titulą.
            4. Pasirinkite **Atlikta**.

        - Jei pažymėjote **Ankstesnis svečias**, atlikite šiuos veiksmus:

            1. Sąraše pažymėkite vieną arba kelis ankstesnius svečius. Matote ankstesnių Svečių, kuriuos įtraukėte į ankstesnes išlaidų ataskaitas, įkeliamas į programą, kad būtų galima naudoti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 elementų, bet kūrėjas gali šį skaičių pakeisti. Daugiau informacijos kūrėjai gali rasti skyriuje [Mobilioji platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jei jūsų ankstesnio svečio sąraše nėra, pasirinkite **Ieskoti**, kad atliktumėte iešką internete. Ieškokite pagal pavadinimą arba pereikite prie ieškos pagal organizaciją, šalį ar titulą.
            2. Pasirinkite **Atlikta**.

        - Jei pažymėjote **Bendradarbiai**, atlikite šiuos veiksmus:

            1. Sąraše pažymėkite vieną arba kelis bendradarbius. Matysite bendradarbių, kurie įkelti į programėlę naudoti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 elementų, bet kūrėjas gali šį skaičių pakeisti. Daugiau informacijos kūrėjai gali rasti skyriuje [Mobilioji platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jei jūsų bendradarbio sąraše nėra, pasirinkite **Ieskoti**, kad atliktumėte iešką internete. Ieškokite pagal pavadinimą arba pereikite prie ieškos pagal įmonę ar titulą.
            2. Pasirinkite **Atlikta**.

    3. Norėdami grįžti prie išlaidų išsamios informacijos, spustelėkite mygtuką **Atgal**.

19. Jei įmonės strategijoje apibrėžiama, kad išlaidos turi būti detalizuojamos, pasirinkite **Detalizuoti** ir atlikite šiuos veiksmus:

    1. Pažymėkite pirmąją datą, kad ją detalizuotumėte.
    2. Pažymėkite **Įtraukti detalizavimą**.
    3. Pažymėkite išlaidų detalizavimo papildomą kategoriją. Matysite išlaidų papildomų kategorijų, kurios įkeltos į programėlę ir skirtos naudoti neprisijungus, sąrašą. Pagal numatytuosius parametrus įkeliama 50 elementų, bet kūrėjas gali šį skaičių pakeisti. Daugiau informacijos kūrėjai gali rasti skyriuje [Mobilioji platforma](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Jei jūsų papildomos kategorijos sąraše nėra, pasirinkite **Ieskoti**, kad atliktumėte iešką internete. Ieškoti pagal išlaidų papildomos kategorijos pavadinimą.
    4. Įveskite operacijos sumą, skirtą detalizavimui.
    5. Jei reikia, redaguokite operacijos datą.
    6. Pasirinkite **Atlikta**.
    7. Pakartokite ankstesnius veiksmus, kol baigsite įtraukti visus pasirinktos datos detalizavimus.
    8. Jei reikia papildomų dienų, galite pažymėti **Kopijuoti į kitą dieną**, kad nukopijuotumėte detalizavimus į kitą dieną. Arba galite pažymėti datą detalizavimui ir įtraukti detalizavimus, kaip tai padarėte pirmą dieną.
    9. Baigę detalizuoti išlaidas, pažymėkite mygtuką **Atgal**, kad grįžtumėte į išsamią išlaidų informaciją.

20. Norėdami grįžti prie puslapio **Išlaidų ataskaita**, spustelėkite mygtuką **Atgal**.
21. Atlikite ankstesnius veiksmus, kol įtrauksite visas išlaidas.
22. Pasirinkite **Pateikti**.
23. Įveskite komentarus tvirtintojui.
24. Pasirinkite **Atlikta**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
