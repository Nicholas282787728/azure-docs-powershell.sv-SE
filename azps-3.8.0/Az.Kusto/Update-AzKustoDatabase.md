---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 858578d36f2f913f903f86b9c556a93d30e2e3b3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088840"
---
# <span data-ttu-id="d6ea8-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="d6ea8-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="d6ea8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ea8-103">Uppdatera en befintlig Kusto-databas.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-103">Update an existing Kusto database.</span></span>

## <span data-ttu-id="d6ea8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6ea8-104">SYNTAX</span></span>

### <span data-ttu-id="d6ea8-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="d6ea8-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6ea8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6ea8-106">ByResourceId</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6ea8-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d6ea8-107">ByInputObject</span></span>
```
Update-AzKustoDatabase [-SoftDeletePeriodInDays <Int32>] [-HotCachePeriodInDays <Int32>]
 [-InputObject] <PSKustoDatabase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6ea8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6ea8-108">DESCRIPTION</span></span>
<span data-ttu-id="d6ea8-109">Uppdatera en befintlig Kusto-databas.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-109">Update an existing Kusto database.</span></span>

## <span data-ttu-id="d6ea8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6ea8-110">EXAMPLES</span></span>

### <span data-ttu-id="d6ea8-111">Exempel 1 – uppdatera en befintlig databas efter namn</span><span class="sxs-lookup"><span data-stu-id="d6ea8-111">Example 1 - Update an existing database by name</span></span>

```
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="d6ea8-112">Kommandot ovan uppdaterar den mjuka borttagnings perioden för Kusto-databasen "mykustodatabase" i klustret "mykustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="d6ea8-112">The above command updates the soft deletion period of the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="d6ea8-113">Exempel 2 – uppdatera en befintlig databas efter ledning</span><span class="sxs-lookup"><span data-stu-id="d6ea8-113">Example 2 - Update an existing database by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Update-AzKustoDatabase -SoftDeletePeriodInDays 5

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 5
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="d6ea8-114">Ovanstående kommando hämtar Kusto-databasen "mykustodatabase" i klustret "mykustocluster" som finns i resurs gruppen "testrg" via `Get-AzKustoDatabase` cmdleten och sedan pipes till `Update-AzKustoDatabase` för att uppdatera databasens mjuka borttagnings period till fem dagar.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-114">The above command gets the Kusto database "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Update-AzKustoDatabase` to update the database's soft deletion period to five days.</span></span>

## <span data-ttu-id="d6ea8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6ea8-115">PARAMETERS</span></span>

### <span data-ttu-id="d6ea8-116">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="d6ea8-116">-ClusterName</span></span>
<span data-ttu-id="d6ea8-117">Namn på det kluster som databasen finns under.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-117">Name of cluster under which the database exists</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ea8-118">-DefaultProfile</span></span>
<span data-ttu-id="d6ea8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ea8-120">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="d6ea8-120">-HotCachePeriodInDays</span></span>
<span data-ttu-id="d6ea8-121">Antalet dagar som data ska sparas i cacheminnet för snabba frågor</span><span class="sxs-lookup"><span data-stu-id="d6ea8-121">The number of days that data should be kept in cache for fast queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6ea8-122">-InputObject</span></span>
<span data-ttu-id="d6ea8-123">Kusto.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-123">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea8-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6ea8-124">-Name</span></span>
<span data-ttu-id="d6ea8-125">Namn på databasen som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="d6ea8-125">Name of the database to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ea8-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6ea8-127">Namnet på den resurs grupp som klustret finns under.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6ea8-128">-ResourceId</span></span>
<span data-ttu-id="d6ea8-129">Kusto-databas ResourceID.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea8-130">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="d6ea8-130">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="d6ea8-131">Antalet dagar som data ska behållas innan det upphör att vara tillgängligt för frågor</span><span class="sxs-lookup"><span data-stu-id="d6ea8-131">The number of days that data should be kept before it stops being accessible to queries</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea8-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d6ea8-132">-Confirm</span></span>
<span data-ttu-id="d6ea8-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ea8-134">-WhatIf</span></span>
<span data-ttu-id="d6ea8-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6ea8-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6ea8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ea8-137">CommonParameters</span></span>
<span data-ttu-id="d6ea8-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ea8-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6ea8-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ea8-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6ea8-140">INPUTS</span></span>

### <span data-ttu-id="d6ea8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d6ea8-141">System.String</span></span>

### <span data-ttu-id="d6ea8-142">Microsoft. Azure. commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="d6ea8-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="d6ea8-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6ea8-143">OUTPUTS</span></span>

### <span data-ttu-id="d6ea8-144">Microsoft. Azure. commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="d6ea8-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="d6ea8-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6ea8-145">NOTES</span></span>

## <span data-ttu-id="d6ea8-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6ea8-146">RELATED LINKS</span></span>
