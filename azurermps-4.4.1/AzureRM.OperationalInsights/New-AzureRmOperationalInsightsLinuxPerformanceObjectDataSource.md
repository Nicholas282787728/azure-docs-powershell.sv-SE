---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 1e9114b9f6b62f6900c975b39e5f8c67b4d9051a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575923"
---
# <span data-ttu-id="71b5d-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="71b5d-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="71b5d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="71b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="71b5d-103">Lägger till prestanda räknare till alla Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="71b5d-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71b5d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="71b5d-104">SYNTAX</span></span>

### <span data-ttu-id="71b5d-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="71b5d-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71b5d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="71b5d-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71b5d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="71b5d-107">DESCRIPTION</span></span>
<span data-ttu-id="71b5d-108">Cmdleten **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** lägger till prestanda räknare som samlar in data från alla Linux-datorer på en arbets yta med Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="71b5d-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="71b5d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="71b5d-109">EXAMPLES</span></span>

## <span data-ttu-id="71b5d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="71b5d-110">PARAMETERS</span></span>

### <span data-ttu-id="71b5d-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="71b5d-111">-CounterNames</span></span>
<span data-ttu-id="71b5d-112">Anger en matris med namn på räknare.</span><span class="sxs-lookup"><span data-stu-id="71b5d-112">Specifies an array of names of counters.</span></span>

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

### <span data-ttu-id="71b5d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="71b5d-113">-Force</span></span>
<span data-ttu-id="71b5d-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="71b5d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71b5d-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="71b5d-115">-InstanceName</span></span>
<span data-ttu-id="71b5d-116">Anger ett förekomst namn.</span><span class="sxs-lookup"><span data-stu-id="71b5d-116">Specifies an instance name.</span></span>

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

### <span data-ttu-id="71b5d-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="71b5d-117">-IntervalSeconds</span></span>
<span data-ttu-id="71b5d-118">Anger intervallet för samlingen.</span><span class="sxs-lookup"><span data-stu-id="71b5d-118">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="71b5d-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="71b5d-119">-Name</span></span>
<span data-ttu-id="71b5d-120">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="71b5d-120">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="71b5d-121">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="71b5d-121">-ObjectName</span></span>
<span data-ttu-id="71b5d-122">Anger namnet på ett objekt.</span><span class="sxs-lookup"><span data-stu-id="71b5d-122">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="71b5d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b5d-123">-ResourceGroupName</span></span>
<span data-ttu-id="71b5d-124">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="71b5d-124">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="71b5d-125">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="71b5d-125">-Workspace</span></span>
<span data-ttu-id="71b5d-126">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="71b5d-126">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="71b5d-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="71b5d-127">-WorkspaceName</span></span>
<span data-ttu-id="71b5d-128">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="71b5d-128">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="71b5d-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="71b5d-129">-Confirm</span></span>
<span data-ttu-id="71b5d-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="71b5d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71b5d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71b5d-131">-WhatIf</span></span>
<span data-ttu-id="71b5d-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="71b5d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71b5d-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="71b5d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71b5d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b5d-134">-DefaultProfile</span></span>
<span data-ttu-id="71b5d-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="71b5d-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71b5d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b5d-136">CommonParameters</span></span>
<span data-ttu-id="71b5d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b5d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b5d-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b5d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b5d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="71b5d-139">INPUTS</span></span>

### <span data-ttu-id="71b5d-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="71b5d-140">PSWorkspace</span></span>
<span data-ttu-id="71b5d-141">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="71b5d-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="71b5d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="71b5d-142">OUTPUTS</span></span>

### <span data-ttu-id="71b5d-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="71b5d-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="71b5d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="71b5d-144">NOTES</span></span>

## <span data-ttu-id="71b5d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="71b5d-145">RELATED LINKS</span></span>

[<span data-ttu-id="71b5d-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="71b5d-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="71b5d-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="71b5d-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


