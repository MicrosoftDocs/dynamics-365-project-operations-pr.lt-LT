---
title: Projekto sutarties patvirtinimas
description: Šioje temoje pateikta informacija, kaip patvirtinti sutartį programoje „Project Operations“.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003686"
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