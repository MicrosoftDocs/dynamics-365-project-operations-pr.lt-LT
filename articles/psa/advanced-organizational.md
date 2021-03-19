---
title: Organizacinius vienetus
description: Šioje temoje pateikta informacija apie organizacijos vienetus Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 89ff652e186601ccdf75d99dc08a4f082e576cb0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291674"
---
# <a name="organizational-units"></a>Organizaciniai vienetai 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, organizacijos vienetas yra atskira grupė arba skyrius profesionalių paslaugų įmonėje, naudojanti apmokestinamus išteklius, turinčius sąnaudų tarifus.

Profesionalių paslaugų įmonėms, kurios naudoja techninius išteklius įvairioms praktinės veiklos sritims arba verslo linijoms, sąnaudos, skirtos atlikti vaidmenį vienoje srityje arba verslo linijoje, gali skirtis nuo sąnaudų, skirtų atlikti vaidmenį kitoje veiklos srityje arba verslo linijoje. Koncepciniai organizaciniai vienetai šiame scenarijuje padeda, suteikdami galimybę grupuoti apmokestinamų vaidmenų rinkinius įmonės, turinčios skirtingą šių vaidmenų sąnaudų struktūrą, skyriuje.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Pagrindiniai organizacinių vienetų atributai ir asociacijos

PSA  organizacinis venetas turi specialią valiutą ir specifinius sąnaudų kainoraščius.

Organizacinio vieneto valiuta yra pagrindinė valiuta, naudojama sąnaudoms sekti.

Prie kiekvieno organizacinio vieneto galima pridėti vieną arba daugiau sąnaudų kainoraščių. PSA suteikia sekančius kainoraščių ribojimus, kuriuos galima pridėti prie organizacinio vieneto:

- Kainoraščiai turi būti organizacinio vieneto valiuta
- Kainoraščiai turi būti iš sąnaudų kainoraščių

Papildomai, yra organizacijos vieneto atributas Išteklių objekte. Kiekvienas išteklius gali būti priskirtas organizaciniam vienetui.

## <a name="roles-of-organizational-units"></a>Organizacinių vienetų vaidmenys

Organizacinis vienetas atlieka du vaidmenis PSA:

- **Sutarties vienetas** – organizacinis vienetas, atstovaujantis įmonių grupę arba padalinį, kuris yra atsakingas už laimėtą pardavimą ir darbo bei paslaugų pristatymą klientui. Sutarties vienetas atpažįstamas iš lauko **Sutarties vienetas** puslapių **Galimybė**, **Pasiūlymas**, **Projekto sutartis** ir **Projektai** antraštės skyriuje.
- **Išteklių vienetas** – organizacinis vienetas, kuriam ištekliai priklauso arba yra priskirti. Šis organizacijos vienetas gali pateikti savo išteklius kai kuriems vaidmenims, susijusiems su darbo ataskaitomis (SOW), ir projektams, priklausantiems sutarties vienetui.

