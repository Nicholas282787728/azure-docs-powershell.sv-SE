---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321591"
---
# <span data-ttu-id="4976f-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="4976f-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="4976f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4976f-102">SYNOPSIS</span></span>
<span data-ttu-id="4976f-103">Skapar en ny CosmosDB Cassandra-kolumn.</span><span class="sxs-lookup"><span data-stu-id="4976f-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="4976f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4976f-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4976f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4976f-105">DESCRIPTION</span></span>
<span data-ttu-id="4976f-106">Den **nya-AzCosmosDBCassandraColumn** skapar en ny CosmosDB-Cassandra-kolumn.</span><span class="sxs-lookup"><span data-stu-id="4976f-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="4976f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4976f-107">EXAMPLES</span></span>

### <span data-ttu-id="4976f-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4976f-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="4976f-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4976f-109">PARAMETERS</span></span>

### <span data-ttu-id="4976f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4976f-110">-DefaultProfile</span></span>
<span data-ttu-id="4976f-111">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4976f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4976f-112">-Namn</span><span class="sxs-lookup"><span data-stu-id="4976f-112">-Name</span></span>
<span data-ttu-id="4976f-113">Namn på kolumnen Cassandra.</span><span class="sxs-lookup"><span data-stu-id="4976f-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="4976f-114">– Skriv</span><span class="sxs-lookup"><span data-stu-id="4976f-114">-Type</span></span>
<span data-ttu-id="4976f-115">Typ av Cassandra-kolumn.</span><span class="sxs-lookup"><span data-stu-id="4976f-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="4976f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4976f-116">CommonParameters</span></span>
<span data-ttu-id="4976f-117">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4976f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4976f-118">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4976f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4976f-119">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4976f-119">INPUTS</span></span>

### <span data-ttu-id="4976f-120">Ingen</span><span class="sxs-lookup"><span data-stu-id="4976f-120">None</span></span>

## <span data-ttu-id="4976f-121">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4976f-121">OUTPUTS</span></span>

### <span data-ttu-id="4976f-122">Microsoft. Azure. commands. CosmosDB. Models. PSColumn</span><span class="sxs-lookup"><span data-stu-id="4976f-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="4976f-123">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4976f-123">NOTES</span></span>

## <span data-ttu-id="4976f-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4976f-124">RELATED LINKS</span></span>