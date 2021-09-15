---
title: „Project Operations“ valdymas pagal subrangos sutartį
description: Šioje temoje pateikta tiesioginio subrangos valdymo proceso, paprastai atliekamo projektu pagrįstose oranizacijose, apžvalga.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 993edfd064279a970d7c42d5fcefd794e949a931
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323606"
---
# <a name="subcontract-management-in-project-operations"></a>„Project Operations“ valdymas pagal subrangos sutartį

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šioje temoje pateikta tiesioginio subrangos valdymo proceso, atliekamo projektu pagrįstose oranizacijose, apžvalga. Paslaugų subrangos procesas paprastai atliekamas vadovaujantis veiklos procesų seka, pavaizduota toliau pateiktoje diagramoje.

![Subrangos procesų seka](../media/SubcontractingProcessFlow.png)

Toliau esančiame sąraše pateikiamas nuoseklus subrangos proceso aprašymas.

1. Projekto vadovas sudaro subrangos sutartį su tiekėju. Pagal numatytuosius nustatymus prie tiekėjo įrašo pridėti kainoraščiai yra naudojami sudarant subrangos sutartį. Tiekėjo kliento ryšio tipas yra **Tiekėjas** arba **Pristatytojas**.
2. Projekto vadovas gali detalizuoti visus pirkimus kaip subrangos sutarties eilutės elementus. Gali būti laiko, išlaidų arba produktų subrangos sutarties eilutės. Subrangos sutarties eilutėje pasirinkta operacijos klasė nurodo, kam skirta eilutė.
3. Tiekėjo kliento vadovas ir projekto vadovas gali kartoti subrangos sutartį. Įkainius galima koreguoti pirkimo kainoraščiuose, pridedamuose prie subrangos sutarties.
4. Šiame etape arba vėliau, jei subrangos sutarties eilutė yra skirta laikui, tiekėjo kliento vadovas susieja tiekėjo kontaktus su kiekviena subrangos sutarties eilute. Šis susiejimas teikia informaciją projekto vadovui, dirbančiam su subrangos sutartimi. Susiejus tiekėjo kontaktą su subrangos sutarties eilute, sistema automatiškai sukuria rezervuojamąjį išteklių iš šio kontakto, jei rezervuojamojo ištekliaus dar nėra.
5. Kiekvienos subrangos sutarties eilutės atsiskaitymo metodas gali būti **Fiksuota kaina** arba **Laikas ir medžiagos**. Fiksuotos kainos subrangos sutarties eilutėms nustatomas etapais pagrįstas sąskaitų faktūrų grafikas.
6.  Parengus subrangos sutartį ir užbaigus derybas, subrangos sutartis patvirtinama. Patvirtintų subrangos sutarčių redaguoti negalima, tačiau įvykus pasikeitimams, jas galima atidaryti iš naujo ir redaguoti – tada būsena iš **Patvirtinta** vėl bus nustatyta į **Juodraštis** ir derybas bus galima pradėti iš naujo. 
7.  Kuriant projekto bendrąjį komandos narį, jį galima susieti su subrangos sutarties eilute. Tokiu būdu nurodomas poreikis bendrąjį komandos narį parinkti iš subrangovo turimo pajėgumo.
8.  Įvardytus komandos narius galima sukurti pačiame projekte arba rezervavus naudojant išteklių planavimo funkciją. Jei įvardytas projekto komandos narys yra sutarties darbuotojas, jį galima susieti su subrangos sutarties eilute. Tokiu būdu į subrangos sutarties eilutę bus įtrauktas galimas pajėgumas.
9.  Subrangovo ištekliai gali registruoti laiką, išlaidas ir projektams bei projekto užduotims sunaudotą medžiagą, tada teikti šią informaciją patvirtinti. Taip pat yra ir su darbuotojais. Įrašydamas laiką, sutarties darbuotojas gali pasirinkti konkrečią subrangos sutartį ir subrangos sutarties eilutę.
10. Patvirtinus, remiantis subrangos sutartyse nurodytu laiku faktiniai projekto išlaidų duomenys bus įrašomi pagal sutarties darbuotojo pirkimo kainą arba vaidmenį, kuris buvo taikomas dirbant su konkrečiu projektu.
11. Tiekėjo sąskaitos faktūros ir tiekėjo sąskaitos faktūros eilutės elementus galima įrašyti į sistemą pagal tiekėjo išteklių atliktą darbą arba tiekėjo pristatytus produktus. Tiekėjo sąskaitos faktūros eilutės turi būti specifinės projektui ir laiko, išlaidų, produkto / medžiagos, etapo arba mokesčio operacijos klasei. Pasirinktinai tiekėjo sąskaitos faktūros eilutės gali nurodyti subrangos sutarties eilutę.
12. Sistema automatiškai susies visas faktinių duomenų išlaidas, atitinkančias subrangos sutarties eilutę ir projektą, su tiekėjo sąskaita faktūra. Taip bus lengviau atlikti 3 dalių sugretinimo ir tikrinimo procesą.
13. Tada projekto vadovas gali peržiūrėti automatiškai sugretintus projekto faktinius duomenis, pašalinti arba įtraukti kito projekto faktinių duomenų išlaidas ir užbaigti tikrinimo procesą.
14. Atlikus visų eilučių tikrinimo procesą, tiekėjo sąskaita faktūra bus pažymėta kaip **Paruošta apmokėti**. Šiuo etapu tiekėjo sąskaitą faktūrą ir eilutes galima perkelti į apskaitos arba mokėtinų sumų sistemą ir apdoroti apmokėjimą tiekėjui. Anksčiau įrašyta projekto savikaina bus atšaukta, o projekte įrašyta tiekėjo sąskaitos faktūros eilutės faktinė savikaina.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Kiekiu pagrįstos subrangos sutarties eilutės ir darbu pagrįstos subrangos sutarties eilutės

Subrangos sutarties eilutė gali būti pagrįsta kiekiu arba darbu. 

Kai subrangos sutarties eilutė yra **pagrįsta kiekiu**, kiekį, perkamą laiko, išlaidų arba medžiagos subrangos sutarties eilutėje, galima naudoti kiekvienam projektui.

Kai subrangos sutarties eilutė yra **pagrįsta darbu**, subrangos sutarties eilutė susiejama su darbo struktūra, kurią nurodo projekto plano mazgas. Subrangos sutarties eilutės vertė yra visų komponentų, reikalingų tai darbo struktūrai pateikti, suma. Šie modeliuojami kaip išsamūs subrangos sutarties eilutės duomenys ir gali būti laiko, išlaidų ar medžiagų rinkinys. Darbu pagrįstos subrangos sutarties eilutės atveju subrangos sutarties eilutė taip pat yra skiriama tik vienam projektui.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

