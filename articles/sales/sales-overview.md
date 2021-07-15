---
title: Pardavimo proceso apžvalga
description: Šioje temoje pateikiama informacija apie pagrindinius pardavimo procesus.
author: rumant
ms.date: 10/29/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: ed9731193e83eebd35e979adffcea529a289b9c5
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368351"
---
# <a name="sales-process-overview"></a>Pardavimo proceso apžvalga

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Organizacijoje, kurios veikla pagrįsta projektu, naudojami pardavimo procesai skiriasi nuo pardavimų procesų, naudojamų organizacijoje, kurios veikla pagrįsta produktais. Taip yra todėl, kad organizacijų, kurių veikla pagrįsta projektu, pardavimo ciklai yra ilgesni ir jiems reikia tinkintų įvertinimo technologijų, kad galėtų išanalizuoti ir kurti visų sandorių pasiūlymus. „Dynamics 365 Project Operations“ naudoja kai kurias iš šių funkcijų, naudojamų pardavimo procese:

- Pardavimo procesas sekamas naudojant įrašą „Galimas klientas“.
- Tinkami galimi klientai sekami kaip galimybės.
- Sisi susiję galimybės artefaktai yra prieinami. Šie artefaktai apima pardavimo komandą, suinteresuotąsias šalis, tikimybę, įvertinimą, pardavimo etapus ir veiklos procesus.
- Sukuriami keli galimybės pasiūlymai.
- Pasiūlymui suteikiamas statusas **Uždarytas kaip laimėtas** ir sukuriamas pardavimo užsakymas. Naudojant „Project Operations“ pardavimo užsakymas yra tinkintas ir vadinamas projekto sutartimi.

## <a name="estimate-a-sale"></a>Pardavimo įvertinimas
Pardavimo vertę galima apskaičiuoti pagal anksčiau pristatytus projektus ir projektų sudėtingumą. Jei projektas yra ankstesnių projektų tęsinys arba projektą vykdo labai patyręs tiekėjas, naudojantis gerai žinomus darbo šablonus, galite naudoti paprastesnį įvertinimo procesą. Sudėtingesnių projektų pirkimo procesas paprastai būna ilgesnis. Todėl pardavimo įvertinimo procesą sudaro daugiau etapų. Proceso pradžioje pardavimo komanda, naudodama klientų vadybininkų ir srities ekspertų įvestis, pradeda kurti aukšto lygio kiekvieno atskiro pasiūlyto darbų komponento įvertinimą. Šie darbų komponentai nurodomi pasiūlymo eilutėse. 

Galite sukurti aukšto lygio pasiūlymo įvertinimą. Vėliau šį aukšto lygio įvertinimą pakeisite išsamesniu įvertinimas, pagrįstu projekto planu, kurį sukursite naudodami standartizuotus projekto šablonus. Šie šablonai naudingi kuriant grafiką ir nustatant pinigines pasiūlymo bei jo komponentų vertes (pasiūlymo eilutes). 

Galite sukurti kelis projekto pasiūlymus ir sugrupuoti juos į vieną pasiūlymo įrašą. Galiausiai vienas iš pasiūlymų pažymimas **Uždarytas kaip laimėtas** ir sukuriama projekto sutartis arba darbų sąrašas („SOW“). Į projekto sutartį įtraukiamos visų komponentų (sutarties eilučių), kuriuos klientas sutiko pristatyti, sutartos vertės. SOW paprastai kuriamas kaip „Microsoft Word“ dokumentas. Visose sąskaitose faktūrose, siunčiamose klientui vykdant projekto sutartį, nurodoma projekto sutartis arba SOW.

Be to, galite sukurti alternatyvių pasiūlymų naudodami vieną pasiūlymo įrašą arba nustatyti sistemą, kad projekto sutartis būtų sukurta laimėjus pasiūlymą. Šiuo atveju prie projekto sutarties įrašo galite pridėti SOW „„Word““ dokumentą.

