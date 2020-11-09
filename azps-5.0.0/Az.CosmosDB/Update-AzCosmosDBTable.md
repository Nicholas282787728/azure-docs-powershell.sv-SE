---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321316"
---
# <span data-ttu-id="51dda-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="51dda-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="51dda-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="51dda-102">SYNOPSIS</span></span>
<span data-ttu-id="51dda-103">Uppdaterar tabellen CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="51dda-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="51dda-104">Utför en klient uppdaterings åtgärd genom att läsa den befintliga tabellen.</span><span class="sxs-lookup"><span data-stu-id="51dda-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="51dda-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="51dda-105">SYNTAX</span></span>

### <span data-ttu-id="51dda-106">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="51dda-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51dda-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51dda-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51dda-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51dda-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51dda-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="51dda-109">DESCRIPTION</span></span>
<span data-ttu-id="51dda-110">Uppdaterar tabellen CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="51dda-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="51dda-111">Utför en klient uppdaterings åtgärd genom att läsa den befintliga tabellen.</span><span class="sxs-lookup"><span data-stu-id="51dda-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="51dda-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="51dda-112">EXAMPLES</span></span>

### <span data-ttu-id="51dda-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="51dda-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="51dda-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="51dda-114">PARAMETERS</span></span>

### <span data-ttu-id="51dda-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="51dda-115">-AccountName</span></span>
<span data-ttu-id="51dda-116">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="51dda-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="51dda-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="51dda-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="51dda-118">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="51dda-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="51dda-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="51dda-119">-Confirm</span></span>
<span data-ttu-id="51dda-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="51dda-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51dda-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51dda-121">-DefaultProfile</span></span>
<span data-ttu-id="51dda-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="51dda-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51dda-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51dda-123">-InputObject</span></span>
<span data-ttu-id="51dda-124">Ett tabell objekt.</span><span class="sxs-lookup"><span data-stu-id="51dda-124">Table Object.</span></span>

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

### <span data-ttu-id="51dda-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="51dda-125">-Name</span></span>
<span data-ttu-id="51dda-126">Namnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="51dda-126">Name of the Table.</span></span>

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

### <span data-ttu-id="51dda-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="51dda-127">-ParentObject</span></span>
<span data-ttu-id="51dda-128">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="51dda-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="51dda-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51dda-129">-ResourceGroupName</span></span>
<span data-ttu-id="51dda-130">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="51dda-130">Name of resource group.</span></span>

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

### <span data-ttu-id="51dda-131">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="51dda-131">-Throughput</span></span>
<span data-ttu-id="51dda-132">Genomflödet i tabellen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="51dda-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="51dda-133">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="51dda-133">Default value is 400.</span></span>

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

### <span data-ttu-id="51dda-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51dda-134">-WhatIf</span></span>
<span data-ttu-id="51dda-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="51dda-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51dda-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="51dda-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51dda-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51dda-137">CommonParameters</span></span>
<span data-ttu-id="51dda-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51dda-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51dda-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51dda-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51dda-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="51dda-140">INPUTS</span></span>

### <span data-ttu-id="51dda-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="51dda-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="51dda-142">Microsoft. Azure. commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="51dda-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="51dda-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="51dda-143">OUTPUTS</span></span>

### <span data-ttu-id="51dda-144">Microsoft. Azure. commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="51dda-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="51dda-145">Microsoft. Azure. commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="51dda-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="51dda-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="51dda-146">NOTES</span></span>

## <span data-ttu-id="51dda-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="51dda-147">RELATED LINKS</span></span>
