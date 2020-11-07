---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 3e5853d99157fef87c2f02c2be9fab7bb983d1ae
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930154"
---
# <span data-ttu-id="eb888-101">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="eb888-101">New-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="eb888-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="eb888-102">SYNOPSIS</span></span>
<span data-ttu-id="eb888-103">Skapar en anslutnings övervakare.</span><span class="sxs-lookup"><span data-stu-id="eb888-103">Creates a connection monitor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb888-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="eb888-104">SYNTAX</span></span>

### <span data-ttu-id="eb888-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="eb888-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String>
 -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="eb888-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="eb888-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> -SourceResourceId <String> [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>]
 [-DestinationResourceId <String>] [-DestinationAddress <String>] [-DestinationPort <Int32>]
 [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="eb888-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="eb888-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> -SourceResourceId <String>
 [-MonitoringIntervalInSeconds <Int32>] [-SourcePort <Int32>] [-DestinationResourceId <String>]
 [-DestinationAddress <String>] [-DestinationPort <Int32>] [-AutoStart <Boolean>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="eb888-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="eb888-108">DESCRIPTION</span></span>
<span data-ttu-id="eb888-109">New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates en anslutnings Övervakare för en viss källa och mål.</span><span class="sxs-lookup"><span data-stu-id="eb888-109">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet rcreates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="eb888-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="eb888-110">EXAMPLES</span></span>

### <span data-ttu-id="eb888-111">---------------Exempel 1: skapa en anslutnings Övervakare för en VM-och Internet mål---------------</span><span class="sxs-lookup"><span data-stu-id="eb888-111">---------------  Example 1: Create a connection monitor for a vm and internet destination ---------------</span></span>
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

<span data-ttu-id="eb888-112">Med den New-AzureRmNetworkWatcherConnectionMonitor cmdleten skapas en anslutnings Övervakare för en viss källa och mål.</span><span class="sxs-lookup"><span data-stu-id="eb888-112">The New-AzureRmNetworkWatcherConnectionMonitor cmdlet creates a connection monitor for a specified source and destination.</span></span>

## <span data-ttu-id="eb888-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="eb888-113">PARAMETERS</span></span>

### <span data-ttu-id="eb888-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb888-114">-AsJob</span></span>
<span data-ttu-id="eb888-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="eb888-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb888-116">-Autostart</span><span class="sxs-lookup"><span data-stu-id="eb888-116">-AutoStart</span></span>
<span data-ttu-id="eb888-117">Starta automatiskt.</span><span class="sxs-lookup"><span data-stu-id="eb888-117">Auto start.</span></span>

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

### <span data-ttu-id="eb888-118">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="eb888-118">-Confirm</span></span>
<span data-ttu-id="eb888-119">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="eb888-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb888-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb888-120">-DefaultProfile</span></span>
<span data-ttu-id="eb888-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="eb888-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb888-122">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="eb888-122">-DestinationAddress</span></span>
<span data-ttu-id="eb888-123">IP-adressen för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="eb888-123">The Ip address of the connection monitor destination.</span></span>

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

### <span data-ttu-id="eb888-124">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="eb888-124">-DestinationPort</span></span>
<span data-ttu-id="eb888-125">Målport.</span><span class="sxs-lookup"><span data-stu-id="eb888-125">Destination port.</span></span>

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

### <span data-ttu-id="eb888-126">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="eb888-126">-DestinationResourceId</span></span>
<span data-ttu-id="eb888-127">ID för anslutnings övervakarens destination.</span><span class="sxs-lookup"><span data-stu-id="eb888-127">The ID of the connection monitor destination.</span></span>

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

### <span data-ttu-id="eb888-128">-Force</span><span class="sxs-lookup"><span data-stu-id="eb888-128">-Force</span></span>
<span data-ttu-id="eb888-129">Fråga inte efter bekräftelse om du vill skriva över en resurs</span><span class="sxs-lookup"><span data-stu-id="eb888-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="eb888-130">-Plats</span><span class="sxs-lookup"><span data-stu-id="eb888-130">-Location</span></span>
<span data-ttu-id="eb888-131">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="eb888-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="eb888-132">-MonitoringIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="eb888-132">-MonitoringIntervalInSeconds</span></span>
<span data-ttu-id="eb888-133">Övervaknings intervall i sekunder.</span><span class="sxs-lookup"><span data-stu-id="eb888-133">Monitoring interval in seconds.</span></span>

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

### <span data-ttu-id="eb888-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="eb888-134">-Name</span></span>
<span data-ttu-id="eb888-135">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="eb888-135">The connection monitor name.</span></span>

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

### <span data-ttu-id="eb888-136">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eb888-136">-NetworkWatcher</span></span>
<span data-ttu-id="eb888-137">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="eb888-137">The network watcher resource.</span></span>

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

### <span data-ttu-id="eb888-138">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="eb888-138">-NetworkWatcherName</span></span>
<span data-ttu-id="eb888-139">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="eb888-139">The name of network watcher.</span></span>

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

### <span data-ttu-id="eb888-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb888-140">-ResourceGroupName</span></span>
<span data-ttu-id="eb888-141">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="eb888-141">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="eb888-142">-SourcePort</span><span class="sxs-lookup"><span data-stu-id="eb888-142">-SourcePort</span></span>
<span data-ttu-id="eb888-143">Källport.</span><span class="sxs-lookup"><span data-stu-id="eb888-143">Source port.</span></span>

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

### <span data-ttu-id="eb888-144">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="eb888-144">-SourceResourceId</span></span>
<span data-ttu-id="eb888-145">ID för källa för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="eb888-145">The ID of the connection monitor source.</span></span>

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

### <span data-ttu-id="eb888-146">-Tagg</span><span class="sxs-lookup"><span data-stu-id="eb888-146">-Tag</span></span>
<span data-ttu-id="eb888-147">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="eb888-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="eb888-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb888-148">-WhatIf</span></span>
<span data-ttu-id="eb888-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="eb888-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb888-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="eb888-150">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="eb888-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="eb888-151">INPUTS</span></span>

### <span data-ttu-id="eb888-152">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="eb888-152">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="eb888-153">System. String</span><span class="sxs-lookup"><span data-stu-id="eb888-153">System.String</span></span>


## <span data-ttu-id="eb888-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="eb888-154">OUTPUTS</span></span>

### <span data-ttu-id="eb888-155">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="eb888-155">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="eb888-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="eb888-156">NOTES</span></span>
<span data-ttu-id="eb888-157">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="eb888-157">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="eb888-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="eb888-158">RELATED LINKS</span></span>
<span data-ttu-id="eb888-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="eb888-159">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="eb888-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="eb888-160">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="eb888-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="eb888-161">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="eb888-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md) 
 [Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="eb888-162">[Get-AzureRmNetworkWatcherConnectionMonitor](./Get-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)
[Remove-AzureRmNetworkWatcherConnectionMonitor](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)</span></span>
