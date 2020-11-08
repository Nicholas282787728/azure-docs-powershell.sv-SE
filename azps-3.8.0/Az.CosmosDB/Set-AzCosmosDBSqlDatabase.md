---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 1af202573ff4b783756b8884707922c64ffcf953
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088280"
---
# <span data-ttu-id="b956c-101">Set-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b956c-101">Set-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="b956c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b956c-102">SYNOPSIS</span></span>
<span data-ttu-id="b956c-103">Skapar en ny eller uppdaterar en befintlig CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="b956c-103">Creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="b956c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b956c-104">SYNTAX</span></span>

### <span data-ttu-id="b956c-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b956c-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-Throughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b956c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b956c-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlDatabase -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b956c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b956c-107">DESCRIPTION</span></span>
<span data-ttu-id="b956c-108">Cmdleten **set-AzCosmosDBSqlDatabase** skapar en ny eller uppdaterar en befintlig CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="b956c-108">The **Set-AzCosmosDBSqlDatabase** cmdlet creates a new or updates an existing CosmosDB Sql Database.</span></span>

## <span data-ttu-id="b956c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b956c-109">EXAMPLES</span></span>

### <span data-ttu-id="b956c-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b956c-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlDatabase -ResourceGroupName {resourceGroupName} -AccountName {accountName}-Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
SqlDatabaseGetResultsId :
_rid                    :
_ts                     :
_etag                   :
_colls                  :
_users                  :
```

## <span data-ttu-id="b956c-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b956c-111">PARAMETERS</span></span>

### <span data-ttu-id="b956c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b956c-112">-AccountName</span></span>
<span data-ttu-id="b956c-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="b956c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b956c-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b956c-114">-Confirm</span></span>
<span data-ttu-id="b956c-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b956c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b956c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b956c-116">-DefaultProfile</span></span>
<span data-ttu-id="b956c-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b956c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b956c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b956c-118">-InputObject</span></span>
<span data-ttu-id="b956c-119">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b956c-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b956c-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b956c-120">-Name</span></span>
<span data-ttu-id="b956c-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="b956c-121">Database name.</span></span>

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

### <span data-ttu-id="b956c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b956c-122">-ResourceGroupName</span></span>
<span data-ttu-id="b956c-123">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b956c-123">Name of resource group.</span></span>

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

### <span data-ttu-id="b956c-124">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="b956c-124">-Throughput</span></span>
<span data-ttu-id="b956c-125">Genomflödet i SQL-databasen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b956c-125">The throughput of SQL database (RU/s).</span></span>
<span data-ttu-id="b956c-126">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="b956c-126">Default value is 400.</span></span>

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

### <span data-ttu-id="b956c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b956c-127">-WhatIf</span></span>
<span data-ttu-id="b956c-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b956c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b956c-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b956c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b956c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b956c-130">CommonParameters</span></span>
<span data-ttu-id="b956c-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b956c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b956c-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b956c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b956c-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b956c-133">INPUTS</span></span>

### <span data-ttu-id="b956c-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="b956c-134">None</span></span>

## <span data-ttu-id="b956c-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b956c-135">OUTPUTS</span></span>

### <span data-ttu-id="b956c-136">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b956c-136">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

## <span data-ttu-id="b956c-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b956c-137">NOTES</span></span>

## <span data-ttu-id="b956c-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b956c-138">RELATED LINKS</span></span>
