---
title: Organizacinius vienetus
description: Šiame straipsnyje aprašoma organizacinių vienetų sąvoka ir paaiškinama, kaip kurti ir prižiūrėti organizacinius vienetus programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921634"
---
# <a name="organizational-units-overview"></a>Organizacinių vienetų apžvalga

Programoje "Microsoft" Dynamics 365 Project Operations organizacinis *vienetas* yra atskira profesionalių paslaugų įmonės grupė arba padalinys, kuriame naudojami apmokėtini ištekliai, turintys išlaidų tarifus.

Profesinių paslaugų įmonėms, kurios naudoja techninius išteklius įvairiose praktikos srityse ar verslo linijose, vaidmens užpildymo išlaidos gali skirtis, priklausomai nuo praktikos srities ar verslo linijos, kurioje vaidmuo yra užpildytas. Šiame scenarijuje organizacinių vienetų sąvoka padeda suteikti galimybę sugrupuoti apmokestinamų vaidmenų rinkinį įmonės padalinyje, kuris turi atskirą šių vaidmenų sąnaudų struktūrą.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Organizacinių vienetų samprata projekto operacijose

Projekto operacijose organizacinis vienetas turi konkrečią valiutą ir konkrečius savikainos kainoraščius.

Organizacinio vieneto valiuta yra pagrindinė valiuta, naudojama sąnaudoms sekti.

Prie kiekvieno organizacinio vieneto galima pridėti vieną arba daugiau sąnaudų kainoraščių. Projekto operacijos kainoraščiuose, kuriuos galima pridėti prie organizacinio vieneto, nurodo šiuos apribojimus:

- Kainoraščiai turi būti organizacinio vieneto valiuta.
- Kainoraščiai turi būti išlaidų kainoraščiai.

Be to, išteklių objekte yra organizacinio vieneto atributas. Kiekvienas išteklius gali būti priskirtas organizaciniam vienetui.

### <a name="roles-of-organizational-units"></a>Organizacinių vienetų vaidmenys

Organizacinis vienetas atlieka du vaidmenis projekto operacijose:

- **Sutarties vienetas** – organizacinis vienetas, atstovaujantis įmonių grupę arba padalinį, kuris yra atsakingas už laimėtą pardavimą ir darbo bei paslaugų pristatymą klientui. Sutarties vienetas atpažįstamas iš lauko **Sutarties vienetas** puslapių **Galimybė**, **Pasiūlymas**, **Projekto sutartis** ir **Projektai** antraštės skyriuje.
- **Išteklių vienetas** – organizacinis vienetas, kuriam ištekliai priklauso arba yra priskirti. Šis organizacijos vienetas gali pateikti savo išteklius kai kuriems vaidmenims, susijusiems su darbo ataskaitomis (SOW), ir projektams, priklausantiems sutarties vienetui.

