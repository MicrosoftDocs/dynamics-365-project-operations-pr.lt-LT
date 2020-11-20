---
title: „Project Operations“ integracijos konfigūravimas juridiniam subjektui
description: Šioje temoje pateikta informacija apie juridinio subjekto integracijos nustatymą naudojant „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122893"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>„Project Operations“ integracijos konfigūravimas juridiniam subjektui 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje nurodyta, kokius veiksmus reikia atlikti norint sukonfigūruoti „Dynamics 365 Project Operations“ juridiniam subjektui.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Funkcijų klavišų įjungimas naudojant „Dynamics 365 Finance“

Norėdami įjungti būtinas funkcijas atlikite toliau nurodytus veiksmus.

1. Naudodami „Dynamics 365 Finance“ eikite į **Funkcijų valdymo** darbo sritį.
2. **Funkcijų sąraše** raskite ir įjunkite šias funkcijas:
  
    - **Įjungti keletą projekto sutarties eilučių**
    - **Įjungti „Project Operations“ naudojant „Dynamics 365 Customer Engagement“**

> [!NOTE]
> Jei nematote išvardytų **Funkcijų klavišų**, patikrinkite, ar jūsų „Finance“ versija atitinka mažiausią versijos reikalavimą (programos 10.0.13 versija su visais kokybės atnaujinimais arba naujesnė). Norėdami atnaujinti funkcijų sąrašą pasirinkite **Tikrinti, ar yra naujinimų**.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>„Project Operations“ juridinio subjekto visuotinio diegimo scenarijaus apibrėžimas

Galite įjungti „Project Operations“ „Dynamics 365 Customer Engagement“ juridinio subjekto lygiu. Galite turėti vieną juridinį subjektą naudodami „Project Operations“ „Dynamics 365 Customer Engagement“ išteklių / ne atsargomis pagrįstuose scenarijuose. Toje pačioje aplinkoje galite turėti kitą juridinį subjektą naudodami „Project Operations“ atsargų / gamybos užsakymų scenarijuose.

1. Naudodami „Dynamics 365 Finance“ eikite į **Projektų valdymas ir apskaita** > **Sąranka** > **Visuotinio projektų valdymo ir apskaitos parametrai**.
2. Galimų juridinių subjektų sąraše pasirinkite subjektus, kuriuose bus įgalintos kelios sutarčių eilučių ir „Project Operations“ „Dynamics 365 Customer Engagement“ funkcijos. Palikite nepasirinktus juridinius subjektus, kurie naudos „Project Operations“ atsargų / gamybos užsakymų scenarijams.

> [!NOTE]
> Juridinį subjektą galima pasirinkti tik tuo atveju, jeigu jis neturi esamų projektų.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektų valdymo ir apskaitos parametrų konfigūravimas

Kiekvienas juridinis subjektas, naudojantis „Project Operations“ „Dynamics 365 Customer Engagement“, turi turėti numatytųjų parametrų rinkinį. Šie parametrai sukonfigūruoti skirtuke **Project Operations**, puslapyje **Projektų valdymo ir apskaitos parametrai**. Parametrai:

  - **Atsiskaitymo tipo numatytosios reikšmės**: „Project Operations“ naudoja nustatytą atsiskaitymo tipo numatytųjų reikšmių rinkinį, kuris turi būti susietas su eilučių ypatybėms Finansai. Sukurkite kiekvieno atsiskaitymo tipo įrašą: **Nenurodyta**, **Apmokestinama**, **Neapmokestinama**, **Nemokama** ir **Nepasiekiama**.
  - **Projekto kategorijų numatytosios reikšmės** : pasirinkite numatytąsias projekto kategorijas, kurios bus naudojamos kiekvienam operacijų tipui. Šios numatytosios reikšmės bus naudojamos **„Project Operations“ integracijos žurnale** ir įvertinimuose, kur nėra nurodytos faktinio projekto operacijos kategorijos.
  - **Prognozės** : pasirinkite prognozės modelį, kuris bus naudojamas laiko ir išlaidų įvertinimams.
