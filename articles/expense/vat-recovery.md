---
title: PVM susigrąžinimas naudojant modulį Išlaidų valdymas
description: Šioje temoje aiškinama, kaip susigrąžinti PVM už atitinkamas pridėtinės vertės mokesčio (PVM) operacijas.
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: a840c808a76c96dd5f9dfb863c230801718c203c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001706"
---
# <a name="vat-recovery-in-expense-management"></a>PVM susigrąžinimas naudojant modulį Išlaidų valdymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Norint susigrąžinti PVM už atitinkamas pridėtinės vertės mokesčio (VAT) operacijas, įmonė arba organizacija turi identifikuoti, rinkti, patikrinti ir pateikti tikslią informaciją. Šis procesas apima kelias užduotis ir, atsižvelgiant į jūsų įmonės dydį, kelis darbuotojus arba vaidmenis.

Norint susigrąžinti PVM naudojant modulį **Išlaidų valdymas**, turi būti įgyvendintos toliau nurodytos būtinosios sąlygos.

- Turi būti sukurti mokesčių kodai, skirti šalims / regionams, kurie priskiriami išlaidų kategorijoms.
- Kiekvienam mokesčių kodui reikia sukurti PVM grupę.
- Kiekvienai PVM grupei reikia sukurti prekės PVM kodą.

Įgyvendinus būtinąsias sąlygas reikia atlikti toliau nurodytus veiksmus, kad būtų galima kreiptis dėl PVM susigrąžinimo.

1. Išlaidų ataskaitoje įveskite mokesčių informaciją apie kredito kortelių operacijas, kad identifikuotumėte tinkamas operacijas, už kurias norite susigrąžinti PVM.
2. Patikrinkite, ar įvesta visa mokesčių informacija, tada užregistruokite išlaidų ataskaitą.
3. Apdorokite išlaidas, atitinkančias užsienyje sumokėto PVM susigrąžinimo reikalavimus.
4. Nusiųskite PVM susigrąžinimo duomenis trečiosios šalies paslaugų teikėjui, kad būtų galima pateikti deklaraciją dėl užsienyje sumokėto PVM susigrąžinimo.
5. Apdorokite išlaidas, už kurias norite susigrąžinti savo šalyje sumokėtą PVM.

Toliau skyriuose pateikiami pavyzdžiai, kaip Contoso darbuotojai atlieka kiekvieną veiksmą.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Mokesčių informacijos apie kredito kortelių operacijas įvedimas, siekiant identifikuoti operacijas, už kurias norima susigrąžinti PVM

Greta, Contoso pardavimo atstovė, įsikūrusi Jungtinėse Valstijose, neseniai grįžo iš pardavimo komandiruotės į Jungtinę Karalystę. Per kelionę Greta savo asmenine kredito kortele mokėjo už maistą. Greta dabar turi sukurti išlaidų ataskaitą, kad suderintų išlaidas.

Greta vesdama informaciją išlaidų ataskaitoje puslapio **Redaguoti išlaidų ataskaitą** lauke **Šalis / regionas** pasirenka **Jungtinė Karalystė**. Tada filtruojamas PVM grupių sąrašas, kad jame būtų rodomos tik Jungtinei Karalystei taikomos grupės. Greta pasirenka PVM grupę **Jungtinė Karalystė 001** ir pasirenka prekės PVM grupę **Maitinimo išlaidos**. Paskui Greta įtraukia naują operaciją už apgyvendinimo paslaugas. Kadangi Jungtinėje Karalystėje apgyvendinimo paslaugoms taikoma tik viena PVM grupė ir viena prekės PVM grupė, ši informacija automatiškai užpildoma Gretos išlaidų ataskaitoje.

Pagal Contoso strategiją visos išlaidos turi turėti sutampantį kvitą. Todėl, kai Greta įrašo išlaidų ataskaitą, ji gauna pranešimą, kad reikia pridėti kiekvienos išlaidų ataskaitoje nurodytos operacijos kvitą. Greta įsitikina, kad pridėjo kiekvienos operacijos kvito skaitmeninį vaizdą prie savo išlaidų ataskaitos, ir pateikia savo ataskaitą patvirtinti. Tada ji nusiunčia popierinius kvitus operacijų skyriaus komandai. Ši komanda nusiųs PVM susigrąžinimo duomenis trečiosios šalies tiekėjui, kuris pateikia grąžintiną tarptautinį PVM Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Mokesčių informacijos tikrinimas ir išlaidų ataskaitos registravimas

