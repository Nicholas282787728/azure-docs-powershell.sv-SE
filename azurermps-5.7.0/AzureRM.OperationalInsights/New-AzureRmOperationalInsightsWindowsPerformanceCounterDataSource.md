---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 09CC097E-0210-4443-BCDB-5CF6C8300288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowsperformancecounterdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource.md
ms.openlocfilehash: b827c9d133ff6fc0bb9df0e1e3e25c3eea23916f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574872"
---
# <span data-ttu-id="947b5-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span><span class="sxs-lookup"><span data-stu-id="947b5-101">New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource</span></span>

## <span data-ttu-id="947b5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="947b5-102">SYNOPSIS</span></span>
<span data-ttu-id="947b5-103">Lägger till data källor för Windows prestanda räknare för anslutna datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="947b5-103">Adds Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="947b5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="947b5-104">SYNTAX</span></span>

### <span data-ttu-id="947b5-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="947b5-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterName] <String>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-UseLegacyCollector] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947b5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="947b5-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterName] <String> [-InstanceName <String>] [-IntervalSeconds <Int32>]
 [-UseLegacyCollector] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="947b5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="947b5-107">DESCRIPTION</span></span>
<span data-ttu-id="947b5-108">Cmdleten **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** lägger till en data källa för Windows prestanda räknare för anslutna datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="947b5-108">The **New-AzureRmOperationalInsightsWindowsPerformanceCounterDataSource** cmdlet adds a Windows performance counter data source for connected computers that run the Windows operating system.</span></span>

## <span data-ttu-id="947b5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="947b5-109">EXAMPLES</span></span>

## <span data-ttu-id="947b5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="947b5-110">PARAMETERS</span></span>

### <span data-ttu-id="947b5-111">-CounterName</span><span class="sxs-lookup"><span data-stu-id="947b5-111">-CounterName</span></span>
<span data-ttu-id="947b5-112">Anger namnet på en räknare.</span><span class="sxs-lookup"><span data-stu-id="947b5-112">Specifies the name of a counter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="947b5-113">-DefaultProfile</span></span>
<span data-ttu-id="947b5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="947b5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="947b5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="947b5-115">-Force</span></span>
<span data-ttu-id="947b5-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="947b5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="947b5-117">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="947b5-117">-InstanceName</span></span>
<span data-ttu-id="947b5-118">Anger ett förekomst namn.</span><span class="sxs-lookup"><span data-stu-id="947b5-118">Specifies an instance name.</span></span>

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

### <span data-ttu-id="947b5-119">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="947b5-119">-IntervalSeconds</span></span>
<span data-ttu-id="947b5-120">Anger intervallet för samlingen.</span><span class="sxs-lookup"><span data-stu-id="947b5-120">Specifies the interval of collection.</span></span>

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

### <span data-ttu-id="947b5-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="947b5-121">-Name</span></span>
<span data-ttu-id="947b5-122">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="947b5-122">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="947b5-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="947b5-123">-ObjectName</span></span>
<span data-ttu-id="947b5-124">Anger namnet på ett objekt.</span><span class="sxs-lookup"><span data-stu-id="947b5-124">Specifies the name of an object.</span></span>

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

### <span data-ttu-id="947b5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="947b5-125">-ResourceGroupName</span></span>
<span data-ttu-id="947b5-126">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="947b5-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="947b5-127">-UseLegacyCollector</span><span class="sxs-lookup"><span data-stu-id="947b5-127">-UseLegacyCollector</span></span>
<span data-ttu-id="947b5-128">Använda äldre insamlare eller standard insamlaren.</span><span class="sxs-lookup"><span data-stu-id="947b5-128">Use legacy collector or the default collector.</span></span>

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

### <span data-ttu-id="947b5-129">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="947b5-129">-Workspace</span></span>
<span data-ttu-id="947b5-130">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="947b5-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="947b5-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="947b5-131">-WorkspaceName</span></span>
<span data-ttu-id="947b5-132">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="947b5-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="947b5-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="947b5-133">-Confirm</span></span>
<span data-ttu-id="947b5-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="947b5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="947b5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="947b5-135">-WhatIf</span></span>
<span data-ttu-id="947b5-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="947b5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="947b5-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="947b5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="947b5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="947b5-138">CommonParameters</span></span>
<span data-ttu-id="947b5-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="947b5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="947b5-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="947b5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="947b5-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="947b5-141">INPUTS</span></span>

### <span data-ttu-id="947b5-142">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="947b5-142">PSWorkspace</span></span>
<span data-ttu-id="947b5-143">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="947b5-143">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="947b5-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="947b5-144">OUTPUTS</span></span>

### <span data-ttu-id="947b5-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="947b5-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="947b5-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="947b5-146">NOTES</span></span>

## <span data-ttu-id="947b5-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="947b5-147">RELATED LINKS</span></span>

