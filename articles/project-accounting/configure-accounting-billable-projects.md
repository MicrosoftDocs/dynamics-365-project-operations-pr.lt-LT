---
title: Apmokėtinų projektų apskaitos konfigūravimas
description: Šioje temoje pateikta informacija apie apmokėtinų projektų apskaitos galimybes.
author: sigitac
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 629e3fc2f9069d104d459d0b4a6fa46c37f5c6f2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858663"
---
# <a name="configure-accounting-for-billable-projects"></a>Apmokėtinų projektų apskaitos konfigūravimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ palaiko įvairias apmokėtinų projektų, į kuriuos įtrauktos laiko ir medžiagų bei fiksuotos kainos operacijos, apskaitos parinktis.

- **Laiko ir medžiagų operacijos**: šioms operacijoms sąskaita faktūra išrašoma darbo eigoje pagal projekto valandų, išlaidų, elementų ir mokesčių suvartojimą. Šios operacijų išlaidos gali būti suderintos su kiekvienos operacijos pajamomis, o projekto sąskaita faktūra išrašoma darbo eigoje. Projekto pajamos taip pat gali būti sukauptos tuo metu, kai vyksta operacija. Sąskaitų faktūrų išrašymo metu pajamos atpažįstamos ir, jei taikoma, atšaukiamos sukauptos pajamos.
- **Fiksuotos kainos operacijos**: šioms operacijoms sąskaitos faktūros išrašomos pagal apmokėjimo grafiką, kuris sudaromas pagal projekto sutartį. Fiksuotos kainos operacijų pajamos gali būti atpažįstamos sąskaitų faktūrų išrašymo metu arba periodiškai apskaičiuojamos ir paskelbiamos pagal **Užbaigtos sutarties** arba **Užbaigimo procentinės dalies** būdus.

Projektas laikomas apmokėtinu, kai jis susietas su viena ar keliomis sutarties eilutėmis. Projekto sutarties eilutėje nurodoma, kuris atsiskaitymo būdas ir operacijų tipai galimi.

Pavyzdžiui, „Fabrikam Robotics“ laimėjo projekto sutartį su „Adatum“ korporacija įrangai optimizuoti. „Adatum“ mokės fiksuotą 10.000 JAV dolerių sumą, kad padengtų projekto išlaidas. Tai fiksuotos kainos atsiskaitymo būdas. Už projekto laiką ir mokesčius sąskaitos faktūros bus išrašomos už naudojimą. Tai yra laiko ir medžiagų apmokėjimo būdas. Visas darbas bus sekamas viename projekte pavadinimu „„Adatum“ įrangos optimizavimas“.

Projekto komandos narys pateikia aštuonių valandų darbą „Adatum“ įrangos optimizavimo projekte. Kai projekto vadovas patvirtina šį laiką, sistema naudoja laiko ir medžiagų apmokėjimo būdą, kad sukurtų faktinių duomenų operacijas, sąskaitą faktūrą ir klientą. Ši operacija nebus įtraukta į fiksuotos kainos pajamų įvertinimą.

Kitas projekto komandos narys pateikia 2000.00 JAV dolerių kelionės išlaidas, patirtas dėl „Adatum“ įrangos optimizavimo projekto. Kai projekto vadovas patvirtina šį pateikimą, sistema naudoja fiksuotos kainos apmokėjimo būdą, kad sukurtų faktinių duomenų operacijas ir šio projekto išlaidų klientą. Klientui nebus išrašyta sąskaita faktūra pagal šią operaciją. Vietoje to, jiems bus išrašyta sąskaita faktūra naudojant atskirai sukonfigūruotas apmokėjimo gaires. Ši išlaidų operacija, kartu su išlaidų įvertinimais, bus įtraukta į fiksuotos kainos pajamų įvertinimo apskaičiavimą.

Projekto operacijų apskaitos principai apibrėžiami projekto išlaidų ir pajamų profiliuose. Atliekant kiekvieną projekto operaciją, sistema nustato atitinkamą projekto išlaidų ir pajamų profilį naudojant projekto išlaidų ir pajamų profilio taisykles, kurios buvo sukonfigūruotos.

