---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabase.md
ms.openlocfilehash: 5efdbc3f1f8172ba59a78d4ec462f57a527faf07
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927917"
---
# <span data-ttu-id="2cd52-101">Get-AzCosmosDBSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2cd52-101">Get-AzCosmosDBSqlDatabase</span></span>

## <span data-ttu-id="2cd52-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2cd52-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd52-103">Hämtar CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="2cd52-103">Gets the CosmosDB Sql Database.</span></span>

## <span data-ttu-id="2cd52-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2cd52-104">SYNTAX</span></span>

### <span data-ttu-id="2cd52-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2cd52-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabase -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cd52-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2cd52-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabase [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cd52-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2cd52-107">DESCRIPTION</span></span>
<span data-ttu-id="2cd52-108">Cmdleten **Get-AzCosmosDBSqlDatabase** hämtar listan över alla befintliga CosmosDB SQL-databaser för ett givet ResourceGroupName, AccountName och hämtar en enda CosmosDB SQL-databas för ett givet ResourceGroupName, AccountName, databasename och ContainerName.</span><span class="sxs-lookup"><span data-stu-id="2cd52-108">The **Get-AzCosmosDBSqlDatabase** cmdlet gets the list of all existing CosmosDB Sql Databases for a given ResourceGroupName, AccountName and gets a single CosmosDB Sql Database for a given ResourceGroupName, AccountName, DatabaseName and ContainerName.</span></span>

## <span data-ttu-id="2cd52-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2cd52-109">EXAMPLES</span></span>

### <span data-ttu-id="2cd52-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2cd52-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabase -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                    : {databaseName}
Id                      : {databaseId}
Resource                 : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetPropertiesResource
```

## <span data-ttu-id="2cd52-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2cd52-111">PARAMETERS</span></span>

### <span data-ttu-id="2cd52-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2cd52-112">-AccountName</span></span>
<span data-ttu-id="2cd52-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="2cd52-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2cd52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd52-114">-DefaultProfile</span></span>
<span data-ttu-id="2cd52-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2cd52-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cd52-116">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="2cd52-116">-Detailed</span></span>
<span data-ttu-id="2cd52-117">Om den anges returnerar cmdleten den med genomflödet.</span><span class="sxs-lookup"><span data-stu-id="2cd52-117">If provided then, the cmdlet returns the container with the throughput value.</span></span>

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

### <span data-ttu-id="2cd52-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cd52-118">-InputObject</span></span>
<span data-ttu-id="2cd52-119">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="2cd52-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cd52-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="2cd52-120">-Name</span></span>
<span data-ttu-id="2cd52-121">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="2cd52-121">Database name.</span></span>

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

### <span data-ttu-id="2cd52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd52-122">-ResourceGroupName</span></span>
<span data-ttu-id="2cd52-123">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2cd52-123">Name of resource group.</span></span>

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

### <span data-ttu-id="2cd52-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd52-124">CommonParameters</span></span>
<span data-ttu-id="2cd52-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cd52-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd52-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cd52-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd52-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2cd52-127">INPUTS</span></span>

### <span data-ttu-id="2cd52-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="2cd52-128">None</span></span>

## <span data-ttu-id="2cd52-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2cd52-129">OUTPUTS</span></span>

### <span data-ttu-id="2cd52-130">Microsoft. Azure. commands. CosmosDB. Models. PSSqlDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="2cd52-130">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlDatabaseGetResults</span></span>

### <span data-ttu-id="2cd52-131">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2cd52-131">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2cd52-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2cd52-132">NOTES</span></span>

## <span data-ttu-id="2cd52-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2cd52-133">RELATED LINKS</span></span>
