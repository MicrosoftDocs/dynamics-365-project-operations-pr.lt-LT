---
title: Tiekėjo sąskaitų faktūrų su patvirtintais faktiniais duomenimis tikrinimas
description: Šiame straipsnyje paaiškinta, kaip "Microsoft Dynamics 365 Project Operations " projektų vadovai patikrina tiekėjo sąskaitas faktūras su faktiniais įrašais, kurie buvo patvirtinti kaip rangovai, atliko darbą ir įrašė laiką, taip pat išlaidas ir medžiagą, kurią naudojo projekto komandos nariai.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522946"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Tiekėjo sąskaitų faktūrų su patvirtintais faktiniais duomenimis tikrinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

"Microsoft Dynamics 365 Project Operations" projektų vadovai patikrinkime tiekėjo sąskaitų faktūrų eilutes šiais būdais:

- Naudokite tiekėjo **sąskaitos faktūros** eilučių lauką Tikrinimo būsena.
- Jei tiekėjo sąskaitos faktūros eilutės nurodo indūrinę eilutę, susiekite išlaidų faktinius sąrašus iš inertoriaus veiklos su tomis tiekėjo sąskaitų faktūrų eilutėmis. Saitas sukuriamas sugretinus faktinius tiekėjo sąskaitos faktūros eilučių išlaidų faktinius skaičius.

    > [!NOTE]
    > Nors galima sekti tiekėjo sąskaitos faktūros eilučių, kurios neturi nuorodos į susektą, tikrinimo būseną, išlaidų faktinių duomenų su tomis tiekėjo sąskaitos faktūros eilutėmis susieti negalima.

## <a name="verification-status"></a>Tikrinimo būsena

Patvirtinimo **būsenos laukas** tiekėjo sąskaitos faktūros eilutėje rodo, kad tikrinimo būsena. Palaikomos tolesnės būsenos:

1. Nepradėta
2. Vykdoma
3. Užbaigta

Tiekėjo sąskaitos faktūros eilučių, kurių tikrinimo būsena yra **Nepradėta**, redaguoti negalima.

Tiekėjo sąskaitos faktūros eilutę galima sukurti tik tuomet, kai jos **Vykdoma** nebegalima redaguoti. Jei tai tiekėjo sąskaitos faktūros eilutė, kuri nurodo perdėtą, tikrinimo būsena automatiškai nustatoma kaip Vykdoma iš karto, kai tik pirmą kartą faktinės išlaidos gretintos su tiekėjo sąskaitos faktūros **eilute**.

Tiekėjo sąskaitos faktūros eilutę galima sukurti tik tuomet, kai jos **Atlikta** nebegalima redaguoti. Kai visų tiekėjo sąskaitos faktūros eilučių tikrinimo būsena yra tokia, galima patvirtinti tiekėjo sąskaitą faktūrą.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Sugretinti realius kaštus su tiekėjo SF eilutėmis

Išlaidų faktinių duomenų gretinimas padeda patikrinti tiekėjo sąskaitos faktūros eilutę. Norėdami sugretinti išlaidų faktines sumas su tiekėjo sąskaitos faktūros eilute, atlikite toliau nurodytus veiksmus.

1. Atidarykite tiekėjo sąskaitos faktūros eilutę ir pažymėkite skirtuką **Nesutaptos išlaidos** faktiniai duomenys. Tinklelyje pateikiamas išlaidų faktinių duomenų sąrašas, kuris nurodo tą pačią asidėją kaip ir tiekėjo sąskaitos faktūros eilutę.
2. Pažymėkite vieną ar daugiau išlaidų faktinių duomenų, tada virš **tinklelio** esančioje įrankių juostoje pasirinkite Greti. Sistema patikrina, ar galima gretuoti pažymėtus faktinius išlaidų duomenis. Patvirtinę, išlaidų faktiniai rezultatai susiejami su tiekėjo sąskaitos faktūros eilute.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Tikrinimo kriterijai, naudojami išlaidų faktiniams sąrašams susieti su tiekėjo sąskaitos faktūros eilutėmis

Vykstant gretinimo procesui, ryšys tarp faktinių išlaidų ir tiekėjo sąskaitos faktūros eilutės gali būti nustatomas tik tada, jei laikomasi šių sąlygų:

- Kiekvieno **pažymėto faktinio** kainos nustatymo būsenos laukas turi būti tuščias. Kitaip tariant, išlaidų faktinių duomenų negalima pakeisti kitomis išlaidų faktinėmis sąrašomis, kurios turi būti atšaukimo, patvirtinimo atšaukimo ar pataisymų proceso metu.
- Toliau nurodytų laukų reikšmės gretintos tarp tiekėjo sąskaitos faktūros eilutės ir pažymėtos faktinės kainos. Jei tiekėjo sąskaitos faktūros eilutėje nėra lauko, jis neatitinka.

    - Projekto sutartis
    - Projekto sutarties eilutė
    - Operacijos klasė
    - Project
    - Užduotis
    - Išteklių kategorija
    - Operacijos kategorija
    - Produktas
    - Subrangos sutarties eilutė
    - Rezervuojami ištekliai

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Atsieti realius kaštus nuo tiekėjo SF eilutės

Išlaidų faktinių duomenų nesutapimas taip pat gali padėti patikrinti tiekėjo sąskaitą faktūrą, nes galima pašalinti anksčiau nustatytus saitus. Realūs kaštai gali būti atsieti nuo tiekėjo sąskaitos eilučių, kurių patvirtinimo būsena **Vykdoma**. Norėdami atiesti išlaidų faktines sumas su tiekėjo sąskaitos faktūros eilute, atlikite toliau nurodytus veiksmus.

1. Atidarykite tiekėjo sąskaitos faktūros eilutę ir pažymėkite skirtuką **Susietos išlaidos** faktiniai duomenys. Tinklelyje pateikiamas išlaidų faktinių duomenų sąrašas, kuris nurodo tą pačią asidėją kaip ir tiekėjo sąskaitos faktūros eilutę.
2. Pažymėkite vieną ar daugiau išlaidų faktinių duomenų, tada virš **tinklelio** esančioje įrankių juostoje pasirinkite atsieti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
