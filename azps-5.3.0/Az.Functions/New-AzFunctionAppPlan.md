---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98523626"
---
# <span data-ttu-id="a6608-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="a6608-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="a6608-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6608-102">SYNOPSIS</span></span>
<span data-ttu-id="a6608-103">Skapar ett Service abonnemang för en funktion.</span><span class="sxs-lookup"><span data-stu-id="a6608-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="a6608-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6608-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6608-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6608-105">DESCRIPTION</span></span>
<span data-ttu-id="a6608-106">Skapar ett Service abonnemang för en funktion.</span><span class="sxs-lookup"><span data-stu-id="a6608-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="a6608-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6608-107">EXAMPLES</span></span>

### <span data-ttu-id="a6608-108">Exempel 1: skapa en Windows Premium-app-plan i West Europe med burst-kapacitet på upp till 10 förekomster.</span><span class="sxs-lookup"><span data-stu-id="a6608-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="a6608-109">Det här kommandot skapar en Windows Premium-app-plan i West Europe med burst-kapacitet på upp till 10 förekomster.</span><span class="sxs-lookup"><span data-stu-id="a6608-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="a6608-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6608-110">PARAMETERS</span></span>

### <span data-ttu-id="a6608-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6608-111">-AsJob</span></span>
<span data-ttu-id="a6608-112">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="a6608-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="a6608-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6608-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="a6608-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="a6608-114">-Location</span></span>
<span data-ttu-id="a6608-115">Platsen för förbruknings planen.</span><span class="sxs-lookup"><span data-stu-id="a6608-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="a6608-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="a6608-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="a6608-117">Maximalt antal arbetare för App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6608-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6608-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="a6608-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="a6608-119">Det minsta antalet arbetare för App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6608-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6608-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a6608-120">-Name</span></span>
<span data-ttu-id="a6608-121">Namn på App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6608-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="a6608-122">-Nowait</span><span class="sxs-lookup"><span data-stu-id="a6608-122">-NoWait</span></span>
<span data-ttu-id="a6608-123">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="a6608-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="a6608-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6608-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6608-125">Namnet på den resurs grupp som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="a6608-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="a6608-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="a6608-126">-Sku</span></span>
<span data-ttu-id="a6608-127">Abonnemangs-SKU.</span><span class="sxs-lookup"><span data-stu-id="a6608-127">The plan sku.</span></span>
<span data-ttu-id="a6608-128">Giltiga indata är: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="a6608-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="a6608-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6608-129">-SubscriptionId</span></span>
<span data-ttu-id="a6608-130">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="a6608-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="a6608-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a6608-131">-Tag</span></span>
<span data-ttu-id="a6608-132">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="a6608-132">Resource tags.</span></span>

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

### <span data-ttu-id="a6608-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="a6608-133">-WorkerType</span></span>
<span data-ttu-id="a6608-134">Arbets typ för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="a6608-134">The worker type for the plan.</span></span>
<span data-ttu-id="a6608-135">Giltiga indata är: Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="a6608-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="a6608-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a6608-136">-Confirm</span></span>
<span data-ttu-id="a6608-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6608-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6608-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6608-138">-WhatIf</span></span>
<span data-ttu-id="a6608-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a6608-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6608-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a6608-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6608-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6608-141">CommonParameters</span></span>
<span data-ttu-id="a6608-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6608-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6608-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6608-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6608-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6608-144">INPUTS</span></span>

## <span data-ttu-id="a6608-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6608-145">OUTPUTS</span></span>

### <span data-ttu-id="a6608-146">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a6608-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="a6608-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6608-147">NOTES</span></span>

<span data-ttu-id="a6608-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a6608-148">ALIASES</span></span>

## <span data-ttu-id="a6608-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6608-149">RELATED LINKS</span></span>

