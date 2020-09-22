---
title: Mobiliųjų įrenginių programėlės „Microsoft Dynamics 365 Project Timesheet“, skirtos „iOS“ ir „Android“, pasirinktinių laukų diegimas
description: Šioje temoje pateikiami įprasti būdai kaip naudoti plėtinius norint įdiegti pasirinktinius laukus.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: 4564bbda-34ea-4647-a9bc-f6ef17b1038b
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 16c3b79dcaaf8c5c491587618256694f82f44753
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753656"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Mobiliųjų įrenginių programėlės „Microsoft Dynamics 365 Project Timesheet“, skirtos „iOS“ ir „Android“, pasirinktinių laukų diegimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiami įprasti būdai kaip naudoti plėtinius norint įdiegti pasirinktinius laukus. Aprašomos šios temos:

- Įvairūs duomenų tipai, kuriuos palaiko pasirinktinio lauko sistema
- Kaip rodyti tik skaitomus arba redaguojamus grafiko įrašų laukus ir įrašyti vartotojo pateikiamas reikšmes į duomenų bazę
- Kaip rodyti tik skaitomus laukus grafiko antraštėje
- Kaip integruoti kitą pasirinktinę verslo logiką norint įvesti numatytąsias reikšmes į laukus ir atlikti papildomą tikrinimą

## <a name="audience"></a>Auditorija

Ši tema skirta programuotojams, integruojantiems pasirinktinius laukus į „Microsoft Dynamics 365 Project Timesheet“ mobiliųjų įrenginių programėlę, skirtą „Apple iOS“ ir „Google"Android“. Daroma prielaida, kad skaitytojai yra susipažinę su X++ kūrimu ir projekto grafikų funkcijomis.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Duomenų sutartis – „TSTimesheetCustomField“ X++ klasė

**TSTimesheetCustomField** klasė yra X++ duomenų sutarties klasė, kuri pateikia informaciją apie grafiko funkcijų pasirinktinį lauką. Pasirinktinio lauko objektų sąrašai perduodami į „TSTimesheetDetails“ duomenų sutartį ir „TSTimesheetEntry“ duomenų sutartį, kad būtų rodomi pasirinktiniai laukai mobiliųjų įrenginių programėlėje.

- **TSTimesheetDetails** – grafiko antraštės sutartis.
- **TSTimesheetEntry** – grafiko operacijos sutartis. Šių objektų grupės, turinčios tą pačią projekto informaciją ir **timesheetLineRecId**, sudaro eilutę.

### <a name="fieldbasetype-types"></a>fieldBaseType (tipai)

Ypatybė **FieldBaseType** objekte **TsTimesheetCustom** nustato lauko, kuris rodomas programėlėje, tipą. Toliau pateiktos palaikomos **Tipai** reikšmės.

| Tipų reikšmės | Tipas              | Pastabos |
|-------------|-------------------|-------|
| 0           | Eilutė (ir išvardijimas) | Laukas rodomas kaip teksto laukas. |
| 1           | Integer           | Reikšmė rodoma kaip skaičius be dešimtainių skilčių. |
| 2           | Tikroji              | Reikšmė rodoma kaip skaičius su dešimtainėmis skiltimis.<p>Norėdami tikrąją reikšmę programėlėje rodyti kaip valiutą, naudokite ypatybę **fieldExtenededType**. Ypatybę **numberOfDecimals** galite naudoti, jei norite nustatyti rodomų dešimtainių skilčių skaičių.</p> |
| 3           | Data              | Datos formatai nustatomi pagal vartotojo parametrą **Datos, laiko ir skaičiaus formatas**, kuris yra nustatytas **Kalbos ir šalies / regiono nuostata** dalyje **Vartotojo parinktys**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Jei ypatybė **stringOptions** nėra pateikta objekte **TSTimesheetCustomField**, laisvos formos teksto laukas pateikiamas vartotojui.

    Ypatybė **StringLength** gali būti naudojama norint nustatyti maksimalų eilutės ilgį, kurį vartotojai gali įvesti.

