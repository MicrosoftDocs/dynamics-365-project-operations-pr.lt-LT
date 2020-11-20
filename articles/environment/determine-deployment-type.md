---
title: Visuotinio diegimo tipo nustatymas
description: Šioje temoje pateikta informacija padės jums nustatyti teisingą visuotinio diegimo tipą, skirtą jūsų įmonės „Project Operations“.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401228"
---
# <a name="determine-your-deployment-type"></a>Visuotinio diegimo tipo nustatymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

> [!IMPORTANT]
> Įsigiję licenciją, pradėkite čia, kad nustatytumėte geriausią „Dynamics 365 Project Operations“ visuotinio diegimo modelį, pasitelkdami [Interaktyvųjį diegimo srautą](https://aka.ms/provisionprojectoperations).
> Baigę interaktyvųjį diegimo srautą, būsite nukreipti į tinkamą valdymo portalą, kur galėsite baigti diegimą. Norėdami baigti diegimą, žr. diegimo informaciją.


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a>Esami „Dynamics“ klientai, naudojantys „Dynamics 365 Project Service Automation“
„Project Operations“ pateikiamos galimybės, pristatytos su „Project Service Automation“. Naujovinimo kelias šiems klientams bus išleistas 2021 m. 1-osios leidimų bangos metu.

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a>Esami „Dynamics 365 Finance“ klientai, naudojantys projektų valdymą ir apskaitą 

Esami „Finance“ klientai, naudojantys projektų valdymo ir apskaitos funkcijas, gali ją naudoti taip, kaip dabar. Žr. [„Project Operations“, skirta laikomų medžiagų / gamybos užsakymo scenarijams](#pma).


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
- „Proforma“ ir klientams prieinamos sąskaitos faktūros 

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
- Pilnas SF išrašymas
- Pajamų pripažinimas
- Gamybos užsakymai
- Medžiagų palaikymas

#### <a name="deployment-steps"></a>Visuotinio diegimo veiksmai
Nustatykite geriausią „Project Operations“ visuotinio diegimo modelį naudodami [Visuotinio diegimo klausimyną](https://aka.ms/provisionprojectoperations).

Šio diegimo ieškokite skiltyse [Užsiregistruokite prenumeratų peržiūros versijai](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ir [Naujos aplinkos konfigūravimas](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json). 

