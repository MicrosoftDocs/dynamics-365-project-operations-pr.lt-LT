---
title: Išteklių priskyrimų kūrimas
description: Šiame straipsnyje pateikta informacija apie bendrųjų ir įvardytųjų išteklių priskyrimų kūrimą.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812004"
---
# <a name="create-resource-assignments"></a>Išteklių priskyrimų kūrimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


Išteklių priskyrimas yra tiesioginė projekto komandos nario jungtis į lapų mazgo užduotį. Šiame straipsnyje pateikiama informacija apie skirtingus išteklių priskyrimo būdus.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Bendrojo komandos nario kūrimas priskiriant užduotį


Kurdami bendrąjį komandos narį per užduoties priskyrimą, jūs sukuriate vietos rezervavimo ženklą arba bendrąjį išteklių. Šis bendrasis išteklius aprašo įvardyto ištekliaus, su kuriuo galiausiai norite dirbti su užduotimis, charakteristikas. Tada sugeneruojate reikalavimą arba pateikiate užklausą naudodami reikalavimą, kuris naudojamas ieškant ir rezervuojant įvardytą išteklių.

1. Užduoties grafiko tinklelyje pasirinkite langelyje **Ištekliai** esančią išteklių piktogramą.
2. Įveskite pavadinimą, kuris bus naudojamas kaip vietos rezervavimo ženklo ištekliaus pavadinimas. Pavyzdžiui, „Programos vadovas“.
3. Pasirinkite **„Kurti“**, o tada lauke **„Spartusis projekto komandos nario kūrimas“** nustatykite bendrųjų išteklių vaidmenį.
4. Užduočiai pasirinkdami išteklių parinktyje **Išteklių išrinkiklis**, priskirkite užduotis šiems vietos rezervavimo ženklo ištekliams. Ištekliai išvardyti skirtuke **Komandos nariai**.
5. Baigę priskirti bendrąjį išteklių, skirtuke Komanda **pasirinkite bendrąjį išteklių,** tada pasirinkite **Generuoti reikalavimą**, kad sukurtumėte bendrojo ištekliaus išteklių poreikį.
6. Bendrajam ištekliui pasirinkite **Rezervuoti**, o tada naudokite grafiko lentą, kad surastumėte ir užrezervuotumėte tikrus išteklius. Taip pat galite išteklių vadovui pateikti reikalavimą, kad jis būtų įvykdytas.
7. Kai bendrasis išteklius visiškai įvykdomas su įvardytuoju ištekliumi, bendrasis išteklius pašalinamas iš komandos. (Įvykdžius dalinį išteklių reikalavimą, ištekliai nebus priskirti.) Bendrojo ištekliaus užduočių priskyrimai priskiriami įvardytam ištekliui, kuris įvykdė bendrojo ištekliaus išteklių poreikį.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Įvardytų išteklių priskyrimas iš visų rezervuojamų išteklių sąrašo

Norėdami ieškoti visų aktyvių rezervuojamų išteklių ir juos priskirti prie bet kurios lapo mazgo užduoties, galite naudoti ieškos laukelį, esantį parinktyje **Išteklių parinkiklis**. Tokiu būdu priskirti ištekliai įtraukiami į komandą neatliekant jokių rezervacijų. Taip pat galima įtraukti komandos narį ir vietoje paskirstymo metodo pažymėti **Nėra**. Ištekliai rodomi skirtukuose **Komanda**, **Išteklių priskyrimas** ir **Suderinimas** kaip ištekliai, turintys tik priskyrimus ir rezervavimo deficitą. Jei norite pasinaudoti jų prieinamumu, juos rezervuokite.

1. Užduočių tinklelyje, lentoje arba laiko planavimo juostoje pereikite prie langelio **Priskirta (kam)**.
2. Ieškos lauke pradėkite vesti pavadinimą. Pavadinimo ieškos rezultatai pateikiami **„Išteklių išrinkiklis“**, parinktyje **„Kiti ištekliai“**.
3. Pažymėkite išteklių, kurį norite priskirti užduočiai arba pažymėkite ištekliaus pavadinimą parinktyje **Kiti komandos ištekliai**.

