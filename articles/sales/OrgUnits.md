---
title: Organizacinius vienetus
description: Šiame straipsnyje aprašoma organizacinių vienetų sąvoka ir paaiškinta, kaip kurti ir prižiūrėti organizacinius vienetus programoje „Microsoft Dynamics 365 Project Operations“.
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

„Microsoft Dynamics 365 Project Operations“ programoje *organizacinis vienetas* yra atskira grupė arba padalinys profesionalių paslaugų įmonėje, naudojanti apmokestinamus išteklius, turinčius savikainos tarifus.

Profesionalių paslaugų įmonėms, kurios naudoja techninius išteklius įvairioms praktinės veiklos sritims arba verslo linijoms, sąnaudos, skirtos atlikti vaidmenį vienoje srityje arba verslo linijoje, gali skirtis nuo sąnaudų, skirtų atlikti vaidmenį kitoje veiklos srityje arba verslo linijoje. Koncepciniai organizaciniai vienetai šiame scenarijuje padeda, suteikdami galimybę grupuoti apmokestinamų vaidmenų rinkinius įmonės, turinčios skirtingą šių vaidmenų sąnaudų struktūrą, skyriuje.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Organizacijos vienetų sąvoka „Project Operations“

„Project Operations“ organizacinis venetas turi specialią valiutą ir specialius savikainų sąrašus.

Organizacinio vieneto valiuta yra pagrindinė valiuta, naudojama sąnaudoms sekti.

Prie kiekvieno organizacinio vieneto galima pridėti vieną arba daugiau sąnaudų kainoraščių. „Project Operations“ uždeda tolesnius kainoraščių ribojimus, kuriuos galima pridėti prie organizacinio vieneto:

- Kainoraščiai turi būti organizacinio vieneto valiuta.
- Kainoraščiai turi būti savikainos sąrašai.

Papildomai, išteklių objektas apima organizacijos vieneto atributą. Kiekvienas išteklius gali būti priskirtas organizaciniam vienetui.

### <a name="roles-of-organizational-units"></a>Organizacinių vienetų vaidmenys

Organizacinis vienetas atlieka du vaidmenis „Project Operations“:

- **Sutarties vienetas** – organizacinis vienetas, atstovaujantis įmonių grupę arba padalinį, kuris yra atsakingas už laimėtą pardavimą ir darbo bei paslaugų pristatymą klientui. Sutarties vienetas atpažįstamas iš lauko **Sutarties vienetas** puslapių **Galimybė**, **Pasiūlymas**, **Projekto sutartis** ir **Projektai** antraštės skyriuje.
- **Išteklių vienetas** – organizacinis vienetas, kuriam ištekliai priklauso arba yra priskirti. Šis organizacijos vienetas gali pateikti savo išteklius kai kuriems vaidmenims, susijusiems su darbo ataskaitomis (SOW), ir projektams, priklausantiems sutarties vienetui.

