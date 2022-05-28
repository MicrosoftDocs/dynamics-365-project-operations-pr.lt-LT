---
title: „Project Operations“ integracijos konfigūravimas juridiniam subjektui
description: Šioje temoje pateikta informacija apie juridinio subjekto integracijos nustatymą naudojant „Project Operations“.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64606a20a49fd8e9602b6ac3c1ab1880796eb128
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585848"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>„Project Operations“ integracijos konfigūravimas juridiniam subjektui 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje pateikti kiekvienam juridiniam subjektui konfigūruoti „Dynamics 365 Project Operations“ būtini žingsniai.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Įgalinti priemonių raktus Dynamics 365 Finance

Norėdami įjungti būtinas funkcijas atlikite toliau nurodytus veiksmus.

1. Dalyje Dynamics 365 Finance eikite į **darbo sritį Funkcijų valdymas**.
2. **Funkcijų sąraše** raskite ir įjunkite šias funkcijas:
  
    - **Įjungti keletą projekto sutarties eilučių**
    - **Įgalinti projekto operacijas Dynamics 365 Customer Engagement**

> [!NOTE]
> Jei nematote išvardytų **Funkcijų klavišų**, patikrinkite, ar jūsų „Finance“ versija atitinka mažiausią versijos reikalavimą (programos 10.0.13 versija su visais kokybės atnaujinimais arba naujesnė). Norėdami atnaujinti funkcijų sąrašą pasirinkite **Tikrinti, ar yra naujinimų**.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>„Project Operations“ juridinio subjekto visuotinio diegimo scenarijaus apibrėžimas

Galite įgalinti "Project Operations" Dynamics 365 Customer Engagement juridinio subjekto lygiu. Galite turėti vieną juridinį subjektą, kuris naudoja "Project Operations" Dynamics 365 Customer Engagement išteklių / nekauptų scenarijų. Toje pačioje aplinkoje galite turėti kitą juridinį subjektą naudodami „Project Operations“ atsargų / gamybos užsakymų scenarijuose.

1. Dynamics 365 Finance eikite į **Projektų valdymo ir apskaitos** > **nustatymas Visuotiniai** > **projektų valdymo ir apskaitos parametrai**.
2. Galimų juridinių subjektų sąraše pasirinkite objektus, kuriuose bus įgalintos kelios sutarties eilutės ir projekto operacijos Dynamics 365 Customer Engagement priemonėse. Palikite nepasirinktus juridinius subjektus, kurie naudos „Project Operations“ atsargų / gamybos užsakymų scenarijams.

> [!NOTE]
> Juridinį subjektą galima pasirinkti tik tuo atveju, jeigu jis neturi esamų projektų.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektų valdymo ir apskaitos parametrų konfigūravimas

Kiekvienam juridiniam subjektui, naudojantiam "Project Operations" Dynamics 365 Customer Engagement reikia numatytųjų parametrų rinkinio. Šie parametrai sukonfigūruoti skirtuke **Project Operations**, puslapyje **Projektų valdymo ir apskaitos parametrai**. Parametrai:

  - **Atsiskaitymo tipo numatytosios reikšmės**: „Project Operations“ naudoja nustatytą atsiskaitymo tipo numatytųjų reikšmių rinkinį, kuris turi būti susietas su eilučių ypatybėms Finansai. Sukurkite kiekvieno atsiskaitymo tipo įrašą: **Nenurodyta**, **Apmokestinama**, **Neapmokestinama**, **Nemokama** ir **Nepasiekiama**.
  - **Projekto kategorijų numatytosios reikšmės** : pasirinkite numatytąsias projekto kategorijas, kurios bus naudojamos kiekvienam operacijų tipui. Šios numatytosios reikšmės bus naudojamos **„Project Operations“ integracijos žurnale** ir įvertinimuose, kur nėra nurodytos faktinio projekto operacijos kategorijos.
  - **Prognozės** : pasirinkite prognozės modelį, kuris bus naudojamas laiko ir išlaidų įvertinimams.


[!INCLUDE[footer-include](../includes/footer-banner.md)]