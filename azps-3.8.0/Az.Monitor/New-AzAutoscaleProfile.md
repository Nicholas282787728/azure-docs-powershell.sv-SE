---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: f857f578ab3f0b8baacd0c5d392659ac09b0790f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93925706"
---
# <span data-ttu-id="80584-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="80584-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="80584-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="80584-102">SYNOPSIS</span></span>
<span data-ttu-id="80584-103">Skapar en Autoskala-profil.</span><span class="sxs-lookup"><span data-stu-id="80584-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="80584-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="80584-104">SYNTAX</span></span>

### <span data-ttu-id="80584-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="80584-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80584-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="80584-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="80584-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="80584-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80584-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="80584-108">DESCRIPTION</span></span>
<span data-ttu-id="80584-109">Cmdleten **New-AzAutoscaleProfile** skapar en Autoskala-profil.</span><span class="sxs-lookup"><span data-stu-id="80584-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="80584-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="80584-110">EXAMPLES</span></span>

### <span data-ttu-id="80584-111">Exempel 1: skapa en profil med ett fast datum</span><span class="sxs-lookup"><span data-stu-id="80584-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="80584-112">Det första kommandot skapar en autoskale-regel med namnet förfrågningar och lagrar den sedan i $Rule variabel.</span><span class="sxs-lookup"><span data-stu-id="80584-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="80584-113">Det andra kommandot skapar en profil med namnet Profile01 med ett fast datum med regeln i $Rule.</span><span class="sxs-lookup"><span data-stu-id="80584-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="80584-114">Exempel 2: skapa en profil med ett schema</span><span class="sxs-lookup"><span data-stu-id="80584-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="80584-115">Det första kommandot skapar en autoskale-regel med namnet förfrågningar och lagrar den sedan i $Rule variabel.</span><span class="sxs-lookup"><span data-stu-id="80584-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="80584-116">Det andra kommandot skapar en profil med namnet SecondProfileName med ett återkommande schema med hjälp av regeln i $Rule.</span><span class="sxs-lookup"><span data-stu-id="80584-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="80584-117">Exempel 3: skapa profiler med två regler</span><span class="sxs-lookup"><span data-stu-id="80584-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDay "1" -ScheduleHour 5 -ScheduleMinute 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="80584-118">De två första kommandona skapar regler och lagrar dem i variabelrna $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="80584-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="80584-119">Det tredje kommandot skapar en profil med namnet profilnamn med reglerna i Rule1 och Rule2 och lagrar dem sedan i variabeln $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="80584-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="80584-120">Med kommandot slut skapas en profil med namnet SecondProfileName med reglerna i Rule1 och Rule2 och sparas sedan i variabeln $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="80584-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="80584-121">Exempel 4: skapa en profil utan schema eller fast datum</span><span class="sxs-lookup"><span data-stu-id="80584-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="80584-122">Det första kommandot skapar en autoskale-regel med namnet förfrågningar och lagrar den sedan i $Rule variabel.</span><span class="sxs-lookup"><span data-stu-id="80584-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="80584-123">Det andra kommandot skapar en profil utan ett schema eller ett fast datum och lagrar den sedan i $Profile variabel.</span><span class="sxs-lookup"><span data-stu-id="80584-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="80584-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="80584-124">PARAMETERS</span></span>

