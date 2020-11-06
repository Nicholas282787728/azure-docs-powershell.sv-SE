---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/new-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/New-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/New-AzureRmConsumptionBudget.md
ms.openlocfilehash: 9c89a4791b4e32637d069a672ddde06862518332
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582752"
---
# <span data-ttu-id="d34e3-101">New-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="d34e3-101">New-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="d34e3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d34e3-102">SYNOPSIS</span></span>
<span data-ttu-id="d34e3-103">Skapa en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d34e3-103">Create a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d34e3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d34e3-104">SYNTAX</span></span>

### <span data-ttu-id="d34e3-105">Abonnemang (standard)</span><span class="sxs-lookup"><span data-stu-id="d34e3-105">Subscription (Default)</span></span>
```
New-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d34e3-106">Underrättelsefråga</span><span class="sxs-lookup"><span data-stu-id="d34e3-106">Notification</span></span>
```
New-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d34e3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d34e3-107">DESCRIPTION</span></span>
<span data-ttu-id="d34e3-108">New-AzureRmConsumptionBudget-cmdleten skapar en budget i antingen en prenumeration eller en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d34e3-108">The New-AzureRmConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="d34e3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d34e3-109">EXAMPLES</span></span>

### <span data-ttu-id="d34e3-110">Exempel 1: skapa en kostnads budget med ett budget namn på en abonnemangs nivå</span><span class="sxs-lookup"><span data-stu-id="d34e3-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzureRmConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

### <span data-ttu-id="d34e3-111">Exempel 2: skapa en kostnads budget med ett budget namn på resurs grupp nivå</span><span class="sxs-lookup"><span data-stu-id="d34e3-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
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

## <span data-ttu-id="d34e3-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d34e3-112">PARAMETERS</span></span>

### <span data-ttu-id="d34e3-113">-Belopp</span><span class="sxs-lookup"><span data-stu-id="d34e3-113">-Amount</span></span>
<span data-ttu-id="d34e3-114">Beloppet för en budget.</span><span class="sxs-lookup"><span data-stu-id="d34e3-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="d34e3-115">-Kategori</span><span class="sxs-lookup"><span data-stu-id="d34e3-115">-Category</span></span>
<span data-ttu-id="d34e3-116">Budgetens kategori kan vara kostnad eller förbrukning.</span><span class="sxs-lookup"><span data-stu-id="d34e3-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="d34e3-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="d34e3-117">-ContactEmail</span></span>
<span data-ttu-id="d34e3-118">E-postadresser för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="d34e3-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="d34e3-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="d34e3-119">-ContactGroup</span></span>
<span data-ttu-id="d34e3-120">Åtgärds grupper för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="d34e3-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="d34e3-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="d34e3-121">-ContactRole</span></span>
<span data-ttu-id="d34e3-122">Kontakt roller för att skicka budget meddelandet till när tröskelvärdet har överskridits.</span><span class="sxs-lookup"><span data-stu-id="d34e3-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="d34e3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34e3-123">-DefaultProfile</span></span>
<span data-ttu-id="d34e3-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d34e3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34e3-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d34e3-125">-EndDate</span></span>
<span data-ttu-id="d34e3-126">Slutdatum (ÅÅÅÅ-MM-DD i UTC) av en budget.</span><span class="sxs-lookup"><span data-stu-id="d34e3-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="d34e3-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="d34e3-127">-MeterFilter</span></span>
<span data-ttu-id="d34e3-128">Kommaavgränsad lista med mätare att filtrera på.</span><span class="sxs-lookup"><span data-stu-id="d34e3-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="d34e3-129">Obligatoriskt om kategorin används.</span><span class="sxs-lookup"><span data-stu-id="d34e3-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="d34e3-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="d34e3-130">-Name</span></span>
<span data-ttu-id="d34e3-131">Namn på en budget.</span><span class="sxs-lookup"><span data-stu-id="d34e3-131">Name of a budget.</span></span>

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

### <span data-ttu-id="d34e3-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="d34e3-132">-NotificationEnabled</span></span>
<span data-ttu-id="d34e3-133">Meddelandet är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="d34e3-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="d34e3-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="d34e3-134">-NotificationKey</span></span>
<span data-ttu-id="d34e3-135">Tangent för ett meddelande som är kopplat till en budget, krävs för att skapa ett meddelande med växeln aktivera avisering, tröskelvärde för meddelanden, kontakt grupper eller kontakt roller.</span><span class="sxs-lookup"><span data-stu-id="d34e3-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="d34e3-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="d34e3-136">-NotificationThreshold</span></span>
<span data-ttu-id="d34e3-137">Tröskel värde kopplat till ett meddelande.</span><span class="sxs-lookup"><span data-stu-id="d34e3-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="d34e3-138">Meddelande skickas när kostnaden eller användningen överskrider tröskelvärdet.</span><span class="sxs-lookup"><span data-stu-id="d34e3-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="d34e3-139">Det är alltid procent och måste vara mellan 0 och 1000.</span><span class="sxs-lookup"><span data-stu-id="d34e3-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="d34e3-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="d34e3-140">-ResourceFilter</span></span>
<span data-ttu-id="d34e3-141">Kommaavgränsad lista över resurs instanser att filtrera efter.</span><span class="sxs-lookup"><span data-stu-id="d34e3-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="d34e3-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="d34e3-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="d34e3-143">Kommaavgränsad lista över resurs grupper att filtrera efter.</span><span class="sxs-lookup"><span data-stu-id="d34e3-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="d34e3-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34e3-144">-ResourceGroupName</span></span>
<span data-ttu-id="d34e3-145">Resurs grupp för en budget.</span><span class="sxs-lookup"><span data-stu-id="d34e3-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="d34e3-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d34e3-146">-StartDate</span></span>
<span data-ttu-id="d34e3-147">Start datum (ÅÅÅÅ-MM-DD i UTC) av en budget.</span><span class="sxs-lookup"><span data-stu-id="d34e3-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="d34e3-148">Inte före aktuell månad för månads tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="d34e3-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="d34e3-149">Inte före tre månader för kvartals tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="d34e3-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="d34e3-150">Inte före 12 månader för års tids kornig het.</span><span class="sxs-lookup"><span data-stu-id="d34e3-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="d34e3-151">Framtida start datum inte mer än tre månader.</span><span class="sxs-lookup"><span data-stu-id="d34e3-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="d34e3-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="d34e3-152">-TimeGrain</span></span>
<span data-ttu-id="d34e3-153">Tids kornig het för budgeten kan vara månatlig, kvartals vis eller årligen.</span><span class="sxs-lookup"><span data-stu-id="d34e3-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="d34e3-154">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d34e3-154">-Confirm</span></span>
<span data-ttu-id="d34e3-155">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d34e3-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d34e3-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d34e3-156">-WhatIf</span></span>
<span data-ttu-id="d34e3-157">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d34e3-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d34e3-158">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d34e3-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d34e3-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34e3-159">CommonParameters</span></span>
<span data-ttu-id="d34e3-160">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34e3-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34e3-161">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d34e3-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34e3-162">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d34e3-162">INPUTS</span></span>

### <span data-ttu-id="d34e3-163">Ingen</span><span class="sxs-lookup"><span data-stu-id="d34e3-163">None</span></span>

## <span data-ttu-id="d34e3-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d34e3-164">OUTPUTS</span></span>

### <span data-ttu-id="d34e3-165">Microsoft. Azure. commands. förbrukning. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="d34e3-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="d34e3-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d34e3-166">NOTES</span></span>

## <span data-ttu-id="d34e3-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d34e3-167">RELATED LINKS</span></span>
