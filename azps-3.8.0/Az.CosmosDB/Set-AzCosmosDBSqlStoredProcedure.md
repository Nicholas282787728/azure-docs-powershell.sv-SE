---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 2914284849fa9a00e3cb2d0b1c96c1efd905e9e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088277"
---
# <span data-ttu-id="b7f20-101">Set-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="b7f20-101">Set-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="b7f20-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7f20-102">SYNOPSIS</span></span>
<span data-ttu-id="b7f20-103">Skapar en ny eller uppdaterar en befintlig CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="b7f20-103">Creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="b7f20-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7f20-104">SYNTAX</span></span>

### <span data-ttu-id="b7f20-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b7f20-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7f20-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7f20-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7f20-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7f20-107">DESCRIPTION</span></span>
<span data-ttu-id="b7f20-108">Cmdleten **set-AzCosmosDBSqlStoredProcedure** skapar en ny eller uppdaterar en befintlig CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="b7f20-108">The **Set-AzCosmosDBSqlStoredProcedure** cmdlet creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="b7f20-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7f20-109">EXAMPLES</span></span>

### <span data-ttu-id="b7f20-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b7f20-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName} -Body {sampleBody}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
SqlStoredProcedureGetResultsId :
Body                           :
_rid                           :
_ts                            :
_etag                          :
```

## <span data-ttu-id="b7f20-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7f20-111">PARAMETERS</span></span>

### <span data-ttu-id="b7f20-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b7f20-112">-AccountName</span></span>
<span data-ttu-id="b7f20-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="b7f20-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b7f20-114">-Body</span><span class="sxs-lookup"><span data-stu-id="b7f20-114">-Body</span></span>
<span data-ttu-id="b7f20-115">Bröd texten i den lagrade proceduren.</span><span class="sxs-lookup"><span data-stu-id="b7f20-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="b7f20-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7f20-116">-Confirm</span></span>
<span data-ttu-id="b7f20-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7f20-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7f20-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b7f20-118">-ContainerName</span></span>
<span data-ttu-id="b7f20-119">Container namn.</span><span class="sxs-lookup"><span data-stu-id="b7f20-119">Container name.</span></span>

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

### <span data-ttu-id="b7f20-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7f20-120">-DatabaseName</span></span>
<span data-ttu-id="b7f20-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="b7f20-121">Database name.</span></span>

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

### <span data-ttu-id="b7f20-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7f20-122">-DefaultProfile</span></span>
<span data-ttu-id="b7f20-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7f20-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7f20-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7f20-124">-InputObject</span></span>
<span data-ttu-id="b7f20-125">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="b7f20-125">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7f20-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7f20-126">-Name</span></span>
<span data-ttu-id="b7f20-127">Lagrat Prcodecure-namn.</span><span class="sxs-lookup"><span data-stu-id="b7f20-127">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="b7f20-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7f20-128">-ResourceGroupName</span></span>
<span data-ttu-id="b7f20-129">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b7f20-129">Name of resource group.</span></span>

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

### <span data-ttu-id="b7f20-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7f20-130">-WhatIf</span></span>
<span data-ttu-id="b7f20-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7f20-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7f20-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7f20-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7f20-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7f20-133">CommonParameters</span></span>
<span data-ttu-id="b7f20-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7f20-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7f20-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7f20-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7f20-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7f20-136">INPUTS</span></span>

### <span data-ttu-id="b7f20-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="b7f20-137">None</span></span>

## <span data-ttu-id="b7f20-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7f20-138">OUTPUTS</span></span>

### <span data-ttu-id="b7f20-139">Microsoft. Azure. commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="b7f20-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="b7f20-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7f20-140">NOTES</span></span>

## <span data-ttu-id="b7f20-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7f20-141">RELATED LINKS</span></span>
