---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 5c7709c234ba762e5b87418cc0e9b3fc4637ac11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756153"
---
# <span data-ttu-id="2209a-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2209a-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="2209a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2209a-102">SYNOPSIS</span></span>
<span data-ttu-id="2209a-103">Uppdatera en anslutnings övervakare.</span><span class="sxs-lookup"><span data-stu-id="2209a-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2209a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2209a-104">SYNTAX</span></span>

### <span data-ttu-id="2209a-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="2209a-105">SetByName (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2209a-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2209a-106">SetByResource</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2209a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2209a-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2209a-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2209a-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2209a-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="2209a-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2209a-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2209a-110">DESCRIPTION</span></span>
<span data-ttu-id="2209a-111">Den angivna anslutnings övervakaren uppdateras med Set-AzureRmNetworkWatcherConnectionMonitor cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2209a-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="2209a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2209a-112">EXAMPLES</span></span>

### <span data-ttu-id="2209a-113">Exempel 1: uppdatera en anslutnings bildskärm</span><span class="sxs-lookup"><span data-stu-id="2209a-113">Example 1: Update a connection monitor</span></span>
```
PS C:\> Set-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
-DestinationAddress google.com -DestinationPort 80 -Tag @{"key1" = "value1"}

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"5b2b20e8-0ce0-417e-9607-76208149bb67"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMach
                                ines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="2209a-114">I det här exemplet uppdaterar vi den befintliga anslutnings övervakningen genom att ändra destinationAddress och lägga till taggar.</span><span class="sxs-lookup"><span data-stu-id="2209a-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="2209a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2209a-115">PARAMETERS</span></span>

### <span data-ttu-id="2209a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2209a-116">-AsJob</span></span>
<span data-ttu-id="2209a-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2209a-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-118">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="2209a-118">-ConfigureOnly</span></span>
<span data-ttu-id="2209a-119">Konfigurera anslutnings övervakaren men starta den inte</span><span class="sxs-lookup"><span data-stu-id="2209a-119">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="2209a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2209a-120">-DefaultProfile</span></span>
<span data-ttu-id="2209a-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2209a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="2209a-122">-DestinationAddress</span></span>
<span data-ttu-id="2209a-123">IP-adressen för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="2209a-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="2209a-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="2209a-124">-DestinationPort</span></span>
<span data-ttu-id="2209a-125">Målport.</span><span class="sxs-lookup"><span data-stu-id="2209a-125">Destination port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="2209a-126">-DestinationResourceId</span></span>
<span data-ttu-id="2209a-127">ID för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="2209a-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="2209a-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2209a-128">-InputObject</span></span>
<span data-ttu-id="2209a-129">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="2209a-129">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="2209a-130">-Location</span></span>
<span data-ttu-id="2209a-131">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="2209a-131">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2209a-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="2209a-133">Övervaknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="2209a-133">Monitoring interval in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="2209a-134">-Name</span></span>
<span data-ttu-id="2209a-135">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="2209a-135">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2209a-136">-NetworkWatcher</span></span>
<span data-ttu-id="2209a-137">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="2209a-137">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2209a-138">-NetworkWatcherName</span></span>
<span data-ttu-id="2209a-139">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="2209a-139">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2209a-140">-ResourceGroupName</span></span>
<span data-ttu-id="2209a-141">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2209a-141">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2209a-142">-ResourceId</span></span>
<span data-ttu-id="2209a-143">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="2209a-143">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-144">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="2209a-144">-SourcePort</span></span>
<span data-ttu-id="2209a-145">Källport.</span><span class="sxs-lookup"><span data-stu-id="2209a-145">Source port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-146">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="2209a-146">-SourceResourceId</span></span>
<span data-ttu-id="2209a-147">ID för källa för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="2209a-147">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="2209a-148">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2209a-148">-Tag</span></span>
<span data-ttu-id="2209a-149">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="2209a-149">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2209a-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2209a-150">-Confirm</span></span>
<span data-ttu-id="2209a-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2209a-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2209a-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2209a-152">-WhatIf</span></span>
<span data-ttu-id="2209a-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2209a-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2209a-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2209a-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2209a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2209a-155">CommonParameters</span></span>
<span data-ttu-id="2209a-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2209a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2209a-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2209a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2209a-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2209a-158">INPUTS</span></span>

### <span data-ttu-id="2209a-159">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2209a-159">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2209a-160">Parametrar: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2209a-160">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="2209a-161">System. String</span><span class="sxs-lookup"><span data-stu-id="2209a-161">System.String</span></span>

### <span data-ttu-id="2209a-162">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="2209a-162">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="2209a-163">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2209a-163">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2209a-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2209a-164">OUTPUTS</span></span>

### <span data-ttu-id="2209a-165">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="2209a-165">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="2209a-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2209a-166">NOTES</span></span>
<span data-ttu-id="2209a-167">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="2209a-167">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="2209a-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2209a-168">RELATED LINKS</span></span>

[<span data-ttu-id="2209a-169">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2209a-169">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="2209a-170">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2209a-170">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="2209a-171">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2209a-171">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="2209a-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2209a-172">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="2209a-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2209a-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="2209a-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2209a-174">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="2209a-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2209a-175">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="2209a-176">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2209a-176">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="2209a-177">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2209a-177">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="2209a-178">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2209a-178">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="2209a-179">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2209a-179">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="2209a-180">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2209a-180">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="2209a-181">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2209a-181">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="2209a-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2209a-182">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="2209a-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2209a-183">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="2209a-184">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2209a-184">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="2209a-185">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2209a-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="2209a-186">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2209a-186">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="2209a-187">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2209a-187">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="2209a-188">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2209a-188">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="2209a-189">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2209a-189">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="2209a-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2209a-190">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="2209a-191">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2209a-191">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="2209a-192">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2209a-192">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="2209a-193">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2209a-193">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="2209a-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2209a-194">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="2209a-195">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2209a-195">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