- Jei ypatybė **stringOptions** yra pateikta objekte **TSTimesheetCustomField**, šie sąrašo elementai yra vienintelės reikšmės, kurias vartotojai gali pažymėti naudodami parinkčių mygtukus (išrinkimo mygtukus).

    Tokiu atveju eilutės laukas gali veikti kaip išvardijimo reikšmė, skirta vartotojo įrašui. Norėdami įrašyti reikšmę į duomenų bazę kaip išvardijimą, rankiniu būdu (naudodami komandų grandinę) susiekite eilutės reikšmę prieš įrašydami į duomenų bazę (kaip pavyzdį žr. tolesnį šios temos skyrių „TSTimesheetEntryService“ klasės komandų grandinės naudojimas norint įrašyti grafiko įrašą iš programėlės į duomenų bazę“).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Naudodami šią ypatybę, galite formatuoti tikrąsias reikšmes kaip valiutą. Šis metodas taikomas tik tada, kai **fieldBaseType** reikšmė yra **Tikroji**.

- **TSCustomFieldExtendedType:None** – formatavimas netaikomas.
- **TSCustomFieldExtendedType::Currency** – reikšmės formatavimas kaip valiutos.

    Kai valiutos formatavimas aktyvus, lauką **stringValue** galima naudoti norint perduoti valiutos kodą, kuris turi būti rodomas programėlėje. Reikšmė yra tik skaitoma.

    Lauke **realValue** yra rodoma pinigų suma, kurią reikia įrašyti į duomenų bazę.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Galite naudoti šią ypatybę norėdami nurodyti, kur programėlėje turi būti rodomas pasirinktinis laukas.

- **TSCustomFieldSection::Header** – laukas bus rodomas programėlės skyriuje **Žiūrėti daugiau informacijos**. Šie laukai visada yra tik skaitomi.
- **TSCustomFieldSection::Line** – laukas bus rodomas po visų paruoštų eilutės laukų grafiko įrašuose. Šiuos laukus galima arba redaguoti, arba tik skaityti.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Ši ypatybė nustato lauką, kai reikšmės, kurias pateikia programėlė, įrašomos atgal į duomenų bazę.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Ši ypatybė nustato lauką, kai reikšmės, kurias pateikia programėlė, įrašomos atgal į duomenų bazę.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Nustatykite šią ypatybę kaip **Taip**, jei norite, kad lauką grafiko įrašo skyriuje galėtų redaguoti vartotojai. Nustatykite ypatybę kaip **Ne**, kad laukas būtų tik skaitomas.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Nustatykite šią ypatybę kaip **Taip**, jei norite, kad laukas grafiko įrašo skyriuje būtų privalomas.

### <a name="label-str"></a>label (str)

Ši ypatybė nurodo žymą, kuri rodoma šalia lauko programėlėje.

### <a name="stringoptions-list-of-strings"></a>stringOptions (eilučių sąrašas)

Ši ypatybė taikoma tik tada, kai **fieldBaseType** yra nustatytas kaip **Eilutė**. Jei **stringOptions** yra nustatytas, eilutės reikšmės, kurias galima pasirinkti naudojant parinkčių mygtukus (išrinkimo mygtukus), nurodomos sąrašo eilutėmis. Jei nėra jokių eilučių, galima naudoti lauko laisvos formos įrašo eilutės (pavyzdys pateiktas šios temos tolimesniame skyriuje „TSTimesheetEntryService“ klasės komandų grandinės naudojimas norint įrašyti grafiko įrašą iš programėlės atgal į duomenų bazę“).

### <a name="stringlength-int"></a>stringLength (int)

Ši ypatybė nurodo maksimalų eilutės lauko ilgį. Ji taikoma tik tada, kai **fieldBaseType** yra nustatytas kaip **Eilutė**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Šios ypatybės nurodo dešimtainių skilčių, kurios rodomos tikrajam laukui, skaičių. Ji taikoma tik tada, kai **fieldBaseType** yra nustatytas kaip **Tikrasis**.

### <a name="ordersequence-int"></a>orderSequence (int)

Ši ypatybė valdo tvarką, kuria pasirinktiniai laukai rodomi programėlėje, kai nurodomas daugiau nei vienas pasirinktinis laukas. Laukai, kuriuose yra mažesni skaičiai, rodomi pirmiausia.

### <a name="booleanvalue-boolean"></a>booleanValue (Bulio logikos)

**Bulio logikos** tipo laukams, ši ypatybė perduoda lauko Bulio logikos reikšmę tarp serverio ir programėlės.

### <a name="guidvalue-guid"></a>guidValue (guid)

**GUID** tipo laukams, ši ypatybė perduoda lauko globaliai unikalaus identifikatoriaus (GUID) reikšmę tarp serverio ir programėlės.

### <a name="int64value-int64"></a>int64Value (Int64)

**Int64** tipo laukams, ši ypatybė perduoda lauko „int64“ reikšmę tarp serverio ir programėlės.

