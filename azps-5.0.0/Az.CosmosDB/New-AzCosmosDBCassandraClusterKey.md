---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321592"
---
# <span data-ttu-id="2d7d6-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="2d7d6-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="2d7d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2d7d6-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7d6-103">Skapar en ny CosmosDB Cassandra-kluster.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="2d7d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2d7d6-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d7d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2d7d6-105">DESCRIPTION</span></span>
<span data-ttu-id="2d7d6-106">**New-AzCosmosDBCassandraClusterKey** skapar en ny CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="2d7d6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2d7d6-107">EXAMPLES</span></span>

### <span data-ttu-id="2d7d6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2d7d6-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="2d7d6-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2d7d6-109">PARAMETERS</span></span>

### <span data-ttu-id="2d7d6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7d6-110">-DefaultProfile</span></span>
<span data-ttu-id="2d7d6-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d7d6-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="2d7d6-112">-Name</span></span>
<span data-ttu-id="2d7d6-113">Namn på Cassandra kluster nycklar.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="2d7d6-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="2d7d6-114">-OrderBy</span></span>
<span data-ttu-id="2d7d6-115">Sortering av kluster Cassandra.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="2d7d6-116">Möjliga värden är: "ASC", "DESC"</span><span class="sxs-lookup"><span data-stu-id="2d7d6-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="2d7d6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7d6-117">CommonParameters</span></span>
<span data-ttu-id="2d7d6-118">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d7d6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7d6-119">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d7d6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7d6-120">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2d7d6-120">INPUTS</span></span>

### <span data-ttu-id="2d7d6-121">Ingen</span><span class="sxs-lookup"><span data-stu-id="2d7d6-121">None</span></span>

## <span data-ttu-id="2d7d6-122">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2d7d6-122">OUTPUTS</span></span>

### <span data-ttu-id="2d7d6-123">Microsoft. Azure. commands. CosmosDB. Models. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="2d7d6-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="2d7d6-124">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2d7d6-124">NOTES</span></span>

## <span data-ttu-id="2d7d6-125">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2d7d6-125">RELATED LINKS</span></span>