---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321340"
---
# <span data-ttu-id="071a2-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="071a2-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="071a2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="071a2-102">SYNOPSIS</span></span>
<span data-ttu-id="071a2-103">Uppdaterar SQL-databasen CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="071a2-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="071a2-104">Utför en klient uppdaterings åtgärd genom att läsa den befintliga databasen.</span><span class="sxs-lookup"><span data-stu-id="071a2-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="071a2-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="071a2-105">SYNTAX</span></span>

### <span data-ttu-id="071a2-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="071a2-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="071a2-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="071a2-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="071a2-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="071a2-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="071a2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="071a2-109">DESCRIPTION</span></span>
<span data-ttu-id="071a2-110">Uppdaterar SQL-databasen CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="071a2-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="071a2-111">Utför en klient uppdaterings åtgärd genom att läsa den befintliga databasen.</span><span class="sxs-lookup"><span data-stu-id="071a2-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="071a2-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="071a2-112">EXAMPLES</span></span>

### <span data-ttu-id="071a2-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="071a2-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="071a2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="071a2-114">PARAMETERS</span></span>

### <span data-ttu-id="071a2-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="071a2-115">-AccountName</span></span>
<span data-ttu-id="071a2-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="071a2-116">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071a2-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="071a2-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="071a2-118">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="071a2-118">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071a2-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="071a2-119">-Confirm</span></span>
<span data-ttu-id="071a2-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="071a2-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071a2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="071a2-121">-DefaultProfile</span></span>
<span data-ttu-id="071a2-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="071a2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="071a2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="071a2-123">-InputObject</span></span>
<span data-ttu-id="071a2-124">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="071a2-124">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="071a2-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="071a2-125">-Name</span></span>
<span data-ttu-id="071a2-126">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="071a2-126">Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071a2-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="071a2-127">-ParentObject</span></span>
<span data-ttu-id="071a2-128">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="071a2-128">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="071a2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="071a2-129">-ResourceGroupName</span></span>
<span data-ttu-id="071a2-130">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="071a2-130">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071a2-131">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="071a2-131">-Throughput</span></span>
<span data-ttu-id="071a2-132">Genomflödet i SQL-databasen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="071a2-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="071a2-133">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="071a2-133">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071a2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="071a2-134">-WhatIf</span></span>
<span data-ttu-id="071a2-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="071a2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="071a2-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="071a2-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="071a2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="071a2-137">CommonParameters</span></span>
<span data-ttu-id="071a2-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="071a2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="071a2-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="071a2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="071a2-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="071a2-140">INPUTS</span></span>

### <span data-ttu-id="071a2-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="071a2-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="071a2-142">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="071a2-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="071a2-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="071a2-143">OUTPUTS</span></span>

### <span data-ttu-id="071a2-144">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="071a2-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="071a2-145">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="071a2-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="071a2-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="071a2-146">NOTES</span></span>

## <span data-ttu-id="071a2-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="071a2-147">RELATED LINKS</span></span>