### <a name="intvalue-int"></a>intValue (INT)

**Int** tipo laukams, ši ypatybė perduoda lauko „int“ reikšmę tarp serverio ir programėlės.

### <a name="realvalue-real"></a>realValue (Real)

**Tikrasis** tipo laukams, ši ypatybė perduoda lauko tikrąją reikšmę tarp serverio ir programėlės.

### <a name="stringvalue-str"></a>stringValue (str)

**Eilutė** tipo laukams, ši ypatybė perduoda lauko eilutės reikšmę tarp serverio ir programėlės. Ji taip pat naudojama **Tikrasis** tipo laukams, kurie suformatuoti kaip valiuta. Šiuose laukuose ypatybė naudojama valiutos kodui į programėlę perduoti.

### <a name="datevalue-date"></a>dateValue (date)

**Data** tipo laukams, ši ypatybė perduoda lauko datos reikšmę tarp serverio ir programėlės.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Pasirinktinio lauko rodymas ir įrašymas grafiko įrašo skyriuje

Toliau pateikiama grafiko įrašo kūrimo mobiliųjų įrenginių programėlėje ekrano kopija. Joje rodomi paruošti laukai ir pasirinktinis laukas skyriuje „Laiko įrašas“, pavadinimu „Testavimo eilutė“, su jau nustatyta „Antroji parinktis“ reikšme.

![Testavimo eilutės pasirinktinis laukas programėlėje](media/timesheet-entry.jpg)



Toliau pateikiama mobiliųjų įrenginių programėlės ekrano kopija, kurioje vartotojas pasirenka vieną iš išvardijimo parinkčių, pasiekiamų pasirinktiniam laukui „Testavimo eilutė“.  Dvi parinktys – „Pirmoji parinktis“ ir „Antroji parinktis“ – yra rodomos kaip išrinkimo mygtukai. Šiuo metu pasirinkta antroji parinktis.

