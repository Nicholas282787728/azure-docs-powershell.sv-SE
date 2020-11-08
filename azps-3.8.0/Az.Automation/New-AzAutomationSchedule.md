---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 9f9cd5b779fcc4e1b9dd6f3df7ed0255adeaa3af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092689"
---
# <span data-ttu-id="05603-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="05603-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="05603-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05603-102">SYNOPSIS</span></span>
<span data-ttu-id="05603-103">Skapar ett automations schema.</span><span class="sxs-lookup"><span data-stu-id="05603-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="05603-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05603-104">SYNTAX</span></span>

### <span data-ttu-id="05603-105">ByDaily (standard)</span><span class="sxs-lookup"><span data-stu-id="05603-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05603-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="05603-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05603-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="05603-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05603-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="05603-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05603-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="05603-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05603-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="05603-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05603-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05603-111">DESCRIPTION</span></span>
<span data-ttu-id="05603-112">**New-AzAutomationSchedule-** cmdleten skapar ett schema i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="05603-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="05603-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05603-113">EXAMPLES</span></span>

### <span data-ttu-id="05603-114">Exempel 1: skapa ett engångs schema i lokal tid</span><span class="sxs-lookup"><span data-stu-id="05603-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="05603-115">Det första kommandot får tidszons-ID: t från systemet och lagrar det i $TimeZone variabel.</span><span class="sxs-lookup"><span data-stu-id="05603-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="05603-116">Det andra kommandot skapar ett schema som körs ett klock slag på det aktuella datumet kl 11:00 EM i den angivna tids zonen..</span><span class="sxs-lookup"><span data-stu-id="05603-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="05603-117">Exempel 2: skapa ett återkommande schema</span><span class="sxs-lookup"><span data-stu-id="05603-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="05603-118">Det första kommandot skapar ett Date-objekt med hjälp av cmdleten **Get-date** och lagrar sedan objektet i variabeln $StartDate.</span><span class="sxs-lookup"><span data-stu-id="05603-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="05603-119">Ange en tid som är minst fem minuter framåt.</span><span class="sxs-lookup"><span data-stu-id="05603-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="05603-120">Det andra kommandot skapar ett Date-objekt med hjälp av cmdleten **Get-date** och lagrar sedan objektet i variabeln $EndDate.</span><span class="sxs-lookup"><span data-stu-id="05603-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="05603-121">Kommandot anger en framtida tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="05603-121">The command specifies a future time.</span></span>
<span data-ttu-id="05603-122">Med kommandot slut skapas ett dagligt schema med namnet Schedule02 som börjar vid den tid som lagras i $StartDate och upphör vid den tid som lagras i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="05603-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="05603-123">Exempel 3: skapa ett veckovis återkommande schema</span><span class="sxs-lookup"><span data-stu-id="05603-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="05603-124">Det första kommandot skapar ett Date-objekt med hjälp av cmdleten **Get-date** och lagrar sedan objektet i variabeln $StartDate.</span><span class="sxs-lookup"><span data-stu-id="05603-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="05603-125">Det andra kommandot skapar en matris med vecko dagar som innehåller måndag, tisdag, onsdag, torsdag och fredag.</span><span class="sxs-lookup"><span data-stu-id="05603-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="05603-126">Med kommandot slut skapas ett dagligt schema med namnet Schedule03 som kommer att köras måndag till fredag varje vecka på 13:00.</span><span class="sxs-lookup"><span data-stu-id="05603-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="05603-127">Schemat upphör aldrig att gälla.</span><span class="sxs-lookup"><span data-stu-id="05603-127">The schedule will never expire.</span></span>

## <span data-ttu-id="05603-128">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05603-128">PARAMETERS</span></span>

