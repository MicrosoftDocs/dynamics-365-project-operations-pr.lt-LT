---
title: Trikčių diagnostika dirbant su užduoties tinkleliu
description: Šiame straipsnyje pateikiama trikčių šalinimo informacija, reikalinga dirbant tinklelyje Užduotis.
author: ruhercul
ms.date: 07/22/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 208ed55abf4cdf0ad2b035bd923e183ff3cae660
ms.sourcegitcommit: e91136d3335ee03db660529eccacd48907774453
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/22/2022
ms.locfileid: "9188242"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Trikčių diagnostika dirbant su užduoties tinkleliu 


_**Taikoma:** „Project Operations“ ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, „Lite“ visuotinis diegimas – sąskaitų faktūrų išrašymo sandoris, „Project for the web“_

Užduočių tinklelis, kurį Dynamics 365 Project Operations naudoja, yra priglobtas iframe viduje Microsoft Dataverse. Dėl šio naudojimo turi būti laikomasi konkrečių reikalavimų, kad būtų užtikrintas autentifikavimas, o autorizacija veiktų tinkamai. Šiame straipsnyje aprašomos dažniausios problemos, kurios gali turėti įtakos galimybei generuoti tinklelį arba valdyti užduotis darbo paskirstymo struktūroje (WBS).

Dažniausiai pasitaikančios problemos:

- Skirtukas **Užduotis** užduočių tinklelyje yra tuščias.
- Atidarant projektą jis neįkeliamas, o vartotojo sąsaja (UI) užstringa.
- **Project for the Web** teisių administravimas.
- Kuriant, naujinant arba naikinant užduotį pakeitimai neįrašomi.

## <a name="issue-the-task-tab-is-empty"></a>Problema: užduoties skirtukas yra tuščias

### <a name="mitigation-1-enable-cookies"></a>1 poveikio sumažinimas: įjunkite slapukus

„Project Operations“ reikia, kad būtų įjungti trečiųjų šalių slapukai, norint atvaizduoti darbo paskirstymo struktūrą. Kai trečiųjų šalių slapukai neįjungti, užuot matę užduotis, puslapyje Projektas **pasirinkę skirtuką** **Užduotys** matysite tuščią puslapį.

Toliau nurodytose procedūrose, skirtose „Microsoft Edge“ arba „Google Chrome“ naršyklėms, apibrėžiama, kaip atnaujinti jūsų naršyklės parametrą ir įgalinti trečiosios šalies slapukus.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Atidarykite „Edge“ naršyklę.
2. Viršutiniame dešiniajame kampe pasirinkite **elipsę** (...), o tada pasirinkite **Parametrai**.
3. Dalyje **Slapukai ir svetainės teisės** pasirinkite **Slapukai ir svetainės duomenys**.
4. Išjunkite parinktį **Blokuoti trečiųjų šalių slapukus**.
5. Atnaujinkite naršyklę. 

#### <a name="google-chrome"></a>Google Chrome

1. Atidarykite „Chrome“ naršyklę.
2. Viršutiniame dešiniajame kampe pasirinkite tris vertikalius taškus ir pasirinkte **Parametrai**.
3. Dalyje **Privatumas ir sauga** pasirinkite **Slapukai ir kiti svetainės duomenys**.
4. Pasirinkite **Leisti visus slapukus**.
5. Atnaujinkite naršyklę. 

> [!NOTE]
> Jei blokuosite trečiųjų šalių slapukus, visi kitų svetainių slapukai ir svetainės duomenys bus blokuojami, net jei svetainė bus leidžiama jūsų išimčių sąraše.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>2 poveikio sumažinimas: patikrinkite, ar tinkamai sukonfigūruotas PEX galinis punktas

Programoje „Project Operations“ reikia, kad projekto parametras nurodytų PEX galinį punktą. Šis galinis punktas būtinas norint palaikyti ryšį su paslauga, kuri naudojama darbo paskirstymo struktūrai atvaizduoti. Jei parametras neįjungtas, gausite klaidą "Projekto parametras negalioja". Norėdami atnaujinti PEX galinį punktą, atlikite toliau nurodytus veiksmus.

1. Įtraukite lauką **PEX galinis punktas** į puslapį **Projekto parametrai**.
2. Identifikuokite naudojamo produkto tipą. Ši reikšmė naudojama nustačius PEX galinį punktą. Gaunant, produkto tipas jau apibrėžtas PEX galiniame punkto. Išlaikykite šią vertę.
3. Atnaujinkite lauką naudodami šią reikšmę: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. Šioje lentelėje pateikiamas tipo parametras, kurį reikia naudoti pagal produkto tipą.

      | **Produkto tipas**                     | **Parametras Tipas** |
      |--------------------------------------|--------------------|
      | Numatytosios organizacijos „Project for the Web”   | type=0             |
      | CDS pavadintos organizacijos „Project for the Web” | type=1             |
      | „Project Operations“                   | type=2             |

4. Pašalinkite lauką iš puslapio **Projekto parametrai**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>3 švelninimas: prisijunkite prie project.microsoft.com

Naršyklėje atidarykite naują skirtuką, eikite į project.microsoft.com ir prisijunkite naudodami vartotojo vaidmenį, kurį naudojate norėdami pasiekti "Project Operations". Svarbu, kad naršyklėje prie "Microsoft" produkto būtų prisijungęs tik vienas vartotojas. Klaidos pranešimas "login.microsoftonline.com atsisakė prisijungti" dažniausiai pasirodo, kai prisijungia daugiau nei vienas vartotojas, kaip parodyta tolesnėje iliustracijoje.

