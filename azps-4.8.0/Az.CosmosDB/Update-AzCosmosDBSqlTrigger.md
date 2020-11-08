---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262798"
---
# <span data-ttu-id="7d3bd-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="7d3bd-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="7d3bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d3bd-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3bd-103">Uppdaterar SQL-utlösaren CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="7d3bd-104">Utför en klient uppdaterings åtgärd genom att läsa den befintliga utlösaren.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="7d3bd-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d3bd-105">SYNTAX</span></span>

### <span data-ttu-id="7d3bd-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7d3bd-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3bd-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d3bd-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3bd-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d3bd-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d3bd-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d3bd-109">DESCRIPTION</span></span>
<span data-ttu-id="7d3bd-110">Uppdaterar SQL-utlösaren CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="7d3bd-111">Utför en klient uppdaterings åtgärd genom att läsa den befintliga utlösaren.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="7d3bd-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d3bd-112">EXAMPLES</span></span>

### <span data-ttu-id="7d3bd-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7d3bd-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="7d3bd-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d3bd-114">PARAMETERS</span></span>

### <span data-ttu-id="7d3bd-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7d3bd-115">-AccountName</span></span>
<span data-ttu-id="7d3bd-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7d3bd-117">-Body</span><span class="sxs-lookup"><span data-stu-id="7d3bd-117">-Body</span></span>
<span data-ttu-id="7d3bd-118">Texten i utlösaren.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="7d3bd-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d3bd-119">-Confirm</span></span>
<span data-ttu-id="7d3bd-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d3bd-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7d3bd-121">-ContainerName</span></span>
<span data-ttu-id="7d3bd-122">Container namn.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-122">Container name.</span></span>

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

### <span data-ttu-id="7d3bd-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7d3bd-123">-DatabaseName</span></span>
<span data-ttu-id="7d3bd-124">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-124">Database name.</span></span>

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

### <span data-ttu-id="7d3bd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3bd-125">-DefaultProfile</span></span>
<span data-ttu-id="7d3bd-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d3bd-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d3bd-127">-InputObject</span></span>
<span data-ttu-id="7d3bd-128">SQL trigger-objekt</span><span class="sxs-lookup"><span data-stu-id="7d3bd-128">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3bd-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="7d3bd-129">-Name</span></span>
<span data-ttu-id="7d3bd-130">Utlösarnamn.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-130">Trigger name.</span></span>

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

### <span data-ttu-id="7d3bd-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7d3bd-131">-ParentObject</span></span>
<span data-ttu-id="7d3bd-132">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-132">Sql Container object.</span></span>

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

### <span data-ttu-id="7d3bd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d3bd-133">-ResourceGroupName</span></span>
<span data-ttu-id="7d3bd-134">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-134">Name of resource group.</span></span>

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

### <span data-ttu-id="7d3bd-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="7d3bd-135">-TriggerOperation</span></span>
<span data-ttu-id="7d3bd-136">Den åtgärd som utlösaren är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="7d3bd-137">Möjliga värden är: "all", "skapa", "ta bort", "Ersätt"</span><span class="sxs-lookup"><span data-stu-id="7d3bd-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="7d3bd-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="7d3bd-138">-TriggerType</span></span>
<span data-ttu-id="7d3bd-139">Typ av utlösare.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-139">Type of the Trigger.</span></span>
<span data-ttu-id="7d3bd-140">Möjliga värden är: ' pre ', "post"</span><span class="sxs-lookup"><span data-stu-id="7d3bd-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="7d3bd-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d3bd-141">-WhatIf</span></span>
<span data-ttu-id="7d3bd-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d3bd-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d3bd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3bd-144">CommonParameters</span></span>
<span data-ttu-id="7d3bd-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d3bd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3bd-146">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d3bd-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3bd-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d3bd-147">INPUTS</span></span>

### <span data-ttu-id="7d3bd-148">Microsoft. Azure. commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="7d3bd-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="7d3bd-149">Microsoft. Azure. commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="7d3bd-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="7d3bd-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d3bd-150">OUTPUTS</span></span>

### <span data-ttu-id="7d3bd-151">Microsoft. Azure. commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="7d3bd-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="7d3bd-152">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="7d3bd-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="7d3bd-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d3bd-153">NOTES</span></span>

## <span data-ttu-id="7d3bd-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d3bd-154">RELATED LINKS</span></span>
