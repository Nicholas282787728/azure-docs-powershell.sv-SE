---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtablethroughput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTableThroughput.md
ms.openlocfilehash: 24e73409dbb28c99b7b678963dc53a4d38584f85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321315"
---
# <span data-ttu-id="52cc4-101">Update-AzCosmosDBTableThroughput</span><span class="sxs-lookup"><span data-stu-id="52cc4-101">Update-AzCosmosDBTableThroughput</span></span>

## <span data-ttu-id="52cc4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="52cc4-103">Uppdaterar genomflödet för en CosmosDB-tabell.</span><span class="sxs-lookup"><span data-stu-id="52cc4-103">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="52cc4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52cc4-104">SYNTAX</span></span>

### <span data-ttu-id="52cc4-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="52cc4-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52cc4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52cc4-106">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52cc4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52cc4-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTableThroughput [-Name <String>] -InputObject <PSTableGetResults> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52cc4-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52cc4-108">DESCRIPTION</span></span>
<span data-ttu-id="52cc4-109">Uppdaterar genomflödet för en CosmosDB-tabell.</span><span class="sxs-lookup"><span data-stu-id="52cc4-109">Updates the throughput value of a CosmosDB Table.</span></span>

## <span data-ttu-id="52cc4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52cc4-110">EXAMPLES</span></span>

### <span data-ttu-id="52cc4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52cc4-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTableThroughput -AccountName {myAccountName} -ResourceGroupName {myResourceGroupName} -Name {myTableName} -Throughput {updatedThroughputValue}
Name                : mxGp
Id                  : /subscriptions/{mySubscriptionId}/resourceGroups/{myResourceGroupName}/providers/Microsoft.DocumentDB/databaseAccounts/{myAccountName}/table/{myTableName}/throughputSettings/default
Throughput          : {updatedThroughputValue}
MinimumThroughput   : 400
OfferReplacePending :
```

## <span data-ttu-id="52cc4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52cc4-112">PARAMETERS</span></span>

### <span data-ttu-id="52cc4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="52cc4-113">-AccountName</span></span>
<span data-ttu-id="52cc4-114">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="52cc4-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="52cc4-115">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="52cc4-115">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="52cc4-116">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="52cc4-116">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="52cc4-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52cc4-117">-Confirm</span></span>
<span data-ttu-id="52cc4-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52cc4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52cc4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52cc4-119">-DefaultProfile</span></span>
<span data-ttu-id="52cc4-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52cc4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52cc4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52cc4-121">-InputObject</span></span>
<span data-ttu-id="52cc4-122">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="52cc4-122">CosmosDB Account object</span></span>

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

### <span data-ttu-id="52cc4-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="52cc4-123">-Name</span></span>
<span data-ttu-id="52cc4-124">Namnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="52cc4-124">Name of the Table.</span></span>

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

### <span data-ttu-id="52cc4-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="52cc4-125">-ParentObject</span></span>
<span data-ttu-id="52cc4-126">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="52cc4-126">CosmosDB Account object</span></span>

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

### <span data-ttu-id="52cc4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52cc4-127">-ResourceGroupName</span></span>
<span data-ttu-id="52cc4-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="52cc4-128">Name of resource group.</span></span>

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

### <span data-ttu-id="52cc4-129">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="52cc4-129">-Throughput</span></span>
<span data-ttu-id="52cc4-130">Genomflödet i tabellen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="52cc4-130">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="52cc4-131">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="52cc4-131">Default value is 400.</span></span>

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

### <span data-ttu-id="52cc4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52cc4-132">-WhatIf</span></span>
<span data-ttu-id="52cc4-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52cc4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52cc4-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52cc4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52cc4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52cc4-135">CommonParameters</span></span>
<span data-ttu-id="52cc4-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52cc4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52cc4-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52cc4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52cc4-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52cc4-138">INPUTS</span></span>

### <span data-ttu-id="52cc4-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="52cc4-139">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="52cc4-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52cc4-140">OUTPUTS</span></span>

### <span data-ttu-id="52cc4-141">Microsoft. Azure. commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="52cc4-141">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="52cc4-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52cc4-142">NOTES</span></span>

## <span data-ttu-id="52cc4-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52cc4-143">RELATED LINKS</span></span>
