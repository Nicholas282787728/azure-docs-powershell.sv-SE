---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 7f6cae6a3187bf4393ea4fb592123c1833a18ebb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091439"
---
# <span data-ttu-id="26b2e-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="26b2e-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="26b2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="26b2e-103">Tar bort ett CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="26b2e-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="26b2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26b2e-104">SYNTAX</span></span>

### <span data-ttu-id="26b2e-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="26b2e-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26b2e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26b2e-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26b2e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26b2e-107">DESCRIPTION</span></span>
<span data-ttu-id="26b2e-108">Cmdleten **Remove-AzCosmosDBCassandraKeyspace** tar bort ett befintligt CosmosDB-Cassandra.</span><span class="sxs-lookup"><span data-stu-id="26b2e-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="26b2e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26b2e-109">EXAMPLES</span></span>

### <span data-ttu-id="26b2e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="26b2e-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="26b2e-111">Cmdleten returnerar ett objekt av typen bool (när-PassThru skickas) vilket är sant om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="26b2e-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="26b2e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26b2e-112">PARAMETERS</span></span>

### <span data-ttu-id="26b2e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26b2e-113">-AccountName</span></span>
<span data-ttu-id="26b2e-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="26b2e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="26b2e-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26b2e-115">-Confirm</span></span>
<span data-ttu-id="26b2e-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26b2e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b2e-117">-DefaultProfile</span></span>
<span data-ttu-id="26b2e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26b2e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26b2e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26b2e-119">-InputObject</span></span>
<span data-ttu-id="26b2e-120">Cassandra-objekt.</span><span class="sxs-lookup"><span data-stu-id="26b2e-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26b2e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="26b2e-121">-Name</span></span>
<span data-ttu-id="26b2e-122">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="26b2e-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="26b2e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26b2e-123">-PassThru</span></span>
<span data-ttu-id="26b2e-124">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="26b2e-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="26b2e-125">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="26b2e-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26b2e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b2e-126">-ResourceGroupName</span></span>
<span data-ttu-id="26b2e-127">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="26b2e-127">Name of resource group.</span></span>

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

### <span data-ttu-id="26b2e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b2e-128">-WhatIf</span></span>
<span data-ttu-id="26b2e-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26b2e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26b2e-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26b2e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b2e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b2e-131">CommonParameters</span></span>
<span data-ttu-id="26b2e-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b2e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b2e-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26b2e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b2e-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26b2e-134">INPUTS</span></span>

### <span data-ttu-id="26b2e-135">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="26b2e-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="26b2e-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26b2e-136">OUTPUTS</span></span>

### <span data-ttu-id="26b2e-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="26b2e-137">System.Void</span></span>

### <span data-ttu-id="26b2e-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26b2e-138">System.Boolean</span></span>

## <span data-ttu-id="26b2e-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26b2e-139">NOTES</span></span>

## <span data-ttu-id="26b2e-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26b2e-140">RELATED LINKS</span></span>
