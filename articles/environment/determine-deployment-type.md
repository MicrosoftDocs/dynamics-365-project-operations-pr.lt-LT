---
title: Visuotinio diegimo tipo nustatymas
description: Šioje temoje pateikta informacija padės jums nustatyti teisingą visuotinio diegimo tipą, skirtą jūsų įmonės „Project Operations“.
author: stsporen
ms.date: 03/15/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 280578b2710a0bccd1973b51b062fef7a2997780
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584146"
---
# <a name="determine-your-deployment-type"></a>Visuotinio diegimo tipo nustatymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

> [!IMPORTANT]
> Įsigę licenciją, čia nustatykite geriausią „Dynamics 365 Project Operations“ visuotinio diegimo modelį naudodamiesi [interaktyviuoju diegimo srautu](https://aka.ms/provisionprojectoperations).
> Baigę interaktyvųjį diegimo srautą, būsite nukreipti į tinkamą valdymo portalą, kur galėsite baigti diegimą. Norėdami baigti diegimą, žr. diegimo informaciją.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Esami „Dynamics“ klientai, naudojantys „Dynamics 365 Project Service Automation“
„Project Operations“ pateikiamos galimybės, pristatytos su „Project Service Automation“. Naujovinimo kelias šiems klientams bus išleistas 2021 m. 1-osios leidimų bangos metu.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Esami Dynamics 365 Finance klientai, naudojantys projektų valdymą ir apskaitą 

Esami „Finance“ klientai, naudojantys projektų valdymo ir apskaitos funkcijas, gali ją naudoti taip, kaip dabar. Žr. [„Project Operations“, skirta laikomų medžiagų / gamybos užsakymo scenarijams](#pma).


## <a name="deployment-regions"></a>Visuotinio diegimo regionai
Norėdami nustatyti, kurie regionai palaikytų „Project Operations“ visuotinį diegimą, žr. [„Dynamics 365“ ir „Power Platform“ ataskaitų geografinis pasiekiamumas](https://dynamics.microsoft.com/en-us/geographic-availability/). Pasirinkite **Peržiūrėti ataskaitą** ir išplėskite **„Dynamics 365“ > „Operations“ programos > „Dynamics 365 Project Operations“** ir peržiūrėkite palaikomus regionus.

## <a name="deployment-types"></a>Visuotinio diegimo tipai
„Project Operations“ palaiko kelias visuotinio diegimo parinktis, atitinkančias jūsų reikalavimus. Jei esate naujas ar esamas „Dynamics 365“ klientas, „Project Operations“ gali atitikti jūsų poreikius.

Mūsų [Vsuotinio diegimo klausimynas](https://aka.ms/provisionprojectoperations) padės nustatyti tinkamą visuotinį diegimą. Remiantis rezultatais, galėsite pasirinkti vieną iš šių visuotinio diegimo tipų:

- [„Lite“ įdiegtis – sandoris į išankstinės sąskaitos faktūros formą](#lite)
- [„Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams](#integrated)
- [„Project Operations“, skirta laikomų medžiagų / gamybos užsakymo scenarijams](#pma)

„Project Operations“ palaiko laikomų medžiagų / gamybos užsakymo scenarijus ir nelaikomų medžiagų / ištekliais pagrįstus scenarijus toje pačioje aplinkoje, naudojant juridinio objekto lygio konfigūracijas. Pavyzdžiui, „Contoso“ gali naudoti savo JAV gamybos patalpų (juridinis subjektas = „Contoso Manufacturing United States“) laikomas / gamybos užsakymo galimybes. „Contoso“ gali naudoti nelaikomas / ištekliais pagrįstas galimybes savo „Contoso Robotics Arms“ techninės priežiūros patalpose JK (juridinis objektas = „Contoso Robotics United Kingdom“).

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a>Supaprastinta įdiegtis – sandoris į išankstinės sąskaitos faktūros formą

„Lite“ visuotinis diegimas turi šias galimybes:

- Projektų pardavimo procesas, išplečiantis „Dynamics 365 Sales“ programos pardavimo galimybes
- Projekto planavimas naudojant „Microsoft Project“, skirtą žiniatinkliui
- Kelių dimensijų įkainiai
- Vieningasis išteklių valdymas
- Laiko sekimas
- Pagrindinės išlaidos
- Išankstinių sąskaitų faktūrų išrašymas projektų vadovui peržiūrėti ir redaguoti 

#### <a name="deployment-steps"></a>Visuotinio diegimo veiksmai
Nustatykite geriausią „Project Operations“ visuotinio diegimo modelį naudodami [Visuotinio diegimo klausimyną](https://aka.ms/provisionprojectoperations).

Šio diegimo ieškokite skiltyse [Užsiregistruokite prenumeratų peržiūros versijai](lite-preview-subscription-sign-up.md) ir [Naujos aplinkos konfigūravimas](lite-deployment.md). 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a>„Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams
„Project Operations“, skirtos ištekliams / nelaikomų medžiagų scenarijams, yra šios galimybės:
 
- Projektų pardavimo procesas, išplečiantis „Dynamics 365 Sales“ programą
- Projekto planavimas naudojant „Microsoft Project“, skirtą žiniatinkliui
- Kelių dimensijų įkainiai
- Vieningasis išteklių valdymas
- Laiko sekimas
- Pagrindinės išlaidos
- Visos išlaidos
- OCR kvitas
- „Proforma“ ir klientams prieinamos sąskaitos faktūros 
- Projektų pajamų pripažinimas

#### <a name="deployment-steps"></a>Visuotinio diegimo veiksmai
Nustatykite geriausią „Project Operations“ visuotinio diegimo modelį naudodami [Visuotinio diegimo klausimyną](https://aka.ms/provisionprojectoperations).

Šio diegimo ieškokite skiltyse [Užsiregistruokite prenumeratų peržiūros versijai](resource-sign-up-preview-subscription.md) ir [Naujos aplinkos konfigūravimas](resource-provision-new-environment.md). 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a>„Project Operations“, skirta laikomų medžiagų / gamybos užsakymo scenarijams

- Projekto planavimo naudojant WBS
- Išteklių valdymas
- Laiko sekimas
- Visos išlaidos
- OCR kvitas
- Visiškas SF išrašymas
- Pajamų pripažinimas
- Gamybos užsakymai
- Sandėliuojamų medžiagų palaikymas ir atsargos

#### <a name="deployment-steps"></a>Visuotinio diegimo veiksmai
Nustatykite geriausią „Project Operations“ visuotinio diegimo modelį naudodami [Visuotinio diegimo klausimyną](https://aka.ms/provisionprojectoperations).

Šio diegimo ieškokite skiltyse [Užsiregistruokite prenumeratų peržiūros versijai](/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=%2fdynamics365%2ffinance%2ftoc.json) ir [Naujos aplinkos konfigūravimas](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=%2fdynamics365%2ffinance%2ftoc.json). 



[!INCLUDE[footer-include](../includes/footer-banner.md)]