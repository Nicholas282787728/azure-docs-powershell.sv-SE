---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925546"
---
# <span data-ttu-id="2cd7d-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="2cd7d-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="2cd7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2cd7d-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd7d-103">Startar en samling av syslog-data från Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="2cd7d-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="2cd7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2cd7d-104">SYNTAX</span></span>

### <span data-ttu-id="2cd7d-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="2cd7d-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cd7d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="2cd7d-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cd7d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2cd7d-107">DESCRIPTION</span></span>
<span data-ttu-id="2cd7d-108">Cmdleten **Enable-AzOperationalInsightsLinuxSyslogCollection** startar en samling av syslog-data från anslutna Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="2cd7d-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="2cd7d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2cd7d-109">EXAMPLES</span></span>

## <span data-ttu-id="2cd7d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2cd7d-110">PARAMETERS</span></span>

### <span data-ttu-id="2cd7d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd7d-111">-DefaultProfile</span></span>
<span data-ttu-id="2cd7d-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="2cd7d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cd7d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd7d-113">-ResourceGroupName</span></span>
<span data-ttu-id="2cd7d-114">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="2cd7d-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="2cd7d-115">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="2cd7d-115">-Workspace</span></span>
<span data-ttu-id="2cd7d-116">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2cd7d-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2cd7d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2cd7d-117">-WorkspaceName</span></span>
<span data-ttu-id="2cd7d-118">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="2cd7d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2cd7d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2cd7d-119">-Confirm</span></span>
<span data-ttu-id="2cd7d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2cd7d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cd7d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cd7d-121">-WhatIf</span></span>
<span data-ttu-id="2cd7d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2cd7d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cd7d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2cd7d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cd7d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd7d-124">CommonParameters</span></span>
<span data-ttu-id="2cd7d-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cd7d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd7d-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cd7d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd7d-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2cd7d-127">INPUTS</span></span>

### <span data-ttu-id="2cd7d-128">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="2cd7d-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="2cd7d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2cd7d-129">System.String</span></span>

## <span data-ttu-id="2cd7d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2cd7d-130">OUTPUTS</span></span>

### <span data-ttu-id="2cd7d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="2cd7d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="2cd7d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2cd7d-132">NOTES</span></span>
* <span data-ttu-id="2cd7d-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="2cd7d-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="2cd7d-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2cd7d-134">RELATED LINKS</span></span>

[<span data-ttu-id="2cd7d-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="2cd7d-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="2cd7d-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="2cd7d-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)