Kad Akvilė, Contoso mokėtinų sumų koordinatorė, galėtų užregistruoti išlaidų ataskaitą, ji turi įvesti visą mokesčių informaciją, kurios joje nėra. Ji atidaro puslapį **Išsami išlaidų ataskaitos informacija** ir mato Gretos patvirtintą išlaidų ataskaitą. Tada Akvilė atidaro išlaidų ataskaitą, kad peržiūrėtų išsamią informaciją apie operacijas. Ji pastebi, kad Greta nenurodė vienos operacijos prekės PVM grupės. Akvilė negali užregistruoti išlaidų ataskaitos, nes trūksta šios informacijos. Todėl ji eina į modulio Išlaidų valdymas puslapį **Mokesčių konfigūracijos** ir randa atitinkamą prekės PVM grupę pagal šalį / regioną ir operacijos tipą. Akvilė dabar gali užregistruoti išlaidų ataskaitą didžiojoje knygoje.

Kai Akvilė užregistruoja išlaidų ataskaitą, sukuriamas susigrąžinamo PVM darbo elementas. Šis darbo elementas priskiriamas operacijų skyriaus komandos nariui. Akvilė gauna pranešimą, patvirtinantį, kad užregistruota sėkmingai. Šiame pranešime taip pat pateikiamas PVM operacijų, už kurias susigrąžinamas PVM, skaičius.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Išlaidų, atitinkančių užsienyje sumokėto PVM susigrąžinimo reikalavimus, apdorojimas

Arnas, Contoso operacijų skyriaus komandos narys, yra atsakingas už tai, kad į išlaidų ataskaitas bus įtraukta visa reikiama PVM informacija. Jis atidaro puslapį **Išlaidų mokesčių susigrąžinimas** ir pasirenka Gretos pateiktą išlaidų ataskaitą. Arnas patikrina, ar pridėti visi reikiami kvitai ir ar nurodyti tinkami PVM grupė ir prekės PVM kodai.

Kai Arnas gauna popierinius kvitus iš Gretos, jis palygina juos su skaitmeninėmis kvitų kopijomis ir pakeičia išlaidų ataskaitos būseną į **Paruošta susigrąžinti**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>PVM susigrąžinimo duomenų siuntimas trečiosios šalies paslaugų teikėjui

Kai Arnas yra pasiruošęs nusiųsti duomenis trečiosios šalies paslaugų teikėjui, kuris tvarkys PVM susigrąžinimą, jis atidaro puslapį **Išlaidų mokesčių susigrąžinimas**. Jis filtruoja puslapį, kad jame būtų rodomos tik tos išlaidų ataskaitos, kurių būsena pažymėta kaip **Paruošta susigrąžinti**. Tada Arnas pasirenka **Failas** &gt; **Eksportuoti į „Excel“**. PVM informacija iš išlaidų ataskaitų eksportuojama į „Microsoft Excel“ darbalapį. Arnas pateikia šį darbalapį trečiosios šalies paslaugų teikėjui ir prideda pranešimą, kuriame nurodo, kad popieriniai kvitai išsiųsti naudojant kurjerių tarnybą.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Išlaidas, už kurias norima susigrąžinti savo šalyje sumokėtą PVM, apdorojimas

Arnas turi patikrinti, ar už išlaidų ataskaitoje nurodytas operacijas galima susigrąžinti PVM ir ar prie ataskaitų pridėtos skaitmeninės kvitų kopijos. Kad galėtų apdoroti išlaidas, už kurias norima susigrąžinti savo šalyje sumokėtą PVM, Arnas atidaro puslapį **Išlaidų mokesčių susigrąžinimas** ir pasirenka išlaidų ataskaitą, kurią reikia patvirtinti. Jis patikrina, ar kvitai išrašyti įmonės, o ne darbuotojo vardu. (Norint susigrąžinti PVM, kvitai turi būti išrašyti įmonės vardu.) Arnas patikrina, ar nurodyti tinkami PVM grupė ir prekės PVM kodai.

Kai Arnas gauna popierinius kvitus, jis pakeičia išlaidų ataskaitos būseną į **Paruošta susigrąžinti**. Tada jis gali pateikti deklaraciją dėl susigrąžinimo atitinkamai mokesčių institucijai. Šiuo atveju atitinkama mokesčių institucija Jungtinėse Valstijose yra Mokesčių tarnyba (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]