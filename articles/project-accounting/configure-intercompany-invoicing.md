---
title: Įmonės vidaus SF išrašymo konfigūravimas
description: Šiame straipsnyje pateikta informacija ir pavyzdžiai apie įmonės vidaus SF išrašymo už projektus konfigūravimą.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ae0c2662bb6b2789ab520f08c7c21935b651ced5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929408"
---
# <a name="configure-intercompany-invoicing"></a>Įmonės vidaus SF išrašymo konfigūravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Norėdami nustatyti įmonės vidaus SF išrašymą už projektus programoje „Dynamics 365 Project Operations“, atlikite toliau nurodytus veiksmus.. Vidinės įmonės operacijos yra laiko ir išlaidų operacijos iš projekto sutarties, priklausančios vienai įmonei arba organizaciniam vienetui, kai projekto sutarties ištekliai priklauso kitai įmonei arba organizaciniam vienetui.

## <a name="example-configure-intercompany-invoicing"></a>Pavyzdys: įmonės vidaus SF išrašymo konfigūravimas

Toliau pateiktame pavyzdyje „Contoso Robotics USA“ (USPM) yra skolinimosi juridinis objektas, o „Contoso Robotics UK“ (GBPM) yra skolinimo juridinis objektas. 

1. **Įmonės vidaus apskaitos skirtinguose juridiniuose subjektuose konfigūravimas**. Kiekviena skolinimosi ir skolinimo juridinių objektų pora turi būti konfigūruota didžiosios knygos [įmonės vidaus apskaitos](/dynamics365/finance/general-ledger/intercompany-accounting-setup) puslapyje.
    
    1. Programoje „Dynamics 365 Finance“ eikite į **Didžioji knyga** > **Registravimo nustatymas** > **Vidinių įmonių apskaita**. Sukurkite įrašą nurodydami toliau pateiktą informaciją:

        - **Pradinė įmonė** = **GBPM**
        - **Paskirties įmonė** = **USPM**

2. **Prekybinių ryšių tarp juridinių objektų konfigūravimas**. Kliento įrašas, atspindintis skolinimosi juridinį objektą, turi būti sukurtas skolinimo juridiniame objekte. Tiekėjo įrašas, atspindintis skolinimo juridinį objektą, turi būti sukurtas skolinimosi juridiniame objekte.

     1. Finansų srityje pasirinkite juridinį objektą **GBPM**.
     2. Eikite į **Gautinos sumos** > **Klientas** > **Visi klientai**. Sukurkite naują juridinio objekto įrašą **USPM**.
     3. Išplėskite **pavadinimą**, filtruokite įrašus pagal **tipą** ir pasirinkite **juridinius objektus**. 
     4. Raskite ir pasirinkite **„Contoso Robotics USA“ (USPM)** kliento įrašą.
     5. Pasirinkite **Naudoti atitikmenį**. 
     6. Pasirinkite klientų grupę **50 – vidinės įmonės klientai** ir įrašykite įrašą.
     7. Pasirinkite juridinį objektą **USPM**.
     8. Eikite į **Mokėtinos sumos** > **Tiekėjai** > **Visi tiekėjai**. Sukurkite naują juridinio objekto įrašą **GBPM**.
     9. Išplėskite **pavadinimą**, filtruokite įrašus pagal **tipą** ir pasirinkite **juridinius objektus**. 
     10. Raskite ir pasirinkite **„Contoso Robotics UK“ (GBPM)** kliento įrašą.
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

      „Contoso Robotics UK“ kūrėjo išteklių savikaina yra 88 GBP už vieną valandą. „Contoso Robotics UK“ išrašys „Contoso Robotics USA“ 120 USD sąskaitą už kiekvieną valandą, kai šie ištekliai dirbo su US projektais. „Contoso Robotics USA“ išrašys klientui „Adventure Works“ 200 USD sąskaitą už darbą, kurį atliko „Contoso Robotics UK“ kūrėjo ištekliai.

      1. „Project Operations“ „Dataverse“ aplinkoje eikite į **Pardavimas** > **Kainoraščiai**. Sukurkite naują savikainos kainoraštį, pavadintą **„Contoso Robotics UK“ savikainos tarifai.** 
      2. Savikainos kainoraštyje sukurkite įrašą nurodydami toliau pateiktą informaciją:
         - **Vaidmuo** = **Kūrėjas**
         - **Savikaina** = **88 GBP**
      3. Eikite į **Parametrai** > **Organizacijos vienetai** ir pridėkite šį savikainos kainoraštį prie **Contoso Robotics UK** organizacijos vieneto.
      4. Eikite į **Pardavimas** > **Kainoraščiai**. Sukurkite savikainos kainoraštį, pavadintą **„Contoso Robotics USA“ savikainos tarifai.** 
      5. Savikainos kainoraštyje sukurkite įrašą nurodydami toliau pateiktą informaciją:
          - **Vaidmuo** = **Kūrėjas**
          - **Išteklių paskirstymo įmonė** = **Contoso Robotics UK**
          - **Savikaina** = **120 USD**
      6. Eikite į **Parametrai** > **Organizacijos vienetai** ir pridėkite **„Contoso Robotics USA“ savikainos tarifų** kainoraštį prie **Contoso Robotics UK** organizacijos vieneto.
      7. Eikite į **Pardavimas** > **Kainoraščiai**. Sukurkite pardavimo kainoraštį, pavadintą **„Adventure Works“ sąskaitų tarifai**. 
      8. Pardavimo kainoraštyje sukurkite įrašą nurodydami toliau pateiktą informaciją:
          - **Vaidmuo** = **Kūrėjas**
          - **Išteklių paskirstymo įmonė** = **Contoso Robotics UK**
          - **Sąskaitos tarifas** = **200 USD**
      9. Eikite į **Pardavimas** > **Projekto sutartys** ir pridėkite " **„Adventure Works“ sąskaitų tarifų** kainoraštį prie „Adventure Works“ projekto sutarties projekto kainoraščio.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
