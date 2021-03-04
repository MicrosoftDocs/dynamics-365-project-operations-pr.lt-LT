---
title: Projekto šablono kūrimas
description: Projekto šablono kūrimas „Project Service“
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: efc404131208e1c971cb091cf174c1f4707552f0
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149373"
---
# <a name="create-a-project-template-project-service"></a>Projekto šablono kūrimas („Project Service“)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Naudojant Projektų šablonus galima sutaupyti laiko, jei jūsų įmonė reguliariai teikia pasiūlymus dėl panašių tipų projektų. Juose pateikiamas standartinis tam tikto tipo projekto vaidmenų ir numatomų valandų rinkinys. Klientų vadovai ir projektų vadovai gali kurti projektus pagal projekto šabloną arba kopijuoti šabloną ir susikurti savąjį.  
  
## <a name="components-of-project-template"></a>Projekto šablono komponentai
 Projekto šabloną sudaro trys toliau nurodyti komponentai.  
  
- **Darbo paskirstymo struktūra**: darbo paskirstymo struktūrą projekto šablone sudaro tie patys elementai kaip ir projekte. Galite kurti užduočių hierarchiją, susieti vaidmenis su užduotimis, nustatyti grafiko atributus, nustatyti priklausomybes ir peržiūrėti visus Ganto diagramos duomenis. Projekto šablonų darbo paskirstymo struktūra taip pat palaiko visų užduočių režimus. Kuriant darbo grafiką, skirtumų tarp projekto šablono ir projekto nėra.  
  
- **Projekto sąmatos**: projekto šablonų ir projektų sąmatos sudaromos pagal tokį patį principą, išskyrus tai, kad numatytųjų išlaidų kainoraščiai ir pardavimo kainos visada yra numatytosios išlaidos ir pardavimo kainų sąrašai, nustatyti „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ parametruose. Kitos funkcijos yra tokios pat kaip projekte.  
  
- **Projekto komandos formavimas**: formuojant projekto komandą projekto šablone, jame negalima užsisakyti pavadino ištekliaus. Galite naudoti parinktį **Generuoti projekto komandą** darbo paskirstymo struktūroje, kad sukurtumėte bendrųjų išteklių rinkinį. Taip pat galite nurodyti reikiamus bendrųjų išteklių įgūdžius ir kvalifikaciją. Projekto šablonuose bendrojo ištekliaus negalima pakeisti rezervuojamu ištekliumi.  
  
## <a name="create-a-project-from-a-template"></a>Projekto kūrimas pagal šabloną  
 Projektą kurti šabloną galima toliau nurodytais būdais.  
  
-   Kurdami projektą pagal pasiūlymą, projekto šabloną galite pasirinkti projekto sparčiojo kūrimo formoje.  
  
-   Kai projektą kuriate spustelėję **Naujas projektas**, prieš įrašant įrašą rodoma projekto forma. Joje galite spustelėti lauką **Pasirinkti šabloną** ir pasirinkti iš jūsų organizacijoje iš anksto nustatytų šablonų sąrašo.  
  
-   Spustelėkite **Kurti projektą pagal šabloną** puslapyje **Projekto šablonas**, kad sukurtumėte projektą pagal šabloną.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Šablono komponentų kopijavimas į projektą  
 Jei kopijuojate šablono komponentus į projektą, įsidėmėkite kelis dalykus.  
  
 **Darbo paskirstymo struktūros kopijavimas**: kai iš projekto šablono kopijuojate darbo paskirstymo struktūrą, jei projekto kalendorius skiriasi nuo šablono kalendoriaus, užduočių grafike bus taikomos projekto kalendoriaus darbo valandos. Tokiu būdu grafikas yra pakoreguojamas pagal atsarginį projekto kalendorių. Panašiai pirmoji darbo paskirstymo struktūros užduotis perima projekto pradžios datą, todėl likęs užduočių hierarchijos grafikas yra atnaujinamas pagal trukmę ir priklausomybes, nurodytas šablono darbo paskirstymo struktūroje.  
  
 **Projekto sąmatos kopijavimas**: kai kopijuojate keliose projekto sąmatų eilutėse, kainoraščiai atnaujinami pagal projekto valdančio vieneto savikainų sąrašą ir kliento pardavimo kainų sąrašą. Pagal šiuos sąrašus nustatomos vieneto savikainos ir pardavimo kainos projektuose, susijusiuose su pardavimo objektu.  
  
 **Projekto komandos kopijavimas**: kopijuojant projekto komandą iš šablono į projektą, nukopijuojami visi bendrieji resursai ir jų įgūdžiai bei kvalifikacija, nurodyti šablone. Bendrųjų išteklių priskyrimai taip pat tvarkomi kaip ir projekto šablone.  
  
### <a name="see-also"></a>Taip pat žr.  
 [Projekto vadovo vadovas](../psa/project-manager-guide.md)
