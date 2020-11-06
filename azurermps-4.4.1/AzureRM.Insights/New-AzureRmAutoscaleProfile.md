---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: a5cea42544f2f24ad6c1f1cc1ce64bf122e53440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584732"
---
# <span data-ttu-id="3b009-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="3b009-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="3b009-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b009-102">SYNOPSIS</span></span>
<span data-ttu-id="3b009-103">Skapar en Autoskala-profil.</span><span class="sxs-lookup"><span data-stu-id="3b009-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b009-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b009-104">SYNTAX</span></span>

### <span data-ttu-id="3b009-105">Parametrar för New-AzureRmAutoscaleProfile cmdlet utan schemalagda tider</span><span class="sxs-lookup"><span data-stu-id="3b009-105">Parameters for New-AzureRmAutoscaleProfile cmdlet without scheduled times</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b009-106">Parametrar för New-AzureRmAutoscaleProfile cmdlet med åtgärd för fast datum</span><span class="sxs-lookup"><span data-stu-id="3b009-106">Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b009-107">Parametrar för New-AzureRmAutoscaleProfile cmdlet med återkommande tids planering</span><span class="sxs-lookup"><span data-stu-id="3b009-107">Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDays <System.Collections.Generic.List`1[System.String]>
 -ScheduleHours <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinutes <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b009-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b009-108">DESCRIPTION</span></span>
<span data-ttu-id="3b009-109">Cmdleten **New-AzureRmAutoscaleProfile** skapar en Autoskala-profil.</span><span class="sxs-lookup"><span data-stu-id="3b009-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="3b009-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b009-110">EXAMPLES</span></span>

### <span data-ttu-id="3b009-111">Exempel 1: skapa en profil med ett fast datum</span><span class="sxs-lookup"><span data-stu-id="3b009-111">Example 1: Create single profile with a fixed date</span></span>
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

<span data-ttu-id="3b009-112">Det första kommandot skapar en autoskale-regel med namnet förfrågningar och lagrar den sedan i $Rule variabel.</span><span class="sxs-lookup"><span data-stu-id="3b009-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="3b009-113">Det andra kommandot skapar en profil med namnet Profile01 med ett fast datum med regeln i $Rule.</span><span class="sxs-lookup"><span data-stu-id="3b009-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="3b009-114">Exempel 2: skapa en profil med ett schema</span><span class="sxs-lookup"><span data-stu-id="3b009-114">Example 2: Create a profile with a schedule</span></span>
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

<span data-ttu-id="3b009-115">Det första kommandot skapar en autoskale-regel med namnet förfrågningar och lagrar den sedan i $Rule variabel.</span><span class="sxs-lookup"><span data-stu-id="3b009-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="3b009-116">Det andra kommandot skapar en profil med namnet SecondProfileName med ett återkommande schema med hjälp av regeln i $Rule.</span><span class="sxs-lookup"><span data-stu-id="3b009-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="3b009-117">Exempel 3: skapa profiler med två regler</span><span class="sxs-lookup"><span data-stu-id="3b009-117">Example 3: Create profiles with two rules</span></span>
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

<span data-ttu-id="3b009-118">De två första kommandona skapar regler och lagrar dem i variabelrna $Rule 1 och $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="3b009-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="3b009-119">Det tredje kommandot skapar en profil med namnet profilnamn med reglerna i Rule1 och Rule2 och lagrar dem sedan i variabeln $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="3b009-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="3b009-120">Med kommandot slut skapas en profil med namnet SecondProfileName med reglerna i Rule1 och Rule2 och sparas sedan i variabeln $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="3b009-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="3b009-121">Exempel 4: skapa en profil utan schema eller fast datum</span><span class="sxs-lookup"><span data-stu-id="3b009-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="3b009-122">Det första kommandot skapar en autoskale-regel med namnet förfrågningar och lagrar den sedan i $Rule variabel.</span><span class="sxs-lookup"><span data-stu-id="3b009-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="3b009-123">Det andra kommandot skapar en profil utan ett schema eller ett fast datum och lagrar den sedan i $Profile variabel.</span><span class="sxs-lookup"><span data-stu-id="3b009-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="3b009-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b009-124">PARAMETERS</span></span>