![Sutartiniai vienetai ir išteklių skyriai.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Organizacinio vieneto DUK

Čia rasite atsakymus į kelis dažniausiai užduodamus klausimus apie organizacinius vienetus:

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kaip organizacijos vieneto objektas projekto operacijose yra susijęs su organizacijos objektu, kuris jau yra "Dynamics 365"?

Organizacijos objektas "Dynamics 365" nurodo visuotinio "Dynamics 365" egzemplioriaus pavadinimą. Šis pavadinimas paprastai yra pasaulinės įmonės pavadinimas.

Organizacinio vieneto objektas atstovauja grupei ar padaliniui globalioje įmonėje. Šioje grupėje ar padalinyje yra vaidmenų rinkinys ir šių vaidmenų sąnaudų kainoraštis, o šie vaidmenys ir kainoraštis skiriasi nuo kitų įmonės grupių ar padalinių vaidmenų ir kainoraščio.

Įdiegus "Project Operations", pagal organizaciją sukuriamas numatytasis organizacinis vienetas. Visi esami ištekliai priskiriami numatytajam organizaciniam vienetui. Jei nauji Active Directory vartotojai ar ištekliai importuojami į "Dynamics 365", vartotojo importavimo procesas priskiria juos numatytajam organizaciniam vienetui programoje "Project Operations".

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kuo organizacinio vieneto objektas skiriasi nuo verslo vieneto objekto?

Dynamics 365 verslo vieneto objektas yra saugos konstruktas. Vartotojo su verslo vienetu susiejimas nustato objektus ir objektų įrašus, prie kurių vartotojas turi prieigą. Ji taip pat nustato teises (kurti, perskaityti, rašyti, naikinti, pridėti, pridėti prie, priskirti arba naudoti), kurias vartotojas turi tiems objektų įrašams.

Organizacinio vieneto objektas atstovauja įmonių grupei arba skyriui, kuriam taikomi individualūs priskirtų darbuotojų sąnaudų tarifai. Išteklių su organizaciniu vienetu susiejimas nustato ištekliaus sąnaudas projekto įtraukimui.

Kai įdiegiate Dynamics 365, optimizuokite saugos leidimus verslo vienetų hierarchijai ir vartotojų priskyrimą verslo vienetams. Priskirkite visus vartotojus, kurie paprastai turi prieiti prie to paties įrašų rinkinio, tam pačiam verslo vienetui. Organizacinis vienetas neturi poveikio saugos leidimui arba prieigai.

**Pavyzdys, rodantis vieną galimą organizacinių vienetų ir verslo vienetų modeliavimo skirtumą**

Contoso turi klestinčią Microsoft technologijos praktiką. Darius ir Diana yra C\# kūrėjai, bet Diana yra Jungtinėse Valstijose, o Darius yra Indijoje. Daugumai projektų įsipareigojimų reikia išteklių tiek iš Contoso Indijos, tiek iš Contoso JAV, o Prakash ir Tricia reikalauja tokio paties lygio saugumo prieigos prie šios praktikos srities projektų. Tačiau Contoso Indija kūrėjų samdymo kaštai gerokai skiriasi nuo Contoso JAV kūrėjų kaštų.

Čia yra optimalus būdas sukurti šį scenarijų naudojant "Dynamics 365" ir "Project Operations".

1. Kurkite Microsoft technologijos praktiką kaip verslo vienetą ir susiekite Darių ir Dianą su juo. Tokiu būdu jūs padedate užtikrinti, kad abu darbuotojai turėtų vienodą saugumo prieigą prie bet kokių tos praktikos srities projektų. Jie abu galės patikrinti pažangą ir pranešti apie laiką, išlaidas, medžiagų naudojimą ir užduočių atnaujinimus.
2. Sukurkite du organizacinius vienetus, kurie padės užtikrinti, kad projekto išlaidos būtų teisingai atspindėtos.
3. Susieti Tricia su Contoso JAV ir Prakash su Contoso Indija.
4. Priskirkite tinkamus sąnaudų kainoraščius abiems organizaciniams vienetams. Tokiu būdu jūs padedate užtikrinti, kad prakash ir Tricia projekte užregistruotos išlaidos tiksliai atspindėtų išlaidų skirtumą tarp Contoso JAV ir Contoso Indijos.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Ar organizaciniai vienetai susiję su pardavimo teritorijomis Dynamics 365?

Nėra jokio susiejimo arba ryšių tarp pardavimo teritorijų ir organizacinių vienetų. Pardavimo teritorija paprastai yra geografinė sritis, kurioje vyksta pardavimas. Pardavimo kainoraštį galima susieti su kiekviena pardavimo teritorija.

Organizacinis vienetas yra įmonės vidinė grupė arba skyrius, kuris seka kitiems skyriams arba išoriniams klientais parduodamų vaidmenų rinkinio sąnaudas.

**Pavyzdys, rodantis vieną galimą organizacinių vienetų ir pardavimo teritorijų modeliavimo skirtumą**

Contoso turi du plėtros centrus: Contoso JAV ir Contoso Indija. Išteklių kaina labai skiriasi tarp šių dviejų plėtros centrų. Contoso parduoda savo informacinių technologijų (IT) paslaugas daugelyje tarptautinių rinkų, tokių kaip Lotynų Amerika, Šiaurės Amerika, Azijos ir Ramiojo vandenyno regionas, Vakarų Europa ir Artimieji Rytai. Tų pačių projektų vaidmenų įkainiai šiose rinkose gali labai skirtis. Contoso JAV ir Contoso Indija turėtų būti nustatyti kaip organizaciniai vienetai ir kiekvienas organizacinis vienetas turėtų turėti savo sąnaudų kainoraštį. Azija – Ramusis vandenynas, Lotynų Amerika, Šiaurės Amerika, Vakarų Europa ir Artimieji Rytai turėtų būti nustatyti kaip pardavimo teritorijos, o kiekviena pardavimo teritorija turėtų turėti nuosavą pardavimo kainoraštį.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Kodėl ribojamas kainoraščių susiejimas su organizaciniais vienetais?

Pardavimo kainodara paprastai yra unikali geografinėse srityse arba rinkose, kuriose parduodamos paslaugos. Įmonės vidaus skyriai paprastai neturi savo pardavimo kainų už to paties tipo aptarnavimą. Tačiau vidaus skyriai turi skirtingas parduotų prekių sąnaudas, atsižvelgiant į dirbančių žmonių įgūdžius, ir regiono, kuriame jie veikia, darbo sąlygas. Kadangi organizaciniai vienetai modeliuojami kaip įmonės vidiniai skyriai, jie gali turėti tik sąnaudų kainoraščius.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Kodėl negalime susieti pardavimo kainoraščių su organizaciniais vienetais?

"Project Operations" pardavimo kainoraščiai gali būti susieti su klientais ir pardavimo teritorijomis. Operacijų objektai, pvz., Galimybė, Pasiūlymas, Projekto sutartis ir Projektas, naudoja pardavimo kainoraščius, pridėtus prie kliento sąskaitos arba pardavimo teritorijos, kad nustatytų sąskaitų tarifus ir galimas projekto įtraukimo įplaukas.

Sąnaudų kainoraščiai susiejami su organizaciniais vienetais. Operacijų objektai, pvz., Galimybė, Pasiūlymas, Projekto sutartis ir Projektas, naudoja savikainos kainoraščius, pridėtus prie perkančiojo vieneto, kad nustatytų projekto įtraukimo išlaidas.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Ar organizaciniai vienetai yra hierarchiniai projekto operacijose?

Ne. Dabartiniame projekto operacijų leidime organizaciniai vienetai nėra hierarchiniai. Todėl negalite atlikti šių užduočių:

- Konfigūruokite numatytųjų savikainų įvedimo šabloną, kuris peržengia hierarchiją.
- Pranešti apie pajamas arba išlaidas, kurios susuktos skirtinguose organizacinių vienetų hierarchijos lygiuose.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Mes esame didelė tarptautinė įmonė, turinti sudėtingą, daugiapakopę išlaidų centrų, padalinių ir atsiskaitymo biurų hierarchiją. Kaip geriausiai panaudoti organizacinių vienetų sąvoką dabartinėje "Project Operations" versijoje?

Kai turite sudėtingą išlaidų centrų, padalinių, atsiskaitymo biurų ir t. t. hierarchiją, nustatykite tos hierarchijos lapų mazgus kaip atskirus organizacinius vienetus.

Toliau pateiktame pavyzdyje parodyta tipinė hierarchija.

**Contoso Indija**

- SAP Praktika

    - Techniniai Konsultantai
    - Funkciniai Konsultantai

- Microsoft Technologijos Praktika

    - Techniniai Konsultantai
    - Funkciniai Konsultantai

**Contoso, JAV**

- SAP Praktika

    - Techniniai Konsultantai
    - Funkciniai Konsultantai

- Microsoft Technologijos Praktika

    - Techniniai Konsultantai
    - Funkciniai Konsultantai

Jei jūsų hierarchija panaši į šį pavyzdį, turite nustatyti jį kaip plokščią sąrašą, kaip parodyta čia:

- Contoso Indija - SAP Praktika - Techniniai konsultantai
- Contoso Indija - SAP Praktika - Funkciniai konsultantai
- Contoso Indija - Microsoft technologijos praktikos funkciniai konsultantai
- Contoso Indija - Microsoft technologijos praktikos funkciniai konsultantai
- Contoso JAV - SAP Praktika - Techniniai konsultantai
- Contoso JAV – SAP Praktika – Funkciniai konsultantai
- Contoso JAV - Microsoft technologijos praktika - Techniniai konsultatai
- Contoso JAV - Microsoft technologijos praktika - Funkciniai konsultantai

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Esame nedidelė profesionalių paslaugų įmonė, veikianti kaip vienas skyrius. Kaip geriausiai panaudoti organizacinių vienetų sąvoką dabartinėje "Project Operations" versijoje?

Jei jūsų įmonė veikia kaip vienas vienetas, turintis vieną sąnaudų kainoraštį, nereikia nustatyti jokių organizacinių vienetų. Įdiegus "Project Operations" sukuriamas vienas numatytasis organizacinis vienetas, kurio pavadinimas yra toks pat kaip organizacijos. Pagal numatymą visi vartotojai priskiriami šiam organizaciniam vienetui. Kai sistema reikalauja, kad būtų pažymėtas organizacijos vienetas, šis organizacinis vienetas pažymimas pagal numatytuosius nustatymus.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Kai projektas kuriamas pagal pasiūlymą arba projekto sutarties eilutę, numatyta sutarties vienetas atsiranda iš pasiūlymo arba projekto sutarties. Kas yra numatytasis sutarties vienetas, jei projektas sukuriamas prieš pardavimo objektus, pvz., Pasiūlymą arba Projekto sutartį?

Kai projektas kuriamas savarankiškai, numatytasis projekto sutarties vienetas priklauso nuo jį sukūrusio vartotojo. Tas vartotojas taip pat yra numatytasis projektų vadovas. Jei projektas susietas su pardavimo objektu, pvz., pasiūlymu arba projekto sutartimi, projekto perkančioji grupė yra pagrįsta pardavimo objektu. Tokiu atveju projektų įvertinimai gali būti perskaičiuojami, nes sąnaudų kainoraštis naudojamas apskaičiuojant išlaidų sąmatos pokyčius, jei sutarties vienetas keičiasi.  Pardavimo kainoraštis naudojamas apskaičiuoti pardavimo įvertinimus, kurie bus pakeisti taip, kad jie būtų sinchronizuojami su pasiūlymo projekto kainoraščiu.

**Projekto laukai Perkančiasis vienetas** ir **valiuta** yra užrakinti redaguoti, nes jie turi būti sinchronizuojami su pardavimo objekto (pasiūlymo arba projekto sutarties), su kuriuo susietas projektas, vertėmis.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Kurti ir prižiūrėti organizacinius vienetus projekto operacijose

Norėdami sukurti organizacinį vienetą programoje "Project Operations", atlikite šiuos veiksmus.

1. Eikite į **Parametrų \> organizaciniai vienetai**.
2. Pasirinkite **Nauja**.
3. **Srities Bendra** lauke Pavadinimas **įveskite** organizacinio vieneto pavadinimą. Tada, jei reikia, nustatykite kitus laukus.
4. Pasirinkite **Įrašyti**, kad sukurtumėte įrašą, kad galėtumėte toliau jį redaguoti.
5. Dalyje **Išlaidų kainoraščiai** pasirinkite pliuso ženklą (**+**), kad įtrauktumėte kainoraštį. Čia galite įtraukti tik kainoraščius, kurių išlaidų **kontekstas yra**.
6. Lauke **Pavadinimas** pasirinkite **mygtuką Ieškoti** ir pasirinkite kainoraštį, kurį norite padaryti prieinamą organizaciniam vienetui. Jei reikia, toliau įtraukite kainoraščius.
7. Baigę įtraukti kainoraščius, apatiniame dešiniajame puslapio kampe pasirinkite **Įrašyti**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
