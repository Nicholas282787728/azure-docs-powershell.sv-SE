---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.dll-Help.xml
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/search-azgraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Search-AzGraph.md
ms.openlocfilehash: e1d9aa5c9bf2538f20d37a23b35dec4d7a850cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271705"
---
# <span data-ttu-id="fddc5-101">Search-AzGraph</span><span class="sxs-lookup"><span data-stu-id="fddc5-101">Search-AzGraph</span></span>

## <span data-ttu-id="fddc5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fddc5-102">SYNOPSIS</span></span>
<span data-ttu-id="fddc5-103">Frågar resurserna som hanteras av Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="fddc5-103">Queries the resources managed by Azure Resource Manager.</span></span>

## <span data-ttu-id="fddc5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fddc5-104">SYNTAX</span></span>

```
Search-AzGraph [-Query] <String> [-Subscription <String[]>] [-First <Int32>] [-Skip <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fddc5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fddc5-105">DESCRIPTION</span></span>
<span data-ttu-id="fddc5-106">Läs mer om frågesyntaxen här: https://aka.ms/resource-graph/learntoquery</span><span class="sxs-lookup"><span data-stu-id="fddc5-106">Learn more about the query syntax here: https://aka.ms/resource-graph/learntoquery</span></span>

## <span data-ttu-id="fddc5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fddc5-107">EXAMPLES</span></span>

### <span data-ttu-id="fddc5-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fddc5-108">Example 1</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location, tags" -First 3


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

<span data-ttu-id="fddc5-109">Enkla resurs frågor begär en delmängd av resurs fälten.</span><span class="sxs-lookup"><span data-stu-id="fddc5-109">Simple resources query requesting a subset of resource fields.</span></span>

### <span data-ttu-id="fddc5-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="fddc5-110">Example 2</span></span>
```powershell
PS C:\> Search-AzGraph "project id, name, type, location | where type =~ 'Microsoft.Compute/virtualMachines' | summarize count() by location | top 3 by count_"

location      count_
--------      ------
eastus            66
westcentralus     32
westus            26
```

<span data-ttu-id="fddc5-111">En komplex fråga om resurser med val av fält, filtrering och sammanställning.</span><span class="sxs-lookup"><span data-stu-id="fddc5-111">A complex query on resources featuring field selection, filtering and summarizing.</span></span>

### <span data-ttu-id="fddc5-112">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="fddc5-112">Example 3</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'where type =~ "Microsoft.Compute/virtualMachines"| where properties.storageProfile.osDisk.managedDisk == "" | project name, resourceGroup, subscriptionDisplayName'

name         resourceGroup      subscriptionDisplayName
----         -------------      -----------------------
ContosoVM    RG-Contoso         Contoso Production Subscription                                               

```
<span data-ttu-id="fddc5-113">En fråga med alla virtuella datorer som inte använder hanterade diskar och som innehåller visnings namn för abonnemang.</span><span class="sxs-lookup"><span data-stu-id="fddc5-113">A query featuring all virtual machines which are not using Managed Disks and includes subscription display names.</span></span>

### <span data-ttu-id="fddc5-114">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="fddc5-114">Example 4</span></span>
```powershell
PS C:\> Search-AzGraph -Include DisplayName -Query 'summarize count() by tenantDisplayName, subscriptionDisplayName'

tenantDisplayName   subscriptionDisplayName              count_
-----------------   -----------------------              ------
ContosoTenant       Contoso Production Subscription      118                                           
```
<span data-ttu-id="fddc5-115">En fråga som visar antalet resurser efter visnings namn för klient och abonnemang.</span><span class="sxs-lookup"><span data-stu-id="fddc5-115">A query displaying the count of resources by tenant and subscription display names.</span></span>

## <span data-ttu-id="fddc5-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fddc5-116">PARAMETERS</span></span>

### <span data-ttu-id="fddc5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddc5-117">-DefaultProfile</span></span>
<span data-ttu-id="fddc5-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fddc5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fddc5-119">-Fråga</span><span class="sxs-lookup"><span data-stu-id="fddc5-119">-Query</span></span>
<span data-ttu-id="fddc5-120">Resurs diagram fråga.</span><span class="sxs-lookup"><span data-stu-id="fddc5-120">Resource Graph query.</span></span>

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

### <span data-ttu-id="fddc5-121">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="fddc5-121">-Subscription</span></span>
<span data-ttu-id="fddc5-122">Abonnemang som du vill köra frågan mot.</span><span class="sxs-lookup"><span data-stu-id="fddc5-122">Subscription(s) to run query against.</span></span>

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

### <span data-ttu-id="fddc5-123">-Hoppa över</span><span class="sxs-lookup"><span data-stu-id="fddc5-123">-Skip</span></span>
<span data-ttu-id="fddc5-124">Ignorerar de första N objekten och hämtar sedan återstående objekt.</span><span class="sxs-lookup"><span data-stu-id="fddc5-124">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="fddc5-125">-Först</span><span class="sxs-lookup"><span data-stu-id="fddc5-125">-First</span></span>
<span data-ttu-id="fddc5-126">Det maximala antalet objekt som ska returneras.</span><span class="sxs-lookup"><span data-stu-id="fddc5-126">The maximum number of objects to return.</span></span> <span data-ttu-id="fddc5-127">Tillåtna värden: 1-5000.</span><span class="sxs-lookup"><span data-stu-id="fddc5-127">Allowed values: 1-5000.</span></span>
<span data-ttu-id="fddc5-128">Standardvärdet är 100.</span><span class="sxs-lookup"><span data-stu-id="fddc5-128">Default value is 100.</span></span>

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

### <span data-ttu-id="fddc5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fddc5-129">CommonParameters</span></span>
<span data-ttu-id="fddc5-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fddc5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fddc5-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fddc5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fddc5-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fddc5-132">INPUTS</span></span>

### <span data-ttu-id="fddc5-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="fddc5-133">None</span></span>

## <span data-ttu-id="fddc5-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fddc5-134">OUTPUTS</span></span>

### <span data-ttu-id="fddc5-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="fddc5-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="fddc5-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fddc5-136">NOTES</span></span>

## <span data-ttu-id="fddc5-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fddc5-137">RELATED LINKS</span></span>