---
title: Projekto sutarties patvirtinimas
description: Šiame straipsnyje pateikta informacija, kaip patvirtinti sutartį programoje „Project Operations“.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930006"
---
# <a name="confirm-a-project-contract"></a>Projekto sutarties patvirtinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ projekto sutartis gali būti aktyvi dėl tipo **Patvirtinta** arba uždaryta dėl tipo **Pralaimėta**. Patvirtinus projekto sutartį, būsena atnaujinama iš **Juodraštis** į **Aktyvi** ir būsenos tipas yra **Patvirtinta**. Aktyvios arba uždarytos sutarties negalima redaguoti arba atidaryti iš naujo. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Projekto sutarties patvirtinimo finansinis poveikis

Kai patvirtinama projekto sutartis, programa perskaičiuoja išlaidas atšaukdama senesnius išlaidų faktinius duomenis ir iš naujo sukurdama naujus išlaidų faktinius duomenis. Tada apdorojamos naujos faktinės išlaidos pagal susietos projekto sutarties eilutės atsiskaitymo būdą. Jei faktinių išlaidų nuoroda yra laiko ir medžiagų sutarties eilutė, programa automatiškai perkuria atitinkamas neapmokestintas pardavimo faktines sumas. Jei faktinių išlaidų nuoroda yra fiksuotos kainos sutarties eilutė, programa sustabdo pakartotinį faktinių išlaidų apdorojimą.

Siekiant neviršyti apribojimų, apmokestinamumo sąranka, kainodaros bei faktinių išlaidos yra įvertinamos ir tada atnaujinamos kaip patvirtinimo proceso dalis.

## <a name="close-a-project-contract-as-lost"></a>Projekto sutarties kaip prarastos uždarymas

Kai uždarote projekto sutartį kaip prarastą, sutarties būsena atnaujinama į **Uždaryta**, o būsenos tipas yra **Prarasta**. Projekto sutartis tampa tik skaitoma. Prieš įvykdant keitimus pateikiamas patvirtinimo dialogo langas, nes uždarytos projekto sutarties iš naujo atidaryti negalima.

Jei projekto sutarties, kuri uždaryta kaip prarasta, eilutėse nurodytas projektas, tas projektas taip pat pažymimas kaip uždarytas. Nuo tos dienos atšaukiami visi išteklių rezervavimai. Visos neapmokestintos faktinės pardavimo sumos, kurių dar nėra sąskaitoje faktūroje, bus anuliuotos.

> [!NOTE]
> Jei „Dynamics 365 Project Operations“ uždarysite projekto sutartį kaip pralaimėtą, tai nepadarys įtakos susietos galimybės būsenai. Galimybė liks atidaryta ir ją reikės uždaryti neautomatiškai.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]