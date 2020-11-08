---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 2ee1f932e1829e6c1d9d35ccd2cf67473a851414
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092161"
---
# <span data-ttu-id="8a5b1-101">Set-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="8a5b1-101">Set-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="8a5b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="8a5b1-103">Anger CosmosDB MongoDB-databas</span><span class="sxs-lookup"><span data-stu-id="8a5b1-103">Sets the CosmosDB MongoDB Database</span></span>

## <span data-ttu-id="8a5b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a5b1-104">SYNTAX</span></span>

### <span data-ttu-id="8a5b1-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8a5b1-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBMongoDBDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a5b1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a5b1-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBMongoDBDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a5b1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a5b1-107">DESCRIPTION</span></span>
<span data-ttu-id="8a5b1-108">Cmdleten **set-AzCosmosDBMongoDBDatabase** hämtar databasen CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-108">The **Set-AzCosmosDBMongoDBDatabase** cmdlet gets the CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="8a5b1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a5b1-109">EXAMPLES</span></span>

### <span data-ttu-id="8a5b1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a5b1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName} 

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetPropertiesResource
```

<span data-ttu-id="8a5b1-111">Resource-objekt innehåller _rid, _ts, _etag egenskaper.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-111">Resource Object contains _rid, _ts, _etag properties.</span></span>

## <span data-ttu-id="8a5b1-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a5b1-112">PARAMETERS</span></span>

### <span data-ttu-id="8a5b1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8a5b1-113">-AccountName</span></span>
<span data-ttu-id="8a5b1-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8a5b1-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a5b1-115">-Confirm</span></span>
<span data-ttu-id="8a5b1-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a5b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a5b1-117">-DefaultProfile</span></span>
<span data-ttu-id="8a5b1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a5b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a5b1-119">-InputObject</span></span>
<span data-ttu-id="8a5b1-120">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8a5b1-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8a5b1-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a5b1-121">-Name</span></span>
<span data-ttu-id="8a5b1-122">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-122">Database name.</span></span>

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

### <span data-ttu-id="8a5b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a5b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="8a5b1-124">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-124">Name of resource group.</span></span>

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

### <span data-ttu-id="8a5b1-125">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="8a5b1-125">-Throughput</span></span>
<span data-ttu-id="8a5b1-126">Genomflödet i Mongo databas (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8a5b1-126">The throughput of Mongo database (RU/s).</span></span>
<span data-ttu-id="8a5b1-127">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-127">Default value is 400.</span></span>

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

### <span data-ttu-id="8a5b1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a5b1-128">-WhatIf</span></span>
<span data-ttu-id="8a5b1-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a5b1-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a5b1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a5b1-131">CommonParameters</span></span>
<span data-ttu-id="8a5b1-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a5b1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a5b1-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a5b1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a5b1-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a5b1-134">INPUTS</span></span>

### <span data-ttu-id="8a5b1-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="8a5b1-135">None</span></span>

## <span data-ttu-id="8a5b1-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a5b1-136">OUTPUTS</span></span>

### <span data-ttu-id="8a5b1-137">Microsoft. Azure. commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8a5b1-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="8a5b1-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a5b1-138">NOTES</span></span>

## <span data-ttu-id="8a5b1-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a5b1-139">RELATED LINKS</span></span>
