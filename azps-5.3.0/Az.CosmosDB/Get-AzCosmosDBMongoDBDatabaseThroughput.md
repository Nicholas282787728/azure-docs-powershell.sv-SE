---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbmongodbdatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBMongoDBDatabaseThroughput.md
ms.openlocfilehash: f73d39c9b09c0ef44edacfc42f439ee444eedc4d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524374"
---
# <span data-ttu-id="64a3b-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="64a3b-101">Get-AzCosmosDBMongoDBDatabaseThroughput</span></span>

## <span data-ttu-id="64a3b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="64a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="64a3b-103">Hämtar CosmosDB genomflöde-egenskaper för MongoDB-databas.</span><span class="sxs-lookup"><span data-stu-id="64a3b-103">Gets the CosmosDB throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="64a3b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="64a3b-104">SYNTAX</span></span>

### <span data-ttu-id="64a3b-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="64a3b-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64a3b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64a3b-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBMongoDBDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64a3b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="64a3b-107">DESCRIPTION</span></span>
<span data-ttu-id="64a3b-108">Cmdleten **Get-AzCosmosDBMongoDBDatabaseThroughput** hämtar genomflödet-egenskaperna för MongoDB-databasen.</span><span class="sxs-lookup"><span data-stu-id="64a3b-108">The **Get-AzCosmosDBMongoDBDatabaseThroughput** cmdlet gets the throughput properties of MongoDB Database.</span></span>

## <span data-ttu-id="64a3b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="64a3b-109">EXAMPLES</span></span>

### <span data-ttu-id="64a3b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="64a3b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBMongoDBDatabaseThroughput -ResourceGroupName {rgName} -AccountName {accountName} -Name {databaseName}

Name: {throughputName}
Id: {Id}
Throughput: {value} 
MinimumThroughput: {value}
OfferReplacePending: {value}
```

## <span data-ttu-id="64a3b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="64a3b-111">PARAMETERS</span></span>

### <span data-ttu-id="64a3b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="64a3b-112">-AccountName</span></span>
<span data-ttu-id="64a3b-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="64a3b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="64a3b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64a3b-114">-DefaultProfile</span></span>
<span data-ttu-id="64a3b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="64a3b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64a3b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64a3b-116">-InputObject</span></span>
<span data-ttu-id="64a3b-117">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="64a3b-117">CosmosDB Account object</span></span>

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

### <span data-ttu-id="64a3b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="64a3b-118">-Name</span></span>
<span data-ttu-id="64a3b-119">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="64a3b-119">Database name.</span></span>

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

### <span data-ttu-id="64a3b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64a3b-120">-ResourceGroupName</span></span>
<span data-ttu-id="64a3b-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="64a3b-121">Name of resource group.</span></span>

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

### <span data-ttu-id="64a3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64a3b-122">CommonParameters</span></span>
<span data-ttu-id="64a3b-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64a3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64a3b-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64a3b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64a3b-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="64a3b-125">INPUTS</span></span>

### <span data-ttu-id="64a3b-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="64a3b-126">None</span></span>

## <span data-ttu-id="64a3b-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="64a3b-127">OUTPUTS</span></span>

### <span data-ttu-id="64a3b-128">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="64a3b-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="64a3b-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="64a3b-129">NOTES</span></span>

## <span data-ttu-id="64a3b-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="64a3b-130">RELATED LINKS</span></span>
