---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBTable.md
ms.openlocfilehash: 9499933ef8e7b9e815d1438778a65f8abfdf7bff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089919"
---
# <span data-ttu-id="d80af-101">Set-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="d80af-101">Set-AzCosmosDBTable</span></span>

## <span data-ttu-id="d80af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d80af-102">SYNOPSIS</span></span>
<span data-ttu-id="d80af-103">Anger tabellen CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="d80af-103">Sets the CosmosDB Table.</span></span>

## <span data-ttu-id="d80af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d80af-104">SYNTAX</span></span>

### <span data-ttu-id="d80af-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d80af-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d80af-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d80af-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBTable -Name <String> [-Throughput <Int32>] -InputObject <PSDatabaseAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d80af-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d80af-107">DESCRIPTION</span></span>
<span data-ttu-id="d80af-108">Cmdleten **set-AzCosmosDBTable** skapar en ny tabell eller uppdaterar en befintlig tabell och ersätter den befintliga tabellen helt.</span><span class="sxs-lookup"><span data-stu-id="d80af-108">The **Set-AzCosmosDBTable** cmdlet creates a new Table or updates an existing Table, replacing the existing Table entirely.</span></span>

## <span data-ttu-id="d80af-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d80af-109">EXAMPLES</span></span>

### <span data-ttu-id="d80af-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d80af-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}

Name    Id    Resource
{name}  {id}  Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

<span data-ttu-id="d80af-111">Resurs objekt innehåller _rid _ts egenskaper för etag för tabellen.</span><span class="sxs-lookup"><span data-stu-id="d80af-111">Resource object contains _rid, _ts, _ etag properties of the Table.</span></span>

## <span data-ttu-id="d80af-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d80af-112">PARAMETERS</span></span>

### <span data-ttu-id="d80af-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d80af-113">-AccountName</span></span>
<span data-ttu-id="d80af-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="d80af-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d80af-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d80af-115">-Confirm</span></span>
<span data-ttu-id="d80af-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d80af-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d80af-117">-DefaultProfile</span></span>
<span data-ttu-id="d80af-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d80af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d80af-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d80af-119">-InputObject</span></span>
<span data-ttu-id="d80af-120">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d80af-120">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d80af-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d80af-121">-Name</span></span>
<span data-ttu-id="d80af-122">Namnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="d80af-122">Name of the Table.</span></span>

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

### <span data-ttu-id="d80af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d80af-123">-ResourceGroupName</span></span>
<span data-ttu-id="d80af-124">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d80af-124">Name of resource group.</span></span>

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

### <span data-ttu-id="d80af-125">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="d80af-125">-Throughput</span></span>
<span data-ttu-id="d80af-126">Genomflödet i tabellen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="d80af-126">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="d80af-127">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="d80af-127">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d80af-128">-WhatIf</span></span>
<span data-ttu-id="d80af-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d80af-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d80af-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d80af-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d80af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d80af-131">CommonParameters</span></span>
<span data-ttu-id="d80af-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d80af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d80af-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d80af-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d80af-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d80af-134">INPUTS</span></span>

### <span data-ttu-id="d80af-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="d80af-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="d80af-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d80af-136">OUTPUTS</span></span>

### <span data-ttu-id="d80af-137">Microsoft. Azure. commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="d80af-137">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="d80af-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d80af-138">NOTES</span></span>

## <span data-ttu-id="d80af-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d80af-139">RELATED LINKS</span></span>
