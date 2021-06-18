---
title: 2021 m. sausio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacijos apie kokybinius naujinimus, pasiekiamus 2021 m. sausio mėn. „Project Operations”, skirtos ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, leidime.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c600c30acd5e07e6370459928e33033a6ba418d6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995766"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 m. sausio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_


Ši tema taikoma toliau nurodytiems „Dynamics 365 Project Operations“ komponentams ir versijoms:

  - „Project Operations“, esanti „Dataverse“ aplinkoje, 4.6.0.154 versija
  - Projektų valdymas ir apskaita „Dynamics 365 Finance” aplinkoje, 10.0.16 versija

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| **Visuotinis diegimas ir konfigūravimas** | 2106818 | Išspręstas žiniatinklio išteklių pervardijimas, dėl kurio kyldavo problemų, susijusių su puslapio tinkinimu. |
| **Sąskaitų pateikimas ir kainodara** | 2091908 | Išspręstas parinkčių **Užrakinti įkainius** ir **Naudoti dabartinius įkainius** matomumas puslapyje **Sąskaita faktūra**, kai „Project Operations“ įdiegiamas su „Dynamics 365 Field Service“. |
| **Sąskaitų pateikimas ir kainodara** | 2103058 | Atnaujintos **Projektų bendros sumos** siekiant apdoroti nulines užduoties faktinių išlaidų reikšmes. |
| **Sąskaitų pateikimas ir kainodara** | 2116100 | Pagerinti klaidų pranešimai, naudojami su funkcija **Įrašų koregavimas faktiniuose duomenyse**. |
| **Sąskaitų pateikimas ir kainodara** | 2116129 | Patobulintas išlaidų įvertinimų matomumas puslapio **Projektas** skirtuke **Įvertinimai**. |
| **Sąskaitų pateikimas ir kainodara** | 2119112 | Fiksuotas faktinių pardavimo ir faktinių išlaidų agregavimas, kai naudojamas kitoks valiutos kursas. |
| **Sąskaitų pateikimas ir kainodara** | 2134705 | Išspręsta klaida „Nepavyko perskaityti neapibrėžtos ypatybės **getResourceString**“, kai atidarytas puslapis **Sąskaita faktūra** ir įdiegtas „Field Service“. |
| **Galimybės valdymas** | 2022195 | Užduotimi pagrįsto atsiskaitymo tinklelyje puslapyje **Projektas** yra piktograma, nurodanti, kad yra sutarties ar pasiūlymo eilutė, susieta su ta užduotimi. |
| **Galimybės valdymas** | 2029135 | Išspręsta verslo proceso klaida, įvykstanti vartotojui bandant atidaryti sąskaitos faktūros eilutę patvirtintoje sąskaitoje faktūroje, pagal kurią išrašyta iš anksto nustatyta suma. |
| **Galimybės valdymas** | 2040713 | Išspręsta scenarijaus klaida, įvykstanti kuriant sąskaitą faktūrą iš sutarties ir kai įdiegtas „Field Service“. |
| **Projektų planavimas ir sekimas** | 2090202 | Pažymėtos veiklos taisyklės, kurios nebenaudojamos kaip **Nerekomenduojama**. |
| **Laikas ir išlaidos** | 2091249 | Sugriežtinti valdikliai, kad vartotojai negalėtų keisti užduoties pateiktame ar patvirtintame laiko įraše. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektų valdymas ir apskaita programoje „Dynamics 365 Finance”

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| **Projektų valdymas ir apskaita** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Neteisinga sutarties suma puslapyje **Laisvos formos sąskaita**, skirta fiksuotos kainos projektui su keliais lėšų skyrimo šaltiniais . |
| **Projektų valdymas ir apskaita** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | **Invoiceproposal.PSAnfRefProjId** vietos rezervavimo ženklas nerodo projekto ID, skirto darbo eigai **Review project invoice proposals**. |
| **Projektų valdymas ir apskaita** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Netinkama mokėjimo nuolaidos data naudojama registruojant projekto sąskaitų faktūrų pasiūlymus. |
| **Projektų valdymas ir apskaita** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Šalinant ir skaitant išteklių priskyrimus „Project Operations“ dubliuoja projekto prognozės įrašus programoje „Finance“. |
| **Projektų valdymas ir apskaita** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Programoje „Project Operations“ negalite kurti projekto įvertinimų „Dataverse“ aplinkoje nesukurdami projekto sutarties eilutės. |
| **Projektų valdymas ir apskaita** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Projekto išlaidų transakcijos finansinės dimensijos nėra sinchronizuotos su susijusiu kvitu ir išlaidų ataskaitos apskaitos paskirstymu, kai išlaidos registruojamos į „Balansas“ |
| **Projektų valdymas ir apskaita** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Neveikia **SF būsena** filtras fiksuotos kainos projektų užregistruotose projekto operacijose. |
| **Projektų valdymas ir apskaita** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Atvirkštinio įvertinimo pašalinimas neveikia skyriuje **Periodinis**. |
| **Projektų valdymas ir apskaita** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | „Project Operations“ programoje galima panaikinti SF pasiūlymo eilutes, kai integruojamos su „Dataverse“. |
| **Projektų valdymas ir apskaita** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Neleidžiama įgalinti kelių sutarties eilučių funkcijos, jei nėra „Dataverse“ integracijos. |
| **Projektų valdymas ir apskaita** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Kai aktyvus SF išrašymas lygus pelnui ir nuostoliui, įplaukos, kurioms išrašyta SF, įvertinimų puslapyje pateikiamos kaip nulis. |
| **Projektų valdymas ir apskaita** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Integruotoje aplinkoje sąskaitų faktūrų taisymai neveikia. |
| **Projektų valdymas ir apskaita** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | NG pardavimų reikšmę registruojant vidinės įmonės projekto SF, pasirenkamas netinkamas klientas. |
| **Projektų valdymas ir apskaita** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | „Project Operations“ programoje negalima atnaujinti įvertinimo užduočių priklausomybių „Dataverse“ aplinkoje. |
| **Projektų valdymas ir apskaita** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Pakartotinai panaikinus „Project Operations“ integravimo žurnalus programoje „Finance“, duomenys prarandami. |
| **Projektų valdymas ir apskaita** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Registruojant projekto SF pasiūlymą, įvyksta ši klaida: „Operacija nesisumuoja ataskaitų valiutoje, kai pridėta išankstinė SF“. |
| **Projektų valdymas ir apskaita** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Po to, kai numatytoji projekto sutartis atnaujinama „Project Operations“ programoje, atskaitymuose įtrauktas netinkamas projekto ID. |
| **Projektų valdymas ir apskaita** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Įjungus „Project Operations“, negalimo atlikti įvertinimo ir pajamų atpažinimo. |
| **Projektų valdymas ir apskaita** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | „Project Operations“ programoje pašalinus projektą iš sutarties, sutartyje numatytasis projektas iš naujo nenustatomas. |
| **Projektų valdymas ir apskaita** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | „Project Operations“ programoje, vidinės įmonės sąskaitose faktūrose, netinkamos išlaidų eilutės rodomos sąraše **Įtraukti eilutę**. |
| **Kelionės ir išlaidos** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Išlaidų eilučių negalima užregistruoti, nes sutarties eilutėje trūksta valandų sąrankos. |
| **Kelionės ir išlaidos** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Kai projekto / kategorijos tikrinimas yra privalomas, išlaidų kategorijos, susietos su projektu, nėra matomos išlaidų ataskaitoje. |
| **Kelionės ir išlaidos** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Avanso grynaisiais pinigais balansas nėra atnaujinamas, kai išlaidų ataskaita užregistruojama pagal eilutę. |
| **Kelionės ir išlaidos** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | **Atnaujinti mokėjimo informaciją** užduotis nepavyksta atšaukus atsiskaitymus, kur SF buvo padengta dviem ar daugiau mokėjimo operacijomis. |
| **Kelionės ir išlaidos** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Įvyko problema dėl paskutinės dienos maitinimo mažinimo apskaičiavimo naudojant dienpinigių išlaidų kategoriją. |
| **Kelionės ir išlaidos** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Ataskaita **Darbuotojo išlaidų tipas** nerodo detaliai išvardytų išlaidų, jei vartotojo pirmasis ryšis buvo es-MX kalba. |
| **Kelionės ir išlaidos** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Išlaidų ataskaitos sąskaitos faktūros tiekėjo apmokėjimas naudoja klaidingą suvestinės sąskaitą atsiskaitymams registruoti. |
| **Kelionės ir išlaidos** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Kai išlaidų ataskaita užregistruojama su įgalintomis parinktimis **Leisti operacijų, pagrįstų korespondentinio mokėjimo sąskaita, grupavimą** ir **Apskaitos datos koregavimas registruojant**, apskaitos datos nėra grupuojamos lentelėje **Apskaitos paskirstymas**, kuri turi įtakos PVM įrašams. |
| **Kelionės ir išlaidos** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Išlaidų subkategorijų susiejimas pašalinamas, kai išvalomas žymės langelis „Naudoti išlaidose“ ir vėl pažymimas. |
| **Kelionės ir išlaidos** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Vidinės įmonės išlaidų ataskaitos negalima kurti, jei projekto ID pridėtas antraštės lygiu. |
| **Kelionės ir išlaidos** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Įvyko išlaidų mokėjimo problema, kai išlaidų suma yra didesnė nei avanso grynaisiais pinigais suma. |
| **Kelionės ir išlaidos** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Laukas **Projekto ID**, esantis vidinės įmonės išlaidų ataskaitoje, yra tuščias, jei vartotojo vaidmuo priskirtas konkrečiai organizacijai. |
| **Kelionės ir išlaidos** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Išlaidų kategorija yra užrakinta įtraukiant naują išlaidų eilutę. |
| **Kelionės ir išlaidos** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Išlaidų ataskaitos eilučių, kurios jau yra perskirstytos, detalus išvardymas lemia, kad uregistruotas mokėtinų sumų / didžiosios knygos kvitas bus nebaigtas. Dėl **TRVEXPTRANS.SOURCEDOCUMENTLINE** duplikavimo, apskaitos šaltinių naršyklė taip pat neveikia. |
| **Kelionės ir išlaidos** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Indekso, kuris buvo įtrauktas į lentelę **TRVREQUISITIONLINE**, kurios dublikatų turi klientas, atnaujinimo metu įvyksta klaida. |
| **Kelionės ir išlaidos** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Naudojant „Project Operations“ negalima sukurti arba patvirtinti laiko su vidinės įmonės užduotimis „Dataverse“ aplinkoje. |

## <a name="regulatory-updates"></a>Reguliavimo naujinimai

Norėdami gauti informacijos apie „Finance and Operations” programų reguliavimo naujinimus, žr. [Reguliavimo naujinimai](/dynamics365/finance/localizations/regulatory-updates). Taip pat galite prisijungti prie LCS ir peržiūrėti planuojamus reguliavimo naujinimus naudodamiesi problemų ieškos įrankiu. Problemų ieška leidžia ieškoti pagal šalį, funkcijos tipą ir leidimą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]