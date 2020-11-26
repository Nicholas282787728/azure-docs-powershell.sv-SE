---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: 41494f860eea0ad811e9066d1fa8a45032b2317d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321468"
---
# <span data-ttu-id="b451b-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="b451b-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="b451b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b451b-102">SYNOPSIS</span></span>
<span data-ttu-id="b451b-103">Skapar en ny CosmosDB-tabell.</span><span class="sxs-lookup"><span data-stu-id="b451b-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="b451b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b451b-104">SYNTAX</span></span>

### <span data-ttu-id="b451b-105">ByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b451b-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b451b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b451b-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b451b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b451b-107">DESCRIPTION</span></span>
<span data-ttu-id="b451b-108">Skapar en ny CosmosDB-tabell.</span><span class="sxs-lookup"><span data-stu-id="b451b-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="b451b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b451b-109">EXAMPLES</span></span>

### <span data-ttu-id="b451b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b451b-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="b451b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b451b-111">PARAMETERS</span></span>

### <span data-ttu-id="b451b-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b451b-112">-AccountName</span></span>
<span data-ttu-id="b451b-113">Namn på Cosmos DB-databas.</span><span class="sxs-lookup"><span data-stu-id="b451b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b451b-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="b451b-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="b451b-115">Maximalt genomflöde-värde om Autoskala är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="b451b-115">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="b451b-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b451b-116">-Confirm</span></span>
<span data-ttu-id="b451b-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b451b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b451b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b451b-118">-DefaultProfile</span></span>
<span data-ttu-id="b451b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b451b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b451b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b451b-120">-Name</span></span>
<span data-ttu-id="b451b-121">Namnet på tabellen.</span><span class="sxs-lookup"><span data-stu-id="b451b-121">Name of the Table.</span></span>

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

### <span data-ttu-id="b451b-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b451b-122">-ParentObject</span></span>
<span data-ttu-id="b451b-123">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b451b-123">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b451b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b451b-124">-ResourceGroupName</span></span>
<span data-ttu-id="b451b-125">Namn på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b451b-125">Name of resource group.</span></span>

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

### <span data-ttu-id="b451b-126">-Genomflöde</span><span class="sxs-lookup"><span data-stu-id="b451b-126">-Throughput</span></span>
<span data-ttu-id="b451b-127">Genomflödet i tabellen (RU/s).</span><span class="sxs-lookup"><span data-stu-id="b451b-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="b451b-128">Standardvärdet är 400.</span><span class="sxs-lookup"><span data-stu-id="b451b-128">Default value is 400.</span></span>

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

### <span data-ttu-id="b451b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b451b-129">-WhatIf</span></span>
<span data-ttu-id="b451b-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b451b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b451b-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b451b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b451b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b451b-132">CommonParameters</span></span>
<span data-ttu-id="b451b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b451b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b451b-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b451b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b451b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b451b-135">INPUTS</span></span>

### <span data-ttu-id="b451b-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="b451b-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="b451b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b451b-137">OUTPUTS</span></span>

### <span data-ttu-id="b451b-138">Microsoft. Azure. commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="b451b-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="b451b-139">Microsoft. Azure. commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="b451b-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="b451b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b451b-140">NOTES</span></span>

## <span data-ttu-id="b451b-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b451b-141">RELATED LINKS</span></span>