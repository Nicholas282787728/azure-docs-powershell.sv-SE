---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925726"
---
# <span data-ttu-id="08649-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="08649-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="08649-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08649-102">SYNOPSIS</span></span>
<span data-ttu-id="08649-103">Skapar en ny CosmosDB Cassandra-kluster.</span><span class="sxs-lookup"><span data-stu-id="08649-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="08649-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08649-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08649-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08649-105">DESCRIPTION</span></span>
<span data-ttu-id="08649-106">**New-AzCosmosDBCassandraClusterKey** skapar en ny CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="08649-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="08649-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08649-107">EXAMPLES</span></span>

### <span data-ttu-id="08649-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="08649-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="08649-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08649-109">PARAMETERS</span></span>

### <span data-ttu-id="08649-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08649-110">-DefaultProfile</span></span>
<span data-ttu-id="08649-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08649-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08649-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="08649-112">-Name</span></span>
<span data-ttu-id="08649-113">Namn på Cassandra kluster nycklar.</span><span class="sxs-lookup"><span data-stu-id="08649-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="08649-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="08649-114">-OrderBy</span></span>
<span data-ttu-id="08649-115">Sortering av kluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="08649-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="08649-116">Möjliga värden är: "ASC", "DESC"</span><span class="sxs-lookup"><span data-stu-id="08649-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="08649-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08649-117">CommonParameters</span></span>
<span data-ttu-id="08649-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08649-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08649-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08649-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08649-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08649-120">INPUTS</span></span>

### <span data-ttu-id="08649-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="08649-121">None</span></span>

## <span data-ttu-id="08649-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08649-122">OUTPUTS</span></span>

### <span data-ttu-id="08649-123">Microsoft. Azure. commands. CosmosDB. Models. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="08649-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="08649-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08649-124">NOTES</span></span>

## <span data-ttu-id="08649-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08649-125">RELATED LINKS</span></span>
