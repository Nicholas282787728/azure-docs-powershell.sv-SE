---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 014942f38abf0caae01463d07343b5ad473a24d7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929362"
---
# <span data-ttu-id="cf74b-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cf74b-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="cf74b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf74b-102">SYNOPSIS</span></span>
<span data-ttu-id="cf74b-103">Returnerar anslutnings övervakning med angivet namn eller listan över anslutnings bildskärmar</span><span class="sxs-lookup"><span data-stu-id="cf74b-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf74b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf74b-104">SYNTAX</span></span>

### <span data-ttu-id="cf74b-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="cf74b-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="cf74b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cf74b-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="cf74b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cf74b-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="cf74b-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf74b-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="cf74b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf74b-109">DESCRIPTION</span></span>
<span data-ttu-id="cf74b-110">Den Get-AzureRmNetworkWatcherConnectionMonitor cmdleten returnerar anslutnings övervakaren med angivet namn/resourceId eller listan över anslutnings skärmar som motsvarar den angivna nätverks övervakaren/platsen.</span><span class="sxs-lookup"><span data-stu-id="cf74b-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="cf74b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf74b-111">EXAMPLES</span></span>

### <span data-ttu-id="cf74b-112">---------------Exempel 1: hämta anslutnings övervakaren efter namn på den angivna platsen---------------</span><span class="sxs-lookup"><span data-stu-id="cf74b-112">---------------  Example 1: Get connection monitor by name in the specified location ---------------</span></span>
```
PS C:\> Get-AzureRmNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm


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

<span data-ttu-id="cf74b-113">I det här exemplet får vi anslutnings övervakarens namn på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="cf74b-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="cf74b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf74b-114">PARAMETERS</span></span>

### <span data-ttu-id="cf74b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf74b-115">-AsJob</span></span>
<span data-ttu-id="cf74b-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cf74b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf74b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf74b-117">-DefaultProfile</span></span>
<span data-ttu-id="cf74b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cf74b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf74b-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="cf74b-119">-Location</span></span>
<span data-ttu-id="cf74b-120">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="cf74b-120">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cf74b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="cf74b-121">-Name</span></span>
<span data-ttu-id="cf74b-122">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="cf74b-122">The connection monitor name.</span></span>

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

### <span data-ttu-id="cf74b-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cf74b-123">-NetworkWatcher</span></span>
<span data-ttu-id="cf74b-124">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="cf74b-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="cf74b-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cf74b-125">-NetworkWatcherName</span></span>
<span data-ttu-id="cf74b-126">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="cf74b-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="cf74b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf74b-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf74b-128">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cf74b-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cf74b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf74b-129">-ResourceId</span></span>
<span data-ttu-id="cf74b-130">Resurs-ID för anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="cf74b-130">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="cf74b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf74b-131">CommonParameters</span></span>
<span data-ttu-id="cf74b-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf74b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf74b-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf74b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf74b-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf74b-134">INPUTS</span></span>

### <span data-ttu-id="cf74b-135">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cf74b-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="cf74b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cf74b-136">System.String</span></span>


## <span data-ttu-id="cf74b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf74b-137">OUTPUTS</span></span>

### <span data-ttu-id="cf74b-138">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="cf74b-138">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>


## <span data-ttu-id="cf74b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf74b-139">NOTES</span></span>
<span data-ttu-id="cf74b-140">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="cf74b-140">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="cf74b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf74b-141">RELATED LINKS</span></span>
<span data-ttu-id="cf74b-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md) 
 [Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md) 
 [Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span><span class="sxs-lookup"><span data-stu-id="cf74b-142">[New-AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)
[Get-AzureRmNetworkWatcher](./Get-AzureRmNetworkWatcher.md)
[Remove-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)</span></span>

<span data-ttu-id="cf74b-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md) 
 [Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md) 
 [Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md) 
 [Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span><span class="sxs-lookup"><span data-stu-id="cf74b-143">[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)
[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)
[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)
[Get-AzureRmNetworkWatcherTroubleshootingResult](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)</span></span>

<span data-ttu-id="cf74b-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md) 
 [New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md) 
 [Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md) 
 [Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md) 
 [Stopp-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span><span class="sxs-lookup"><span data-stu-id="cf74b-144">[New-AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)
[New-AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)
[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)
[Remove-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)
[Stop-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)</span></span>

<span data-ttu-id="cf74b-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md) 
 [Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span><span class="sxs-lookup"><span data-stu-id="cf74b-145">[New-AzureRmNetworkWatcherConnectionMonitor](./New-AzureRmNetworkWatcherConnectionMonitor.md)
[Get-AzureRmNetworkWatcherConnectionMonitorReport](./Get-AzureRmNetworkWatcherConnectionMonitorReport.md)</span></span>
