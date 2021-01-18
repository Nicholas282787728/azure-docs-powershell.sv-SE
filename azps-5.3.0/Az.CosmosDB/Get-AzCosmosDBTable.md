---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: d405c081ab1f848e25b67de4ec100f40b40fb4c8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524368"
---
# <span data-ttu-id="44d35-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="44d35-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="44d35-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44d35-102">SYNOPSIS</span></span>
<span data-ttu-id="44d35-103">Hämtar en CosmosDB-tabell.</span><span class="sxs-lookup"><span data-stu-id="44d35-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="44d35-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44d35-104">SYNTAX</span></span>

### <span data-ttu-id="44d35-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="44d35-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44d35-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44d35-106">ByParentObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44d35-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44d35-107">DESCRIPTION</span></span>
<span data-ttu-id="44d35-108">Cmdleten **Get-AzCosmosDBTable** hämtar en befintlig tabell.</span><span class="sxs-lookup"><span data-stu-id="44d35-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="44d35-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44d35-109">EXAMPLES</span></span>

### <span data-ttu-id="44d35-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="44d35-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="44d35-111">Resurs objekt innehåller _rid _ts egenskaper för etag för tabellen.</span><span class="sxs-lookup"><span data-stu-id="44d35-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="44d35-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44d35-112">PARAMETERS</span></span>

### <span data-ttu-id="44d35-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="44d35-113">-AccountName</span></span>
<span data-ttu-id="44d35-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="44d35-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="44d35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44d35-115">-DefaultProfile</span></span>
<span data-ttu-id="44d35-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44d35-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44d35-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="44d35-117">-Name</span></span>
<span data-ttu-id="44d35-118">Namnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="44d35-118">Name of the Table.</span></span>

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

### <span data-ttu-id="44d35-119">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="44d35-119">-ParentObject</span></span>
<span data-ttu-id="44d35-120">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="44d35-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="44d35-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44d35-121">-ResourceGroupName</span></span>
<span data-ttu-id="44d35-122">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="44d35-122">Name of resource group.</span></span>

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

### <span data-ttu-id="44d35-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d35-123">CommonParameters</span></span>
<span data-ttu-id="44d35-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44d35-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d35-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44d35-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d35-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44d35-126">INPUTS</span></span>

### <span data-ttu-id="44d35-127">Ingen</span><span class="sxs-lookup"><span data-stu-id="44d35-127">None</span></span>

## <span data-ttu-id="44d35-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44d35-128">OUTPUTS</span></span>

### <span data-ttu-id="44d35-129">Microsoft. Azure. commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="44d35-129">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="44d35-130">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="44d35-130">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="44d35-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44d35-131">NOTES</span></span>

## <span data-ttu-id="44d35-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44d35-132">RELATED LINKS</span></span>
