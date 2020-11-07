---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 27363873996505a15e8eccd3dcb3620a2f88c1a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925725"
---
# <span data-ttu-id="8e8a1-101">Set-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="8e8a1-101">Set-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="8e8a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8e8a1-102">SYNOPSIS</span></span>
<span data-ttu-id="8e8a1-103">Skapar en ny eller uppdaterar en befintlig CosmosDB SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-103">Creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="8e8a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8e8a1-104">SYNTAX</span></span>

### <span data-ttu-id="8e8a1-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8e8a1-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e8a1-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e8a1-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e8a1-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8e8a1-107">DESCRIPTION</span></span>
<span data-ttu-id="8e8a1-108">Cmdleten **set-AzCosmosDBSqlUserDefinedFunction** skapar en ny eller uppdaterar en befintlig CosmosDB SQL-UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-108">The **Set-AzCosmosDBSqlUserDefinedFunction** cmdlet creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="8e8a1-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8e8a1-109">EXAMPLES</span></span>

### <span data-ttu-id="8e8a1-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8e8a1-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {udfName} -ContainerName {containerName} -Body {sampleBody}

Name                               : {udfName}
Id                                 : {udfId}
SqlUserDefinedFunctionGetResultsId :
Body                               :
_rid                               :
_ts                                :
_etag                              :
```

## <span data-ttu-id="8e8a1-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8e8a1-111">PARAMETERS</span></span>

### <span data-ttu-id="8e8a1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e8a1-112">-AccountName</span></span>
<span data-ttu-id="8e8a1-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="8e8a1-114">-Body</span><span class="sxs-lookup"><span data-stu-id="8e8a1-114">-Body</span></span>
<span data-ttu-id="8e8a1-115">Bröd texten i den användardefinierade funktionen.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="8e8a1-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8e8a1-116">-Confirm</span></span>
<span data-ttu-id="8e8a1-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e8a1-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="8e8a1-118">-ContainerName</span></span>
<span data-ttu-id="8e8a1-119">Container namn.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-119">Container name.</span></span>

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

### <span data-ttu-id="8e8a1-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8e8a1-120">-DatabaseName</span></span>
<span data-ttu-id="8e8a1-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-121">Database name.</span></span>

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

### <span data-ttu-id="8e8a1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e8a1-122">-DefaultProfile</span></span>
<span data-ttu-id="8e8a1-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e8a1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e8a1-124">-InputObject</span></span>
<span data-ttu-id="8e8a1-125">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-125">Sql Container object.</span></span>

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

### <span data-ttu-id="8e8a1-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="8e8a1-126">-Name</span></span>
<span data-ttu-id="8e8a1-127">Användardefinierat funktions namn.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-127">User Defined Function Name.</span></span>

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

### <span data-ttu-id="8e8a1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e8a1-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e8a1-129">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-129">Name of resource group.</span></span>

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

### <span data-ttu-id="8e8a1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e8a1-130">-WhatIf</span></span>
<span data-ttu-id="8e8a1-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e8a1-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e8a1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e8a1-133">CommonParameters</span></span>
<span data-ttu-id="8e8a1-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e8a1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e8a1-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e8a1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e8a1-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8e8a1-136">INPUTS</span></span>

### <span data-ttu-id="8e8a1-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="8e8a1-137">None</span></span>

## <span data-ttu-id="8e8a1-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8e8a1-138">OUTPUTS</span></span>

### <span data-ttu-id="8e8a1-139">Microsoft. Azure. commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="8e8a1-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="8e8a1-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8e8a1-140">NOTES</span></span>

## <span data-ttu-id="8e8a1-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8e8a1-141">RELATED LINKS</span></span>
