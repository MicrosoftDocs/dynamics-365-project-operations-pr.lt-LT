---
title: Tvirtinimų apžvalga
description: Šioje temoje pateikta informacija, kaip dirbti su patvirtinimais programoje „Project Operations“.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961176"
---
# <a name="approvals-overview"></a>Tvirtinimų apžvalga

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Laiko ir išlaidų pateikimai vyksta per patvirtinimo darbo eigą. Patvirtinus įrašus, operacijos įrašomos faktiniuose duomenyse arba laikas rezervuojamas grafike.

## <a name="approvals-workflow"></a>Patvirtinimų darbo eiga
Kai kuriate ir pateikiate laiko arba išlaidų įrašą, sukuriamas patvirtinimo įrašas. Projekto tvirtintojas arba jūsų vadovas peržiūri ir patvirtina įrašą. Jei įrašas yra susijęs su projektu, jį patvirtinus, bus sukurti faktiniai duomenys. Tai leidžia sekti išlaidas ir sąskaitas. 

## <a name="approve-an-entry"></a>Įrašo patvirtinimas
**Patvirtinimo** forma leidžia persijungti iš skirtingų rodinių, kad galėtumėte peržiūrėti skirtingų tipų patvirtinimus.
  
1. Eikite į **Patvirtinimų** formą ir pasirinkite **Išlaidos**, **Laikas**arba **Atšaukimai**.
2. Peržiūrėkite kiekvieną patvirtinimą ir pažymėkite tuos, kuriuos norite patvirtinti.
3. Pažymėkite **Patvirtinti**, kad patvirtintumėte pažymėtus įrašus.
Sistema apdoros šiuos įrašus ir sukurs faktinius duomenis arba užsakymą.

## <a name="reject-an-entry"></a>Įrašo atmetimas
Kaip projektų tvirtintojui, jums gali tekti nusiųsti įrašą atgal vartotojui pataisymui.
  
1. Eikite į formą **Patvirtinimai** ir pasirinkite įrašą, kurį norite atmesti. 
2. Pasirinkite **Atmesti**.
3. Pasirinktinai – dialogo lange **Atmetimo komentarai** įtraukite komentarą, kad informuotumėte vartotoją, kodėl įrašas yra atmetamas.
4. Pasirinkite **Gerai**. Įrašas bus grąžintas vartotojui.
  
## <a name="recall-entries"></a>Įrašų atšaukimas
Tam tikru momentu gali prireikti atšaukti pateiktą įrašą. Jei įrašas nebuvo patvirtintas, jis bus nedelsiant grąžintas. Tačiau patvirtintas įrašas gali turėti reikšmingą poveikį. Projektų tvirtintojas privalo patvirtinti atšaukimą tam, kad pakeisti operaciją faktiniuose duomenyse.

## <a name="specify-project-approvers"></a>Projekto tvirtintojų nurodymas
Kiekvienas projektas turi keletą projekto komandos narių. Galite nurodyti, kurie komandos nariai taip pat yra projektų tvirtintojai.

1. Eikite į formą **Projektai** ir atidarykite projektą iš sąrašo.
2. Skirtuke **Komanda** pasirinkite komandos narį, kuris bus projekto tvirtintojas ir pasirinkite **Redaguoti**.
3. Nustatykite lauką **Projekto tvirtintojas** į **Taip**.
4. Pasirinkite **Įrašyti**.
5. Pakartokite 2–4 veiksmus, jei norite įtraukti papildomų projekto tvirtintojų.

## <a name="configure-the-users-manager"></a>Vartotojo vadovo konfigūravimas

1. Pasirinkite **Parametrai** > **Sauga** > **Vartotojai**.
2. Pažymėkite vartotoją, kuriam priskiriate vadovą ir srityje **Organizacijos informacija** sąraše pasirinkite vadovą. 
3. Pasirinkite **Įrašyti**.


