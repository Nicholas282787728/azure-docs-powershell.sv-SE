---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101598"
---
# <span data-ttu-id="1cc08-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="1cc08-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="1cc08-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1cc08-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc08-103">Skapar en ny CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="1cc08-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="1cc08-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1cc08-104">SYNTAX</span></span>

### <span data-ttu-id="1cc08-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1cc08-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc08-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cc08-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc08-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1cc08-107">DESCRIPTION</span></span>
<span data-ttu-id="1cc08-108">Skapar en ny CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="1cc08-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="1cc08-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1cc08-109">EXAMPLES</span></span>

### <span data-ttu-id="1cc08-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1cc08-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="1cc08-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1cc08-111">PARAMETERS</span></span>

### <span data-ttu-id="1cc08-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1cc08-112">-AccountName</span></span>
<span data-ttu-id="1cc08-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="1cc08-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1cc08-114">-Body</span><span class="sxs-lookup"><span data-stu-id="1cc08-114">-Body</span></span>
<span data-ttu-id="1cc08-115">Bröd texten i den lagrade proceduren.</span><span class="sxs-lookup"><span data-stu-id="1cc08-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="1cc08-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1cc08-116">-Confirm</span></span>
<span data-ttu-id="1cc08-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1cc08-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc08-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1cc08-118">-ContainerName</span></span>
<span data-ttu-id="1cc08-119">Container namn.</span><span class="sxs-lookup"><span data-stu-id="1cc08-119">Container name.</span></span>

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

### <span data-ttu-id="1cc08-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1cc08-120">-DatabaseName</span></span>
<span data-ttu-id="1cc08-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="1cc08-121">Database name.</span></span>

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

### <span data-ttu-id="1cc08-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc08-122">-DefaultProfile</span></span>
<span data-ttu-id="1cc08-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc08-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc08-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="1cc08-124">-Name</span></span>
<span data-ttu-id="1cc08-125">Lagrat Prcodecure-namn.</span><span class="sxs-lookup"><span data-stu-id="1cc08-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="1cc08-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1cc08-126">-ParentObject</span></span>
<span data-ttu-id="1cc08-127">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="1cc08-127">Sql Container object.</span></span>

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

### <span data-ttu-id="1cc08-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc08-128">-ResourceGroupName</span></span>
<span data-ttu-id="1cc08-129">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1cc08-129">Name of resource group.</span></span>

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

### <span data-ttu-id="1cc08-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc08-130">-WhatIf</span></span>
<span data-ttu-id="1cc08-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1cc08-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc08-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1cc08-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc08-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc08-133">CommonParameters</span></span>
<span data-ttu-id="1cc08-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc08-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc08-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1cc08-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc08-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1cc08-136">INPUTS</span></span>

### <span data-ttu-id="1cc08-137">Microsoft. Azure. commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="1cc08-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="1cc08-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1cc08-138">OUTPUTS</span></span>

### <span data-ttu-id="1cc08-139">Microsoft. Azure. commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="1cc08-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="1cc08-140">Microsoft. Azure. commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="1cc08-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="1cc08-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1cc08-141">NOTES</span></span>

## <span data-ttu-id="1cc08-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1cc08-142">RELATED LINKS</span></span>
