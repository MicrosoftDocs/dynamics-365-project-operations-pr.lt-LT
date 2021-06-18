---
title: Įmonės vidaus SF išrašymo konfigūravimas
description: Šioje temoje pateikta informacija ir pavyzdžiai apie įmonės vidaus SF išrašymo už projektus konfigūravimą.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9894a405403d4faeb2f02387b03c77a40a6cea3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001166"
---
# <a name="configure-intercompany-invoicing"></a>Įmonės vidaus SF išrašymo konfigūravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Norėdami nustatyti įmonės vidaus SF išrašymą už projektus programoje „Dynamics 365 Project Operations“, atlikite toliau nurodytus veiksmus.. Vidinės įmonės operacijos yra laiko ir išlaidų operacijos iš projekto sutarties, priklausančios vienai įmonei arba organizaciniam vienetui, kai projekto sutarties ištekliai priklauso kitai įmonei arba organizaciniam vienetui.

## <a name="example-configure-intercompany-invoicing"></a>Pavyzdys: įmonės vidaus SF išrašymo konfigūravimas

Toliau pateiktame pavyzdyje „Contoso Robotics USA“ (USPM) yra besiskolinantysis juridinis subjektas, o „Contoso Robotics UK“ (GBPM) – skolinantysis juridinis subjektas. 

1. **Įmonės vidaus apskaitos skirtinguose juridiniuose subjektuose konfigūravimas**. Kiekviena skolinimosi ir skolinimo juridinių objektų pora turi būti konfigūruota didžiosios knygos [įmonės vidaus apskaitos](/dynamics365/finance/general-ledger/intercompany-accounting-setup) puslapyje.
    
    1. Programoje „Dynamics 365 Finance“ eikite į **Didžioji knyga** > **Registravimo nustatymas** > **Vidinių įmonių apskaita**. Sukurkite įrašą nurodydami toliau pateiktą informaciją:

        - **Pradinė įmonė** = **GBPM**
        - **Paskirties įmonė** = **USPM**

2. **Prekybinių ryšių tarp juridinių objektų konfigūravimas**. Kliento įrašas, atspindintis skolinimosi juridinį objektą, turi būti sukurtas skolinimo juridiniame objekte. Tiekėjo įrašas, atspindintis skolinimo juridinį objektą, turi būti sukurtas skolinimosi juridiniame objekte.

     1. Finansų srityje pasirinkite juridinį objektą **GBPM**.
     2. Eikite į **Gautinos sumos** > **Klientas** > **Visi klientai**. Sukurkite naują juridinio objekto įrašą **USPM**.
     3. Išplėskite **pavadinimą**, filtruokite įrašus pagal **tipą** ir pasirinkite **juridinius objektus**. 
     4. Raskite ir pasirinkite kliento įrašą **„Contoso Robotics USA“ (USPM)**.
     5. Pasirinkite **Naudoti atitikmenį**. 
     6. Pasirinkite klientų grupę **50 – vidinės įmonės klientai** ir įrašykite įrašą.
     7. Pasirinkite juridinį objektą **USPM**.
     8. Eikite į **Mokėtinos sumos** > **Tiekėjai** > **Visi tiekėjai**. Sukurkite naują juridinio objekto įrašą **GBPM**.
     9. Išplėskite **pavadinimą**, filtruokite įrašus pagal **tipą** ir pasirinkite **juridinius objektus**. 
     10. Raskite ir pasirinkite kliento įrašą **„Contoso Robotics UK“ (GBPM)**.
     11. Pasirinkite **Naudoti atitikmenį**, tiekėjų grupę, o tada įrašykite įrašą.
     12. Tiekėjo įraše pasirinkite **Bendra** > **Nustatyti** > **Įmonės vidaus**.
     13. Skirtuke **Prekybiniai ryšiai** parinktį **Aktyvus** nustatykite į **Taip**.
     14. Lauką **Kliento įmonė** nustatykite kaip **GBPM**, o lauke **Mano kliento įrašas** pasirinkite kliento įrašą, kurį sukūrėte anksčiau, atlikdami procedūrą.

3. **Įmonės vidaus parametrų konfigūravimas projektų valdymo ir apskaitos parametruose**. 

    1. Pasirinkite juridinį objektą **USPM** ir eikite į **Projektų valdymas ir apskaita** > **Nustatyti** > **Projektų valdymo ir apskaitos parametrai**.
    2. **Įmonės vidaus** skirtuke pasirinkite įsigijimų kategoriją, kad sutapdintumėte automatiškai sugeneruotas tiekėjo sąskaitas faktūras.
    3. **Numatytoje kategorijoje** pasirinkite **Įmonės vidaus ištekliai**.
    4. Pasirinkite juridinį objektą **GBPM** ir eikite į **Projektų valdymas ir apskaita** > **Nustatyti** > **Projektų valdymo ir apskaitos parametrai**.
    5. **Įmonės vidaus** skirtuke kiekvienam operacijų tipui pasirinkite numatytąją projekto kategoriją. Projekto kategorijos naudojamos mokesčių konfigūracijoje, kai vidinės įmonės operacijų SF išrašymo kategorija taikoma tik besiskolinančiam juridiniam subjektui. Galite pasirinkti, kaip kaupti vidinės įmonės operacijų įplaukas. Kaupimas vyksta, kai operacijos užregistruojamos skolinimo juridiniame objekte, naudojant „Project Operations“ integravimo žurnalą. Žurnalas anuliuojamas, kai užregistruojama įmonės vidaus sąskaita faktūra.
    6. **Skolinant išteklius** grupėje pasirinkite **...** > **Naujas**. 
    7. Tinklelyje pasirinkite toliau nurodytą informaciją:

          - **Skolinimosi juridinis objektas** = **USPM**
          - **Kaupti įplaukas** = **Taip**
          - **Numatytoji grafiko kategorija** = **Numatytoji – valanda**
          - **Numatytoji išlaidų kategorija** = **Numatytoji – išlaidos**