### <span data-ttu-id="3b009-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="3b009-125">-DefaultCapacity</span></span>
<span data-ttu-id="3b009-126">Anger standard kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="3b009-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="3b009-127">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="3b009-127">-EndTimeWindow</span></span>
<span data-ttu-id="3b009-128">Anger slutet av tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="3b009-128">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b009-129">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="3b009-129">-MaximumCapacity</span></span>
<span data-ttu-id="3b009-130">Anger maximal kapacitet.</span><span class="sxs-lookup"><span data-stu-id="3b009-130">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="3b009-131">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="3b009-131">-MinimumCapacity</span></span>
<span data-ttu-id="3b009-132">Anger den minsta kapaciteten.</span><span class="sxs-lookup"><span data-stu-id="3b009-132">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="3b009-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="3b009-133">-Name</span></span>
<span data-ttu-id="3b009-134">Anger namnet på den profil som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3b009-134">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="3b009-135">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="3b009-135">-RecurrenceFrequency</span></span>
<span data-ttu-id="3b009-136">Anger frekvensen för återkommande.</span><span class="sxs-lookup"><span data-stu-id="3b009-136">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="3b009-137">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3b009-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b009-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="3b009-138">None</span></span>
- <span data-ttu-id="3b009-139">Igen</span><span class="sxs-lookup"><span data-stu-id="3b009-139">Second</span></span>
- <span data-ttu-id="3b009-140">Minut</span><span class="sxs-lookup"><span data-stu-id="3b009-140">Minute</span></span>
- <span data-ttu-id="3b009-141">Timme</span><span class="sxs-lookup"><span data-stu-id="3b009-141">Hour</span></span>
- <span data-ttu-id="3b009-142">Day</span><span class="sxs-lookup"><span data-stu-id="3b009-142">Day</span></span>
- <span data-ttu-id="3b009-143">Fjorton</span><span class="sxs-lookup"><span data-stu-id="3b009-143">Week</span></span>
- <span data-ttu-id="3b009-144">Månad</span><span class="sxs-lookup"><span data-stu-id="3b009-144">Month</span></span>
- <span data-ttu-id="3b009-145">Vinåret</span><span class="sxs-lookup"><span data-stu-id="3b009-145">Year</span></span>

<span data-ttu-id="3b009-146">Alla dessa värden stöds inte.</span><span class="sxs-lookup"><span data-stu-id="3b009-146">Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b009-147">-Regler</span><span class="sxs-lookup"><span data-stu-id="3b009-147">-Rules</span></span>
<span data-ttu-id="3b009-148">Anger listan över regler som ska läggas till i profilen.</span><span class="sxs-lookup"><span data-stu-id="3b009-148">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="3b009-149">-ScheduleDays</span><span class="sxs-lookup"><span data-stu-id="3b009-149">-ScheduleDays</span></span>
<span data-ttu-id="3b009-150">Anger de schemalagda dagarna.</span><span class="sxs-lookup"><span data-stu-id="3b009-150">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b009-151">-ScheduleHours</span><span class="sxs-lookup"><span data-stu-id="3b009-151">-ScheduleHours</span></span>
<span data-ttu-id="3b009-152">Anger de schemalagda timmarna.</span><span class="sxs-lookup"><span data-stu-id="3b009-152">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b009-153">-ScheduleMinutes</span><span class="sxs-lookup"><span data-stu-id="3b009-153">-ScheduleMinutes</span></span>
<span data-ttu-id="3b009-154">Anger det schemalagda antalet minuter.</span><span class="sxs-lookup"><span data-stu-id="3b009-154">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b009-155">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="3b009-155">-ScheduleTimeZone</span></span>
<span data-ttu-id="3b009-156">Anger tids zonen för schemat.</span><span class="sxs-lookup"><span data-stu-id="3b009-156">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b009-157">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="3b009-157">-StartTimeWindow</span></span>
<span data-ttu-id="3b009-158">Anger tidsfönstrets början.</span><span class="sxs-lookup"><span data-stu-id="3b009-158">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b009-159">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="3b009-159">-TimeWindowTimeZone</span></span>
<span data-ttu-id="3b009-160">Anger tids zonen för tidsfönstret.</span><span class="sxs-lookup"><span data-stu-id="3b009-160">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b009-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b009-161">-DefaultProfile</span></span>
<span data-ttu-id="3b009-162">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b009-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b009-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b009-163">CommonParameters</span></span>
<span data-ttu-id="3b009-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b009-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b009-165">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b009-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b009-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b009-166">INPUTS</span></span>

## <span data-ttu-id="3b009-167">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b009-167">OUTPUTS</span></span>

### <span data-ttu-id="3b009-168">Microsoft. Azure. Management. Monitoring. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="3b009-168">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="3b009-169">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b009-169">NOTES</span></span>

## <span data-ttu-id="3b009-170">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b009-170">RELATED LINKS</span></span>

[<span data-ttu-id="3b009-171">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="3b009-171">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="3b009-172">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="3b009-172">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="3b009-173">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="3b009-173">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="3b009-174">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="3b009-174">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="3b009-175">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="3b009-175">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