> ![Sutartiniai vienetai ir išteklių skyriai](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Organizacinio vieneto DUK

Čia rasite atsakymus į kelis dažniausiai užduodamus klausimus apie organizacinius vienetus:

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Kaip PSA Organizacinis Vieneto objektas susijęs su Organizaciniu objektu, kuris jau yra Dynamics 365?

Organizacinis objektas Microsoft Dynamics 365 atitinka visuotinio Dynamics 365 egzemplioriaus pavadinimą. Šis pavadinimas paprastai yra pasaulinės įmonės pavadinimas.

Organizacinio vieneto objektas atstovauja grupei ar padaliniui globalioje įmonėje. Šioje grupėje ar padalinyje yra vaidmenų rinkinys ir šių vaidmenų sąnaudų kainoraštis, o šie vaidmenys ir kainoraštis skiriasi nuo kitų įmonės grupių ar padalinių vaidmenų ir kainoraščio.

Įdiegus PSA, pagal šią organizaciją sukuriamas numatytasis organizacinis vienetas. Visi esami ištekliai priskiriami numatytajam organizaciniam vienetui. Jei bet kuris naujas Active Directory vartotojas arba ištekliai importuojami į Dynamics 365, vartotojo importavimo procesas priskiria juos numatytajam PSA organizaciniam vienetui.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Kaip organizacinis vieneto objektas skiriasi nuo verslo vieneto objekto?

Dynamics 365 verslo vieneto objektas yra saugos konstruktas. Vartotojo su verslo vienetu susiejimas nustato objektus ir objektų įrašus, prie kurių vartotojas turi prieigą. Ji taip pat nustato teises (kurti, perskaityti, rašyti, naikinti, pridėti, pridėti prie, priskirti arba naudoti), kurias vartotojas turi tiems objektų įrašams.

Organizacinio vieneto objektas atstovauja įmonių grupei arba skyriui, kuriam taikomi individualūs priskirtų darbuotojų sąnaudų tarifai. Išteklių su organizaciniu vienetu susiejimas nustato ištekliaus sąnaudas projekto įtraukimui.

Kai įdiegiate Dynamics 365, optimizuokite saugos leidimus verslo vienetų hierarchijai ir vartotojų priskyrimą verslo vienetams. Priskirkite visus vartotojus, kurie paprastai turi prieiti prie to paties įrašų rinkinio, tam pačiam verslo vienetui. Organizacinis vienetas neturi poveikio saugos leidimui arba prieigai.

#### <a name="example-of-organizational-units-and-business-units"></a>Organizaciinių vienetų ir verslo vienetų pavyzdys

Contoso turi klestinčią Microsoft technologijos praktiką. Darius ir Diana yra C\# kūrėjai, bet Diana yra Jungtinėse Valstijose, o Darius yra Indijoje. Daugeliui projekto užduočių reikia išteklių iš Contoso Indija ir Contoso JAV, o Dariui ir Dianai reikia turėti tokį patį saugos prieigos lygį į šios praktikos srities projektus. Tačiau Contoso Indija kūrėjų samdymo kaštai gerokai skiriasi nuo Contoso JAV kūrėjų kaštų.

Čia pateikiamas optimalus būdas kurti šį scenarijų naudojant Dynamics 365 ir PSA.

1. Kurkite Microsoft technologijos praktiką kaip verslo vienetą ir susiekite Darių ir Dianą su juo. Tokiu būdu padėsite užtikrinti, kad abu darbuotojai turėtų vienodą saugos prieigą prie bet kokio projekto toje praktikos srityje. Jie abu galės tikrinti eigą ir rengti ataskaitas apie laiką, išlaidas ir užduoties atnaujinimus. 
2. Sukurkite du organizacinius vienetus, kad padėtumėte užtikrinti, jog projekto sąnaudos yra teisingai atsispindimos. 
3. Susiekite Dianą su Contoso JAV ir Darių su Contoso Indija.
4. Priskirkite tinkamus sąnaudų kainoraščius abiems organizaciniams vienetams. Taip galėsite garantuoti, kad Dariui ir Dianai projekte įrašytos sąnaudos teisingai atspindi sąnaudų tarp Contoso JAV ir Contoso Indija skirtumą.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Ar organizaciniai vienetai susiję su pardavimo teritorijomis Dynamics 365?

Nėra jokio susiejimo arba ryšių tarp pardavimo teritorijų ir organizacinių vienetų. Pardavimo teritorija paprastai yra geografinė sritis, kurioje vyksta pardavimas. Pardavimo kainoraštį galima susieti su kiekviena pardavimo teritorija.

Organizacinis vienetas yra įmonės vidinė grupė arba skyrius, kuris seka kitiems skyriams arba išoriniams klientais parduodamų vaidmenų rinkinio sąnaudas.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Organizacijos vienetų ir verslo vienetų pavyzdys

Contoso turi du plėtros centrus: Contoso JAV ir Contoso Indija. Šių dviejų plėtros centrų išteklių sąnaudos labai skiriasi.

Contoso parduoda IT paslaugas daugelyje tarptautinių rinkų, pvz., Lotynų Amerikoje, Šiaurės Amerikoje, Azijoje ir Ramiojo vandenyno regione, Vakarų Europoje ir Artimuosiuose Rytuose. Tų pačių projektų vaidmenų įkainiai šiose rinkose gali labai skirtis.

Contoso JAV ir Contoso Indija turėtų būti nustatyti kaip organizaciniai vienetai ir kiekvienas organizacinis vienetas turėtų turėti savo sąnaudų kainoraštį. Azija – Ramusis vandenynas, Lotynų Amerika, Šiaurės Amerika, Vakarų Europa ir Artimieji Rytai turėtų būti nustatyti kaip pardavimo teritorijos, o kiekviena pardavimo teritorija turėtų turėti nuosavą pardavimo kainoraštį.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Kodėl ribojamas kainoraščių susiejimas su organizaciniais vienetais? 

Pardavimo kainodara paprastai yra unikali geografinėse srityse arba rinkose, kuriose parduodamos paslaugos. Įmonės vidaus skyriai paprastai neturi savo pardavimo kainų už to paties tipo aptarnavimą. Tačiau vidaus skyriai turi skirtingas parduotų prekių sąnaudas, atsižvelgiant į dirbančių žmonių įgūdžius, ir regiono, kuriame jie veikia, darbo sąlygas. Kadangi organizaciniai vienetai modeliuojami kaip įmonės vidiniai skyriai, jie gali turėti tik sąnaudų kainoraščius.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Kodėl mes negalime susieti pardavimo kainoraščių su organizacijos vienetais?

PSA pardavimo kainoraščiai gali būti susieti su klientais ir pardavimo teritorijomis. Operacijų objektai, pvz., Galimybė, Pasiūlymas, Projekto Sutartis ir Projektas naudoja prie kliento abonemento arba pardavimo teritorijos priskiriamus pardavimo kainoraščius, kad nustatyti projekto vykdymo sąskaitų įkainius bei potencialias pajamas.

Sąnaudų kainoraščiai susiejami su organizaciniais vienetais. Operacijų objektai, pvz., Galimybė, Pasiūlymas, Projekto Sutartis ir Projektas naudoja prie sutarties įmonės priskiriamus sąnaudų kainoraščius, kad nustatyti projekto vykdymo sąnaudas.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Ar organizaciniai vienetai skirstomi pagal hierarchijas PSA?

Ne. Dabartiniame PSA leidime organizaciniai vienetai neskirstomi pagal hierarchijas. Tai reiškia, kad jūs negalite:

- Konfigūruoti numatytą sąnaudų modelį, kuris eina aukštyn hierarchijoje. 
- Teikti ataskaitas apie pajamas ar sąnaudas skirtinguose organizacinių vienetų hierarchijos lygiuose.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Esame didelė daugianacionalinė įmonė, turinti sudėtingą, daugiapakopę sąnaudų centrų, skyrių ir atsiskaitymo biurų hierarchiją. Kaip galime geriausiai panaudoti organizacinio vieneto koncepciją šioje Project Service programos versijoje?

Kai turite sudėtingą sąnaudų centrų, skyrių, atsiskaitymo biurų ir kt. hierarchiją, nustatykite tos hierarchijos baigtinius mazgus kaip atskirus organizacinius vienetus.
Toliau pateiktame pavyzdyje pavaizduotą įprastą hierarchiją:

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
 
Jei jūsų hierarchija yra panaši, turite ją nustatyti kaip plokščią sąrašą, kaip parodyta čia:
- Contoso Indija - SAP Praktika - Techniniai konsultantai 
- Contoso Indija - SAP Praktika - Funkciniai konsultantai       
- Contoso Indija - Microsoft technologijos praktikos funkciniai konsultantai 
- Contoso Indija - Microsoft technologijos praktikos funkciniai konsultantai 
- Contoso JAV - SAP Praktika - Techniniai konsultantai  
- Contoso JAV – SAP Praktika – Funkciniai konsultantai  
- Contoso JAV - Microsoft technologijos praktika - Techniniai konsultatai 
- Contoso JAV - Microsoft technologijos praktika - Funkciniai konsultantai

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Esame nedidelė profesionalių paslaugų įmonė, veikianti kaip vienas skyrius. Kaip galime geriausiai naudoti organizacinio vieneto koncepciją dabartinėje PSA versijoje?

Jei jūsų įmonė veikia kaip vienas vienetas, turintis vieną sąnaudų kainoraštį, nereikia nustatyti jokių organizacinių vienetų. PSA įdiegimo metu Dynamics 365 sukuria vieną numatytąjį organizacijos vienetą, kuris turi tą patį pavadinimą kaip ir organizacija. Pagal numatymą visi vartotojai priskiriami šiam organizaciniam vienetui. Kai sistema reikalauja, kad būtų pažymėtas organizacijos vienetas, šis organizacinis vienetas pažymimas pagal numatytuosius nustatymus.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Kai projektas kuriamas pagal pasiūlymą arba projekto sutarties eilutę, numatyta sutarties vienetas atsiranda iš pasiūlymo arba projekto sutarties. Jei projektas kuriamas iki pardavimo objektų, pvz., pasiūlymo arba projekto sutarties, kas yra numatytasis sutarties vienetas?

Kai projektas kuriamas savarankiškai, numatytasis projekto sutarties vienetas priklauso nuo jį sukūrusio vartotojo. Tas vartotojas taip pat yra numatytasis projektų vadovas. Jei projektas susietas su pardavimo objektu, pvz., pasiūlymu arba projekto sutartimi, projekto sutarties vienetas įtakojamas pardavimo objekto. Tokiu atveju projektų įvertinimai gali būti perskaičiuojami, nes sąnaudų kainoraštis naudojamas apskaičiuojant išlaidų sąmatos pokyčius, jei sutarties vienetas keičiasi.  Pardavimo kainoraštis naudojamas pardavimo skaičiavimams, kurie bus pakeisti taip, kad jie būtų sinchronizuojami su projekto pasiūlymo kainoraščiu.

Projekto **Sutarties vienetas** ir **Valiuta** laukai užrakinami redagavimui, nes jie turi būti sinchronizuojami su pardavimo objekto (pasiūlymo arba projekto sutarties), su kuriuo susietas projektas, reikšmėmis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]