---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526412"
---
# <span data-ttu-id="04e9f-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="04e9f-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="04e9f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="04e9f-103">Tar bort en CosmosDB Cassandra-tabell.</span><span class="sxs-lookup"><span data-stu-id="04e9f-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="04e9f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04e9f-104">SYNTAX</span></span>

### <span data-ttu-id="04e9f-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="04e9f-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04e9f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04e9f-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04e9f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04e9f-107">DESCRIPTION</span></span>
<span data-ttu-id="04e9f-108">Tabellen **Remove-AzCosmosDBCassandraTable** Delete a CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="04e9f-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="04e9f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04e9f-109">EXAMPLES</span></span>

### <span data-ttu-id="04e9f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="04e9f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="04e9f-111">Cmdleten returnerar ett objekt av typen bool (när-PassThru skickas), vilket är sant, om borttagningen lyckades.</span><span class="sxs-lookup"><span data-stu-id="04e9f-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="04e9f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04e9f-112">PARAMETERS</span></span>

### <span data-ttu-id="04e9f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="04e9f-113">-AccountName</span></span>
<span data-ttu-id="04e9f-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="04e9f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="04e9f-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04e9f-115">-Confirm</span></span>
<span data-ttu-id="04e9f-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04e9f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04e9f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e9f-117">-DefaultProfile</span></span>
<span data-ttu-id="04e9f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="04e9f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04e9f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04e9f-119">-InputObject</span></span>
<span data-ttu-id="04e9f-120">Cassandra.</span><span class="sxs-lookup"><span data-stu-id="04e9f-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04e9f-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="04e9f-121">-KeyspaceName</span></span>
<span data-ttu-id="04e9f-122">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="04e9f-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="04e9f-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="04e9f-123">-Name</span></span>
<span data-ttu-id="04e9f-124">Cassandra tabell namn.</span><span class="sxs-lookup"><span data-stu-id="04e9f-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="04e9f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04e9f-125">-PassThru</span></span>
<span data-ttu-id="04e9f-126">Anges till sant om användaren vill få ett resultat.</span><span class="sxs-lookup"><span data-stu-id="04e9f-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="04e9f-127">Resultatet är sant om åtgärden lyckades och ett fel inträffar om det inte är det.</span><span class="sxs-lookup"><span data-stu-id="04e9f-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="04e9f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04e9f-128">-ResourceGroupName</span></span>
<span data-ttu-id="04e9f-129">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="04e9f-129">Name of resource group.</span></span>

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

### <span data-ttu-id="04e9f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04e9f-130">-WhatIf</span></span>
<span data-ttu-id="04e9f-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04e9f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04e9f-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04e9f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04e9f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e9f-133">CommonParameters</span></span>
<span data-ttu-id="04e9f-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04e9f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e9f-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04e9f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e9f-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04e9f-136">INPUTS</span></span>

### <span data-ttu-id="04e9f-137">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="04e9f-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="04e9f-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04e9f-138">OUTPUTS</span></span>

### <span data-ttu-id="04e9f-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="04e9f-139">System.Void</span></span>

### <span data-ttu-id="04e9f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04e9f-140">System.Boolean</span></span>

## <span data-ttu-id="04e9f-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04e9f-141">NOTES</span></span>

## <span data-ttu-id="04e9f-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04e9f-142">RELATED LINKS</span></span>
