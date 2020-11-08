---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1c52d1f163f5f5d23f6f282a7f00a071a38761de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260578"
---
# <span data-ttu-id="f50ea-101">Update-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f50ea-101">Update-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="f50ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f50ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f50ea-103">Uppdaterar SQL-databasen CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f50ea-103">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="f50ea-104">Utför en klient uppdaterings åtgärd genom att läsa den befintliga databasen.</span><span class="sxs-lookup"><span data-stu-id="f50ea-104">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="f50ea-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f50ea-105">SYNTAX</span></span>

### <span data-ttu-id="f50ea-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f50ea-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f50ea-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f50ea-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f50ea-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f50ea-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlDatabase [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSSqlDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f50ea-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f50ea-109">DESCRIPTION</span></span>
<span data-ttu-id="f50ea-110">Uppdaterar SQL-databasen CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f50ea-110">Updates the CosmosDB Sql Database.</span></span> <span data-ttu-id="f50ea-111">Utför en klient uppdaterings åtgärd genom att läsa den befintliga databasen.</span><span class="sxs-lookup"><span data-stu-id="f50ea-111">Performs a client side patch operation by reading the existing Database.</span></span>

## <span data-ttu-id="f50ea-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f50ea-112">EXAMPLES</span></span>

### <span data-ttu-id="f50ea-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f50ea-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName -Throughput 900

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="f50ea-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f50ea-114">PARAMETERS</span></span>

### <span data-ttu-id="f50ea-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f50ea-115">-AccountName</span></span>
<span data-ttu-id="f50ea-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="f50ea-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f50ea-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="f50ea-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="f50ea-118">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="f50ea-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="f50ea-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f50ea-119">-Confirm</span></span>
<span data-ttu-id="f50ea-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f50ea-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f50ea-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f50ea-121">-DefaultProfile</span></span>
<span data-ttu-id="f50ea-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f50ea-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f50ea-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f50ea-123">-InputObject</span></span>
<span data-ttu-id="f50ea-124">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="f50ea-124">Sql Database object.</span></span>

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

### <span data-ttu-id="f50ea-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="f50ea-125">-Name</span></span>
<span data-ttu-id="f50ea-126">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="f50ea-126">Database name.</span></span>

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

### <span data-ttu-id="f50ea-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f50ea-127">-ParentObject</span></span>
<span data-ttu-id="f50ea-128">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f50ea-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="f50ea-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f50ea-129">-ResourceGroupName</span></span>
<span data-ttu-id="f50ea-130">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f50ea-130">Name of resource group.</span></span>

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

### <span data-ttu-id="f50ea-131">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="f50ea-131">-Throughput</span></span>
<span data-ttu-id="f50ea-132">Genomflödet i SQL-databasen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="f50ea-132">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="f50ea-133">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="f50ea-133">Default value is 400.</span></span>

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

### <span data-ttu-id="f50ea-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f50ea-134">-WhatIf</span></span>
<span data-ttu-id="f50ea-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f50ea-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f50ea-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f50ea-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f50ea-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f50ea-137">CommonParameters</span></span>
<span data-ttu-id="f50ea-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f50ea-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f50ea-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f50ea-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f50ea-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f50ea-140">INPUTS</span></span>

### <span data-ttu-id="f50ea-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f50ea-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="f50ea-142">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f50ea-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="f50ea-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f50ea-143">OUTPUTS</span></span>

### <span data-ttu-id="f50ea-144">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="f50ea-144">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="f50ea-145">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f50ea-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f50ea-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f50ea-146">NOTES</span></span>

## <span data-ttu-id="f50ea-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f50ea-147">RELATED LINKS</span></span>
