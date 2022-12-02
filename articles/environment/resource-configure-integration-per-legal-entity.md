---
title: „Project Operations“ integracijos konfigūravimas juridiniam subjektui
description: Šiame straipsnyje pateikta informacija apie juridinio subjekto integracijos nustatymą naudojant „Project Operations“.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914688"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>„Project Operations“ integracijos konfigūravimas juridiniam subjektui 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šiame straipsnyje pateikti kiekvienam juridiniam subjektui konfigūruoti „Dynamics 365 Project Operations“ būtini žingsniai.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Įjungti „Dynamics 365 Finance“ funkcijos raktus

Norėdami įjungti būtinas funkcijas atlikite toliau nurodytus veiksmus.

1. „Dynamics 365 Finance“ nueikite į darbo sritį **Funkcijų tvarkymas**.
2. **Funkcijų sąraše** raskite ir įjunkite šias funkcijas:
  
    - **Įjungti keletą projekto sutarties eilučių**
    - **„Project Operations‟ įjungimas „Dynamics 365 Customer Engagement‟**

> [!NOTE]
> Jei nematote išvardytų **Funkcijų klavišų**, patikrinkite, ar jūsų „Finance“ versija atitinka mažiausią versijos reikalavimą (programos 10.0.13 versija su visais kokybės atnaujinimais arba naujesnė). Norėdami atnaujinti funkcijų sąrašą pasirinkite **Tikrinti, ar yra naujinimų**.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>„Project Operations“ juridinio subjekto visuotinio diegimo scenarijaus apibrėžimas

Galite įjungti „Project Operations“ „Dynamics 365 Customer Engagement“ juridinio subjekto lygiu. Galite turėti vieną juridinį subjektą naudodami „Project Operations“ „Dynamics 365 Customer Engagement“ išteklių / ne atsargomis pagrįstuose scenarijuose. Toje pačioje aplinkoje galite turėti kitą juridinį subjektą naudodami „Project Operations“ atsargų / gamybos užsakymų scenarijuose.

1. Naudodami „Dynamics 365 Finance“ eikite į **projektų valdymas ir apskaita** > **Sąranka** > **Visuotinio projektų valdymo ir apskaitos parametrai**.
2. Galimų juridinių subjektų sąraše pasirinkite subjektus, kuriuose bus įgalintos kelios sutarčių eilučių ir „Project Operations“ „Dynamics 365 Customer Engagement“ funkcijos. Palikite nepasirinktus juridinius subjektus, kurie naudos „Project Operations“ atsargų / gamybos užsakymų scenarijams.

> [!NOTE]
> Juridinį subjektą galima pasirinkti tik tuo atveju, jeigu jis neturi esamų projektų.

## <a name="configure-project-management-and-accounting-parameters"></a>Projektų valdymo ir apskaitos parametrų konfigūravimas

Kiekvienas juridinis subjektas, naudojantis „Project Operations“ „Dynamics 365 Customer Engagement“, turi turėti numatytųjų parametrų rinkinį. Šie parametrai sukonfigūruoti skirtuke **Project Operations**, puslapyje **Projektų valdymo ir apskaitos parametrai**. Parametrai:

  - **Atsiskaitymo tipo numatytosios reikšmės**: „Project Operations“ naudoja nustatytą atsiskaitymo tipo numatytųjų reikšmių rinkinį, kuris turi būti susietas su eilučių ypatybėms Finansai. Sukurkite kiekvieno atsiskaitymo tipo įrašą: **Nenurodyta**, **Apmokestinama**, **Neapmokestinama**, **Nemokama** ir **Nepasiekiama**.
  - **Projekto kategorijų numatytosios reikšmės** : pasirinkite numatytąsias projekto kategorijas, kurios bus naudojamos kiekvienam operacijų tipui. Šios numatytosios reikšmės bus naudojamos **„Project Operations“ integracijos žurnale** ir įvertinimuose, kur nėra nurodytos faktinio projekto operacijos kategorijos.
  - **Prognozės** : pasirinkite prognozės modelį, kuris bus naudojamas laiko ir išlaidų įvertinimams.


[!INCLUDE[footer-include](../includes/footer-banner.md)]