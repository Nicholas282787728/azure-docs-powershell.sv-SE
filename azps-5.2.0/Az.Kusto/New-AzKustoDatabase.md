---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: dc0b4ea1616c916edacaf4d5a4a2b431e7f7d113
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394880"
---
# <span data-ttu-id="75f2b-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="75f2b-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="75f2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="75f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="75f2b-103">Skapar eller uppdaterar en databas.</span><span class="sxs-lookup"><span data-stu-id="75f2b-103">Creates or updates a database.</span></span>

## <span data-ttu-id="75f2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="75f2b-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75f2b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="75f2b-105">DESCRIPTION</span></span>
<span data-ttu-id="75f2b-106">Skapar eller uppdaterar en databas.</span><span class="sxs-lookup"><span data-stu-id="75f2b-106">Creates or updates a database.</span></span>

## <span data-ttu-id="75f2b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="75f2b-107">EXAMPLES</span></span>

### <span data-ttu-id="75f2b-108">Exempel 1: skapa en ny Kusto-databas med namn</span><span class="sxs-lookup"><span data-stu-id="75f2b-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="75f2b-109">Kommandot ovan skapar en ny Kusto-databas med namnet "mykustodatabase" i det befintliga klustret "testnewkustocluster" i resurs gruppen "testrg".</span><span class="sxs-lookup"><span data-stu-id="75f2b-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="75f2b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="75f2b-110">PARAMETERS</span></span>

### <span data-ttu-id="75f2b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75f2b-111">-AsJob</span></span>
<span data-ttu-id="75f2b-112">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="75f2b-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f2b-113">-Kluster namn</span><span class="sxs-lookup"><span data-stu-id="75f2b-113">-ClusterName</span></span>
<span data-ttu-id="75f2b-114">Namnet på Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="75f2b-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="75f2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f2b-115">-DefaultProfile</span></span>
<span data-ttu-id="75f2b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="75f2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f2b-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="75f2b-117">-HotCachePeriod</span></span>
<span data-ttu-id="75f2b-118">Tiden som data ska behållas i cacheminnet för snabba frågor i TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="75f2b-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f2b-119">-Sort</span><span class="sxs-lookup"><span data-stu-id="75f2b-119">-Kind</span></span>
<span data-ttu-id="75f2b-120">Typ av databas</span><span class="sxs-lookup"><span data-stu-id="75f2b-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f2b-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="75f2b-121">-Location</span></span>
<span data-ttu-id="75f2b-122">Resurs plats.</span><span class="sxs-lookup"><span data-stu-id="75f2b-122">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f2b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="75f2b-123">-Name</span></span>
<span data-ttu-id="75f2b-124">Namnet på databasen i Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="75f2b-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f2b-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="75f2b-125">-NoWait</span></span>
<span data-ttu-id="75f2b-126">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="75f2b-126">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f2b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75f2b-127">-ResourceGroupName</span></span>
<span data-ttu-id="75f2b-128">Namnet på resurs gruppen som innehåller Kusto-klustret.</span><span class="sxs-lookup"><span data-stu-id="75f2b-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="75f2b-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="75f2b-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="75f2b-130">Den tid då informationen ska behållas innan den inte längre är tillgänglig för frågor i TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="75f2b-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f2b-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="75f2b-131">-SubscriptionId</span></span>
<span data-ttu-id="75f2b-132">Hämtar dina prenumerations uppgifter som unikt identifierar Microsoft Azure-prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="75f2b-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="75f2b-133">Prenumerations-ID: t utgör en del av URI: n för varje service samtal.</span><span class="sxs-lookup"><span data-stu-id="75f2b-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f2b-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="75f2b-134">-Confirm</span></span>
<span data-ttu-id="75f2b-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="75f2b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75f2b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75f2b-136">-WhatIf</span></span>
<span data-ttu-id="75f2b-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="75f2b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75f2b-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="75f2b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75f2b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f2b-139">CommonParameters</span></span>
<span data-ttu-id="75f2b-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f2b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f2b-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75f2b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f2b-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="75f2b-142">INPUTS</span></span>

## <span data-ttu-id="75f2b-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="75f2b-143">OUTPUTS</span></span>

### <span data-ttu-id="75f2b-144">Microsoft. Azure. PowerShell. cmdletar. Kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="75f2b-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="75f2b-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="75f2b-145">NOTES</span></span>

<span data-ttu-id="75f2b-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="75f2b-146">ALIASES</span></span>

## <span data-ttu-id="75f2b-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="75f2b-147">RELATED LINKS</span></span>

