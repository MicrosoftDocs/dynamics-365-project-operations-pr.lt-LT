---
title: Kas naujo arba pakeista projekto operacijose, 2021 m. rugsėjo mėn.
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. rugsėjo mėn.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 7016d702719b2d432ec929aaca8d609ebf6e996b
ms.sourcegitcommit: abdd6cb3461ebb12fd2ca7ea78439c29aecd0a94
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2021
ms.locfileid: "7815828"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Kas naujo arba pakeista projekto operacijose, 2021 m. rugsėjo mėn.

_**Taikoma (kam):**„Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_

Ši tema taikoma šių komponentų ir versijų Microsoft Dynamics 365 Project Operations:

- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkos 10.0.21 versijoje
 
## <a name="quality-updates"></a>Kokybės naujinimai

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
|---|---|---|
| Projektų valdymas ir apskaita | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Jei pirkimo tvarkytuvo vaidmeniui suteikiama prieiga prie vieno juridinio subjekto, jis taip pat gauna prieigą prie visų visų juridinių subjektų projektų. |
| Projektų valdymas ir apskaita | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Pridėtinės vertės mokesčio (PVM) apvalinimo problema kyla, kai kredito pažyma sudengiama pagal pradinę projekto SF. |
| Projektų valdymas ir apskaita | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Biudžeto tikrinimui naudokite alternatyvų projekto biudžetą. |
| Projektų valdymas ir apskaita | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | **Pardavimo kainos valandų kainų grupė** neskaičiuojama projekto pasiūlymų darbo paskirstymo struktūroje. |
| Projektų valdymas ir apskaita | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Įvertinimo pašalinti nepavyksta, kai **įgalinta įgalinti projekto sutarties valiutą įvertinimo skaičiavimo** funkcijai. |
| Projektų valdymas ir apskaita | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | PVM faktoringas pagal kiekį pridedamas prie pardavimo kainos sumos, kai naudojimo mokestis naudojamas projekto išlaidų žurnalo PVM grupėje. |
| Projektų valdymas ir apskaita | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Sąlyginis mokestis nėra tinkamai apskaičiuotas paskutiniam mokėjimui, kai tiekėjo užlaikymas ir išankstinis apmokėjimas taikomas pirkimo užsakymo SF. |
| Projektų valdymas ir apskaita | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Koregavimo sekimas neveikia pradžios balanso žurnaluose. |
| Projektų valdymas ir apskaita | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Projekto biudžeto tikslinimo paskirstymas pagal laikotarpį** padalijamas visiems biudžeto laikotarpiams. Kai pateikiamas paskirstymas, įrašas neišvalomas. |
| Projektų valdymas ir apskaita | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Nebaigtų darbų (NG) registravimų DK suma neteisinga. |
| Projektų valdymas ir apskaita | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Projekto valandų žurnalo patvirtinimas neveikia. |
| Projektų valdymas ir apskaita | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Projekto koregavimo pardavimo kaina neatnaujinama netiesioginėmis išlaidomis, kai nepažymėtas lėšų limitas. |
| Projektų valdymas ir apskaita | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Prekės poreikio sukurti negalima, kai pardavimo lentelės antraštei išrašoma SF ir baigiamas kurti esamų eilučių atsarginis pirkimo užsakymas. |
| Projektų valdymas ir apskaita | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Atsiskaitymo taisyklės, kurios etapas skirtas kitam projektui, saugojimo suma neregistruota atitinkamame projekto ID, kuris buvo pasirinktas etapui. Vietoj to, jis paskelbtas su pirmuoju projektu. |
| Projektų valdymas ir apskaita | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Kai SF pasiūlyme pasirenkate **Finansinių** dimensijų rinkinys, įvyksta tokia klaida: "Neįmanoma mesti objekto, kurio tipas 'Dynamics.AX. Application.FormIntControl", kad įvestumėte "Dynamics.AX. Application.FormStringControl'." |
| Projektų valdymas ir apskaita | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | **Projekto SF ataskaitoje** praleidžiamos eilutės. |
| Projektų valdymas ir apskaita | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Skaičiuojant investicinio projekto išlaidų kontrolę įvyksta klaida. |
| Projektų valdymas ir apskaita | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | **ProjTable::InitFromCustTable - canDeletePostalAddress** metodas sukelia efektyvumo problema. |
| Projektų valdymas ir apskaita | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Klaidos pranešimas turi būti aiškesnis nei "Netikėta klaida". |
| Projektų valdymas ir apskaita | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Projekto SF registravimo paketinė užduotis apdoroja ir registruoja SF pasiūlymą, net jei SF eilutės nebuvo sugeneruotos. |
| Projektų valdymas ir apskaita | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Apvalinimo problema kyla, kai viešojo sektoriaus licencijos konfigūracijos raktas yra išjungtas. Sutarčių, kuriose yra keli steigėjai, tabelio valandomis generuojama neteisinga savikaina arba pardavimo kaina. |
| Projektų valdymas ir apskaita | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Projekto pardavimo kaina projekto pirkimo užsakyme, kuriam išrašyta SF, neteisingai apskaičiuojama, kai pardavimo kainos modelis yra **Įnašo koeficientas**. |
| Projektų valdymas ir apskaita | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistema neatsižvelgia į aktyvias dienas tarp to, kai ji apskaičiuoja efektyvų darbuotojo darbo tarifą. |
| Projektų valdymas ir apskaita | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Vidinės įmonės tabelio registravimo klaida įvyksta dėl šios tikrinimo klaidos: "Nesukonfigūruotas joks juridinio subjekto prekybos partneris." |
| Projektų valdymas ir apskaita | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Aprašymas iš pirkimo užsakymo, kuriame yra išlaidų kategorija, nėra nuskaitomas užregistruotų projekto operacijų sąraše. |
| Projektų valdymas ir apskaita | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Prekių žurnaluose, kurie registruojami projekte, yra neteisingas konvertavimas. |
| Projektų valdymas ir apskaita | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Galite patvirtinti pirkimo užsakymą, net jei viršytas lėšų limitas. |
| Projektų valdymas ir apskaita | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | **Laisvos formos SF skyrius Taisymas/Atšaukti SF dingsta** pasirinkus projekto ID. |
| Projektų valdymas ir apskaita | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Yra efektyvumo problemų, kai projekto SF pasiūlymas registruojamas iš projekto pardavimo užsakymo, kuriame yra laikoma prekė. |
| Projektų valdymas ir apskaita | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Projekto pirkimo SF užregistruoti negalima, nes įvyksta ši klaida: "Funkcija AccDistProcessorProjectExtension.createForProjectRevenueLine buvo iškviesta neteisingai." |
| Projektų valdymas ir apskaita | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Atnaujinti į projekto įvertinimo paketinių užduočių kūrimą, kad būtų palaikomas kelių antrinių užduočių vykdymas. |
| Projektų valdymas ir apskaita | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Grafiko būsenos negalima atnaujinti į **Juodraštis,** kai darbo eiga užstrigo **būsenoje** Atšaukta. |
| Projektų valdymas ir apskaita | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Saugojimo sumos kredito pažymos SF pasiūlyme neskaičiuojamos, jei yra kelios eilutės. |
| Projektų valdymas ir apskaita | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Kai bandote pakeisti sugeneruotos SF sumą iš pirkimo užsakymo, įvyksta ši klaida: "Kvito operacijos nesubalansuotos pagal XX/XX/XXXX. (apskaitos valiuta: 0,00 – ataskaitų valiuta: 0,01)“. |
| Projektų valdymas ir apskaita | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Yra efektyvumo problema, kai projekto SF pasiūlymas registruojamas paketiniu režimu, nes sujungimo su **GeneralJournalAccountEntry**. |
| Projektų valdymas ir apskaita | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Registruojant tabelį kyla efektyvumo problemų. |
| Projektų valdymas ir apskaita | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Darbo paskirstymo struktūros išlaidų įvertinimo hierarchija netinkamai sulygiuota išplėtus visas užduotis arba išplėtus vieną užduotį neautomatiniu būdu. |
| Projektų valdymas ir apskaita | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Projekto pasiūlymo "Excel" šablono negalima įtraukti į **meniu Atidaryti naudojant "Excel".** |
| Projektų valdymas ir apskaita | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Juridinio subjekto NEAPMOKESTINIMO kodas neįtrauktas į išspausdintą projekto SF. |
| Projektų valdymas ir apskaita | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Atsargų vieneto klaida neatnaujinama jokiais finansiniais duomenimis, kai projektas koreguojamas atsižvelgiant į kredito eilutes. |
| Projektų valdymas ir apskaita | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Pritaikius KB 461935, negalite registruoti įvertinimų, jei perjungiate į nuolatines numeracijas. |
| Projektų valdymas ir apskaita | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** sukelia projekto tabelio mobiliojo ryšio programą Android nustoti reaguoti. |
| Projektų valdymas ir apskaita | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | SF registravimo NG atšaukta vertė skiriasi nuo iš pradžių užregistruotos NG vertės nuo laiko įrašo. |
| Projektų valdymas ir apskaita | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Sugretinto laikiklio atvejais kvito operacijos nesubalansuotos, kai užregistruotos projekto įplaukos, kurioms išrašyta SF. |
| Projektų valdymas ir apskaita | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Įgalinus **projekto išteklių planavimo efektyvumo didinimo** funkciją, dešimtainės reikšmės neteisingai suapvalinamos išteklių pakankamumui ir pajėgumui. |
| Projektų valdymas ir apskaita | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Įgalinus **funkciją Kurti projekto įvertinimus naudojant kelias paketines** užduotis, įvertinimų kūrimas pakete, kuriame yra kelios antrinės užduotys, veikia tik dabartiniame laikotarpiuose. |
| Kelionės ir išlaidos | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Kelionės paraiškos strategijos nepaisoma, o darbo eiga patvirtinama be klaidų. |
| Kelionės ir išlaidos | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobiliųjų išlaidų programėlė išlaidų eilutėje neįrašo šios informacijos:</p><ul><li>Projekto ID</li><li>Ar išlaidos yra apmokėtinos</li><li>Veiklos numeris</li></ul> |
| Kelionės ir išlaidos | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | **Laukas Pridėti gavimai** nustatytas kaip **Taip**, net jei prie išlaidų eilutės nepridėtas kvitas. |
| Kelionės ir išlaidos | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Klaida įvyksta, kai pakeičiate išlaidų kategoriją į **Asmeninė**. |
| Kelionės ir išlaidos | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Negalite pridėti kvito ir redaguoti pirminių išlaidų po to, kai kredito kortelės operacija padalyta į asmenines išlaidas. |
| Kelionės ir išlaidos | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Vidinės įmonės operacijų, kurių projekto ID yra, išlaidų strategija veikia netinkamai. |
| Kelionės ir išlaidos | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Trūksta užregistruotų išlaidų ataskaitų užregistruotos datos informacijos. |
| Kelionės ir išlaidos | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Programėlėje Išlaidos mobiliajame įrenginyje yra mokėjimo būdo problemų. |
| Kelionės ir išlaidos | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Vienam darbuotojui sukurtą kelionės paraišką galima naudoti kito darbuotojo išlaidų ataskaitoje prieš atstovo datą. |
| Kelionės ir išlaidos | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Kai kuriate išlaidas, finansinių dimensijų verčių pakeitimai netinkamai atnaujinami darbo srities Išlaidų valdymas apskaitos paskirstymo **lygyje**. |
| Kelionės ir išlaidos | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Pagrindinės išlaidų eilutės patvirtinimo būsena nesinchronizuojama su detalizuota eilutės darbo eigos patvirtinimo būsena. |
| Kelionės ir išlaidos | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Klaida įvyksta, jei registruojate išlaidų ataskaitą ir mokesčių susigrąžinimas yra įjungtas. |
| Kelionės ir išlaidos | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Atstovas negali panaikinti atleisto darbuotojo išlaidų dokumentų. |
| Kelionės ir išlaidos | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Išlaidų eilutės naikinimas užtrunka ilgiau nei tikėtasi ir turi įtakos našumui. |
| Kelionės ir išlaidos | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** sukelia vienišas **TaxUncommit** įrašas, nes tik **SourceDocumentLine** panaikinamas. |
| Kelionės ir išlaidos | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId() nepaiso** **trvExpTrans.ReferenceDataAreaId** sukurti naują numeraciją. |

## <a name="regulatory-updates"></a>Reguliavimo naujinimai

Informacijos apie "Finance and Operations" programų reguliavimo naujinimus ieškokite [Regulatory updates](/dynamics365/finance/localizations/regulatory-updates). Taip pat galite prisijungti prie Microsoft Dynamics gyvavimo ciklo paslaugų (LCS) ir naudoti problemų ieškos įrankį, kad peržiūrėtumėte suplanuotus reguliavimo naujinimus. Problemų ieška leidžia ieškoti pagal šalį ar regioną, funkcijos tipą ir leidimą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
