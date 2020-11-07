---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 93c54df5cb0976aa0bd8f73881208c1966bbe9d0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924177"
---
# <span data-ttu-id="f4829-101">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f4829-101">Set-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="f4829-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4829-102">SYNOPSIS</span></span>
<span data-ttu-id="f4829-103">Uppdatera en anslutnings övervakare.</span><span class="sxs-lookup"><span data-stu-id="f4829-103">Update a connection monitor.</span></span>

## <span data-ttu-id="f4829-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4829-104">SYNTAX</span></span>

### <span data-ttu-id="f4829-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="f4829-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f4829-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f4829-106">SetByName</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f4829-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f4829-107">SetByLocation</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f4829-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f4829-108">SetByResourceId</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f4829-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="f4829-109">SetByInputObject</span></span>
```
Set-AzNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f4829-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4829-110">DESCRIPTION</span></span>
<span data-ttu-id="f4829-111">Den angivna anslutnings övervakaren uppdateras med Set-AzNetworkWatcherConnectionMonitor cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4829-111">The Set-AzNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="f4829-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4829-112">EXAMPLES</span></span>

### <span data-ttu-id="f4829-113">---------------Exempel 1: uppdatera en anslutnings övervakare---------------</span><span class="sxs-lookup"><span data-stu-id="f4829-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
```
PS C:\> Set-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm -SourceResourceId /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/RgCentralUSEUAP/providers/Microsoft.Compute/virtualMachines/vm 
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

<span data-ttu-id="f4829-114">I det här exemplet uppdaterar vi den befintliga anslutnings övervakningen genom att ändra destinationAddress och lägga till taggar.</span><span class="sxs-lookup"><span data-stu-id="f4829-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="f4829-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4829-115">PARAMETERS</span></span>

### <span data-ttu-id="f4829-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4829-116">-AsJob</span></span>
<span data-ttu-id="f4829-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f4829-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4829-118">-Autostart</span><span class="sxs-lookup"><span data-stu-id="f4829-118">-AutoStart</span></span>
<span data-ttu-id="f4829-119">Starta automatiskt.</span><span class="sxs-lookup"><span data-stu-id="f4829-119">Auto start.</span></span>

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

### <span data-ttu-id="f4829-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4829-120">-Confirm</span></span>
<span data-ttu-id="f4829-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4829-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4829-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4829-122">-DefaultProfile</span></span>
<span data-ttu-id="f4829-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4829-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4829-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="f4829-124">-DestinationAddress</span></span>
<span data-ttu-id="f4829-125">IP-adressen för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="f4829-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="f4829-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="f4829-126">-DestinationPort</span></span>
<span data-ttu-id="f4829-127">Målport.</span><span class="sxs-lookup"><span data-stu-id="f4829-127">Destination port.</span></span>

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

### <span data-ttu-id="f4829-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="f4829-128">-DestinationResourceId</span></span>
<span data-ttu-id="f4829-129">ID för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="f4829-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="f4829-130">-Force</span><span class="sxs-lookup"><span data-stu-id="f4829-130">-Force</span></span>
<span data-ttu-id="f4829-131">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="f4829-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f4829-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4829-132">-InputObject</span></span>
<span data-ttu-id="f4829-133">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="f4829-133">Connection monitor object.</span></span>

```yaml
Type: PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4829-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="f4829-134">-Location</span></span>
<span data-ttu-id="f4829-135">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="f4829-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f4829-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f4829-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="f4829-137">Övervaknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="f4829-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="f4829-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4829-138">-Name</span></span>
<span data-ttu-id="f4829-139">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="f4829-139">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4829-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f4829-140">-NetworkWatcher</span></span>
<span data-ttu-id="f4829-141">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="f4829-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="f4829-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f4829-142">-NetworkWatcherName</span></span>
<span data-ttu-id="f4829-143">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="f4829-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="f4829-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4829-144">-ResourceGroupName</span></span>
<span data-ttu-id="f4829-145">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f4829-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f4829-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4829-146">-ResourceId</span></span>
<span data-ttu-id="f4829-147">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="f4829-147">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4829-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="f4829-148">-SourcePort</span></span>
<span data-ttu-id="f4829-149">Källport.</span><span class="sxs-lookup"><span data-stu-id="f4829-149">Source port.</span></span>

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

### <span data-ttu-id="f4829-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="f4829-150">-SourceResourceId</span></span>
<span data-ttu-id="f4829-151">ID för källa för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="f4829-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="f4829-152">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f4829-152">-Tag</span></span>
<span data-ttu-id="f4829-153">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="f4829-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f4829-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4829-154">-WhatIf</span></span>
<span data-ttu-id="f4829-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4829-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4829-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4829-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="f4829-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4829-157">INPUTS</span></span>

### <span data-ttu-id="f4829-158">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f4829-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f4829-159">System. String Microsoft. Azure. commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="f4829-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="f4829-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4829-160">OUTPUTS</span></span>

### <span data-ttu-id="f4829-161">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="f4829-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="f4829-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4829-162">NOTES</span></span>
<span data-ttu-id="f4829-163">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="f4829-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="f4829-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4829-164">RELATED LINKS</span></span>
<span data-ttu-id="f4829-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="f4829-165">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="f4829-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="f4829-166">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="f4829-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="f4829-167">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="f4829-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md) 
 [Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="f4829-168">[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)
[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)
[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)</span></span>

