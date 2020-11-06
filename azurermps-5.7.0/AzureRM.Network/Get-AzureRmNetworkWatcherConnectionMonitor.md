---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: a78114bbf47113983453a0dd5c1e13db0fc73a6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574921"
---
# <span data-ttu-id="74e3b-101">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74e3b-101">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="74e3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="74e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="74e3b-103">Returnerar anslutnings övervakning med angivet namn eller listan över anslutnings bildskärmar</span><span class="sxs-lookup"><span data-stu-id="74e3b-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74e3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="74e3b-104">SYNTAX</span></span>

### <span data-ttu-id="74e3b-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="74e3b-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74e3b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="74e3b-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74e3b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="74e3b-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74e3b-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="74e3b-108">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74e3b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="74e3b-109">DESCRIPTION</span></span>
<span data-ttu-id="74e3b-110">Den Get-AzureRmNetworkWatcherConnectionMonitor cmdleten returnerar anslutnings övervakaren med angivet namn/resourceId eller listan över anslutnings skärmar som motsvarar den angivna nätverks övervakaren/platsen.</span><span class="sxs-lookup"><span data-stu-id="74e3b-110">The Get-AzureRmNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="74e3b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="74e3b-111">EXAMPLES</span></span>

### <span data-ttu-id="74e3b-112">Exempel 1: hämta anslutnings övervakare efter namn på den angivna platsen</span><span class="sxs-lookup"><span data-stu-id="74e3b-112">Example 1: Get connection monitor by name in the specified location</span></span>
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

<span data-ttu-id="74e3b-113">I det här exemplet får vi anslutnings övervakarens namn på den angivna platsen.</span><span class="sxs-lookup"><span data-stu-id="74e3b-113">In this example we get connection monitor by name in the specified location.</span></span>

## <span data-ttu-id="74e3b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="74e3b-114">PARAMETERS</span></span>

### <span data-ttu-id="74e3b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e3b-115">-DefaultProfile</span></span>
<span data-ttu-id="74e3b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="74e3b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74e3b-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="74e3b-117">-Location</span></span>
<span data-ttu-id="74e3b-118">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="74e3b-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="74e3b-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="74e3b-119">-Name</span></span>
<span data-ttu-id="74e3b-120">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="74e3b-120">The connection monitor name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e3b-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74e3b-121">-NetworkWatcher</span></span>
<span data-ttu-id="74e3b-122">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="74e3b-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="74e3b-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="74e3b-123">-NetworkWatcherName</span></span>
<span data-ttu-id="74e3b-124">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="74e3b-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="74e3b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74e3b-125">-ResourceGroupName</span></span>
<span data-ttu-id="74e3b-126">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="74e3b-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="74e3b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74e3b-127">-ResourceId</span></span>
<span data-ttu-id="74e3b-128">Resurs-ID för anslutnings övervakaren.</span><span class="sxs-lookup"><span data-stu-id="74e3b-128">Resource ID of the connection monitor.</span></span>

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

### <span data-ttu-id="74e3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e3b-129">CommonParameters</span></span>
<span data-ttu-id="74e3b-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74e3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="74e3b-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74e3b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e3b-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="74e3b-132">INPUTS</span></span>

### <span data-ttu-id="74e3b-133">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74e3b-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="74e3b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="74e3b-134">System.String</span></span>

## <span data-ttu-id="74e3b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="74e3b-135">OUTPUTS</span></span>

### <span data-ttu-id="74e3b-136">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="74e3b-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>

## <span data-ttu-id="74e3b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="74e3b-137">NOTES</span></span>
<span data-ttu-id="74e3b-138">Nyckelord: Azure, azurerm, arm, resurs, anslutning, hantering, chef, nätverk, nätverk, nätverks bevakning, anslutnings övervakning</span><span class="sxs-lookup"><span data-stu-id="74e3b-138">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="74e3b-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="74e3b-139">RELATED LINKS</span></span>

[<span data-ttu-id="74e3b-140">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74e3b-140">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="74e3b-141">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74e3b-141">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="74e3b-142">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="74e3b-142">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="74e3b-143">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="74e3b-143">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="74e3b-144">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="74e3b-144">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="74e3b-145">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="74e3b-145">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="74e3b-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="74e3b-146">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="74e3b-147">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74e3b-147">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="74e3b-148">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="74e3b-148">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="74e3b-149">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74e3b-149">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="74e3b-150">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74e3b-150">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="74e3b-151">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="74e3b-151">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="74e3b-152">New-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74e3b-152">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="74e3b-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="74e3b-153">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="74e3b-154">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74e3b-154">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="74e3b-155">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74e3b-155">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="74e3b-156">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74e3b-156">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="74e3b-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="74e3b-157">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()
