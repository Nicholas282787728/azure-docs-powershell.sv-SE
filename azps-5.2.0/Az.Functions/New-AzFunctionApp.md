---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398355"
---
# <span data-ttu-id="c3e39-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="c3e39-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="c3e39-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3e39-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e39-103">Skapar ett Function-program.</span><span class="sxs-lookup"><span data-stu-id="c3e39-103">Creates a function app.</span></span>

## <span data-ttu-id="c3e39-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3e39-104">SYNTAX</span></span>

### <span data-ttu-id="c3e39-105">Förbrukning (standard)</span><span class="sxs-lookup"><span data-stu-id="c3e39-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3e39-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c3e39-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3e39-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="c3e39-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3e39-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3e39-108">DESCRIPTION</span></span>
<span data-ttu-id="c3e39-109">Skapar ett Function-program.</span><span class="sxs-lookup"><span data-stu-id="c3e39-109">Creates a function app.</span></span>

## <span data-ttu-id="c3e39-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3e39-110">EXAMPLES</span></span>

### <span data-ttu-id="c3e39-111">Exempel 1: skapa en PowerShell-funktion för användning i Central USA.</span><span class="sxs-lookup"><span data-stu-id="c3e39-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="c3e39-112">Det här kommandot skapar en PowerShell-funktion för förbrukning i Central USA.</span><span class="sxs-lookup"><span data-stu-id="c3e39-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="c3e39-113">Exempel 2: skapa ett PowerShell-Function-program som finns i en tjänste plan.</span><span class="sxs-lookup"><span data-stu-id="c3e39-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="c3e39-114">Det här kommandot skapar ett PowerShell-Function-program som finns i en tjänste plan.</span><span class="sxs-lookup"><span data-stu-id="c3e39-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="c3e39-115">Exempel 3: skapa ett funktions program med hjälp av en privat ACR-bild.</span><span class="sxs-lookup"><span data-stu-id="c3e39-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="c3e39-116">Det här kommandot skapar ett funktions program med hjälp av en privat ACR-bild.</span><span class="sxs-lookup"><span data-stu-id="c3e39-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="c3e39-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3e39-117">PARAMETERS</span></span>

