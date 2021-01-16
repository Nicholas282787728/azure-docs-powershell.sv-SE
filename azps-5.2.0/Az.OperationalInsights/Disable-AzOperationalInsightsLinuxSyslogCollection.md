---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 4A91EEDA-D8F0-4109-A32E-B83694952C06
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: f5bc73ee6fc2f3c20b92f8780bcddec99bc46fee
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404856"
---
# <span data-ttu-id="c585a-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="c585a-101">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="c585a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c585a-102">SYNOPSIS</span></span>
<span data-ttu-id="c585a-103">Stoppar insamling av syslog-data från Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="c585a-103">Stops collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="c585a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c585a-104">SYNTAX</span></span>

### <span data-ttu-id="c585a-105">ByWorkspaceName (standard)</span><span class="sxs-lookup"><span data-stu-id="c585a-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c585a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c585a-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c585a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c585a-107">DESCRIPTION</span></span>
<span data-ttu-id="c585a-108">Cmdleten **disable-AzOperationalInsightsLinuxSyslogCollection** stoppar samlingen syslog-data från anslutna Linux-datorer på en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="c585a-108">The **Disable-AzOperationalInsightsLinuxSyslogCollection** cmdlet stops collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="c585a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c585a-109">EXAMPLES</span></span>

## <span data-ttu-id="c585a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c585a-110">PARAMETERS</span></span>

### <span data-ttu-id="c585a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c585a-111">-DefaultProfile</span></span>
<span data-ttu-id="c585a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="c585a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c585a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c585a-113">-ResourceGroupName</span></span>
<span data-ttu-id="c585a-114">Anger namnet på en resurs grupp som innehåller Linux-datorer.</span><span class="sxs-lookup"><span data-stu-id="c585a-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="c585a-115">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="c585a-115">-Workspace</span></span>
<span data-ttu-id="c585a-116">Anger en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="c585a-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c585a-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c585a-117">-WorkspaceName</span></span>
<span data-ttu-id="c585a-118">Anger namnet på en arbets yta där denna cmdlet körs.</span><span class="sxs-lookup"><span data-stu-id="c585a-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="c585a-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c585a-119">-Confirm</span></span>
<span data-ttu-id="c585a-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c585a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c585a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c585a-121">-WhatIf</span></span>
<span data-ttu-id="c585a-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c585a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c585a-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c585a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c585a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c585a-124">CommonParameters</span></span>
<span data-ttu-id="c585a-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c585a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c585a-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c585a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c585a-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c585a-127">INPUTS</span></span>

### <span data-ttu-id="c585a-128">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c585a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="c585a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c585a-129">System.String</span></span>

## <span data-ttu-id="c585a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c585a-130">OUTPUTS</span></span>

### <span data-ttu-id="c585a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="c585a-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="c585a-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c585a-132">NOTES</span></span>
* <span data-ttu-id="c585a-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, drift, insikter</span><span class="sxs-lookup"><span data-stu-id="c585a-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="c585a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c585a-134">RELATED LINKS</span></span>

[<span data-ttu-id="c585a-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="c585a-135">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="c585a-136">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="c585a-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


