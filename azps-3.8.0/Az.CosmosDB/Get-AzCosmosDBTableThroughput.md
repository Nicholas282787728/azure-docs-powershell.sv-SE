---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 684572dd9b43f68eab0497d2603fea30c747415a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091831"
---
# <span data-ttu-id="ee7fd-101">Get-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="ee7fd-101">Get-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="ee7fd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ee7fd-102">SYNOPSIS</span></span>
<span data-ttu-id="ee7fd-103">Hämtar genomflödet för en CosmosDB-tabell.</span><span class="sxs-lookup"><span data-stu-id="ee7fd-103">Gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="ee7fd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ee7fd-104">SYNTAX</span></span>

### <span data-ttu-id="ee7fd-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="ee7fd-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTableThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee7fd-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee7fd-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTableThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee7fd-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ee7fd-107">DESCRIPTION</span></span>
<span data-ttu-id="ee7fd-108">Cmdleten **Get-AzCosmosDBTableThroughput** hämtar data flödet för en CosmosDB-tabell.</span><span class="sxs-lookup"><span data-stu-id="ee7fd-108">The **Get-AzCosmosDBTableThroughput** cmdlet gets the throughput of a CosmosDB Table.</span></span>

## <span data-ttu-id="ee7fd-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ee7fd-109">EXAMPLES</span></span>

### <span data-ttu-id="ee7fd-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="ee7fd-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTableThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="ee7fd-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ee7fd-111">PARAMETERS</span></span>

### <span data-ttu-id="ee7fd-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ee7fd-112">-AccountName</span></span>
<span data-ttu-id="ee7fd-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="ee7fd-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="ee7fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee7fd-114">-DefaultProfile</span></span>
<span data-ttu-id="ee7fd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ee7fd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee7fd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee7fd-116">-InputObject</span></span>
<span data-ttu-id="ee7fd-117">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="ee7fd-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee7fd-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="ee7fd-118">-Name</span></span>
<span data-ttu-id="ee7fd-119">Namnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="ee7fd-119">Name of the Table.</span></span>

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

### <span data-ttu-id="ee7fd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee7fd-120">-ResourceGroupName</span></span>
<span data-ttu-id="ee7fd-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ee7fd-121">Name of resource group.</span></span>

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

### <span data-ttu-id="ee7fd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee7fd-122">CommonParameters</span></span>
<span data-ttu-id="ee7fd-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee7fd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee7fd-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee7fd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee7fd-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ee7fd-125">INPUTS</span></span>

### <span data-ttu-id="ee7fd-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="ee7fd-126">None</span></span>

## <span data-ttu-id="ee7fd-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ee7fd-127">OUTPUTS</span></span>

### <span data-ttu-id="ee7fd-128">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="ee7fd-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="ee7fd-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ee7fd-129">NOTES</span></span>

## <span data-ttu-id="ee7fd-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ee7fd-130">RELATED LINKS</span></span>
