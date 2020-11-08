---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbsqldatabasethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBSqlDatabaseThroughput.md
ms.openlocfilehash: 9ba9c092f021041f1a56626a79e07b369b694d5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088288"
---
# <span data-ttu-id="61a4f-101">Get-AzCosmosDBSqlDatabaseThroughput</span><span class="sxs-lookup"><span data-stu-id="61a4f-101">Get-AzCosmosDBSqlDatabaseThroughput</span></span>

## <span data-ttu-id="61a4f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="61a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="61a4f-103">Hämtar genomflödet som motsvarar en CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="61a4f-103">Gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="61a4f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="61a4f-104">SYNTAX</span></span>

### <span data-ttu-id="61a4f-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="61a4f-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -ResourceGroupName <String> -AccountName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61a4f-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a4f-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBSqlDatabaseThroughput -Name <String> -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61a4f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="61a4f-107">DESCRIPTION</span></span>
<span data-ttu-id="61a4f-108">Cmdleten **Get-AzCosmosDBSqlDatabaseThroughput** hämtar de genomflöde-inställningar som motsvarar en CosmosDB SQL-databas.</span><span class="sxs-lookup"><span data-stu-id="61a4f-108">The **Get-AzCosmosDBSqlDatabaseThroughput** cmdlet gets the throughput settings corresponding to a CosmosDB Sql Database.</span></span>

## <span data-ttu-id="61a4f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="61a4f-109">EXAMPLES</span></span>

### <span data-ttu-id="61a4f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="61a4f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBSqlDatabaseThroughput -AccountName {accountName} -ResourceGroupName {resourceGroupName} -Name {databaseName}

Name                : {throughputResourceName}
Id                  : {throughputId}
Throughput          : 0
MinimumThroughput   :
OfferReplacePending :
```

## <span data-ttu-id="61a4f-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="61a4f-111">PARAMETERS</span></span>

### <span data-ttu-id="61a4f-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61a4f-112">-AccountName</span></span>
<span data-ttu-id="61a4f-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="61a4f-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="61a4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a4f-114">-DefaultProfile</span></span>
<span data-ttu-id="61a4f-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="61a4f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61a4f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61a4f-116">-InputObject</span></span>
<span data-ttu-id="61a4f-117">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="61a4f-117">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61a4f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="61a4f-118">-Name</span></span>
<span data-ttu-id="61a4f-119">Databas namn.</span><span class="sxs-lookup"><span data-stu-id="61a4f-119">Database name.</span></span>

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

### <span data-ttu-id="61a4f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a4f-120">-ResourceGroupName</span></span>
<span data-ttu-id="61a4f-121">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="61a4f-121">Name of resource group.</span></span>

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

### <span data-ttu-id="61a4f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a4f-122">CommonParameters</span></span>
<span data-ttu-id="61a4f-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a4f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a4f-124">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61a4f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a4f-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="61a4f-125">INPUTS</span></span>

### <span data-ttu-id="61a4f-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="61a4f-126">None</span></span>

## <span data-ttu-id="61a4f-127">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="61a4f-127">OUTPUTS</span></span>

### <span data-ttu-id="61a4f-128">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="61a4f-128">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="61a4f-129">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="61a4f-129">NOTES</span></span>

## <span data-ttu-id="61a4f-130">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="61a4f-130">RELATED LINKS</span></span>
