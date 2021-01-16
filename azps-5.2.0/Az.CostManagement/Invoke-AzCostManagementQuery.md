---
external help file: ''
Module Name: Az.CostManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement/invoke-azcostmanagementquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Invoke-AzCostManagementQuery.md
ms.openlocfilehash: 1eec241ab9fba3f9e8daa3218b65140d644d56ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394224"
---
# <span data-ttu-id="0b324-101">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="0b324-101">Invoke-AzCostManagementQuery</span></span>

## <span data-ttu-id="0b324-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0b324-102">SYNOPSIS</span></span>
<span data-ttu-id="0b324-103">Söka efter definierade användnings data för området.</span><span class="sxs-lookup"><span data-stu-id="0b324-103">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="0b324-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0b324-104">SYNTAX</span></span>

### <span data-ttu-id="0b324-105">UsageExpanded (standard)</span><span class="sxs-lookup"><span data-stu-id="0b324-105">UsageExpanded (Default)</span></span>
```
Invoke-AzCostManagementQuery -Scope <String> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0b324-106">UsageExpanded1</span><span class="sxs-lookup"><span data-stu-id="0b324-106">UsageExpanded1</span></span>
```
Invoke-AzCostManagementQuery -ExternalCloudProviderId <String>
 -ExternalCloudProviderType <ExternalCloudProviderType> -Timeframe <TimeframeType> -Type <ExportType>
 [-ConfigurationColumn <String[]>] [-DatasetAggregation <Hashtable>] [-DatasetFilter <IQueryFilter>]
 [-DatasetGranularity <GranularityType>] [-DatasetGrouping <IQueryGrouping[]>] [-TimePeriodFrom <DateTime>]
 [-TimePeriodTo <DateTime>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b324-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0b324-107">DESCRIPTION</span></span>
<span data-ttu-id="0b324-108">Söka efter definierade användnings data för området.</span><span class="sxs-lookup"><span data-stu-id="0b324-108">Query the usage data for scope defined.</span></span>

## <span data-ttu-id="0b324-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0b324-109">EXAMPLES</span></span>

### <span data-ttu-id="0b324-110">Exempel 1: Invoke AzCostManagementQuery by scope</span><span class="sxs-lookup"><span data-stu-id="0b324-110">Example 1: Invoke AzCostManagementQuery by Scope</span></span>
```powershell
PS C:\> Invoke-AzCostManagementQuery -Scope "/subscriptions/***********" -Timeframe MonthToDate -Type Usage -DatasetGranularity 'Daily'

Column                Row
------                ---
{UsageDate, Currency} {20201101 USD, 20201102 USD, 20201103 USD, 20201104 USD…}
```

<span data-ttu-id="0b324-111">Anropa AzCostManagementQuery efter omfattning</span><span class="sxs-lookup"><span data-stu-id="0b324-111">Invoke AzCostManagementQuery by Scope</span></span>

### <span data-ttu-id="0b324-112">Exempel 2: anropa AzCostManagementQuery efter omfattning med dimensioner</span><span class="sxs-lookup"><span data-stu-id="0b324-112">Example 2: Invoke AzCostManagementQuery by Scope with Dimensions</span></span>
```powershell
PS C:\> $dimensions = New-AzCostManagementQueryComparisonExpressionObject -Name 'ResourceGroup' -Operator 'In' -Value 'API'
$filter = New-AzCostManagementQueryFilterObject -Dimensions $dimensions
Invoke-AzCostManagementQuery -Type Usage -Scope "subscriptions/***********" -DatasetGranularity 'Monthly' -DatasetFilter $filter -Timeframe MonthToDate -Debug


Column                   Row
------                   ---
{BillingMonth, Currency} {}
```

<span data-ttu-id="0b324-113">Anropa AzCostManagementQuery efter omfattning med dimensioner</span><span class="sxs-lookup"><span data-stu-id="0b324-113">Invoke AzCostManagementQuery by Scope with Dimensions</span></span>

## <span data-ttu-id="0b324-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0b324-114">PARAMETERS</span></span>

### <span data-ttu-id="0b324-115">-ConfigurationColumn</span><span class="sxs-lookup"><span data-stu-id="0b324-115">-ConfigurationColumn</span></span>
<span data-ttu-id="0b324-116">Matris med kolumn namn som ska inkluderas i frågan.</span><span class="sxs-lookup"><span data-stu-id="0b324-116">Array of column names to be included in the query.</span></span>

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

### <span data-ttu-id="0b324-117">-DatasetAggregation</span><span class="sxs-lookup"><span data-stu-id="0b324-117">-DatasetAggregation</span></span>
<span data-ttu-id="0b324-118">Ord lista med mängd uttryck som du vill använda i frågan.</span><span class="sxs-lookup"><span data-stu-id="0b324-118">Dictionary of aggregation expression to use in the query.</span></span>

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

### <span data-ttu-id="0b324-119">-DatasetFilter</span><span class="sxs-lookup"><span data-stu-id="0b324-119">-DatasetFilter</span></span>
<span data-ttu-id="0b324-120">Har ett filter uttryck som används i frågan.</span><span class="sxs-lookup"><span data-stu-id="0b324-120">Has filter expression to use in the query.</span></span>
<span data-ttu-id="0b324-121">För att konstruera kan du läsa avsnittet anteckningar för DATASETFILTER-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0b324-121">To construct, see NOTES section for DATASETFILTER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b324-122">-DatasetGranularity</span><span class="sxs-lookup"><span data-stu-id="0b324-122">-DatasetGranularity</span></span>
<span data-ttu-id="0b324-123">Hur detaljerad raderna i frågan är.</span><span class="sxs-lookup"><span data-stu-id="0b324-123">The granularity of rows in the query.</span></span>

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

### <span data-ttu-id="0b324-124">-DatasetGrouping</span><span class="sxs-lookup"><span data-stu-id="0b324-124">-DatasetGrouping</span></span>
<span data-ttu-id="0b324-125">Matris med Group by-uttryck som du vill använda i frågan.</span><span class="sxs-lookup"><span data-stu-id="0b324-125">Array of group by expression to use in the query.</span></span>
<span data-ttu-id="0b324-126">För att konstruera kan du läsa avsnittet anteckningar för DATASETGROUPING-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="0b324-126">To construct, see NOTES section for DATASETGROUPING properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryGrouping[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b324-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b324-127">-DefaultProfile</span></span>
<span data-ttu-id="0b324-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0b324-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b324-129">-ExternalCloudProviderId</span><span class="sxs-lookup"><span data-stu-id="0b324-129">-ExternalCloudProviderId</span></span>
<span data-ttu-id="0b324-130">Det här kan vara ' {externalSubscriptionId} ' för det länkade kontot eller ' {externalBillingAccountId} ' för det konsoliderade kontot som används med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="0b324-130">This can be '{externalSubscriptionId}' for linked account or '{externalBillingAccountId}' for consolidated account used with dimension/query operations.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b324-131">-ExternalCloudProviderType</span><span class="sxs-lookup"><span data-stu-id="0b324-131">-ExternalCloudProviderType</span></span>
<span data-ttu-id="0b324-132">Typen av extern moln leverantör som är associerad med dimension/frågor.</span><span class="sxs-lookup"><span data-stu-id="0b324-132">The external cloud provider type associated with dimension/query operations.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExternalCloudProviderType
Parameter Sets: UsageExpanded1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b324-133">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="0b324-133">-Scope</span></span>
<span data-ttu-id="0b324-134">Detta inkluderar "prenumerationer/{subscriptionId}/" för prenumerations omfattningen, "prenumerationer/{subscriptionId}/resourceGroups/{resourceGroupName}" för resourceGroup omfattning "leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId} ' för fakturerings konto omfattning och" leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/avdelningar/{departmentId} "för avdelningens omfattning," leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId} "för EnrollmentAccount omfattning" providers/Microsoft. Management/managementGroups/{managementGroupId} for Management Group scope, "providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}" för billingProfile omfattning "providers/Microsoft. fakturering/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId} ' för invoiceSection omfattning och ' leverantörer/Microsoft. fakturering/billingAccounts/{billingAccountId}/kunder/{customerId} är specifika för partner.</span><span class="sxs-lookup"><span data-stu-id="0b324-134">This includes 'subscriptions/{subscriptionId}/' for subscription scope, 'subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}' for resourceGroup scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}' for Billing Account scope and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/departments/{departmentId}' for Department scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/enrollmentAccounts/{enrollmentAccountId}' for EnrollmentAccount scope, 'providers/Microsoft.Management/managementGroups/{managementGroupId} for Management Group scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}' for billingProfile scope, 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/billingProfiles/{billingProfileId}/invoiceSections/{invoiceSectionId}' for invoiceSection scope, and 'providers/Microsoft.Billing/billingAccounts/{billingAccountId}/customers/{customerId}' specific for partners.</span></span>

```yaml
Type: System.String
Parameter Sets: UsageExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b324-135">-Tidsram</span><span class="sxs-lookup"><span data-stu-id="0b324-135">-Timeframe</span></span>
<span data-ttu-id="0b324-136">Tids ramen för att hämta data för frågan.</span><span class="sxs-lookup"><span data-stu-id="0b324-136">The time frame for pulling data for the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.TimeframeType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b324-137">-TimePeriodFrom</span><span class="sxs-lookup"><span data-stu-id="0b324-137">-TimePeriodFrom</span></span>
<span data-ttu-id="0b324-138">Start datum för att hämta data från.</span><span class="sxs-lookup"><span data-stu-id="0b324-138">The start date to pull data from.</span></span>

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

### <span data-ttu-id="0b324-139">-TimePeriodTo</span><span class="sxs-lookup"><span data-stu-id="0b324-139">-TimePeriodTo</span></span>
<span data-ttu-id="0b324-140">Slutdatum för att hämta data till.</span><span class="sxs-lookup"><span data-stu-id="0b324-140">The end date to pull data to.</span></span>

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

### <span data-ttu-id="0b324-141">– Skriv</span><span class="sxs-lookup"><span data-stu-id="0b324-141">-Type</span></span>
<span data-ttu-id="0b324-142">Frågetypen.</span><span class="sxs-lookup"><span data-stu-id="0b324-142">The type of the query.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Support.ExportType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b324-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0b324-143">-Confirm</span></span>
<span data-ttu-id="0b324-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0b324-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b324-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b324-145">-WhatIf</span></span>
<span data-ttu-id="0b324-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0b324-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b324-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0b324-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b324-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b324-148">CommonParameters</span></span>
<span data-ttu-id="0b324-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b324-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b324-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0b324-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b324-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0b324-151">INPUTS</span></span>

## <span data-ttu-id="0b324-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0b324-152">OUTPUTS</span></span>

### <span data-ttu-id="0b324-153">Microsoft. Azure. PowerShell. cmdletar. CostManagement. Models. Api20200601. IQueryResult</span><span class="sxs-lookup"><span data-stu-id="0b324-153">Microsoft.Azure.PowerShell.Cmdlets.CostManagement.Models.Api20200601.IQueryResult</span></span>

## <span data-ttu-id="0b324-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0b324-154">NOTES</span></span>

<span data-ttu-id="0b324-155">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0b324-155">ALIASES</span></span>

<span data-ttu-id="0b324-156">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="0b324-156">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0b324-157">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="0b324-157">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0b324-158">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0b324-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0b324-159">DATASETFILTER <IQueryFilter> : har filter uttryck som används i frågan.</span><span class="sxs-lookup"><span data-stu-id="0b324-159">DATASETFILTER <IQueryFilter>: Has filter expression to use in the query.</span></span>
  - <span data-ttu-id="0b324-160">`[And <IQueryFilter[]>]`: Det logiska uttrycket "och".</span><span class="sxs-lookup"><span data-stu-id="0b324-160">`[And <IQueryFilter[]>]`: The logical "AND" expression.</span></span> <span data-ttu-id="0b324-161">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="0b324-161">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0b324-162">`[Dimensions <IQueryComparisonExpression>]`: Jämförelse uttryck för en dimension</span><span class="sxs-lookup"><span data-stu-id="0b324-162">`[Dimensions <IQueryComparisonExpression>]`: Has comparison expression for a dimension</span></span>
    - <span data-ttu-id="0b324-163">`Name <String>`: Namnet på den kolumn som ska användas vid jämförelse.</span><span class="sxs-lookup"><span data-stu-id="0b324-163">`Name <String>`: The name of the column to use in comparison.</span></span>
    - <span data-ttu-id="0b324-164">`Operator <OperatorType>`: Den operator som ska användas för jämförelse.</span><span class="sxs-lookup"><span data-stu-id="0b324-164">`Operator <OperatorType>`: The operator to use for comparison.</span></span>
    - <span data-ttu-id="0b324-165">`Value <String[]>`: Matris med värden som ska användas för jämförelse</span><span class="sxs-lookup"><span data-stu-id="0b324-165">`Value <String[]>`: Array of values to use for comparison</span></span>
  - <span data-ttu-id="0b324-166">`[Not <IQueryFilter>]`: Det logiska uttrycket "inte".</span><span class="sxs-lookup"><span data-stu-id="0b324-166">`[Not <IQueryFilter>]`: The logical "NOT" expression.</span></span>
  - <span data-ttu-id="0b324-167">`[Or <IQueryFilter[]>]`: Det logiska uttrycket "eller".</span><span class="sxs-lookup"><span data-stu-id="0b324-167">`[Or <IQueryFilter[]>]`: The logical "OR" expression.</span></span> <span data-ttu-id="0b324-168">Måste innehålla minst två objekt.</span><span class="sxs-lookup"><span data-stu-id="0b324-168">Must have at least 2 items.</span></span>
  - <span data-ttu-id="0b324-169">`[Tag <IQueryComparisonExpression>]`: Jämförelse uttryck för en tagg</span><span class="sxs-lookup"><span data-stu-id="0b324-169">`[Tag <IQueryComparisonExpression>]`: Has comparison expression for a tag</span></span>

<span data-ttu-id="0b324-170">DATASETGROUPING <IQueryGrouping [] >: matris med Group by-uttryck som du vill använda i frågan.</span><span class="sxs-lookup"><span data-stu-id="0b324-170">DATASETGROUPING <IQueryGrouping[]>: Array of group by expression to use in the query.</span></span>
  - <span data-ttu-id="0b324-171">`Name <String>`: Namnet på den kolumn som ska grupperas.</span><span class="sxs-lookup"><span data-stu-id="0b324-171">`Name <String>`: The name of the column to group.</span></span>
  - <span data-ttu-id="0b324-172">`Type <QueryColumnType>`: Anger vilken kolumn som ska grupperas.</span><span class="sxs-lookup"><span data-stu-id="0b324-172">`Type <QueryColumnType>`: Has type of the column to group.</span></span>

## <span data-ttu-id="0b324-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0b324-173">RELATED LINKS</span></span>

