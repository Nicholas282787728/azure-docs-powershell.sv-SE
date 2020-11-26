---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainer.md
ms.openlocfilehash: 0090e63086614e64c8e1c6dfc46ede52ce18ec42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261935"
---
# <span data-ttu-id="2253f-101">Get-AzCosmosDBSqlContainer</span><span class="sxs-lookup"><span data-stu-id="2253f-101">Get-AzCosmosDBSqlContainer</span></span>

## <span data-ttu-id="2253f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2253f-102">SYNOPSIS</span></span>
<span data-ttu-id="2253f-103">Hämtar SQL-containern för CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2253f-103">Gets the CosmosDB Sql Container.</span></span>

## <span data-ttu-id="2253f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2253f-104">SYNTAX</span></span>

### <span data-ttu-id="2253f-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2253f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainer -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] -AccountName <String> -DatabaseName <String> [<CommonParameters>]
```

### <span data-ttu-id="2253f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2253f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainer [-Name <String>] -ParentObject <PSSqlDatabaseGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2253f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2253f-107">DESCRIPTION</span></span>
<span data-ttu-id="2253f-108">Cmdleten **Get-AzCosmosDBSqlContainer** hämtar listan över alla befintliga CosmosDB SQL-behållare för ett givet ResourceGroupName, AccountName och databasename och hämtar en enda CosmosDB SQL-behållare för ett givet ResourceGroupName, AccountName, databasename och ContainerName.</span><span class="sxs-lookup"><span data-stu-id="2253f-108">The **Get-AzCosmosDBSqlContainer** cmdlet gets the list of all existing CosmosDB Sql Containers for a given ResourceGroupName, AccountName and DatabaseName and gets a single CosmosDB Sql Container for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="2253f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2253f-109">EXAMPLES</span></span>

### <span data-ttu-id="2253f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2253f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainer -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName}

Name                     : {containerName1}
Id                       : Id
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetPropertiesResource
```

## <span data-ttu-id="2253f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2253f-111">PARAMETERS</span></span>

### <span data-ttu-id="2253f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2253f-112">-AccountName</span></span>
<span data-ttu-id="2253f-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="2253f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2253f-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2253f-114">-DatabaseName</span></span>
<span data-ttu-id="2253f-115">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="2253f-115">Database name.</span></span>

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

### <span data-ttu-id="2253f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2253f-116">-DefaultProfile</span></span>
<span data-ttu-id="2253f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2253f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2253f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2253f-118">-Name</span></span>
<span data-ttu-id="2253f-119">Container namn.</span><span class="sxs-lookup"><span data-stu-id="2253f-119">Container name.</span></span>

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

### <span data-ttu-id="2253f-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2253f-120">-ParentObject</span></span>
<span data-ttu-id="2253f-121">SQL-databasnamn.</span><span class="sxs-lookup"><span data-stu-id="2253f-121">Sql Database object.</span></span>

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

### <span data-ttu-id="2253f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2253f-122">-ResourceGroupName</span></span>
<span data-ttu-id="2253f-123">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2253f-123">Name of resource group.</span></span>

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

### <span data-ttu-id="2253f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2253f-124">CommonParameters</span></span>
<span data-ttu-id="2253f-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2253f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2253f-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2253f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2253f-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2253f-127">INPUTS</span></span>

### <span data-ttu-id="2253f-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="2253f-128">None</span></span>

## <span data-ttu-id="2253f-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2253f-129">OUTPUTS</span></span>

### <span data-ttu-id="2253f-130">Microsoft. Azure. commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="2253f-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="2253f-131">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2253f-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2253f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2253f-132">NOTES</span></span>

## <span data-ttu-id="2253f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2253f-133">RELATED LINKS</span></span>