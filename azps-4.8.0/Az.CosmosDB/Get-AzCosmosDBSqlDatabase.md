---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 87c0436ce4aa62de7a1145d501e71783433b09eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261924"
---
# <span data-ttu-id="1a9d9-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1a9d9-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="1a9d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1a9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="1a9d9-103">Hämtar CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="1a9d9-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="1a9d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1a9d9-104">SYNTAX</span></span>

### <span data-ttu-id="1a9d9-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1a9d9-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a9d9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a9d9-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a9d9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1a9d9-107">DESCRIPTION</span></span>
<span data-ttu-id="1a9d9-108">Cmdleten **Get-AzCosmosDBSqlDatabase** hämtar listan över alla befintliga CosmosDB SQL-databaser för ett givet ResourceGroupName, AccountName och hämtar en enda CosmosDB SQL-databas för ett givet ResourceGroupName, AccountName, databasename och ContainerName.</span><span class="sxs-lookup"><span data-stu-id="1a9d9-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="1a9d9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1a9d9-109">EXAMPLES</span></span>

### <span data-ttu-id="1a9d9-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1a9d9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="1a9d9-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1a9d9-111">PARAMETERS</span></span>

### <span data-ttu-id="1a9d9-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a9d9-112">-AccountName</span></span>
<span data-ttu-id="1a9d9-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="1a9d9-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1a9d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a9d9-114">-DefaultProfile</span></span>
<span data-ttu-id="1a9d9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1a9d9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a9d9-116">-Namn</span><span class="sxs-lookup"><span data-stu-id="1a9d9-116">-Name</span></span>
<span data-ttu-id="1a9d9-117">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="1a9d9-117">Database name.</span></span>

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

### <span data-ttu-id="1a9d9-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1a9d9-118">-ParentObject</span></span>
<span data-ttu-id="1a9d9-119">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1a9d9-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a9d9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a9d9-120">-ResourceGroupName</span></span>
<span data-ttu-id="1a9d9-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1a9d9-121">Name of resource group.</span></span>

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

### <span data-ttu-id="1a9d9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a9d9-122">CommonParameters</span></span>
<span data-ttu-id="1a9d9-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a9d9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a9d9-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a9d9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a9d9-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1a9d9-125">INPUTS</span></span>

### <span data-ttu-id="1a9d9-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="1a9d9-126">None</span></span>

## <span data-ttu-id="1a9d9-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1a9d9-127">OUTPUTS</span></span>

### <span data-ttu-id="1a9d9-128">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="1a9d9-128">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="1a9d9-129">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="1a9d9-129">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="1a9d9-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1a9d9-130">NOTES</span></span>

## <span data-ttu-id="1a9d9-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1a9d9-131">RELATED LINKS</span></span>