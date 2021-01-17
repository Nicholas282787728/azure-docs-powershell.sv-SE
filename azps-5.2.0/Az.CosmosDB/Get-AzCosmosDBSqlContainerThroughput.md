---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405235"
---
# <span data-ttu-id="b88e2-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="b88e2-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="b88e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b88e2-102">SYNOPSIS</span></span>
<span data-ttu-id="b88e2-103">Hämtar de genomflöde-inställningar som motsvarar en CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="b88e2-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="b88e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b88e2-104">SYNTAX</span></span>

### <span data-ttu-id="b88e2-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b88e2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b88e2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b88e2-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b88e2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b88e2-107">DESCRIPTION</span></span>
<span data-ttu-id="b88e2-108">Cmdleten **Get-AzCosmosDBSqlContainerThroughput** hämtar de data flödes inställningar som motsvarar en CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="b88e2-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="b88e2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b88e2-109">EXAMPLES</span></span>

### <span data-ttu-id="b88e2-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b88e2-110">Example 1</span></span>
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

## <span data-ttu-id="b88e2-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b88e2-111">PARAMETERS</span></span>

### <span data-ttu-id="b88e2-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b88e2-112">-AccountName</span></span>
<span data-ttu-id="b88e2-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="b88e2-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b88e2-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b88e2-114">-DatabaseName</span></span>
<span data-ttu-id="b88e2-115">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="b88e2-115">Database name.</span></span>

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

### <span data-ttu-id="b88e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b88e2-116">-DefaultProfile</span></span>
<span data-ttu-id="b88e2-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b88e2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b88e2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b88e2-118">-InputObject</span></span>
<span data-ttu-id="b88e2-119">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="b88e2-119">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b88e2-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b88e2-120">-Name</span></span>
<span data-ttu-id="b88e2-121">Container namn.</span><span class="sxs-lookup"><span data-stu-id="b88e2-121">Container name.</span></span>

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

### <span data-ttu-id="b88e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b88e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="b88e2-123">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b88e2-123">Name of resource group.</span></span>

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

### <span data-ttu-id="b88e2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b88e2-124">CommonParameters</span></span>
<span data-ttu-id="b88e2-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b88e2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b88e2-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b88e2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b88e2-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b88e2-127">INPUTS</span></span>

### <span data-ttu-id="b88e2-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="b88e2-128">None</span></span>

## <span data-ttu-id="b88e2-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b88e2-129">OUTPUTS</span></span>

### <span data-ttu-id="b88e2-130">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="b88e2-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="b88e2-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b88e2-131">NOTES</span></span>

## <span data-ttu-id="b88e2-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b88e2-132">RELATED LINKS</span></span>
