---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 92fbc7e67bb81422e021a23810f3045b5cf32cba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925533"
---
# <span data-ttu-id="2b9c7-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="2b9c7-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="2b9c7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2b9c7-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9c7-103">Stoppar insamling av prestanda räknare från Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="2b9c7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2b9c7-104">SYNTAX</span></span>

### <span data-ttu-id="2b9c7-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="2b9c7-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b9c7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2b9c7-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b9c7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2b9c7-107">DESCRIPTION</span></span>
<span data-ttu-id="2b9c7-108">Cmdleten **disable-AzOperationalInsightsLinuxPerformanceCollection** stoppar samlingen av prestanda räknare från anslutna Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="2b9c7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2b9c7-109">EXAMPLES</span></span>

## <span data-ttu-id="2b9c7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2b9c7-110">PARAMETERS</span></span>

### <span data-ttu-id="2b9c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9c7-111">-DefaultProfile</span></span>
<span data-ttu-id="2b9c7-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2b9c7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b9c7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b9c7-113">-ResourceGroupName</span></span>
<span data-ttu-id="2b9c7-114">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="2b9c7-115">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="2b9c7-115">-Workspace</span></span>
<span data-ttu-id="2b9c7-116">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2b9c7-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2b9c7-117">-WorkspaceName</span></span>
<span data-ttu-id="2b9c7-118">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2b9c7-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2b9c7-119">-Confirm</span></span>
<span data-ttu-id="2b9c7-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9c7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9c7-121">-WhatIf</span></span>
<span data-ttu-id="2b9c7-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b9c7-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9c7-124">CommonParameters</span></span>
<span data-ttu-id="2b9c7-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b9c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9c7-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b9c7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9c7-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2b9c7-127">INPUTS</span></span>

### <span data-ttu-id="2b9c7-128">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b9c7-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2b9c7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2b9c7-129">System.String</span></span>

## <span data-ttu-id="2b9c7-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2b9c7-130">OUTPUTS</span></span>

### <span data-ttu-id="2b9c7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2b9c7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2b9c7-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2b9c7-132">NOTES</span></span>
* <span data-ttu-id="2b9c7-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="2b9c7-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="2b9c7-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2b9c7-134">RELATED LINKS</span></span>

[<span data-ttu-id="2b9c7-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="2b9c7-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="2b9c7-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="2b9c7-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)

