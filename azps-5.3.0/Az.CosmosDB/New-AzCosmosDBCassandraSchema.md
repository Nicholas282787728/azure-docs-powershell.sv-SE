---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524352"
---
# <span data-ttu-id="86d24-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="86d24-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="86d24-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="86d24-102">SYNOPSIS</span></span>
<span data-ttu-id="86d24-103">Skapar ett nytt CosmosDB Cassandra-schema.</span><span class="sxs-lookup"><span data-stu-id="86d24-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="86d24-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="86d24-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86d24-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="86d24-105">DESCRIPTION</span></span>
<span data-ttu-id="86d24-106">**New-AzCosmosDBCassandraSchema** skapar ett nytt CosmosDB Cassandra-schema.</span><span class="sxs-lookup"><span data-stu-id="86d24-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="86d24-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="86d24-107">EXAMPLES</span></span>

### <span data-ttu-id="86d24-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="86d24-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="86d24-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="86d24-109">PARAMETERS</span></span>

### <span data-ttu-id="86d24-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="86d24-110">-ClusterKey</span></span>
<span data-ttu-id="86d24-111">Matris med PSClusterKey-objekt.</span><span class="sxs-lookup"><span data-stu-id="86d24-111">Array of PSClusterKey objects.</span></span>

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d24-112">-Kolumn</span><span class="sxs-lookup"><span data-stu-id="86d24-112">-Column</span></span>
<span data-ttu-id="86d24-113">PSColumn-objekt.</span><span class="sxs-lookup"><span data-stu-id="86d24-113">PSColumn object.</span></span>

```yaml
Type: PSColumn[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d24-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d24-114">-DefaultProfile</span></span>
<span data-ttu-id="86d24-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="86d24-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86d24-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="86d24-116">-PartitionKey</span></span>
<span data-ttu-id="86d24-117">Matris med strängar som innehåller partitionsalternativ.</span><span class="sxs-lookup"><span data-stu-id="86d24-117">Array of strings containing Partition Keys.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d24-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d24-118">CommonParameters</span></span>
<span data-ttu-id="86d24-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d24-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d24-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86d24-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d24-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="86d24-121">INPUTS</span></span>

### <span data-ttu-id="86d24-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="86d24-122">None</span></span>

## <span data-ttu-id="86d24-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="86d24-123">OUTPUTS</span></span>

### <span data-ttu-id="86d24-124">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="86d24-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="86d24-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="86d24-125">NOTES</span></span>

## <span data-ttu-id="86d24-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="86d24-126">RELATED LINKS</span></span>