![Parinkčių mygtukai (išrinkimo mygtukai), skirti testavimo eilutės pasirinktiniam laukui](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Išplėskite lentelę „TSTimesheetLine“, kad joje būtų pasirinktinis laukas

Esant įprastam scenarijui, gali būti, kad duomenys, skirti pasirinktiniam laukui grafiko įrašo skyriuje, bus įrašyti į lentelę „TSTimesheetLine“. Tačiau galima naudoti kitas lenteles, jei duomenys gali būti nuskaitomi pagal „TSTimesheetTrans“ įrašą, kuris yra pateiktas, arba jei jis neturi specifinio įrašo konteksto (pavyzdžiui, jei lauko reikšmė nustatyta kaip tik skaitomas projekto parametruose).

Atkreipkite dėmesį, kad pasirinktiniai laukai neturi jokio atsarginio duomenų bazės įrašo. Jie gali būti dinamiškai sugeneruoti pagal X++ logiką. Šis metodas gali būti naudingas tik skaityti galimuose scenarijuose (dinamiškai sugeneruotų pasirinktinio lauko verčių pavyzdį žr. skyriuje „Komandų grandinės naudojimas klasės „TSTimesheetDetails“ metode „buildCustomFieldListForHeader“ norint užpildyti grafiko išsamią informaciją“).

Toliau pateikiama taikomosios programos objektų medžio „Visual Studio“ ekrano kopija. Joje rodomas lentelės „TSTimesheetLine“ plėtinys su „TestLineString“ lauku, įtrauktu kaip pasirinktinis laukas.

![Atskira eilutė](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Naudokite komandų grandinę, esančią metode „buildCustomFieldList“ klasėje „TSTimesheetSettings“, kad galėtumėte rodyti lauką grafiko įrašo skyriuje

Šis kodas valdo lauko rodymo parametrus programėlėje. Pavyzdžiui, jis valdo lauko tipą, žymą, ar laukas yra privalomas ir kokiame skyriuje rodomas laukas.

Tolimesniame pavyzdyje rodomas eilutės laukas laiko įrašuose. Šiame lauke yra dvi parinktys – **Pirmoji parinktis** ir **Antroji parinktis**, pasiekiamos parinkčių mygtukais (išrinkimo mygtukais). Programėlės laukas yra susietas su lauku **TestLineString**, kuris yra įtraukiamas į lentelę „TSTimesheetLine“.

Atkreipkite dėmesį, kad **TSTimesheetCustomField::newFromMetatdata()** metodas naudojamas siekiant supaprastinti šių pasirinktinio lauko ypatybių inicijavimą: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ir **numberOfDecimals**. Taip pat galite nustatyti šiuos parametrus rankiniu būdų, jei to pageidaujate.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Naudokite komandų grandinę, esančią metode „buildCustomFieldListForEntry“ klasėje „TSTimesheetEntry“, kad įvestumėte reikšmes į grafiko įrašą

Metodas **buildCustomFieldListForEntry** naudojamas norint įvesti reikšmes į įrašytas grafiko eilutes mobiliųjų įrenginių programėlėje. Kaip parametras naudojamas „TSTimesheetTrans“ įrašas. Laukai iš to įrašo gali būti naudojami pasirinktinio lauko vertei užpildyti programėlėje.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Naudokite komandų grandinę klasėje „TSTimesheetEntryService“, kad atgal į duomenų bazę įrašytumėte grafiko įrašą

Norėdami vėl įrašyti pasirinktinį lauką į duomenų bazę įprasto naudojimo metu, turite išplėsti kelis metodus.

- Metodas **timesheetLineNeedsUpdating** naudojamas norint nustatyti, ar programėlėje vartotojas pakeitė eilutės įrašą ir jis turi būti įrašytas į duomenų bazę. Jei našumo problema neaktuali, šį metodą galima supaprastinti, kad jis visada grįžtų į reikšmę **teisinga**.
- Metodus **populateTimesheetLineFromEntryDuringCreate** ir **populateTimesheetLineFromEntryDuringUpdate** galima išplėsti, kad jie įvestų reikšmes į „TSTimesheetLine“ duomenų bazę iš pateikto „TSTimesheetEntry“ duomenų sutarties įrašo. Pateiktame pavyzdyje atkreipkite dėmesį į tai, kaip duomenų bazės lauko ir įvesties lauko susiejimas rankiniu būdu atliekamas naudojant X++ kodą.
- Metodą **populateTimesheetWeekFromEntry** taip pat galima išplėsti, jei pasirinktinis laukas, susietas su objektu **TSTimesheetEntry**, turi būti įrašytas atgal į „TSTimesheetLineweek“ duomenų bazę.

> [!NOTE]
> Toliau pateiktame pavyzdyje įrašoma **firstOption** arba **secondOption** reikšmė, kurią vartotojas pasirenka duomenų bazėje kaip pirminę eilutės reikšmę. Jei duomenų bazės laukas yra **Išvardijimas** tipo laukas, šias reikšmes galima rankiniu būdu susieti su išvardijimo reikšme ir tada įrašyti į duomenų bazės lentelės išvardijimo lauką.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Pasirinktinio lauko rodymas grafiko antraštės skyriuje

Toliau pateikiama mobiliųjų įrenginių programėlės ekrano kopija, kurioje vartotojas peržiūri grafiką. Mygtukas „Daugiau informacijos“ buvo pažymėtas viršutiniame dešiniajame kampe, kad būtų rodoma parinktis „Žiūrėti daugiau informacijos“.  

![Komanda „Žiūrėti daugiau informacijos“](media/show-more.png)

Toliau pateikiama mobiliųjų įrenginių programėlės grafiko skyriaus „Daugiau“ ekrano kopija. Pasirinktinis laukas, vadinamas „Šio grafiko naudingumo koeficientas (apskaičiuotas pasirinktinis laukas)“, įtrauktas į grafiko antraštės skyrių. Pasirinktiniam laukui nustatoma tik skaitymo reikšmė „0,667“.

![Daugiau skyrių](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Išplėskite lentelę „TSTimesheetTable“, kad joje būtų pasirinktinis laukas

Esant įprastam scenarijui, gali būti, kad duomenys, skirti pasirinktiniam laukui antraštės skyriuje, bus ištraukti iš lentelės „TSTimesheetHeader“. Tačiau galima naudoti kitas lenteles, jei duomenys gali būti nuskaitomi pagal „TSTimesheetTable“ įrašą, kuris yra pateiktas, arba jei jis neturi specifinio įrašo konteksto (pavyzdžiui, jei lauko reikšmė nustatyta kaip tik skaitomas projekto parametruose).

Atkreipkite dėmesį, kad pasirinktiniai laukai neturi jokio atsarginio duomenų bazės įrašo. Jie gali būti dinamiškai sugeneruoti pagal X++ logiką. Šis metodas parodytas tolesniame pavyzdyje.

Antraštės skyriaus laukai programėlėje visada yra tik skaitomi.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Naudokite komandų grandinę, esančią metode „buildCustomFieldList“ klasėje „TSTimesheetSettings“, kad galėtumėte rodyti lauką antraštės skyriuje

Šis kodas valdo lauko rodymo parametrus programėlėje. Pavyzdžiui, jis valdo lauko tipą, žymą, ar laukas yra privalomas ir kokiame skyriuje rodomas laukas.

Toliau pateiktame pavyzdyje rodoma apskaičiuota reikšmė programėlės antraštės skyriuje.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Naudokite komandų grandinę, esančią metode „buildCustomFieldListForHeader“ klasėje „TSTimesheetDetails“, kad užpildytumėte grafiko išsamią informaciją

Metodas **buildCustomFieldListForHeader** naudojamas norint užpildyti grafiko antraštės išsamią informaciją mobiliųjų įrenginių programėlėje. Kaip parametras naudojamas „TSTimesheetTable“ įrašas. Laukai iš to įrašo gali būti naudojami pasirinktinio lauko vertei užpildyti programėlėje. Toliau pateiktame pavyzdyje nenuskaitomos jokios reikšmės iš duomenų bazės. Vietoje to naudojama X++ logika, pagal kurią sugeneruojama apskaičiuota reikšmė, kuri rodoma programėlėje.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Kitos konfigūravimo / išplėtimo galimybės

### <a name="adding-additional-validation-for-the-app"></a>Papildomo programėlės tikrinimo įtraukimas

Esama grafiko funkcijų duomenų bazėje logika ir toliau veiks, kaip numatyta. Kad būtų nutrauktos įrašymo arba pateikimo operacijos ir rodomas konkretus klaidos pranešimas, į kodą naudodami komandų plėtinio grandinę galite įtraukti **rodyti klaidą („pranešimas vartotojui“)**. Toliau pateikiami trys naudingi išplečiamų metodų pavyzdžiai.

- Jei grafiko eilutės įrašymo operacijos metu **validateWrite** lentelėje „TSTimesheetLine“ rodo **klaida**, mobiliųjų įrenginių programėlėje rodomas klaidos pranešimas.
- Jei grafiko pateikimo į programėlę operacijos metu **validateSubmit** lentelėje „TSTimesheetTable“ rodo **klaida**, vartotojui rodomas klaidos pranešimas.
- Logika, kuri užpildo laukus (pvz., **Eilutės ypatybė**), kai lentelėje „TSTimesheetLine“ naudojamas metodas **įterpti**, vis dar veiks.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Paruoštų laukų paslėpimo ir pažymėjimo tik kaip skaitomų konfigūravimas

Projekto parametruose galite nustatyti, kad paruošti laukai mobiliųjų įrenginių programėlėje būtų tik skaitomi arba paslėpti. Nustatykite parinktis puslapio **Projektų valdymo ir apskaitos parametrai** skyriaus **Mobiliųjų įrenginių grafikai** skirtuke **Grafikas**.

![Projekto parametrai](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Veiklų, kurias galima pasirinkti naudojant plėtinius, keitimas

Veiklos, kurias galima pasirinkti projektui, užpildomos naudojant metodus **getActivitiesForProject()** ir **getActivityQuery()** klasėje **TsTimesheetProjectService**. Galite naudoti komandų grandinę, kad pakeistumėte šį veikimą, ir veiklos, kurias galite pasirinkti konkrečiam objektui, atitiktų jūsų verslo scenarijų.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Numatytosios projekto kategorijos įvedimas į grafiko įrašus

Numatytosios projekto kategorijos įrašas grafiko įrašuose pateikiamas trimis lygiais. Galite naudoti komandų grandinę, kad išplėstumėte bet kurio ar visų šių lygių veikimą ir pasiektumėte pageidaujamą veikimą. Naudojama tolesnė hierarchija.

1. Programėlė bando įvesti numatytąją kategoriją iš projekto išteklių. Ši numatytoji kategorija yra nustatyta metoduose **getCurrentUserResource** ir **getDelegatedResourcesForCurrentUser** klasėje **TSTimesheetSettingsService**.
2. Jei numatytoji kategorija nepateikta projekto išteklių lygyje, programėlė bando ją ištraukti iš projekto veiklos. Ši numatytoji kategorija yra nustatyta metode **getActivitiesForProject** klasėje **TSTimesheetProjectService**.
3. Jei numatytoji kategorija nepateikta projekto veiklos lygyje, numatytoji kategorija paimama iš projekto parametrų. Ši numatytoji kategorija yra nustatyta metode **getProjectDetailsbyRule** klasėje **TSTimesheetProjectService**.
