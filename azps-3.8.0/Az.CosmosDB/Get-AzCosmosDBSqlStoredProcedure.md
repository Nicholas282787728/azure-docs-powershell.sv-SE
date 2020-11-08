---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: a9a81336ab921ebd63b8a969be5fbf65f4b7fa14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088287"
---
# <span data-ttu-id="917e5-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="917e5-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="917e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="917e5-102">SYNOPSIS</span></span>
<span data-ttu-id="917e5-103">Hämtar CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="917e5-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="917e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="917e5-104">SYNTAX</span></span>

### <span data-ttu-id="917e5-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="917e5-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="917e5-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="917e5-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="917e5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="917e5-107">DESCRIPTION</span></span>
<span data-ttu-id="917e5-108">Cmdleten **Get-AzCosmosDBSqlStoredProcedure** hämtar listan över alla befintliga CosmosDB SQL-StoredProcedures för ett givet ResourceGroupName, AccountName, databasename och ContainerName och hämtar en enda CosmosDB SQL-StoredProcedure för en given ResourceGroupName, AccountName, databasename, ContainerName och StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="917e5-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="917e5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="917e5-109">EXAMPLES</span></span>

### <span data-ttu-id="917e5-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="917e5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="917e5-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="917e5-111">PARAMETERS</span></span>

### <span data-ttu-id="917e5-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="917e5-112">-AccountName</span></span>
<span data-ttu-id="917e5-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="917e5-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="917e5-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="917e5-114">-ContainerName</span></span>
<span data-ttu-id="917e5-115">Container namn.</span><span class="sxs-lookup"><span data-stu-id="917e5-115">Container name.</span></span>

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

### <span data-ttu-id="917e5-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="917e5-116">-DatabaseName</span></span>
<span data-ttu-id="917e5-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="917e5-117">Database name.</span></span>

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

### <span data-ttu-id="917e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917e5-118">-DefaultProfile</span></span>
<span data-ttu-id="917e5-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="917e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="917e5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="917e5-120">-InputObject</span></span>
<span data-ttu-id="917e5-121">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="917e5-121">Sql Container object.</span></span>

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

### <span data-ttu-id="917e5-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="917e5-122">-Name</span></span>
<span data-ttu-id="917e5-123">Lagrat Prcodecure-namn.</span><span class="sxs-lookup"><span data-stu-id="917e5-123">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="917e5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917e5-124">-ResourceGroupName</span></span>
<span data-ttu-id="917e5-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="917e5-125">Name of resource group.</span></span>

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

### <span data-ttu-id="917e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917e5-126">CommonParameters</span></span>
<span data-ttu-id="917e5-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="917e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917e5-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="917e5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917e5-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="917e5-129">INPUTS</span></span>

### <span data-ttu-id="917e5-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="917e5-130">None</span></span>

## <span data-ttu-id="917e5-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="917e5-131">OUTPUTS</span></span>

### <span data-ttu-id="917e5-132">Microsoft. Azure. commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="917e5-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="917e5-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="917e5-133">NOTES</span></span>

## <span data-ttu-id="917e5-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="917e5-134">RELATED LINKS</span></span>
