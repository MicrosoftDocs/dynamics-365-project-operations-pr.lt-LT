---
title: 2020 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2020 m. lapkričio mėn. „Project Operations Lite”, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c7ec9360401bf214ae867769b0e48e545a6bad48
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367276"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>2020 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Ši tema taikoma toliau nurodytiems „Dynamics 365 Project Operations” komponentams ir versijoms.

- „Project Operations” CDS aplinkoje, 4.4.0.70 versija
- Projektų valdymas ir apskaita „Dynamics 365 Finance” aplinkoje, 10.0.14 versija

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>„Project Operations“, skirtos ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, naujinimai

### <a name="project-operations-on-cds"></a>„Project Operations“ programoje CDS

| Funkcijų sritis                 | Nuorodos numeris | Kokybės naujinimas                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  Galimybių valdymas       | 2036993          | Įvertinimo eilutė ir išteklių priskyrimo sutarties eilutės atnaujinamos laimėjus pasiūlymą, kai pasiūlymo eilutės tipas yra **Visos užduotys**.                                                 |
| Sąskaitų siuntimas ir kainodara          | 2070392          | Projekto sutarties eilutės sąskaitoje faktūroje didėja kaskart pasirinkus **Atnaujinti sąskaitos faktūros operacijas**.                                                                         |
| Projekto planavimas             | 2043336          | Nepavyksta panaikinti projekto komandos nario įrašo.                                                                                                                                  |
| Projekto planavimas             | 2046013          | Nesuderinamas įvertinimų žymės stulpelių veikimas įkeliant ir keičiant laipsniško išdėstymo laike tipą.                                                                                   |
| Projekto planavimas             | 2046647          | Pradžios ir pabaigos laikai yra išjungti iki tos valandos, kai išteklių reikalavimai sugeneruojami iš projekto komandos narių.                                                                      |
| Projekto planavimas             | 2053879          | (Artėjančiame CDS diegime) PublishUnassignedAssignments nutraukia bandymą įrašyti užduotį, kai klaida „Reikšmė perduota ConditionOperator.In” yra tuščia.                       |
| Projekto planavimas             | 2055501          | Palikus lauką **Projekto pradžios data** tuščią, atsiranda grafiko triktis.                                                                                                      |
| Projekto planavimas             | 2066817          | Nepavyksta sukurti bendrojo ištekliaus naudojant žmonių išrinkiklį skirtuke **Užduotys**.                                                                                                   |
| Projekto planavimas             | 2067034          | Mygtukas **Peržiūrėti išsamią informaciją** nepasiekiamas puslapyje **Išsami užduoties informacija**.                                                                                                       |
| Išteklių valdymas          | 2046667          | Bendrieji komandos nariai nepanaikinami net ir įvykdžius visus išteklius.                                                                                                    |
| Laikas ir spartusis išlaidų įrašas | 2047499          | Laiko įrašo puslapyje esančiu mygtuku **Naujas** atidaromas puslapis **Naujas el. pašto parašas**.                                                                                               |
| Laikas ir spartusis išlaidų įrašas | 2059859          | Kuriant išlaidų įrašą, atidaromas netikėtas iššokantysis langas.                                                                                                                         |
| Kita                        | 2044181          | (Pirkimo užsakymo šalinimas) Bandant pašalinti msdyn_ProjectServiceCore_Patch ir msdyn „Project Service” pagrindinius sprendimus, įvyksta klaida „Įrašas nepasiekiamas“.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektų valdymas ir apskaita programoje „Dynamics 365 Finance”

| Funkcijų sritis        | Nuorodos numeris | Kokybės naujinimas                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pajamų pripažinimas | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Projekto įvertinimo užbaigimo procentas yra neteisingas, kai sutartyje naudojama užsienio valiuta ir darbo eigos procentas, skirtas užbaigtam metodui.                     |
| Pajamų pripažinimas | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Nepavyksta užregistruoti įvertinimų naudojant užbaigimo metodą **Faktinę savikainą**.                                                                                                    |
| Pajamų pripažinimas | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Pašalinti nepavyksta dėl kvito disbalanso klaidos, kai įmonės valiuta skiriasi nuo operacijos valiutos.                                              |
| Išlaidų valdymas  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Ne administratoriams peržvalgos išlaidų eilutės stulpelių reikšmės, pvz., **Projekto ID** ir **Išlaidų kategorija**, nerodomos tinkamai duomenų jungties kadre. |
| Išlaidų valdymas  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Numatytoji eilutės ypatybė nerodoma išlaidų kategorijoms.                                                                                                         |
| Išlaidų valdymas  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Išlaidų integravimas turi apimti eilutės ypatybę iš išlaidų ataskaitos.                                                                                             |
| SF išrašymas           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Nepavyksta užregistruoti projekto sąskaitos faktūros pasiūlymų dėl klaidos pranešimo, kuriame sakoma, kad FD derinys nebuvo patvirtintas.                                                    |
| SF išrašymas           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Nepavyksta peržiūrėti operacijų iš **sąskaitos faktūros** išsamios informacijos puslapio.                                                                                                              |
| SF išrašymas           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Sąskaitos faktūros pasiūlymo eilutes galima naikinti.                                                                                                                                  |
| Projekto apskaita  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Meniu **Prognozė** elementai nerodomi **projektų** sąrašo puslapyje.                                                                                                   |
| Projekto apskaita  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Nepavyksta atidaryti **Projekto patvirtinimas**   > **Operacijos ir prognozė**.                                                                                                       |
| Projekto apskaita  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | Parinktis **Koreguoti apskaitą** neįjungta projekto operacijoms, pagal kurias išrašyta SF.                                                                                                  |
| Projekto apskaita  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Apskaitos informacija neįtraukiama į lentelę **ProjCDSActualsImport** registruojant **integravimo žurnalą**.                                                  |
| Projekto apskaita  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Projekto prognozės įrašas dvigubinamas, kai šalinate ir iš naujo pridedate išteklių priskyrimą.                                                                            |
| Projekto apskaita  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Pasirinkus projekto ID saitą neatidaromas CDS giliojo saito URL.                                                                                                         |
| Projekto apskaita  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Nepavyksta atnaujinti CDS užduoties pradžios datos.                                                                                                                           |
| Projekto apskaita  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Įjungus šią funkciją, kelios sutarties eilutės negalimos be CDS integravimo.                                                                                   |

### <a name="regulatory-updates"></a>Reguliavimo naujinimai
Norėdami gauti informacijos apie „Finance and Operations” programų reguliavimo naujinimus, žr. [Reguliavimo naujinimai](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Taip pat galite prisijungti prie LCS ir peržiūrėti planuojamus reguliavimo naujinimus naudodamiesi problemų ieškos įrankiu. Problemų ieška leidžia ieškoti pagal šalį, funkcijos tipą ir leidimą.
