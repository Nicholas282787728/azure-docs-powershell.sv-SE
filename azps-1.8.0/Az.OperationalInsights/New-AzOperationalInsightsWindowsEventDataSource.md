---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: 4230eadc005ca53600feb2e6bc7ee2e001d7b209
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93747568"
---
# <span data-ttu-id="bf05d-101">New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="bf05d-101">New-AzOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="bf05d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bf05d-102">SYNOPSIS</span></span>
<span data-ttu-id="bf05d-103">Samlar in händelse loggar från datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="bf05d-103">Collects event logs from computers that run the Windows operating system.</span></span>

## <span data-ttu-id="bf05d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bf05d-104">SYNTAX</span></span>

### <span data-ttu-id="bf05d-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="bf05d-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf05d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bf05d-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf05d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bf05d-107">DESCRIPTION</span></span>
<span data-ttu-id="bf05d-108">Cmdleten **New-AzOperationalInsightsWindowsEventDataSource** lägger till en data källa som samlar Windows händelse loggar från anslutna datorer som kör operativ systemet Windows i Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="bf05d-108">The **New-AzOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="bf05d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bf05d-109">EXAMPLES</span></span>

## <span data-ttu-id="bf05d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bf05d-110">PARAMETERS</span></span>

### <span data-ttu-id="bf05d-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="bf05d-111">-CollectErrors</span></span>
<span data-ttu-id="bf05d-112">Anger att drift insikter samlar in fel meddelanden.</span><span class="sxs-lookup"><span data-stu-id="bf05d-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="bf05d-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="bf05d-113">-CollectInformation</span></span>
<span data-ttu-id="bf05d-114">Anger att operativa insikter samlar in informations meddelanden.</span><span class="sxs-lookup"><span data-stu-id="bf05d-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="bf05d-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="bf05d-115">-CollectWarnings</span></span>
<span data-ttu-id="bf05d-116">Anger att drift insikter samlar in varnings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="bf05d-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="bf05d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf05d-117">-DefaultProfile</span></span>
<span data-ttu-id="bf05d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="bf05d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf05d-119">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="bf05d-119">-EventLogName</span></span>
<span data-ttu-id="bf05d-120">Anger namnet på händelse loggen.</span><span class="sxs-lookup"><span data-stu-id="bf05d-120">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="bf05d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bf05d-121">-Force</span></span>
<span data-ttu-id="bf05d-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bf05d-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf05d-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="bf05d-123">-Name</span></span>
<span data-ttu-id="bf05d-124">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="bf05d-124">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="bf05d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf05d-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf05d-126">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="bf05d-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="bf05d-127">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="bf05d-127">-Workspace</span></span>
<span data-ttu-id="bf05d-128">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="bf05d-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bf05d-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bf05d-129">-WorkspaceName</span></span>
<span data-ttu-id="bf05d-130">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="bf05d-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="bf05d-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bf05d-131">-Confirm</span></span>
<span data-ttu-id="bf05d-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bf05d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf05d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf05d-133">-WhatIf</span></span>
<span data-ttu-id="bf05d-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bf05d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf05d-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bf05d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf05d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf05d-136">CommonParameters</span></span>
<span data-ttu-id="bf05d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf05d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf05d-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf05d-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf05d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bf05d-139">INPUTS</span></span>

### <span data-ttu-id="bf05d-140">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bf05d-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="bf05d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bf05d-141">System.String</span></span>

## <span data-ttu-id="bf05d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bf05d-142">OUTPUTS</span></span>

### <span data-ttu-id="bf05d-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="bf05d-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="bf05d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bf05d-144">NOTES</span></span>

## <span data-ttu-id="bf05d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bf05d-145">RELATED LINKS</span></span>
