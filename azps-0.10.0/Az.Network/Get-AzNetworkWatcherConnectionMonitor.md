---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: d8ab2ce24db9c6ab07989dc5a4a45b8bfca8fc78
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93922245"
---
# <span data-ttu-id="bd10e-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="bd10e-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="bd10e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd10e-102">SYNOPSIS</span></span>
<span data-ttu-id="bd10e-103">Returnerar anslutnings övervakning med angivet namn eller listan över anslutnings bildskärmar</span><span class="sxs-lookup"><span data-stu-id="bd10e-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="bd10e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd10e-104">SYNTAX</span></span>

### <span data-ttu-id="bd10e-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="bd10e-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="bd10e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bd10e-106">SetByName</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="bd10e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="bd10e-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="bd10e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bd10e-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="bd10e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd10e-109">DESCRIPTION</span></span>
<span data-ttu-id="bd10e-110">Den Get-AzNetworkWatcherConnectionMonitor cmdleten returnerar anslutnings övervakaren med angivet namn/resourceId eller listan över anslutnings skärmar som motsvarar den angivna nätverks övervakaren/platsen.</span><span class="sxs-lookup"><span data-stu-id="bd10e-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="bd10e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd10e-111">EXAMPLES</span></span>

### <span data-ttu-id="bd10e-112">---------------Exempel 1: hämta anslutnings övervakaren efter namn på den angivna platsen---------------</span><span class="sxs-lookup"><span data-stu-id="bd10e-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


Name                        : cm
Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro
                              ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher
                              s/NetworkWatcher_centraluseuap/connectionMonitors/cm
Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095"
ProvisioningState           : Succeeded
Source                      : {
                                "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6
                              a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C
                              ompute/virtualMachines/irinavm",
                                "Port": 0
                              }
Destination                 : {
                                "Address": "google.com",
                                "Port": 80
                              }
MonitoringIntervalInSeconds : 60
AutoStart                   : True
StartTime                   : 1/12/2018 7:19:28 PM
MonitoringStatus            : Stopped
Location                    : centraluseuap
Type                        : Microsoft.Network/networkWatchers/connectionMonitors
Tags                        : {
                                "key1": "value1"
                              }
```

<span data-ttu-id="bd10e-113">I det här exemplet får vi anslutnings övervakarens namn på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="bd10e-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="bd10e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd10e-114">PARAMETERS</span></span>

### <span data-ttu-id="bd10e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd10e-115">-AsJob</span></span>
<span data-ttu-id="bd10e-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bd10e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd10e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd10e-117">-DefaultProfile</span></span>
<span data-ttu-id="bd10e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd10e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd10e-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="bd10e-119">-Location</span></span>
<span data-ttu-id="bd10e-120">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="bd10e-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="bd10e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd10e-121">-Name</span></span>
<span data-ttu-id="bd10e-122">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="bd10e-122">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd10e-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd10e-123">-NetworkWatcher</span></span>
<span data-ttu-id="bd10e-124">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="bd10e-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="bd10e-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bd10e-125">-NetworkWatcherName</span></span>
<span data-ttu-id="bd10e-126">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="bd10e-126">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd10e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd10e-127">-ResourceGroupName</span></span>
<span data-ttu-id="bd10e-128">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bd10e-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bd10e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd10e-129">-ResourceId</span></span>
<span data-ttu-id="bd10e-130">Resurs-ID för anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="bd10e-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="bd10e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd10e-131">CommonParameters</span></span>
<span data-ttu-id="bd10e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd10e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd10e-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd10e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd10e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd10e-134">INPUTS</span></span>

### <span data-ttu-id="bd10e-135">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bd10e-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="bd10e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bd10e-136">System.String</span></span>


## <span data-ttu-id="bd10e-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd10e-137">OUTPUTS</span></span>

### <span data-ttu-id="bd10e-138">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="bd10e-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="bd10e-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd10e-139">NOTES</span></span>
<span data-ttu-id="bd10e-140">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="bd10e-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="bd10e-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd10e-141">RELATED LINKS</span></span>
<span data-ttu-id="bd10e-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md) 
 [Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md) 
 [Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="bd10e-142">[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)
[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)
[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)</span></span>

<span data-ttu-id="bd10e-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md) 
 [Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md) 
 [Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md) 
 [Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="bd10e-143">[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)
[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)
[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)
[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="bd10e-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md) 
 [New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md) 
 [Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md) 
 [Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md) 
 [Stopp-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="bd10e-144">[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)
[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)
[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)
[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)
[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="bd10e-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md) 
 [Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="bd10e-145">[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)
[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)</span></span>