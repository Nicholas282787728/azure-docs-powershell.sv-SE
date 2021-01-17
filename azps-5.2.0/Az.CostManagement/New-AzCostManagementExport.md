---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/new-azcostmanagementexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/New-AzCostManagementExport.md
ms.openlocfilehash: edc0475a9d4299e1bd7346ab441a78b09905d59c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395563"
---
# <span data-ttu-id="d9dbf-101">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d9dbf-101">New-AzCostManagementExport</span></span>

## <span data-ttu-id="d9dbf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="d9dbf-103">Operationen för att skapa eller uppdatera en export.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-103">The operation to create or update a export.</span></span>
<span data-ttu-id="d9dbf-104">Det krävs att den senaste eTag-åtgärden anges i begäran.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-104">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d9dbf-105">Du kan erhålla den senaste eTag-åtgärden genom att utföra en get-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-105">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d9dbf-106">Skapa åtgärd kräver inte eTag.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-106">Create operation does not require eTag.</span></span>

## <span data-ttu-id="d9dbf-107">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9dbf-107">SYNTAX</span></span>

```
New-AzCostManagementExport -Name <String> -Scope <String> [-ConfigurationColumn <String[]>]
 [-DataSetGranularity <GranularityType>] [-DefinitionTimeframe <TimeframeType>] [-DefinitionType <ExportType>]
 [-DestinationContainer <String>] [-DestinationResourceId <String>] [-DestinationRootFolderPath <String>]
 [-Format <FormatType>] [-RecurrencePeriodFrom <DateTime>] [-RecurrencePeriodTo <DateTime>]
 [-ScheduleRecurrence <RecurrenceType>] [-ScheduleStatus <StatusType>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9dbf-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9dbf-108">DESCRIPTION</span></span>
<span data-ttu-id="d9dbf-109">Operationen för att skapa eller uppdatera en export.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-109">The operation to create or update a export.</span></span>
<span data-ttu-id="d9dbf-110">Det krävs att den senaste eTag-åtgärden anges i begäran.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-110">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="d9dbf-111">Du kan erhålla den senaste eTag-åtgärden genom att utföra en get-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-111">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="d9dbf-112">Skapa åtgärd kräver inte eTag.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-112">Create operation does not require eTag.</span></span>

## <span data-ttu-id="d9dbf-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9dbf-113">EXAMPLES</span></span>

### <span data-ttu-id="d9dbf-114">Exempel 1: skapa en AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d9dbf-114">Example 1: Create an AzCostManagementExport</span></span>
```powershell
PS C:\> New-AzCostManagementExport -Scope "subscriptions/***********" -Name "CostManagementExportTest" -ScheduleStatus "Active" -ScheduleRecurrence "Daily" -RecurrencePeriodFrom "2020-10-31T20:00:00Z" -RecurrencePeriodTo "2020-11-30T00:00:00Z" -Format "Csv" -DestinationResourceId "/subscriptions/*************/resourceGroups/ResourceGroupTest/providers/Microsoft.Storage/storageAccounts/storageAccountTest" `  -DestinationContainer "exports" -DestinationRootFolderPath "ad-hoc" -DefinitionType "Usage" -DefinitionTimeframe "MonthToDate" -DatasetGranularity "Daily"

ETag              Name                                      Type
----              ----                                      ----
"********" TestExportDatasetAggregationInfosagdhaghj Microsoft.CostManagement/exports
```

<span data-ttu-id="d9dbf-115">Skapa en AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="d9dbf-115">Create an AzCostManagementExport</span></span>

## <span data-ttu-id="d9dbf-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9dbf-116">PARAMETERS</span></span>

### <span data-ttu-id="d9dbf-117">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="d9dbf-117">-ConfigurationColumn</span></span>
<span data-ttu-id="d9dbf-118">Matris med kolumn namn som ska ingå i exporten.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-118">Array of column names to be included in the export.</span></span>
<span data-ttu-id="d9dbf-119">Om det inte anges kommer exportera alla tillgängliga kolumner att tas med.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-119">If not provided then the export will include all available columns.</span></span>
<span data-ttu-id="d9dbf-120">De tillgängliga kolumnerna kan variera beroende på kund kanal (se exempel).</span><span class="sxs-lookup"><span data-stu-id="d9dbf-120">The available columns can vary by customer channel (see examples).</span></span>

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

### <span data-ttu-id="d9dbf-121">-DataSetGranularity</span><span class="sxs-lookup"><span data-stu-id="d9dbf-121">-DataSetGranularity</span></span>
<span data-ttu-id="d9dbf-122">Hur många rader som är i exporten.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-122">The granularity of rows in the export.</span></span>
<span data-ttu-id="d9dbf-123">För närvarande stöds endast "daglig".</span><span class="sxs-lookup"><span data-stu-id="d9dbf-123">Currently only 'Daily' is supported.</span></span>

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

### <span data-ttu-id="d9dbf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9dbf-124">-DefaultProfile</span></span>
<span data-ttu-id="d9dbf-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9dbf-126">-DefinitionTimeframe</span><span class="sxs-lookup"><span data-stu-id="d9dbf-126">-DefinitionTimeframe</span></span>
<span data-ttu-id="d9dbf-127">Tids ramen för att dra data för exporten.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-127">The time frame for pulling data for the export.</span></span>
<span data-ttu-id="d9dbf-128">Om du väljer Custom måste du ange en specifik tids period.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-128">If custom, then a specific time period must be provided.</span></span>

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

