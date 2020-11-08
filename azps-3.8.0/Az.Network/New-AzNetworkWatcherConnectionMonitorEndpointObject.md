---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 58e26de74abb46234f6985c3973b5bbe494bd0ad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088755"
---
# <span data-ttu-id="0735f-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0735f-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="0735f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0735f-102">SYNOPSIS</span></span>
<span data-ttu-id="0735f-103">Skapar slut punkt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="0735f-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="0735f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0735f-104">SYNTAX</span></span>

### <span data-ttu-id="0735f-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0735f-105">SetByResourceId</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] -ResourceId <String>
 [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0735f-106">SetByAddress</span><span class="sxs-lookup"><span data-stu-id="0735f-106">SetByAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] [-Address <String>] [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0735f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0735f-107">DESCRIPTION</span></span>
<span data-ttu-id="0735f-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet skapar slut punkt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="0735f-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="0735f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0735f-109">EXAMPLES</span></span>

### <span data-ttu-id="0735f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0735f-110">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name "workspaceEndpoint" -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

<span data-ttu-id="0735f-111">Namn: workspaceEndpoint ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: filter: {"typ": "include", "objekt": [{"Type": "AgentAddress", "adress": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="0735f-111">Name       : workspaceEndpoint ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Filter     : { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="0735f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0735f-112">PARAMETERS</span></span>

### <span data-ttu-id="0735f-113">-Adress</span><span class="sxs-lookup"><span data-stu-id="0735f-113">-Address</span></span>
<span data-ttu-id="0735f-114">Adress för anslutnings övervakarens slut punkt (IP eller domän namn).</span><span class="sxs-lookup"><span data-stu-id="0735f-114">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0735f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0735f-115">-DefaultProfile</span></span>
<span data-ttu-id="0735f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0735f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0735f-117">-FilterItem</span><span class="sxs-lookup"><span data-stu-id="0735f-117">-FilterItem</span></span>
<span data-ttu-id="0735f-118">Lista över objekt i filtret.</span><span class="sxs-lookup"><span data-stu-id="0735f-118">List of items in the filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0735f-119">-FilterType</span><span class="sxs-lookup"><span data-stu-id="0735f-119">-FilterType</span></span>
<span data-ttu-id="0735f-120">Beteendet för slut punkts filtret.</span><span class="sxs-lookup"><span data-stu-id="0735f-120">The behavior of the endpoint filter.</span></span> <span data-ttu-id="0735f-121">För närvarande stöds endast.</span><span class="sxs-lookup"><span data-stu-id="0735f-121">Currently only 'Include' is supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0735f-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="0735f-122">-Name</span></span>
<span data-ttu-id="0735f-123">Namnet på anslutnings övervakarens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="0735f-123">The name of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0735f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0735f-124">-ResourceId</span></span>
<span data-ttu-id="0735f-125">Resurs-ID för anslutnings övervakarens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="0735f-125">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0735f-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0735f-126">-Confirm</span></span>
<span data-ttu-id="0735f-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0735f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0735f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0735f-128">-WhatIf</span></span>
<span data-ttu-id="0735f-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0735f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0735f-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0735f-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0735f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0735f-131">CommonParameters</span></span>
<span data-ttu-id="0735f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0735f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0735f-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0735f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0735f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0735f-134">INPUTS</span></span>

### <span data-ttu-id="0735f-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="0735f-135">None</span></span>

## <span data-ttu-id="0735f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0735f-136">OUTPUTS</span></span>

### <span data-ttu-id="0735f-137">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0735f-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="0735f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0735f-138">NOTES</span></span>

## <span data-ttu-id="0735f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0735f-139">RELATED LINKS</span></span>
