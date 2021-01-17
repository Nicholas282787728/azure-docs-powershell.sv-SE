---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 535d6aa9f2ea6538e6b00f1334ce1114fad89f81
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403784"
---
# <span data-ttu-id="fa0f1-101">New-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="fa0f1-101">New-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="fa0f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fa0f1-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0f1-103">Skapar en ny CosmosDB Gremlin-databas.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-103">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="fa0f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fa0f1-104">SYNTAX</span></span>

### <span data-ttu-id="fa0f1-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="fa0f1-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBGremlinDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa0f1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa0f1-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBGremlinDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa0f1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fa0f1-107">DESCRIPTION</span></span>
<span data-ttu-id="fa0f1-108">Skapar en ny CosmosDB Gremlin-databas.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-108">Creates a new CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="fa0f1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fa0f1-109">EXAMPLES</span></span>

### <span data-ttu-id="fa0f1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="fa0f1-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/gremlinDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetPropertiesResource
```

## <span data-ttu-id="fa0f1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fa0f1-111">PARAMETERS</span></span>

### <span data-ttu-id="fa0f1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fa0f1-112">-AccountName</span></span>
<span data-ttu-id="fa0f1-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fa0f1-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="fa0f1-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="fa0f1-115">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="fa0f1-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fa0f1-116">-Confirm</span></span>
<span data-ttu-id="fa0f1-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa0f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa0f1-118">-DefaultProfile</span></span>
<span data-ttu-id="fa0f1-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa0f1-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="fa0f1-120">-Name</span></span>
<span data-ttu-id="fa0f1-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-121">Database name.</span></span>

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

### <span data-ttu-id="fa0f1-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fa0f1-122">-ParentObject</span></span>
<span data-ttu-id="fa0f1-123">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fa0f1-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fa0f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa0f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa0f1-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-125">Name of resource group.</span></span>

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

### <span data-ttu-id="fa0f1-126">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="fa0f1-126">-Throughput</span></span>
<span data-ttu-id="fa0f1-127">Genomflödet i Gremlin databas (RU/s).</span><span class="sxs-lookup"><span data-stu-id="fa0f1-127">The throughput of Gremlin Database (RU/s).</span></span>
<span data-ttu-id="fa0f1-128">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-128">Default value is 400.</span></span>

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

### <span data-ttu-id="fa0f1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa0f1-129">-WhatIf</span></span>
<span data-ttu-id="fa0f1-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa0f1-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa0f1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0f1-132">CommonParameters</span></span>
<span data-ttu-id="fa0f1-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa0f1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0f1-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa0f1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0f1-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fa0f1-135">INPUTS</span></span>

### <span data-ttu-id="fa0f1-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fa0f1-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="fa0f1-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fa0f1-137">OUTPUTS</span></span>

### <span data-ttu-id="fa0f1-138">Microsoft. Azure. commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="fa0f1-138">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

### <span data-ttu-id="fa0f1-139">Microsoft. Azure. commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="fa0f1-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="fa0f1-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fa0f1-140">NOTES</span></span>

## <span data-ttu-id="fa0f1-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fa0f1-141">RELATED LINKS</span></span>