## <a name="define-project-cost-and-revenue-profiles"></a>Projekto išlaidų ir pajamų profilių nustatymas 

Projekto išlaidos ir pajamų profiliai apibrėžia projekto operacijų apskaitos taisykles. Šie profiliai sukonfigūruoti projektų valdyme ir apskaitoje. 

Atlikite toliau nurodytus veiksmus, kad sukurtumėte naują projekto išlaidų ir pajamų profilį. 

1. Eikite į **Projekto valdymas ir apskaita** > **Nustatymas** > **Publikavimas** > **Projekto išlaidų ir pajamų profiliai**. 
2. Pasirinkite **Naujas**, kad sukurtumėte naują projekto išlaidų ir pajamų profilį.
3. Lauke **Pavadinimas** įveskite profilio pavadinimą ir trumpą aprašą.
4. Lauke **Apmokėjimo būdas** pasirinkite **Laikas ir medžiagos** arba **Fiksuota kaina**.
5. Išplėskite **DK** „FastTab“. Šiame skirtuke esantys laukai apibrėžia apskaitos principus, naudojamus, kai projekto operacijos įtraukiamos į žurnalą naudojant „Project Operations“ integravimo žurnalą, o tada už jas išrašomos sąskaitos faktūros vykdant projekto sąskaitos faktūros pasiūlymą.
6. Toliau nurodytuose **DK** „FastTab“ laukuose pasirinkite tinkama informaciją:

    - **Skelbimo išlaidos – valanda**:

       - *Nėra DK*: laiko operacijų kaina nebus užregistruota į DK, kai paskelbiamas projekto operacijų integravimo žurnalas. Tačiau apskaitininkas gali vėliau publikuoti išlaidas naudodamas išlaidų publikavimo funkciją.
       - **Balansas**: laiko operacijų išlaidos bus nurašytos į DK sąskaitos tipą *NG – išlaidų reikšmė* ir bus sumokamos į *Algalapių paskirstymo sąskaitą* DK publikavimo nustatymuose. Apskaitininkas naudos publikavimo išlaidų funkciją, kad periodiškai perkeltų šias išlaidas iš balanso sąskaitos į pelno ir nuostolių sąskaitą.
       - **Pelnas ir nuostoliai**: publikuojant „Project Operations“ integravimo žurnalą, laiko operacijos išlaidos bus nurašytos į DK sąskaitos tipą *Išlaidos* ir sumokamos į *Algalapių paskirstymo sąskaitą*, apibrėžtą skirtuke **Išlaidos**, esančiame puslapyje **DK publikavimo nustatymai** (**Projekto valdymas ir apskaita**\>**Nustatymai**\>**Publikavimas**\>**DK publikavimo nustatymas**). Tai dažniausiai pasitaikanti laiko ir medžiagų operacijų sąranka.
        - *Niekada neregistruoti į DK*: laiko operacijų išlaidos niekada nebus registruojamos į DK.

    - **Publikavimo kaina – išlaidos**:

         - **Balansas**: publikuojant „Project Operations“ integravimo žurnalą, išlaidų operacijos kaina bus nurašyta nuo DK sąskaitos tipo *NG – išlaidų reikšmė*, kaip nurodyta skirtuke **Išlaidos**, esančiame puslapyje **DK publikavimo nustatymai** ir sumokama į žurnalo eilutės korespondentinę sąskaitą. Numatytosios korespondentinės išlaidų sąskaitos apibrėžiamos **Projektų valdymas ir apskaita** > **Nustatymai**\>**Publikavimas**\>**Numatytoji korespondentinė išlaidų sąskaitą**. Apskaitininkas naudos funkciją **Publikavimo išlaidos**, kad periodiškai perkeltų šias išlaidas iš balanso sąskaitos į pelno ir nuostolių sąskaitą.
        - **Pelnas ir nuostoliai**: publikuojant „Project Operations“ integravimo žurnalą, išlaidų operacijos kaina bus nurašyta nuo DK sąskaitos tipo *Išlaidos*, kaip nurodyta skirtuke **Išlaidos**, esančiame puslapyje **DK publikavimo nustatymai** ir sumokama į žurnalo eilutės korespondentinę sąskaitą. Numatytosios korespondentinės išlaidų sąskaitos apibrėžiamos **Projektų valdymas ir apskaita**\>**Nustatymai**\>**Publikavimas**\>**Numatytoji korespondentinė išlaidų sąskaita**.
      
    - **Registruoti sąnaudas – prekė**:

         - **Balansas**: registruojant „Project Operations“ integravimo žurnalą, operacijos už prekę savikaina bus nurašoma į didžiosios knygos sąskaitos tipą *Vykdomo projekto skaičiavimas – Savikainos reikšmė – prekė* taip, kaip apibrėžta skirtuke **Savikaina**, esančiame puslapyje **DK publikavimo sąranka**, ir sumokama taip, kaip nurodyta toliau.
    
              - Naudojimas pagal dokumento tipą: sąskaita **Savikaina – prekė**, esanti dalyje **DK publikavimo sąranka**.  
              - Pirkimas pagal dokumento tipą: **Viešųjų pirkimų integravimo sąskaita**, esanti dalyje **Projektų valdymo ir apskaitos parametrai**.
           Apskaitininkas naudos funkciją **Publikavimo išlaidos**, kad periodiškai perkeltų šias išlaidas iš balanso sąskaitos į pelno ir nuostolių sąskaitą.
        - **Pelnas ir nuostolis**: registruojant „Project Operations“ integravimo žurnalą, operacijos už prekę savikaina bus nurašoma į didžiosios knygos sąskaitos tipą *Savikaina* taip, kaip apibrėžta skirtuke **Savikaina**, esančiame puslapyje **DK publikavimo sąranka**, ir sumokama taip, kaip nurodyta toliau.
         
             - Naudojimas pagal dokumento tipą: sąskaita **Savikaina – prekė**, esanti dalyje **DK publikavimo sąranka**.  
             - Pirkimas pagal dokumento tipą: **Viešųjų pirkimų integravimo sąskaita**, esanti dalyje **Projektų valdymo ir apskaitos parametrai**.
       
    - **Kliento sąskaitų faktūrų išrašymas**:

        - **Balansas**: publikuojant projekto sąskaitos faktūros pasiūlymą, kliento operacija (atsiskaitymo gairė) bus sumokama į DK sąskaitos tipą *NG, už kurį išrašyta SF – klientas*, kaip nurodyta skirtuke **Pajamos**, esančiame puslapyje **DK publikavimo nustatymai** ir bus nurašyta iš Kliento balanso sąskaitos.
         - **Pelnas ir nuostoliai**: publikuojant projekto sąskaitos faktūros pasiūlymą, kliento operacija (atsiskaitymo gairė) bus sumokama į DK sąskaitos tipą *Pajamos, už kurias išrašyta SF – klientas*, kaip nurodyta skirtuke **Pajamos**, esančiame puslapyje **DK publikavimo nustatymai** ir bus nurašyta iš Kliento balanso sąskaitos. Klientų balanso sąskaitos apibrėžiamos **Gautinos sumos**\>**Nustatymai**\>**Klientų publikavimo profiliai**.

   Apibrėžę atsiskaitymo už laiką ir medžiagą būdų skelbimo profilius, galite pasirinkti kaupti pajamas pagal operacijos tipą (valandą, išlaidas, prekę ir mokestį). Jei parinktis **Sukaupti pajamas** nustatyta į **Taip**, „Project Operations“ integravimo žurnale esančios pardavimų operacijos, už kurias neišrašyta sąskaita, bus įrašytos į DK. Pardavimų reikšmė nurašoma iš **NG – pardavimų reikšmės sąskaita** ir sumokama į **Sukauptos pajamos – pardavimo reikšmė** sąskaitą, kuri buvo nustatyta puslapyje **DK publikavimo sąranka**, esančiame skirtuke **Pajamos**. 
  
  > [!NOTE]
  > Parinktį **Kaupti pajamas** galima naudoti tik tada, kai atitinkamas operacijų tipas **Išlaidos** publikuojamos pelno ir nuostolių sąskaitoje.
    
