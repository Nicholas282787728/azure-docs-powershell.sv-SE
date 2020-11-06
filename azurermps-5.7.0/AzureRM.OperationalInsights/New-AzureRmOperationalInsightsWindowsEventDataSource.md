---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 36B3B1AC-6E7F-4607-A024-91583D952B62
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightswindowseventdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWindowsEventDataSource.md
ms.openlocfilehash: cebbcb0526c35fb803de783604db291612694baf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575578"
---
# <span data-ttu-id="aeb72-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="aeb72-101">New-AzureRmOperationalInsightsWindowsEventDataSource</span></span>

## <span data-ttu-id="aeb72-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="aeb72-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb72-103">Samlar in händelse loggar från datorer som kör operativ systemet Windows.</span><span class="sxs-lookup"><span data-stu-id="aeb72-103">Collects event logs from computers that run the Windows operating system.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aeb72-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="aeb72-104">SYNTAX</span></span>

### <span data-ttu-id="aeb72-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="aeb72-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aeb72-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="aeb72-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsWindowsEventDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-EventLogName] <String> [-CollectErrors] [-CollectWarnings] [-CollectInformation] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeb72-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="aeb72-107">DESCRIPTION</span></span>
<span data-ttu-id="aeb72-108">Cmdleten **New-AzureRmOperationalInsightsWindowsEventDataSource** lägger till en data källa som samlar Windows händelse loggar från anslutna datorer som kör operativ systemet Windows i Azure Operational Insights.</span><span class="sxs-lookup"><span data-stu-id="aeb72-108">The **New-AzureRmOperationalInsightsWindowsEventDataSource** cmdlet adds a data source that collects Windows event logs from connected computers that run the Windows operating system in Azure Operational Insights.</span></span>

## <span data-ttu-id="aeb72-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="aeb72-109">EXAMPLES</span></span>

## <span data-ttu-id="aeb72-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="aeb72-110">PARAMETERS</span></span>

### <span data-ttu-id="aeb72-111">-CollectErrors</span><span class="sxs-lookup"><span data-stu-id="aeb72-111">-CollectErrors</span></span>
<span data-ttu-id="aeb72-112">Anger att drift insikter samlar in fel meddelanden.</span><span class="sxs-lookup"><span data-stu-id="aeb72-112">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="aeb72-113">-CollectInformation</span><span class="sxs-lookup"><span data-stu-id="aeb72-113">-CollectInformation</span></span>
<span data-ttu-id="aeb72-114">Anger att operativa insikter samlar in informations meddelanden.</span><span class="sxs-lookup"><span data-stu-id="aeb72-114">Indicates that Operational Insights collects information messages.</span></span>

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

### <span data-ttu-id="aeb72-115">-CollectWarnings</span><span class="sxs-lookup"><span data-stu-id="aeb72-115">-CollectWarnings</span></span>
<span data-ttu-id="aeb72-116">Anger att drift insikter samlar in varnings meddelanden.</span><span class="sxs-lookup"><span data-stu-id="aeb72-116">Indicates that Operational Insights collects warning messages.</span></span>

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

### <span data-ttu-id="aeb72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb72-117">-DefaultProfile</span></span>
<span data-ttu-id="aeb72-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="aeb72-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeb72-119">-EventLogName</span><span class="sxs-lookup"><span data-stu-id="aeb72-119">-EventLogName</span></span>
<span data-ttu-id="aeb72-120">Anger namnet på händelse loggen.</span><span class="sxs-lookup"><span data-stu-id="aeb72-120">Specifies the name of the event log.</span></span>

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

### <span data-ttu-id="aeb72-121">-Force</span><span class="sxs-lookup"><span data-stu-id="aeb72-121">-Force</span></span>
<span data-ttu-id="aeb72-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="aeb72-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aeb72-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="aeb72-123">-Name</span></span>
<span data-ttu-id="aeb72-124">Anger ett namn för data källan.</span><span class="sxs-lookup"><span data-stu-id="aeb72-124">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="aeb72-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeb72-125">-ResourceGroupName</span></span>
<span data-ttu-id="aeb72-126">Anger namnet på en resurs grupp som innehåller datorer.</span><span class="sxs-lookup"><span data-stu-id="aeb72-126">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="aeb72-127">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="aeb72-127">-Workspace</span></span>
<span data-ttu-id="aeb72-128">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="aeb72-128">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="aeb72-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="aeb72-129">-WorkspaceName</span></span>
<span data-ttu-id="aeb72-130">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="aeb72-130">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="aeb72-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="aeb72-131">-Confirm</span></span>
<span data-ttu-id="aeb72-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="aeb72-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeb72-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeb72-133">-WhatIf</span></span>
<span data-ttu-id="aeb72-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="aeb72-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeb72-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="aeb72-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeb72-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb72-136">CommonParameters</span></span>
<span data-ttu-id="aeb72-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeb72-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb72-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeb72-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb72-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="aeb72-139">INPUTS</span></span>

### <span data-ttu-id="aeb72-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="aeb72-140">PSWorkspace</span></span>
<span data-ttu-id="aeb72-141">Parametern ' Workspace ' godkänner värdet av typen ' PSWorkspace ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="aeb72-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="aeb72-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="aeb72-142">OUTPUTS</span></span>

### <span data-ttu-id="aeb72-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="aeb72-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="aeb72-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="aeb72-144">NOTES</span></span>

## <span data-ttu-id="aeb72-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="aeb72-145">RELATED LINKS</span></span>

