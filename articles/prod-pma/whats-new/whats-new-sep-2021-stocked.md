---
title: Kas naujo ar pakeista "Project Operations", 2021 m. rugsėjo mėn., jei norite, kad būtų galima laikyti / gaminti pagrįstus scenarijus
description: Šioje temoje pateikiama informacija apie kokybės atnaujinimus, kuriuos galima rasti 2021 m. rugsėjo mėn.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 24de8626199a3ed56bb6703b78d746ff7a43a089
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582030"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Kas naujo ar pakeista "Project Operations", 2021 m. rugsėjo mėn., jei norite, kad būtų galima laikyti / gaminti pagrįstus scenarijus

_**Taikoma (kam):**„Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_

Ši tema taikoma šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.21 versija
 
## <a name="quality-updates"></a>Kokybės naujinimai

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
|---|---|---|
| Projektų valdymas ir apskaita | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Jei pirkimo vadybininko vaidmeniui suteikiama prieiga prie vieno juridinio asmens, jis taip pat gauna prieigą prie visų projektų visuose juridiniuose subjektuose. |
| Projektų valdymas ir apskaita | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Pridėtinės vertės mokesčio (PVM) apvalinimo išdavimas įvyksta, kai kredito pažyma sudengiama su pradine projekto SF. |
| Projektų valdymas ir apskaita | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Biudžeto tikrinimui naudokite alternatyvų projekto biudžetą. |
| Projektų valdymas ir apskaita | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Pardavimo **kainos valandų** kainų grupė neskaičiuojama pagal projekto pasiūlymų darbo paskirstymo struktūrą. |
| Projektų valdymas ir apskaita | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Įvertinimo pašalinimas nepavyksta, **kai įgalinta vertinimo skaičiavimo** funkcija Įgalinti projekto sutarties valiutą. |
| Projektų valdymas ir apskaita | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | PVM faktoringas pagal kiekį įtraukiamas į pardavimo kainos sumą, kai projekto išlaidų žurnalo PVM grupėje naudojamas naudojimo mokestis. |
| Projektų valdymas ir apskaita | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Sąlyginis mokestis neteisingai apskaičiuojamas už paskutinį mokėjimą, kai pirkimo užsakymo SF taikomi tiekėjo užlaikymas ir išankstinis apmokėjimas. |
| Projektų valdymas ir apskaita | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Koregavimo sekimas neveikia pradžios balanso žurnaluose. |
| Projektų valdymas ir apskaita | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Projekto biudžeto tikslinimo paskirstymas pagal laikotarpį** yra padalintas į visus biudžeto laikotarpius. Pateikus paskirstymą, įrašas neišvalomas. |
| Projektų valdymas ir apskaita | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Nebaigtų darbų (NG) registravimų DK suma neteisinga. |
| Projektų valdymas ir apskaita | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Projekto valandų žurnalo patvirtinimas neveikia. |
| Projektų valdymas ir apskaita | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Projekto koregavimo pardavimo kaina neatnaujinama netiesioginėmis išlaidomis, kai lėšų skyrimo limitas nepažymėtas. |
| Projektų valdymas ir apskaita | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Prekės poreikio sukurti negalima, kai pardavimo lentelės antraštei išrašoma SF ir užbaigiamas esamų eilučių atsarginis pirkimo užsakymas. |
| Projektų valdymas ir apskaita | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Atsiskaitymo taisyklės, turinčios kito projekto etapą, užlaikymo suma neregistruojama atitinkamame projekto ID, kuris buvo pasirinktas etapui. Vietoj to, jis paskelbtas su pirmuoju projektu. |
| Projektų valdymas ir apskaita | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | **Pasirinkus SF pasiūlyme nustatytą** finansinę dimensiją, įvyksta tokia klaida: "Neįmanoma mesti objekto, kurio tipas 'Dynamics..AX Application.FormIntControl" įveskite "Dynamics.AX" Application.FormStringControl'. |
| Projektų valdymas ir apskaita | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Projekto **SF** ataskaita praleidžia eilutes. |
| Projektų valdymas ir apskaita | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Klaida įvyksta, kai skaičiuojate investicinio projekto išlaidų kontrolę. |
| Projektų valdymas ir apskaita | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metodas **ProjTable:: InitFromCustTable - canDeletePostalAddress** sukelia našumo problemą. |
| Projektų valdymas ir apskaita | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Klaidos pranešimas turėtų būti aiškesnis nei "Netikėta klaida". |
| Projektų valdymas ir apskaita | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Projekto SF registravimo paketinė užduotis apdoroja ir registruoja SF pasiūlymą, net jei SF eilutės nesugeneruotos. |
| Projektų valdymas ir apskaita | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Apvalinimo problema kyla išjungus viešojo sektoriaus licencijos konfigūracijos raktą. Sutarčių, turinčių kelis steigimo šaltinius, tabelio valandomis generuojama neteisinga savikaina arba pardavimo kaina. |
| Projektų valdymas ir apskaita | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Projekto pardavimo kaina projekto pirkimo užsakyme, kuriam išrašyta SF, neteisingai apskaičiuojama, kai pardavimo kainos modelis yra **Įnašo santykis**. |
| Projektų valdymas ir apskaita | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistema neatsižvelgia į aktyvias dienas tarp jų, kai apskaičiuoja faktinį darbuotojo darbo užmokestį. |
| Projektų valdymas ir apskaita | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Vidinės įmonės tabelyje įvyksta registravimo klaida dėl šios tikrinimo klaidos: "Joks prekybos partneris nesukonfigūruotas juridiniam subjektui". |
| Projektų valdymas ir apskaita | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Pirkimo užsakymo, turinčio išlaidų kategoriją, aprašymas nėra nuskaitomas užregistruotame projekto operacijų sąraše. |
| Projektų valdymas ir apskaita | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Prekių žurnaluose, kurie registruojami projekte, yra neteisingas konvertavimas. |
| Projektų valdymas ir apskaita | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Galite patvirtinti pirkimo užsakymą, net jei finansavimo riba buvo viršyta. |
| Projektų valdymas ir apskaita | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Laisvos **formos SF sekcija Taisymas/Atšaukti SF** dingsta pasirinkus projekto ID. |
| Projektų valdymas ir apskaita | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Yra našumo problemų, kai projekto SF pasiūlymas registruojamas iš projekto pardavimo užsakymo, kuriame yra laikoma prekė. |
| Projektų valdymas ir apskaita | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Projekto pirkimo SF užregistruoti negalima, nes įvyksta tokia klaida: "Function AccDistProcessorProjectExtension.createForProjectRevenueLine buvo neteisingai iškviesta." |
| Projektų valdymas ir apskaita | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Atnaujinti į projekto įvertinimo paketinių užduočių kūrimą, kad būtų palaikomas kelių antrinių užduočių vykdymas. |
| Projektų valdymas ir apskaita | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Tabelio būsenos negalima atnaujinti į **Juodraštis**, kai darbo eiga įstrigo atšaukta **būsenoje**. |
| Projektų valdymas ir apskaita | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Užlaikymo sumos kredito pažymos SF pasiūlyme neskaičiuojamos, jei yra kelios eilutės. |
| Projektų valdymas ir apskaita | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Kai bandote pakeisti sugeneruotos SF sumą iš pirkimo užsakymo, įvyksta tokia klaida: "Kvito operacijos nebalansuojamos pagal XX/XX/XXXX. (apskaitos valiuta: 0,00 – ataskaitų valiuta: 0,01)“. |
| Projektų valdymas ir apskaita | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Yra našumo problema, kai projekto SF pasiūlymas registruojamas paketiniu režimu dėl prisijungimo prie **GeneralJournalAccountEntry**. |
| Projektų valdymas ir apskaita | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Registruojant tabelį kyla našumo problemų. |
| Projektų valdymas ir apskaita | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Išplėtus visas užduotis arba neautomatiniu būdu išplėtus vieną užduotį, darbo suskirstymo struktūros išlaidų sąmatų hierarchija nesulygiuojama teisingai. |
| Projektų valdymas ir apskaita | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Projekto pasiūlymo "Excel" šablono negalima įtraukti į **meniu Atidaryti naudojant "Excel"**. |
| Projektų valdymas ir apskaita | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Juridinio subjekto pvm mokėtojo kodas neįtrauktas į išspausdintą projekto SF. |
| Projektų valdymas ir apskaita | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Atsargų vieneto paklaidoje neatnaujinami jokie finansiniai duomenys, kai projektas koreguojamas atsižvelgiant į kredito eilutes. |
| Projektų valdymas ir apskaita | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Pritaikę KB 461935, negalite registruoti įvertinimų, jei pereisite prie nepertraukiamų numeracijų. |
| Projektų valdymas ir apskaita | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** sukelia projekto tabelio mobiliųjų įrenginių programą, kad nustotų Android reaguoti. |
| Projektų valdymas ir apskaita | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | SF registravimo ng atvirkštinė vertė skiriasi nuo iš pradžių užregistruotos NG vertės nuo laiko įrašo. |
| Projektų valdymas ir apskaita | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Tais atvejais, kai taikomos užlaikamosios priemonės, kvito operacijos nebalansuojamos, kai užregistruojamos projekto įplaukos, kurioms išrašyta SF. |
| Projektų valdymas ir apskaita | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Įgalinus **projekto išteklių planavimo našumo didinimo** funkciją, dešimtainės reikšmės neteisingai suapvalinamos pagal išteklių pakankamumą ir pajėgumą. |
| Projektų valdymas ir apskaita | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Įgalinus **funkciją Kurti projekto įvertinimus naudojant kelias paketines užduotis**, įvertinimų kūrimas pakete, kuriame yra kelios antrinės užduotys, veikia tik šiuo laikotarpiu. |
| Kelionės ir išlaidos | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Kelionės paraiškos strategijos nepaisoma, o darbo eiga patvirtinama be klaidų. |
| Kelionės ir išlaidos | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Mobiliųjų išlaidų programa neišsaugo šios informacijos išlaidų eilutėje:</p><ul><li>Projekto ID</li><li>Ar išlaidos yra apmokėtinos</li><li>Veiklos numeris</li></ul> |
| Kelionės ir išlaidos | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Lauke **Pridėti kvitai** nustatyta į Taip **,** net jei prie išlaidų eilutės nėra pridėtas kvitas. |
| Kelionės ir išlaidos | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Klaida įvyksta, kai pakeičiate išlaidų kategoriją į **Asmeninę**. |
| Kelionės ir išlaidos | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Negalite pridėti kvito ir redaguoti pirminių išlaidų, kai kredito kortelės operacija padalijama į asmenines išlaidas. |
| Kelionės ir išlaidos | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Vidinės įmonės operacijų, turinčių projekto ID, išlaidų strategija veikia netinkamai. |
| Kelionės ir išlaidos | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Užregistruotos datos informacijos trūksta užregistruotoms išlaidų ataskaitoms. |
| Kelionės ir išlaidos | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Mobiliojoje programėlėje Išlaidos yra mokėjimo būdo problemų. |
| Kelionės ir išlaidos | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Vienam darbuotojui sukurta kelionės paraiška gali būti naudojama kito darbuotojo išlaidų ataskaitai iki atstovo datos. |
| Kelionės ir išlaidos | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Kai kuriate išlaidas, finansinių dimensijų verčių pakeitimai nėra teisingai atnaujinami apskaitos paskirstymo lygiu **darbo srityje Išlaidų valdymas**. |
| Kelionės ir išlaidos | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Pagrindinės išlaidų eilutės patvirtinimo būsena nesinchronizuojama su detalizuotos eilutės darbo eigos patvirtinimo būsena. |
| Kelionės ir išlaidos | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Klaida įvyksta, jei registruojate išlaidų ataskaitą ir įgalintas mokesčių susigrąžinimas. |
| Kelionės ir išlaidos | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Atstovas negali panaikinti atleisto darbuotojo išlaidų dokumentų. |
| Kelionės ir išlaidos | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Išlaidų eilutės ištrynimas trunka ilgiau nei tikėtasi ir turi įtakos našumui. |
| Kelionės ir išlaidos | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** sukelia nenustatytą **TaxUncommitted** įrašą, nes panaikinamas tik **SourceDocumentLine**. |
| Kelionės ir išlaidos | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** neatitinka **trvExpTrans.ReferenceDataAreaId**, kad sukurtų naują numeraciją. |

## <a name="regulatory-updates"></a>Reguliavimo naujinimai

Informacijos apie "Finance and Operations" programų reguliavimo naujinimus ieškokite [reguliavimo naujinimai](/dynamics365/finance/localizations/regulatory-updates). Taip pat galite prisijungti prie Microsoft Dynamics "Lifecycle Services" (LCS) ir naudoti problemų paieškos įrankį, kad peržiūrėtumėte suplanuotus reguliavimo naujinimus. Problemų ieška leidžia ieškoti pagal šalį ar regioną, funkcijos tipą ir leidimą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