7. Išplėskite **Įvertinimas** „FastTab“. Šiame skirtuke esantys laukai apibrėžia fiksuotų kainų pajamų įvertinimų skaičiavimo parametrus. Šiame skirtuke esantys laukai taikomi tik projekto išlaidų ir pajamų profiliams su **Fiksuotos kainos** atsiskaitymo būdu.
8. Toliau nurodytuose **Įvertinimas** „FastTab“ laukuose pasirinkite tinkama informaciją:

    - **Projekto užbaigimo skaičiavimų principas**:

        - **Baigta sutartis**: išlaidų gretinimas ir pajamų pripažinimas vykdomas tik projekto pabaigoje. Balanse išlaidos rodomos kaip NG iki projekto pabaigos.
        - **Baigtas procentinis dydis**: sukauptos pajamos apskaičiuojamos ir užregistruojamos Į DK kiekvieną laikotarpį pagal projekto užbaigimo procentinę dalį. Procentui skaičiuoti galima taikyti kelis būdus. Šie būdai gali būti automatiniai, atsižvelgiant į konfigūraciją arba vadovą.
        - **Ne NG**: šis nustatymas naudojamas fiksuotos kainos projektams su trumpo laiko tarpu ir kur sąskaita faktūra ir išlaidos sudaromos tuo pačiu laikotarpiu. Šiuo atveju **Sąskaitų faktūrų klientams išrašymo** lauko reikšmė, esanti **DK** „FastTab“, automatiškai nustatoma į **Pelnas ir nuostoliai**, kad pajamos būtų atpažįstamos sąskaitos faktūros išrašymo metu. Pajamų įvertinimo procesas nebus naudojamas šio projekto išlaidų ir pajamų profiliui.

    - **Gretinimo principas**: šiame lauke nustatoma, kaip apskaičiuota pardavimo reikšmė (sukauptos pajamos) bus užregistruota DK.

        - Naudojant principą **Rardavimo reikšmė**, sistema apskaičiuos pardavimo reikšmę suderindama išlaidas ir pajamas ir užregistruodama ją kaip vieną sumą.
        - Naudojant principą **Gamyba ir pelnas**, sistema suskaidys pardavimo reikšmę į įvykdytas išlaidas ir apskaičiuotą pelną. Jie registruojami atskirai.

    - **Išlaidų šablonai**: leiskite, kad projektų operacijos būtų grupuojamos pagal operacijos tipą ir projekto kategoriją ir apibrėžkite šių grupių užbaigtų procentinės dalies skaičiavimo taisykles.
    - **Laikotarpio kodai**: nustatykite konkretaus projekto išlaidų ir pajamų profilio įvertinimo dažnumą.
    - **Įvertinimo kategorijos**: naudojamos pardavimo reikšmei (sukauptų pajamų) registruojant projektų operacijas. Pirmiausia sukonfigūruokite skirtųjų projektų kategoriją **mokesčio** operacijos tipui, o tada nustatykite vėliavėlę **Įvertinimas** šiai projekto kategorijai. Po to, atsižvelgdami į pasirinktą gretinimo principą, pasirinkite šią projekto kategoriją **pardavimo** reikšmėje arba **pelno** lauke, esančiame projekto išlaidų ir pajamų profilyje.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Projekto išlaidų ir pajamų profilių pavyzdinės konfigūracijos

