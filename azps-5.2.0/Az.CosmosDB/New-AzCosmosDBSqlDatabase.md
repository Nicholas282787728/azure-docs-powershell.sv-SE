---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 2953da3747404c0b6b98992cc8a8b80573da5129
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418195"
---
# <span data-ttu-id="8e709-101">New-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e709-101">New-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="8e709-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e709-102">SYNOPSIS</span></span>
<span data-ttu-id="8e709-103">Skapar en ny CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="8e709-103">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="8e709-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e709-104">SYNTAX</span></span>

### <span data-ttu-id="8e709-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8e709-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e709-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e709-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e709-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e709-107">DESCRIPTION</span></span>
<span data-ttu-id="8e709-108">Skapar en ny CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="8e709-108">Creates a new CosmosDB Sql Database.</span></span>

## <span data-ttu-id="8e709-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e709-109">EXAMPLES</span></span>

### <span data-ttu-id="8e709-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8e709-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlDatabase -AccountName myAccountName -Name myDatabaseName -ResourceGroupName myResourcegroupName

Name     : myDatabaseName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/sqlDatabases/myDatabaseName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="8e709-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e709-111">PARAMETERS</span></span>

### <span data-ttu-id="8e709-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e709-112">-AccountName</span></span>
<span data-ttu-id="8e709-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="8e709-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8e709-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="8e709-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="8e709-115">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="8e709-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="8e709-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e709-116">-Confirm</span></span>
<span data-ttu-id="8e709-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e709-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e709-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e709-118">-DefaultProfile</span></span>
<span data-ttu-id="8e709-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e709-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e709-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e709-120">-Name</span></span>
<span data-ttu-id="8e709-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="8e709-121">Database name.</span></span>

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

### <span data-ttu-id="8e709-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8e709-122">-ParentObject</span></span>
<span data-ttu-id="8e709-123">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="8e709-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="8e709-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e709-124">-ResourceGroupName</span></span>
<span data-ttu-id="8e709-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8e709-125">Name of resource group.</span></span>

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

### <span data-ttu-id="8e709-126">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="8e709-126">-Throughput</span></span>
<span data-ttu-id="8e709-127">Genomflödet i SQL-databasen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="8e709-127">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="8e709-128">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="8e709-128">Default value is 400.</span></span>

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

### <span data-ttu-id="8e709-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e709-129">-WhatIf</span></span>
<span data-ttu-id="8e709-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e709-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e709-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e709-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e709-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e709-132">CommonParameters</span></span>
<span data-ttu-id="8e709-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e709-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e709-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e709-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e709-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e709-135">INPUTS</span></span>

### <span data-ttu-id="8e709-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="8e709-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="8e709-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e709-137">OUTPUTS</span></span>

### <span data-ttu-id="8e709-138">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="8e709-138">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="8e709-139">Microsoft. Azure. commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="8e709-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="8e709-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e709-140">NOTES</span></span>

## <span data-ttu-id="8e709-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e709-141">RELATED LINKS</span></span>
