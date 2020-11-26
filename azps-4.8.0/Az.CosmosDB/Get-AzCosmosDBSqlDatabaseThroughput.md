---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 7c3dea3fc8f7fd6bf4870e68e242917421647661
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260600"
---
# <span data-ttu-id="22d62-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="22d62-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="22d62-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="22d62-102">SYNOPSIS</span></span>
<span data-ttu-id="22d62-103">Hämtar genomflödet som motsvarar en CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="22d62-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="22d62-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="22d62-104">SYNTAX</span></span>

### <span data-ttu-id="22d62-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="22d62-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22d62-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22d62-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22d62-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="22d62-107">DESCRIPTION</span></span>
<span data-ttu-id="22d62-108">Cmdleten **Get-AzCosmosDBSqlDatabaseThroughput** hämtar de genomflöde-inställningar som motsvarar en CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="22d62-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="22d62-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="22d62-109">EXAMPLES</span></span>

### <span data-ttu-id="22d62-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="22d62-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="22d62-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="22d62-111">PARAMETERS</span></span>

### <span data-ttu-id="22d62-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="22d62-112">-AccountName</span></span>
<span data-ttu-id="22d62-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="22d62-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="22d62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d62-114">-DefaultProfile</span></span>
<span data-ttu-id="22d62-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="22d62-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22d62-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22d62-116">-InputObject</span></span>
<span data-ttu-id="22d62-117">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="22d62-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22d62-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="22d62-118">-Name</span></span>
<span data-ttu-id="22d62-119">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="22d62-119">Database name.</span></span>

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

### <span data-ttu-id="22d62-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d62-120">-ResourceGroupName</span></span>
<span data-ttu-id="22d62-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="22d62-121">Name of resource group.</span></span>

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

### <span data-ttu-id="22d62-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d62-122">CommonParameters</span></span>
<span data-ttu-id="22d62-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22d62-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d62-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22d62-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d62-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="22d62-125">INPUTS</span></span>

### <span data-ttu-id="22d62-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="22d62-126">None</span></span>

## <span data-ttu-id="22d62-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="22d62-127">OUTPUTS</span></span>

### <span data-ttu-id="22d62-128">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="22d62-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="22d62-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="22d62-129">NOTES</span></span>

## <span data-ttu-id="22d62-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="22d62-130">RELATED LINKS</span></span>