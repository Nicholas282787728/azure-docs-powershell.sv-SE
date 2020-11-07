---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitorreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitorReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitorReport.md
ms.openlocfilehash: b524eb04ef9f6765fceb0f3ccb457e29bcc81093
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922244"
---
# <span data-ttu-id="d53fd-101">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d53fd-101">Get-AzNetworkWatcherConnectionMonitorReport</span></span>

## <span data-ttu-id="d53fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d53fd-102">SYNOPSIS</span></span>
<span data-ttu-id="d53fd-103">Fråga en ögonblicks bild av de senaste anslutnings lägena.</span><span class="sxs-lookup"><span data-stu-id="d53fd-103">Query a snapshot of the most recent connection states.</span></span>

## <span data-ttu-id="d53fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d53fd-104">SYNTAX</span></span>

### <span data-ttu-id="d53fd-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="d53fd-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="d53fd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d53fd-106">SetByName</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="d53fd-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d53fd-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="d53fd-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d53fd-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="d53fd-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="d53fd-109">SetByInputObject</span></span>
```
Get-AzNetworkWatcherConnectionMonitorReport -InputObject <PSConnectionMonitorResult> [-Name <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="d53fd-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d53fd-110">DESCRIPTION</span></span>
<span data-ttu-id="d53fd-111">Get-AzNetworkWatcherConnectionMonitorReport cmdlet returnerar rapporten med de senaste anslutnings lägena.</span><span class="sxs-lookup"><span data-stu-id="d53fd-111">The Get-AzNetworkWatcherConnectionMonitorReport cmdlet returns the report on the most recent connection states.</span></span>

## <span data-ttu-id="d53fd-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d53fd-112">EXAMPLES</span></span>

### <span data-ttu-id="d53fd-113">---------------Exempel 1: hämta den senaste anslutningen för anslutnings övervakaren med namn på den angivna platsen---------------</span><span class="sxs-lookup"><span data-stu-id="d53fd-113">---------------  Example 1: Get the most recent connection snapshot of the connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitorReport -Location centraluseuap -Name cm


States : [
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-12T01:18:20Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "1530e0f2-c9b7-4bc0-a205-cf7332cd8983",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "b19b74b1-423d-4f0b-99cd-bcaed4d0b8a2",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "80e46c56-2cf9-4106-8602-608a74832d41"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "80e46c56-2cf9-4106-8602-608a74832d41",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "e17cf884-69db-43b8-9cd5-f920770a0dbe"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "e17cf884-69db-43b8-9cd5-f920770a0dbe",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Unreachable",
             "StartTime": "2018-01-12T01:14:11Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "b6251ff8-3d07-4fdf-98f8-04b168e1cf90",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "de6d463b-47fb-4beb-afc4-d77782755313"
                 ],
                 "Issues": [
                   {
                     "Origin": "Local",
                     "Severity": "Error",
                     "Type": "NetworkError",
                     "Context": []
                   }
                 ]
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "de6d463b-47fb-4beb-afc4-d77782755313",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "0cbadb7e-cd99-4fa9-a832-eb4e0d112293"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "0cbadb7e-cd99-4fa9-a832-eb4e0d112293",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "538005d1-994a-4350-9866-6985385beecf"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "538005d1-994a-4350-9866-6985385beecf",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           },
           {
             "ConnectionState": "Reachable",
             "StartTime": "2018-01-11T23:54:05Z",
             "EvaluationState": "Completed",
             "Hops": [
               {
                 "Type": "Source",
                 "Id": "3dbec7e8-a37f-4acd-bc5f-86918fffba0e",
                 "Address": "10.1.1.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "1a87cf61-1be6-4add-bba7-f84afbcf3726"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "1a87cf61-1be6-4add-bba7-f84afbcf3726",
                 "Address": "10.1.2.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/fwNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "070c0740-308e-43ba-b72f-5d8d5a6537ec"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualAppliance",
                 "Id": "070c0740-308e-43ba-b72f-5d8d5a6537ec",
                 "Address": "10.1.3.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/auNic/ipConfigurations/ipconfig1",
                 "NextHopIds": [
                   "760182e1-c88d-4cfc-a711-65e7e622a67a"
                 ],
                 "Issues": []
               },
               {
                 "Type": "VirtualNetwork",
                 "Id": "760182e1-c88d-4cfc-a711-65e7e622a67a",
                 "Address": "10.1.4.4",
                 "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/VarunRgCentralUSEUAP
         /providers/Microsoft.Network/networkInterfaces/dbNic0/ipConfigurations/ipconfig1",
                 "NextHopIds": [],
                 "Issues": []
               }
             ]
           }
         ]

```

<span data-ttu-id="d53fd-114">I det här exemplet frågar vi de senaste anslutnings lägena för den angivna anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="d53fd-114">In this example we query the most recent connection states of the specified connection monitor.</span></span>

## <span data-ttu-id="d53fd-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d53fd-115">PARAMETERS</span></span>

### <span data-ttu-id="d53fd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d53fd-116">-AsJob</span></span>
<span data-ttu-id="d53fd-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d53fd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d53fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d53fd-118">-DefaultProfile</span></span>
<span data-ttu-id="d53fd-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d53fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d53fd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d53fd-120">-InputObject</span></span>
<span data-ttu-id="d53fd-121">Objekt för anslutnings övervakning.</span><span class="sxs-lookup"><span data-stu-id="d53fd-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="d53fd-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="d53fd-122">-Location</span></span>
<span data-ttu-id="d53fd-123">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="d53fd-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d53fd-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="d53fd-124">-Name</span></span>
<span data-ttu-id="d53fd-125">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="d53fd-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="d53fd-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d53fd-126">-NetworkWatcher</span></span>
<span data-ttu-id="d53fd-127">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="d53fd-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="d53fd-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d53fd-128">-NetworkWatcherName</span></span>
<span data-ttu-id="d53fd-129">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="d53fd-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="d53fd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d53fd-130">-ResourceGroupName</span></span>
<span data-ttu-id="d53fd-131">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d53fd-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d53fd-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d53fd-132">-ResourceId</span></span>
<span data-ttu-id="d53fd-133">Resurs-ID för anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="d53fd-133">Resource ID of the connection monitor.</span></span>

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

## <span data-ttu-id="d53fd-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d53fd-134">INPUTS</span></span>

### <span data-ttu-id="d53fd-135">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d53fd-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d53fd-136">System. String Microsoft. Azure. commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="d53fd-136">System.String Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="d53fd-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d53fd-137">OUTPUTS</span></span>

### <span data-ttu-id="d53fd-138">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorQueryResult</span><span class="sxs-lookup"><span data-stu-id="d53fd-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorQueryResult</span></span>


## <span data-ttu-id="d53fd-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d53fd-139">NOTES</span></span>
<span data-ttu-id="d53fd-140">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="d53fd-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="d53fd-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d53fd-141">RELATED LINKS</span></span>
<span data-ttu-id="d53fd-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="d53fd-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="d53fd-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="d53fd-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="d53fd-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="d53fd-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="d53fd-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span><span class="sxs-lookup"><span data-stu-id="d53fd-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)</span></span>

