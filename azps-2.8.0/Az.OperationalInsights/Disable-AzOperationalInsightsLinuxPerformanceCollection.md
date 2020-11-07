---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 0a39dae7ebdc6cc2c1fcc1b77ceb9b5d8e330d66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919640"
---
# <span data-ttu-id="94f60-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="94f60-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="94f60-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94f60-102">SYNOPSIS</span></span>
<span data-ttu-id="94f60-103">Stoppar insamling av prestanda räknare från Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="94f60-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="94f60-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94f60-104">SYNTAX</span></span>

### <span data-ttu-id="94f60-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="94f60-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f60-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="94f60-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f60-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94f60-107">DESCRIPTION</span></span>
<span data-ttu-id="94f60-108">Cmdleten **disable-AzOperationalInsightsLinuxPerformanceCollection** stoppar samlingen av prestanda räknare från anslutna Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="94f60-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="94f60-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94f60-109">EXAMPLES</span></span>

## <span data-ttu-id="94f60-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94f60-110">PARAMETERS</span></span>

### <span data-ttu-id="94f60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f60-111">-DefaultProfile</span></span>
<span data-ttu-id="94f60-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="94f60-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94f60-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f60-113">-ResourceGroupName</span></span>
<span data-ttu-id="94f60-114">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="94f60-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="94f60-115">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="94f60-115">-Workspace</span></span>
<span data-ttu-id="94f60-116">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="94f60-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="94f60-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="94f60-117">-WorkspaceName</span></span>
<span data-ttu-id="94f60-118">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="94f60-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="94f60-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="94f60-119">-Confirm</span></span>
<span data-ttu-id="94f60-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="94f60-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f60-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f60-121">-WhatIf</span></span>
<span data-ttu-id="94f60-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="94f60-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f60-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="94f60-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f60-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f60-124">CommonParameters</span></span>
<span data-ttu-id="94f60-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f60-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f60-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f60-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f60-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94f60-127">INPUTS</span></span>

### <span data-ttu-id="94f60-128">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="94f60-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="94f60-129">System. String</span><span class="sxs-lookup"><span data-stu-id="94f60-129">System.String</span></span>

## <span data-ttu-id="94f60-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94f60-130">OUTPUTS</span></span>

### <span data-ttu-id="94f60-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="94f60-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="94f60-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94f60-132">NOTES</span></span>
* <span data-ttu-id="94f60-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="94f60-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="94f60-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94f60-134">RELATED LINKS</span></span>

[<span data-ttu-id="94f60-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="94f60-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="94f60-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="94f60-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


