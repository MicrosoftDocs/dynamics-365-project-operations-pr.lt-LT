---
title: Trikčių diagnostika dirbant su užduoties tinkleliu
description: Šioje temoje pateikta trikčių diagnostikos informacija, būtina dirbant su užduočių tinkleliu.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031547"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Trikčių diagnostika dirbant su užduoties tinkleliu 

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Šioje temoje aprašoma, kaip išspręsti problemas, su kuriomis galite susidurti dirbdami su išlaidų valdymu.

## <a name="enable-cookies"></a>Slapukų įjungimas

Programoje „Project Operations“ reikia įgalinti trečiųjų šalių slapukus, kad būtų galima sukurti darbo paskirstymo struktūrą. Kai trečiųjų šalių slapukai nėra įgalinti, užuot matę užduotis, matysite tuščią puslapį, kai puslapyje **Projektas** pasirinksite skirtuką **Užduotys**.

![Tuščias skirtukas, kai neįgalinti trečiųjų šalių slapukai](media/blankschedule.png)


### <a name="workaround"></a>Alternatyvus sprendimas
Toliau nurodytose procedūrose, skirtose „Microsoft Edge“ arba „Google Chrome“ naršyklėms, apibrėžiama, kaip atnaujinti jūsų naršyklės parametrą ir įgalinti trečiosios šalies slapukus.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Atidarykite „Edge“ naršyklę.
2. Viršutiniame dešiniajame kampe pasirinkite **elipsę** (...), o tada pasirinkite **Parametrai**.
3. Dalyje **Slapukai ir svetainės teisės** pasirinkite **Slapukai ir svetainės duomenys**.
4. Išjunkite parinktį **Blokuoti trečiųjų šalių slapukus**.

#### <a name="google-chrome"></a>Google Chrome

1. Atidarykite „Chrome“ naršyklę.
2. Viršutiniame dešiniajame kampe pasirinkite tris vertikalius taškus ir pasirinkte **Parametrai**.
3. Dalyje **Privatumas ir sauga** pasirinkite **Slapukai ir kiti svetainės duomenys**.
4. Pasirinkite **Leisti visus slapukus**.

> [!IMPORTANT]
> Jei blokuosite trečiųjų šalių slapukus, visi kitų svetainių slapukai ir svetainės duomenys bus blokuojami, net jei svetainė bus leidžiama jūsų išimčių sąraše.

## <a name="pex-endpoint"></a>PEX galinis punktas

Programoje „Project Operations“ reikia, kad projekto parametras nurodytų PEX galinį punktą. Šis galinis punktas būtinas tam, kad galėtų palaikyti ryšį su paslauga, naudojama darbo paskirstymo struktūrai generuoti. Jei parametras neįjungtas, matysite klaidą „Projekto parametras negalioja“. 

### <a name="workaround"></a>Alternatyvus sprendimas
 ![Projekto parametro PEX galinio punkto laukas](media/projectparameter.png)

1. Įtraukite lauką **PEX galinis punktas** į puslapį **Projekto parametrai**.
2. Atnaujinkite lauką naudodami šią reikšmę: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Pašalinkite lauką iš puslapio **Projekto parametrai**.

## <a name="privileges-for-project-for-the-web"></a>Žiniatinklio projekto teisės

„Project Operations“ remiasi išorine planavimo paslauga. Paslauga reikalauja, kad vartotojas turėtų kelis vaidmenis, priskirtus skaityti ir rašyti objektuose, susijusiuose su darbo paskirstymo struktūra. Šie objektai apima projekto užduotis, išteklių priskyrimus ir užduočių priklausomybes. Jei vartotojas negali sugeneruoti darbo paskirstymo struktūros skirtuke **Užduotys**, tai tikriausiai yra dėl to, kad „Project Operations“ projektas nebuvo įgalintas. Vartotojas gali matyti saugos vaidmens klaidą arba klaidą, susijusią su prieigos atsisakymu.


## <a name="workaround"></a>Alternatyvus sprendimas

1. Eikite į **Parametras > Sauga > Vartotojai > Programos vartotojai**.  

   ![Programos skaitytuvas](media/applicationuser.jpg)
   
2. Dukart spustelėkite programos vartotojo įrašą ir patikrinkite, ar:

 - Vartotojas turi prieigą prie projekto. Šį tikrinimą paprastai užtikrina tai, kad vartotojas turi **Projekto vadovas** saugos vaidmenį.
 - „Microsoft Project“ programos vartotojas egzistuoja ir yra teisingai sukonfigūruotas.
 
3. Jei šis vartotojas neegzistuoja, galite sukurti naują vartotojo įrašą. Pasirinkite **Nauji vartotojai**. Pakeiskite įrašo formą į **Programos vartotojas**, o tada įtraukite **Programos ID**.

   ![Programos vartotojo išsami informacija](media/applicationuserdetails.jpg)

4. Patikrinkite, ar vartotojui priskirta tinkama licencija ir ar paslauga įgalinta paslaugos plano licencijos išsamioje informacijoje.
5. Patikrinkite, ar vartotojas gali atidaryti project.microsoft.com.
6. Projekto parametruose patikrinkite, ar sistema rodo tinkamą projekto galinį punktą.
7. Patikrinkite, ar sukurtas projekto programos vartotojas.
8. Vartotojui pritaikykite šiuos saugos vaidmenis:

  - „Dataverse“ vartotojas
  - „Project Operations“ sistema
  - „Project“ sistema

## <a name="error-when-updating-the-work-breakdown-structure"></a>Klaida naujinant darbo paskirstymo struktūrą

Darbo paskirstymo struktūroje atliekant vieną ar daugiau naujinimų, pakeitimai galiausiai nepavyks ir nebus įrašyti. Grafiko tinklelyje įvyksta klaida, nurodanti, kad „Naujausio pakeitimo įrašyti nepavyko“.

### <a name="workaround"></a>Alternatyvus sprendimas

1. Patikrinkite, ar vartotojui priskirta tinkama licencija ir ar paslauga įgalinta paslaugos plano licencijos išsamioje informacijoje.
2. Patikrinkite, ar vartotojas gali atidaryti project.microsoft.com.
3. Patikrinkite, ar sistema rodo tinkamą projekto galinį punktą.
4. Patikrinkite, ar programoje „Project“ sukurtas vartotojas.
5. Vartotojui pritaikykite šiuos saugos vaidmenis:
  
  - „Dataverse“ vartotojas arba pagrindinis vartotojas
  - „Project Operations“ sistema
  - „Project“ sistema
  - „Project Operations“ dvigubo rašymo sistema (šis vaidmuo būtinas, jei diegiate „Project Operations“, skirtą ištekliais / nelaikomomis medžiagomis pagrįstiems scenarijams).