### <span data-ttu-id="80584-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="80584-125">-DefaultCapacity</span></span>
<span data-ttu-id="80584-126">Anger standard kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="80584-126">Specifies the default capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80584-127">-DefaultProfile</span></span>
<span data-ttu-id="80584-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="80584-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80584-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="80584-129">-EndTimeWindow</span></span>
<span data-ttu-id="80584-130">Anger slutet av tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="80584-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="80584-131">-MaximumCapacity</span></span>
<span data-ttu-id="80584-132">Anger maximal kapacitet.</span><span class="sxs-lookup"><span data-stu-id="80584-132">Specifies the maximum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="80584-133">-MinimumCapacity</span></span>
<span data-ttu-id="80584-134">Anger den minsta kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="80584-134">Specifies the minimum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="80584-135">-Name</span></span>
<span data-ttu-id="80584-136">Anger namnet på den profil som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="80584-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="80584-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="80584-138">Anger frekvensen för återkommande.</span><span class="sxs-lookup"><span data-stu-id="80584-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="80584-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="80584-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="80584-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="80584-140">None</span></span>
- <span data-ttu-id="80584-141">Igen</span><span class="sxs-lookup"><span data-stu-id="80584-141">Second</span></span>
- <span data-ttu-id="80584-142">Minut</span><span class="sxs-lookup"><span data-stu-id="80584-142">Minute</span></span>
- <span data-ttu-id="80584-143">Timme</span><span class="sxs-lookup"><span data-stu-id="80584-143">Hour</span></span>
- <span data-ttu-id="80584-144">Day</span><span class="sxs-lookup"><span data-stu-id="80584-144">Day</span></span>
- <span data-ttu-id="80584-145">Fjorton</span><span class="sxs-lookup"><span data-stu-id="80584-145">Week</span></span>
- <span data-ttu-id="80584-146">Månad</span><span class="sxs-lookup"><span data-stu-id="80584-146">Month</span></span>
- <span data-ttu-id="80584-147">Det går inte att använda alla dessa värden.</span><span class="sxs-lookup"><span data-stu-id="80584-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-148">-Regel</span><span class="sxs-lookup"><span data-stu-id="80584-148">-Rule</span></span>
<span data-ttu-id="80584-149">Anger listan över regler som ska läggas till i profilen.</span><span class="sxs-lookup"><span data-stu-id="80584-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="80584-150">-ScheduleDay</span></span>
<span data-ttu-id="80584-151">Anger de schemalagda dagarna.</span><span class="sxs-lookup"><span data-stu-id="80584-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="80584-152">-ScheduleHour</span></span>
<span data-ttu-id="80584-153">Anger de schemalagda timmarna.</span><span class="sxs-lookup"><span data-stu-id="80584-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="80584-154">-ScheduleMinute</span></span>
<span data-ttu-id="80584-155">Anger det schemalagda antalet minuter.</span><span class="sxs-lookup"><span data-stu-id="80584-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="80584-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="80584-157">Anger tids zonen för schemat.</span><span class="sxs-lookup"><span data-stu-id="80584-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="80584-158">-StartTimeWindow</span></span>
<span data-ttu-id="80584-159">Anger tidsfönstrets början.</span><span class="sxs-lookup"><span data-stu-id="80584-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="80584-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="80584-161">Anger tids zonen för tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="80584-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80584-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80584-162">CommonParameters</span></span>
<span data-ttu-id="80584-163">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80584-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80584-164">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80584-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80584-165">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="80584-165">INPUTS</span></span>

### <span data-ttu-id="80584-166">System. String</span><span class="sxs-lookup"><span data-stu-id="80584-166">System.String</span></span>

### <span data-ttu-id="80584-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="80584-167">System.DateTime</span></span>

### <span data-ttu-id="80584-168">Microsoft. Azure. Management. Monitoring. Management. Models. RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="80584-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="80584-169">System. Collections. Generic. list ' 1 [[system. String, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80584-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="80584-170">System. Collections. Generic. list `1[[System.Nullable` 1 [[system. Int32, system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]], system. Private. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80584-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="80584-171">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Monitoring. Management. Models. ScaleRule, Microsoft. Azure. PowerShell. cmdletar. Monitor, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="80584-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="80584-172">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="80584-172">OUTPUTS</span></span>

### <span data-ttu-id="80584-173">Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="80584-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="80584-174">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="80584-174">NOTES</span></span>

## <span data-ttu-id="80584-175">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="80584-175">RELATED LINKS</span></span>

[<span data-ttu-id="80584-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="80584-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="80584-177">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="80584-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="80584-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="80584-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="80584-179">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="80584-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="80584-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="80584-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


