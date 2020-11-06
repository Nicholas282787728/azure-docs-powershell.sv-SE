---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: 44273f05793e8f84b28e6dc68f8cc12633fadf0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575662"
---
# <span data-ttu-id="9a71d-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9a71d-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="9a71d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9a71d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a71d-103">Skapar en Autoskala-profil.</span><span class="sxs-lookup"><span data-stu-id="9a71d-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a71d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9a71d-104">SYNTAX</span></span>

### <span data-ttu-id="9a71d-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="9a71d-105">CreateWithoutScheduledTimes</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String> -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a71d-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="9a71d-106">CreateWithFixedDateScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a71d-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="9a71d-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a71d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9a71d-108">DESCRIPTION</span></span>
<span data-ttu-id="9a71d-109">Cmdleten **New-AzureRmAutoscaleProfile** skapar en Autoskala-profil.</span><span class="sxs-lookup"><span data-stu-id="9a71d-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="9a71d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9a71d-110">EXAMPLES</span></span>

### <span data-ttu-id="9a71d-111">Exempel 1: skapa en profil med ett fast datum</span><span class="sxs-lookup"><span data-stu-id="9a71d-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="9a71d-112">Det första kommandot skapar en autoskale-regel med namnet förfrågningar och lagrar den sedan i $Rule variabel.</span><span class="sxs-lookup"><span data-stu-id="9a71d-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="9a71d-113">Det andra kommandot skapar en profil med namnet Profile01 med ett fast datum med regeln i $Rule.</span><span class="sxs-lookup"><span data-stu-id="9a71d-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="9a71d-114">Exempel 2: skapa en profil med ett schema</span><span class="sxs-lookup"><span data-stu-id="9a71d-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="9a71d-115">Det första kommandot skapar en autoskale-regel med namnet förfrågningar och lagrar den sedan i $Rule variabel.</span><span class="sxs-lookup"><span data-stu-id="9a71d-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="9a71d-116">Det andra kommandot skapar en profil med namnet SecondProfileName med ett återkommande schema med hjälp av regeln i $Rule.</span><span class="sxs-lookup"><span data-stu-id="9a71d-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="9a71d-117">Exempel 3: skapa profiler med två regler</span><span class="sxs-lookup"><span data-stu-id="9a71d-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="9a71d-118">De två första kommandona skapar regler och lagrar dem i variabelrna $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="9a71d-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="9a71d-119">Det tredje kommandot skapar en profil med namnet profilnamn med reglerna i Rule1 och Rule2 och lagrar dem sedan i variabeln $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="9a71d-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="9a71d-120">Med kommandot slut skapas en profil med namnet SecondProfileName med reglerna i Rule1 och Rule2 och sparas sedan i variabeln $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="9a71d-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="9a71d-121">Exempel 4: skapa en profil utan schema eller fast datum</span><span class="sxs-lookup"><span data-stu-id="9a71d-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="9a71d-122">Det första kommandot skapar en autoskale-regel med namnet förfrågningar och lagrar den sedan i $Rule variabel.</span><span class="sxs-lookup"><span data-stu-id="9a71d-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="9a71d-123">Det andra kommandot skapar en profil utan ett schema eller ett fast datum och lagrar den sedan i $Profile variabel.</span><span class="sxs-lookup"><span data-stu-id="9a71d-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="9a71d-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9a71d-124">PARAMETERS</span></span>

### <span data-ttu-id="9a71d-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="9a71d-125">-DefaultCapacity</span></span>
<span data-ttu-id="9a71d-126">Anger standard kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="9a71d-126">Specifies the default capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a71d-127">-DefaultProfile</span></span>
<span data-ttu-id="9a71d-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9a71d-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="9a71d-129">-EndTimeWindow</span></span>
<span data-ttu-id="9a71d-130">Anger slutet av tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="9a71d-130">Specifies the end of the time window.</span></span>

