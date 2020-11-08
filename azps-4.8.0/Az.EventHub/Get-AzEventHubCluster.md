---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubCluster.md
ms.openlocfilehash: 4e2657d6a4af26b96a2e7a97a56b735838610005
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262261"
---
# <span data-ttu-id="15a2a-101">Get-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="15a2a-101">Get-AzEventHubCluster</span></span>

## <span data-ttu-id="15a2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="15a2a-103">Hämtar information om ett enskilt nav-kluster eller hämtar en lista med kluster för händelse nav.</span><span class="sxs-lookup"><span data-stu-id="15a2a-103">Gets the details of a single Event Hub Cluster , or gets a list of Event Hub Clusters.</span></span>

## <span data-ttu-id="15a2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15a2a-104">SYNTAX</span></span>

```
Get-AzEventHubCluster [-ResourceGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15a2a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15a2a-105">DESCRIPTION</span></span>
<span data-ttu-id="15a2a-106">Med cmdleten Get-AzEventHubCluster returneras antingen information om ett kluster för händelse hubbar eller en lista över alla händelse nav kluster i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="15a2a-106">The Get-AzEventHubCluster cmdlet returns either the details of an Event Hub Cluster, or a list of all Event Hub Clusters in given resource group.</span></span>
<span data-ttu-id="15a2a-107">Om kluster namnet tillhandahålls returneras informationen om ett enskilt kluster.</span><span class="sxs-lookup"><span data-stu-id="15a2a-107">If the cluster name is provided, the details of a single cluster are returned.</span></span>
<span data-ttu-id="15a2a-108">Om inget kluster namn anges returneras en lista över alla kluster i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="15a2a-108">If an cluster name is not provided, a list of all clusters in the specified resource group is returned.</span></span>

## <span data-ttu-id="15a2a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15a2a-109">EXAMPLES</span></span>

### <span data-ttu-id="15a2a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="15a2a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557

Id        : /subscriptions/326100e2-f69d-4268-8503-075374f62b6e/resourceGroups/RSG-Cluster27651/providers/Microsoft.Eve
            ntHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/10/2020 23:02:48
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag2, Tag4], [ClusterTag1, Tag3]}

```

<span data-ttu-id="15a2a-111">Returnerar detials för klustret ' Eventhub-Cluster-5557 ' från resurs gruppen ' RSG-Cluster27651 '</span><span class="sxs-lookup"><span data-stu-id="15a2a-111">Returns the detials of cluster 'Eventhub-Cluster-5557' from the resource group 'RSG-Cluster27651'</span></span>

## <span data-ttu-id="15a2a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15a2a-112">PARAMETERS</span></span>

### <span data-ttu-id="15a2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a2a-113">-DefaultProfile</span></span>
<span data-ttu-id="15a2a-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="15a2a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a2a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="15a2a-115">-Name</span></span>
<span data-ttu-id="15a2a-116">Kluster namn</span><span class="sxs-lookup"><span data-stu-id="15a2a-116">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a2a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a2a-117">-ResourceGroupName</span></span>
<span data-ttu-id="15a2a-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="15a2a-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a2a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a2a-119">CommonParameters</span></span>
<span data-ttu-id="15a2a-120">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a2a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a2a-121">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15a2a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a2a-122">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15a2a-122">INPUTS</span></span>

### <span data-ttu-id="15a2a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="15a2a-123">System.String</span></span>

## <span data-ttu-id="15a2a-124">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15a2a-124">OUTPUTS</span></span>

### <span data-ttu-id="15a2a-125">Microsoft. Azure. commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="15a2a-125">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="15a2a-126">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15a2a-126">NOTES</span></span>

## <span data-ttu-id="15a2a-127">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15a2a-127">RELATED LINKS</span></span>
