---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 45e41da30d90041c1e8670ebe8e356688785e355
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754669"
---
# <span data-ttu-id="757f5-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="757f5-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="757f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="757f5-102">SYNOPSIS</span></span>
<span data-ttu-id="757f5-103">Skapa en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="757f5-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="757f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="757f5-104">SYNTAX</span></span>

### <span data-ttu-id="757f5-105">Abonnemang (standard)</span><span class="sxs-lookup"><span data-stu-id="757f5-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="757f5-106">Underrättelsefråga</span><span class="sxs-lookup"><span data-stu-id="757f5-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="757f5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="757f5-107">DESCRIPTION</span></span>
<span data-ttu-id="757f5-108">New-AzConsumptionBudget-cmdleten skapar en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="757f5-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="757f5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="757f5-109">EXAMPLES</span></span>

### <span data-ttu-id="757f5-110">Exempel 1: skapa en kostnads budget med ett budget namn på en abonnemangs nivå</span><span class="sxs-lookup"><span data-stu-id="757f5-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="757f5-111">Exempel 2: skapa en kostnads budget med ett budget namn på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="757f5-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="757f5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="757f5-112">PARAMETERS</span></span>

### <span data-ttu-id="757f5-113">-Belopp</span><span class="sxs-lookup"><span data-stu-id="757f5-113">-Amount</span></span>
<span data-ttu-id="757f5-114">Beloppet för en budget.</span><span class="sxs-lookup"><span data-stu-id="757f5-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-115">-Kategori</span><span class="sxs-lookup"><span data-stu-id="757f5-115">-Category</span></span>
<span data-ttu-id="757f5-116">Budgetens kategori kan vara kostnad eller förbrukning.</span><span class="sxs-lookup"><span data-stu-id="757f5-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="757f5-117">-ContactEmail</span></span>
<span data-ttu-id="757f5-118">E-postadresser för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="757f5-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="757f5-119">-ContactGroup</span></span>
<span data-ttu-id="757f5-120">Åtgärds grupper för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="757f5-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="757f5-121">-ContactRole</span></span>
<span data-ttu-id="757f5-122">Kontakt roller för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="757f5-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="757f5-123">-DefaultProfile</span></span>
<span data-ttu-id="757f5-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="757f5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="757f5-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="757f5-125">-EndDate</span></span>
<span data-ttu-id="757f5-126">Slutdatum (ÅÅÅÅ-MM-DD i UTC) av en budget.</span><span class="sxs-lookup"><span data-stu-id="757f5-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="757f5-127">-MeterFilter</span></span>
<span data-ttu-id="757f5-128">Kommaavgränsad lista med mätare att filtrera på.</span><span class="sxs-lookup"><span data-stu-id="757f5-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="757f5-129">Obligatoriskt om kategorin används.</span><span class="sxs-lookup"><span data-stu-id="757f5-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="757f5-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="757f5-130">-Name</span></span>
<span data-ttu-id="757f5-131">Namn på en budget.</span><span class="sxs-lookup"><span data-stu-id="757f5-131">Name of a budget.</span></span>

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

### <span data-ttu-id="757f5-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="757f5-132">-NotificationEnabled</span></span>
<span data-ttu-id="757f5-133">Meddelandet är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="757f5-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="757f5-134">-NotificationKey</span></span>
<span data-ttu-id="757f5-135">Tangent för ett meddelande som är kopplat till en budget, krävs för att skapa ett meddelande med växeln aktivera avisering, tröskelvärde för meddelanden, kontakt grupper eller kontakt roller.</span><span class="sxs-lookup"><span data-stu-id="757f5-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="757f5-136">-NotificationThreshold</span></span>
<span data-ttu-id="757f5-137">Tröskel värde kopplat till ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="757f5-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="757f5-138">Meddelande skickas när kostnaden eller användningen överskrider tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="757f5-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="757f5-139">Det är alltid procent och måste vara mellan 0 och 1000.</span><span class="sxs-lookup"><span data-stu-id="757f5-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="757f5-140">-ResourceFilter</span></span>
<span data-ttu-id="757f5-141">Kommaavgränsad lista över resurs instanser att filtrera efter.</span><span class="sxs-lookup"><span data-stu-id="757f5-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="757f5-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="757f5-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="757f5-143">Kommaavgränsad lista över resurs grupper att filtrera efter.</span><span class="sxs-lookup"><span data-stu-id="757f5-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="757f5-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="757f5-144">-ResourceGroupName</span></span>
<span data-ttu-id="757f5-145">Resurs grupp för en budget.</span><span class="sxs-lookup"><span data-stu-id="757f5-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="757f5-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="757f5-146">-StartDate</span></span>
<span data-ttu-id="757f5-147">Start datum (ÅÅÅÅ-MM-DD i UTC) av en budget.</span><span class="sxs-lookup"><span data-stu-id="757f5-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="757f5-148">Inte före aktuell månad för månads tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="757f5-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="757f5-149">Inte före tre månader för kvartals tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="757f5-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="757f5-150">Inte före 12 månader för års tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="757f5-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="757f5-151">Framtida start datum inte mer än tre månader.</span><span class="sxs-lookup"><span data-stu-id="757f5-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="757f5-152">-TimeGrain</span></span>
<span data-ttu-id="757f5-153">Tids kornig het för budgeten kan vara månatlig, kvartals vis eller årligen.</span><span class="sxs-lookup"><span data-stu-id="757f5-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="757f5-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="757f5-154">-Confirm</span></span>
<span data-ttu-id="757f5-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="757f5-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="757f5-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="757f5-156">-WhatIf</span></span>
<span data-ttu-id="757f5-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="757f5-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="757f5-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="757f5-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="757f5-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="757f5-159">CommonParameters</span></span>
<span data-ttu-id="757f5-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="757f5-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="757f5-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="757f5-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="757f5-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="757f5-162">INPUTS</span></span>

### <span data-ttu-id="757f5-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="757f5-163">None</span></span>

## <span data-ttu-id="757f5-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="757f5-164">OUTPUTS</span></span>

### <span data-ttu-id="757f5-165">Microsoft. Azure. commands. förbrukning. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="757f5-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="757f5-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="757f5-166">NOTES</span></span>

## <span data-ttu-id="757f5-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="757f5-167">RELATED LINKS</span></span>
