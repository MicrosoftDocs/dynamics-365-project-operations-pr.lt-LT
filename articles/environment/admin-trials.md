---
title: Užsiregistravimas norint naudotis „Project Operations“ bandomosiomis versijomis
description: Šioje temoje pateikiama informacija apie tai, kaip įdiegti „Dynamics 365 Project Operations“ bandomąją versiją.
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e9c0d81591061f0ff01200dd5fd634a4a9ff31e4
ms.sourcegitcommit: 0e5de344f2040075ba431918a4499a80510458d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/25/2021
ms.locfileid: "7418467"
---
# <a name="sign-up-for-project-operations-trials"></a>Užsiregistravimas norint naudotis „Project Operations“ bandomosiomis versijomis 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, „Lite” versijos visuotinis diegimas – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje aiškinama, kaip užsiprenumeruoti peržiūros partnerio pasiūlymą ir įdiegti „Dynamics 365 Project Operations“ aplinką.

Naudodami naują „Project Operations“ bandomąją versiją, galite automatiškai įdiegti bet kurį iš trijų palaikomų visuotinio diegimo scenarijų, prieš tai užpildę klausimyną, pagal kurį nustatomas geriausias visuotinio diegimo metodas. Šioje temoje pateikta informacija apie tai, kaip atlikti toliau nurodytus veiksmus.

- Pasinaudoti bandomosios versijos pasiūlymu.
- Pradėti parengimą.
- Sukonfigūruoti dvigubą rašymą.
- Sužinoti daugiau apie „Project Operations“. 

Toliau esančioje lentelėje pateikta naujo bandomosios versijos pasiūlymo išsami informacija.

| **Pasiūlymo elementas**               | **Informacija**                                  |
|------------------------------|----------------------------------------------|
| Pasiūlymo tipas                   | Šis pasiūlymo tipas yra galimas administratoriaus klientas, todėl norint pasinaudoti reikalingas nuomotojo administratorius. |
| Pasinaudojimas pasiūlymu                    | Vieną kartą vienam nuomotojui                          |
| Pasiūlymo trukmė               | 30 kalendorinių dienų                             |
| Vieno nuomotojo priėmimai       | 1                                            |
| Vartotojų skaičius              | 25                                           |
| Plėtinys                    | 1 plėtinys, 30 kalendorių dienų               |
| Bandomųjų aplinkų skaičius | 3                                            |


## <a name="admin-trial-details"></a>Išsami administratoriaus bandomosios versijos informacija
Toliau esančioje lentelėje pateikta išsami bandomosios versijos informacija ir kaip ji taikoma kiekvienam visuotinio diegimo tipui.

| **Elementas**                      | **„Lite“**                                     | **Nelaikomos medžiagos** | **Laikomos medžiagos** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Pateikti sąrankos duomenys           | Taip                                          | Taip                       | Taip (USSI)            |
| Sandorio duomenys            | No                                           | No                        | No                    |
| Parengimo laikas minutėmis  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Būtinosios sąlygos
Toliau nurodytos būtinosios sąlygos yra reikalingos norint visuotinai įdiegti „Dynamics 365 Project Operations“ bandomąją versiją.

