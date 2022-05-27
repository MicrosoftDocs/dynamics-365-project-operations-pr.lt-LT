---
title: Būsenos Neviršyti ir tikrinimų valdymas
description: Šioje temoje pateikiama informacija apie limito, kurio negalima viršyti, patikras, atliekamas sistemoje „Project Operations“.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3444d311386ae925617c9c9be657fe012f8f867b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576142"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Būsenos Neviršyti ir tikrinimų valdymas 

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

## <a name="not-to-exceed-on-approvals"></a>Limito, kurio negalima viršyti, patikra patvirtinimuose

Pateikus įrašą apie sugaištą laiką, panaudotas išlaidas arba medžiagą, sukuriamas patvirtinimo įrašas. Jei patvirtinimas yra apmokestinamas ir susietas su laiko ir medžiagų sutarties eilute, sistema atlieka limito, kurio negalima viršyti, patikrą toliau nurodytais lygmenimis.

  - Patikra pagal projekto sutarties eilutėje nustatytą klientui taikomą limitą
  - Patikra pagal sutarties eilutėje nustatytą limitą
  - Patikra pagal nustatytą klientui taikomą limitą
  - Patikra pagal sutartyje nustatytą limitą

Kiekvienu lygmeniu atliekamos patikros užtikrina, kad šiame patvirtinime nurodyta pardavimo sumos vertė nepažeis limito, kurio negalima viršyti, tuo konkrečiu lygmeniu, įvertinus užregistruotą atsiskaitymo nebaigtų užduočių sumą ir sumą, už kurią išrašyta sąskaita faktūra iki datos tuo lygmeniu.

Jei patikra atliekama sėkmingai, patvirtinimui suteikiama tikrinimo būsena **Pavyko**.

Jei patikra atliekama nesėkmingai, patvirtinimui suteikiama tikrinimo būsena **Nepavyko**. Išsamioje limito, kurio negalima viršyti, patikros informacijoje vartotojui nurodoma, kokiu lygmeniu patikra atlikta nesėkmingai.

Kai pateiktas įrašas apie sugaištą laiką, panaudotas išlaidas arba medžiagą laikomas neapmokestinamu, tikrinimo būsena „Neviršyti“ nustatoma kaip **Netaikoma**, o tikrinimo informacijai taip pat taikoma būsena **Netaikoma**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Limito, kurio negalima viršyti, patikra pardavimo faktiniuose duomenyse, už kuriuos neišrašyta sąskaita faktūra

Kai įrašas apie sugaištą laiką, panaudotas išlaidas arba medžiagą patvirtinamas, sukuriami savikainos ir pardavimo faktinių duomenų, kuriems neišrašyta sąskaita faktūra, įrašai. Jei kuriami pardavimo faktiniai duomenys, už kuriuos neišrašyta sąskaita faktūra, yra apmokestinami ir susieti su laiko ir medžiagų sutarties eilute, programa atlieka limito, kurio negalima viršyti, patikrą toliau nurodytais lygmenimis.

  - Patikra pagal projekto sutarties eilutėje nustatytą klientui taikomą limitą
  - Patikra pagal sutarties eilutėje nustatytą limitą
  - Patikra pagal nustatytą klientui taikomą limitą
  - Patikra pagal sutartyje nustatytą limitą

Kiekvienu lygmeniu atliekamos patikros užtikrina, kad faktiniuose duomenyse nurodyta pardavimo sumos vertė nepažeis limito, kurio negalima viršyti, tuo konkrečiu lygmeniu, įvertinus užregistruotą atsiskaitymo nebaigtų užduočių sumą ir sumą, už kurią išrašyta sąskaita faktūra iki datos tuo lygmeniu.

Jei patikra atliekama sėkmingai, pardavimo faktiniams duomenims, už kuriuos neišrašyta sąskaita faktūra, suteikiama limito, kurio negalima viršyti, būsena **Užfiksuota**.

Jei patikra atliekama nesėkmingai, pardavimo faktiniams duomenims, už kuriuos neišrašyta sąskaita faktūra, suteikiama limito, kurio negalima viršyti, būsena **Nepavyko**. Išsamioje tikrinimo informacijoje vartotojui nurodoma, kokiu lygmeniu patikra atlikta nesėkmingai.

