---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: d90df542fd2acc925531f4bf9da7244ea1831a63
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089908"
---
# <span data-ttu-id="c2579-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="c2579-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="c2579-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2579-102">SYNOPSIS</span></span>
<span data-ttu-id="c2579-103">Uppdaterar genomflödet för en CosmosDB MongoDB-databas.</span><span class="sxs-lookup"><span data-stu-id="c2579-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="c2579-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2579-104">SYNTAX</span></span>

### <span data-ttu-id="c2579-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c2579-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 -Throughput <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2579-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2579-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -ParentObject <PSDatabaseAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2579-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2579-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -Throughput <Int32>
 -InputObject <PSMongoDBDatabaseGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2579-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2579-108">EXAMPLES</span></span>

### <span data-ttu-id="c2579-109">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c2579-109">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="c2579-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2579-110">PARAMETERS</span></span>

### <span data-ttu-id="c2579-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2579-111">-AccountName</span></span>
<span data-ttu-id="c2579-112">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="c2579-112">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c2579-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2579-113">-Confirm</span></span>
<span data-ttu-id="c2579-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2579-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2579-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2579-115">-DefaultProfile</span></span>
<span data-ttu-id="c2579-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2579-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2579-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2579-117">-InputObject</span></span>
<span data-ttu-id="c2579-118">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c2579-118">CosmosDB Account object</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2579-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2579-119">-Name</span></span>
<span data-ttu-id="c2579-120">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="c2579-120">Database name.</span></span>

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

### <span data-ttu-id="c2579-121">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c2579-121">-ParentObject</span></span>
<span data-ttu-id="c2579-122">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c2579-122">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2579-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2579-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2579-124">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c2579-124">Name of resource group.</span></span>

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

### <span data-ttu-id="c2579-125">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="c2579-125">-Throughput</span></span>
<span data-ttu-id="c2579-126">Genomflödet i Mongo databas (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c2579-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="c2579-127">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="c2579-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2579-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2579-128">-WhatIf</span></span>
<span data-ttu-id="c2579-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2579-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2579-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2579-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2579-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2579-131">CommonParameters</span></span>
<span data-ttu-id="c2579-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2579-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2579-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2579-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2579-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2579-134">INPUTS</span></span>

### <span data-ttu-id="c2579-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="c2579-135">None</span></span>

## <span data-ttu-id="c2579-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2579-136">OUTPUTS</span></span>

### <span data-ttu-id="c2579-137">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c2579-137">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c2579-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2579-138">NOTES</span></span>

## <span data-ttu-id="c2579-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2579-139">RELATED LINKS</span></span>
