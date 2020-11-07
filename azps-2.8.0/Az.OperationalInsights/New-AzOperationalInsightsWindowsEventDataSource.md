---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 89aed8cb651fc5e11f6314df0ec74f3b4f9aa29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919614"
---
# <span data-ttu-id="c6ace-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="c6ace-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="c6ace-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6ace-102">SYNOPSIS</span></span>
<span data-ttu-id="c6ace-103">Samlar in händelse loggar från datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="c6ace-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="c6ace-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6ace-104">SYNTAX</span></span>

### <span data-ttu-id="c6ace-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="c6ace-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6ace-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c6ace-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6ace-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6ace-107">DESCRIPTION</span></span>
<span data-ttu-id="c6ace-108">Cmdleten **New-AzOperationalInsightsWindowsEventDataSource** lägger till en data källa som samlar Windows händelse loggar från anslutna datorer som kör operativ systemet Windows i Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="c6ace-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="c6ace-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6ace-109">EXAMPLES</span></span>

### <span data-ttu-id="c6ace-110">Exempel 1: skapa en data källa för systemet Windows-händelse</span><span class="sxs-lookup"><span data-stu-id="c6ace-110">Example 1: Create system Windows event data source</span></span>
```
$EventLogNames       = @()
$EventLogNames      += 'Directory Service'
$EventLogNames      += 'Microsoft-Windows-EventCollector/Operational'
$EventLogNames      += 'System'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($EventLogName in $EventLogNames) {
    $Count++
    $null = New-AzOperationalInsightsWindowsEventDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Windows-event-$($Count)" `
    -EventLogName $EventLogName `
    -CollectErrors `
    -CollectWarnings `
    -CollectInformation
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'WindowsEvent'
```

## <span data-ttu-id="c6ace-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6ace-111">PARAMETERS</span></span>

### <span data-ttu-id="c6ace-112">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="c6ace-112">-CollectErrors</span></span>
<span data-ttu-id="c6ace-113">Anger att drift insikter samlar in fel meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c6ace-113">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="c6ace-114">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="c6ace-114">-CollectInformation</span></span>
<span data-ttu-id="c6ace-115">Anger att operativa insikter samlar in informations meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c6ace-115">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="c6ace-116">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="c6ace-116">-CollectWarnings</span></span>
<span data-ttu-id="c6ace-117">Anger att drift insikter samlar in varnings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="c6ace-117">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="c6ace-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6ace-118">-DefaultProfile</span></span>
<span data-ttu-id="c6ace-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c6ace-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6ace-120">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="c6ace-120">-EventLogName</span></span>
<span data-ttu-id="c6ace-121">Anger namnet på händelse loggen.</span><span class="sxs-lookup"><span data-stu-id="c6ace-121">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="c6ace-122">-Force</span><span class="sxs-lookup"><span data-stu-id="c6ace-122">-Force</span></span>
<span data-ttu-id="c6ace-123">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c6ace-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c6ace-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6ace-124">-Name</span></span>
<span data-ttu-id="c6ace-125">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="c6ace-125">Specifies a name for the data source.</span></span> <span data-ttu-id="c6ace-126">Namnet visas inte i Azure-portalen och en sträng kan användas så länge det är unikt.</span><span class="sxs-lookup"><span data-stu-id="c6ace-126">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="c6ace-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6ace-127">-ResourceGroupName</span></span>
<span data-ttu-id="c6ace-128">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="c6ace-128">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="c6ace-129">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="c6ace-129">-Workspace</span></span>
<span data-ttu-id="c6ace-130">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="c6ace-130">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c6ace-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c6ace-131">-WorkspaceName</span></span>
<span data-ttu-id="c6ace-132">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="c6ace-132">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c6ace-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c6ace-133">-Confirm</span></span>
<span data-ttu-id="c6ace-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c6ace-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6ace-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6ace-135">-WhatIf</span></span>
<span data-ttu-id="c6ace-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c6ace-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6ace-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c6ace-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6ace-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6ace-138">CommonParameters</span></span>
<span data-ttu-id="c6ace-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6ace-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6ace-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6ace-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6ace-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6ace-141">INPUTS</span></span>

### <span data-ttu-id="c6ace-142">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c6ace-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c6ace-143">System. String</span><span class="sxs-lookup"><span data-stu-id="c6ace-143">System.String</span></span>

## <span data-ttu-id="c6ace-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6ace-144">OUTPUTS</span></span>

### <span data-ttu-id="c6ace-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c6ace-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c6ace-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6ace-146">NOTES</span></span>

## <span data-ttu-id="c6ace-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6ace-147">RELATED LINKS</span></span>