![Sutartiniai vienetai ir išteklių skyriai.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>Organizacinio vieneto DUK

Čia rasite atsakymus į kelis dažniausiai užduodamus klausimus apie organizacinius vienetus:

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kaip organizacinio vieneto objektas „Project Operations“ susijęs su Organizaciniu objektu, kuris jau yra „Dynamics 365“?

Organizacinis objektas „Dynamics 365“ atitinka visuotinio „Dynamics 365” egzemplioriaus pavadinimą. Šis pavadinimas paprastai yra pasaulinės įmonės pavadinimas.

Organizacinio vieneto objektas atstovauja grupei ar padaliniui globalioje įmonėje. Šioje grupėje ar padalinyje yra vaidmenų rinkinys ir šių vaidmenų sąnaudų kainoraštis, o šie vaidmenys ir kainoraštis skiriasi nuo kitų įmonės grupių ar padalinių vaidmenų ir kainoraščio.

Įdiegus „Project Operations”, pagal šią organizaciją sukuriamas numatytasis organizacinis vienetas. Visi esami ištekliai priskiriami numatytajam organizaciniam vienetui. Jei bet kuris naujas Active Directory vartotojas arba ištekliai importuojami į „Dynamics 365“, vartotojo importavimo procesas priskiria juos numatytajam „Project Operations” organizaciniam vienetui.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kaip organizacinis vieneto objektas skiriasi nuo verslo vieneto objekto?

Dynamics 365 verslo vieneto objektas yra saugos konstruktas. Vartotojo su verslo vienetu susiejimas nustato objektus ir objektų įrašus, prie kurių vartotojas turi prieigą. Ji taip pat nustato teises (kurti, perskaityti, rašyti, naikinti, pridėti, pridėti prie, priskirti arba naudoti), kurias vartotojas turi tiems objektų įrašams.

Organizacinio vieneto objektas atstovauja įmonių grupei arba skyriui, kuriam taikomi individualūs priskirtų darbuotojų sąnaudų tarifai. Išteklių su organizaciniu vienetu susiejimas nustato ištekliaus sąnaudas projekto įtraukimui.

Kai įdiegiate Dynamics 365, optimizuokite saugos leidimus verslo vienetų hierarchijai ir vartotojų priskyrimą verslo vienetams. Priskirkite visus vartotojus, kurie paprastai turi prieiti prie to paties įrašų rinkinio, tam pačiam verslo vienetui. Organizacinis vienetas neturi poveikio saugos leidimui arba prieigai.

**Pavyzdys, rodantis vieną galimą organizacijos vienetų ir verslo vienetų modeliavimo skirtumą**

Contoso turi klestinčią Microsoft technologijos praktiką. Darius ir Diana yra C\# kūrėjai, bet Diana yra Jungtinėse Valstijose, o Darius yra Indijoje. Daugeliui projekto užduočių reikia išteklių ir iš Contoso Indija, ir iš Contoso JAV, o Prakash ir Tricia reikia turėti tokį patį saugos prieigos lygį šios praktikos srities projektuose. Tačiau Contoso Indija kūrėjų samdymo kaštai gerokai skiriasi nuo Contoso JAV kūrėjų kaštų.

Čia pateikiamas optimalus būdas kurti šį scenarijų naudojant „Dynamics 365“ ir „Project Operations”.

1. Kurkite Microsoft technologijos praktiką kaip verslo vienetą ir susiekite Darių ir Dianą su juo. Tokiu būdu padėsite užtikrinti, kad abu darbuotojai turėtų vienodą saugos prieigą prie bet kokio projekto toje praktikos srityje. Jie abu galės tikrinti eigą ir rengti ataskaitas apie laiką, išlaidas, materialias sąnaudas ir užduoties atnaujinimus.
2. Sukurkite du organizacinius vienetus, kad padėtumėte užtikrinti, jog projekto sąnaudos yra atspindimos teisingai.
3. Susiekite Tricia su Contoso JAV ir Prakash su Contoso Indija.
4. Priskirkite tinkamus sąnaudų kainoraščius abiems organizaciniams vienetams. Taip galėsite garantuoti, kad Prakash and Tricia projekte įrašytos sąnaudos teisingai atspindi sąnaudų tarp Contoso JAV ir Contoso Indija skirtumą.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Ar organizaciniai vienetai susiję su pardavimo teritorijomis Dynamics 365?

Nėra jokio susiejimo arba ryšių tarp pardavimo teritorijų ir organizacinių vienetų. Pardavimo teritorija paprastai yra geografinė sritis, kurioje vyksta pardavimas. Pardavimo kainoraštį galima susieti su kiekviena pardavimo teritorija.

Organizacinis vienetas yra įmonės vidinė grupė arba skyrius, kuris seka kitiems skyriams arba išoriniams klientais parduodamų vaidmenų rinkinio sąnaudas.

**Pavyzdys, rodantis vieną galimą organizacijos vienetų ir pardavimo teritorijų modeliavimo skirtumą**

Contoso turi du plėtros centrus: Contoso JAV ir Contoso Indija. Šių dviejų plėtros centrų išteklių sąnaudos labai skiriasi. Contoso parduoda informacinių technologijų (IT) paslaugas daugelyje tarptautinių rinkų, pvz., Lotynų Amerikoje, Šiaurės Amerikoje, Azijoje ir Ramiojo vandenyno regione, Vakarų Europoje ir Artimuosiuose Rytuose. Tų pačių projektų vaidmenų įkainiai šiose rinkose gali labai skirtis. Contoso JAV ir Contoso Indija turėtų būti nustatyti kaip organizaciniai vienetai ir kiekvienas organizacinis vienetas turėtų turėti savo sąnaudų kainoraštį. Azija – Ramusis vandenynas, Lotynų Amerika, Šiaurės Amerika, Vakarų Europa ir Artimieji Rytai turėtų būti nustatyti kaip pardavimo teritorijos, o kiekviena pardavimo teritorija turėtų turėti nuosavą pardavimo kainoraštį.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Kodėl ribojamas kainoraščių susiejimas su organizaciniais vienetais?

Pardavimo kainodara paprastai yra unikali geografinėse srityse arba rinkose, kuriose parduodamos paslaugos. Įmonės vidaus skyriai paprastai neturi savo pardavimo kainų už to paties tipo aptarnavimą. Tačiau vidaus skyriai turi skirtingas parduotų prekių sąnaudas, atsižvelgiant į dirbančių žmonių įgūdžius, ir regiono, kuriame jie veikia, darbo sąlygas. Kadangi organizaciniai vienetai modeliuojami kaip įmonės vidiniai skyriai, jie gali turėti tik sąnaudų kainoraščius.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Kodėl mes negalime susieti pardavimo kainoraščių su organizacijos vienetais?

„Project Operations” pardavimo kainoraščiai gali būti susieti su klientais ir pardavimo teritorijomis. Operacijų objektai, pvz., Galimybė, Pasiūlymas, Projekto Sutartis ir Projektas naudoja prie kliento abonemento arba pardavimo teritorijos priskiriamus pardavimo kainoraščius, kad būtų gallima nustatyti projekto vykdymo sąskaitų įkainius bei potencialias pajamas.

Sąnaudų kainoraščiai susiejami su organizaciniais vienetais. Operacijų objektai, pvz., Galimybė, Pasiūlymas, Projekto Sutartis ir Projektas naudoja prie sutarties įmonės priskiriamus sąnaudų kainoraščius, kad būtų galima nustatyti projekto vykdymo sąnaudas.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Ar „Project operations”organizaciniai vienetai skirstomi pagal hierarchijas?

Ne. Dabartiniame „Project Operations“ leidime organizaciniai vienetai neskirstomi pagal hierarchijas. Todėl negalite atlikti šių užduočių:

- Konfigūruoti numatytojo sąnaudų modelio įvedimo, kuris eina aukštyn hierarchijoje.
- Teikti ataskaitas apie pajamas ar sąnaudas skirtinguose organizacinių vienetų hierarchijos lygiuose.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Esame didelė daugianacionalinė įmonė, turinti sudėtingą, daugiapakopę sąnaudų centrų, skyrių ir atsiskaitymo biurų hierarchiją. Kaip galime geriausiai naudoti organizacinių vienetų koncepciją dabartinėje „Project Operations“ versijoje?

Kai turite sudėtingą sąnaudų centrų, skyrių, atsiskaitymo biurų ir kt. hierarchiją, nustatykite tos hierarchijos baigtinius mazgus kaip atskirus organizacinius vienetus.

Toliau pateiktame pavyzdyje pavaizduota įprasta hierarchija.

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

Jei jūsų hierarchija yra panaši į šį pavyzdį, turite ją nustatyti kaip plokščią sąrašą, kaip parodyta čia:

- Contoso Indija - SAP Praktika - Techniniai konsultantai
- Contoso Indija - SAP Praktika - Funkciniai konsultantai
- Contoso Indija - Microsoft technologijos praktikos funkciniai konsultantai
- Contoso Indija - Microsoft technologijos praktikos funkciniai konsultantai
- Contoso JAV - SAP Praktika - Techniniai konsultantai
- Contoso JAV – SAP Praktika – Funkciniai konsultantai
- Contoso JAV - Microsoft technologijos praktika - Techniniai konsultatai
- Contoso JAV - Microsoft technologijos praktika - Funkciniai konsultantai

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Esame nedidelė profesionalių paslaugų įmonė, veikianti kaip vienas skyrius. Kaip galime geriausiai naudoti organizacinių vienetų koncepciją dabartinėje „Project Operations“ versijoje?

Jei jūsų įmonė veikia kaip vienas vienetas, turintis vieną sąnaudų kainoraštį, nereikia nustatyti jokių organizacinių vienetų. „Project Operations“ įdiegimas sukuria vieną numatytąjį organizacijos vienetą, kuris turi tą patį pavadinimą kaip ir organizacija. Pagal numatymą visi vartotojai priskiriami šiam organizaciniam vienetui. Kai sistema reikalauja, kad būtų pažymėtas organizacijos vienetas, šis organizacinis vienetas pažymimas pagal numatytuosius nustatymus.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Kai projektas kuriamas pagal pasiūlymą arba projekto sutarties eilutę, numatyta sutarties vienetas atsiranda iš pasiūlymo arba projekto sutarties. Jei projektas kuriamas iki pardavimo objektų, pvz., pasiūlymo arba projekto sutarties, kas yra numatytasis sutarties vienetas?

Kai projektas kuriamas savarankiškai, numatytasis projekto sutarties vienetas priklauso nuo jį sukūrusio vartotojo. Tas vartotojas taip pat yra numatytasis projektų vadovas. Jei projektas susietas su pardavimo objektu, pvz., pasiūlymu arba projekto sutartimi, projekto sutarties vienetas vietoje to paremtas pardavimo objektu. Tokiu atveju projektų įvertinimai gali būti perskaičiuojami, nes sąnaudų kainoraštis naudojamas apskaičiuojant išlaidų sąmatos pokyčius, jei sutarties vienetas keičiasi. Pardavimų kainoraštis naudojamas paskaičiuoti pardavimų sąmatas, kurios bus pakeistos, kad būtų sinkronizuotos su pasiūlytu projekto kainoraščiu.

Projekto **Sutarties vienetas** ir **Valiuta** laukai užrakinami redagavimui, nes jie turi būti sinchronizuojami su pardavimo objekto (pasiūlymo arba projekto sutarties), su kuriuo susietas projektas, reikšmėmis.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Organizacijos vienetų kūrimas ir valdymas „Project Operations“

Norėdami sukurti „Project Operations“ organizacinį vienetą, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Nustatymai \> Organizaciniai vienetai**
2. Pasirinkite **Nauja**.
3. Srityje **Bendra**, lauke **Pavadinimas** įveskite organizacinio vieneto pavadinimą. Tada nustatykite kitus laukus, kaip reikalaujama.
4. Pasirinkite **Įrašyti**, kad sukurtumėte įrašą, kurį vėliau galėsite redaguoti.
5. Norėdami įtraukti naują kainoraštį, srityje **Savikainų kainoraščiai** spustelėkite **+**. Čia galite įtraukti tik kainoraščius, susijusius su **Savikaina**.
6. Lauke **Pavadinimas** spustelėkite mygtuką **Ieškoti** ir pasirinkite kainoraštį, kuriuo norite leisti naudotis šiam organizaciniam vienetui. Įtraukite tiek kainoraščių, kiek reikalaujama.
7. Kai pridėsite kainoraščius, apatiniame dešiniajame puslapio kampe pasirinkite piktogramą **Įrašyti**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
