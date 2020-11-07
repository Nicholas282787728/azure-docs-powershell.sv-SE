---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a68604e9701a6ae2c251edf3f2a0935df5ffa94f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916162"
---
# <span data-ttu-id="83f38-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="83f38-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="83f38-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="83f38-102">SYNOPSIS</span></span>
<span data-ttu-id="83f38-103">Lista alla Kusto-kluster i en resurs grupp eller skaffa ett visst Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="83f38-103">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="83f38-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="83f38-104">SYNTAX</span></span>

### <span data-ttu-id="83f38-105">ByClusterOrResourceGroupOrSubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="83f38-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="83f38-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="83f38-106">ByResourceId</span></span>
```
Get-AzKustoCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83f38-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="83f38-107">DESCRIPTION</span></span>
<span data-ttu-id="83f38-108">Lista alla Kusto-kluster i en resurs grupp eller skaffa ett visst Kusto-kluster.</span><span class="sxs-lookup"><span data-stu-id="83f38-108">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

## <span data-ttu-id="83f38-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="83f38-109">EXAMPLES</span></span>

### <span data-ttu-id="83f38-110">Exempel 1 – lista alla Kusto-kluster i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="83f38-110">Example 1 - List all Kusto clusters in a resource group</span></span>

<span data-ttu-id="83f38-111">Skriv: Microsoft. Kusto/kluster-ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup: testrg namn: mykustocluster1 plats: Central USA-kapacitet: 3 SKU: D13_v2 ProvisioningState: lyckades: kör tagg: {} URI: https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster1.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="83f38-111">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster1 ResourceGroup     : testrg Name              : mykustocluster1 Location          : Central US Capacity          : 3 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster1.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net</span></span>

<span data-ttu-id="83f38-112">Skriv: Microsoft. Kusto/kluster-ID:/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup: testrg namn: mykustocluster2 plats: Central USA-kapacitet: 5 SKU: D13_v2 ProvisioningState: lyckades: kör tagg: {} URI: https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri: https://ingest-mykustocluster2.centralus.kusto.windows.net</span><span class="sxs-lookup"><span data-stu-id="83f38-112">Type              : Microsoft.Kusto/Clusters Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster2 ResourceGroup     : testrg Name              : mykustocluster2 Location          : Central US Capacity          : 5 Sku               : D13_v2 ProvisioningState : Succeeded State             : Running Tag               : {} Uri               : https://mykustocluster2.centralus.kusto.windows.net DataIngestionUri  : https://ingest-mykustocluster2.centralus.kusto.windows.net</span></span>


```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg
```

<span data-ttu-id="83f38-113">Kommandot ovan visar alla Kusto-kluster i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="83f38-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="83f38-114">Exempel 2 – få ett specifikt Kusto-kluster med namn</span><span class="sxs-lookup"><span data-stu-id="83f38-114">Example 2 - Get a specific Kusto cluster by name</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="83f38-115">Kommandot ovan returnerar Kusto-klustret med namnet "mykustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="83f38-115">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

### <span data-ttu-id="83f38-116">Exempel 3 – skaffa ett specifikt Kusto-kluster efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="83f38-116">Example 3 - Get a specific Kusto cluster by resource id</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/clusters/mykustocluster
Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 5
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="83f38-117">Kommandot ovan returnerar Kusto-klustret med namnet "mykustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="83f38-117">The above command returns the Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="83f38-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="83f38-118">PARAMETERS</span></span>

### <span data-ttu-id="83f38-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f38-119">-DefaultProfile</span></span>
<span data-ttu-id="83f38-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="83f38-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83f38-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="83f38-121">-Name</span></span>
<span data-ttu-id="83f38-122">Namn på ett specifikt kluster.</span><span class="sxs-lookup"><span data-stu-id="83f38-122">Name of a specific cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f38-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f38-123">-ResourceGroupName</span></span>
<span data-ttu-id="83f38-124">Namnet på den resurs grupp som användaren vill hämta klustret under.</span><span class="sxs-lookup"><span data-stu-id="83f38-124">Name of resource group under which the user wants to retrieve the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByClusterOrResourceGroupOrSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83f38-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83f38-125">-ResourceId</span></span>
<span data-ttu-id="83f38-126">Kusto-kluster-ResourceID.</span><span class="sxs-lookup"><span data-stu-id="83f38-126">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83f38-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f38-127">CommonParameters</span></span>
<span data-ttu-id="83f38-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83f38-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f38-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83f38-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f38-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="83f38-130">INPUTS</span></span>

### <span data-ttu-id="83f38-131">System. String</span><span class="sxs-lookup"><span data-stu-id="83f38-131">System.String</span></span>

## <span data-ttu-id="83f38-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="83f38-132">OUTPUTS</span></span>

### <span data-ttu-id="83f38-133">Microsoft. Azure. commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="83f38-133">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="83f38-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="83f38-134">NOTES</span></span>

## <span data-ttu-id="83f38-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="83f38-135">RELATED LINKS</span></span>
