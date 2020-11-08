---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: e144e863ec0c9d55b14295486cdc4e94e26e8909
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101612"
---
# <span data-ttu-id="bd109-101">Get-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="bd109-101">Get-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="bd109-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd109-102">SYNOPSIS</span></span>
<span data-ttu-id="bd109-103">Hämtar CosmosDB SQL-StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="bd109-103">Gets the CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="bd109-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd109-104">SYNTAX</span></span>

### <span data-ttu-id="bd109-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd109-105">ByNameParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd109-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd109-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlStoredProcedure [-Name <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd109-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd109-107">DESCRIPTION</span></span>
<span data-ttu-id="bd109-108">Cmdleten **Get-AzCosmosDBSqlStoredProcedure** hämtar listan över alla befintliga CosmosDB SQL-StoredProcedures för ett givet ResourceGroupName, AccountName, databasename och ContainerName och hämtar en enda CosmosDB SQL-StoredProcedure för en given ResourceGroupName, AccountName, databasename, ContainerName och StoredProcedureName.</span><span class="sxs-lookup"><span data-stu-id="bd109-108">The **Get-AzCosmosDBSqlStoredProcedure** cmdlet gets the list of all existing CosmosDB Sql StoredProcedures for a given ResourceGroupName, AccountName, DatabaseName and ContainerName and gets a single CosmosDB Sql StoredProcedure for a given ResourceGroupName, AccountName, DatabaseName, ContainerName and StoredProcedureName.</span></span>

## <span data-ttu-id="bd109-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd109-109">EXAMPLES</span></span>

### <span data-ttu-id="bd109-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bd109-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
Resource                       : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="bd109-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd109-111">PARAMETERS</span></span>

### <span data-ttu-id="bd109-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bd109-112">-AccountName</span></span>
<span data-ttu-id="bd109-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="bd109-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bd109-114">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="bd109-114">-ContainerName</span></span>
<span data-ttu-id="bd109-115">Container namn.</span><span class="sxs-lookup"><span data-stu-id="bd109-115">Container name.</span></span>

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

### <span data-ttu-id="bd109-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bd109-116">-DatabaseName</span></span>
<span data-ttu-id="bd109-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="bd109-117">Database name.</span></span>

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

### <span data-ttu-id="bd109-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd109-118">-DefaultProfile</span></span>
<span data-ttu-id="bd109-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd109-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd109-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd109-120">-Name</span></span>
<span data-ttu-id="bd109-121">Lagrat Prcodecure-namn.</span><span class="sxs-lookup"><span data-stu-id="bd109-121">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="bd109-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="bd109-122">-ParentObject</span></span>
<span data-ttu-id="bd109-123">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="bd109-123">Sql Container object.</span></span>

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

### <span data-ttu-id="bd109-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd109-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd109-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bd109-125">Name of resource group.</span></span>

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

### <span data-ttu-id="bd109-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd109-126">CommonParameters</span></span>
<span data-ttu-id="bd109-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd109-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd109-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd109-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd109-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd109-129">INPUTS</span></span>

### <span data-ttu-id="bd109-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="bd109-130">None</span></span>

## <span data-ttu-id="bd109-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd109-131">OUTPUTS</span></span>

### <span data-ttu-id="bd109-132">Microsoft. Azure. commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="bd109-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="bd109-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd109-133">NOTES</span></span>

## <span data-ttu-id="bd109-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd109-134">RELATED LINKS</span></span>