### <span data-ttu-id="05603-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05603-129">-AutomationAccountName</span></span>
<span data-ttu-id="05603-130">Anger namnet på ett Automation-konto som denna cmdlet skapar ett schema för.</span><span class="sxs-lookup"><span data-stu-id="05603-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05603-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="05603-131">-DayInterval</span></span>
<span data-ttu-id="05603-132">Anger ett intervall, i dagar, för schemat.</span><span class="sxs-lookup"><span data-stu-id="05603-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="05603-133">Om du inte anger den här parametern och du inte anger parametern *OneTime* , är standardvärdet ett (1).</span><span class="sxs-lookup"><span data-stu-id="05603-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByDaily
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05603-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="05603-134">-DayOfWeek</span></span>
<span data-ttu-id="05603-135">Anger en lista med vecko dagar för varje vecka.</span><span class="sxs-lookup"><span data-stu-id="05603-135">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.Nullable`1[System.DayOfWeek]
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05603-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="05603-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="05603-137">Anger vecko förekomsten i den månad som schemat körs.</span><span class="sxs-lookup"><span data-stu-id="05603-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="05603-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="05603-138">psdx_paramvalues</span></span>
- <span data-ttu-id="05603-139">9.1</span><span class="sxs-lookup"><span data-stu-id="05603-139">1</span></span>
- <span data-ttu-id="05603-140">två</span><span class="sxs-lookup"><span data-stu-id="05603-140">2</span></span>
- <span data-ttu-id="05603-141">amp;3D</span><span class="sxs-lookup"><span data-stu-id="05603-141">3</span></span>
- <span data-ttu-id="05603-142">9.4</span><span class="sxs-lookup"><span data-stu-id="05603-142">4</span></span>
- <span data-ttu-id="05603-143">-1</span><span class="sxs-lookup"><span data-stu-id="05603-143">-1</span></span>
- <span data-ttu-id="05603-144">Skapas</span><span class="sxs-lookup"><span data-stu-id="05603-144">First</span></span>
- <span data-ttu-id="05603-145">Igen</span><span class="sxs-lookup"><span data-stu-id="05603-145">Second</span></span>
- <span data-ttu-id="05603-146">Utanför</span><span class="sxs-lookup"><span data-stu-id="05603-146">Third</span></span>
- <span data-ttu-id="05603-147">Sång</span><span class="sxs-lookup"><span data-stu-id="05603-147">Fourth</span></span>
- <span data-ttu-id="05603-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="05603-148">LastDay</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05603-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="05603-149">-DaysOfMonth</span></span>
<span data-ttu-id="05603-150">Anger en lista på dagar i månaden för månads schemat.</span><span class="sxs-lookup"><span data-stu-id="05603-150">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases:
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05603-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="05603-151">-DaysOfWeek</span></span>
<span data-ttu-id="05603-152">Anger en lista med vecko dagar för varje vecka.</span><span class="sxs-lookup"><span data-stu-id="05603-152">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: ByWeekly
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05603-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05603-153">-DefaultProfile</span></span>
<span data-ttu-id="05603-154">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="05603-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05603-155">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="05603-155">-Description</span></span>
<span data-ttu-id="05603-156">Anger en beskrivning av schemat.</span><span class="sxs-lookup"><span data-stu-id="05603-156">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05603-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="05603-157">-ExpiryTime</span></span>
<span data-ttu-id="05603-158">Anger utgångs tiden för ett schema som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="05603-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="05603-159">Du kan ange en sträng som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="05603-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05603-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="05603-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="05603-161">Anger att det här schemaobjektet används för att schemalägga en program uppdaterings konfiguration</span><span class="sxs-lookup"><span data-stu-id="05603-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05603-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="05603-162">-HourInterval</span></span>
<span data-ttu-id="05603-163">Anger ett intervall, i timmar, för schemat.</span><span class="sxs-lookup"><span data-stu-id="05603-163">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByHourly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05603-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="05603-164">-MonthInterval</span></span>
<span data-ttu-id="05603-165">Anger ett intervall, i månader, för schemat.</span><span class="sxs-lookup"><span data-stu-id="05603-165">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05603-166">-Namn</span><span class="sxs-lookup"><span data-stu-id="05603-166">-Name</span></span>
<span data-ttu-id="05603-167">Anger ett namn för schemat.</span><span class="sxs-lookup"><span data-stu-id="05603-167">Specifies a name for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05603-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="05603-168">-OneTime</span></span>
<span data-ttu-id="05603-169">Anger att cmdleten skapar ett engångs schema.</span><span class="sxs-lookup"><span data-stu-id="05603-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByOneTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05603-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05603-170">-ResourceGroupName</span></span>
<span data-ttu-id="05603-171">Anger namnet på en resurs grupp för vilken denna cmdlet skapar ett schema.</span><span class="sxs-lookup"><span data-stu-id="05603-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05603-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="05603-172">-StartTime</span></span>
<span data-ttu-id="05603-173">Anger start tiden för ett schema som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="05603-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="05603-174">Du kan ange en sträng som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="05603-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="05603-175">Om parametern *timezone* anges ignoreras förskjutningen och den angivna tids zonen används.</span><span class="sxs-lookup"><span data-stu-id="05603-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05603-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="05603-176">-TimeZone</span></span>
<span data-ttu-id="05603-177">Anger tids zonen för schemat.</span><span class="sxs-lookup"><span data-stu-id="05603-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="05603-178">Strängen kan vara IANA-ID eller Windows tidszons-ID.</span><span class="sxs-lookup"><span data-stu-id="05603-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05603-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="05603-179">-WeekInterval</span></span>
<span data-ttu-id="05603-180">Anger ett intervall, i veckor, för schemat.</span><span class="sxs-lookup"><span data-stu-id="05603-180">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByWeekly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05603-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05603-181">CommonParameters</span></span>
<span data-ttu-id="05603-182">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05603-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05603-183">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05603-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05603-184">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05603-184">INPUTS</span></span>

### <span data-ttu-id="05603-185">System. String</span><span class="sxs-lookup"><span data-stu-id="05603-185">System.String</span></span>

### <span data-ttu-id="05603-186">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="05603-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="05603-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="05603-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="05603-188">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05603-188">OUTPUTS</span></span>

### <span data-ttu-id="05603-189">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="05603-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="05603-190">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05603-190">NOTES</span></span>

## <span data-ttu-id="05603-191">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05603-191">RELATED LINKS</span></span>

[<span data-ttu-id="05603-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="05603-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="05603-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="05603-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="05603-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="05603-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)

