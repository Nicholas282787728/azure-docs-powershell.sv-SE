---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: bfdcfbf57f44479ad35a2b9075590a0d40351ec9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922106"
---
# <span data-ttu-id="a5c09-101">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a5c09-101">New-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a5c09-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5c09-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c09-103">Skapar en anslutnings övervakare.</span><span class="sxs-lookup"><span data-stu-id="a5c09-103">Creates a connection monitor.</span></span>

## <span data-ttu-id="a5c09-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5c09-104">SYNTAX</span></span>

### <span data-ttu-id="a5c09-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="a5c09-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a5c09-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a5c09-106">SetByName</span></span>
```
New-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="a5c09-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a5c09-107">SetByLocation</span></span>
```
New-AzNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a5c09-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5c09-108">DESCRIPTION</span></span>
<span data-ttu-id="a5c09-109">New-AzNetworkWatcherConnectionMonitor cmdlet rcreates en anslutnings Övervakare för en viss källa och mål.</span><span class="sxs-lookup"><span data-stu-id="a5c09-109">The New-AzNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a5c09-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5c09-110">EXAMPLES</span></span>

### <span data-ttu-id="a5c09-111">---------------Exempel 1: skapa en anslutnings Övervakare för en VM-och Internet mål---------------</span><span class="sxs-lookup"><span data-stu-id="a5c09-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
```
PS C:\> New-AzNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm -DestinationAddress bing.com -DestinationPort 80

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

<span data-ttu-id="a5c09-112">Med den New-AzNetworkWatcherConnectionMonitor cmdleten skapas en anslutnings Övervakare för en viss källa och mål.</span><span class="sxs-lookup"><span data-stu-id="a5c09-112">The New-AzNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="a5c09-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5c09-113">PARAMETERS</span></span>

### <span data-ttu-id="a5c09-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5c09-114">-AsJob</span></span>
<span data-ttu-id="a5c09-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a5c09-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5c09-116">-Autostart</span><span class="sxs-lookup"><span data-stu-id="a5c09-116">-AutoStart</span></span>
<span data-ttu-id="a5c09-117">Starta automatiskt.</span><span class="sxs-lookup"><span data-stu-id="a5c09-117">Auto start.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c09-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5c09-118">-Confirm</span></span>
<span data-ttu-id="a5c09-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5c09-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5c09-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c09-120">-DefaultProfile</span></span>
<span data-ttu-id="a5c09-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5c09-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5c09-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a5c09-122">-DestinationAddress</span></span>
<span data-ttu-id="a5c09-123">IP-adressen för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="a5c09-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a5c09-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a5c09-124">-DestinationPort</span></span>
<span data-ttu-id="a5c09-125">Målport.</span><span class="sxs-lookup"><span data-stu-id="a5c09-125">Destination port.</span></span>

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

### <span data-ttu-id="a5c09-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c09-126">-DestinationResourceId</span></span>
<span data-ttu-id="a5c09-127">ID för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="a5c09-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="a5c09-128">-Force</span><span class="sxs-lookup"><span data-stu-id="a5c09-128">-Force</span></span>
<span data-ttu-id="a5c09-129">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="a5c09-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a5c09-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="a5c09-130">-Location</span></span>
<span data-ttu-id="a5c09-131">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="a5c09-131">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c09-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a5c09-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="a5c09-133">Övervaknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="a5c09-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="a5c09-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5c09-134">-Name</span></span>
<span data-ttu-id="a5c09-135">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="a5c09-135">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c09-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5c09-136">-NetworkWatcher</span></span>
<span data-ttu-id="a5c09-137">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="a5c09-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="a5c09-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a5c09-138">-NetworkWatcherName</span></span>
<span data-ttu-id="a5c09-139">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="a5c09-139">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c09-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c09-140">-ResourceGroupName</span></span>
<span data-ttu-id="a5c09-141">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a5c09-141">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c09-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="a5c09-142">-SourcePort</span></span>
<span data-ttu-id="a5c09-143">Källport.</span><span class="sxs-lookup"><span data-stu-id="a5c09-143">Source port.</span></span>

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

### <span data-ttu-id="a5c09-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="a5c09-144">-SourceResourceId</span></span>
<span data-ttu-id="a5c09-145">ID för källa för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="a5c09-145">The ID of the connection monitor source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5c09-146">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a5c09-146">-Tag</span></span>
<span data-ttu-id="a5c09-147">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="a5c09-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a5c09-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c09-148">-WhatIf</span></span>
<span data-ttu-id="a5c09-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5c09-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c09-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5c09-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="a5c09-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5c09-151">INPUTS</span></span>

### <span data-ttu-id="a5c09-152">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a5c09-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a5c09-153">System. String</span><span class="sxs-lookup"><span data-stu-id="a5c09-153">System.String</span></span>


## <span data-ttu-id="a5c09-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5c09-154">OUTPUTS</span></span>

### <span data-ttu-id="a5c09-155">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a5c09-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="a5c09-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5c09-156">NOTES</span></span>
<span data-ttu-id="a5c09-157">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="a5c09-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a5c09-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5c09-158">RELATED LINKS</span></span>
<span data-ttu-id="a5c09-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="a5c09-159">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="a5c09-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="a5c09-160">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="a5c09-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="a5c09-161">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="a5c09-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="a5c09-162">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)</span></span>
