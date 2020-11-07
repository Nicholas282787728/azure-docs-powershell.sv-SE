---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTopology.md
ms.openlocfilehash: e52c2a3080954e94d1610a7553331f93b3b0b58a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755998"
---
# <span data-ttu-id="ecf59-101">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ecf59-101">Get-AzureRmNetworkWatcherTopology</span></span>

## <span data-ttu-id="ecf59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ecf59-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf59-103">Hämtar en nätverks nivå över resurser och deras relationer i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ecf59-103">Gets a network level view of resources and their relationships in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecf59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ecf59-104">SYNTAX</span></span>

### <span data-ttu-id="ecf59-105">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="ecf59-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTopology -NetworkWatcher <PSNetworkWatcher> -TargetResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecf59-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ecf59-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTopology -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecf59-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ecf59-107">DESCRIPTION</span></span>
<span data-ttu-id="ecf59-108">Get-AzureRmNetworkWatcherTopology cmdlet en nätverks nivå med resurser och deras relationer i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ecf59-108">The Get-AzureRmNetworkWatcherTopology cmdlet a network level view of resources and their relationships in a resource group.</span></span> <span data-ttu-id="ecf59-109">OBS! om resurser från flera regioner lagras i resurs gruppen är det bara resurserna i samma område som nätverks Watchen som visas i JSON-utdata.</span><span class="sxs-lookup"><span data-stu-id="ecf59-109">Note: If resources from multiple regions reside in the resource group, only the resources in the same region as the Network Watcher will be included in the JSON output.</span></span>

## <span data-ttu-id="ecf59-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ecf59-110">EXAMPLES</span></span>

### <span data-ttu-id="ecf59-111">--------------------------Exempel 1: skaffa en Azure-topologi--------------------------</span><span class="sxs-lookup"><span data-stu-id="ecf59-111">--------------------------  Example 1: Get an Azure Topology  --------------------------</span></span>
```
$networkWatcher = Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG 
Get-AzureRmNetworkWatcherTopology -NetworkWatcher $networkWatcher -ResourceGroupName testresourcegroup

Id                : e33d80cf-4f76-4b8f-b51c-5bb8eba80103
CreatedDateTime   : 0/00/0000 9:21:51 PM
LastModified      : 0/00/0000 4:53:29 AM
TopologyResources : [
                      {
                        "Name": "testresourcegroup-vnet",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "vm0131",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "VM0",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Compute/virtualMachines/VM0",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-nsg",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "default",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/virtualNetworks/testresourcegroup-vnet/subnets/default",
                            "AssociationType": "Associated"
                          },
                          {
                            "Name": "VM0-ip",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                            "AssociationType": "Associated"
                          }
                        ]
                      },
                      {
                        "Name": "VM0-nsg",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "default-allow-rdp",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                            "AssociationType": "Contains"
                          }
                        ]
                      },
                      {
                        "Name": "default-allow-rdp",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkSecurityGroups/VM0-nsg/securityRules/default-allow-rdp",
                        "Location": "westcentralus",
                        "TopologyAssociations": []
                      },
                      {
                        "Name": "VM0-ip",
                        "Id": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/publicIPAddresses/VM0-ip",
                        "Location": "westcentralus",
                        "TopologyAssociations": [
                          {
                            "Name": "vm0131",
                            "ResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/testresourcegroup/providers/Microsoft.Network/networkInterfaces/vm0131",
                            "AssociationType": "Associated"
                          }
                        ]
                      }
                    ]
```

<span data-ttu-id="ecf59-112">I det här exemplet kör vi Get-AzureRmNetworkWatcherTopology cmdlet för en resurs grupp som innehåller en VM, NIC, NSG och offentlig IP.</span><span class="sxs-lookup"><span data-stu-id="ecf59-112">In this example we run the Get-AzureRmNetworkWatcherTopology cmdlet on a resource group that contains a VM, Nic, NSG, and public IP.</span></span>

## <span data-ttu-id="ecf59-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ecf59-113">PARAMETERS</span></span>

### <span data-ttu-id="ecf59-114">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ecf59-114">-NetworkWatcher</span></span>
<span data-ttu-id="ecf59-115">Nätverks bevaknings resursen.</span><span class="sxs-lookup"><span data-stu-id="ecf59-115">The network watcher resource.</span></span>

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

### <span data-ttu-id="ecf59-116">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ecf59-116">-NetworkWatcherName</span></span>
<span data-ttu-id="ecf59-117">Nätverks Bevakningens namn.</span><span class="sxs-lookup"><span data-stu-id="ecf59-117">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf59-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf59-118">-ResourceGroupName</span></span>
<span data-ttu-id="ecf59-119">Namnet på nätverks bevaknings resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ecf59-119">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf59-120">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf59-120">-TargetResourceGroupName</span></span>
<span data-ttu-id="ecf59-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="ecf59-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf59-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf59-122">-DefaultProfile</span></span>
<span data-ttu-id="ecf59-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf59-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf59-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf59-124">CommonParameters</span></span>
<span data-ttu-id="ecf59-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecf59-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf59-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf59-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf59-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ecf59-127">INPUTS</span></span>

### <span data-ttu-id="ecf59-128">Microsoft. Azure. commands. Networks. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ecf59-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ecf59-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ecf59-129">System.String</span></span>

## <span data-ttu-id="ecf59-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ecf59-130">OUTPUTS</span></span>

### <span data-ttu-id="ecf59-131">Microsoft. Azure. commands. Networks. Models. PSTopology</span><span class="sxs-lookup"><span data-stu-id="ecf59-131">Microsoft.Azure.Commands.Network.Models.PSTopology</span></span>

## <span data-ttu-id="ecf59-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ecf59-132">NOTES</span></span>
<span data-ttu-id="ecf59-133">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, nätverk, nätverk, nätverks bevakning, topologi, vy</span><span class="sxs-lookup"><span data-stu-id="ecf59-133">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, topology, view</span></span> 

## <span data-ttu-id="ecf59-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ecf59-134">RELATED LINKS</span></span>

[<span data-ttu-id="ecf59-135">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ecf59-135">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ecf59-136">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ecf59-136">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ecf59-137">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ecf59-137">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ecf59-138">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ecf59-138">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ecf59-139">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ecf59-139">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ecf59-140">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ecf59-140">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ecf59-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ecf59-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ecf59-142">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ecf59-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ecf59-143">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ecf59-143">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ecf59-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ecf59-144">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ecf59-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ecf59-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ecf59-146">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ecf59-146">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

