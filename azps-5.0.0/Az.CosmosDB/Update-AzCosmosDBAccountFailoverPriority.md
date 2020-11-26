---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321400"
---
# <span data-ttu-id="bce89-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="bce89-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="bce89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bce89-102">SYNOPSIS</span></span>
<span data-ttu-id="bce89-103">{{Fyll i sammanfattningen}}</span><span class="sxs-lookup"><span data-stu-id="bce89-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="bce89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bce89-104">SYNTAX</span></span>

### <span data-ttu-id="bce89-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bce89-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce89-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bce89-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bce89-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bce89-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bce89-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bce89-108">DESCRIPTION</span></span>
<span data-ttu-id="bce89-109">{{Fyll i beskrivningen}}</span><span class="sxs-lookup"><span data-stu-id="bce89-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="bce89-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bce89-110">EXAMPLES</span></span>

### <span data-ttu-id="bce89-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bce89-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="bce89-112">FailoverPolicies uppdateras med Region1 som FailoverPriority 1, Region2 som FailoverPriority 2 och region3 som FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="bce89-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="bce89-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bce89-113">PARAMETERS</span></span>

### <span data-ttu-id="bce89-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bce89-114">-AsJob</span></span>
<span data-ttu-id="bce89-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bce89-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bce89-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bce89-116">-Confirm</span></span>
<span data-ttu-id="bce89-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bce89-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bce89-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce89-118">-DefaultProfile</span></span>
<span data-ttu-id="bce89-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bce89-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bce89-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="bce89-120">-FailoverPolicy</span></span>
<span data-ttu-id="bce89-121">Matris med strängar med region namn sorterade efter prioritet för växling vid fel.</span><span class="sxs-lookup"><span data-stu-id="bce89-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="bce89-122">Omöstern, väst</span><span class="sxs-lookup"><span data-stu-id="bce89-122">E.g eastus, westus</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce89-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bce89-123">-InputObject</span></span>
<span data-ttu-id="bce89-124">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="bce89-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bce89-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="bce89-125">-Name</span></span>
<span data-ttu-id="bce89-126">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="bce89-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bce89-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce89-127">-ResourceGroupName</span></span>
<span data-ttu-id="bce89-128">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bce89-128">Name of resource group.</span></span>

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

### <span data-ttu-id="bce89-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bce89-129">-ResourceId</span></span>
<span data-ttu-id="bce89-130">ResourceId för resursen.</span><span class="sxs-lookup"><span data-stu-id="bce89-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce89-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bce89-131">-WhatIf</span></span>
<span data-ttu-id="bce89-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bce89-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bce89-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bce89-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bce89-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce89-134">CommonParameters</span></span>
<span data-ttu-id="bce89-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce89-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce89-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bce89-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce89-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bce89-137">INPUTS</span></span>

### <span data-ttu-id="bce89-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="bce89-138">None</span></span>

## <span data-ttu-id="bce89-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bce89-139">OUTPUTS</span></span>

### <span data-ttu-id="bce89-140">System. Void</span><span class="sxs-lookup"><span data-stu-id="bce89-140">System.Void</span></span>

## <span data-ttu-id="bce89-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bce89-141">NOTES</span></span>

## <span data-ttu-id="bce89-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bce89-142">RELATED LINKS</span></span>