---
title: Kaip, naudojantis „Web App“, užduočiai priskirti rezervuojamus išteklius?
description: Peržiūrėkite, kaip galite priskirti rezervuojamus išteklius.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 25cf017c53d7db23e467b3b610e2990e56e95cb56bdf9820e427dfeeeb979637
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987716"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Kaip žiniatinklio programoje užduočiai priskirti rezervuotinus išteklius („Project Service“ programa v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ištekliams priskirti užduotį „Project Service“ programoje galima dviem būdais. Išteklius galite rezervuoti kaip komandos narys ir tada priskirti juos užduočiai. Arba, naudodami vaidmenų paskyrimą užduotims atlikti, galite sukurti bendrąjį komandos narį ir tada įvykdyti atsarginius reikalavimus su įvardytais ištekliais.

Atminkite, kad norėdami užduočiai priskirti rezervuotinus išteklius, rezervuotinų išteklių komandos narys privalo turėti pakankamai galimų rezervavimų. Rezervavimo būsena turi būti „Patvirtinti galutinio rezervavimo tipą“ ir „Būsena patvirtinta“. Jei ištekliams rezervuoti nėra pakankamai rezervavimų, Project Service paskyrimą pašalina ir parodo tokį klaidos pranešimą:

*Užduočiai paskirti išteklių nepavyko – nepakanka toliau nurodytiems ištekliams rezervuotų valandų, susietų su šiuo projektu.*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Išteklių rezervavimas būnant komandos nariu ir išteklio priskyrimas užduočiai

Naudodami šį metodą prie projekto komandos pridedate išteklius ir tada projekto grafike ištekliams priskiriate užduotis. Štai kaip galite tai padaryti:
1.  Komandos nario tinklelyje pridėkite naują komandos narį, pasirinkę **„Naujas“**.
2.  Ekrane „Spartusis komandos nario kūrimas“ pasirinkite rezervuotinų išteklių pavadinimą ir nustatykite vaidmenį.
3.  Pasirinkite **„Nuo“** ir **„Iki“** datas.

    > [!div class="mx-imgBorder"] 
    > ![Komandos nario įtraukimo ekrano kopija.](media/FAQ-Resources-to-Tasks2-1.png "Komandos nario įtraukimo ekrano kopija")
 
4.  Pasirinkite vieną iš šių išteklių rezervavimo paskirstymo metodų:
    - **Visas pajėgumo metodas** – rezervuojamas visas išteklių pajėgumas tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.
    - **Pajėgumo procentinės dalies rezervavimo metodas** – rezervuojama išteklių pajėgumo dalis procentais tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.
    - **Tolygiai paskirstomų valandų metodas** – ištekliai rezervuojami nurodytam valandų skaičiui, kiekvienai dienai skirtą laiką tolygiai paskirstant tarp nustatytų pradžios ir pabaigos datų esančiam laikotarpiui
    - **Pirminės apkrovos metodas** – ištekliai rezervuojami į išteklių naudojimo pradžios dieną keliant didžiausią dienos valandų skaičių tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.

    Nesirinkite parinkties **Joks**, nes tuomet ištekliai bus pridėti komandai, bet nebus sukuriami jokie išteklių pajėgumą naudojantys rezervavimai.
5.  Pasirinkite **Įrašyti**.

    Atkreipkite dėmesį, kad turi būti rezervuota pakankamai valandų, kad būtų padengtos pastangų valandos bei datų intervalai, kuriems priskyrėte šiuos išteklius. Jei tai nebus suderinta, užduočiai priskirti resursų nepavyks.

6.  Užduoties darbo paskirstymo struktūroje (WBS), spustelėkite išteklių langelio išplečiamąjį meniu. Tada: 

    1. Pasirinkite **Įtraukti**.
    2. Pasirinkite po parinktimi **„Ištekliai“** esantį išplečiamąjį meniu ir pasirinkite komandos narį, kurį pridėjote aukščiau.
    3. Pasirinkite **Gerai**. Dabar komandos nariui yra priskirta užduotis.

    > [!div class="mx-imgBorder"] 
    > ![Išteklių su WBS įtraukimo ekrano kopija.](media/FAQ-Resources-to-Tasks2-2.png "Išteklių su WBS įtraukimo ekrano kopija")
 
Komandos nario tinklelyje, po parinktimi „Paskirtos valandos“ matysite visas paskirtas valandas. Ši reikšmė bus mažesnė arba lygi rezervuotoms išteklių valandoms. 

> [!div class="mx-imgBorder"] 
> ![Ištekliams priskirtų valandų ekrano kopija.](media/FAQ-Resources-to-Tasks2-3.png "Ištekliams priskirtų valandų ekrano kopija")
 
Ištekliai nebus matomi išplečiamajame meniu, jei užduotis, kurią bandote priskirti ištekliams, prasidės po išteklių rezervavimo pabaigos datos.

