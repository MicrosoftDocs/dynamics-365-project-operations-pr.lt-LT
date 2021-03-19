---
title: Pardavimų procesai
description: Šioje temoje pateikiama informacija apie pagrindinius pardavimo procesus.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ad32757821a4cf966abd0b98cc4632dece613bc4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291089"
---
# <a name="sales-processes"></a>Pardavimų procesai

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Organizacijoje, kurios veikla pagrįsta projektu, naudojami pardavimo procesai skiriasi nuo pardavimų procesų, naudojamų organizacijoje, kurios veikla pagrįsta produktais. Šis skirtumas atsiranda todėl, kad organizacijų, kurių veikla pagrįsta projektu, pardavimo ciklai yra ilgesni ir jiems reikia tinkintų įvertinimo technologijų, kad galėtų išanalizuoti ir kurti visų sandorių pasiūlymus. „Dynamics 365 Project Service Automation“ naudoja tam tikras funkcijas, kurios naudojamos „Dynamics 365 Sales“ pardavimo procese. Štai keli pavyzdžiai:

- Pardavimo procesas sekamas naudojant objektą Galimas klientas.
- Tinkami galimi klientai sekami kaip galimybės. Pardavimo procesą taip pat galima pradėti nuo galimybės.
- Pasitelkiami visi susiję galimybės artefaktai. Šie artefaktai apima pardavimo komandą, suinteresuotąsias šalis, tikimybę, įvertinimą, pardavimo etapus ir veiklos procesus.
- Sukuriami keli galimybės pasiūlymai.
- Pasiūlymas pažymimas **Uždarytas kaip laimėtas** ir sukuriamas pardavimo užsakymas. Naudojant PSA pardavimo užsakymas yra tinkintas ir vadinamas projekto sutartimi.

Tolesnėje iliustracijoje parodytas tipinis organizacijos, kurios veikla pagrįsta projektu, pardavimo procesas.