4. **Įmonės vidaus kaštų ir įplaukų sąskaitų nustatymas naudojant registravimo DK nustatymus**. Įmonės vidaus įplaukų sąskaita kredituojama, kai įmonės vidaus kliento sąskaita faktūra užregistruojama skolinimo juridiniame objekte. Įmonės vidaus išlaidų sąskaita debetuojama, kai sutampanti tiekėjo sąskaita faktūra užregistruojama skolinimosi juridiniame objekte. Šios sąskaitos nustatomos atitinkamuose juridiniuose objektuose. 
      
     1. Finansų srityje pasirinkite skolinimosi juridinį objektą **USPM**. 
     2. Eikite į **Projektų valdymas ir apskaita** > **Nustatyti** > **Registravimas** > **Registravimo DK nustatymai**. 
     3. Skirtuko **Išlaidų sąskaitos** lauke **DK sąskaitos tipas** pasirinkite **Vidinės įmonės išlaidos**. Sukurkite naują įrašą nurodydami toliau pateiktą informaciją:
      
        - **Skolinimo juridinis objektas** = **GBPM**
        - **Pagrindinė sąskaita** = pasirinkite įmonės vidaus išlaidų pagrindinę sąskaitą. Ši sąranka yra būtina. Ši sąranka naudojama „Finance“ vidinės įmonės srautams, bet ne su projektais susijusiems vidinės įmonės srautams. Ši pasirinktis tolimesniems procesams įtakos neturi. 
        
     4. Pasirinkite skolinimo juridinį objektą **GBPM**. 
     5. Eikite į **Projektų valdymas ir apskaita** > **Nustatyti** > **Registravimas** > **Registravimo DK nustatymai**. 
     6. Skirtuko **Įplaukų sąskaitos** lauke **DK sąskaitos tipas** pasirinkite **Vidinės įmonės įplaukos**. Sukurkite naują įrašą nurodydami toliau pateiktą informaciją:

        - **Skolinimosi juridinis objektas** = **USPM**
        - **Pagrindinė sąskaita** = pasirinkite įmonės vidaus įplaukų pagrindinę sąskaitą. Ši sąranka yra būtina. Ši sąranka naudojama „Finance“ vidinės įmonės srautams, bet ne su projektais susijusiems vidinės įmonės srautams. Ši pasirinktis tolimesniems procesams įtakos neturi. 

5. **Perdavimo kainodaros už darbą nustatymas**. Įmonės vidaus perdavimo kainodara konfigūruojama „Project Operations“ „Dataverse“ aplinkoje. Konfigūruokite įmonės vidaus SF išrašymo [darbo savikainos tarifus](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) ir [darbo sąskaitų tarifus](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions). Perdavimo kainodara nepalaikoma atliekant įmonės vidaus išlaidų operacijas. Pardavimo tarp organizacijų kaina visada bus nustatyta tokia pati, kaip ir išteklių skyrimo vieneto savikaina.

      „Contoso“ Robotics UK kūrėjų išteklių kaštai yra 88 GBP per valandą. „Contoso Robotics UK“ už kiekvieną valandą, kai šis išteklius dirba su JAV projektais, „Contoso Robotics USA“ apmokestina 120 USD. „Contoso Robotics USA“ už „Contoso Robotics UK“ kūrėjų ištekliaus atliktą darbą klientą „Adventure Works“ apmokestins 200 USD.

      1. „Project Operations“ „Dataverse“ aplinkoje eikite į **Pardavimas** > **Kainoraščiai**. Sukurkite naują savikainos kainoraštį pavadinimu **„Contoso Robotics UK“ savikainos tarifai**. 
      2. Savikainos kainoraštyje sukurkite įrašą nurodydami toliau pateiktą informaciją:
         - **Vaidmuo** = **Kūrėjas**
         - **Savikaina** = **88 GBP**
      3. Nueikite į **Parametrai** > **Organizaciniai vienetai** ir šį savikainos kainoraštį pridėkite prie organizacinio vieneto **„Contoso Robotics UK“**.
      4. Eikite į **Pardavimas** > **Kainoraščiai**. Sukurkite savikainos kainoraštį pavadinimu **„Contoso Robotics USA“ savikainos tarifai**. 
      5. Savikainos kainoraštyje sukurkite įrašą nurodydami toliau pateiktą informaciją:
          - **Vaidmuo** = **Kūrėjas**
          - **Išteklių paskirstymo įmonė** = **„Contoso Robotics UK“**
          - **Savikaina** = **120 USD**
      6. Nueikite į **Parametrai** > **Organizaciniai vienetai** ir savikainos kainoraštį **„Contoso Robotics USA“ savikainos tarifai** pridėkite prie organizacinio vieneto **„Contoso Robotics USA“**.
      7. Eikite į **Pardavimas** > **Kainoraščiai**. Sukurkite pardavimo kainoraštį, pavadintą **„Adventure Works“ sąskaitų tarifai**. 
      8. Pardavimo kainoraštyje sukurkite įrašą nurodydami toliau pateiktą informaciją:
          - **Vaidmuo** = **Kūrėjas**
          - **Išteklių paskirstymo įmonė** = **„Contoso Robotics UK“**
          - **Sąskaitos tarifas** = **200 USD**
      9. Eikite į **Pardavimas** > **Projekto sutartys** ir pridėkite " **„Adventure Works“ sąskaitų tarifų** kainoraštį prie „Adventure Works“ projekto sutarties projekto kainoraščio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