### <span data-ttu-id="d9dbf-129">-DefinitionType</span><span class="sxs-lookup"><span data-stu-id="d9dbf-129">-DefinitionType</span></span>
<span data-ttu-id="d9dbf-130">Typ av export.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-130">The type of the export.</span></span>
<span data-ttu-id="d9dbf-131">Observera att ' användning ' motsvarar ' ActualCost ' och gäller för export som ännu inte tillhandahåller data för debitering eller amortering för tjänste reservationer.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-131">Note that 'Usage' is equivalent to 'ActualCost' and is applicable to exports that do not yet provide data for charges or amortization for service reservations.</span></span>

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

### <span data-ttu-id="d9dbf-132">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="d9dbf-132">-DestinationContainer</span></span>
<span data-ttu-id="d9dbf-133">Namnet på den behållare där exporten ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-133">The name of the container where exports will be uploaded.</span></span>

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

### <span data-ttu-id="d9dbf-134">-DestinationResourceId</span><span class="sxs-lookup"><span data-stu-id="d9dbf-134">-DestinationResourceId</span></span>
<span data-ttu-id="d9dbf-135">Resurs-ID för lagrings kontot där exporten levereras.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-135">The resource id of the storage account where exports will be delivered.</span></span>

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

### <span data-ttu-id="d9dbf-136">-DestinationRootFolderPath</span><span class="sxs-lookup"><span data-stu-id="d9dbf-136">-DestinationRootFolderPath</span></span>
<span data-ttu-id="d9dbf-137">Namnet på den katalog där exporten ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-137">The name of the directory where exports will be uploaded.</span></span>

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

### <span data-ttu-id="d9dbf-138">-Format</span><span class="sxs-lookup"><span data-stu-id="d9dbf-138">-Format</span></span>
<span data-ttu-id="d9dbf-139">Formatet för de som levereras.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-139">The format of the export being delivered.</span></span>
<span data-ttu-id="d9dbf-140">För närvarande stöds endast CSV.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-140">Currently only 'Csv' is supported.</span></span>

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

### <span data-ttu-id="d9dbf-141">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9dbf-141">-Name</span></span>
<span data-ttu-id="d9dbf-142">Exportera namn.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-142">Export Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExportName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9dbf-143">-RecurrencePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="d9dbf-143">-RecurrencePeriodFrom</span></span>
<span data-ttu-id="d9dbf-144">Start datumet för återkommande.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-144">The start date of recurrence.</span></span>

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

### <span data-ttu-id="d9dbf-145">-RecurrencePeriodTo</span><span class="sxs-lookup"><span data-stu-id="d9dbf-145">-RecurrencePeriodTo</span></span>
<span data-ttu-id="d9dbf-146">Slutdatum för återkommande.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-146">The end date of recurrence.</span></span>

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

### <span data-ttu-id="d9dbf-147">-ScheduleRecurrence</span><span class="sxs-lookup"><span data-stu-id="d9dbf-147">-ScheduleRecurrence</span></span>
<span data-ttu-id="d9dbf-148">Schemat.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-148">The schedule recurrence.</span></span>

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

### <span data-ttu-id="d9dbf-149">-ScheduleStatus</span><span class="sxs-lookup"><span data-stu-id="d9dbf-149">-ScheduleStatus</span></span>
<span data-ttu-id="d9dbf-150">Statusen för exportens schema.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-150">The status of the export's schedule.</span></span>
<span data-ttu-id="d9dbf-151">Om det är inaktivt pausas exportens schema.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-151">If 'Inactive', the export's schedule is paused.</span></span>

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

### <span data-ttu-id="d9dbf-152">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="d9dbf-152">-Scope</span></span>
<span data-ttu-id="d9dbf-153">Den här parametern definierar omfattningen av costmanagement från olika perspektiv, "ResourceGroup" och "tillhandahåller tjänst".</span><span class="sxs-lookup"><span data-stu-id="d9dbf-153">This parameter defines the scope of costmanagement from different perspectives 'Subscription','ResourceGroup' and 'Provide Service'.</span></span>

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

### <span data-ttu-id="d9dbf-154">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="d9dbf-154">-TimePeriodFrom</span></span>
<span data-ttu-id="d9dbf-155">Start datum för export av data.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-155">The start date for export data.</span></span>

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

### <span data-ttu-id="d9dbf-156">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="d9dbf-156">-TimePeriodTo</span></span>
<span data-ttu-id="d9dbf-157">Slutdatum för export av data.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-157">The end date for export data.</span></span>

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

### <span data-ttu-id="d9dbf-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9dbf-158">-Confirm</span></span>
<span data-ttu-id="d9dbf-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9dbf-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9dbf-160">-WhatIf</span></span>
<span data-ttu-id="d9dbf-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9dbf-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9dbf-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9dbf-163">CommonParameters</span></span>
<span data-ttu-id="d9dbf-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9dbf-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9dbf-165">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9dbf-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9dbf-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9dbf-166">INPUTS</span></span>

## <span data-ttu-id="d9dbf-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9dbf-167">OUTPUTS</span></span>

### <span data-ttu-id="d9dbf-168">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. Api20200601. IExport</span><span class="sxs-lookup"><span data-stu-id="d9dbf-168">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IExport</span></span>

## <span data-ttu-id="d9dbf-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9dbf-169">NOTES</span></span>

<span data-ttu-id="d9dbf-170">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d9dbf-170">ALIASES</span></span>

## <span data-ttu-id="d9dbf-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9dbf-171">RELATED LINKS</span></span>

