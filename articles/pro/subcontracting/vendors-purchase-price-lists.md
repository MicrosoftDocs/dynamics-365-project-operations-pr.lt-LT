---
title: Tiekėjų ir pirkimo kainoraščių valdymas programoje „Project Operations”
description: Šioje temoje pateikta informacija, kuri padės kurti ir prižiūrėti tiekėjo duomenis bei pirkimo kainoraščius, naudojamus subrangos sutarčiai sudaryti.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf62ef8eb87ac2bc138e63c7f92132e00451df6d7766291a8399a94a070799ab
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994151"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Tiekėjų ir pirkimo kainoraščių valdymas programoje „Project Operations”

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

## <a name="vendors-in-project-operations"></a>Tiekėjai programoje „Project Operations”

Programoje „Microsoft Dynamics 365 Project Operations” tiekėjo klientų ryšio tipas yra **Tiekėjas** arba **Pristatytojas**. Pasirinkti galite tik tą kliento įrašą, kuriame nurodytas vienas šių ryšio tipų kaip subrangos sutarties tiekėjas.

Su tiekėjo įrašu galite susieti vieną ar daugiau pirkimo kainoraščių. Tačiau kiekvieno su tiekėjo įrašu susieto pirkimo kainoraščio galiojimo laikotarpis turi būti skirtingas. „Project Operations” nepalaiko persidengiančių pirkimo kainoraščių galiojimo laikotarpių.

Pagal numatytuosius nustatymus toliau nurodyti tiekėjo įrašo laukai ir sąvokos yra naudojami bet kokioje tiekėjui sukurtoje subrangos sutartyje.

- Mokėjimo sąlygos
- Sąskaitų gavėjo kontaktas
- Pagrindinis kontaktinis asmuo

    > [!NOTE]
    > Pagal numatytuosius nustatymus pirminis tiekėjo kontaktas naudojamas kaip subrangos tiekėjo kliento vadovas.

- Valiuta
- Dabartinio pirkimo kainoraščiai

## <a name="purchase-price-lists-in-project-operations"></a>Pirkimo kainoraščiai programoje „Project Operations”

Kainoraštis, kuriame laukas **Kontekstas** nustatytas kaip **Pirkimas** laikomas pirkimo kainoraščiu. Pirkimo kainoraščius galima apibrėžti kaip laiko, išlaidų ir medžiagų pirkimo tarifų katalogą. Pirkimo kainoraščiai yra panašūs į išlaidų ir pardavimo kainoraščius programoje „Project Operations”. Toliau nurodytos sąvokos taikomos pirkimo kainoraščiams taip pat kaip išlaidų ir pardavimo kainoraščiams.

- **Galiojimo laikotarpis** – pirkimo kainoraščiai turi galiojimo laikotarpį. Galiojimo laikotarpį atspindi kiekvieno kainoraščio pradžios datos ir pabaigos datos laukai. Laikas tarp pradžios datos ir pabaigos datos yra galiojimo laikotarpis.
- **Valiuta** – kainoraščio antraštės valiuta yra valiuta, kuria nurodomos darbo, išlaidų kategorijų ir kataloge esančių produktų pirkimo kainos.
- **Numatytasis laiko vienetas** – numatytuoju laiko vienetu išreiškiamos pirkimo darbo kainos. Kainoraščio laiko vieneto laukas naudojamas tik numatytajai reikšmei pateikti. Šią reikšmę galima keisti atskirose vaidmens kainos eilutėse.

Pirkimo kainoraščius galima pridėti prie tiekėjo įrašų kaip asociacijas, žinomas kaip projekto kainoraščiai. Šie kainoraščiai naudojami numatytosioms subrangos sutarties eilučių kainoms įvesti. Pagal numatytuosius nustatymus, kai prie tiekėjo įrašo pridedami keli pirkimo kainoraščiai, tiekėjui kuriamose subrangos sutartyse naudojamas naujausias kainoraštis. Prie tiekėjo įrašų galima pridėti tik tuos kainoraščius, kuriuose laukas **Kontekstas** nustatytas kaip **Pirkimas**.

### <a name="subcontract-specific-purchase-price-lists"></a>Konkrečiai subrangos sutarčiai taikomi pirkimo kainoraščiai

Taip pat pirkimo kainoraščius galima pridėti prie subrangos sutarčių kaip asociacijas, žinomas kaip projekto kainoraščiai. Šie kainoraščiai naudojami numatytosioms subrangos sutarties eilučių kainoms įvesti. Pagal numatytuosius nustatymus, kai prie subrangos sutarties pridedami keli pirkimo kainoraščiai, kiekvieno galiojimo laikotarpis turi būti skirtingas. „Project Operations” nepalaiko persidengiančių pirkimo kainoraščių galiojimo laikotarpių. Prie subrangos sutarčių galima pridėti tik tuos kainoraščius, kuriuose laukas **Kontekstas** nustatytas kaip **Pirkimas**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