Kai pardavimo faktiniai duomenys, už kuriuos neišrašyta sąskaita faktūra, yra neapmokestinami arba nemokami, jei nė vienu iš keturių lygmenų nenustatytas limitas, kurio negalima viršyti, arba jei kuriami faktiniai duomenys Savikaina, Išankstinis apmokėjimas, Išteklių paskirstymo vienetas arba Tarp organizacijų vykdomas pardavimas, reikia nustatyti laukų **Neviršijimo būsena** ir **Išsami neviršijimo patikros informacija** vertę **Netaikoma**.

## <a name="reset-the-not-to-exceed-status"></a>Neviršijimo būsenos nustatymas iš naujo

Galite atlikti masinį neviršijimo būsenos nustatymą iš naujo. Projektų vadovai gali pakoreguoti tikrinimą „Neviršyti“ taip, kad prioritetas išrašant sąskaitas faktūras būtų teikiamas sąskaitoms faktūroms pagal konkretų atliktą darbą, sugaištą laiką, panaudotas išlaidas arba medžiagą išrašyti, o ne prioritetams, jau įtrauktiems į negalimą viršyti sumą.

Iš naujo nustačius neviršijimo būseną pardavimo faktiniuose duomenyse, už kuriuos neišrašyta sąskaita faktūra, paskirta suma sumažinama. Projekto vadovas gali pasirinkti kitą įrašo apie atliktą darbą, sugaištą laiką, panaudotas išlaidas arba medžiagas tipą, kuriam anksčiau nepavyko atlikti tikrinimo „Neviršyti“, ir įvertinti iš naujo. Sumažinus paskirtą sumą, šie faktiniai duomenys dabar atitinka tikrinimą, o tai projekto vadovui leidžia daryti didesnę įtaką atitinkamo laikotarpio operacijoms, kurioms išrašytina sąskaita faktūra, ir jas valdyti.

Norėdami iš naujo nustatyti neviršijimo būseną, pasirinkite vieną arba kelis pardavimo faktinių duomenų elementus rodinyje **Laiko ir medžiagų atsiskaitymo nebaigtos užduotys** arba **Faktiniai duomenys** ir pasirinkite **Iš naujo nustatyti neviršijimo būseną**.

Neviršijimo būsena nustatoma iš naujo kaip **Neįvertinta** visuose atitinkamuose pasirinktuose faktiniuose duomenyse. Faktiniai duomenys, kurių neviršijimo būsena nustatoma iš naujo, yra pardavimo faktiniai duomenys, už kuriuos neišrašyta sąskaita faktūra, kurie nėra sąskaitose faktūros juodraštyje ir kurie yra pažymėti kaip apmokestinami. Visų kitų pasirinktų faktinių duomenų nepaisoma.

## <a name="reevaluate-not-to-exceed-status"></a>Neviršijimo būsenos įvertinimas iš naujo

Galite atlikti masinį neviršijimo būsenos įvertinimą iš naujo. Neviršijimo būseną naudinga įvertinti iš naujo toliau nurodytais atvejais.

  - Su klientu iš naujo susitarta dėl limitų, kurių negalima viršyti, todėl faktinius duomenis reikia įvertinti iš naujo.
  - Projekto vadovas nori užtikrinti tikslų sąskaitos faktūros išrašymą už pardavimo neatliktas užduotis, už kurias neišrašyta sąskaita faktūra, teikdamas prioritetą vienam konkrečiam darbo elementui.

Norėdami iš naujo įvertinti neviršijimo būseną, pasirinkite vieną arba kelis pardavimo faktinių duomenų elementus rodinyje **Laiko ir medžiagų atsiskaitymo nebaigtos užduotys** arba **Faktiniai duomenys** ir pasirinkite **Neviršijimo būsenos įvertinimas iš naujo**.

Visi atitinkami pasirinkti faktiniai duomenys, kuriems taikomas limitas, kurio negalima viršyti, bus įvertinti remiantis limito, kurio negalima viršyti, sąranka. Faktiniai duomenys, susiję su neviršijimo būsenos įvertinimu iš naujo, yra pardavimo faktiniai duomenys, už kuriuos neišrašyta sąskaita faktūra, kurie nėra sąskaitose faktūros juodraštyje ir kurie yra pažymėti kaip apmokestinami. Visi kiti pasirinkti faktiniai duomenys.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
