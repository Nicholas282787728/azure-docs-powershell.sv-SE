---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a67b2a665f763c32876177414a347270f557c914
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088276"
---
# <span data-ttu-id="7fb4a-101">Set-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="7fb4a-101">Set-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="7fb4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fb4a-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb4a-103">Skapar en ny eller uppdaterar en befintlig CosmosDB SQL-utlösare.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-103">Creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="7fb4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fb4a-104">SYNTAX</span></span>

### <span data-ttu-id="7fb4a-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7fb4a-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb4a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb4a-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7fb4a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fb4a-107">DESCRIPTION</span></span>
<span data-ttu-id="7fb4a-108">Cmdleten **set-AzCosmosDBSqlTrigger** skapar en ny eller uppdaterar en befintlig CosmosDB SQL-utlösare.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-108">The **Set-AzCosmosDBSqlTrigger** cmdlet creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="7fb4a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fb4a-109">EXAMPLES</span></span>

### <span data-ttu-id="7fb4a-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7fb4a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} -Body {sampleBody}

Name                   : {triggerName}
Id                     : {triggerId}
SqlTriggerGetResultsId :
Body                   :
TriggerType            :
TriggerOperation       :
_rid                   :
_ts                    :
_etag                  :
```

## <span data-ttu-id="7fb4a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fb4a-111">PARAMETERS</span></span>

### <span data-ttu-id="7fb4a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7fb4a-112">-AccountName</span></span>
<span data-ttu-id="7fb4a-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7fb4a-114">-Body</span><span class="sxs-lookup"><span data-stu-id="7fb4a-114">-Body</span></span>
<span data-ttu-id="7fb4a-115">Texten i utlösaren.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="7fb4a-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7fb4a-116">-Confirm</span></span>
<span data-ttu-id="7fb4a-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb4a-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7fb4a-118">-ContainerName</span></span>
<span data-ttu-id="7fb4a-119">Container namn.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-119">Container name.</span></span>

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

### <span data-ttu-id="7fb4a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7fb4a-120">-DatabaseName</span></span>
<span data-ttu-id="7fb4a-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-121">Database name.</span></span>

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

### <span data-ttu-id="7fb4a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb4a-122">-DefaultProfile</span></span>
<span data-ttu-id="7fb4a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb4a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fb4a-124">-InputObject</span></span>
<span data-ttu-id="7fb4a-125">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-125">Sql Container object.</span></span>

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

### <span data-ttu-id="7fb4a-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="7fb4a-126">-Name</span></span>
<span data-ttu-id="7fb4a-127">Utlösarnamn.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-127">Trigger name.</span></span>

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

### <span data-ttu-id="7fb4a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb4a-128">-ResourceGroupName</span></span>
<span data-ttu-id="7fb4a-129">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-129">Name of resource group.</span></span>

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

### <span data-ttu-id="7fb4a-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="7fb4a-130">-TriggerOperation</span></span>
<span data-ttu-id="7fb4a-131">Den åtgärd som utlösaren är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="7fb4a-132">Möjliga värden är: "all", "skapa", "ta bort", "Ersätt"</span><span class="sxs-lookup"><span data-stu-id="7fb4a-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="7fb4a-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="7fb4a-133">-TriggerType</span></span>
<span data-ttu-id="7fb4a-134">Typ av utlösare.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-134">Type of the Trigger.</span></span>
<span data-ttu-id="7fb4a-135">Möjliga värden är: ' pre ', "post"</span><span class="sxs-lookup"><span data-stu-id="7fb4a-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="7fb4a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb4a-136">-WhatIf</span></span>
<span data-ttu-id="7fb4a-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fb4a-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb4a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb4a-139">CommonParameters</span></span>
<span data-ttu-id="7fb4a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fb4a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb4a-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fb4a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb4a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fb4a-142">INPUTS</span></span>

### <span data-ttu-id="7fb4a-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="7fb4a-143">None</span></span>

## <span data-ttu-id="7fb4a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fb4a-144">OUTPUTS</span></span>

### <span data-ttu-id="7fb4a-145">Microsoft. Azure. commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="7fb4a-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="7fb4a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fb4a-146">NOTES</span></span>

## <span data-ttu-id="7fb4a-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fb4a-147">RELATED LINKS</span></span>
