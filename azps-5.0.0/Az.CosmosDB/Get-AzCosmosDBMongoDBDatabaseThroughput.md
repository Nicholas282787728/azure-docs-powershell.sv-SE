---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321675"
---
# <span data-ttu-id="a9fdf-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="a9fdf-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="a9fdf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fdf-103">Hämtar CosmosDB genomflöde-egenskaper för MongoDB-databas.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="a9fdf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9fdf-104">SYNTAX</span></span>

### <span data-ttu-id="a9fdf-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a9fdf-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9fdf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9fdf-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9fdf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9fdf-107">DESCRIPTION</span></span>
<span data-ttu-id="a9fdf-108">Cmdleten **Get-AzCosmosDBMongoDBDatabaseThroughput** hämtar genomflödet-egenskaperna för MongoDB-databasen.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="a9fdf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9fdf-109">EXAMPLES</span></span>

### <span data-ttu-id="a9fdf-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a9fdf-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="a9fdf-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9fdf-111">PARAMETERS</span></span>

### <span data-ttu-id="a9fdf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a9fdf-112">-AccountName</span></span>
<span data-ttu-id="a9fdf-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a9fdf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fdf-114">-DefaultProfile</span></span>
<span data-ttu-id="a9fdf-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9fdf-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9fdf-116">-InputObject</span></span>
<span data-ttu-id="a9fdf-117">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a9fdf-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9fdf-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9fdf-118">-Name</span></span>
<span data-ttu-id="a9fdf-119">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-119">Database name.</span></span>

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

### <span data-ttu-id="a9fdf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fdf-120">-ResourceGroupName</span></span>
<span data-ttu-id="a9fdf-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-121">Name of resource group.</span></span>

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

### <span data-ttu-id="a9fdf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fdf-122">CommonParameters</span></span>
<span data-ttu-id="a9fdf-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fdf-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9fdf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fdf-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9fdf-125">INPUTS</span></span>

### <span data-ttu-id="a9fdf-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="a9fdf-126">None</span></span>

## <span data-ttu-id="a9fdf-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9fdf-127">OUTPUTS</span></span>

### <span data-ttu-id="a9fdf-128">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="a9fdf-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="a9fdf-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9fdf-129">NOTES</span></span>

## <span data-ttu-id="a9fdf-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9fdf-130">RELATED LINKS</span></span>
