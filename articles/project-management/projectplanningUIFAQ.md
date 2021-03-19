---
title: Trikčių diagnostika dirbant su užduoties tinkleliu
description: Šioje temoje pateikta trikčių diagnostikos informacija, būtina dirbant su užduočių tinkleliu.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: dedd989cc7c959d9ea97a0abfb13f8f1b2150a56
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286573"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="1e0f4-103">Trikčių diagnostika dirbant su užduoties tinkleliu</span><span class="sxs-lookup"><span data-stu-id="1e0f4-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="1e0f4-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="1e0f4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1e0f4-105">Šioje temoje aprašoma, kaip išspręsti problemas, su kuriomis galite susidurti dirbdami su išlaidų valdymu.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="1e0f4-106">Slapukų įjungimas</span><span class="sxs-lookup"><span data-stu-id="1e0f4-106">Enable cookies</span></span>

<span data-ttu-id="1e0f4-107">Programoje „Project Operations“ reikia įgalinti trečiųjų šalių slapukus, kad būtų galima sukurti darbo paskirstymo struktūrą.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="1e0f4-108">Kai trečiųjų šalių slapukai nėra įgalinti, užuot matę užduotis, matysite tuščią puslapį, kai puslapyje **Projektas** pasirinksite skirtuką **Užduotys**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Tuščias skirtukas, kai neįgalinti trečiųjų šalių slapukai](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="1e0f4-110">Alternatyvus sprendimas</span><span class="sxs-lookup"><span data-stu-id="1e0f4-110">Workaround</span></span>
<span data-ttu-id="1e0f4-111">Toliau nurodytose procedūrose, skirtose „Microsoft Edge“ arba „Google Chrome“ naršyklėms, apibrėžiama, kaip atnaujinti jūsų naršyklės parametrą ir įgalinti trečiosios šalies slapukus.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="1e0f4-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1e0f4-112">Microsoft Edge</span></span>

1. <span data-ttu-id="1e0f4-113">Atidarykite „Edge“ naršyklę.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="1e0f4-114">Viršutiniame dešiniajame kampe pasirinkite **elipsę** (...), o tada pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="1e0f4-115">Dalyje **Slapukai ir svetainės teisės** pasirinkite **Slapukai ir svetainės duomenys**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="1e0f4-116">Išjunkite parinktį **Blokuoti trečiųjų šalių slapukus**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="1e0f4-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="1e0f4-117">Google Chrome</span></span>

1. <span data-ttu-id="1e0f4-118">Atidarykite „Chrome“ naršyklę.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="1e0f4-119">Viršutiniame dešiniajame kampe pasirinkite tris vertikalius taškus ir pasirinkte **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="1e0f4-120">Dalyje **Privatumas ir sauga** pasirinkite **Slapukai ir kiti svetainės duomenys**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="1e0f4-121">Pasirinkite **Leisti visus slapukus**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e0f4-122">Jei blokuosite trečiųjų šalių slapukus, visi kitų svetainių slapukai ir svetainės duomenys bus blokuojami, net jei svetainė bus leidžiama jūsų išimčių sąraše.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="1e0f4-123">PEX galinis punktas</span><span class="sxs-lookup"><span data-stu-id="1e0f4-123">PEX Endpoint</span></span>

<span data-ttu-id="1e0f4-124">Programoje „Project Operations“ reikia, kad projekto parametras nurodytų PEX galinį punktą.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="1e0f4-125">Šis galinis punktas būtinas tam, kad galėtų palaikyti ryšį su paslauga, naudojama darbo paskirstymo struktūrai generuoti.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="1e0f4-126">Jei parametras neįjungtas, matysite klaidą „Projekto parametras negalioja“.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="1e0f4-127">Alternatyvus sprendimas</span><span class="sxs-lookup"><span data-stu-id="1e0f4-127">Workaround</span></span>
 ![Projekto parametro PEX galinio punkto laukas](media/projectparameter.png)

1. <span data-ttu-id="1e0f4-129">Įtraukite lauką **PEX galinis punktas** į puslapį **Projekto parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="1e0f4-130">Atnaujinkite lauką naudodami šią reikšmę: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="1e0f4-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`</span></span>
3. <span data-ttu-id="1e0f4-131">Pašalinkite lauką iš puslapio **Projekto parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="1e0f4-132">Žiniatinklio projekto teisės</span><span class="sxs-lookup"><span data-stu-id="1e0f4-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="1e0f4-133">„Project Operations“ remiasi išorine planavimo paslauga.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="1e0f4-134">Paslauga reikalauja, kad vartotojas turėtų kelis vaidmenis, priskirtus skaityti ir rašyti objektuose, susijusiuose su darbo paskirstymo struktūra.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="1e0f4-135">Šie objektai apima projekto užduotis, išteklių priskyrimus ir užduočių priklausomybes.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="1e0f4-136">Jei vartotojas negali sugeneruoti darbo paskirstymo struktūros skirtuke **Užduotys**, tai tikriausiai yra dėl to, kad „Project Operations“ projektas nebuvo įgalintas.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="1e0f4-137">Vartotojas gali matyti saugos vaidmens klaidą arba klaidą, susijusią su prieigos atsisakymu.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="1e0f4-138">Alternatyvus sprendimas</span><span class="sxs-lookup"><span data-stu-id="1e0f4-138">Workaround</span></span>

1. <span data-ttu-id="1e0f4-139">Eikite į **Parametras > Sauga > Vartotojai > Programos vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Programos skaitytuvas](media/applicationuser.jpg)
   
