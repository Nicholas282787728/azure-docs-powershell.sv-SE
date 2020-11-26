---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 009048c5f37936d469fe88c5e75cab8270efa81c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102988"
---
# <span data-ttu-id="d9a65-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="d9a65-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="d9a65-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9a65-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a65-103">Använd det här alternativet om du vill migrera AutoScale-genomströmning till manuell genomflöde och vice versa.</span><span class="sxs-lookup"><span data-stu-id="d9a65-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="d9a65-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9a65-104">SYNTAX</span></span>

### <span data-ttu-id="d9a65-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d9a65-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a65-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9a65-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a65-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9a65-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a65-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9a65-108">DESCRIPTION</span></span>
<span data-ttu-id="d9a65-109">ThroughpyteType parameter definierar den genomflöde som du vill migrera till.</span><span class="sxs-lookup"><span data-stu-id="d9a65-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="d9a65-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9a65-110">EXAMPLES</span></span>

### <span data-ttu-id="d9a65-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d9a65-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="d9a65-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9a65-112">PARAMETERS</span></span>

### <span data-ttu-id="d9a65-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d9a65-113">-AccountName</span></span>
<span data-ttu-id="d9a65-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="d9a65-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d9a65-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9a65-115">-Confirm</span></span>
<span data-ttu-id="d9a65-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9a65-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9a65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a65-117">-DefaultProfile</span></span>
<span data-ttu-id="d9a65-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9a65-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9a65-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9a65-119">-InputObject</span></span>
<span data-ttu-id="d9a65-120">Ett tabell objekt.</span><span class="sxs-lookup"><span data-stu-id="d9a65-120">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a65-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9a65-121">-Name</span></span>
<span data-ttu-id="d9a65-122">Namnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="d9a65-122">Name of the Table.</span></span>

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

### <span data-ttu-id="d9a65-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d9a65-123">-ParentObject</span></span>
<span data-ttu-id="d9a65-124">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d9a65-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="d9a65-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9a65-125">-ResourceGroupName</span></span>
<span data-ttu-id="d9a65-126">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d9a65-126">Name of resource group.</span></span>

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

### <span data-ttu-id="d9a65-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="d9a65-127">-ThroughputType</span></span>
<span data-ttu-id="d9a65-128">Data flödes typ att migrera till.</span><span class="sxs-lookup"><span data-stu-id="d9a65-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="d9a65-129">Möjliga värden är: Autoskala, manuell.</span><span class="sxs-lookup"><span data-stu-id="d9a65-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="d9a65-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a65-130">-WhatIf</span></span>
<span data-ttu-id="d9a65-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9a65-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9a65-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9a65-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9a65-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a65-133">CommonParameters</span></span>
<span data-ttu-id="d9a65-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a65-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a65-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9a65-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a65-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9a65-136">INPUTS</span></span>

### <span data-ttu-id="d9a65-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="d9a65-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="d9a65-138">Microsoft. Azure. commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="d9a65-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="d9a65-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9a65-139">OUTPUTS</span></span>

### <span data-ttu-id="d9a65-140">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="d9a65-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="d9a65-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9a65-141">NOTES</span></span>

## <span data-ttu-id="d9a65-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9a65-142">RELATED LINKS</span></span>