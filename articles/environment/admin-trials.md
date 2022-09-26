---
title: Užsiregistravimas norint naudotis „Project Operations“ bandomosiomis versijomis
description: Šiame straipsnyje pateikiama informacija apie tai, kaip įdiegti bandomąją Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 60790d83d5fcc8c75fef8eac2877d1ca14a761f2
ms.sourcegitcommit: 385081ecc839d7d4a557eda2bb1578ca073f7e41
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/19/2022
ms.locfileid: "9528030"
---
# <a name="sign-up-for-project-operations-trials"></a>Užsiregistravimas norint naudotis „Project Operations“ bandomosiomis versijomis 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, „Lite” versijos visuotinis diegimas – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_ 



Šiame straipsnyje paaiškinama, kaip užsiprenumeruoti peržiūros partnerio pasiūlymą ir įdiegti Dynamics 365 Project Operations aplinką.

Naudodami naują „Project Operations“ bandomąją versiją, galite automatiškai įdiegti bet kurį iš trijų palaikomų visuotinio diegimo scenarijų, prieš tai užpildę klausimyną, pagal kurį nustatomas geriausias visuotinio diegimo metodas. Šiame straipsnyje pateikiama informacija apie tai, kaip:

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
 
  Kai parengimas baigtas, jūsų aplinkos būsena yra **Paruošta**. Aplinkos parengimas apima demonstracinių duomenų diegimą.
 
4.  Pasirinkite atitinkamą Microsoft Dataverse URL ir finansavimo bei operacijų programų URL, kad patvirtintumėte diegimą.

## <a name="configuring-dual-write"></a>Dvigubo rašymo konfigūravimas
- Norėdami konfigūruoti saugos vaidmenis dvigubam rašymui, žiūrėkite ["Project Operations" saugos parametrų naujinimas Dataverse](resource-provision-new-environment.md#update-security-settings-on-project-operations-on-dataverse).
- Norėdami pasiekti dvigubo rašymo konfigūraciją, eikite į "Finance and Operations" egzempliorių, tada eikite į **"Data Management** > **Dual Write"**.
- Norėdami konfigūruoti dvigubo rašymo žemėlapius, žiūrėkite ["Project Operations" dvigubo rašymo žemėlapių vykdymas](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Licencijų priskyrimas

Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Microsoft 365“ portalo.

1. Eikite į [Microsoft 365 administravimo centrą](https://portal.office.com/) ir priskirkite licencijas savo vartotojams.

   ![Administravimo centro pagrindinis puslapis](./media/14AdminPortal.png)

2. Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.

   ![Licencijų priskyrimas](./media/15AssignLicenses.png)

3. Patikrinkite, ar pasirinkta **„Dynamics 365 Project Operations“** peržiūros versija, tada pasirinkite **Įrašyti keitimus**.

## <a name="additional-resources"></a>Papildomi ištekliai

Toliau nurodytuose ištekliuose pateiktos naudingos gairės pradėjus veiklos ciklą „Project Operations“:

- [Vaizdo įrašų serija – „Project Operations“ apžvalga, išsamus funkcijų pristatymas ir veiksmų planas](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/training/modules/examine-dynamics-365-project-operations/)
- [Visuotinio diegimo tipo nustatymas](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Ką daryti, jei mano finansų ir operacijų programų aplinkai reikia ALM arba ELM?

- Partnerius, reikalaujančius visų aplinkos ciklo valdymo galimybių, žr. temoje [Partnerio smėlio dėžės licencijos užklausa](https://experience.dynamics.com/requestlicense) ir peržiūrėkite naują partnerio pasiūlymą. 
- Partnerius, kuriems reikalinga daugiau informacijos apie vidines naudojimo teises, žr. straipsnyje [Vidinių naudojimo teisių debesies ir programinės įrangos pranašumas (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Ar galiu bandomąja versija naudotis ilgiau nei 30 dienų?
Norėdami prailginti bandomosios versijos laikotarpį, atlikite toliau nurodytus veiksmus.

1. **Microsoft 365 Administravimo centre** eikite į **Atsiskaitymas už** > **produktus**.
2. Pasirinkite **„Dynamics 365 Project Operations (CE)“ – peržiūros versijos bandomąją versiją**.
3. Dalyje **Galiojimo pabaigos data** pasirinkite **Nustatyti vėlesnę datą**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Ar iš „Lite“ visuotinio diegimo versijos galiu atnaujinti į ištekliais / nelaikomų medžiagų scenarijumi pagrįstą visuotinį diegimą?
Šiuo metu aplinkos atnaujinimas iš „Lite“ versijos į nelaikomomis medžiagomis pagrįstą visuotinį diegimą nepalaikomas.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Ar galiu pasiekti savo finansų aplinkų „Lifecycle Services“ (LCS)?  
Ne. Šių bandomųjų versijų visuotinis diegimas tvarkomas „Power Platform“ administravimo centre. Prieiga prie finansų aplinkos yra apribota.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Ar galiu bandomąją versiją įdiegti į esamą aplinką?
Jei turite esamą aplinką, įdiegti „Lite“ visuotinį diegimą į esamą pardavimo „Dataverse“ aplinką galėsite apsilankę „Power Platform“ administravimo centre.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
