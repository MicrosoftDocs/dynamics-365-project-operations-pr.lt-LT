---
title: Vidinės įmonės SF išrašymas
description: Šiame straipsnyje pateikiama informacija ir pavyzdžiai apie projektų vidinės įmonės SF išrašymą.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d1debf8f67b7dbe7752075c6f8e5f2cdd37a3ae
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002786"
---
# <a name="intercompany-invoicing"></a>Vidinės įmonės SF išrašymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija ir pavyzdžiai apie projektų vidinės įmonės SF išrašymą.

Jūsų organizaciją gali sudaryti keli skyriai, filialai ir kiti juridiniai subjektai, kurie, vykdydami projektus, keičiasi produktais ir paslaugomis. Juridinis subjektas, kuris teikia informaciją ar produktą, vadinamas *skolinančiu juridiniu subjektu*, o juridinis subjektas, kuris gauna paslaugą ar produktą, vadinamas *besiskolinančiu juridiniu subjektu*. 

Tolesnėje iliustracijoje pavaizduotas įprastas scenarijus, kai du juridiniai subjektai – SI FR (besiskolinantis juridinis subjektas) ir SI USA (skolinantis juridinis subjektas) – dalijasi ištekliais, kad įvykdytų kliento A projektą. Pagal šį scenarijų, SI FR sutartimi įpareigojamas atlikti darbą klientui A. 

