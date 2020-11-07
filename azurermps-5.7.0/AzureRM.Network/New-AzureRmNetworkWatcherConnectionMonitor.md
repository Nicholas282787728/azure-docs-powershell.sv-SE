---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: b8dd04fa4727465ee9b3be3eaf5e5e06a2243338
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757665"
---
# <span data-ttu-id="8ca24-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca24-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="8ca24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8ca24-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca24-103">Skapar en anslutnings övervakare.</span><span class="sxs-lookup"><span data-stu-id="8ca24-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ca24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8ca24-104">SYNTAX</span></span>

### <span data-ttu-id="8ca24-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="8ca24-105">SetByName (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ca24-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8ca24-106">SetByResource</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ca24-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="8ca24-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-ConfigureOnly] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ca24-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8ca24-108">DESCRIPTION</span></span>
<span data-ttu-id="8ca24-109">New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates en anslutnings Övervakare för en viss källa och mål.</span><span class="sxs-lookup"><span data-stu-id="8ca24-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="8ca24-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8ca24-110">EXAMPLES</span></span>

### <span data-ttu-id="8ca24-111">Exempel 1: skapa en anslutnings Övervakare för ett virtuellt dator-och Internet mål</span><span class="sxs-lookup"><span data-stu-id="8ca24-111">Example 1: Create a connection monitor for a vm and internet destination</span></span>
```
PS C:\> New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/t1
Etag                        : W/"e86b28cf-b907-4475-a8b7-34d310367694"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/00000000-0000-0000-0000-0000000
                                00000/resourceGroups/RgCentralUSEUAP/providers/Microsoft
                                .Compute/virtualMachines/vm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "bing.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:13:11 PM
MonitoringStatus            : Running
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {}
```

<span data-ttu-id="8ca24-112">Med den New-AzureRmNetworkWatcherConnectionMonitor cmdleten skapas en anslutnings Övervakare för en viss källa och mål.</span><span class="sxs-lookup"><span data-stu-id="8ca24-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="8ca24-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8ca24-113">PARAMETERS</span></span>

### <span data-ttu-id="8ca24-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ca24-114">-AsJob</span></span>
<span data-ttu-id="8ca24-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8ca24-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8ca24-116">-Confirm</span></span>
<span data-ttu-id="8ca24-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8ca24-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ca24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca24-118">-DefaultProfile</span></span>
<span data-ttu-id="8ca24-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8ca24-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ca24-120">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="8ca24-120">-DestinationAddress</span></span>
<span data-ttu-id="8ca24-121">IP-adressen för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="8ca24-121">The Ip address of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-122">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="8ca24-122">-DestinationPort</span></span>
<span data-ttu-id="8ca24-123">Målport.</span><span class="sxs-lookup"><span data-stu-id="8ca24-123">Destination port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-124">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="8ca24-124">-DestinationResourceId</span></span>
<span data-ttu-id="8ca24-125">ID för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="8ca24-125">The ID of the connection monitor destination.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-126">-Force</span><span class="sxs-lookup"><span data-stu-id="8ca24-126">-Force</span></span>
<span data-ttu-id="8ca24-127">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="8ca24-127">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-128">-Plats</span><span class="sxs-lookup"><span data-stu-id="8ca24-128">-Location</span></span>
<span data-ttu-id="8ca24-129">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="8ca24-129">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-130">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8ca24-130">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="8ca24-131">Övervaknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="8ca24-131">Monitoring interval in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="8ca24-132">-Name</span></span>
<span data-ttu-id="8ca24-133">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="8ca24-133">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-134">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ca24-134">-NetworkWatcher</span></span>
<span data-ttu-id="8ca24-135">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="8ca24-135">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-136">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8ca24-136">-NetworkWatcherName</span></span>
<span data-ttu-id="8ca24-137">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="8ca24-137">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ca24-138">-ResourceGroupName</span></span>
<span data-ttu-id="8ca24-139">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8ca24-139">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-140">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="8ca24-140">-SourcePort</span></span>
<span data-ttu-id="8ca24-141">Källport.</span><span class="sxs-lookup"><span data-stu-id="8ca24-141">Source port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-142">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="8ca24-142">-SourceResourceId</span></span>
<span data-ttu-id="8ca24-143">ID för källa för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="8ca24-143">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-144">-Tagg</span><span class="sxs-lookup"><span data-stu-id="8ca24-144">-Tag</span></span>
<span data-ttu-id="8ca24-145">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="8ca24-145">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ca24-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ca24-146">-WhatIf</span></span>
<span data-ttu-id="8ca24-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8ca24-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ca24-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8ca24-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ca24-149">-ConfigureOnly</span><span class="sxs-lookup"><span data-stu-id="8ca24-149">-ConfigureOnly</span></span>
<span data-ttu-id="8ca24-150">Konfigurera anslutnings övervakaren men starta den inte</span><span class="sxs-lookup"><span data-stu-id="8ca24-150">Configure connection monitor, but do not start it</span></span>

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

### <span data-ttu-id="8ca24-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca24-151">CommonParameters</span></span>
<span data-ttu-id="8ca24-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ca24-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8ca24-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ca24-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca24-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8ca24-154">INPUTS</span></span>

### <span data-ttu-id="8ca24-155">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ca24-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8ca24-156">System. String</span><span class="sxs-lookup"><span data-stu-id="8ca24-156">System.String</span></span>

## <span data-ttu-id="8ca24-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8ca24-157">OUTPUTS</span></span>

### <span data-ttu-id="8ca24-158">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="8ca24-158">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="8ca24-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8ca24-159">NOTES</span></span>
<span data-ttu-id="8ca24-160">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="8ca24-160">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="8ca24-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8ca24-161">RELATED LINKS</span></span>

[<span data-ttu-id="8ca24-162">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ca24-162">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8ca24-163">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ca24-163">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8ca24-164">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8ca24-164">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="8ca24-165">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8ca24-165">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="8ca24-166">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8ca24-166">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="8ca24-167">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8ca24-167">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="8ca24-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8ca24-168">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="8ca24-169">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ca24-169">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8ca24-170">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8ca24-170">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="8ca24-171">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ca24-171">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8ca24-172">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ca24-172">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8ca24-173">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8ca24-173">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="8ca24-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca24-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8ca24-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8ca24-175">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="8ca24-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca24-176">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8ca24-177">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca24-177">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8ca24-178">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca24-178">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="8ca24-179">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8ca24-179">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
