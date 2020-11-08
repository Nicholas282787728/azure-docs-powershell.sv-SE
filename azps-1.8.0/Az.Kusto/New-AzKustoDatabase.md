---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: 33272012d81160a055bcd5d1eb0ef617787eed1e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916158"
---
# <span data-ttu-id="91518-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="91518-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="91518-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="91518-102">SYNOPSIS</span></span>
<span data-ttu-id="91518-103">Skapar en ny Kusto-databas i ett befintligt kluster.</span><span class="sxs-lookup"><span data-stu-id="91518-103">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="91518-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="91518-104">SYNTAX</span></span>

### <span data-ttu-id="91518-105">ByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="91518-105">ByNameAndResourceGroup (Default)</span></span>
```
New-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91518-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="91518-106">ByResourceId</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91518-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="91518-107">ByInputObject</span></span>
```
New-AzKustoDatabase -Name <String> -SoftDeletePeriodInDays <Int32> -HotCachePeriodInDays <Int32>
 [-InputObject] <PSKustoCluster> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91518-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="91518-108">DESCRIPTION</span></span>
<span data-ttu-id="91518-109">Skapar en ny Kusto-databas i ett befintligt kluster.</span><span class="sxs-lookup"><span data-stu-id="91518-109">Creates a new Kusto database in an existing cluster.</span></span>

## <span data-ttu-id="91518-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="91518-110">EXAMPLES</span></span>

### <span data-ttu-id="91518-111">Exempel 1 – Skapa en ny Kusto-databas efter namn</span><span class="sxs-lookup"><span data-stu-id="91518-111">Example 1 - Create a new Kusto database by name</span></span>

```
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase -SoftDeletePeriodInDays 4 -HotCachePeriodInDays 2

Name                   : mykustocluster/mykustodatabase
SoftDeletePeriodInDays : 4
HotCachePeriodInDays   : 2
Statistic              : Microsoft.Azure.Management.Kusto.Models.DatabaseStatistics
Id                     : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster/Databases/mykustodatabase
Location               : Central US
Type                   : Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="91518-112">Kommandot ovan skapar en ny Kusto-databas med namnet "mykustodatabase" i det befintliga klustret "mykustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="91518-112">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "mykustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="91518-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="91518-113">PARAMETERS</span></span>

### <span data-ttu-id="91518-114">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="91518-114">-ClusterName</span></span>
<span data-ttu-id="91518-115">Namnet på det kluster som du vill skapa databasen under.</span><span class="sxs-lookup"><span data-stu-id="91518-115">Name of cluster under which you want to create the database.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91518-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91518-116">-DefaultProfile</span></span>
<span data-ttu-id="91518-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="91518-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91518-118">-HotCachePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="91518-118">-HotCachePeriodInDays</span></span>
<span data-ttu-id="91518-119">Antalet dagar med data som ska behållas i cacheminnet för snabba frågor.</span><span class="sxs-lookup"><span data-stu-id="91518-119">The number of days of data that should be kept in cache for fast queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91518-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91518-120">-InputObject</span></span>
<span data-ttu-id="91518-121">Kusto.</span><span class="sxs-lookup"><span data-stu-id="91518-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91518-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="91518-122">-Name</span></span>
<span data-ttu-id="91518-123">Namn på databasen som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="91518-123">Name of the database to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91518-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91518-124">-ResourceGroupName</span></span>
<span data-ttu-id="91518-125">Namnet på den resurs grupp som klustret finns under.</span><span class="sxs-lookup"><span data-stu-id="91518-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91518-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91518-126">-ResourceId</span></span>
<span data-ttu-id="91518-127">Kusto-kluster-ResourceID.</span><span class="sxs-lookup"><span data-stu-id="91518-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91518-128">-SoftDeletePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="91518-128">-SoftDeletePeriodInDays</span></span>
<span data-ttu-id="91518-129">Antalet dagar som data ska sparas innan det upphör att vara tillgängligt för frågor.</span><span class="sxs-lookup"><span data-stu-id="91518-129">The number of days data should be kept before it stops being accessible to queries.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91518-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="91518-130">-Confirm</span></span>
<span data-ttu-id="91518-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="91518-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91518-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91518-132">-WhatIf</span></span>
<span data-ttu-id="91518-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="91518-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91518-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="91518-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91518-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91518-135">CommonParameters</span></span>
<span data-ttu-id="91518-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91518-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91518-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91518-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91518-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="91518-138">INPUTS</span></span>

### <span data-ttu-id="91518-139">System. String</span><span class="sxs-lookup"><span data-stu-id="91518-139">System.String</span></span>

### <span data-ttu-id="91518-140">Microsoft. Azure. commands. Kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="91518-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="91518-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="91518-141">OUTPUTS</span></span>

### <span data-ttu-id="91518-142">Microsoft. Azure. commands. Kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="91518-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="91518-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="91518-143">NOTES</span></span>

## <span data-ttu-id="91518-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="91518-144">RELATED LINKS</span></span>