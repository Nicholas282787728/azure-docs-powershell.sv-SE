---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 18c1c215daa499514cf671f0c33956757dd56611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092162"
---
# <span data-ttu-id="70297-101">Set-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="70297-101">Set-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="70297-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="70297-102">SYNOPSIS</span></span>
<span data-ttu-id="70297-103">Ställer in CosmosDB Gremlin-databasen.</span><span class="sxs-lookup"><span data-stu-id="70297-103">Sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="70297-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="70297-104">SYNTAX</span></span>

### <span data-ttu-id="70297-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="70297-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70297-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70297-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70297-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="70297-107">DESCRIPTION</span></span>
<span data-ttu-id="70297-108">Cmdleten **set-AzCosmosDBGremlinDatabase** anger databas för CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="70297-108">The **Set-AzCosmosDBGremlinDatabase** cmdlet sets the CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="70297-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="70297-109">EXAMPLES</span></span>

### <span data-ttu-id="70297-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="70297-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name    Id   Resource
{name}  {id} Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

<span data-ttu-id="70297-111">Resource-objekt innehåller _rid, _ts, _etag.</span><span class="sxs-lookup"><span data-stu-id="70297-111">Resource Object contains _rid, _ts, _etag.</span></span>

## <span data-ttu-id="70297-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="70297-112">PARAMETERS</span></span>

### <span data-ttu-id="70297-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="70297-113">-AccountName</span></span>
<span data-ttu-id="70297-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="70297-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="70297-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="70297-115">-Confirm</span></span>
<span data-ttu-id="70297-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="70297-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70297-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70297-117">-DefaultProfile</span></span>
<span data-ttu-id="70297-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="70297-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70297-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70297-119">-InputObject</span></span>
<span data-ttu-id="70297-120">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="70297-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70297-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="70297-121">-Name</span></span>
<span data-ttu-id="70297-122">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="70297-122">Database name.</span></span>

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

### <span data-ttu-id="70297-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70297-123">-ResourceGroupName</span></span>
<span data-ttu-id="70297-124">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="70297-124">Name of resource group.</span></span>

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

### <span data-ttu-id="70297-125">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="70297-125">-Throughput</span></span>
<span data-ttu-id="70297-126">Genomflödet i Gremlin databas (RU/s).</span><span class="sxs-lookup"><span data-stu-id="70297-126">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="70297-127">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="70297-127">Default value is 400.</span></span>

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

### <span data-ttu-id="70297-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70297-128">-WhatIf</span></span>
<span data-ttu-id="70297-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="70297-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70297-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="70297-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70297-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70297-131">CommonParameters</span></span>
<span data-ttu-id="70297-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70297-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70297-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70297-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70297-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="70297-134">INPUTS</span></span>

### <span data-ttu-id="70297-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="70297-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="70297-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="70297-136">OUTPUTS</span></span>

### <span data-ttu-id="70297-137">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="70297-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="70297-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="70297-138">NOTES</span></span>

## <span data-ttu-id="70297-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="70297-139">RELATED LINKS</span></span>
