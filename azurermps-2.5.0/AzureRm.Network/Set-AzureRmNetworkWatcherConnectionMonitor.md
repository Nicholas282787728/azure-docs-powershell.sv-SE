---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8ebbf4a554ef3dcb13726839ee8b7ebb330bad8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929657"
---
# <span data-ttu-id="e0c9f-101">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e0c9f-101">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="e0c9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0c9f-103">Uppdatera en anslutnings övervakare.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-103">Update a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0c9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0c9f-104">SYNTAX</span></span>

### <span data-ttu-id="e0c9f-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="e0c9f-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e0c9f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="e0c9f-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e0c9f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="e0c9f-107">SetByLocation</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e0c9f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0c9f-108">SetByResourceId</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="e0c9f-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="e0c9f-109">SetByInputObject</span></span>
```
Set-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-Name <String>]
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e0c9f-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0c9f-110">DESCRIPTION</span></span>
<span data-ttu-id="e0c9f-111">Den angivna anslutnings övervakaren uppdateras med Set-AzureRmNetworkWatcherConnectionMonitor cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-111">The Set-AzureRmNetworkWatcherConnectionMonitor cmdlet updates the specified connection monitor.</span></span>

## <span data-ttu-id="e0c9f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0c9f-112">EXAMPLES</span></span>

### <span data-ttu-id="e0c9f-113">---------------Exempel 1: uppdatera en anslutnings övervakare---------------</span><span class="sxs-lookup"><span data-stu-id="e0c9f-113">---------------  Example 1: Update a connection monitor ---------------</span></span>
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

<span data-ttu-id="e0c9f-114">I det här exemplet uppdaterar vi den befintliga anslutnings övervakningen genom att ändra destinationAddress och lägga till taggar.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-114">In this example we update existing connection monitor by changing destinationAddress and adding tags.</span></span>

## <span data-ttu-id="e0c9f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0c9f-115">PARAMETERS</span></span>

### <span data-ttu-id="e0c9f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0c9f-116">-AsJob</span></span>
<span data-ttu-id="e0c9f-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e0c9f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0c9f-118">-Autostart</span><span class="sxs-lookup"><span data-stu-id="e0c9f-118">-AutoStart</span></span>
<span data-ttu-id="e0c9f-119">Starta automatiskt.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-119">Auto start.</span></span>

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

### <span data-ttu-id="e0c9f-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e0c9f-120">-Confirm</span></span>
<span data-ttu-id="e0c9f-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0c9f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0c9f-122">-DefaultProfile</span></span>
<span data-ttu-id="e0c9f-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0c9f-124">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="e0c9f-124">-DestinationAddress</span></span>
<span data-ttu-id="e0c9f-125">IP-adressen för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-125">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="e0c9f-126">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="e0c9f-126">-DestinationPort</span></span>
<span data-ttu-id="e0c9f-127">Målport.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-127">Destination port.</span></span>

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

### <span data-ttu-id="e0c9f-128">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="e0c9f-128">-DestinationResourceId</span></span>
<span data-ttu-id="e0c9f-129">ID för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-129">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="e0c9f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e0c9f-130">-Force</span></span>
<span data-ttu-id="e0c9f-131">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="e0c9f-131">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e0c9f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0c9f-132">-InputObject</span></span>
<span data-ttu-id="e0c9f-133">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-133">Connection monitor object.</span></span>

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

### <span data-ttu-id="e0c9f-134">-Plats</span><span class="sxs-lookup"><span data-stu-id="e0c9f-134">-Location</span></span>
<span data-ttu-id="e0c9f-135">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-135">Location of the network watcher.</span></span>

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

### <span data-ttu-id="e0c9f-136">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e0c9f-136">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="e0c9f-137">Övervaknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-137">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="e0c9f-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="e0c9f-138">-Name</span></span>
<span data-ttu-id="e0c9f-139">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-139">The connection monitor name.</span></span>

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

### <span data-ttu-id="e0c9f-140">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0c9f-140">-NetworkWatcher</span></span>
<span data-ttu-id="e0c9f-141">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="e0c9f-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="e0c9f-142">-NetworkWatcherName</span></span>
<span data-ttu-id="e0c9f-143">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="e0c9f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0c9f-144">-ResourceGroupName</span></span>
<span data-ttu-id="e0c9f-145">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="e0c9f-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0c9f-146">-ResourceId</span></span>
<span data-ttu-id="e0c9f-147">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-147">Resource ID.</span></span>

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

### <span data-ttu-id="e0c9f-148">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="e0c9f-148">-SourcePort</span></span>
<span data-ttu-id="e0c9f-149">Källport.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-149">Source port.</span></span>

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

### <span data-ttu-id="e0c9f-150">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="e0c9f-150">-SourceResourceId</span></span>
<span data-ttu-id="e0c9f-151">ID för källa för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-151">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="e0c9f-152">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e0c9f-152">-Tag</span></span>
<span data-ttu-id="e0c9f-153">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-153">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e0c9f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0c9f-154">-WhatIf</span></span>
<span data-ttu-id="e0c9f-155">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0c9f-156">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e0c9f-156">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="e0c9f-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0c9f-157">INPUTS</span></span>

### <span data-ttu-id="e0c9f-158">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e0c9f-158">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="e0c9f-159">System. String Microsoft. Azure. commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="e0c9f-159">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="e0c9f-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0c9f-160">OUTPUTS</span></span>

### <span data-ttu-id="e0c9f-161">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="e0c9f-161">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="e0c9f-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0c9f-162">NOTES</span></span>
<span data-ttu-id="e0c9f-163">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="e0c9f-163">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="e0c9f-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0c9f-164">RELATED LINKS</span></span>
<span data-ttu-id="e0c9f-165">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="e0c9f-165">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="e0c9f-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="e0c9f-166">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="e0c9f-167">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="e0c9f-167">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="e0c9f-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="e0c9f-168">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)
[Start-AzureRmNetworkWatcherConnectionMonitor](./Start-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>

