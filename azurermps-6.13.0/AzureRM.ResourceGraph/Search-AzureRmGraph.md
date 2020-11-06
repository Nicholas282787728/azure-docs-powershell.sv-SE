---
external help file: Microsoft.Azure.Commands.ResourceGraph.dll-Help.xml
Module Name: AzureRM.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resourcegraph/search-azurermgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ResourceGraph/Commands.ResourceGraph/help/Search-AzureRmGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ResourceGraph/Commands.ResourceGraph/help/Search-AzureRmGraph.md
ms.openlocfilehash: 900722c15d1c7a6560ba1f498b9dd0d3981f899a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580723"
---
# <span data-ttu-id="016ad-101">Search-AzureRmGraph</span><span class="sxs-lookup"><span data-stu-id="016ad-101">Search-AzureRmGraph</span></span>

## <span data-ttu-id="016ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="016ad-102">SYNOPSIS</span></span>
<span data-ttu-id="016ad-103">Frågar resurserna som hanteras av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="016ad-103">Queries the resources managed by Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="016ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="016ad-104">SYNTAX</span></span>

```
Search-AzureRmGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="016ad-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="016ad-105">DESCRIPTION</span></span>
<span data-ttu-id="016ad-106">Läs mer om frågesyntaxen här: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="016ad-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="016ad-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="016ad-107">EXAMPLES</span></span>

### <span data-ttu-id="016ad-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="016ad-108">Example 1</span></span>
```powershell
PS C:\> Search-AzureRmGraph "project id, name, type, location, tags" -First 3


id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.Compute/virtualMachineScaleSets/nt
name       : nt
type       : microsoft.compute/virtualmachinescalesets
location   : eastus
tags       : @{resourceType=Service Fabric; clusterName=gov-art-int-nt-a}

id         : /subscriptions/1ef51df4-f8a9-4b69-9919-1ef51df4eff6/resourceGroups/Service-INT-a/providers/Microsoft.EventGrid/topics/egtopic-1
name       : egtopic-1
type       : microsoft.eventgrid/topics
location   : westus2
tags       :
```

<span data-ttu-id="016ad-109">Enkla resurs frågor begär en delmängd av resurs fälten.</span><span class="sxs-lookup"><span data-stu-id="016ad-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="016ad-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="016ad-110">Example 2</span></span>
```powershell
PS C:\> Search-AzureRmGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="016ad-111">En komplex fråga om resurser med val av fält, filtrering och sammanställning.</span><span class="sxs-lookup"><span data-stu-id="016ad-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

## <span data-ttu-id="016ad-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="016ad-112">PARAMETERS</span></span>

### <span data-ttu-id="016ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="016ad-113">-DefaultProfile</span></span>
<span data-ttu-id="016ad-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="016ad-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="016ad-115">-Fråga</span><span class="sxs-lookup"><span data-stu-id="016ad-115">-Query</span></span>
<span data-ttu-id="016ad-116">Resurs diagram fråga.</span><span class="sxs-lookup"><span data-stu-id="016ad-116">Resource Graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016ad-117">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="016ad-117">-Subscription</span></span>
<span data-ttu-id="016ad-118">Abonnemang som du vill köra frågan mot.</span><span class="sxs-lookup"><span data-stu-id="016ad-118">Subscription(s) to run query against.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016ad-119">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="016ad-119">-Skip</span></span>
<span data-ttu-id="016ad-120">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="016ad-120">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016ad-121">-Först</span><span class="sxs-lookup"><span data-stu-id="016ad-121">-First</span></span>
<span data-ttu-id="016ad-122">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="016ad-122">The maximum number of objects to return.</span></span> <span data-ttu-id="016ad-123">Tillåtna värden: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="016ad-123">Allowed values: 1-5000.</span></span>
<span data-ttu-id="016ad-124">Standardvärdet är 100.</span><span class="sxs-lookup"><span data-stu-id="016ad-124">Default value is 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="016ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="016ad-125">CommonParameters</span></span>
<span data-ttu-id="016ad-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="016ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="016ad-127">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="016ad-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="016ad-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="016ad-128">INPUTS</span></span>

### <span data-ttu-id="016ad-129">System. String</span><span class="sxs-lookup"><span data-stu-id="016ad-129">System.String</span></span>

## <span data-ttu-id="016ad-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="016ad-130">OUTPUTS</span></span>

### <span data-ttu-id="016ad-131">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="016ad-131">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="016ad-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="016ad-132">NOTES</span></span>

## <span data-ttu-id="016ad-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="016ad-133">RELATED LINKS</span></span>
