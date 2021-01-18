---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: d6d00892a8650964fbe7560ffa8e5fe279fb103b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524386"
---
# <span data-ttu-id="2dbe2-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="2dbe2-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="2dbe2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2dbe2-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbe2-103">Hämtar genomflödet-värdet för Cassandra-tecken.</span><span class="sxs-lookup"><span data-stu-id="2dbe2-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="2dbe2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2dbe2-104">SYNTAX</span></span>

### <span data-ttu-id="2dbe2-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2dbe2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dbe2-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dbe2-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dbe2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2dbe2-107">DESCRIPTION</span></span>
<span data-ttu-id="2dbe2-108">Cmdleten **Get-AzCosmosDBCassandraKeyspaceThroughput** hämtar det genomflöde-objekt som motsvarar ett givet tecken.</span><span class="sxs-lookup"><span data-stu-id="2dbe2-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="2dbe2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2dbe2-109">EXAMPLES</span></span>

### <span data-ttu-id="2dbe2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2dbe2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="2dbe2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2dbe2-111">PARAMETERS</span></span>

### <span data-ttu-id="2dbe2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2dbe2-112">-AccountName</span></span>
<span data-ttu-id="2dbe2-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="2dbe2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2dbe2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbe2-114">-DefaultProfile</span></span>
<span data-ttu-id="2dbe2-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbe2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dbe2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dbe2-116">-InputObject</span></span>
<span data-ttu-id="2dbe2-117">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="2dbe2-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="2dbe2-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2dbe2-118">-Name</span></span>
<span data-ttu-id="2dbe2-119">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="2dbe2-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="2dbe2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dbe2-120">-ResourceGroupName</span></span>
<span data-ttu-id="2dbe2-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2dbe2-121">Name of resource group.</span></span>

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

### <span data-ttu-id="2dbe2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbe2-122">CommonParameters</span></span>
<span data-ttu-id="2dbe2-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dbe2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbe2-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dbe2-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbe2-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2dbe2-125">INPUTS</span></span>

### <span data-ttu-id="2dbe2-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2dbe2-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2dbe2-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2dbe2-127">OUTPUTS</span></span>

### <span data-ttu-id="2dbe2-128">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="2dbe2-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="2dbe2-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2dbe2-129">NOTES</span></span>

## <span data-ttu-id="2dbe2-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2dbe2-130">RELATED LINKS</span></span>
