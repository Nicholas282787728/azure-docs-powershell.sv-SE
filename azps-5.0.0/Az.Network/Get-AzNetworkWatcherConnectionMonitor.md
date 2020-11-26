---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325890"
---
# <span data-ttu-id="1ea43-101">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1ea43-101">Get-AzNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="1ea43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1ea43-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea43-103">Returnerar anslutnings övervakning med angivet namn eller listan över anslutnings bildskärmar</span><span class="sxs-lookup"><span data-stu-id="1ea43-103">Returns connection monitor with specified name or the list of connection monitors</span></span>

## <span data-ttu-id="1ea43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1ea43-104">SYNTAX</span></span>

### <span data-ttu-id="1ea43-105">SetByName (standard)</span><span class="sxs-lookup"><span data-stu-id="1ea43-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ea43-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="1ea43-106">SetByResource</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ea43-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1ea43-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ea43-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="1ea43-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ea43-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1ea43-109">DESCRIPTION</span></span>
<span data-ttu-id="1ea43-110">Den Get-AzNetworkWatcherConnectionMonitor cmdleten returnerar anslutnings övervakaren med angivet namn/resourceId eller listan över anslutnings skärmar som motsvarar den angivna nätverks övervakaren/platsen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-110">The Get-AzNetworkWatcherConnectionMonitor cmdlet returns the connection monitor with the specified name / resourceId or the list of connection monitors corresponding to the specified network watcher / location.</span></span>

## <span data-ttu-id="1ea43-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1ea43-111">EXAMPLES</span></span>

### <span data-ttu-id="1ea43-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1ea43-112">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

<span data-ttu-id="1ea43-113">Namn: cm-ID:/subscriptions/00000000-0000-0000-0000-000000000000/resourceGro UPS/NetworkWatcherRG/providers/Microsoft. Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm etag: W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState: lyckad Källa: {"ResourceId": "/Subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft. C ompute/virtualMachines/irinavm", "Port": 0} mål: {"adress": "google.com", "Port": 80} MonitoringIntervalInSeconds: 60 Autostart: true StartTime: 1/12/2018 7:19:28 PM MonitoringStatus: stoppad plats: centraluseuap typ: Microsoft. Network/networkWatchers/connectionMonitors Taggar: {"KEY1": "värde1"}</span><span class="sxs-lookup"><span data-stu-id="1ea43-113">Name                        : cm Id                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGro ups/NetworkWatcherRG/providers/Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag                        : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState           : Succeeded Source                      : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination                 : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart                   : True StartTime                   : 1/12/2018 7:19:28 PM MonitoringStatus            : Stopped Location                    : centraluseuap Type                        : Microsoft.Network/networkWatchers/connectionMonitors Tags                        : { "key1": "value1" }</span></span>

## <span data-ttu-id="1ea43-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1ea43-114">PARAMETERS</span></span>

### <span data-ttu-id="1ea43-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea43-115">-DefaultProfile</span></span>
<span data-ttu-id="1ea43-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1ea43-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea43-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="1ea43-117">-Location</span></span>
<span data-ttu-id="1ea43-118">Nätverks Bevakningens plats.</span><span class="sxs-lookup"><span data-stu-id="1ea43-118">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1ea43-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="1ea43-119">-Name</span></span>
<span data-ttu-id="1ea43-120">Anslutnings övervakarens namn.</span><span class="sxs-lookup"><span data-stu-id="1ea43-120">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea43-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ea43-121">-NetworkWatcher</span></span>
<span data-ttu-id="1ea43-122">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="1ea43-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1ea43-123">-NetworkWatcherName</span></span>
<span data-ttu-id="1ea43-124">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="1ea43-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="1ea43-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ea43-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ea43-126">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1ea43-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1ea43-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ea43-127">-ResourceId</span></span>
<span data-ttu-id="1ea43-128">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="1ea43-128">Resource ID.</span></span>

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

### <span data-ttu-id="1ea43-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea43-129">CommonParameters</span></span>
<span data-ttu-id="1ea43-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ea43-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea43-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ea43-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea43-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1ea43-132">INPUTS</span></span>

### <span data-ttu-id="1ea43-133">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1ea43-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1ea43-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1ea43-134">System.String</span></span>

## <span data-ttu-id="1ea43-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1ea43-135">OUTPUTS</span></span>

### <span data-ttu-id="1ea43-136">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResultV1</span><span class="sxs-lookup"><span data-stu-id="1ea43-136">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1</span></span>

### <span data-ttu-id="1ea43-137">Microsoft. Azure. commands. Networks. Models. PSConnectionMonitorResultV2</span><span class="sxs-lookup"><span data-stu-id="1ea43-137">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2</span></span>

## <span data-ttu-id="1ea43-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1ea43-138">NOTES</span></span>

## <span data-ttu-id="1ea43-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1ea43-139">RELATED LINKS</span></span>