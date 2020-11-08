---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 89a48ecb4b167919562428e1116d95bb1e3d6390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091834"
---
# <span data-ttu-id="09339-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="09339-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="09339-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09339-102">SYNOPSIS</span></span>
<span data-ttu-id="09339-103">Hämtar SQL-containern för CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="09339-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="09339-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09339-104">SYNTAX</span></span>

### <span data-ttu-id="09339-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="09339-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="09339-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09339-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -InputObject <PSSqlDatabaseGetResults> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09339-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09339-107">DESCRIPTION</span></span>
<span data-ttu-id="09339-108">Cmdleten **Get-AzCosmosDBSqlContainer** hämtar listan över alla befintliga CosmosDB SQL-behållare för ett givet ResourceGroupName, AccountName och databasename och hämtar en enda CosmosDB SQL-behållare för ett givet ResourceGroupName, AccountName, databasename och ContainerName.</span><span class="sxs-lookup"><span data-stu-id="09339-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="09339-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09339-109">EXAMPLES</span></span>

### <span data-ttu-id="09339-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="09339-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="09339-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09339-111">PARAMETERS</span></span>

### <span data-ttu-id="09339-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="09339-112">-AccountName</span></span>
<span data-ttu-id="09339-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="09339-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="09339-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09339-114">-DatabaseName</span></span>
<span data-ttu-id="09339-115">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="09339-115">Database name.</span></span>

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

### <span data-ttu-id="09339-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09339-116">-DefaultProfile</span></span>
<span data-ttu-id="09339-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09339-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09339-118">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="09339-118">-Detailed</span></span>
<span data-ttu-id="09339-119">Om den anges returnerar cmdleten den med genomflödet.</span><span class="sxs-lookup"><span data-stu-id="09339-119">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="09339-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09339-120">-InputObject</span></span>
<span data-ttu-id="09339-121">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="09339-121">Sql Database object.</span></span>

```yaml
Type: PSSqlDatabaseGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09339-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="09339-122">-Name</span></span>
<span data-ttu-id="09339-123">Container namn.</span><span class="sxs-lookup"><span data-stu-id="09339-123">Container name.</span></span>

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

### <span data-ttu-id="09339-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09339-124">-ResourceGroupName</span></span>
<span data-ttu-id="09339-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="09339-125">Name of resource group.</span></span>

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

### <span data-ttu-id="09339-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09339-126">CommonParameters</span></span>
<span data-ttu-id="09339-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09339-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09339-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09339-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09339-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09339-129">INPUTS</span></span>

### <span data-ttu-id="09339-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="09339-130">None</span></span>

## <span data-ttu-id="09339-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09339-131">OUTPUTS</span></span>

### <span data-ttu-id="09339-132">Microsoft. Azure. commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="09339-132">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="09339-133">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="09339-133">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="09339-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09339-134">NOTES</span></span>

## <span data-ttu-id="09339-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09339-135">RELATED LINKS</span></span>