[![Vidinės įmonės SF išrašymo pavyzdys](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Tikslas yra vidinių įmonių projektų operacijų išlaidų kontrolę, įplaukų pripažinimą, mokesčius ir perdavimo kainą padaryti lankstesnius ir veiksmingesnius. Be to, suteikiamos tolesnės galimybės.

-   Kliento SF kūrimas pagal besiskolinančio juridinio subjekto projektą, naudojant skolinančio juridinio subjekto vidinės įmonės grafikus, išlaidas ir tiekėjo SF.
-   Mokesčių skaičiavimo ir netiesioginių išlaidų palaikymas.
-   Skolinančio juridinio subjekto įplaukų pripažinimo atidėjimas ir laiko, kada besiskolinantis juridinis subjektas turėtų pripažinti išlaidas, atidėjimas.
-   Skolinančio juridinio subjekto nebaigtos gamybos (NG) įplaukų kaupimas.
-   Perkėlimo kainų, kurios gali būti grįstos įvairiais kainodaros modeliais, nustatymas. Štai keli pavyzdžiai:
    -   **Kiekis** – suma, įvesta lauke **Kainos**, yra faktinės kiekio arba vieneto išlaidos.
    -   **Išlaidų suma** – operacijos kaina / išlaidos ir išlaidų suma, įvesta lauke **Kainos**.
    -   **Išlaidų procentinis dydis** – perkėlimo kaina yra operacijos kaina / išlaidos, padaugintos iš išlaidų procentinio dydžio, įvesto lauke **Kainos**.
    -   **Pardavimo kainos procentinė dydis** – pardavimo kainos, perkeliamos skolinančiam juridiniam subjektui, procentinė dalis.
    -   **Suma, mažesnė už pardavimo kainą** – pardavimo kainos dalies suma, kurią besiskolinantis juridinis subjektas pasilieka prieš perkeldamas skolinančiam juridiniam subjektui.
    -   **Įnašo koeficientas** – skaičius, įvestas lauke **Kainos**, yra įnašo koeficientas, kuris išreiškiamas kaip pardavimo kainos procentinė dalis.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>1 pavyzdys: vidinės įmonės SF išrašymo parametrų nustatymas
Šiame pavyzdyje USSI yra skolinantis juridinio subjektas, o jo ištekliai teikia laiko ataskaitas pagal besiskolinantį juridinį subjektą, FRSI, kuris yra sudaręs sutartį su galutiniu klientu. Valandos ir išlaidos, apie kurias praneša USSI darbuotojai, gali būti įtrauktos į projekto SF, kurią sugeneravo FRSI. Be to, yra trečias operacijų šaltinis, kuris gali kilti iš skolinančio juridinio subjekto (šiame pavyzdyje – USSI), kai jis filialams (pvz., FRSI) suteikia bendrų tiekėjų paslaugas ir tada perkelia tas išlaidas į tų filialų projektus. Visus sutampančius SF dokumentus užpildo ir mokesčius suskaičiuoja „Finance“. 

Šiame pavyzdyje FRSI turi būti USSI juridinio subjekto klientas, o USSI turi būti FRSI juridinio subjekto tiekėjas. Tada galite nustatyti vidinės įmonės ryšį tarp dviejų juridinių subjektų. Tolesnėje procedūroje parodoma, kaip nustatyti parametrus, kad abu juridiniai subjektai galėtų dalyvauti išrašant vidinės įmonės SF.

1. Nustatykite FRSI kaip USSI juridinio subjekto klientą, o USSI nustatykite kaip FRSI juridinio subjekto tiekėją.  Šios užduoties veiksmams atlikti naudojamos trys įvesties vietos.

   | Veiksmas |                                                       Įvesties taškas                                                        |                                                                                                                                                                                               Aprašo                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | USSI spustelėkite <strong>Gautinos sumos</strong> &gt; <strong>Klientai</strong> &gt; <strong>Visi klientai</strong>. |                                                                                                                                                                  Sukurkite naują FRSI kliento įrašą ir pasirinkite klientų grupę.                                                                                                                                                                  |
   |  B   |    FRSI spustelėkite <strong>Mokėtinos sumos</strong> &gt; <strong>Tiekėjai</strong> &gt; <strong>Visi tiekėjai</strong>.     |                                                                                                                                                                    Sukurkite naują tiekėjo įrašą ir pasirinkite tiekėjų grupę.                                                                                                                                                                    |
   |  C   |                                  Pasirinkite FRSI ir atidarykite ką tik sukurtą tiekėjo įrašą.                                  | Veiksmų srityje, skirtuke <strong>Bendra</strong>, grupėje <strong>Nustatymas</strong> spustelėkite <strong>Vidinė įmonė</strong>. Puslapio <strong>Vidinė įmonė</strong> skirtuke <strong>Prekybiniai ryšiai</strong> nustatykite slankiklį <strong>Aktyvusis</strong> kaip <strong>Taip</strong>. Lauke <strong>Kliento įmonė</strong> pasirinkite kliento įrašą, kurį sukūrėte atlikdami A veiksmą. |


2. Spustelėkite **Projektų valdymo ir apskaita** &gt; **Sąranka** &gt; **Projektų valdymo apskaitos parametrai**, tada spustelėkite skirtuką **Vidinė įmonė**. Parametrų nustatymas priklauso nuo to, ar esate beskolinantis juridinis subjektas, ar skolinantis juridinis subjektas.
   -   Jei esate besiskolinantis juridinis subjektas, pasirinkite įsigijimo kategoriją, naudotiną siekiant gretinti tiekėjo SF, kurios sugeneruojamos automatiškai.
   -   Jei esate skolinantis juridinis subjektas, kiekvienam besiskolinančiam subjektui pažymėkite kiekvieno operacijos tipo numatytąją projekto kategoriją. Projekto kategorijos naudojamos mokesčių konfigūracijoje, kai vidinės įmonės operacijų SF išrašymo kategorija taikoma tik besiskolinančiam juridiniam subjektui. Galite pasirinkti, kaip kaupti vidinės įmonės operacijų įplaukas. Šis kaupimas atliekamas, kai operacijos yra registruojamos, ir jis atšaukiamas, kai vidinės įmonės SF yra užregistruota.

3. Spustelėkite **Projektų valdymas ir apskaita** &gt; **Sąranka** &gt; **Kainos** &gt; **Perkėlimo kaina**.
4. Pasirinkite valiutą, operacijos tipą ir perkėlimo kainos modelį. Valiuta, naudojama SF, yra valiuta, sukonfigūruojama skolinančio juridinio subjekto kliento įraše, skirtame besiskolinančiam juridiniam subjektui. Valiuta yra naudoja įrašams perkėlimo kainų lentelėje gretinti.
5. Spustelėkite **Didžioji knyga** &gt; **Registravimo sąranka** &gt; **Vidinės įmonės apskaita** ir nustatykite ryšį tarp USSI ir FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>2 pavyzdys: vidinės įmonės grafiko kūrimas ir registravimas
USSI, skolinantis juridinis subjektas, turi kurti ir registruoti FRSI, besiskolinančio juridinio subjekto, projekto grafiką. Šios užduoties veiksmams atlikti naudojamos dvi įvesties vietos.

| Veiksmas | Įvesties taškas                                                                       | Aprašo                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektų valdymas ir apskaita** &gt; **Grafikas** &gt; **Visi grafikai** | Sukurkite naują grafiką. Grafiko eilutės lauke **Juridinis subjektas** pasirinkite **FRSI**. Lauke **Projekto ID** pasirinkite FRSI projektą. Įveskite kiekvienos savaitės dienos valandas. |
| B    | Puslapis **Grafikas**                                                                | Paleidę darbo eigą, užregistruokite grafiką ir užsirašykite kvito numerį.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>3 pavyzdys: vidinės įmonės tiekėjo SF kūrimas ir registravimas
USSI, skolinantis juridinis subjektas, turi kurti ir registruoti FRSI, besiskolinančio juridinio subjekto, projekto vidinės įmonės tiekėjo SF. Šioje tiekėjo SF nurodoma užsakomųjų paslaugų darbo jėga ir išlaidos, kurias tiekėjams padengė USSI. Šios užduoties veiksmams atlikti naudojamos dvi įvesties vietos.

| Veiksmas | Įvesties taškas                                                                                      | Aprašo                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Mokėtinos sumos** &gt; **SF** &gt; **Atviros tiekėjų SF** &gt; **Nauja tiekėjo SF** | Sukurkite naują tiekėjo SF ir įveskite į paslaugas, kurios buvo įsigytos FRSI projekto vardu.                                                                                                                                                                                  |
| B    | Puslapis **Tiekėjo SF**                                                                      | Įveskite eilutes, kuriose nurodytos FRSI vardu užsakomos paslaugos. „FatstTab“ **Eilutės išsami informacija** SF eilutės skirtuke **Projektas**, lauke **Projekto įmonė** įveskite **FRSI**. Įveskite projektą ir atitinkamą informaciją. Tada užregistruokite tiekėjo SF. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>4 pavyzdys: vidinės įmonės SF kūrimas ir registravimas
USSI, skolinantis juridinis subjektas, turi sukurti ir užregistruoti vidinės įmonės SF. Šios užduoties veiksmams atlikti naudojamos dvi įvesties vietos.

| Veiksmas | Įvesties taškas                                                                                             | Aprašo                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projektų valdymas ir apskaita** &gt; **Projekto SF** &gt; **Vidinės įmonės kliento SF**  | Spustelėkite **Naujas**, kad atidarytumėte puslapį **Kurti vidinės įmonės SF**.                                                                                  |
| B    | **Projektų valdymas ir apskaita** &gt; **Projekto SF** &gt; **Vidinės įmonės kliento SF** | Puslapyje **Kurti vidinės įmonės sąskaitą faktūrą** įveskite juridinį subjektą, nurodykite norimą įtraukti operaciją, tada spustelėkite **Ieškoti**. |
| C    | **Projektų valdymas ir apskaita** &gt; **Projekto SF** &gt; **Vidinės įmonės kliento SF** | Pažymėkite operacijas, kurioms reikia išrašyti SF, spustelėkite **Žymėti viską**, jei norite išrašyti visų sąrašo operacijų SF, tada spustelėkite **Gerai**.                  |
| D    | Puslapis **Vidinės įmonės SF**                                                                       | Rodomas vidinės įmonės kliento SF pasiūlymas.                                                                                             |
| E    | Puslapis **Vidinės įmonės SF**                                                                       | Spustelėkite **Registruoti**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>5 pavyzdys: tiekėjo SF registravimas ir SF išrašymas klientui
Kai skolinantis juridinis subjektas, USSI, užregistruoja vidinės įmonės kliento SF, besiskolinančiame juridiniame subjekte, FRSI, sukuriama atitinkanti laukianti tiekėjo SF. Užregistravus šią tiekėjo SF, FRSI taip pat išrašo SF projekto klientui už USSI įvestas valandas.  Šios užduoties veiksmams atlikti naudojamos trys įvesties vietos.

| Veiksmas | Įvesties taškas                                                                                        | Aprašo                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Mokėtinos sumos** &gt; **SF** &gt; **Laukiančios tiekėjo SF**                            | Peržiūrėkite SF ir įsitikinkite, kad įtrauktos grafiko reikšmės, tada užregistruokite tiekėjo sąskaitą SF.                  |
| B    | **Projektų valdymas ir apskaita** &gt; **Projekto SF** &gt; **Projekto SF pasiūlymai** | Sukurkite naują projektui skirtą projekto SF ir patikrinkite, ar rodomos užregistruotos valandinės operacijos.            |
| C    | Puslapis **Projekto SF**                                                                       | Pažymėkite projekto SF, tada spustelėkite **Peržiūrėti išsamią informaciją** ir peržiūrėkite išlaidas ir pardavimo sumą. Tada užregistruokite SF. |


Daugiau informacijos žr. [Vidinės įmonės projektų SF išrašymo konfigūravimas](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]