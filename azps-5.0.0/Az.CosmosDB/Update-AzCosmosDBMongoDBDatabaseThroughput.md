---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: 1948bc5b5488c951861509c9b3c9ee7815eddec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321352"
---
# <span data-ttu-id="c4a28-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="c4a28-101">Update-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="c4a28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4a28-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a28-103">Uppdaterar genomflödet för en CosmosDB MongoDB-databas.</span><span class="sxs-lookup"><span data-stu-id="c4a28-103">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="c4a28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4a28-104">SYNTAX</span></span>

### <span data-ttu-id="c4a28-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c4a28-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4a28-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4a28-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4a28-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4a28-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBMongoDBDatabaseThroughput [-Name <String>] -InputObject <PSMongoDBDatabaseGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4a28-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4a28-108">DESCRIPTION</span></span>
<span data-ttu-id="c4a28-109">Uppdaterar genomflödet för en CosmosDB MongoDB-databas.</span><span class="sxs-lookup"><span data-stu-id="c4a28-109">Updates the throughput value of a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="c4a28-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4a28-110">EXAMPLES</span></span>

### <span data-ttu-id="c4a28-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4a28-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBMongoDBThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myDatabaseName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/mongodbDatabases/{myDatabaseName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="c4a28-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4a28-112">PARAMETERS</span></span>

### <span data-ttu-id="c4a28-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c4a28-113">-AccountName</span></span>
<span data-ttu-id="c4a28-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="c4a28-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="c4a28-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="c4a28-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="c4a28-116">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="c4a28-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="c4a28-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4a28-117">-Confirm</span></span>
<span data-ttu-id="c4a28-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4a28-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a28-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a28-119">-DefaultProfile</span></span>
<span data-ttu-id="c4a28-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a28-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4a28-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4a28-121">-InputObject</span></span>
<span data-ttu-id="c4a28-122">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c4a28-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="c4a28-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4a28-123">-Name</span></span>
<span data-ttu-id="c4a28-124">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="c4a28-124">Database name.</span></span>

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

### <span data-ttu-id="c4a28-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c4a28-125">-ParentObject</span></span>
<span data-ttu-id="c4a28-126">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="c4a28-126">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4a28-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4a28-127">-ResourceGroupName</span></span>
<span data-ttu-id="c4a28-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="c4a28-128">Name of resource group.</span></span>

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

### <span data-ttu-id="c4a28-129">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="c4a28-129">-Throughput</span></span>
<span data-ttu-id="c4a28-130">Genomflödet i Mongo databas (RU/s).</span><span class="sxs-lookup"><span data-stu-id="c4a28-130">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="c4a28-131">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="c4a28-131">Default value is 400.</span></span>

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

### <span data-ttu-id="c4a28-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a28-132">-WhatIf</span></span>
<span data-ttu-id="c4a28-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4a28-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a28-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4a28-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a28-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a28-135">CommonParameters</span></span>
<span data-ttu-id="c4a28-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4a28-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a28-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4a28-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a28-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4a28-138">INPUTS</span></span>

### <span data-ttu-id="c4a28-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="c4a28-139">None</span></span>

## <span data-ttu-id="c4a28-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4a28-140">OUTPUTS</span></span>

### <span data-ttu-id="c4a28-141">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="c4a28-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="c4a28-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4a28-142">NOTES</span></span>

## <span data-ttu-id="c4a28-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4a28-143">RELATED LINKS</span></span>
