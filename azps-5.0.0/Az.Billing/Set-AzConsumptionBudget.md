---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: 89d628790297bfb677dab11f0b19ba525d8b9e47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272792"
---
# <span data-ttu-id="7c47c-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="7c47c-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="7c47c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7c47c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c47c-103">Uppdatera en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7c47c-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="7c47c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7c47c-104">SYNTAX</span></span>

### <span data-ttu-id="7c47c-105">Abonnemang (standard)</span><span class="sxs-lookup"><span data-stu-id="7c47c-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c47c-106">Underrättelsefråga</span><span class="sxs-lookup"><span data-stu-id="7c47c-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c47c-107">Fäst</span><span class="sxs-lookup"><span data-stu-id="7c47c-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c47c-108">Rör dragning och anmälan</span><span class="sxs-lookup"><span data-stu-id="7c47c-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c47c-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7c47c-109">DESCRIPTION</span></span>
<span data-ttu-id="7c47c-110">Set-AzConsumptionBudget cmdlet uppdaterar en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="7c47c-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="7c47c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7c47c-111">EXAMPLES</span></span>

### <span data-ttu-id="7c47c-112">Exempel 1: uppdatera en budget med ett nytt belopp med ett budget namn på abonnemangs nivå</span><span class="sxs-lookup"><span data-stu-id="7c47c-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="7c47c-113">Exempel 2: uppdatera en budget med ett meddelande när kostnad eller användning når en tröskel på 90 procent av beloppet på prenumerations nivå</span><span class="sxs-lookup"><span data-stu-id="7c47c-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="7c47c-114">Exempel 3: uppdatera en budget med ett nytt belopp med ett budget namn på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="7c47c-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="7c47c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7c47c-115">PARAMETERS</span></span>

### <span data-ttu-id="7c47c-116">-Belopp</span><span class="sxs-lookup"><span data-stu-id="7c47c-116">-Amount</span></span>
<span data-ttu-id="7c47c-117">Beloppet för en budget.</span><span class="sxs-lookup"><span data-stu-id="7c47c-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-118">-Kategori</span><span class="sxs-lookup"><span data-stu-id="7c47c-118">-Category</span></span>
<span data-ttu-id="7c47c-119">Budgetens kategori kan vara kostnad eller förbrukning.</span><span class="sxs-lookup"><span data-stu-id="7c47c-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="7c47c-120">-ContactEmail</span></span>
<span data-ttu-id="7c47c-121">E-postadresser för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="7c47c-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="7c47c-122">-ContactGroup</span></span>
<span data-ttu-id="7c47c-123">Åtgärds grupper för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="7c47c-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="7c47c-124">-ContactRole</span></span>
<span data-ttu-id="7c47c-125">Kontakt roller för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="7c47c-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c47c-126">-DefaultProfile</span></span>
<span data-ttu-id="7c47c-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7c47c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c47c-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="7c47c-128">-EndDate</span></span>
<span data-ttu-id="7c47c-129">Slutdatum (ÅÅÅÅ-MM-DD i UTC) av en budget.</span><span class="sxs-lookup"><span data-stu-id="7c47c-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="7c47c-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c47c-130">-InputObject</span></span>
<span data-ttu-id="7c47c-131">Budget objekt.</span><span class="sxs-lookup"><span data-stu-id="7c47c-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="7c47c-132">-MeterFilter</span></span>
<span data-ttu-id="7c47c-133">Kommaavgränsad lista med mätare att filtrera på.</span><span class="sxs-lookup"><span data-stu-id="7c47c-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="7c47c-134">Obligatoriskt om kategorin används.</span><span class="sxs-lookup"><span data-stu-id="7c47c-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="7c47c-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="7c47c-135">-Name</span></span>
<span data-ttu-id="7c47c-136">Namn på en budget.</span><span class="sxs-lookup"><span data-stu-id="7c47c-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="7c47c-137">-NotificationEnabled</span></span>
<span data-ttu-id="7c47c-138">Meddelandet är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="7c47c-138">The notification is enabled.</span></span>
<span data-ttu-id="7c47c-139">Om inget anges är aviseringen inaktive rad som standard.</span><span class="sxs-lookup"><span data-stu-id="7c47c-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="7c47c-140">-NotificationKey</span></span>
<span data-ttu-id="7c47c-141">Tangent för ett meddelande som är kopplat till en budget, krävs för att skapa ett meddelande med växeln aktivera avisering, tröskelvärde för meddelanden, kontakt grupper eller kontakt roller.</span><span class="sxs-lookup"><span data-stu-id="7c47c-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="7c47c-142">-NotificationThreshold</span></span>
<span data-ttu-id="7c47c-143">Tröskel värde kopplat till ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="7c47c-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="7c47c-144">Meddelande skickas när kostnaden eller användningen överskrider tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="7c47c-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="7c47c-145">Det är alltid procent och måste vara mellan 0 och 1000.</span><span class="sxs-lookup"><span data-stu-id="7c47c-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="7c47c-146">-ResourceFilter</span></span>
<span data-ttu-id="7c47c-147">Kommaavgränsad lista över resurs instanser att filtrera efter.</span><span class="sxs-lookup"><span data-stu-id="7c47c-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="7c47c-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="7c47c-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="7c47c-149">Kommaavgränsad lista över resurs grupper att filtrera efter.</span><span class="sxs-lookup"><span data-stu-id="7c47c-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="7c47c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c47c-150">-ResourceGroupName</span></span>
<span data-ttu-id="7c47c-151">Resurs grupp för en budget.</span><span class="sxs-lookup"><span data-stu-id="7c47c-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="7c47c-152">-StartDate</span></span>
<span data-ttu-id="7c47c-153">Start datum (ÅÅÅÅ-MM-DD i UTC) av en budget.</span><span class="sxs-lookup"><span data-stu-id="7c47c-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="7c47c-154">Inte före aktuell månad för månads tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="7c47c-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="7c47c-155">Inte före tre månader för kvartals tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="7c47c-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="7c47c-156">Inte före 12 månader för års tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="7c47c-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="7c47c-157">Framtida start datum inte mer än tre månader.</span><span class="sxs-lookup"><span data-stu-id="7c47c-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="7c47c-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="7c47c-158">-TimeGrain</span></span>
<span data-ttu-id="7c47c-159">Tids kornig het för budgeten kan vara månatlig, kvartals vis eller årligen.</span><span class="sxs-lookup"><span data-stu-id="7c47c-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c47c-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7c47c-160">-Confirm</span></span>
<span data-ttu-id="7c47c-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7c47c-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c47c-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c47c-162">-WhatIf</span></span>
<span data-ttu-id="7c47c-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7c47c-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c47c-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7c47c-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c47c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c47c-165">CommonParameters</span></span>
<span data-ttu-id="7c47c-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c47c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c47c-167">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c47c-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c47c-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7c47c-168">INPUTS</span></span>

### <span data-ttu-id="7c47c-169">Microsoft. Azure. commands. förbrukning. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="7c47c-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="7c47c-170">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7c47c-170">OUTPUTS</span></span>

### <span data-ttu-id="7c47c-171">Microsoft. Azure. commands. förbrukning. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="7c47c-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="7c47c-172">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7c47c-172">NOTES</span></span>

## <span data-ttu-id="7c47c-173">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7c47c-173">RELATED LINKS</span></span>
