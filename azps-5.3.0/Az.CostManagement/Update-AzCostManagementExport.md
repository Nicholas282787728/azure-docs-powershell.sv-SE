---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/update-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Update-AzCostManagementExport.md
ms.openlocfilehash: 310600555f36fa0f6b129f2cf2a84581ffad044b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526371"
---
# <span data-ttu-id="1dabc-101">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="1dabc-101">Update-AzCostManagementExport</span></span>

## <span data-ttu-id="1dabc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1dabc-102">SYNOPSIS</span></span>
<span data-ttu-id="1dabc-103">Operationen för att skapa eller uppdatera en export.</span><span class="sxs-lookup"><span data-stu-id="1dabc-103">The operation to create or update a export.</span></span>
<span data-ttu-id="1dabc-104">Det krävs att den senaste eTag-åtgärden anges i begäran.</span><span class="sxs-lookup"><span data-stu-id="1dabc-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="1dabc-105">Du kan erhålla den senaste eTag-åtgärden genom att utföra en get-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="1dabc-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="1dabc-106">Skapa åtgärd kräver inte eTag.</span><span class="sxs-lookup"><span data-stu-id="1dabc-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="1dabc-107">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1dabc-107">SYNTAX</span></span>

### <span data-ttu-id="1dabc-108">UpdateExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="1dabc-108">UpdateExpanded (Default)</span></span>
```
Update-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1dabc-109">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1dabc-109">UpdateViaIdentityExpanded</span></span>
```
Update-AzCostManagementExport -InputObject <ICostManagementIdentity> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-ETag <String>] [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1dabc-110">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1dabc-110">DESCRIPTION</span></span>
<span data-ttu-id="1dabc-111">Operationen för att skapa eller uppdatera en export.</span><span class="sxs-lookup"><span data-stu-id="1dabc-111">The operation to create or update a export.</span></span>
<span data-ttu-id="1dabc-112">Det krävs att den senaste eTag-åtgärden anges i begäran.</span><span class="sxs-lookup"><span data-stu-id="1dabc-112">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="1dabc-113">Du kan erhålla den senaste eTag-åtgärden genom att utföra en get-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="1dabc-113">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="1dabc-114">Skapa åtgärd kräver inte eTag.</span><span class="sxs-lookup"><span data-stu-id="1dabc-114">Create operation does not require eTag.</span></span>

## <span data-ttu-id="1dabc-115">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1dabc-115">EXAMPLES</span></span>

### <span data-ttu-id="1dabc-116">Exempel 1: uppdatera AzCostManagementExport efter omfattning och namn</span><span class="sxs-lookup"><span data-stu-id="1dabc-116">Example 1: Update AzCostManagementExport by scope and name</span></span>
```powershell
PS C:\> Update-AzCostManagementExport -Scope "subscriptions//*********" -Name "TestExport" -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="1dabc-117">Uppdatera AzCostManagementExport efter omfattning och namn</span><span class="sxs-lookup"><span data-stu-id="1dabc-117">Update AzCostManagementExport by Scope and name</span></span>

### <span data-ttu-id="1dabc-118">Exempel 2: uppdatera AzCostManagementExport via InputObject</span><span class="sxs-lookup"><span data-stu-id="1dabc-118">Example 2: Update AzCostManagementExport by InputObject</span></span>
```powershell
PS C:\> $oldExport = Get-AzCostManagementExport -Scope "subscriptions/*********" -Name "TestExport"
Update-AzCostManagementExport -InputObject $oldExport -ScheduleRecurrence 'Weekly'

ETag              Name                                 Type
----              ----                                 ----
"********" TestExportDatasetAggregationInfo Microsoft.CostManagement/exports
```

<span data-ttu-id="1dabc-119">Uppdatera AzCostManagementExport via InputObject</span><span class="sxs-lookup"><span data-stu-id="1dabc-119">Update AzCostManagementExport by InputObject</span></span>

## <span data-ttu-id="1dabc-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1dabc-120">PARAMETERS</span></span>

### <span data-ttu-id="1dabc-121">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="1dabc-121">-ConfigurationColumn</span></span>
<span data-ttu-id="1dabc-122">Matris med kolumn namn som ska ingå i exporten.</span><span class="sxs-lookup"><span data-stu-id="1dabc-122">Array of column names to be included in the export.</span></span>
<span data-ttu-id="1dabc-123">Om det inte anges kommer exportera alla tillgängliga kolumner att tas med.</span><span class="sxs-lookup"><span data-stu-id="1dabc-123">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="1dabc-124">De tillgängliga kolumnerna kan variera beroende på kund kanal (se exempel).</span><span class="sxs-lookup"><span data-stu-id="1dabc-124">The available columns can vary by customer channel (see examples).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-125">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="1dabc-125">-DataSetGranularity</span></span>
<span data-ttu-id="1dabc-126">Hur många rader som är i exporten.</span><span class="sxs-lookup"><span data-stu-id="1dabc-126">The granularity of rows in the export.</span></span>
<span data-ttu-id="1dabc-127">För närvarande stöds endast "daglig".</span><span class="sxs-lookup"><span data-stu-id="1dabc-127">Currently only 'Daily' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.GranularityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dabc-128">-DefaultProfile</span></span>
<span data-ttu-id="1dabc-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1dabc-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dabc-130">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="1dabc-130">-DefinitionTimeframe</span></span>
<span data-ttu-id="1dabc-131">Tids ramen för att dra data för exporten.</span><span class="sxs-lookup"><span data-stu-id="1dabc-131">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="1dabc-132">Om du väljer Custom måste du ange en specifik tids period.</span><span class="sxs-lookup"><span data-stu-id="1dabc-132">If custom, then a specific time period must be provided.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-133">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="1dabc-133">-DefinitionType</span></span>
<span data-ttu-id="1dabc-134">Typ av export.</span><span class="sxs-lookup"><span data-stu-id="1dabc-134">The type of the export.</span></span>
<span data-ttu-id="1dabc-135">Observera att ' användning ' motsvarar ' ActualCost ' och gäller för export som ännu inte tillhandahåller data för debitering eller amortering för tjänste reservationer.</span><span class="sxs-lookup"><span data-stu-id="1dabc-135">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-136">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="1dabc-136">-DestinationContainer</span></span>
<span data-ttu-id="1dabc-137">Namnet på den behållare där exporten ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="1dabc-137">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="1dabc-138">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="1dabc-138">-DestinationResourceId</span></span>
<span data-ttu-id="1dabc-139">Resurs-ID för lagrings kontot där exporten levereras.</span><span class="sxs-lookup"><span data-stu-id="1dabc-139">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="1dabc-140">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="1dabc-140">-DestinationRootFolderPath</span></span>
<span data-ttu-id="1dabc-141">Namnet på den katalog där exporten ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="1dabc-141">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="1dabc-142">-ETag</span><span class="sxs-lookup"><span data-stu-id="1dabc-142">-ETag</span></span>
<span data-ttu-id="1dabc-143">eTag för resursen.</span><span class="sxs-lookup"><span data-stu-id="1dabc-143">eTag of the resource.</span></span>
<span data-ttu-id="1dabc-144">För att hantera samtidig uppdaterings scenario används det här fältet för att avgöra om användaren uppdaterar den senaste versionen eller inte.</span><span class="sxs-lookup"><span data-stu-id="1dabc-144">To handle concurrent update scenario, this field will be used to determine whether the user is updating the latest version or not.</span></span>

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

### <span data-ttu-id="1dabc-145">-Format</span><span class="sxs-lookup"><span data-stu-id="1dabc-145">-Format</span></span>
<span data-ttu-id="1dabc-146">Formatet för de som levereras.</span><span class="sxs-lookup"><span data-stu-id="1dabc-146">The format of the export being delivered.</span></span>
<span data-ttu-id="1dabc-147">För närvarande stöds endast CSV.</span><span class="sxs-lookup"><span data-stu-id="1dabc-147">Currently only 'Csv' is supported.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.FormatType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-148">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dabc-148">-InputObject</span></span>
<span data-ttu-id="1dabc-149">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="1dabc-149">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-150">-Namn</span><span class="sxs-lookup"><span data-stu-id="1dabc-150">-Name</span></span>
<span data-ttu-id="1dabc-151">Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="1dabc-151">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-152">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="1dabc-152">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="1dabc-153">Start datumet för återkommande.</span><span class="sxs-lookup"><span data-stu-id="1dabc-153">The start date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-154">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="1dabc-154">-RecurrencePeriodTo</span></span>
<span data-ttu-id="1dabc-155">Slutdatum för återkommande.</span><span class="sxs-lookup"><span data-stu-id="1dabc-155">The end date of recurrence.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-156">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="1dabc-156">-ScheduleRecurrence</span></span>
<span data-ttu-id="1dabc-157">Schemat.</span><span class="sxs-lookup"><span data-stu-id="1dabc-157">The schedule recurrence.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.RecurrenceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-158">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="1dabc-158">-ScheduleStatus</span></span>
<span data-ttu-id="1dabc-159">Statusen för exportens schema.</span><span class="sxs-lookup"><span data-stu-id="1dabc-159">The status of the export's schedule.</span></span>
<span data-ttu-id="1dabc-160">Om det är inaktivt pausas exportens schema.</span><span class="sxs-lookup"><span data-stu-id="1dabc-160">If 'Inactive', the export's schedule is paused.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.StatusType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-161">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="1dabc-161">-Scope</span></span>
<span data-ttu-id="1dabc-162">Den här parametern definierar omfattningen av costmanagement från olika perspektiv, "ResourceGroup" och "tillhandahåller tjänst".</span><span class="sxs-lookup"><span data-stu-id="1dabc-162">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-163">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="1dabc-163">-TimePeriodFrom</span></span>
<span data-ttu-id="1dabc-164">Start datum för export av data.</span><span class="sxs-lookup"><span data-stu-id="1dabc-164">The start date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-165">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="1dabc-165">-TimePeriodTo</span></span>
<span data-ttu-id="1dabc-166">Slutdatum för export av data.</span><span class="sxs-lookup"><span data-stu-id="1dabc-166">The end date for export data.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dabc-167">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1dabc-167">-Confirm</span></span>
<span data-ttu-id="1dabc-168">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1dabc-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dabc-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dabc-169">-WhatIf</span></span>
<span data-ttu-id="1dabc-170">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1dabc-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dabc-171">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1dabc-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dabc-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dabc-172">CommonParameters</span></span>
<span data-ttu-id="1dabc-173">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dabc-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dabc-174">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1dabc-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dabc-175">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1dabc-175">INPUTS</span></span>

### <span data-ttu-id="1dabc-176">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. ICostManagementIdentity</span><span class="sxs-lookup"><span data-stu-id="1dabc-176">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.ICostManagementIdentity</span></span>

## <span data-ttu-id="1dabc-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1dabc-177">OUTPUTS</span></span>

### <span data-ttu-id="1dabc-178">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="1dabc-178">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="1dabc-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1dabc-179">NOTES</span></span>

<span data-ttu-id="1dabc-180">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1dabc-180">ALIASES</span></span>

<span data-ttu-id="1dabc-181">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="1dabc-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1dabc-182">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="1dabc-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1dabc-183">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1dabc-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1dabc-184">INPUTOBJECT <ICostManagementIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="1dabc-184">INPUTOBJECT <ICostManagementIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1dabc-185">`[AlertId <String>]`: ID</span><span class="sxs-lookup"><span data-stu-id="1dabc-185">`[AlertId <String>]`: Alert ID</span></span>
  - <span data-ttu-id="1dabc-186">`[ExportName <String>]`: Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="1dabc-186">`[ExportName <String>]`: Export Name.</span></span>
  - <span data-ttu-id="1dabc-187">`[ExternalCloudProviderId <String>]`: Det kan vara ' {externalSubscriptionId} ' för det länkade kontot eller ' {externalBillingAccountId} ' för det konsoliderade kontot som används med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="1dabc-187">`[ExternalCloudProviderId <String>]`: This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>
  - <span data-ttu-id="1dabc-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: Typen av extern moln leverantör som är associerad med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="1dabc-188">`[ExternalCloudProviderType <ExternalCloudProviderType?>]`: The external cloud provider type associated with dimension/query operations.</span></span> <span data-ttu-id="1dabc-189">Detta inkluderar ' externalSubscriptions ' för det länkade kontot och ' externalBillingAccounts ' för konsoliderat konto.</span><span class="sxs-lookup"><span data-stu-id="1dabc-189">This includes 'externalSubscriptions' for linked account and 'externalBillingAccounts' for consolidated account.</span></span>
  - <span data-ttu-id="1dabc-190">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="1dabc-190">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1dabc-191">`[Scope <String>]`: Omfattningen som är associerad med vyn View.</span><span class="sxs-lookup"><span data-stu-id="1dabc-191">`[Scope <String>]`: The scope associated with view operations.</span></span> <span data-ttu-id="1dabc-192">Här ingår "prenumerationer/{subscriptionId}" för abonnemangs omfattningen, "prenumerationer/{subscriptionId}/resourceGroups/{resourceGroupName}" för resourceGroup omfattning "leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId} ' för fakturerings konto omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/avdelningar/{departmentId} "för avdelningens omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "för EnrollmentAccount omfattning" providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId} ' for BillingProfile scope "providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId} ' för InvoiceSection omfattning" providers/Microsoft. Management/managementGroups/{managementGroupId} "for Management Group scope," providers/Microsoft. CostManagement/externalBillingAccounts/{externalBillingAccountName} "för externa scope för fakturerings konto och" leverantörer/Microsoft. CostManagement/externalSubscriptions/{externalSubscriptionName} "för extern abonnemangs omfattning.</span><span class="sxs-lookup"><span data-stu-id="1dabc-192">This includes 'subscriptions/{subscriptionId}' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for BillingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/invoiceSections/{invoiceSectionId}' for InvoiceSection scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId}' for Management Group scope, 'providers/Microsoft.CostManagement/externalBillingAccounts/{externalBillingAccountName}' for External Billing Account scope and 'providers/Microsoft.CostManagement/externalSubscriptions/{externalSubscriptionName}' for External Subscription scope.</span></span>
  - <span data-ttu-id="1dabc-193">`[ViewName <String>]`: Vynamn</span><span class="sxs-lookup"><span data-stu-id="1dabc-193">`[ViewName <String>]`: View name</span></span>

## <span data-ttu-id="1dabc-194">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1dabc-194">RELATED LINKS</span></span>