![Pasirinkite paskyros prisijungimo puslapį, kuriame rodoma, kad du vartotojai yra prisijungę.](media/MULTIPLE_USERS_LOGGED_IN.png)

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problema: projektas neįkeliamas, o UI užstringa

Kad būtų galima autentifikuoti, turi būti įjungti iššokantys langai norint įkelti užduočių tinklelį. Jei iššokantys langai neįjungti, ekranas užstrigs įkėlimo suktuke. Toliau pateiktame grafike rodomas URL su užblokuota iššokančia etikete adreso juostoje, todėl suktukas užstringa bandydamas įkelti puslapį. 

   ![Užstrigęs suktukas ir iššokančių langų blokavimas.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>1 poveikio sumažinimas: įjunkite iššokančius langus

Kai jūsų projektas užstringa, gali būti, kad neįjungti iššokantys langai.

#### <a name="microsoft-edge"></a>Microsoft Edge

„Edge“ naršyklėje iššokančius langus galima įjungti dviem būdais.

1. „Edge“ naršyklėje pažymėkite pranešimą viršutiniame dešiniajame naršyklės kampe.
2. Pasirinkite **Visada leisti iššokančius langus ir nukreipimus iš** konkrečios „Dataverse“ aplinkos.
 
     ![Iššokančių langų blokavimo langas.](media/enablepopups.png)

Arba galite atlikti vieną iš nurodytų veiksmų.

1. Atidarykite „Edge“ naršyklę.
2. Viršutiniame dešiniajame kampe pasirinkite **daugtaškį** (...), tada – **Parametrai** > **Svetainės leidimai** > **Iššokantys langai ir nukreipimai**.
3. Išjunkite iššokančių langų blokavimo **Iššokančius langus ir nukreipimus** arba įjunkite norėdami savo įrenginyje leisti iššokančius langus.
4. Įjungę iššokančius langus atnaujinkite naršyklę. 

#### <a name="google-chrome"></a>Google Chrome
1. Atidarykite „Chrome“ naršyklę.
2. Pereikite į puslapį, kuriame blokuojami iššokantys langai.
3. Adreso juostoje pažymėkite **Užblokuoti iššokantys langai**.
4. Pažymėkite norimo peržiūrėti iššokančio lango nuorodą.
5. Įjungę iššokančius langus atnaujinkite naršyklę. 

> [!NOTE]
> Norėdami visada matyti iššokančius svetainės langus pažymėkite **Visada leisti iššokančius langus ir nukreipimus iš [svetainės]** ir **Atlikta**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>3 poveikio sumažinimas: „Project for the Web“ teisių administravimas

„Project Operations“ remiasi išorine planavimo paslauga. Paslauga reikalauja, kad vartotojui būtų priskirti keli vaidmenys, leidžiantys skaityti ir rašyti objektams, susijusiems su WBS. Šie objektai apima projekto užduotis, išteklių priskyrimus ir užduočių priklausomybes. Jei vartotojas negali pateikti WBS, kai pereina į skirtuką **Užduotys**, tikriausiai taip yra todėl **, kad "Project for Project Operations"** **neįjungta**. Vartotojas gali matyti saugos vaidmens klaidą arba klaidą, susijusią su prieigos atsisakymu.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>1 poveikio sumažinimas: patikrinkite programos vartotojo ir galutinio vartotojo saugos vaidmenis

1. Eikite į **Parametras** > **Sauga** > **Vartotojai** > **Programos vartotojai**.  

   ![Programos skaitytuvas.](media/applicationuser.jpg)
   
2. Dukart spustelėkite programos vartotojo įrašą norėdami patikrinti:

     - Vartotojas turi prieigą prie projekto. Tai galite padaryti patikrindami, ar vartotojas turi **Projekto vadovo** saugos vaidmenį.
     - „Microsoft Project“ programos vartotojas egzistuoja ir yra teisingai sukonfigūruotas.
 
3. Jei šio vartotojo nėra, sukurkite naujo vartotojo įrašą. 
4. Pažymėkite **Nauji vartotojai**, pakeiskite įrašo formą į **Programos vartotojas**, tada įtraukite **Programos ID**.

   ![Programos vartotojo išsami informacija.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>4 problema: kuriant, naujinant arba naikinant užduotį pakeitimai neįrašomi

Atliekant vieną ar daugiau WBS naujinimų, keitimai neatliekami ir neįrašomi. Grafiko tinklelyje įvyksta klaida ir rodomas pranešimas „Naujausio jūsų atlikto pakeitimo nepavyko įrašyti“.

### <a name="mitigation-1-validate-the-license-assignment"></a>1 poveikio sumažinimas: patikrinkite licencijos priskyrimą

1. Patikrinkite, ar vartotojui priskirta tinkama licencija ir ar paslauga įgalinta paslaugos plano licencijos išsamioje informacijoje.  
2. Patikrinkite, ar vartotojas gali atidaryti **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>2 poveikio sumažinimas: projekto programos vartotojo tikrinimo konfigūracija
1. Patikrinkite, ar programoje „Project“ sukurtas vartotojas.
2. Vartotojui pritaikykite šiuos saugos vaidmenis:
  
  - „Dataverse“ vartotojas arba pagrindinis vartotojas
  - „Project Operations“ sistema
  - „Project“ sistema
  - „Project Operations“ dvigubo rašymo sistema. Šis vaidmuo reikalingas „Project Operations“ ištekliais / atsargose nelaikomomis prekėmis pagrįsto visuotinio diegimo scenarijui.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