> ![Pardavimo procesas organizacijoje, kurios veikla pagrįsta projektu](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Pardavimo įvertinimas
Pardavimo vertę galima apskaičiuoti pagal anksčiau pristatytus projektus ir projektų sudėtingumą. Jei projektas yra ankstesnių projektų tęsinys arba projektą vykdo labai patyręs tiekėjas, naudojantis gerai žinomus darbo šablonus, galite naudoti paprastesnį įvertinimo procesą. Sudėtingesnių projektų pirkimo procesas paprastai būna ilgesnis. Todėl pardavimo įvertinimo procesą sudaro daugiau etapų. Proceso pradžioje pardavimo komanda, naudodama klientų vadybininkų ir srities ekspertų įvestis, pradeda kurti aukšto lygio kiekvieno atskiro pasiūlyto darbų komponento įvertinimą. Šie darbų komponentai nurodomi pasiūlymo eilutėse. 

Galite sukurti aukšto lygio pasiūlymo įvertinimą. Vėliau šį aukšto lygio įvertinimą pakeisite išsamesniu įvertinimas, pagrįstu projekto planu, kurį sukursite naudodami standartizuotus projekto šablonus. Šie šablonai naudingi kuriant grafiką ir nustatant pinigines pasiūlymo bei jo komponentų vertes (pasiūlymo eilutes). 

Galite sukurti kelis projekto pasiūlymus ir sugrupuoti juos į vieną objekto tipą Galimybė. Galiausiai vienas iš šių pasiūlymų pažymimas **Uždarytas kaip laimėtas** ir sukuriama projekto sutartis arba darbų sąrašas (SOW). Į projekto sutartį įtraukiamos visų komponentų (sutarties eilučių), kuriuos klientas sutiko pristatyti, sutartos vertės. SOW paprastai kuriamas kaip „Microsoft Word“ dokumentas. Visose sąskaitose faktūrose, siunčiamose klientui vykdant projekto sutartį, nurodoma projekto sutartis arba SOW.

Be to, galite sukurti alternatyvių pasiūlymų naudodami vieną objekto tipą Galimybė arba nustatyti sistemą, kad projekto sutartis būtų sukurta laimėjus pasiūlymą. Šiuo atveju prie projekto sutarties įrašo galite pridėti SOW „„Word““ dokumentą.

![Pasiūlymo uždarymas siekiant sukurti projekto sutartį](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Pardavimo proceso konfigūravimas
Norėdami sukonfigūruoti pardavimo procesą, programoje „Microsoft Dynamics 365“ galite naudoti veiklos procesų sekas. Veiklos procesų eigos teikia pardavimo darbuotojams interaktyviąją vaizdinę sąsają, kuria naudodamiesi jie gali perduoti sandorius iš vieno tipinio įmonės etapo į kitą.

Pavyzdžiui, jūsų įmonės pardavimo procesą gali sudaryti šeši toliau išvardyti etapai.

1. Patvirtinti tinkamumą
2. Numatyti
3. Vidinė peržiūra
4. Sutartis
5. Pristatyti
6. Uždaryti

Šiuos šešis etapus nurodo ševronai (\>), kuriuos galite pasirinkti išplėsti kiekviename sukurtame objekto Galimybė tipe.

![Veiklos procesų konfigūravimas programoje „Dynamics 365“](media/basic-guide-3.png)
 
Vykdydama tą patį sandorį organizacija gali naudoti įvairius objektus jam nurodyti. Pardavimo proceso pradžioje sandorį nurodo objektas Galimybė. Laikui bėgant gavę daugiau informacijos galite naudoti aukšto lygio įvertinimus ir sukurti vieną ar kelis pasiūlymus. Jei vieną iš šių pasiūlymų peržiūri vidaus ir kliento suinteresuotosios šalys, sandoris nurodomas kaip objektas Pasiūlymas. Klientui priėmus pasiūlymą, sandorį nurodo projekto sutartis arba SOW. Siekiant palaikyti šį veikimo principą veiklos procesų eigos yra sudarytos taip, kad kiekvienas proceso etapas būtų susietas su skirtinga duomenų bazės lentele.

Pardavimo proceso etapą **Patvirtinimas** galima susieti su objektu Galimybė. Etapus **Įvertinimas** ir **Vidinė peržiūra** galima susieti su objektu Pasiūlymas. Etapus **Sutartis**, **Pristatymas** ir **Uždarymas** galima susieti su objektu Projekto sutartis.

Vykdydami sandorio etapus būsite paraginti sukurti atitinkamą objekto įrašą, kad galėtumėte lengviau ir tiksliau atlikti procesą. Etapai gali būti sąlyginiai. Pavyzdžiui, jei jums pasiūlymo vidinės peržiūros jums tik tuo atveju, jei pasiūlymui naudojamas pasirinktinis kainoraštis, galite sukonfigūruoti šią sąlygą atitinkamame veiklos proceso etape. Tada etapas **Vidinė peržiūra** bus rodomas tik pasiūlymuose, kuriems naudojamas pasirinktinis kainoraštis. Visų kitų sandorių ir pasiūlymų atveju po etapo **Įvertinimas** vykdomas etapas **Sutartis**.

> [!NOTE]
> PSA yra specialūs objektų Galimybė, Pasiūlymas, Užsakymas ir Sąskaita faktūra puslapiai. „Project Service“ galimybes, pasiūlymus, užsakymus ir sąskaitas faktūras reikia kurti naudojant šių objektų projekto informacijos puslapius. Jei kurdami įrašą naudosite kitą puslapį, negalėsite atidaryti įrašo puslapyje **Projekto informacija**. Norėdami atidaryti įrašą iš puslapio **Projekto informacija**, turėsite panaikinti įrašą ir iš naujo jį sukurti naudodami puslapį **Projekto informacija**. Puslapyje **Projekto informacija** kiekvieno iš šių objektų verslo logika užtikrina, kad įrašo laukas **Tipas** būtų tinkamai nustatytas ir visos privalomos koncepcijos būtų tinkamai inicijuotos.

> ![Naujo užsakymo projekto informacija](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Skirtumai tarp „Project Service Automation“ ir „Sales“
Nors PSA pardavimo procesui naudojamos pagrindines „Sales“ pardavimo proceso funkcijos, jis iš esmės skiriasi, nes organizacijų, kurių veikla pagrįsta projektu, verslo veiklos yra skirtingos. Štai keli pavyzdžiai:

- **Projekto pasiūlymai** – programoje „Project Service Automation“ pasiūlymas uždaromas, kai iš pasiūlymo sukuriama projekto sutartis. Programoje „Sales“ laimėję pasiūlymą galite palikti jį atidarytą. Šio skirtumo priežastis yra ta, kad organizacijų, kurių veikla pagrįsta projektu, atitiktis tarp pasiūlymo ir projekto sutarties yra geresnė. 
- **Aktyvinimas ir peržiūrėjimas** – PSA nepalaiko projektų pasiūlymų aktyvinimo ir peržiūros funkcijų. Naudojant „Sales“ pasiūlymą galima užrakinti ir neleisti daugiau redaguoti.
- **Pasiūlymo kaip pralaimėto arba laimėto uždarymas** – naudojant PSA, kai projekto pasiūlymas uždaromas kaip laimėtas arba pralaimėtas, galimybė lieka atidaryta. Visi kiti galimybės pasiūlymai uždaromi kaip pralaimėti. Kai pasiūlymas uždaromas kaip laimėtas arba pralaimėtas, vartotojas paraginamas imtis su galimybe susijusių veiksmų. Atsižvelgiant į vartotojo įvestį, pamatinė galimybė gali būti uždaryta arba palikta atidaryta.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Pardavimo ciklo pasiūlymų ir projektų planų peržiūrų sekimas
Naudodami PSA negalite sekti atliktų pasiūlymo peržiūrų. Turite pažymėti esamą pasiūlymą **Uždarytas kaip pralaimėtas**, o tada sukurti naują pasiūlymą. Naudodami PSA galite nukopijuoti pasiūlymą arba klonuoti projektu pagrįstą pasiūlymą.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Pasiūlymų ir projektų sutarčių komentarų bei patvirtinimų sekimas
Naudodami įrašų sieną ir įrašus galite valdyti pasiūlymų ir projektų sutarčių peržiūrą bei patvirtinimą. Siekdama priskirti, peradresuoti, perskirti ir valdyti peržiūros ir patvirtinimo darbų elementų pranešimus organizacija gali kurti pasirinktines darbo eigas ir priedus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]