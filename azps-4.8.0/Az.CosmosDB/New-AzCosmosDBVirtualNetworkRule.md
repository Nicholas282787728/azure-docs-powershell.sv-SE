---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260105"
---
# <span data-ttu-id="239e9-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="239e9-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="239e9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="239e9-102">SYNOPSIS</span></span>
<span data-ttu-id="239e9-103">Skapa ett nytt CosmosDB VirtualNetworkRule-objekt (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="239e9-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="239e9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="239e9-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="239e9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="239e9-105">DESCRIPTION</span></span>
<span data-ttu-id="239e9-106">Skapa ett nytt CosmosDB VirtualNetworkRule-objekt (PSVirtualNetworkRule).</span><span class="sxs-lookup"><span data-stu-id="239e9-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="239e9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="239e9-107">EXAMPLES</span></span>

### <span data-ttu-id="239e9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="239e9-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="239e9-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="239e9-109">PARAMETERS</span></span>

### <span data-ttu-id="239e9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="239e9-110">-DefaultProfile</span></span>
<span data-ttu-id="239e9-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="239e9-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239e9-112">-ID</span><span class="sxs-lookup"><span data-stu-id="239e9-112">-Id</span></span>
<span data-ttu-id="239e9-113">Resurs-ID för ett undernät, till exempel:/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="239e9-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="239e9-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="239e9-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="239e9-115">Boolean för att ange om du vill skapa en brand Väggs regel innan slut punkts tjänsten för virtuellt nätverk har Aktiver ATS.</span><span class="sxs-lookup"><span data-stu-id="239e9-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="239e9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="239e9-116">CommonParameters</span></span>
<span data-ttu-id="239e9-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="239e9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="239e9-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="239e9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="239e9-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="239e9-119">INPUTS</span></span>

### <span data-ttu-id="239e9-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="239e9-120">None</span></span>

## <span data-ttu-id="239e9-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="239e9-121">OUTPUTS</span></span>

### <span data-ttu-id="239e9-122">Microsoft. Azure. commands. CosmosDB. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="239e9-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="239e9-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="239e9-123">NOTES</span></span>

## <span data-ttu-id="239e9-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="239e9-124">RELATED LINKS</span></span>
