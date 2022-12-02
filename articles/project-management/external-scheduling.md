---
title: Išorinis planavimas
description: Šiame straipsnyje pateikta informacija apie išorinį planavimą.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736990"
---
# <a name="external-scheduling"></a>Išorinis planavimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Naudojant išorinio planavimo režimą galima kurti, naujinti ir naikinti objektus, susijusius su darbo paskirstymo struktūromis (WBS) be dabartinių apribojimų, kuriuos vykdo „Microsoft Project for the Web“. Jis taip pat užtikrina ribotą tikrinimą. Šį režimą gali naudoti tik šie klientai:

- Klientai, kurie turi įrankius, kurių reikia WBS apibrėžti ne planavimo logikoje, kurią teikia „Project Operations“
- Klientai, kurie turi valdyti grafikų hierarchiją, priklausomybes arba užduoties trukmę

> [!IMPORTANT]
> Duomenys, netinkamai įvesti į WBS susijusius objektus, gali būti nerodomi išteklių suderinimo tinklelyje, įvertinimų tinklelyje, sekimo tinklelyje arba išteklių priskyrimo tinklelyje.

## <a name="configuration"></a>Konfigūravimas

Pagal numatytuosius nustatymus ši funkcija įjungta. Tačiau parengtame naudoti pagrindiniame projektų puslapyje pagal numatytuosius nustatymus susijęs laukas nerodomas. Norėdami įjungti šį lauką, naudokite „Maker Portal“ ir atidarykite pagrindinį projekto objekto puslapį, pasirinkite lauką **Planavimo modulis**, tada pakeiskite, kad lauką būtų **Matomas pagal numatytuosius nustatymus** . Jei nenaudojate parengto naudoti projekto pagrindinio puslapio, redaguokite esamą puslapį ir į jį įtraukite lauką **Planavimo modulis**.

## <a name="settings"></a>Parametrai

Norėdami naudoti išorinio planavimo režimą, pirma turite sukurti naują projektą ir išplečiamajame sąraše, esančiame projekto pagrindiniame puslapyje, pasirinkti planavimo modulį **Suplanuota iš išorės** . Nustačius šį projekto režimą, jo pakeisti negalima.

## <a name="viewing-the-wbs"></a>WBS peržiūra

Jei projektas suplanuotas iš išorės, to projekto prieiga prie „Project for the Web“ yra ribojama. Norėdami peržiūrėti WBS, turite pereiti į sekimo tinklelį, kuriame rodomas visos WBS.

## <a name="creating-and-editing-the-wbs"></a>WBS kūrimas ir redagavimas

Jei įjungtas projekto išorinis planavimas, turite apibrėžti visų su WBS susijusių objektų duomenis, įskaitant užduotis, komandos narius, išteklių priskyrimus ir priklausomybes.

Toliau pateiktoje iliustracijoje parodytas projekto planavimo duomenų modelis.

![Projektų planavimo duomenų modelis.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funkcijų apribojimai

Su iš išorės suplanuotais projektais neleidžiama atlikti toliau nurodytų operacijų.

### <a name="project-planning"></a>Projekto planavimas

- **Kopijuoti projektą** – ši operacija nepalaikoma išoriškai suplanuotose projektuose.
- **Perkelti projektą** – projekto pradžios datos pakeitimai neperkels užduočių arba išteklių priskyrimų pradžios WBS.
- **Projekto vadovo naujinimas** – projekto vadovo pakeitimai pagrindiniame projekto puslapyje automatiškai nesukurs naujo projekto komandos nario, kol projektas nebus konvertuotas.
- **Projekto darbo valandų šablono naujinimas** – dėl projekto darbo valandų šablono pakeitimų nebus perskaičiuotas projekto grafikas.
- **Išteklių priskyrimo kontūrai** – dėl išteklių priskyrimų kūrimo nebus automatiškai atnaujintas laukas **mdyn\_PlannedWork**. Šis laukas naudojamas išteklių priskyrimo pastangų kontūrams saugoti. Jei išteklių priskyrimo tinklelyje arba išteklių suderinimo tinklelyje norėsite rodyti laipsniškai laike išdėstytas pastangas, turėsite apibrėžti tinkamus išteklių priskyrimo kontūrus. Šie kontūrai turi būti tinkamai suformatuoti, kad jie paleistų skaičiavimą ir savikainos, ir pardavimo kainos kontūruose. Rekomenduojame sukurti bandomąjį projektą, kuris būtų suplanuotas naudojant „Project for the Web“, tada peržiūrėti susijusius duomenis, kad būtų galima patvirtinti reikalavimus ir formatavimą.

### <a name="resource-management"></a>Išteklių valdymas

- **Bendrasis išteklių įvykdymas** – iš išorės suplanuotų projektų bendrųjų išteklių įvykdymas nepalaikomas. Bandant įvykdyti aktyvius atvirus reikalavimus, bus sukurti nauji projekto komandos nariai, tačiau dėl to nebus panaikintas ar pakeistas bendrasis komandos narys jokiuose esamuose išteklių priskyrimuose.
- **Naikinti komandos narį** – panaikinus komandos narį nebus automatiškai panaikinti išteklių priskyrimai.

### <a name="quoting-and-contracting"></a>Pasiūlymų teikimas ir sutarčių sudarymas

- **Pasiūlymo eilutės ir sutarties eilutės išsamios informacijos importavimas** – iš projekto importuojant pasiūlymo arba sutarties eilutės išsamią informaciją, programa buvo testuota, kad WBA palaikytų daugiausia 500 užduočių, remiantis 20 priskyrimų limitu vienai užduočiai.

### <a name="actuals-and-invoicing"></a>Faktiniai duomenys ir sąskaitų faktūrų išrašymas

- Nors ir nėra WBS ir finansinių operacijų esamų tikrinimų pakeitimų, svarbu, kad būtų atitikimas parengtam naudoti duomenų modeliui, norint užtikrinti, kad visos tolesnės operacijos būtų vykdomos kaip numatyta.