## <a name="configure-the-sales-process"></a>Pardavimo proceso konfigūravimas
Norėdami sukonfigūruoti pardavimo procesą, galite naudoti veiklos procesų sekas. Šie srautai užtikrina interaktyviąją vizualią sąsają, kad sandoriai būtų perkeliami į priekį per pardavimo proceso etapus.

Pavyzdžiui, jūsų įmonės pardavimo procesą gali sudaryti šeši toliau išvardyti etapai.

1. Patvirtinti tinkamumą
2. Numatoma
3. Vidinė peržiūra
4. Sutartis
5. Pristatyti
6. Uždaryti objektą 
 
Vykdydama tą patį sandorį organizacija gali naudoti įvairius objektus jam nurodyti. Pardavimo proceso pradžioje sandorį nurodo objektas Galimybė. Laikui bėgant gavę daugiau informacijos galite naudoti aukšto lygio įvertinimus ir sukurti vieną ar kelis pasiūlymus. Jei vieną iš šių pasiūlymų peržiūri vidaus ir kliento suinteresuotosios šalys, sandoris nurodomas kaip objektas Pasiūlymas. Klientui priėmus pasiūlymą, sandorį nurodo projekto sutartis arba SOW. Siekiant palaikyti šį veikimo principą veiklos procesų eigos yra sudarytos taip, kad kiekvienas proceso etapas būtų susietas su skirtinga duomenų bazės lentele.

Pardavimo proceso etapą **Patvirtinimas** galima susieti su objektu Galimybė. Etapus **Įvertinimas** ir **Vidinė peržiūra** galima susieti su objektu Pasiūlymas. Etapus **Sutartis**, **Pristatymas** ir **Uždarymas** galima susieti su objektu Projekto sutartis.

Vykdydami sandorio etapus būsite paraginti sukurti atitinkamą objekto įrašą, kad galėtumėte lengviau ir tiksliau atlikti procesą. Etapai gali būti sąlyginiai. Pavyzdžiui, jei jums pasiūlymo vidinės peržiūros jums tik tuo atveju, jei pasiūlymui naudojamas pasirinktinis kainoraštis, galite sukonfigūruoti šią sąlygą atitinkamame veiklos proceso etape. Tada etapas **Vidinė peržiūra** bus rodomas tik pasiūlymuose, kuriems naudojamas pasirinktinis kainoraštis. Visų kitų sandorių ir pasiūlymų atveju po etapo **Įvertinimas** vykdomas etapas **Sutartis**.

> [!NOTE]
> Programoje „Project Operations“ yra specialūs puslapiai, skirti galimybės, pasiūlymo, užsakymo ir sąskaitos faktūros objektų įrašams. Šiuos duomenis reikia kurti naudojant šių objektų projekto informacinius puslapius. Kitu atveju negalėsite atidaryti įrašo naudodami **Projekto informacijos** puslapį. Jei norite atidaryti įrašą iš **Projekto informacijos** puslapio, turite panaikinti įrašą ir sukurti jį iš naujo naudodami **Projekto informacijos** puslapį, kuriame kiekvieno iš šių objektų tipų verslo logika užtikrinama, kad įrašo laukas **Tipas** nustatytas teisingai, o visos privalomos sąvokos inicijuojamos tinkamai.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Pardavimo ciklo pasiūlymų ir projektų planų peržiūrų sekimas
Naudodami „Project Operations“ negalite sekti atliktų pasiūlymo peržiūrų. Turite pažymėti esamą pasiūlymą **Uždarytas kaip pralaimėtas**, o tada sukurti naują pasiūlymą. Galite nukopijuoti pasiūlymą arba klonuoti projektu pagrįstą pasiūlymą.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Pasiūlymų ir projektų sutarčių komentarų bei patvirtinimų sekimas
Naudodami įrašų sieną ir įrašus galite valdyti pasiūlymų ir projektų sutarčių peržiūrą bei patvirtinimą. Siekdama priskirti, peradresuoti, perskirti ir valdyti peržiūros ir patvirtinimo darbų elementų pranešimus organizacija gali kurti pasirinktines darbo eigas ir priedus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]