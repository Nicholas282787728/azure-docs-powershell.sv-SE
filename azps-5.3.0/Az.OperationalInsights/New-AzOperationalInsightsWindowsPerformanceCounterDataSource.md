---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: 23154fe78b25ab469cc1f993af879c8b1e5bdad1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521801"
---
# <span data-ttu-id="4bf1a-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="4bf1a-101">New-AzOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="4bf1a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4bf1a-102">SYNOPSIS</span></span>
<span data-ttu-id="4bf1a-103">Lägger till data källor för Windows prestanda räknare för anslutna datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="4bf1a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4bf1a-104">SYNTAX</span></span>

### <span data-ttu-id="4bf1a-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="4bf1a-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bf1a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4bf1a-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bf1a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4bf1a-107">DESCRIPTION</span></span>
<span data-ttu-id="4bf1a-108">Cmdleten **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** lägger till en data källa för Windows prestanda räknare för anslutna datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-108">The **New-AzOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="4bf1a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4bf1a-109">EXAMPLES</span></span>

## <span data-ttu-id="4bf1a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4bf1a-110">PARAMETERS</span></span>

### <span data-ttu-id="4bf1a-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="4bf1a-111">-CounterName</span></span>
<span data-ttu-id="4bf1a-112">Anger namnet på en räknare.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-112">Specifies the name of a counter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bf1a-113">-DefaultProfile</span></span>
<span data-ttu-id="4bf1a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4bf1a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4bf1a-115">-Force</span></span>
<span data-ttu-id="4bf1a-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4bf1a-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="4bf1a-117">-InstanceName</span></span>
<span data-ttu-id="4bf1a-118">Anger ett förekomst namn.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-118">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="4bf1a-119">-IntervalSeconds</span></span>
<span data-ttu-id="4bf1a-120">Anger intervallet för samlingen.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-120">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="4bf1a-121">-Name</span></span>
<span data-ttu-id="4bf1a-122">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-122">Specifies a name for the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="4bf1a-123">-ObjectName</span></span>
<span data-ttu-id="4bf1a-124">Anger namnet på ett objekt.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-124">Specifies the name of an object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bf1a-125">-ResourceGroupName</span></span>
<span data-ttu-id="4bf1a-126">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-126">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="4bf1a-127">-UseLegacyCollector</span></span>
<span data-ttu-id="4bf1a-128">Använda äldre insamlare eller standard insamlaren.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="4bf1a-129">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="4bf1a-129">-Workspace</span></span>
<span data-ttu-id="4bf1a-130">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-130">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4bf1a-131">-WorkspaceName</span></span>
<span data-ttu-id="4bf1a-132">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4bf1a-133">-Confirm</span></span>
<span data-ttu-id="4bf1a-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bf1a-135">-WhatIf</span></span>
<span data-ttu-id="4bf1a-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bf1a-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bf1a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bf1a-138">CommonParameters</span></span>
<span data-ttu-id="4bf1a-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bf1a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bf1a-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bf1a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bf1a-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4bf1a-141">INPUTS</span></span>

### <span data-ttu-id="4bf1a-142">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="4bf1a-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="4bf1a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4bf1a-143">System.String</span></span>

### <span data-ttu-id="4bf1a-144">System. Int32</span><span class="sxs-lookup"><span data-stu-id="4bf1a-144">System.Int32</span></span>

## <span data-ttu-id="4bf1a-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4bf1a-145">OUTPUTS</span></span>

### <span data-ttu-id="4bf1a-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="4bf1a-146">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="4bf1a-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4bf1a-147">NOTES</span></span>

## <span data-ttu-id="4bf1a-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4bf1a-148">RELATED LINKS</span></span>
