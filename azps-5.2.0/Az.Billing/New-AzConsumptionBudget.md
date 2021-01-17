---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400976"
---
# <span data-ttu-id="c8a0f-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="c8a0f-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="c8a0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8a0f-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a0f-103">Skapa en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="c8a0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8a0f-104">SYNTAX</span></span>

### <span data-ttu-id="c8a0f-105">Abonnemang (standard)</span><span class="sxs-lookup"><span data-stu-id="c8a0f-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a0f-106">Underrättelsefråga</span><span class="sxs-lookup"><span data-stu-id="c8a0f-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8a0f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8a0f-107">DESCRIPTION</span></span>
<span data-ttu-id="c8a0f-108">New-AzConsumptionBudget-cmdleten skapar en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="c8a0f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8a0f-109">EXAMPLES</span></span>

### <span data-ttu-id="c8a0f-110">Exempel 1: skapa en kostnads budget med ett budget namn på en abonnemangs nivå</span><span class="sxs-lookup"><span data-stu-id="c8a0f-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
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

### <span data-ttu-id="c8a0f-111">Exempel 2: skapa en kostnads budget med ett budget namn på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="c8a0f-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
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

## <span data-ttu-id="c8a0f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8a0f-112">PARAMETERS</span></span>

### <span data-ttu-id="c8a0f-113">-Belopp</span><span class="sxs-lookup"><span data-stu-id="c8a0f-113">-Amount</span></span>
<span data-ttu-id="c8a0f-114">Beloppet för en budget.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="c8a0f-115">-Kategori</span><span class="sxs-lookup"><span data-stu-id="c8a0f-115">-Category</span></span>
<span data-ttu-id="c8a0f-116">Budgetens kategori kan vara kostnad eller förbrukning.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="c8a0f-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="c8a0f-117">-ContactEmail</span></span>
<span data-ttu-id="c8a0f-118">E-postadresser för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="c8a0f-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="c8a0f-119">-ContactGroup</span></span>
<span data-ttu-id="c8a0f-120">Åtgärds grupper för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="c8a0f-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="c8a0f-121">-ContactRole</span></span>
<span data-ttu-id="c8a0f-122">Kontakt roller för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="c8a0f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a0f-123">-DefaultProfile</span></span>
<span data-ttu-id="c8a0f-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a0f-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c8a0f-125">-EndDate</span></span>
<span data-ttu-id="c8a0f-126">Slutdatum (ÅÅÅÅ-MM-DD i UTC) av en budget.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="c8a0f-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="c8a0f-127">-MeterFilter</span></span>
<span data-ttu-id="c8a0f-128">Kommaavgränsad lista med mätare att filtrera på.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="c8a0f-129">Obligatoriskt om kategorin används.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="c8a0f-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8a0f-130">-Name</span></span>
<span data-ttu-id="c8a0f-131">Namn på en budget.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-131">Name of a budget.</span></span>

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

### <span data-ttu-id="c8a0f-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="c8a0f-132">-NotificationEnabled</span></span>
<span data-ttu-id="c8a0f-133">Meddelandet är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="c8a0f-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="c8a0f-134">-NotificationKey</span></span>
<span data-ttu-id="c8a0f-135">Tangent för ett meddelande som är kopplat till en budget, krävs för att skapa ett meddelande med växeln aktivera avisering, tröskelvärde för meddelanden, kontakt grupper eller kontakt roller.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="c8a0f-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="c8a0f-136">-NotificationThreshold</span></span>
<span data-ttu-id="c8a0f-137">Tröskel värde kopplat till ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="c8a0f-138">Meddelande skickas när kostnaden eller användningen överskrider tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="c8a0f-139">Det är alltid procent och måste vara mellan 0 och 1000.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="c8a0f-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="c8a0f-140">-ResourceFilter</span></span>
<span data-ttu-id="c8a0f-141">Kommaavgränsad lista över resurs instanser att filtrera efter.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="c8a0f-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="c8a0f-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="c8a0f-143">Kommaavgränsad lista över resurs grupper att filtrera efter.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="c8a0f-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a0f-144">-ResourceGroupName</span></span>
<span data-ttu-id="c8a0f-145">Resurs grupp för en budget.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="c8a0f-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c8a0f-146">-StartDate</span></span>
<span data-ttu-id="c8a0f-147">Start datum (ÅÅÅÅ-MM-DD i UTC) av en budget.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="c8a0f-148">Inte före aktuell månad för månads tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="c8a0f-149">Inte före tre månader för kvartals tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="c8a0f-150">Inte före 12 månader för års tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="c8a0f-151">Framtida start datum inte mer än tre månader.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="c8a0f-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="c8a0f-152">-TimeGrain</span></span>
<span data-ttu-id="c8a0f-153">Tids kornig het för budgeten kan vara månatlig, kvartals vis eller årligen.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="c8a0f-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c8a0f-154">-Confirm</span></span>
<span data-ttu-id="c8a0f-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8a0f-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a0f-156">-WhatIf</span></span>
<span data-ttu-id="c8a0f-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8a0f-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8a0f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a0f-159">CommonParameters</span></span>
<span data-ttu-id="c8a0f-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a0f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a0f-161">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8a0f-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a0f-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8a0f-162">INPUTS</span></span>

### <span data-ttu-id="c8a0f-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="c8a0f-163">None</span></span>

## <span data-ttu-id="c8a0f-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8a0f-164">OUTPUTS</span></span>

### <span data-ttu-id="c8a0f-165">Microsoft. Azure. commands. förbrukning. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="c8a0f-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="c8a0f-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8a0f-166">NOTES</span></span>

## <span data-ttu-id="c8a0f-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8a0f-167">RELATED LINKS</span></span>
