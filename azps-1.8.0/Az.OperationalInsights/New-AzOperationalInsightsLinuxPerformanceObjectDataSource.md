---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 6372abc324601761c07ec4c69d52db188172ba0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747572"
---
# <span data-ttu-id="c0654-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="c0654-101">New-AzOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="c0654-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0654-102">SYNOPSIS</span></span>
<span data-ttu-id="c0654-103">Lägger till prestanda räknare till alla Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="c0654-103">Adds performance counters to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="c0654-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0654-104">SYNTAX</span></span>

### <span data-ttu-id="c0654-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="c0654-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0654-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c0654-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0654-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0654-107">DESCRIPTION</span></span>
<span data-ttu-id="c0654-108">Cmdleten **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** lägger till prestanda räknare som samlar in data från alla Linux-datorer på en arbets yta med Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="c0654-108">The **New-AzOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="c0654-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0654-109">EXAMPLES</span></span>

## <span data-ttu-id="c0654-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0654-110">PARAMETERS</span></span>

### <span data-ttu-id="c0654-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="c0654-111">-CounterNames</span></span>
<span data-ttu-id="c0654-112">Anger en matris med namn på räknare.</span><span class="sxs-lookup"><span data-stu-id="c0654-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0654-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0654-113">-DefaultProfile</span></span>
<span data-ttu-id="c0654-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c0654-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0654-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c0654-115">-Force</span></span>
<span data-ttu-id="c0654-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c0654-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0654-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c0654-117">-InstanceName</span></span>
<span data-ttu-id="c0654-118">Anger ett förekomst namn.</span><span class="sxs-lookup"><span data-stu-id="c0654-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="c0654-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="c0654-119">-IntervalSeconds</span></span>
<span data-ttu-id="c0654-120">Anger intervallet för samlingen.</span><span class="sxs-lookup"><span data-stu-id="c0654-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="c0654-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0654-121">-Name</span></span>
<span data-ttu-id="c0654-122">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="c0654-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="c0654-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="c0654-123">-ObjectName</span></span>
<span data-ttu-id="c0654-124">Anger namnet på ett objekt.</span><span class="sxs-lookup"><span data-stu-id="c0654-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="c0654-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0654-125">-ResourceGroupName</span></span>
<span data-ttu-id="c0654-126">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="c0654-126">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="c0654-127">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="c0654-127">-Workspace</span></span>
<span data-ttu-id="c0654-128">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="c0654-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c0654-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0654-129">-WorkspaceName</span></span>
<span data-ttu-id="c0654-130">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="c0654-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c0654-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0654-131">-Confirm</span></span>
<span data-ttu-id="c0654-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0654-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0654-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0654-133">-WhatIf</span></span>
<span data-ttu-id="c0654-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0654-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0654-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0654-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0654-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0654-136">CommonParameters</span></span>
<span data-ttu-id="c0654-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0654-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0654-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0654-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0654-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0654-139">INPUTS</span></span>

### <span data-ttu-id="c0654-140">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0654-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c0654-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c0654-141">System.String</span></span>

### <span data-ttu-id="c0654-142">System. string []</span><span class="sxs-lookup"><span data-stu-id="c0654-142">System.String[]</span></span>

### <span data-ttu-id="c0654-143">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c0654-143">System.Int32</span></span>

## <span data-ttu-id="c0654-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0654-144">OUTPUTS</span></span>

### <span data-ttu-id="c0654-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c0654-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c0654-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0654-146">NOTES</span></span>

## <span data-ttu-id="c0654-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0654-147">RELATED LINKS</span></span>

[<span data-ttu-id="c0654-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="c0654-148">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="c0654-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="c0654-149">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)


