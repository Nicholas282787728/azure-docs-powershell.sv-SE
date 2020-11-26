---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqlcontainerthroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlContainerThroughput.md
ms.openlocfilehash: f4e830cbcaab74b3cc70b201fd0f7f0557f2e840
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321668"
---
# <span data-ttu-id="21d21-101">Get-AzCosmosDBSqlContainerThroughput</span><span class="sxs-lookup"><span data-stu-id="21d21-101">Get-AzCosmosDBSqlContainerThroughput</span></span>

## <span data-ttu-id="21d21-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21d21-102">SYNOPSIS</span></span>
<span data-ttu-id="21d21-103">Hämtar de genomflöde-inställningar som motsvarar en CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="21d21-103">Gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span>

## <span data-ttu-id="21d21-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21d21-104">SYNTAX</span></span>

### <span data-ttu-id="21d21-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="21d21-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlContainerThroughput -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21d21-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21d21-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlContainerThroughput [-Name <String>] -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21d21-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21d21-107">DESCRIPTION</span></span>
<span data-ttu-id="21d21-108">Cmdleten **Get-AzCosmosDBSqlContainerThroughput** hämtar de data flödes inställningar som motsvarar en CosmosDB SQL-behållare.</span><span class="sxs-lookup"><span data-stu-id="21d21-108">The **Get-AzCosmosDBSqlContainerThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Container.</span></span> 

## <span data-ttu-id="21d21-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21d21-109">EXAMPLES</span></span>

### <span data-ttu-id="21d21-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="21d21-110">Example 1</span></span>
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

## <span data-ttu-id="21d21-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21d21-111">PARAMETERS</span></span>

### <span data-ttu-id="21d21-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="21d21-112">-AccountName</span></span>
<span data-ttu-id="21d21-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="21d21-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="21d21-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="21d21-114">-DatabaseName</span></span>
<span data-ttu-id="21d21-115">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="21d21-115">Database name.</span></span>

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

### <span data-ttu-id="21d21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d21-116">-DefaultProfile</span></span>
<span data-ttu-id="21d21-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="21d21-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21d21-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21d21-118">-InputObject</span></span>
<span data-ttu-id="21d21-119">SQL-behållarobjekt.</span><span class="sxs-lookup"><span data-stu-id="21d21-119">Sql Container object.</span></span>

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

### <span data-ttu-id="21d21-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="21d21-120">-Name</span></span>
<span data-ttu-id="21d21-121">Container namn.</span><span class="sxs-lookup"><span data-stu-id="21d21-121">Container name.</span></span>

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

### <span data-ttu-id="21d21-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d21-122">-ResourceGroupName</span></span>
<span data-ttu-id="21d21-123">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="21d21-123">Name of resource group.</span></span>

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

### <span data-ttu-id="21d21-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d21-124">CommonParameters</span></span>
<span data-ttu-id="21d21-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d21-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d21-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21d21-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d21-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21d21-127">INPUTS</span></span>

### <span data-ttu-id="21d21-128">Ingen</span><span class="sxs-lookup"><span data-stu-id="21d21-128">None</span></span>

## <span data-ttu-id="21d21-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21d21-129">OUTPUTS</span></span>

### <span data-ttu-id="21d21-130">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="21d21-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="21d21-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21d21-131">NOTES</span></span>

## <span data-ttu-id="21d21-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21d21-132">RELATED LINKS</span></span>