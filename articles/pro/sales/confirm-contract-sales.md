---
title: Projekto sutarties patvirtinimas
description: Šioje temoje pateikta informacija, kaip patvirtinti sutartį programoje „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128293"
---
# <a name="confirm-a-project-contract"></a>Projekto sutarties patvirtinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projekto sutartis programoje „Dynamics 365 Project Operations“ gali būti aktyvi su tipu **Patvirtinta** arba uždaryta su tipu **Prarasta**. Patvirtinus projekto sutartį, būsena atnaujinama iš **Juodraštis** į **Aktyvi** ir būsenos tipas yra **Patvirtinta**. Aktyvios arba uždarytos sutarties negalima redaguoti arba atidaryti iš naujo. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Projekto sutarties patvirtinimo finansinis poveikis

Kai patvirtinama projekto sutartis, programa perskaičiuoja išlaidas atšaukdama senesnius išlaidų faktinius duomenis ir iš naujo sukurdama naujus išlaidų faktinius duomenis. Tada apdorojamos naujos faktinės išlaidos pagal susietos projekto sutarties eilutės atsiskaitymo būdą. Jei faktinių išlaidų nuoroda yra laiko ir medžiagų sutarties eilutė, programa automatiškai perkuria atitinkamas neapmokestintas pardavimo faktines sumas. Jei faktinių išlaidų nuoroda yra fiksuotos kainos sutarties eilutė, programa sustabdo pakartotinį faktinių išlaidų apdorojimą.

Siekiant neviršyti apribojimų, apmokestinamumo sąranka, kainodaros bei faktinių išlaidos yra įvertinamos ir tada atnaujinamos kaip patvirtinimo proceso dalis.

## <a name="close-a-project-contract-as-lost"></a>Projekto sutarties kaip prarastos uždarymas

Kai uždarote projekto sutartį kaip prarastą, sutarties būsena atnaujinama į **Uždaryta**, o būsenos tipas yra **Prarasta**. Projekto sutartis tampa tik skaitoma. Prieš įvykdant keitimus pateikiamas patvirtinimo dialogo langas, nes uždarytos projekto sutarties iš naujo atidaryti negalima.

Jei projekto sutarties, kuri uždaryta kaip prarasta, eilutėse nurodytas projektas, tas projektas taip pat pažymimas kaip uždarytas. Nuo tos dienos atšaukiami visi išteklių rezervavimai. Visos neapmokestintos faktinės pardavimo sumos, kurių dar nėra sąskaitoje faktūroje, bus anuliuotos.

> [!NOTE]
> Naudojant „Dynamics 365 Project Operations“, projekto sutarties kaip prarastos uždarymas nepaveiks susietos galimybės būsenai. Galimybė liks atidaryta ir ją reikės uždaryti neautomatiškai.
