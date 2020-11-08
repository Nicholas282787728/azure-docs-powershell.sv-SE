---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b84d11f259ffbf606bf0538a2ff71f6e9999db0a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088753"
---
# <span data-ttu-id="7c8a0-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7c8a0-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="7c8a0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c8a0-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8a0-103">Skapar en resurs för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-103">Creates a connection monitor resource.</span></span>

## <span data-ttu-id="7c8a0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c8a0-104">SYNTAX</span></span>

### <span data-ttu-id="7c8a0-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="7c8a0-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c8a0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7c8a0-106">SetByResource</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>]
 [-DestinationResourceId <String>] -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c8a0-107">SetByResourceV2</span><span class="sxs-lookup"><span data-stu-id="7c8a0-107">SetByResourceV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c8a0-108">SetByNameV2</span><span class="sxs-lookup"><span data-stu-id="7c8a0-108">SetByNameV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c8a0-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7c8a0-109">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 -MonitoringIntervalInSeconds <Int32> [-SourcePort <Int32>] [-DestinationResourceId <String>]
 -DestinationPort <Int32> [-DestinationAddress <String>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c8a0-110">SetByLocationV2</span><span class="sxs-lookup"><span data-stu-id="7c8a0-110">SetByLocationV2</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String>
 [-TestGroup <PSNetworkWatcherConnectionMonitorTestGroupObject[]>]
 [-Output <PSNetworkWatcherConnectionMonitorOutputObject[]>] [-Note <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c8a0-111">SetByConnectionMonitorV2Object</span><span class="sxs-lookup"><span data-stu-id="7c8a0-111">SetByConnectionMonitorV2Object</span></span>
```
New-AzNetworkWatcherConnectionMonitor [-ConnectionMonitor <PSNetworkWatcherConnectionMonitorObject>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c8a0-112">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c8a0-112">DESCRIPTION</span></span>
<span data-ttu-id="7c8a0-113">Med den New-AzNetworkWatcherConnectionMonitor cmdleten skapas en anslutnings övervaknings resurs för angiven källa och mål (SingleSourcedestination-anslutning) eller en uppsättning test grupper (MultiEndpointConnectionMonitor).</span><span class="sxs-lookup"><span data-stu-id="7c8a0-113">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor resource for specified source and destination (SingleSourcedestination connection monitor) or set of test groups (MultiEndpointConnectionMonitor).</span></span>

## <span data-ttu-id="7c8a0-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c8a0-114">EXAMPLES</span></span>

### <span data-ttu-id="7c8a0-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7c8a0-115">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80
```

<span data-ttu-id="7c8a0-116">Namn: cm-ID:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/providers/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 etag: W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState: lyckad Källa: {"ResourceId": "/Subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft. Compute/virtualMachines/VM "," Port ": 0} destination: {" adress ":" bing.com "," Port ": 80} MonitoringIntervalInSeconds: 60 Autostart: true StartTime: 1/12/2018 7:13:11 PM MonitoringStatus: Start plats: centraluseuap typ: Microsoft. Network/networkWatchers/connectionMonitors-Taggar: {}</span><span class="sxs-lookup"><span data-stu-id="7c8a0-116">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/t1 Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000 00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft .Compute/virtualMachines/vm", "Port": 0 } Destination                 : { "Address": "bing.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:13:11 PM MonitoringStatus            : Running Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : {}</span></span>

## <span data-ttu-id="7c8a0-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c8a0-117">PARAMETERS</span></span>

### <span data-ttu-id="7c8a0-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c8a0-118">-AsJob</span></span>
<span data-ttu-id="7c8a0-119">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7c8a0-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c8a0-120">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="7c8a0-120">-ConfigureOnly</span></span>
<span data-ttu-id="7c8a0-121">Konfigurera anslutnings övervakaren men starta den inte</span><span class="sxs-lookup"><span data-stu-id="7c8a0-121">Configure connection monitor, but do not start it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-122">-ConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7c8a0-122">-ConnectionMonitor</span></span>
<span data-ttu-id="7c8a0-123">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-123">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorObject
Parameter Sets: SetByConnectionMonitorV2Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8a0-124">-DefaultProfile</span></span>
<span data-ttu-id="7c8a0-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c8a0-126">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="7c8a0-126">-DestinationAddress</span></span>
<span data-ttu-id="7c8a0-127">Adress för anslutnings övervakarens destination (IP eller domän namn).</span><span class="sxs-lookup"><span data-stu-id="7c8a0-127">Address of the connection monitor destination (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-128">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="7c8a0-128">-DestinationPort</span></span>
<span data-ttu-id="7c8a0-129">Målport som används av anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-129">The destination port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-130">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="7c8a0-130">-DestinationResourceId</span></span>
<span data-ttu-id="7c8a0-131">ID för resursen som används som mål för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-131">The ID of the resource used as the destination by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-132">-Force</span><span class="sxs-lookup"><span data-stu-id="7c8a0-132">-Force</span></span>
<span data-ttu-id="7c8a0-133">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="7c8a0-133">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7c8a0-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="7c8a0-134">-Location</span></span>
<span data-ttu-id="7c8a0-135">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-135">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation, SetByLocationV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7c8a0-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="7c8a0-137">Övervaknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-137">Monitoring interval in seconds.</span></span> <span data-ttu-id="7c8a0-138">Standardvärdet är 60 sekunder.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-138">Default value is 60 seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c8a0-139">-Name</span></span>
<span data-ttu-id="7c8a0-140">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-140">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-141">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7c8a0-141">-NetworkWatcher</span></span>
<span data-ttu-id="7c8a0-142">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-142">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7c8a0-143">-NetworkWatcherName</span></span>
<span data-ttu-id="7c8a0-144">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-144">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-145">-Obs!</span><span class="sxs-lookup"><span data-stu-id="7c8a0-145">-Note</span></span>
<span data-ttu-id="7c8a0-146">Anteckningar som är kopplade till anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-146">Notes associated with connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-147">-Utdata</span><span class="sxs-lookup"><span data-stu-id="7c8a0-147">-Output</span></span>
<span data-ttu-id="7c8a0-148">Beskriver ett mål för att ansluta till en anslutning</span><span class="sxs-lookup"><span data-stu-id="7c8a0-148">Describes a connection monitor output destinations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c8a0-149">-ResourceGroupName</span></span>
<span data-ttu-id="7c8a0-150">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-150">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByNameV2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-151">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="7c8a0-151">-SourcePort</span></span>
<span data-ttu-id="7c8a0-152">Käll porten som används av anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-152">The source port used by connection monitor.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-153">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="7c8a0-153">-SourceResourceId</span></span>
<span data-ttu-id="7c8a0-154">ID för resursen som används som källa för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-154">The ID of the resource used as the source by connection monitor.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-155">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7c8a0-155">-Tag</span></span>
<span data-ttu-id="7c8a0-156">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-156">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceV2, SetByNameV2, SetByLocation, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-157">-TestGroup</span><span class="sxs-lookup"><span data-stu-id="7c8a0-157">-TestGroup</span></span>
<span data-ttu-id="7c8a0-158">Listan med test grupper.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-158">The list of test groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject[]
Parameter Sets: SetByResourceV2, SetByNameV2, SetByLocationV2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8a0-159">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7c8a0-159">-Confirm</span></span>
<span data-ttu-id="7c8a0-160">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c8a0-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c8a0-161">-WhatIf</span></span>
<span data-ttu-id="7c8a0-162">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c8a0-163">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c8a0-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8a0-164">CommonParameters</span></span>
<span data-ttu-id="7c8a0-165">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8a0-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8a0-166">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c8a0-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8a0-167">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c8a0-167">INPUTS</span></span>

### <span data-ttu-id="7c8a0-168">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7c8a0-168">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="7c8a0-169">System. String</span><span class="sxs-lookup"><span data-stu-id="7c8a0-169">System.String</span></span>

### <span data-ttu-id="7c8a0-170">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft. Azure. PowerShell. cmdletar. Network, version = 2.2.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7c8a0-170">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7c8a0-171">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. Network. Models. PSNetworkWatcherConnectionMonitorOutputObject, Microsoft. Azure. PowerShell. cmdletar. Network, version = 2.2.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7c8a0-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorOutputObject, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=2.2.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7c8a0-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c8a0-172">OUTPUTS</span></span>

### <span data-ttu-id="7c8a0-173">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="7c8a0-173">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="7c8a0-174">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="7c8a0-174">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="7c8a0-175">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c8a0-175">NOTES</span></span>

## <span data-ttu-id="7c8a0-176">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c8a0-176">RELATED LINKS</span></span>