---
title: Pardavimo kainoraščio projekto perrašymas
description: Šiame straipsnyje pateikiama informacija apie pasirinktinių pardavimo kainoraščių kūrimą.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8d0a769f415679b08f3228fcb14fbbbd37533ebc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911928"
---
# <a name="override-project-sales-price-lists"></a>Pardavimo kainoraščio projekto perrašymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

## <a name="customer-specific-project-price-lists"></a>Konkrečiam klientui taikomi projekto kainoraščiai

Konkrečiam klientui taikomų kainų sutartys gali būti nustatytos kaip projekto kainoraščiai kliento įraše programoje „Dynamics 365 Project Operations”.

Norėdami nustatyti konkrečiam klientui taikomą projekto kainoraštį, srityje **Pardavimas** pereikite prie kliento įrašo.

1. Atidarykite sąrašo puslapį **Klientai**.
2. Raskite ir dukart spustelėkite kliento įrašą, kad atidarytumėte informacijos puslapį **Klientas**.
3. Skirtuke **Projekto kainoraščiai** pasirinkite **+ Naujas projekto kainoraštis**.
4. Puslapyje **Naujas projekto kainoraštis** išplečiamajame sąraše pasirinkite kainoraštį. Įtraukiami tik tie kainoraščiai, kurių kontekstas nustatytas kaip **Pardavimas** ir kurių valiuta atitinka kliento valiutą.
5. Suteikite sąsajai pavadinimą ir pasirinkite **Įrašyti**. Konkrečiam klientui taikomas projekto kainoraštis sukurtas. Šis kainoraštis bus naudojamas siekiant pagal numatytuosius nustatymus nustatyti projekto kainas projekto pasiūlymuose arba sutartyse, sukurtose šiam klientui, kai pasiūlymo arba projekto sutarties sukūrimo data patenka į kainoraščio galiojimo datų diapazoną.

## <a name="custom-pricing-on-project-quotes"></a>Projekto pasiūlymų pasirinktinė kainodara

Projektų pasiūlymuose galite nustatyti projektų kainodarą, prasidedančią numatytuoju standartiniu kainoraščiu, kuris pagal numatytuosius nustatymus nustatomas naudojant kliento arba projekto parametrus.

Kai jums reikalinga pasirinktinė kainodara, skirta su projektu susijusiam darbui, esančiam konkrečiame pasiūlyme, galite gauti ją iš su projektu kainoraščiu susijusio objekto.

Atlikite toliau nurodytus veiksmus, kad nustatytumėte konkrečiam pasiūlymui taikomą projekto kainodarą.

1. Atidarykite projekto pasiūlymą ir pažymėkite skirtuką **Projekto kainoraščiai**.
2. Antriniame tinklelyje pasirinkite **Kurti pasirinktinę kainodarą**.

Visi projekto kainoraščiai, pridėti prie pasiūlymo, kopijuojami į naujus kainoraščius. Naujų kainoraščių pavadinimai perteikia pasiūlymo pavadinimą ir turi šių kainoraščių sukūrimo datos ir laiko žymą.

Galite naudoti visus šiuos kainoraščius ir atnaujinti darbo (vaidmens kaina) ir išlaidų (kategorijos kaina) kainas. Šios kainos bus taikomos tik šiam projekto pasiūlymui.

## <a name="price-lists-on-a-project-contract"></a>Projekto sutartyje esantys kainoraščiai

Projekto sutartyje numatytoji projekto kainodara visada yra pasirinktinis kainoraštis, kuriame nurodytas sutarties pavadinimas ir prie pavadinimo pridėta sukūrimo datos ir laiko žyma. Tai taikytina ir kai sutartis buvo sukurta laimėjus pasiūlymą, ir kai sutartis buvo sukurta nuo pradžių. Jei reikia, galite pašalinti šį susiejimą su pasirinktiniu kainoraščiu ir vietoj to susieti standartinį kainoraštį su projekto sutartimi.

Kai susiejate standartinį kainoraštį su projekto kainoraščiu pasiūlyme ar sutartyje, visi kainoraščio kainų pakeitimai turės įtakos visiems pasiūlymams ir sutartims, kurie naudoja šį kainoraštį.


[!INCLUDE[footer-include](../includes/footer-banner.md)]