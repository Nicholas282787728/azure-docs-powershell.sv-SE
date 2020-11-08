---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: 61acd388dabcfe71c83d282d032e9d4bb688d88b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091835"
---
# <span data-ttu-id="cdc42-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="cdc42-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="cdc42-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cdc42-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc42-103">Hämtar de genomflöde-inställningar som motsvarar en CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="cdc42-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="cdc42-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cdc42-104">SYNTAX</span></span>

### <span data-ttu-id="cdc42-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="cdc42-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cdc42-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdc42-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdc42-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cdc42-107">DESCRIPTION</span></span>
<span data-ttu-id="cdc42-108">Cmdleten **Get-AzCosmosDBSqlContainerThroughput** hämtar de data flödes inställningar som motsvarar en CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="cdc42-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="cdc42-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cdc42-109">EXAMPLES</span></span>

### <span data-ttu-id="cdc42-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cdc42-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlContainerThroughput  -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {containerName}

Throughput          : {throughputValue}
MinimumThroughput   :
OfferReplacePending :
Id                  : 
Name                : {Name}
Type                : Microsoft.DocumentDB/databaseAccounts/sqlDatabases/containers/throughputSettings
Location            :
Tags                :
```

## <span data-ttu-id="cdc42-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cdc42-111">PARAMETERS</span></span>

### <span data-ttu-id="cdc42-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cdc42-112">-AccountName</span></span>
<span data-ttu-id="cdc42-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="cdc42-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="cdc42-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cdc42-114">-DatabaseName</span></span>
<span data-ttu-id="cdc42-115">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="cdc42-115">Database name.</span></span>

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

### <span data-ttu-id="cdc42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc42-116">-DefaultProfile</span></span>
<span data-ttu-id="cdc42-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc42-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdc42-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdc42-118">-InputObject</span></span>
<span data-ttu-id="cdc42-119">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="cdc42-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc42-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="cdc42-120">-Name</span></span>
<span data-ttu-id="cdc42-121">Container namn.</span><span class="sxs-lookup"><span data-stu-id="cdc42-121">Container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdc42-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc42-122">-ResourceGroupName</span></span>
<span data-ttu-id="cdc42-123">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cdc42-123">Name of resource group.</span></span>

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

### <span data-ttu-id="cdc42-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc42-124">CommonParameters</span></span>
<span data-ttu-id="cdc42-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc42-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc42-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdc42-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc42-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cdc42-127">INPUTS</span></span>

### <span data-ttu-id="cdc42-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="cdc42-128">None</span></span>

## <span data-ttu-id="cdc42-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cdc42-129">OUTPUTS</span></span>

### <span data-ttu-id="cdc42-130">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="cdc42-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="cdc42-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cdc42-131">NOTES</span></span>

## <span data-ttu-id="cdc42-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cdc42-132">RELATED LINKS</span></span>