Atkreipkite dėmesį – jei ištekliuose yra likusių nepriskirtų pajėgumų, ištekliams galite priskirti daugiau valandų nei jų buvo rezervuota. Tokiu atveju rezervavimams ištekliai bus priskirti tik iš dalies. Galėsite peržiūrėti likusias nepriskirtas užduoties valandas, jei prie darbo paskirstymo struktūros pridėsite stulpelį „Valandos, kurioms nepriskirtas personalas“.

Jei ištekliai yra priskirti toms valandoms, kurioms buvo rezervuoti (rezervuotų valandų skaičius lygus paskirtų valandų skaičiui), mėginant juos priskirti kitoms užduotims, pamatysite tokį klaidos pranešimą:

*Užduočiai paskirti išteklių nepavyko – nepakanka toliau nurodytiems ištekliams rezervuotų valandų, susietų su šiuo projektu.*

Jie nebus rodomi išteklių išplečiamajame sąraše užduočių. Jie nebus rodomi išteklių išplečiamajame sąraše užduotims atlikti.

Jei norite priskirti šiuos išteklius, turite juos pašalinti iš komandos ir tada iš juos įtraukti iš naujo, pasirinkdami bet kokį paskirstymo būdą, išskyrus „Joks“. Sukūrus projektą jie yra įtraukiami į komandą todėl, kad pagal numatytuosius nustatymus projekte yra bent vienas projekto tvirtintojas.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Sukurkite bendrąjį komandos narį, naudojant užduočių vaidmenų paskyrimą.

Šiuo metodu užtikrinama, kad ištekliai rezervuoti užduotims atlikti reikalingam laikotarpiui. Visų pirma, sukuriate vietos rezervavimo ženklo arba bendrinius išteklius, kuriais būtų nurodoma įvardytų išteklių, su kuriais norite dirbti atlikdami užduotis, charakteristika, baigus vaidmenų užduotims sukūrimą sugeneruojant komandą. Štai kaip galite tai padaryti:

1. Darbo paskirstymo struktūros srityje pasirinkite užduotį.
2. Išteklių langelyje pasirinkite išskleidžiamąją piktogramą **„Priskirtas vaidmuo“**.
3. Pasirinkite išskleidžiamąją parinktį **„Vaidmuo“** ir pasirinkite bendrųjų išteklių vaidmenį.
4. Pasirinkite **Gerai**.

    > [!div class="mx-imgBorder"] 
    > ![IWBS naudojimo išteklių įtraukimui ekrano kopija.](media/FAQ-Resources-to-Tasks2-4.png "IWBS naudojimo išteklių įtraukimui ekrano kopija")
 
Baigę vaidmenų priskyrimą užduotims WBS, pasirinkite **„Generuoti projekto komandą“**. Agreguojant užduoties paskyrimus, „Project Service“ programoje sukuriamas mažiausias galimas bendrųjų komandos narių skaičius, remiantis jų vaidmenimis, išteklių paskirstymo organizacijos vienetais ir projekto kalendoriumi.

> [!div class="mx-imgBorder"] 
> ![Projekto komandos generavimo ekrano kopija.](media/FAQ-Resources-to-Tasks2-5.png "Projekto komandos generavimo ekrano kopija")
 
Komandos nario tinklelyje matysite bendrųjų išteklių tipo išteklius, kur bus nurodytas jų vaidmuo ir pareigų pavadinimas. Jei norint pabaigti darbą vaidmeniui reikia dviejų išteklių, naudojantis funkcija „Generuoti komandą“ galima sukurti du komandos narius ir, naudojant pareigų pavadinimą, juos atskirti.

> [!div class="mx-imgBorder"] 
> ![Dviejų bendrųjų išteklių įtraukimo ekrano kopija.](media/FAQ-Resources-to-Tasks2-6.png "Dviejų bendrųjų išteklių įtraukimo ekrano kopija")
 
Galite atidaryti atsarginių išteklių reikalavimus bendrajam komandos nariui, paspausdami nuorodą po parinktimi „Išteklių reikalavimai“.

> [!div class="mx-imgBorder"] 
> ![Atsarginės išteklių įrangos atidarymo ekrano kopija.](media/FAQ-Resources-to-Tasks2-7.png "Atsarginės išteklių įrangos atidarymo ekrano kopija")

Bendriniams ištekliams pasirinkite **„Rezervuoti“** ir tada galėsite naudoti grafiko lentą tam, kad rastumėte ir rezervuotumėte tikrus išteklius. Taip pat galite išteklių vadovui pateikti reikalavimą, kad jis būtų įvykdytas. pasirinkdami **„Pateikti prašymą“**.

Kai bendrieji ištekliai pakeičiami įvardytais ištekliais, bendrieji ištekliai yra pašalinami iš komandos, o jiems paskirtos užduotys paskiriamos įvardytiems ištekliams, kuriais pakeičiami bendrųjų išteklių išteklių reikalavimai.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]