## <a name="editing-resource-assignment-contours"></a>Išteklių priskyrimo kontūrų redagavimas

Pagal numatytuosius nustatymus, kai ištekliai priskiriami užduočiai pagal grafiką, jų pastangos tiesiškai paskirstomos kiekvienam ištekliui, atsižvelgiant į to ištekliaus darbo valandas ir projekto grafiko režimą. Projekto vadovas gali naudoti išteklių priskyrimo tinklelį, kad patikslintų kiekvieno ištekliaus, priskirto vienai ar kelioms užduotims skirtingose laiko skalėse, pastangų įvertinimus. Ši funkcija padeda projektų vadovams parengti tikslesnius savikainos ir pardavimo įvertinimus, kuriuos lemia išteklių priskyrimo kontūrai, generuojami priskyrus išteklius užduočiai. Be to, projektų vadovai gali lengviau atspindėti išteklių poreikį, kurio reikia norint sukurti išteklių poreikio poreikį.

### <a name="navigation"></a>Naršymas

Norėdami pasiekti kontūro redagavimo tinklelį, projekto vadovas pirmiausia projekto pagrindiniame puslapyje pasirenka skirtuką Užduotys, tada pasirenka **skirtuką** Priskyrimai **.** 

![Skirtukas Priskyrimai projekto pagrindinio puslapio skirtuke Užduotys.](media/AssignmentGrid.png)

Tinklelis palaiko du grupavimo būdus: **grupuoti pagal išteklius** ir **grupuoti pagal užduotį**. Kitaip nei tinklelio rodinyje, stulpelių negalima konfigūruoti. Vieninteliai matomi stulpeliai yra **Priskirta**, Užduoties pavadinimas **, Priskyrimo pradžia**, **·** **Priskyrimo užbaigimas** ir **Priskyrimo pastangos.**

Kai tinklelis iš pradžių pateikiamas, jis prasideda nuo anksčiausio užduoties kontūro. Jei jūsų tvarkaraštyje nėra jokių užduočių, kurioms reikia pastangų, tinklelis bus tuščias ir nieko nepateiks.

![Tuščias priskyrimo tinklelis.](media/emptyassignmentgrid.png)

Jei norite peržiūrėti savo kontūrus ir skirtingas laiko skales, taip pat yra tik skaitomas išteklių priskyrimo tinklelis ir išteklių derinimo tinklelis.

### <a name="resource-calendars"></a>Išteklių kalendoriai

Galimybė redaguoti konkrečios dienos kontūrą priklauso nuo išteklių darbo dienų, kaip atsispindi jų kalendoriuje. Jei tam tikro ištekliaus langelis išjungtas, tas išteklius per tą laikotarpį neturi darbo dienų.

Ištekliaus kontūrai gali apimti daugiau nei dabartinės priskirtos užduoties pradžios ir pabaigos datos. Jei kontūras atnaujinamas taip, kad jis yra po paskutinės užduoties pabaigos datos arba anksčiausios užduoties pradžios datos, užduoties pabaigos data arba pradžios data bus atitinkamai pakeista. Tačiau jei kontūras atnaujinamas taip, kad jis yra ankstesnis nei užduoties, susietos su ankstesne užduotimi, pradžios data, naujinti nepavyks, nes priskyrimas suaktyvins užduoties pradžią prieš užbaigiant ankstesnę užduotį ir šis veikimas šiuo metu nepalaikomas.

### <a name="co-authoring"></a>Redagavimas vienu metu

Išteklių priskyrimo tinklelio pakeitimai automatiškai atsispindi visuose susijusiuose rodiniuose, įskaitant diagramą, laiko planavimo juostą, lentą ir tinklelio rodinius. Jei keli vartotojai peržiūri projektą tuo pačiu metu, visi vieno vartotojo atlikti pakeitimai atsispindės tinklelyje. Ir atvirkščiai, visi pakeitimai, atlikti išteklių priskyrimo tinklelyje, bus rodomi visiems kitiems vartotojams, kurie peržiūri projektą to paties seanso metu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
