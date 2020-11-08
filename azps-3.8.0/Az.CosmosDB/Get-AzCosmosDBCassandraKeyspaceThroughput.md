---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbcassandrakeyspacethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBCassandraKeyspaceThroughput.md
ms.openlocfilehash: 21a32bc2c3251d0069dcdb05d9eea29c52207ae8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091856"
---
# <span data-ttu-id="f0483-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span><span class="sxs-lookup"><span data-stu-id="f0483-101">Get-AzCosmosDBCassandraKeyspaceThroughput</span></span>

## <span data-ttu-id="f0483-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f0483-102">SYNOPSIS</span></span>
<span data-ttu-id="f0483-103">Hämtar genomflödet-värdet för Cassandra-tecken.</span><span class="sxs-lookup"><span data-stu-id="f0483-103">Gets the throughput value of the Cassandra Keyspace.</span></span>

## <span data-ttu-id="f0483-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f0483-104">SYNTAX</span></span>

### <span data-ttu-id="f0483-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f0483-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0483-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0483-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBCassandraKeyspaceThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0483-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f0483-107">DESCRIPTION</span></span>
<span data-ttu-id="f0483-108">Cmdleten **Get-AzCosmosDBCassandraKeyspaceThroughput** hämtar det genomflöde-objekt som motsvarar ett givet tecken.</span><span class="sxs-lookup"><span data-stu-id="f0483-108">The **Get-AzCosmosDBCassandraKeyspaceThroughput** cmdlet gets the throughput object corresponding to a given Keyspace.</span></span>

## <span data-ttu-id="f0483-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f0483-109">EXAMPLES</span></span>

### <span data-ttu-id="f0483-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f0483-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBCassandraKeyspaceThroughput -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {name}
```

## <span data-ttu-id="f0483-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f0483-111">PARAMETERS</span></span>

### <span data-ttu-id="f0483-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f0483-112">-AccountName</span></span>
<span data-ttu-id="f0483-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="f0483-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f0483-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0483-114">-DefaultProfile</span></span>
<span data-ttu-id="f0483-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f0483-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0483-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0483-116">-InputObject</span></span>
<span data-ttu-id="f0483-117">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f0483-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0483-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="f0483-118">-Name</span></span>
<span data-ttu-id="f0483-119">Namn på Cassandra-namnet.</span><span class="sxs-lookup"><span data-stu-id="f0483-119">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="f0483-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0483-120">-ResourceGroupName</span></span>
<span data-ttu-id="f0483-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f0483-121">Name of resource group.</span></span>

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

### <span data-ttu-id="f0483-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0483-122">CommonParameters</span></span>
<span data-ttu-id="f0483-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0483-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0483-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0483-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0483-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f0483-125">INPUTS</span></span>

### <span data-ttu-id="f0483-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="f0483-126">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="f0483-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f0483-127">OUTPUTS</span></span>

### <span data-ttu-id="f0483-128">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f0483-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f0483-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f0483-129">NOTES</span></span>

## <span data-ttu-id="f0483-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f0483-130">RELATED LINKS</span></span>
