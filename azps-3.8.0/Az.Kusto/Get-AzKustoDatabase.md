---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: f78dd41283312434f8a3ea833f9c96df6527cb95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088859"
---
# <span data-ttu-id="a74f4-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="a74f4-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="a74f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a74f4-102">SYNOPSIS</span></span>
<span data-ttu-id="a74f4-103">Lista alla Kusto-databaser i ett kluster eller skaffa en specifik Kusto-databas.</span><span class="sxs-lookup"><span data-stu-id="a74f4-103">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="a74f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a74f4-104">SYNTAX</span></span>

### <span data-ttu-id="a74f4-105">ByClusterOrResourceGroupOrSubscription (standard)</span><span class="sxs-lookup"><span data-stu-id="a74f4-105">ByClusterOrResourceGroupOrSubscription (Default)</span></span>
```
Get-AzKustoDatabase -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a74f4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a74f4-106">ByResourceId</span></span>
```
Get-AzKustoDatabase [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a74f4-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a74f4-107">ByInputObject</span></span>
```
Get-AzKustoDatabase [-Name <String>] -InputObject <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a74f4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a74f4-108">DESCRIPTION</span></span>
<span data-ttu-id="a74f4-109">Lista alla Kusto-databaser i ett kluster eller skaffa en specifik Kusto-databas.</span><span class="sxs-lookup"><span data-stu-id="a74f4-109">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

## <span data-ttu-id="a74f4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a74f4-110">EXAMPLES</span></span>

### <span data-ttu-id="a74f4-111">Exempel 1 – lista alla Kusto-databaser i ett kluster med namn</span><span class="sxs-lookup"><span data-stu-id="a74f4-111">Example 1 - List all Kusto databases in a cluster by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster

Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="a74f4-112">Kommandot ovan returnerar alla Kusto-databaser i klustret "mykustocluster" som finns i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="a74f4-112">The above command returns all Kusto databases in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="a74f4-113">Exempel 2 – Visa alla Kusto-databaser i ett kluster med ledning</span><span class="sxs-lookup"><span data-stu-id="a74f4-113">Example 2 - List all Kusto databases in a cluster by piping</span></span>

```
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Get-AzKustoDatabase
Name                   : mykustocluster/mykustodatabase1
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase1
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases

Name                   : mykustocluster/mykustodatabase2
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase2
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="a74f4-114">Kommandot ovan kommer att hämta Kusto-klustret med namnet "mykustocluster" som finns i resurs gruppen "testrg" med `Get-AzKustoCluster` cmdleten och koppla resultatet till `Get-AzKustoDatabase` cmdleten för att lista alla databaser i klustret.</span><span class="sxs-lookup"><span data-stu-id="a74f4-114">The above command will get the Kusto cluster named "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and pipe the result to the `Get-AzKustoDatabase` cmdlet to list all databases in that cluster.</span></span>

### <span data-ttu-id="a74f4-115">Exempel 3 – hämta en specifik Kusto-databas med namn</span><span class="sxs-lookup"><span data-stu-id="a74f4-115">Example 3 - Get a specific Kusto database by name</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 3650
HotCachePeriodInDays   : 31
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="a74f4-116">Kommandot ovan returnerar Kusto-databasen med namnet "mykustodatabase" i klustret "mykustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="a74f4-116">The above command returns the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="a74f4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a74f4-117">PARAMETERS</span></span>

### <span data-ttu-id="a74f4-118">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="a74f4-118">-ClusterName</span></span>
<span data-ttu-id="a74f4-119">Namn på det kluster som databasen finns under.</span><span class="sxs-lookup"><span data-stu-id="a74f4-119">Name of cluster under which the database exists.</span></span>

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

### <span data-ttu-id="a74f4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a74f4-120">-DefaultProfile</span></span>
<span data-ttu-id="a74f4-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a74f4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a74f4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a74f4-122">-InputObject</span></span>
<span data-ttu-id="a74f4-123">Kusto.</span><span class="sxs-lookup"><span data-stu-id="a74f4-123">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a74f4-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a74f4-124">-Name</span></span>
<span data-ttu-id="a74f4-125">namnet på databasen.</span><span class="sxs-lookup"><span data-stu-id="a74f4-125">the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a74f4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a74f4-126">-ResourceGroupName</span></span>
<span data-ttu-id="a74f4-127">Namnet på den resurs grupp som användaren vill hämta klustret under.</span><span class="sxs-lookup"><span data-stu-id="a74f4-127">Name of resource group under which the user wants to retrieve the cluster.</span></span>

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

### <span data-ttu-id="a74f4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a74f4-128">-ResourceId</span></span>
<span data-ttu-id="a74f4-129">Kusto-kluster-ResourceID.</span><span class="sxs-lookup"><span data-stu-id="a74f4-129">Kusto cluster ResourceID.</span></span>

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

### <span data-ttu-id="a74f4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a74f4-130">CommonParameters</span></span>
<span data-ttu-id="a74f4-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a74f4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a74f4-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a74f4-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a74f4-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a74f4-133">INPUTS</span></span>

### <span data-ttu-id="a74f4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a74f4-134">System.String</span></span>

### <span data-ttu-id="a74f4-135">Microsoft. Azure. commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="a74f4-135">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="a74f4-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a74f4-136">OUTPUTS</span></span>

### <span data-ttu-id="a74f4-137">Microsoft. Azure. commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="a74f4-137">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="a74f4-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a74f4-138">NOTES</span></span>

## <span data-ttu-id="a74f4-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a74f4-139">RELATED LINKS</span></span>