2. <span data-ttu-id="1e0f4-141">Dukart spustelėkite programos vartotojo įrašą ir patikrinkite, ar:</span><span class="sxs-lookup"><span data-stu-id="1e0f4-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="1e0f4-142">Vartotojas turi prieigą prie projekto.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-142">The user has access to the project.</span></span> <span data-ttu-id="1e0f4-143">Šį tikrinimą paprastai užtikrina tai, kad vartotojas turi **Projekto vadovas** saugos vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="1e0f4-144">„Microsoft Project“ programos vartotojas egzistuoja ir yra teisingai sukonfigūruotas.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="1e0f4-145">Jei šis vartotojas neegzistuoja, galite sukurti naują vartotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="1e0f4-146">Pasirinkite **Nauji vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-146">Select **New Users**.</span></span> <span data-ttu-id="1e0f4-147">Pakeiskite įrašo formą į **Programos vartotojas**, o tada įtraukite **Programos ID**.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Programos vartotojo išsami informacija](media/applicationuserdetails.jpg)

4. <span data-ttu-id="1e0f4-149">Patikrinkite, ar vartotojui priskirta tinkama licencija ir ar paslauga įgalinta paslaugos plano licencijos išsamioje informacijoje.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="1e0f4-150">Patikrinkite, ar vartotojas gali atidaryti project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="1e0f4-151">Projekto parametruose patikrinkite, ar sistema rodo tinkamą projekto galinį punktą.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="1e0f4-152">Patikrinkite, ar sukurtas projekto programos vartotojas.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="1e0f4-153">Vartotojui pritaikykite šiuos saugos vaidmenis:</span><span class="sxs-lookup"><span data-stu-id="1e0f4-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="1e0f4-154">„Dataverse“ vartotojas</span><span class="sxs-lookup"><span data-stu-id="1e0f4-154">Dataverse User</span></span>
  - <span data-ttu-id="1e0f4-155">„Project Operations“ sistema</span><span class="sxs-lookup"><span data-stu-id="1e0f4-155">Project Operations System</span></span>
  - <span data-ttu-id="1e0f4-156">„Project“ sistema</span><span class="sxs-lookup"><span data-stu-id="1e0f4-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="1e0f4-157">Klaida naujinant darbo paskirstymo struktūrą</span><span class="sxs-lookup"><span data-stu-id="1e0f4-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="1e0f4-158">Darbo paskirstymo struktūroje atliekant vieną ar daugiau naujinimų, pakeitimai galiausiai nepavyks ir nebus įrašyti.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="1e0f4-159">Grafiko tinklelyje įvyksta klaida, nurodanti, kad „Naujausio pakeitimo įrašyti nepavyko“.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="1e0f4-160">Alternatyvus sprendimas</span><span class="sxs-lookup"><span data-stu-id="1e0f4-160">Workaround</span></span>

1. <span data-ttu-id="1e0f4-161">Patikrinkite, ar vartotojui priskirta tinkama licencija ir ar paslauga įgalinta paslaugos plano licencijos išsamioje informacijoje.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="1e0f4-162">Patikrinkite, ar vartotojas gali atidaryti project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="1e0f4-163">Patikrinkite, ar sistema rodo tinkamą projekto galinį punktą.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="1e0f4-164">Patikrinkite, ar programoje „Project“ sukurtas vartotojas.</span><span class="sxs-lookup"><span data-stu-id="1e0f4-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="1e0f4-165">Vartotojui pritaikykite šiuos saugos vaidmenis:</span><span class="sxs-lookup"><span data-stu-id="1e0f4-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="1e0f4-166">„Dataverse“ vartotojas arba pagrindinis vartotojas</span><span class="sxs-lookup"><span data-stu-id="1e0f4-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="1e0f4-167">„Project Operations“ sistema</span><span class="sxs-lookup"><span data-stu-id="1e0f4-167">Project Operations System</span></span>
  - <span data-ttu-id="1e0f4-168">„Project“ sistema</span><span class="sxs-lookup"><span data-stu-id="1e0f4-168">Project System</span></span>
  - <span data-ttu-id="1e0f4-169">„Project Operations“ dvigubo rašymo sistema (šis vaidmuo būtinas, jei diegiate „Project Operations“, skirtą ištekliais / nelaikomomis medžiagomis pagrįstiems scenarijams).</span><span class="sxs-lookup"><span data-stu-id="1e0f4-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]