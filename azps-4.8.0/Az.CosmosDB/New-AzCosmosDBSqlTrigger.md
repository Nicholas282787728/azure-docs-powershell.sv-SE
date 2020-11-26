---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260593"
---
# <span data-ttu-id="a218e-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="a218e-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="a218e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a218e-102">SYNOPSIS</span></span>
<span data-ttu-id="a218e-103">Skapar en ny CosmosDB SQL-utlösare.</span><span class="sxs-lookup"><span data-stu-id="a218e-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="a218e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a218e-104">SYNTAX</span></span>

### <span data-ttu-id="a218e-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a218e-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a218e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a218e-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a218e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a218e-107">DESCRIPTION</span></span>
<span data-ttu-id="a218e-108">Skapar en ny CosmosDB SQL-utlösare.</span><span class="sxs-lookup"><span data-stu-id="a218e-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="a218e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a218e-109">EXAMPLES</span></span>

### <span data-ttu-id="a218e-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a218e-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="a218e-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a218e-111">PARAMETERS</span></span>

### <span data-ttu-id="a218e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a218e-112">-AccountName</span></span>
<span data-ttu-id="a218e-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="a218e-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a218e-114">-Body</span><span class="sxs-lookup"><span data-stu-id="a218e-114">-Body</span></span>
<span data-ttu-id="a218e-115">Texten i utlösaren.</span><span class="sxs-lookup"><span data-stu-id="a218e-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="a218e-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a218e-116">-Confirm</span></span>
<span data-ttu-id="a218e-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a218e-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a218e-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a218e-118">-ContainerName</span></span>
<span data-ttu-id="a218e-119">Container namn.</span><span class="sxs-lookup"><span data-stu-id="a218e-119">Container name.</span></span>

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

### <span data-ttu-id="a218e-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a218e-120">-DatabaseName</span></span>
<span data-ttu-id="a218e-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="a218e-121">Database name.</span></span>

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

### <span data-ttu-id="a218e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a218e-122">-DefaultProfile</span></span>
<span data-ttu-id="a218e-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a218e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a218e-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="a218e-124">-Name</span></span>
<span data-ttu-id="a218e-125">Utlösarnamn.</span><span class="sxs-lookup"><span data-stu-id="a218e-125">Trigger name.</span></span>

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

### <span data-ttu-id="a218e-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a218e-126">-ParentObject</span></span>
<span data-ttu-id="a218e-127">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="a218e-127">Sql Container object.</span></span>

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

### <span data-ttu-id="a218e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a218e-128">-ResourceGroupName</span></span>
<span data-ttu-id="a218e-129">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a218e-129">Name of resource group.</span></span>

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

### <span data-ttu-id="a218e-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="a218e-130">-TriggerOperation</span></span>
<span data-ttu-id="a218e-131">Den åtgärd som utlösaren är kopplad till.</span><span class="sxs-lookup"><span data-stu-id="a218e-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="a218e-132">Möjliga värden är: "all", "skapa", "ta bort", "Ersätt"</span><span class="sxs-lookup"><span data-stu-id="a218e-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="a218e-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="a218e-133">-TriggerType</span></span>
<span data-ttu-id="a218e-134">Typ av utlösare.</span><span class="sxs-lookup"><span data-stu-id="a218e-134">Type of the Trigger.</span></span>
<span data-ttu-id="a218e-135">Möjliga värden är: ' pre ', "post"</span><span class="sxs-lookup"><span data-stu-id="a218e-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="a218e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a218e-136">-WhatIf</span></span>
<span data-ttu-id="a218e-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a218e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a218e-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a218e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a218e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a218e-139">CommonParameters</span></span>
<span data-ttu-id="a218e-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a218e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a218e-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a218e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a218e-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a218e-142">INPUTS</span></span>

### <span data-ttu-id="a218e-143">Microsoft. Azure. commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="a218e-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="a218e-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a218e-144">OUTPUTS</span></span>

### <span data-ttu-id="a218e-145">Microsoft. Azure. commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="a218e-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="a218e-146">Microsoft. Azure. commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="a218e-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="a218e-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a218e-147">NOTES</span></span>

## <span data-ttu-id="a218e-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a218e-148">RELATED LINKS</span></span>