### <span data-ttu-id="c3e39-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="c3e39-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="c3e39-119">Instrumentation-tangenten för App Insights för att läggas till.</span><span class="sxs-lookup"><span data-stu-id="c3e39-119">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="c3e39-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="c3e39-121">Namnet på det befintliga App Insights-projektet som ska läggas till i programmets funktion.</span><span class="sxs-lookup"><span data-stu-id="c3e39-121">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="c3e39-122">-AppSetting</span></span>
<span data-ttu-id="c3e39-123">Inställningar för programmets funktion.</span><span class="sxs-lookup"><span data-stu-id="c3e39-123">Function app settings.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3e39-124">-AsJob</span></span>
<span data-ttu-id="c3e39-125">Kör cmdleten som ett bakgrunds jobb.</span><span class="sxs-lookup"><span data-stu-id="c3e39-125">Runs the cmdlet as a background job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e39-126">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c3e39-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="c3e39-128">Inaktivera att skapa Application Insights-resursen under generering av funktions program.</span><span class="sxs-lookup"><span data-stu-id="c3e39-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="c3e39-129">Inga loggar kommer att vara tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="c3e39-129">No logs will be available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: DisableAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="c3e39-130">-DockerImageName</span></span>
<span data-ttu-id="c3e39-131">Endast Linux.</span><span class="sxs-lookup"><span data-stu-id="c3e39-131">Linux only.</span></span>
<span data-ttu-id="c3e39-132">Namn på behållar bilden från docknings registret, till exempel Publisher/Image-Name: tagg.</span><span class="sxs-lookup"><span data-stu-id="c3e39-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="c3e39-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="c3e39-134">Användar namn och lösen ord för behållar registret.</span><span class="sxs-lookup"><span data-stu-id="c3e39-134">The container registry user name and password.</span></span>
<span data-ttu-id="c3e39-135">Krävs för privata register.</span><span class="sxs-lookup"><span data-stu-id="c3e39-135">Required for private registries.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CustomDockerImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="c3e39-136">-FunctionsVersion</span></span>
<span data-ttu-id="c3e39-137">Funktions versionen.</span><span class="sxs-lookup"><span data-stu-id="c3e39-137">The Functions version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="c3e39-138">-IdentityID</span></span>
<span data-ttu-id="c3e39-139">Anger listan över användar identiteter som är kopplade till programmet funktion.</span><span class="sxs-lookup"><span data-stu-id="c3e39-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="c3e39-140">Användarens identitets referenser kommer att vara ARM-Resource-ID: n i formatet "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}"</span><span class="sxs-lookup"><span data-stu-id="c3e39-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c3e39-141">-IdentityType</span></span>
<span data-ttu-id="c3e39-142">Anger den typ av identitet som används för funktionen.</span><span class="sxs-lookup"><span data-stu-id="c3e39-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="c3e39-143">De acceptabla värdena för denna parameter är:-SystemAssigned-UserAssigned</span><span class="sxs-lookup"><span data-stu-id="c3e39-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-144">-Plats</span><span class="sxs-lookup"><span data-stu-id="c3e39-144">-Location</span></span>
<span data-ttu-id="c3e39-145">Platsen för förbruknings planen.</span><span class="sxs-lookup"><span data-stu-id="c3e39-145">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-146">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3e39-146">-Name</span></span>
<span data-ttu-id="c3e39-147">Namnet på funktionen funktion.</span><span class="sxs-lookup"><span data-stu-id="c3e39-147">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-148">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c3e39-148">-NoWait</span></span>
<span data-ttu-id="c3e39-149">Startar operationen och returnerar omedelbart innan operationen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="c3e39-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="c3e39-150">Använd en annan mekanism för att avgöra om åtgärden har slutförts.</span><span class="sxs-lookup"><span data-stu-id="c3e39-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="c3e39-151">-OSType</span></span>
<span data-ttu-id="c3e39-152">Operativ systemet som ska fungera som funktion.</span><span class="sxs-lookup"><span data-stu-id="c3e39-152">The OS to host the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3e39-153">-PassThru</span></span>
<span data-ttu-id="c3e39-154">Returnerar sant när kommandot fungerar.</span><span class="sxs-lookup"><span data-stu-id="c3e39-154">Returns true when the command succeeds.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="c3e39-155">-PlanName</span></span>
<span data-ttu-id="c3e39-156">Namnet på service planen.</span><span class="sxs-lookup"><span data-stu-id="c3e39-156">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e39-157">-ResourceGroupName</span></span>
<span data-ttu-id="c3e39-158">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c3e39-158">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="c3e39-159">-Runtime</span></span>
<span data-ttu-id="c3e39-160">Funktionen kör.</span><span class="sxs-lookup"><span data-stu-id="c3e39-160">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="c3e39-161">-RuntimeVersion</span></span>
<span data-ttu-id="c3e39-162">Funktionen kör.</span><span class="sxs-lookup"><span data-stu-id="c3e39-162">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c3e39-163">-StorageAccountName</span></span>
<span data-ttu-id="c3e39-164">Namnet på lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="c3e39-164">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3e39-165">-SubscriptionId</span></span>
<span data-ttu-id="c3e39-166">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c3e39-166">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-167">-Tagg</span><span class="sxs-lookup"><span data-stu-id="c3e39-167">-Tag</span></span>
<span data-ttu-id="c3e39-168">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="c3e39-168">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-169">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3e39-169">-Confirm</span></span>
<span data-ttu-id="c3e39-170">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3e39-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e39-171">-WhatIf</span></span>
<span data-ttu-id="c3e39-172">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3e39-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e39-173">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3e39-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3e39-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e39-174">CommonParameters</span></span>
<span data-ttu-id="c3e39-175">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e39-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e39-176">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3e39-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e39-177">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3e39-177">INPUTS</span></span>

## <span data-ttu-id="c3e39-178">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3e39-178">OUTPUTS</span></span>

### <span data-ttu-id="c3e39-179">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="c3e39-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="c3e39-180">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3e39-180">NOTES</span></span>

<span data-ttu-id="c3e39-181">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c3e39-181">ALIASES</span></span>

## <span data-ttu-id="c3e39-182">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3e39-182">RELATED LINKS</span></span>

