---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: f5bc73ee6fc2f3c20b92f8780bcddec99bc46fee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325650"
---
# <span data-ttu-id="093f2-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="093f2-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="093f2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="093f2-102">SYNOPSIS</span></span>
<span data-ttu-id="093f2-103">Stoppar insamling av syslog-data från Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="093f2-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="093f2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="093f2-104">SYNTAX</span></span>

### <span data-ttu-id="093f2-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="093f2-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="093f2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="093f2-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="093f2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="093f2-107">DESCRIPTION</span></span>
<span data-ttu-id="093f2-108">Cmdleten **disable-AzOperationalInsightsLinuxSyslogCollection** stoppar samlingen syslog-data från anslutna Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="093f2-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="093f2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="093f2-109">EXAMPLES</span></span>

## <span data-ttu-id="093f2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="093f2-110">PARAMETERS</span></span>

### <span data-ttu-id="093f2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="093f2-111">-DefaultProfile</span></span>
<span data-ttu-id="093f2-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="093f2-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="093f2-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="093f2-113">-ResourceGroupName</span></span>
<span data-ttu-id="093f2-114">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="093f2-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="093f2-115">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="093f2-115">-Workspace</span></span>
<span data-ttu-id="093f2-116">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="093f2-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="093f2-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="093f2-117">-WorkspaceName</span></span>
<span data-ttu-id="093f2-118">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="093f2-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="093f2-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="093f2-119">-Confirm</span></span>
<span data-ttu-id="093f2-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="093f2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="093f2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="093f2-121">-WhatIf</span></span>
<span data-ttu-id="093f2-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="093f2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="093f2-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="093f2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="093f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="093f2-124">CommonParameters</span></span>
<span data-ttu-id="093f2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="093f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="093f2-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="093f2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="093f2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="093f2-127">INPUTS</span></span>

### <span data-ttu-id="093f2-128">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="093f2-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="093f2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="093f2-129">System.String</span></span>

## <span data-ttu-id="093f2-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="093f2-130">OUTPUTS</span></span>

### <span data-ttu-id="093f2-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="093f2-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="093f2-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="093f2-132">NOTES</span></span>
* <span data-ttu-id="093f2-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="093f2-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="093f2-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="093f2-134">RELATED LINKS</span></span>

[<span data-ttu-id="093f2-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="093f2-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="093f2-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="093f2-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)

