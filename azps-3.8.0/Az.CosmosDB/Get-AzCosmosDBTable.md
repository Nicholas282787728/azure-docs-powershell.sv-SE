---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBTable.md
ms.openlocfilehash: 7fb12f7413a0452a3e74f6fa03aa9a391dcacd26
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092608"
---
# <span data-ttu-id="f32b0-101">Get-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="f32b0-101">Get-AzCosmosDBTable</span></span>

## <span data-ttu-id="f32b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f32b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f32b0-103">Hämtar en CosmosDB-tabell.</span><span class="sxs-lookup"><span data-stu-id="f32b0-103">Gets a CosmosDB Table.</span></span>

## <span data-ttu-id="f32b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f32b0-104">SYNTAX</span></span>

### <span data-ttu-id="f32b0-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f32b0-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f32b0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f32b0-106">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBTable [-Name <String>] -InputObject <PSDatabaseAccount> [-Detailed]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f32b0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f32b0-107">DESCRIPTION</span></span>
<span data-ttu-id="f32b0-108">Cmdleten **Get-AzCosmosDBTable** hämtar en befintlig tabell.</span><span class="sxs-lookup"><span data-stu-id="f32b0-108">The **Get-AzCosmosDBTable** cmdlet gets an existing Table.</span></span>

## <span data-ttu-id="f32b0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f32b0-109">EXAMPLES</span></span>

### <span data-ttu-id="f32b0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f32b0-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="f32b0-111">Resurs objekt innehåller _rid _ts egenskaper för etag för tabellen.</span><span class="sxs-lookup"><span data-stu-id="f32b0-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="f32b0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f32b0-112">PARAMETERS</span></span>

### <span data-ttu-id="f32b0-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f32b0-113">-AccountName</span></span>
<span data-ttu-id="f32b0-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="f32b0-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f32b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f32b0-115">-DefaultProfile</span></span>
<span data-ttu-id="f32b0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f32b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f32b0-117">-Detaljerad</span><span class="sxs-lookup"><span data-stu-id="f32b0-117">-Detailed</span></span>
<span data-ttu-id="f32b0-118">Om den anges returnerar cmdleten tabellen med motsvarande genomflöde-värde.</span><span class="sxs-lookup"><span data-stu-id="f32b0-118">If provided then, the cmdlet returns the Table with the corresponding throughput value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32b0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f32b0-119">-InputObject</span></span>
<span data-ttu-id="f32b0-120">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="f32b0-120">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f32b0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f32b0-121">-Name</span></span>
<span data-ttu-id="f32b0-122">Namnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="f32b0-122">Name of the Table.</span></span>

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

### <span data-ttu-id="f32b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f32b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="f32b0-124">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f32b0-124">Name of resource group.</span></span>

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

### <span data-ttu-id="f32b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f32b0-125">CommonParameters</span></span>
<span data-ttu-id="f32b0-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f32b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f32b0-127">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f32b0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f32b0-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f32b0-128">INPUTS</span></span>

### <span data-ttu-id="f32b0-129">Ingen</span><span class="sxs-lookup"><span data-stu-id="f32b0-129">None</span></span>

## <span data-ttu-id="f32b0-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f32b0-130">OUTPUTS</span></span>

### <span data-ttu-id="f32b0-131">Microsoft. Azure. commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="f32b0-131">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="f32b0-132">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="f32b0-132">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="f32b0-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f32b0-133">NOTES</span></span>

## <span data-ttu-id="f32b0-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f32b0-134">RELATED LINKS</span></span>
