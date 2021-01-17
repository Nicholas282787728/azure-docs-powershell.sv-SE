---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398360"
---
# <span data-ttu-id="2d3ce-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="2d3ce-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="2d3ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d3ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2d3ce-103">Skapar ett Service abonnemang för en funktion.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="2d3ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d3ce-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2d3ce-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d3ce-105">DESCRIPTION</span></span>
<span data-ttu-id="2d3ce-106">Skapar ett Service abonnemang för en funktion.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="2d3ce-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d3ce-107">EXAMPLES</span></span>

### <span data-ttu-id="2d3ce-108">Exempel 1: skapa en Windows Premium-app-plan i West Europe med burst-kapacitet på upp till 10 förekomster.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="2d3ce-109">Det här kommandot skapar en Windows Premium-app-plan i West Europe med burst-kapacitet på upp till 10 förekomster.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="2d3ce-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d3ce-110">PARAMETERS</span></span>

### <span data-ttu-id="2d3ce-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d3ce-111">-AsJob</span></span>
<span data-ttu-id="2d3ce-112">Kör kommandot som ett jobb.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-112">Run the command as a job.</span></span>

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

### <span data-ttu-id="2d3ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d3ce-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="2d3ce-114">-Plats</span><span class="sxs-lookup"><span data-stu-id="2d3ce-114">-Location</span></span>
<span data-ttu-id="2d3ce-115">Platsen för förbruknings planen.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-115">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="2d3ce-116">-MaximumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="2d3ce-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="2d3ce-117">Maximalt antal arbetare för App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-117">The maximum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="2d3ce-118">-MinimumWorkerCount</span><span class="sxs-lookup"><span data-stu-id="2d3ce-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="2d3ce-119">Det minsta antalet arbetare för App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-119">The minimum number of workers for the app service plan.</span></span>

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

### <span data-ttu-id="2d3ce-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2d3ce-120">-Name</span></span>
<span data-ttu-id="2d3ce-121">Namn på App Service-abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-121">Name of the App Service plan.</span></span>

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

### <span data-ttu-id="2d3ce-122">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2d3ce-122">-NoWait</span></span>
<span data-ttu-id="2d3ce-123">Kör kommandot asynkront.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-123">Run the command asynchronously.</span></span>

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

### <span data-ttu-id="2d3ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d3ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="2d3ce-125">Namnet på den resurs grupp som resursen tillhör.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-125">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="2d3ce-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="2d3ce-126">-Sku</span></span>
<span data-ttu-id="2d3ce-127">Abonnemangs-SKU.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-127">The plan sku.</span></span>
<span data-ttu-id="2d3ce-128">Giltiga indata är: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="2d3ce-128">Valid inputs are: EP1, EP2, EP3</span></span>

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

### <span data-ttu-id="2d3ce-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d3ce-129">-SubscriptionId</span></span>
<span data-ttu-id="2d3ce-130">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-130">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="2d3ce-131">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2d3ce-131">-Tag</span></span>
<span data-ttu-id="2d3ce-132">Resource-taggar.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-132">Resource tags.</span></span>

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

### <span data-ttu-id="2d3ce-133">-WorkerType</span><span class="sxs-lookup"><span data-stu-id="2d3ce-133">-WorkerType</span></span>
<span data-ttu-id="2d3ce-134">Arbets typ för abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-134">The worker type for the plan.</span></span>
<span data-ttu-id="2d3ce-135">Giltiga indata är: Windows eller Linux.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-135">Valid inputs are: Windows or Linux.</span></span>

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

### <span data-ttu-id="2d3ce-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2d3ce-136">-Confirm</span></span>
<span data-ttu-id="2d3ce-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d3ce-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d3ce-138">-WhatIf</span></span>
<span data-ttu-id="2d3ce-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d3ce-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d3ce-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d3ce-141">CommonParameters</span></span>
<span data-ttu-id="2d3ce-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d3ce-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d3ce-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d3ce-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d3ce-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d3ce-144">INPUTS</span></span>

## <span data-ttu-id="2d3ce-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d3ce-145">OUTPUTS</span></span>

### <span data-ttu-id="2d3ce-146">Microsoft. Azure. PowerShell. cmdletar. functions. Models. Api20190801. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2d3ce-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="2d3ce-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d3ce-147">NOTES</span></span>

<span data-ttu-id="2d3ce-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2d3ce-148">ALIASES</span></span>

## <span data-ttu-id="2d3ce-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d3ce-149">RELATED LINKS</span></span>