```yaml
Type: DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="9a71d-131">-MaximumCapacity</span></span>
<span data-ttu-id="9a71d-132">Anger maximal kapacitet.</span><span class="sxs-lookup"><span data-stu-id="9a71d-132">Specifies the maximum capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="9a71d-133">-MinimumCapacity</span></span>
<span data-ttu-id="9a71d-134">Anger den minsta kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="9a71d-134">Specifies the minimum capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="9a71d-135">-Name</span></span>
<span data-ttu-id="9a71d-136">Anger namnet på den profil som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="9a71d-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="9a71d-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="9a71d-138">Anger frekvensen för återkommande.</span><span class="sxs-lookup"><span data-stu-id="9a71d-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="9a71d-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9a71d-139">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9a71d-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="9a71d-140">None</span></span>
- <span data-ttu-id="9a71d-141">Igen</span><span class="sxs-lookup"><span data-stu-id="9a71d-141">Second</span></span>
- <span data-ttu-id="9a71d-142">Minut</span><span class="sxs-lookup"><span data-stu-id="9a71d-142">Minute</span></span>
- <span data-ttu-id="9a71d-143">Timme</span><span class="sxs-lookup"><span data-stu-id="9a71d-143">Hour</span></span>
- <span data-ttu-id="9a71d-144">Day</span><span class="sxs-lookup"><span data-stu-id="9a71d-144">Day</span></span>
- <span data-ttu-id="9a71d-145">Fjorton</span><span class="sxs-lookup"><span data-stu-id="9a71d-145">Week</span></span>
- <span data-ttu-id="9a71d-146">Månad</span><span class="sxs-lookup"><span data-stu-id="9a71d-146">Month</span></span>
- <span data-ttu-id="9a71d-147">Vinåret</span><span class="sxs-lookup"><span data-stu-id="9a71d-147">Year</span></span>

<span data-ttu-id="9a71d-148">Alla dessa värden stöds inte.</span><span class="sxs-lookup"><span data-stu-id="9a71d-148">Not all of these values are supported.</span></span>

```yaml
Type: RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-149">-Regel</span><span class="sxs-lookup"><span data-stu-id="9a71d-149">-Rule</span></span>
<span data-ttu-id="9a71d-150">Anger listan över regler som ska läggas till i profilen.</span><span class="sxs-lookup"><span data-stu-id="9a71d-150">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases: Rules

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-151">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="9a71d-151">-ScheduleDay</span></span>
<span data-ttu-id="9a71d-152">Anger de schemalagda dagarna.</span><span class="sxs-lookup"><span data-stu-id="9a71d-152">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleDays

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-153">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="9a71d-153">-ScheduleHour</span></span>
<span data-ttu-id="9a71d-154">Anger de schemalagda timmarna.</span><span class="sxs-lookup"><span data-stu-id="9a71d-154">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleHours

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-155">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="9a71d-155">-ScheduleMinute</span></span>
<span data-ttu-id="9a71d-156">Anger det schemalagda antalet minuter.</span><span class="sxs-lookup"><span data-stu-id="9a71d-156">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: ScheduleMinutes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-157">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="9a71d-157">-ScheduleTimeZone</span></span>
<span data-ttu-id="9a71d-158">Anger tids zonen för schemat.</span><span class="sxs-lookup"><span data-stu-id="9a71d-158">Specifies the time zone of the schedule.</span></span>

```yaml
Type: String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-159">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="9a71d-159">-StartTimeWindow</span></span>
<span data-ttu-id="9a71d-160">Anger tidsfönstrets början.</span><span class="sxs-lookup"><span data-stu-id="9a71d-160">Specifies the start of the time window.</span></span>

```yaml
Type: DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-161">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="9a71d-161">-TimeWindowTimeZone</span></span>
<span data-ttu-id="9a71d-162">Anger tids zonen för tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="9a71d-162">Specifies the time zone of the time window.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithFixedDateScheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a71d-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a71d-163">CommonParameters</span></span>
<span data-ttu-id="9a71d-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a71d-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a71d-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a71d-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a71d-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9a71d-166">INPUTS</span></span>

### <span data-ttu-id="9a71d-167">Ingen</span><span class="sxs-lookup"><span data-stu-id="9a71d-167">None</span></span>
<span data-ttu-id="9a71d-168">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9a71d-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a71d-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9a71d-169">OUTPUTS</span></span>

### <span data-ttu-id="9a71d-170">Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="9a71d-170">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="9a71d-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9a71d-171">NOTES</span></span>

## <span data-ttu-id="9a71d-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9a71d-172">RELATED LINKS</span></span>

[<span data-ttu-id="9a71d-173">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9a71d-173">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9a71d-174">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="9a71d-174">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="9a71d-175">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9a71d-175">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="9a71d-176">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="9a71d-176">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="9a71d-177">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="9a71d-177">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