Laikas ir medžiagos – be NG

![Išlaidų ir pajamų profilis: laikas ir medžiagos – be NG](media/time-material-no-wip.png)

Laikas ir medžiagos – NG (pajamos)

![Išlaidų ir pajamų profilis: laikas ir medžiagos – NG](media/time-material-with-wip.png)

Fiksuota kaina – be NG

![Išlaidų ir pajamų profilis: fiksuota kaina – be NG](media/fixed-price-no-wip.png)

Fiksuota kaina – baigta sutartis

![Išlaidų ir pajamų profilis: fiksuota kaina – baigta sutartis](media/fixed-price-completed-contract.png)

Fiksuota kaina – procentinė dalis

![Išlaidų ir pajamų profilis: fiksuota kaina – procentinė dalis](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Apskaitos įvykių pavyzdžiai, skirti pavyzdinių projektų išlaidų ir pajamų profiliams.

| Apskaitos įvykis                  | Laikas ir medžiagos – be NG                       | Laikas ir medžiagos – NG                                                                                           | Fiksuota kaina – be NG                                            | Fiksuota kaina – baigta sutartis                                                                            | Fiksuota kaina – procentinė dalis                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Laiko operacijų įtraukimas į žurnalą    | Debetas – kaina <br>Kreditas – algalapio paskirstymas          | Debetas – kaina <br>Kreditas – algalapio paskirstymas <br>Debetas – NG pardavimo reikšmė <br>Kreditas – sukauptų pajamų pardavimo reikšmė                | Debetas – kaina <br>Kreditas – algalapio paskirstymas                         | Debetas – kaina <br>Kreditas – algalapio paskirstymas                                                                    | Debetas – kaina <br>Kreditas – algalapio paskirstymas                       |
| Išlaid operacijų įtraukimas į žurnalą | Debetas – kaina <br>Kreditas – korespondentinė sąskaita už išlaidas | Debetas – kaina <br>Kreditas – korespondentinė sąskaita už išlaidas <br>Debetas – NG pardavimo reikšmė <br>Kreditas – sukauptų pajamų pardavimo reikšmė      | Debetas – kaina <br>Kreditas – korespondentinė sąskaita už išlaidas                 | Debetas – kaina<br> Kreditas – korespondentinė sąskaita už išlaidas                                                            | Debetas – kaina <br>Kreditas – korespondentinė sąskaita už išlaidas               |
| Sąskaitos faktūros klientas                | Debetas – kliento balansas <br>Kreditas – pajamos, už kurias išrašyta SF | Debetas – kliento balansas <br>Kreditas – pajamos, už kurias išrašyta SF <br>Kreditas – NG pardavimo reikšmė. Debetas – sukauptų pajamų pardavimo vertė | Debetas – kliento balansas <br>Kreditas – pajamų sąskaita faktūra – sąskaitoje | Debetas – kliento balansas <br>Kreditas – NG – sąskaitoje išrašyta SF                                                  | Debetas – kliento balansas <br>Kreditas – NG – sąskaitoje išrašyta SF    |
| Pajamų įvertinimo publikavimas             | Netaikoma                                   | Netaikoma                                                                                                    | Netaikoma                                                  | Debetas – NG išlaidų reikšmė <br>Kreditas – kaina                                                                         | Debetas – NG – pardavimo reikšmė <br>Kreditas – sukauptų pajamų pardavimo reikšmė |
| Naikinti                         | Netaikoma                                   | Netaikoma                                                                                                    | Netaikoma                                                  | Kreditas – NG išlaidų reikšmė <br>Debetas – kaina <br>Kreditas – sukauptų pajamų pardavimo reikšmė <br>Debetas – NG – sąskaitoje išrašyta SF | Debetas – NG – sąskaitoje išrašyta SF <br>Kreditas – NG pardavimo reikšmė     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Projekto išlaidų ir pajamų profilio taisyklių konfigūravimas

Projekto išlaidų ir pajamų profilio taisyklės nustato projekto išlaidų ir pajamų profilį, kurį reikia naudoti apdorojant bet kokias apmokėtinas projekto operacijas. Apibrėžkite taisykles nuėję į **Projektų valdymas ir apskaita**\>**Nustatymas**\>**Publikavimas**\>**Projekto išlaidų ir pajamų profilio taisyklės**.

Taisykles galima apibrėžti pagal projektų sutartis, projektų grupes arba pagal tam tikrą projektą. Pirmiausia sistema visada rinks didžiausią detalumo taisyklę.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
