---
title: Planuodami savo darbą „Microsoft Project“, naudokite „Project Service“ papildinį | „MicrosoftDocs“
description: Šiame straipsnyje pateikiama informacija apie tai, kaip įtraukti, konfigūruoti ir naudoti "Microsoft Project" priedą, skirtą "Microsoft Project Service".
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d286adfdffa6a0b5f0c96eb14be588c6cedb80c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925544"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Planuodami savo darbą „Microsoft Project“, naudokite „Project Service Automation“ papildinį

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] palengvina projekto planavimą, įskaitant įvertinimus. Darbą galite nustatyti taip, kad, pateikus galutinį pasiūlymą, išlaidų, pastangų ir pardavimo vertė būtų aiški.  

 Dabar galite įdiegti „[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)]“ ir atlikti planavimo darbus pažįstamoje „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]‟ aplinkoje. Pasinaudokite veiksmingomis„[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]‟ planavimo ir valdymo galimybėmis, tada atnaujinkite savo projekto planą „Project Service Automation“.  

> [!IMPORTANT]
> - Tam, kad galėtumėte naudoti SharePoint dokumentų valdymo funkciją [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], kad išsaugotumėte [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projektų failus, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administratorius turės įjungti dokumentų valdymo funkciją. 
> - „[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)]“ yra suderinama tik su „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition“.  

## <a name="download-and-install-the-add-in"></a>Papildinio atsisiuntimas ir įdiegimas  
 Paruoškite savo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] prisijungimo informaciją. Šios informacijos jums reikės, kad iš „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“ prisijungtumėte prie „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“.  

1.  Iš atsisiuntimo centro galite atsisiųsti priedą, skirtą jūsų palaikomai Project Service versijai, arba [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) arba [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Spustelėkite atsisiuntimo saitą.  

3.  Kai atsisiuntimas bus baigtas, spustelėkite **Taip**, kad įdiegtumėte papildinį.  

## <a name="configure-the-add-in"></a>Papildinio konfigūravimas  

1. Atidarykite „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]‟ ir spustelėkite skirtuką **Project Service**.  

2. Spustelėkite **Prijungti**.  

3. Įveskite savo prisijungimo informaciją ir spustelėkite **Prisijungti**.  

   Dabar galite pradėti naudoti papildinį.  

## <a name="read-from-a-template"></a>Skaitymas iš šablono  
 Norėdami pradėti projekto planavimą, skaitykite iš šablono, kurį sukūrėte „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ ir nukopijavote į „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projekto šablono kūrimas („Project Service Automation“)](../psa/create-project-template.md)  

1.  Skirtuke **Project Service** spustelėkite **Skaityti** > **„Project Service Automation‟ projekto šablonas**.  

