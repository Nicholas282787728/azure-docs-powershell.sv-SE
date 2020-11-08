---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088284"
---
# <span data-ttu-id="a8d45-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="a8d45-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="a8d45-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8d45-102">SYNOPSIS</span></span>
<span data-ttu-id="a8d45-103">Skapar ett nytt CosmosDB Cassandra-schema.</span><span class="sxs-lookup"><span data-stu-id="a8d45-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="a8d45-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8d45-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8d45-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8d45-105">DESCRIPTION</span></span>
<span data-ttu-id="a8d45-106">**New-AzCosmosDBCassandraSchema** skapar ett nytt CosmosDB Cassandra-schema.</span><span class="sxs-lookup"><span data-stu-id="a8d45-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="a8d45-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8d45-107">EXAMPLES</span></span>

### <span data-ttu-id="a8d45-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a8d45-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="a8d45-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8d45-109">PARAMETERS</span></span>

### <span data-ttu-id="a8d45-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="a8d45-110">-ClusterKey</span></span>
<span data-ttu-id="a8d45-111">Matris med PSClusterKey-objekt.</span><span class="sxs-lookup"><span data-stu-id="a8d45-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="a8d45-112">-Kolumn</span><span class="sxs-lookup"><span data-stu-id="a8d45-112">-Column</span></span>
<span data-ttu-id="a8d45-113">PSColumn-objekt.</span><span class="sxs-lookup"><span data-stu-id="a8d45-113">PSColumn object.</span></span>

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

### <span data-ttu-id="a8d45-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8d45-114">-DefaultProfile</span></span>
<span data-ttu-id="a8d45-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8d45-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8d45-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="a8d45-116">-PartitionKey</span></span>
<span data-ttu-id="a8d45-117">Matris med strängar som innehåller partitionsalternativ.</span><span class="sxs-lookup"><span data-stu-id="a8d45-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="a8d45-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8d45-118">CommonParameters</span></span>
<span data-ttu-id="a8d45-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8d45-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8d45-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8d45-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8d45-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8d45-121">INPUTS</span></span>

### <span data-ttu-id="a8d45-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="a8d45-122">None</span></span>

## <span data-ttu-id="a8d45-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8d45-123">OUTPUTS</span></span>

### <span data-ttu-id="a8d45-124">Microsoft. Azure. commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="a8d45-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="a8d45-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8d45-125">NOTES</span></span>

## <span data-ttu-id="a8d45-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8d45-126">RELATED LINKS</span></span>