- Užsiregistruokite [Dynamics 365 Project Operations – peržiūros versijos bandomajai versijai](https://www.aka.ms/try-po).
- Vartotojas, kuris įdiegia peržiūros versiją, turi turėti „Azure“ kliento visuotinio administratoriaus teises.

> [!IMPORTANT]
> Šią užduotį turi atlikti tik vienas organizacijos asmuo – nuomotojo administratorius. Jei nesate šio leidimo prenumeratorius, palaukite, kol jūsų organizacija bus užregistruota ir gausite vartotojo kredencialus.

### <a name="dynamics-365-project-operations---preview-trial"></a>„Dynamics 365 Project Operations“ – peržiūros versijos bandomoji versija 

Prieš pradėdami prisijunkite prie naršyklės naudodami vartotojo darbo paskyrą tame nuomotoje, kuriame norite peržiūrėti „Project Operations“.

1. Panaudokite pirmąjį pasiūlymo kodą, skirtą **„Dynamics 365 Project Operations“ – peržiūros versijos bandomajai versijai**, įklijuodami jį į naršyklės URL.

    ![Pasinaudoti pasiūlymu](./media/16RedeemFirstOfferNew.png)

2. Patvirtinkite užsakymą.

    ![Patvirtinkite užsakymą](./media/17ConfirmOrderNew.png)

  Pamatysite, kad patvirtinimo pasiūlymu buvo sėkmingai pasinaudota.

   ![Patvirtinimas](./media/18OrderConfirmationNew.png)

  Būsite nukreipti į [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Klausimynas ir parengimas

1.  Eikite į [„Power Platform“ administravimo centrą](https://admin.powerplatform.com/projectoperationstrial) ir užpildykite klausimyną.  
2.  Peržiūrėkite rekomenduojamą visuotinio diegimo tipą ir pasirinkite **Pradėti sąranką**, kad pradėtumėte parengimą.
3.  Peržiūrėkite sąlygas ir pasirinkite **Pradėti**.

   Prasidėjus parengimui būsite nukreipti į „Power Platform“ administravimo centro aplinkų sąrašą. Vykstant parengimui jūsų aplinkos būsena bus **PreparingInstance**.
 
  Parengimui pasibaigus jūsų aplinkos būsena bus **Parengta**.
 
4.  Kai parengimas bus baigtas, pasirinkite atitinkamą „Microsoft Dataverse“ URL ir „Finance and Operations“ programų URL, kad patikrintumėte visuotinį diegimą.

## <a name="demo-data-installation"></a>Demonstracinių duomenų įdiegimas

Pasinaudodami toliau pateiktais saitais, pasiekite nelaikomų medžiagų ir „Lite“ visuotinio diegimo scenarijų demonstracinių duomenų paketus. 
- [Nelaikomų medžiagų demonstraciniai duomenys](resource-apply-pro-setup-config-data.md)
- [„Lite“ demonstraciniai duomenys](lite-apply-demo-setup-config-data.md)

## <a name="configuring-dual-write"></a>Dvigubo rašymo konfigūravimas
Naudodami tik nelaikomų medžiagų visuotinį diegimą, sukonfigūruokite dvigubo rašymo susiejimus. Daugiau informacijos žr. [„Project Operations“ dvigubo rašymo schemų versijas](resource-dual-write-maps.md).

## <a name="assign-licenses"></a>Licencijų priskyrimas

Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Microsoft 365 Portal“.

1. Eikite į [„Microsoft 365“ administravimo centrą](https://portal.office.com/) ir priskirkite licencijas vartotojams.

   ![Administravimo centro pagrindinis puslapis](./media/14AdminPortal.png)

2. Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.

   ![Licencijų priskyrimas](./media/15AssignLicenses.png)

3. Patikrinkite, ar pasirinkta **„Dynamics 365 Project Operations“** peržiūros versija, tada pasirinkite **Įrašyti keitimus**.

## <a name="additional-resources"></a>Papildomi ištekliai

Toliau nurodytuose ištekliuose pateiktos naudingos gairės pradėjus veiklos ciklą „Project Operations“:

- [Vaizdo įrašų serija – „Project Operations“ apžvalga, išsamus funkcijų pristatymas ir veiksmų planas](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Visuotinio diegimo tipo nustatymas](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Ką daryti, jei savo „Finance and Operations“ programų aplinkoje reikalauju ALM arba ELM?

- Partnerius, reikalaujančius visų aplinkos ciklo valdymo galimybių, žr. temoje [Partnerio smėlio dėžės licencijos užklausa](https://experience.dynamics.com/requestlicense) ir peržiūrėkite naują partnerio pasiūlymą. 
- Partnerius, kuriems reikalinga daugiau informacijos apie vidines naudojimo teises, žr. straipsnyje [Vidinių naudojimo teisių debesies ir programinės įrangos pranašumas (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Ar galiu bandomąja versija naudotis ilgiau nei 30 dienų?
Norėdami prailginti bandomosios versijos laikotarpį, atlikite toliau nurodytus veiksmus.

1. **„Microsoft 365“ administravimo centre** eikite į **Atsiskaitymas** > **Jūsų produktai**.
2. Pasirinkite **„Dynamics 365 Project Operations (CE)“ – peržiūros versijos bandomąją versiją**.
3. Dalyje **Galiojimo pabaigos data** pasirinkite **Nustatyti vėlesnę datą**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Ar iš „Lite“ visuotinio diegimo versijos galiu atnaujinti į ištekliais / nelaikomų medžiagų scenarijumi pagrįstą visuotinį diegimą?
Šiuo metu aplinkos atnaujinimas iš „Lite“ versijos į nelaikomomis medžiagomis pagrįstą visuotinį diegimą nepalaikomas.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Ar galiu pasiekti savo finansų aplinkų „Lifecycle Services“ (LCS)?  
Ne. Šių bandomųjų versijų visuotinis diegimas tvarkomas „Power Platform“ administravimo centre. Prieiga prie finansų aplinkos yra apribota.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Ar galiu bandomąją versiją įdiegti į esamą aplinką?
Jei turite esamą aplinką, įdiegti „Lite“ visuotinį diegimą į esamą pardavimo „Dataverse“ aplinką galėsite apsilankę „Power Platform“ administravimo centre.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