2.  Pasirinkite projekto šabloną iš sąrašo, tada spustelėkite **Atidaryti**.  

    > [!NOTE]
    >  Pagal numatytuosius nustatymus užduotys, kurios į Projektą nukopijuojamos iš šablono, yra nustatomos kaip suplanuotos rankiniu būdu.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>„[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ vaidmenų priskyrimas projekto ištekliams  

1.  Atidarykite projektą ir spustelėkite juostelę **Užduotys**.  

2.  Spustelėkite meniu **Ganto diagrama** ir pasirinkite **Išteklių aprašą**.  

3.  Išteklių apraše spustelėkite išskleidžiamąjį meniu **„Project Service“ išteklių vaidmuo** ir pasirinkite „Project Service Automation“ vaidmenį.  

## <a name="staff-your-project-with-resources"></a>Projekto aprūpinimas ištekliais  

1.  Skirtuke „Project Service“ pasirinkite eilutę ir spustelėkite **Rasti išteklių**.  

2.  Ekrane **Rezervuoti išteklius** pasirinkite norimą naudoti projekto išteklių.  

3.  Spustelėkite **Rezervuoti**, tada spustelėkite **Gerai**.  

## <a name="publish-your-project"></a>Projekto publikavimas  
Baigus projekto planavimą, kitas veiksmas yra importuoti ir publikuoti projektą [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projektas bus importuotas į [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Taikomas kainodaros ir komandos formavimo procesas. Atidarykite projektą [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], kad pamatytumėte, jog komanda, projekto įvertinimai ir darbo paskirstymo struktūra buvo sugeneruoti. Tolesnėje lentelėje parodyta, kur rasti rezultatus.

| Project | Informacija |
| ---- | --- |
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ganto diagrama**   | Importuojama į „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ ekraną **Darbo paskirstymo struktūra**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Išteklių aprašas** |   Importuojama į „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ ekraną **Project Team Members**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Naudojimas**    |    Importuojama į „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ ekraną **Projekto įvertinimai**.     |

**Projekto importavimas ir publikavimas**  
1. Skirtuke **Project Service** spustelėkite **Publikuoti** > **Naujas „Project Service Automation‟ projektas**.  

2. Dialogo lange **Publikuoti naują projektą naudojant „Project Service“** įveskite **Projekto pavadinimą** ir pasirinkite **Klientas**.  

3. Pasirinktinai pažymėkite **Susieti projekto planą su „Project Service Automation“,** kad susietumėte plano Projekto failą su „Project Service Automation“.  

4. Spustelėkite **Publikuoti**.  

   Projekto failą susiejus su [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], Projekto failas tampa pagrindiniu, o darbo paskirstymo struktūra [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nustatoma kaip skirta tik skaityti.  Norėdami pakeisti projekto planą, turite atlikti pakeitimus naudodami „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“ ir publikuoti juos kaip „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ naujinimus.  

## <a name="edit-a-project-thats-been-imported"></a>Importuoto projekto redagavimas  
 Keisti į „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ importuoto projekto planą galite dviem būdais.  

- Atidarykite pagrindinį failą ir jį redaguokite naudodami „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“.  

- Atsieti failą ir jį redaguoti tiesiai „Project Service“. Pagal numatytuosius parametrus projektas, kuris įkeltas iš „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]‟, yra užrakinamas ir jį galima redaguoti tik projekte. Norint redaguoti failą [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], failas turi būti atsietas.  

### <a name="edit-in-pn_microsoft_project"></a>Redaguoti „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“  

1. Pagrindiniame meniu spustelėkite **Project Service** > **Projektai**.  

2. Iš projektų sąrašo pasirinkite ir atidarykite projektą, kurį sukūrėte „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“.  

3. Juostelėje spustelėkite **Atidaryti „MS Project“**. Susietas pagrindinis failas bus atidarytas „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“.  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Atsiekite failą ir redaguokite jį naudodamiesi „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service“  

1. Pagrindiniame meniu spustelėkite **Project Service** > **Projektai**.  

2. Iš projektų sąrašo pasirinkite ir atidarykite projektą, kurį sukūrėte „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“.  

3. Juostelėje spustelėkite **Atsieti nuo „MS Project“**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Įkelkite Projekto failą į SharePoint ar Biuro Grupės  
 Savo Projekto failą galite įkelti į SharePoint ir jį rasti savo [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekto dalyje Susiję Dokumentai.  Turite pasirūpinti, kad jūsų administratorius sukonfigūruotų SharePoint dokumentų valdymą ir įjungtų jį Projekto objektui. 

 Projekto failą taip pat galite nusiųsti į „[!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)]“, jei esate nustatę „Office Groups“.

### <a name="upload-a-file-for-sharepoint"></a>Nusiųsti failą į SharePoint  

1. Pagrindiniame meniu spustelėkite **Project Service** > **Įkelti**.  

2. Pasirinkite **„Project Service Automation“ projekto dokumentai**.  

3. Dialogo lange **Leisti atidaryti programoje „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“** pasirinkite **Taip** arba **Ne**.  

   - Paspaudus **Taip**, galėsite pasirinkti mygtuką **Atidaryti programoje [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, esantį „Project Service Automation“, paleisti [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ir įkelti Projekto failą iš SharePoint dokumentų bibliotekos.  

   - Spustelėjus **Ne**, mygtuko **Atidaryti programoje [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** saitas neveiks.  

4. „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“ failą galima rasti „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ dalyje **Dokumentai** pagal konkretų „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ projektą.  

### <a name="upload-a-file-for-office-groups"></a>Failo, skirto „Office Groups“ įkėlimas  

1. Pagrindiniame meniu spustelėkite **Project Service** > **Įkelti**.  

2. Pasirinkite **„Project Service Automation“ projekto dokumentai**.  

3. Dialogo lange **Leisti atidaryti programoje „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“** pasirinkite **Taip** arba **Ne**.  

   - Paspaudus **Taip**, galėsite pasirinkti mygtuką **Atidaryti programoje [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, esantį „Project Service Automation“, paleisti [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ir įkelti Projekto failą iš SharePoint dokumentų bibliotekos.  

   - Spustelėjus **Ne**, mygtuko **Atidaryti programoje [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** saitas neveiks.  

4. „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“ failą galima rasti „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ dalyje **Dokumentai** pagal konkretų „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ projektą.  

## <a name="publish--your-project-as-a-template"></a>Projekto kaip šablono publikavimas  
 Galite įrašyti savo projektą ir pakartotinai ją naudoti įrašydami jį kaip projekto šabloną [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Projektų šablonai yra daugkartinio naudojimo projektų planai [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Projekto šablono kūrimas („Project Service Automation“)](../psa/create-project-template.md)  

1. Skirtuke **Project Service** spustelėkite **Publikuoti** > **Naujas „Project Service Automation‟ projekto šablonas**.  

2. Dialogo lange **Publikuoti į naują projektą „Project Service“ šablone** įveskite **Projekto šablono pavadinimą**.  

3. Arba pažymėkite **Susieti projekto planą su „Project Service Automation“,** kad susietumėte Projekto failą su [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Spustelėkite **Publikuoti**.  

Projekto failą susiejus su [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], Projekto failas tampa pagrindiniu, o darbo paskirstymo struktūra [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] nustatoma kaip šablonas, skirtas tik skaityti.  Norėdami pakeisti projekto planą, turite atlikti pakeitimus naudodami „[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]“ ir publikuoti juos kaip „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ naujinimus.

## <a name="read-a-resource-loaded-schedule"></a>Išteklių įkelto grafiko skaitymas

Skaitant „Project Service Automation“ projektą, išteklių kalendorius nesinchronizuojamas su stalinio kompiuterio klientu. Jei užduočių trukmės, pastangų arba pabaigos reikšmės skiriasi, tikriausiai dėl to, kad ištekliai ir stalinio kompiuterio klientas neturi paties darbo valandų šablono kalendoriaus, taikomo projektui.


## <a name="data-synchronization"></a>Duomenų sinchronizavimas

Toliau esančioje lentelėje nurodoma, kaip sinchronizuojami duomenys „Project Service Automation“ ir „Microsoft Project“ stalinio kompiuterio papildinyje.

| **Objektas** | **Laukas** | **Iš „Microsoft Project“ į „Project Service Automation“** | **Iš „Project Service Automation“ į „Microsoft Project“** |
| --- | --- | --- | --- |
| Projekto užduotis | Terminas | ● | - |
| Projekto užduotis | Įvertintos pastangos | ● | - |
| Projekto užduotis | „MS Project“ kliento ID | ● | - |
| Projekto užduotis | Pirminė užduotis | ● | - |
| Projekto užduotis | Project | ● | - |
| Projekto užduotis | Projekto užduotis | ● | - |
| Projekto užduotis | Projekto užduoties pavadinimas | ● | - |
| Projekto užduotis | Išteklių paskirstymo vienetas (nebenaudojama v3.0) | ● | - |
| Projekto užduotis | Suplanuota trukmė | ● | - |
| Projekto užduotis | Pradžios data | ● | - |
| Projekto užduotis | WBS ID | ● | - |

| **Objektas** | **Laukas** | **Iš „Microsoft Project“ į „Project Service Automation“** | **Iš „Project Service Automation“ į „Microsoft Project“** |
| --- | --- | --- | --- |
| Komandos narys | „MS Project“ kliento ID | ● | - |
| Komandos narys | Pareigų pavadinimas | ● | - |
| Komandos narys | projektas | ● | ● |
| Komandos narys | Projekto komanda | ● | ● |
| Komandos narys | Išteklių paskirstymo vienetas | - | ● |
| Komandos narys | Vaidmuo | - | ● |
| Komandos narys | Darbo valandos | Nesinchronizuota | Nesinchronizuota |

| **Objektas** | **Laukas** | **Iš „Microsoft Project“ į „Project Service Automation“** | **Iš „Project Service Automation“ į „Microsoft Project“** |
| --- | --- | --- | --- |
| Išteklių priskyrimas | Pradžios data | ● | - |
| Išteklių priskyrimas | Val. | ● | - |
| Išteklių priskyrimas | „MS Project“ kliento ID | ● | - |
| Išteklių priskyrimas | Suplanuotas darbas | ● | - |
| Išteklių priskyrimas | Project | ● | - |
| Išteklių priskyrimas | Projekto komanda | ● | - |
| Išteklių priskyrimas | Išteklių priskyrimas | ● | - |
| Išteklių priskyrimas | Užduotis | ● | - |
| Išteklių priskyrimas | Iki datos | ● | - |

| **Objektas** | **Laukas** | **Iš „Microsoft Project“ į „Project Service Automation“** | **Iš „Project Service Automation“ į „Microsoft Project“** |
| --- | --- | --- | --- |
| Projekto užduoties priklausomybės | Projekto užduoties priklausomybė | ● | - |
| Projekto užduoties priklausomybės | Saito tipas | ● | - |
| Projekto užduoties priklausomybės | Ankstesnė užduotis | ● | - |
| Projekto užduoties priklausomybės | Project | ● | - |
| Projekto užduoties priklausomybės | Vėlesnė užduotis | ● | - |

### <a name="see-also"></a>Taip pat žr.  
 [Projekto vadovo vadovas](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
