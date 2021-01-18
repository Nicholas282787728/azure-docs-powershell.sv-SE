---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEnvironment.md
ms.openlocfilehash: b4f27c31ebc3eb54727d6df1139409529c20eed9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522167"
---
# <span data-ttu-id="f8ed2-101">New-AzTimeSeriesInsightsEnvironment</span><span class="sxs-lookup"><span data-stu-id="f8ed2-101">New-AzTimeSeriesInsightsEnvironment</span></span>

## <span data-ttu-id="f8ed2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ed2-103">Skapa en miljö i den angivna abonnemangs-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-103">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="f8ed2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8ed2-104">SYNTAX</span></span>

### <span data-ttu-id="f8ed2-105">Gen1 (standard)</span><span class="sxs-lookup"><span data-stu-id="f8ed2-105">Gen1 (Default)</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Capacity <Int32>
 -DataRetentionTime <TimeSpan> -Kind <Kind> -Location <String> -Sku <SkuName> [-SubscriptionId <String>]
 [-PartitionKeyProperty <ITimeSeriesIdProperty[]>] [-StorageLimitExceededBehavior <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f8ed2-106">Gen2</span><span class="sxs-lookup"><span data-stu-id="f8ed2-106">Gen2</span></span>
```
New-AzTimeSeriesInsightsEnvironment -Name <String> -ResourceGroupName <String> -Kind <Kind> -Location <String>
 -Sku <SkuName> -StorageAccountKey <SecureString> -StorageAccountName <String>
 -TimeSeriesIdProperty <ITimeSeriesIdProperty[]> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-WarmStoreDataRetentionTime <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f8ed2-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8ed2-107">DESCRIPTION</span></span>
<span data-ttu-id="f8ed2-108">Skapa en miljö i den angivna abonnemangs-och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-108">Create an environment in the specified subscription and resource group.</span></span>

## <span data-ttu-id="f8ed2-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8ed2-109">EXAMPLES</span></span>

### <span data-ttu-id="f8ed2-110">Exempel 1: skapa en gen1 för tids serier</span><span class="sxs-lookup"><span data-stu-id="f8ed2-110">Example 1: Create a Gen1 time series insights environment</span></span>
```powershell
PS C:\> $TimeSpan = New-TimeSpan -Days 1 -Hours 1 -Minutes 25
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest001 -Kind Gen1 -Location eastus -Sku S1 -DataRetentionTime $TimeSpan -Capacity 2

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen1 eastus   tsitest001 2           S1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="f8ed2-111">Det här kommandot skapar en gen1 tids serie miljö.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-111">This command creates a Gen1 time series insights environment.</span></span>

### <span data-ttu-id="f8ed2-112">Exempel 2: skapa en Gen2 för tids serier</span><span class="sxs-lookup"><span data-stu-id="f8ed2-112">Example 2: Create a Gen2 time series insights environment</span></span>
```powershell
PS C:\> $ks = Get-AzStorageAccountKey -ResourceGroupName "testgroup" -Name "staccount001"
PS C:\> $k  = $ks[0].Value | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEnvironment -ResourceGroupName testgroup -Name tsitest002 -Kind Gen2 -Location eastus -Sku L1 -StorageAccountName staccount001 -StorageAccountKey $k -TimeSeriesIdProperty @{name='cdc';type='string'}

Kind     Location Name       SkuCapacity SkuName Type
----     -------- ----       ----------- ------- ----
Gen2 eastus   tsitest002 1           L1      Microsoft.TimeSeriesInsights/Environments
```

<span data-ttu-id="f8ed2-113">Det här kommandot skapar en Gen2 tids serie miljö.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-113">This command creates a Gen2 time series insights environment.</span></span>

## <span data-ttu-id="f8ed2-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8ed2-114">PARAMETERS</span></span>

### <span data-ttu-id="f8ed2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8ed2-115">-AsJob</span></span>
<span data-ttu-id="f8ed2-116">Köra kommandot som ett jobb</span><span class="sxs-lookup"><span data-stu-id="f8ed2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f8ed2-117">-Kapacitet</span><span class="sxs-lookup"><span data-stu-id="f8ed2-117">-Capacity</span></span>
<span data-ttu-id="f8ed2-118">Kapaciteten för SKU: n.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-118">The capacity of the sku.</span></span>
<span data-ttu-id="f8ed2-119">För gen1-miljöer kan det här värdet ändras för att stöd skalas utanför miljöer efter att de har skapats.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-119">For Gen1 environments, this value can be changed to support scale out of environments after they have been created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-120">-DataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="f8ed2-120">-DataRetentionTime</span></span>
<span data-ttu-id="f8ed2-121">Tiden för data lagring.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-121">The data retention time.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ed2-122">-DefaultProfile</span></span>
<span data-ttu-id="f8ed2-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8ed2-124">-Sort</span><span class="sxs-lookup"><span data-stu-id="f8ed2-124">-Kind</span></span>
<span data-ttu-id="f8ed2-125">Typen av miljö.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-125">The kind of the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-126">-Plats</span><span class="sxs-lookup"><span data-stu-id="f8ed2-126">-Location</span></span>
<span data-ttu-id="f8ed2-127">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-127">The location of the resource.</span></span>

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

### <span data-ttu-id="f8ed2-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8ed2-128">-Name</span></span>
<span data-ttu-id="f8ed2-129">Namnet på miljön</span><span class="sxs-lookup"><span data-stu-id="f8ed2-129">Name of the environment</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f8ed2-130">-NoWait</span></span>
<span data-ttu-id="f8ed2-131">Kör kommandot asynkront</span><span class="sxs-lookup"><span data-stu-id="f8ed2-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f8ed2-132">-PartitionKeyProperty</span><span class="sxs-lookup"><span data-stu-id="f8ed2-132">-PartitionKeyProperty</span></span>
<span data-ttu-id="f8ed2-133">Listan med händelse egenskaper som används för att partitionera data i miljön.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-133">The list of event properties which will be used to partition data in the environment.</span></span>
<span data-ttu-id="f8ed2-134">För att konstruera kan du läsa avsnittet anteckningar för PARTITIONKEYPROPERTY-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-134">To construct, see NOTES section for PARTITIONKEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8ed2-135">-ResourceGroupName</span></span>
<span data-ttu-id="f8ed2-136">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="f8ed2-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="f8ed2-137">-Sku</span></span>
<span data-ttu-id="f8ed2-138">Namnet på denna SKU.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-138">The name of this SKU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f8ed2-139">-StorageAccountKey</span></span>
<span data-ttu-id="f8ed2-140">Värdet för hanterings knappen som beviljar tjänsten tids serie insikter skriv åtkomst till lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-140">The value of the management key that grants the Time Series Insights service write access to the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f8ed2-141">-StorageAccountName</span></span>
<span data-ttu-id="f8ed2-142">Namnet på det lagrings konto som ska innehålla miljöns långsiktiga data.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-142">The name of the storage account that will hold the environment's long term data.</span></span>

```yaml
Type: System.String
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-143">-StorageLimitExceededBehavior</span><span class="sxs-lookup"><span data-stu-id="f8ed2-143">-StorageLimitExceededBehavior</span></span>
<span data-ttu-id="f8ed2-144">Beteendet för tids serie insikter bör tas när miljöns kapacitet har överskridits</span><span class="sxs-lookup"><span data-stu-id="f8ed2-144">The behavior the Time Series Insights service should take when the environment's capacity has been exceeded</span></span>

```yaml
Type: System.String
Parameter Sets: Gen1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f8ed2-145">-SubscriptionId</span></span>
<span data-ttu-id="f8ed2-146">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-146">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f8ed2-147">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f8ed2-147">-Tag</span></span>
<span data-ttu-id="f8ed2-148">Nyckeltal för fler egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-148">Key-value pairs of additional properties for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-149">-TimeSeriesIdProperty</span><span class="sxs-lookup"><span data-stu-id="f8ed2-149">-TimeSeriesIdProperty</span></span>
<span data-ttu-id="f8ed2-150">Listan med händelse egenskaper som används för att definiera miljöens tidsserie-ID. För att konstruera kan du läsa avsnittet anteckningar för TIMESERIESIDPROPERTY-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-150">The list of event properties which will be used to define the environment's time series id. To construct, see NOTES section for TIMESERIESIDPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.ITimeSeriesIdProperty[]
Parameter Sets: Gen2
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-151">-WarmStoreDataRetentionTime</span><span class="sxs-lookup"><span data-stu-id="f8ed2-151">-WarmStoreDataRetentionTime</span></span>
<span data-ttu-id="f8ed2-152">ISO8601 TimeSpan som anger hur många dagar miljöns händelser ska vara tillgängliga för frågor från det varmt Store.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-152">ISO8601 timespan specifying the number of days the environment's events will be available for query from the warm store.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: Gen2
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ed2-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f8ed2-153">-Confirm</span></span>
<span data-ttu-id="f8ed2-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8ed2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ed2-155">-WhatIf</span></span>
<span data-ttu-id="f8ed2-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8ed2-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8ed2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ed2-158">CommonParameters</span></span>
<span data-ttu-id="f8ed2-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ed2-160">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8ed2-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ed2-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8ed2-161">INPUTS</span></span>

## <span data-ttu-id="f8ed2-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8ed2-162">OUTPUTS</span></span>

### <span data-ttu-id="f8ed2-163">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IEnvironmentResource</span><span class="sxs-lookup"><span data-stu-id="f8ed2-163">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEnvironmentResource</span></span>

## <span data-ttu-id="f8ed2-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8ed2-164">NOTES</span></span>

<span data-ttu-id="f8ed2-165">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f8ed2-165">ALIASES</span></span>

<span data-ttu-id="f8ed2-166">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f8ed2-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f8ed2-167">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f8ed2-168">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f8ed2-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty [] >: listan med händelse egenskaper som används för att partitionera data i miljön.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-169">PARTITIONKEYPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to partition data in the environment.</span></span>
  - <span data-ttu-id="f8ed2-170">`[Name <String>]`: Namnet på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-170">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="f8ed2-171">`[Type <PropertyType?>]`: Typen av egenskap.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-171">`[Type <PropertyType?>]`: The type of the property.</span></span>

<span data-ttu-id="f8ed2-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty [] >: listan med händelse egenskaper som används för att ange miljöens tidsserie-ID.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-172">TIMESERIESIDPROPERTY <ITimeSeriesIdProperty[]>: The list of event properties which will be used to define the environment's time series id.</span></span>
  - <span data-ttu-id="f8ed2-173">`[Name <String>]`: Namnet på egenskapen.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-173">`[Name <String>]`: The name of the property.</span></span>
  - <span data-ttu-id="f8ed2-174">`[Type <PropertyType?>]`: Typen av egenskap.</span><span class="sxs-lookup"><span data-stu-id="f8ed2-174">`[Type <PropertyType?>]`: The type of the property.</span></span>

## <span data-ttu-id="f8ed2-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8ed2-175">RELATED LINKS</span></span>

