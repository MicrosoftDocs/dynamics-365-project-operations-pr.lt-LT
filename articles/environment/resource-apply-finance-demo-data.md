---
title: „Project Operations“ demonstracinių duomenų taikymas debesyje esančioje „Finance“ aplinkoje
description: Šioje temoje aiškinama, kaip taikyti demonstracinius „Project Operations“ duomenis „Dynamics 365 Finance“ debesyje esančioje aplinkoje.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948985"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>„Project Operations“ demonstracinių duomenų taikymas debesyje esančioje „Finance“ aplinkoje

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

>[Svarbu] Ši tema taikoma tik 10.0.13 versijos „Microsoft Dynamics 365 Finance“ ir veiksmus galima atlikti tik debesyje esančiai aplinkai. Atlikite šioje temoje aprašytus veiksmus **PRIEŠ** taikydami kokybinius naujinimus aplinkoje.

1. LCS projekte atidarykite puslapį **Išsami aplinkos informacija**. Atkreipkite dėmesį, kad jame yra išsami informacija, kurios reikia norint prisijungti prie aplinkos naudojant nuotolinio darbalaukio protokolą (RDP).

![Išsami „“ aplinkos informacija](./media/1EnvironmentDetails.png)

Pirmasis paryškintų kredencialų rinkinys yra vietinės paskyros kredencialai ir turi nuotolinio darbalaukio hipersaitą. Kredencialai apima aplinkos administratoriaus vartotojo vardą ir slaptažodį. Antrasis kredencialų rinkinys naudojamas siekiant prisijungti prie „SQL Server“ šioje aplinkoje.

2. Prisijunkite nuotoliniu būdu prie aplinkos naudodami hipersaitą, esantį dalyje **Vietinės paskyros**, ir naudokite **Vietinės paskyros kredencialai**, kad atliktumėte autentifikavimą.
3. Eikite į **Informacinės interneto paslaugos** > **Programų telkiniai** > **AOSService** ir sustabdykite tarnybą. Dabar sustabdėte šią tarnybą, kad galėtumėte tęsti SQL duomenų bazės pakeitimo procesą.

![Sustabdyti AOS](./media/2StopAOS.png)

4. Eikite į **Tarnybos** ir sustabdykite du toliau nurodytus elementus:

- „Microsoft Dynamics 365 Unified Operations“: paketų valdymo tarnyba
- „Microsoft Dynamics 365 Unified Operations“: duomenų importavimo / eksportavimo sistema

![Sustabdyti tarnybas](./media/3StopServices.png)

5. Atidarykite „Microsoft SQL Server Management Studio“. Prisijunkite naudodami SQL serverio kredencialus ir naudokite axdbadmin vartotojo vardą ir slaptažodį iš LCS puslapio **Išsami aplinkos informacija**.

![„SQL Server Management Studio“](./media/4SSMS.png)

6. Objektų naršyklėje raskite **Duomenų bazės** ir raskite **AXDB**. Duomenų bazę pakeisite nauja duomenų baze, esančia [Atsisiuntimo centre](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Nukopijuokite suglaudintą failą į VM, prie kurios esate prisijungę nuotoliniu būdu, ir išskleiskite suglaudinto failo turinį.
8. „SQL Server Management Studio“ spustelėkite dešiniuoju pelės mygtuku **AxDB**, tada pasirinkite **Užduotys** > **Atkūrimas** > **Duomenų bazė**.

![Duomenų bazės atkūrimas](./media/5RestoreDatabase.png)

9. Pasirinkite **Šaltinio įrenginys** ir eikite į failą, kurį išskleidėte iš nukopijuoto suglaudinto failo.

![Šaltinio įrenginiai](./media/6SourceDevice.png)

10. Pasirinkite **Parinktys**, tada pasirinkite **Perrašyti esamą duomenų bazę** ir **Uždaryti esamus ryšius su paskirties duomenų baze**. 
11. Pasirinkite **Gerai**.

![Parametrų atkūrimas](./media/7RestoreSetting.png)

Gausite patvirtinimą, kad AXDB atkūrimas atliktas sėkmingai. Gavę šį patvirtinimą galite uždaryti „SQL Services Management Studio“.

12. Grįžkite atgal į **Informacinės interneto paslaugos** > **Programų telkiniai** > **AOSService** ir paleiskite AOSService.
13. Eikite į **Tarnybos** ir paleiskite dvi tarnybas, kurias buvote sustabdę anksčiau.

14. Šioje VM raskite įrankį AdminUserProvisioning. Ieškokite dalyje K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Vykdykite .ext failą naudodami savo vartotojo adresą, nurodytą lauke **El. pašto adresas**. 
16. Pasirinkite **Pateikti**.

![Administratoriaus vartotojo parengimas](./media/8AdminUserProvisioning.png)

Tai užtruks keletą minučių. Turėtumėte gauti patvirtinimo pranešimą, kad administratoriaus vartotojas sėkmingai atnaujintas.

17. Galiausiai paleiskite komandinę eilutę kaip administratorius ir atlikite iisreset

![IIS nustatymas iš naujo](./media/9IISReset.png)

18. Uždarykite nuotolinio darbalaukio seansą ir naudokite LCS puslapį **Išsami aplinkos informacija**, kad prisijungtumėte prie aplinkos ir įsitikintumėte, kad ji veikia taip, kaip tikimasi.

![Finance and Operations](./media/10FinanceAndOperations.png)
