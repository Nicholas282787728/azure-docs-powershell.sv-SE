---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394104"
---
# <span data-ttu-id="56f23-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="56f23-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="56f23-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="56f23-102">SYNOPSIS</span></span>
<span data-ttu-id="56f23-103">Skapar slut punkt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="56f23-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="56f23-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="56f23-104">SYNTAX</span></span>

### <span data-ttu-id="56f23-105">AzureVM</span><span class="sxs-lookup"><span data-stu-id="56f23-105">AzureVM</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56f23-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="56f23-106">AzureVNet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56f23-107">AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="56f23-107">AzureSubnet</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56f23-108">ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="56f23-108">ExternalAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56f23-109">MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="56f23-109">MMAWorkspaceMachine</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56f23-110">MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="56f23-110">MMAWorkspaceNetwork</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56f23-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="56f23-111">DESCRIPTION</span></span>
<span data-ttu-id="56f23-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet skapar slut punkt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="56f23-112">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="56f23-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="56f23-113">EXAMPLES</span></span>

### <span data-ttu-id="56f23-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="56f23-114">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

<span data-ttu-id="56f23-115">Namn: workspaceEndpoint: MMAWorkspaceMachine ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace adress: scope: {"include": [{"Address": "WIN-P0HGNDO2S1B"}]}</span><span class="sxs-lookup"><span data-stu-id="56f23-115">Name       : workspaceEndpoint Type       : MMAWorkspaceMachine ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Scope     : { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="56f23-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="56f23-116">PARAMETERS</span></span>

### <span data-ttu-id="56f23-117">-Adress</span><span class="sxs-lookup"><span data-stu-id="56f23-117">-Address</span></span>
<span data-ttu-id="56f23-118">Adress för anslutnings övervakarens slut punkt (IP eller domän namn).</span><span class="sxs-lookup"><span data-stu-id="56f23-118">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-119">-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="56f23-119">-AzureSubnet</span></span>
<span data-ttu-id="56f23-120">Slut punkts brytare för Azure under nätet.</span><span class="sxs-lookup"><span data-stu-id="56f23-120">Azure Subnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-121">-AzureVM</span><span class="sxs-lookup"><span data-stu-id="56f23-121">-AzureVM</span></span>
<span data-ttu-id="56f23-122">Virtuell dator slut punkts brytare för Azure.</span><span class="sxs-lookup"><span data-stu-id="56f23-122">Azure VM endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-123">-AzureVNet</span><span class="sxs-lookup"><span data-stu-id="56f23-123">-AzureVNet</span></span>
<span data-ttu-id="56f23-124">Slut punkts brytare för Azure VNet.</span><span class="sxs-lookup"><span data-stu-id="56f23-124">Azure Vnet endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-125">-CoverageLevel</span><span class="sxs-lookup"><span data-stu-id="56f23-125">-CoverageLevel</span></span>
<span data-ttu-id="56f23-126">Testa täckning för slut punkten.</span><span class="sxs-lookup"><span data-stu-id="56f23-126">Test coverage for the endpoint.</span></span>
<span data-ttu-id="56f23-127">Värden som stöds är standard, lågt, BelowAverage, Average, AboveAvergae, full.</span><span class="sxs-lookup"><span data-stu-id="56f23-127">Supported values are Default, Low, BelowAverage, Average, AboveAvergae, Full.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f23-128">-DefaultProfile</span></span>
<span data-ttu-id="56f23-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="56f23-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56f23-130">-ExcludeItem</span><span class="sxs-lookup"><span data-stu-id="56f23-130">-ExcludeItem</span></span>
<span data-ttu-id="56f23-131">Lista över objekt som ska undantas från slut punktens omfattning.</span><span class="sxs-lookup"><span data-stu-id="56f23-131">List of items which need to be excluded from endpoint scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-132">-ExternalAddress</span><span class="sxs-lookup"><span data-stu-id="56f23-132">-ExternalAddress</span></span>
<span data-ttu-id="56f23-133">Slut punkts brytare för extern adress.</span><span class="sxs-lookup"><span data-stu-id="56f23-133">External Address endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-134">-IncludeItem</span><span class="sxs-lookup"><span data-stu-id="56f23-134">-IncludeItem</span></span>
<span data-ttu-id="56f23-135">Lista över objekt som måste ingå i endpont scope.</span><span class="sxs-lookup"><span data-stu-id="56f23-135">List of items which need to be included into endpont scope.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-136">-MMAWorkspaceMachine</span><span class="sxs-lookup"><span data-stu-id="56f23-136">-MMAWorkspaceMachine</span></span>
<span data-ttu-id="56f23-137">Slut punkts brytare för MMA-arbetsyta.</span><span class="sxs-lookup"><span data-stu-id="56f23-137">MMA Workspace Machine endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-138">-MMAWorkspaceNetwork</span><span class="sxs-lookup"><span data-stu-id="56f23-138">-MMAWorkspaceNetwork</span></span>
<span data-ttu-id="56f23-139">Slut punkts brytare för nätverks MMA.</span><span class="sxs-lookup"><span data-stu-id="56f23-139">MMA Workspace Network endpoint switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-140">-Namn</span><span class="sxs-lookup"><span data-stu-id="56f23-140">-Name</span></span>
<span data-ttu-id="56f23-141">Namnet på anslutnings övervakarens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="56f23-141">The name of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56f23-142">-ResourceId</span></span>
<span data-ttu-id="56f23-143">Resurs-ID för anslutnings övervakarens slut punkt.</span><span class="sxs-lookup"><span data-stu-id="56f23-143">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56f23-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="56f23-144">-Confirm</span></span>
<span data-ttu-id="56f23-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="56f23-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56f23-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56f23-146">-WhatIf</span></span>
<span data-ttu-id="56f23-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="56f23-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56f23-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="56f23-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56f23-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f23-149">CommonParameters</span></span>
<span data-ttu-id="56f23-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f23-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f23-151">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56f23-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f23-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="56f23-152">INPUTS</span></span>

### <span data-ttu-id="56f23-153">Ingen</span><span class="sxs-lookup"><span data-stu-id="56f23-153">None</span></span>

## <span data-ttu-id="56f23-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="56f23-154">OUTPUTS</span></span>

### <span data-ttu-id="56f23-155">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="56f23-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="56f23-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="56f23-156">NOTES</span></span>

## <span data-ttu-id="56f23-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="56f23-157">RELATED LINKS</span></span>
