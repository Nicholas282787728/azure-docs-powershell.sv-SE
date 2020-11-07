---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightslinuxperformanceobjectdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: decae9e9282ad85832df676162f6bc684684f339
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93758201"
---
# <span data-ttu-id="aceb3-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="aceb3-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="aceb3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aceb3-102">SYNOPSIS</span></span>
<span data-ttu-id="aceb3-103">Lägger till prestanda räknare till alla Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="aceb3-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aceb3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aceb3-104">SYNTAX</span></span>

### <span data-ttu-id="aceb3-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="aceb3-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aceb3-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="aceb3-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aceb3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aceb3-107">DESCRIPTION</span></span>
<span data-ttu-id="aceb3-108">Cmdleten **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** lägger till prestanda räknare som samlar in data från alla Linux-datorer på en arbets yta med Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="aceb3-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="aceb3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aceb3-109">EXAMPLES</span></span>

## <span data-ttu-id="aceb3-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aceb3-110">PARAMETERS</span></span>

### <span data-ttu-id="aceb3-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="aceb3-111">-CounterNames</span></span>
<span data-ttu-id="aceb3-112">Anger en matris med namn på räknare.</span><span class="sxs-lookup"><span data-stu-id="aceb3-112">Specifies an array of names of counters.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aceb3-113">-DefaultProfile</span></span>
<span data-ttu-id="aceb3-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aceb3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aceb3-115">-Force</span></span>
<span data-ttu-id="aceb3-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="aceb3-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="aceb3-117">-InstanceName</span></span>
<span data-ttu-id="aceb3-118">Anger ett förekomst namn.</span><span class="sxs-lookup"><span data-stu-id="aceb3-118">Specifies an instance name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="aceb3-119">-IntervalSeconds</span></span>
<span data-ttu-id="aceb3-120">Anger intervallet för samlingen.</span><span class="sxs-lookup"><span data-stu-id="aceb3-120">Specifies the interval of collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="aceb3-121">-Name</span></span>
<span data-ttu-id="aceb3-122">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="aceb3-122">Specifies a name for the data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="aceb3-123">-ObjectName</span></span>
<span data-ttu-id="aceb3-124">Anger namnet på ett objekt.</span><span class="sxs-lookup"><span data-stu-id="aceb3-124">Specifies the name of an object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aceb3-125">-ResourceGroupName</span></span>
<span data-ttu-id="aceb3-126">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="aceb3-126">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-127">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="aceb3-127">-Workspace</span></span>
<span data-ttu-id="aceb3-128">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="aceb3-128">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aceb3-129">-WorkspaceName</span></span>
<span data-ttu-id="aceb3-130">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="aceb3-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aceb3-131">-Confirm</span></span>
<span data-ttu-id="aceb3-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aceb3-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aceb3-133">-WhatIf</span></span>
<span data-ttu-id="aceb3-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aceb3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aceb3-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aceb3-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aceb3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aceb3-136">CommonParameters</span></span>
<span data-ttu-id="aceb3-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aceb3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aceb3-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aceb3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aceb3-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aceb3-139">INPUTS</span></span>

### <span data-ttu-id="aceb3-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="aceb3-140">PSWorkspace</span></span>
<span data-ttu-id="aceb3-141">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="aceb3-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="aceb3-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aceb3-142">OUTPUTS</span></span>

### <span data-ttu-id="aceb3-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="aceb3-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="aceb3-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aceb3-144">NOTES</span></span>

## <span data-ttu-id="aceb3-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aceb3-145">RELATED LINKS</span></span>

[<span data-ttu-id="aceb3-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="aceb3-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="aceb3-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="aceb3-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


