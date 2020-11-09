---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321328"
---
# <span data-ttu-id="a94ef-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="a94ef-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="a94ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a94ef-102">SYNOPSIS</span></span>
<span data-ttu-id="a94ef-103">Uppdaterar CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="a94ef-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="a94ef-104">Utför en klient uppdaterings åtgärd genom att läsa de befintliga StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="a94ef-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="a94ef-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a94ef-105">SYNTAX</span></span>

### <span data-ttu-id="a94ef-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a94ef-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a94ef-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a94ef-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a94ef-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a94ef-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a94ef-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a94ef-109">DESCRIPTION</span></span>
<span data-ttu-id="a94ef-110">Uppdaterar CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="a94ef-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="a94ef-111">Utför en klient uppdaterings åtgärd genom att läsa de befintliga StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="a94ef-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="a94ef-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a94ef-112">EXAMPLES</span></span>

### <span data-ttu-id="a94ef-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a94ef-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="a94ef-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a94ef-114">PARAMETERS</span></span>

### <span data-ttu-id="a94ef-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a94ef-115">-AccountName</span></span>
<span data-ttu-id="a94ef-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="a94ef-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a94ef-117">-Body</span><span class="sxs-lookup"><span data-stu-id="a94ef-117">-Body</span></span>
<span data-ttu-id="a94ef-118">Bröd texten i den lagrade proceduren.</span><span class="sxs-lookup"><span data-stu-id="a94ef-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="a94ef-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a94ef-119">-Confirm</span></span>
<span data-ttu-id="a94ef-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a94ef-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a94ef-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a94ef-121">-ContainerName</span></span>
<span data-ttu-id="a94ef-122">Container namn.</span><span class="sxs-lookup"><span data-stu-id="a94ef-122">Container name.</span></span>

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

### <span data-ttu-id="a94ef-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a94ef-123">-DatabaseName</span></span>
<span data-ttu-id="a94ef-124">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="a94ef-124">Database name.</span></span>

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

### <span data-ttu-id="a94ef-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94ef-125">-DefaultProfile</span></span>
<span data-ttu-id="a94ef-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a94ef-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a94ef-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a94ef-127">-InputObject</span></span>
<span data-ttu-id="a94ef-128">Lagrat SQL-objekt</span><span class="sxs-lookup"><span data-stu-id="a94ef-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a94ef-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="a94ef-129">-Name</span></span>
<span data-ttu-id="a94ef-130">Lagrat Prcodecure-namn.</span><span class="sxs-lookup"><span data-stu-id="a94ef-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="a94ef-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a94ef-131">-ParentObject</span></span>
<span data-ttu-id="a94ef-132">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="a94ef-132">Sql Container object.</span></span>

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

### <span data-ttu-id="a94ef-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a94ef-133">-ResourceGroupName</span></span>
<span data-ttu-id="a94ef-134">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a94ef-134">Name of resource group.</span></span>

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

### <span data-ttu-id="a94ef-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a94ef-135">-WhatIf</span></span>
<span data-ttu-id="a94ef-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a94ef-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a94ef-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a94ef-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a94ef-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94ef-138">CommonParameters</span></span>
<span data-ttu-id="a94ef-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a94ef-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94ef-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a94ef-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94ef-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a94ef-141">INPUTS</span></span>

### <span data-ttu-id="a94ef-142">Microsoft. Azure. commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="a94ef-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="a94ef-143">Microsoft. Azure. commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="a94ef-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="a94ef-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a94ef-144">OUTPUTS</span></span>

### <span data-ttu-id="a94ef-145">Microsoft. Azure. commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="a94ef-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="a94ef-146">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="a94ef-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="a94ef-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a94ef-147">NOTES</span></span>

## <span data-ttu-id="a94ef-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a94ef-148">RELATED LINKS</span></span>
