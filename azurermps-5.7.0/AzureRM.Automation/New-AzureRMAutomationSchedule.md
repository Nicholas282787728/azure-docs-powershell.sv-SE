---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: 3528a95e9dab3c92571ec49e9bf5d567012fb5b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583691"
---
# <span data-ttu-id="6513b-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6513b-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="6513b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6513b-102">SYNOPSIS</span></span>
<span data-ttu-id="6513b-103">Skapar ett automations schema.</span><span class="sxs-lookup"><span data-stu-id="6513b-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6513b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6513b-104">SYNTAX</span></span>

### <span data-ttu-id="6513b-105">ByDaily (standard)</span><span class="sxs-lookup"><span data-stu-id="6513b-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6513b-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="6513b-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6513b-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="6513b-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6513b-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="6513b-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6513b-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="6513b-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6513b-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="6513b-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6513b-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6513b-111">DESCRIPTION</span></span>
<span data-ttu-id="6513b-112">**New-AzureRmAutomationSchedule-** cmdleten skapar ett schema i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6513b-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="6513b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6513b-113">EXAMPLES</span></span>

### <span data-ttu-id="6513b-114">Exempel 1: skapa ett engångs schema i lokal tid</span><span class="sxs-lookup"><span data-stu-id="6513b-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="6513b-115">Det första kommandot får tidszons-ID: t från systemet och lagrar det i $TimeZone variabel.</span><span class="sxs-lookup"><span data-stu-id="6513b-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="6513b-116">Det andra kommandot skapar ett schema som körs ett klock slag på det aktuella datumet kl 11:00 EM i den angivna tids zonen..</span><span class="sxs-lookup"><span data-stu-id="6513b-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="6513b-117">Exempel 2: skapa ett återkommande schema</span><span class="sxs-lookup"><span data-stu-id="6513b-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6513b-118">Det första kommandot skapar ett Date-objekt med hjälp av cmdleten **Get-date** och lagrar sedan objektet i variabeln $StartDate.</span><span class="sxs-lookup"><span data-stu-id="6513b-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="6513b-119">Ange en tid som är minst fem minuter framåt.</span><span class="sxs-lookup"><span data-stu-id="6513b-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="6513b-120">Det andra kommandot skapar ett Date-objekt med hjälp av cmdleten **Get-date** och lagrar sedan objektet i variabeln $EndDate.</span><span class="sxs-lookup"><span data-stu-id="6513b-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="6513b-121">Kommandot anger en framtida tidpunkt.</span><span class="sxs-lookup"><span data-stu-id="6513b-121">The command specifies a future time.</span></span>

<span data-ttu-id="6513b-122">Med kommandot slut skapas ett dagligt schema med namnet Schedule01 som börjar vid den tid som lagras i $StartDate och upphör vid den tid som lagras i $EndDate.</span><span class="sxs-lookup"><span data-stu-id="6513b-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="6513b-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6513b-123">PARAMETERS</span></span>

### <span data-ttu-id="6513b-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6513b-124">-AutomationAccountName</span></span>
<span data-ttu-id="6513b-125">Anger namnet på ett Automation-konto som denna cmdlet skapar ett schema för.</span><span class="sxs-lookup"><span data-stu-id="6513b-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-126">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="6513b-126">-DayInterval</span></span>
<span data-ttu-id="6513b-127">Anger ett intervall, i dagar, för schemat.</span><span class="sxs-lookup"><span data-stu-id="6513b-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="6513b-128">Om du inte anger den här parametern och du inte anger parametern *OneTime* , är standardvärdet ett (1).</span><span class="sxs-lookup"><span data-stu-id="6513b-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="6513b-129">-DayOfWeek</span></span>
<span data-ttu-id="6513b-130">Anger en lista med vecko dagar för varje vecka.</span><span class="sxs-lookup"><span data-stu-id="6513b-130">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="6513b-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="6513b-132">Anger vecko förekomsten i den månad som schemat körs.</span><span class="sxs-lookup"><span data-stu-id="6513b-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="6513b-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="6513b-133">psdx_paramvalues</span></span>

- <span data-ttu-id="6513b-134">9.1</span><span class="sxs-lookup"><span data-stu-id="6513b-134">1</span></span>
- <span data-ttu-id="6513b-135">två</span><span class="sxs-lookup"><span data-stu-id="6513b-135">2</span></span>
- <span data-ttu-id="6513b-136">amp;3D</span><span class="sxs-lookup"><span data-stu-id="6513b-136">3</span></span>
- <span data-ttu-id="6513b-137">9.4</span><span class="sxs-lookup"><span data-stu-id="6513b-137">4</span></span>
- <span data-ttu-id="6513b-138">-1</span><span class="sxs-lookup"><span data-stu-id="6513b-138">-1</span></span>
- <span data-ttu-id="6513b-139">Skapas</span><span class="sxs-lookup"><span data-stu-id="6513b-139">First</span></span>
- <span data-ttu-id="6513b-140">Igen</span><span class="sxs-lookup"><span data-stu-id="6513b-140">Second</span></span>
- <span data-ttu-id="6513b-141">Utanför</span><span class="sxs-lookup"><span data-stu-id="6513b-141">Third</span></span>
- <span data-ttu-id="6513b-142">Sång</span><span class="sxs-lookup"><span data-stu-id="6513b-142">Fourth</span></span>
- <span data-ttu-id="6513b-143">LastDay</span><span class="sxs-lookup"><span data-stu-id="6513b-143">LastDay</span></span>

```yaml
Type: DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-144">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="6513b-144">-DaysOfMonth</span></span>
<span data-ttu-id="6513b-145">Anger en lista på dagar i månaden för månads schemat.</span><span class="sxs-lookup"><span data-stu-id="6513b-145">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases: 
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-146">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="6513b-146">-DaysOfWeek</span></span>
<span data-ttu-id="6513b-147">Anger en lista med vecko dagar för varje vecka.</span><span class="sxs-lookup"><span data-stu-id="6513b-147">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: DayOfWeek[]
Parameter Sets: ByWeekly
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6513b-148">-DefaultProfile</span></span>
<span data-ttu-id="6513b-149">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6513b-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6513b-150">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="6513b-150">-Description</span></span>
<span data-ttu-id="6513b-151">Anger en beskrivning av schemat.</span><span class="sxs-lookup"><span data-stu-id="6513b-151">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-152">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="6513b-152">-ExpiryTime</span></span>
<span data-ttu-id="6513b-153">Anger utgångs tiden för ett schema som ett **DateTimeOffest** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6513b-153">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="6513b-154">Du kan ange en sträng som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="6513b-154">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-155">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="6513b-155">-HourInterval</span></span>
<span data-ttu-id="6513b-156">Anger ett intervall, i timmar, för schemat.</span><span class="sxs-lookup"><span data-stu-id="6513b-156">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-157">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="6513b-157">-MonthInterval</span></span>
<span data-ttu-id="6513b-158">Anger ett intervall, i månader, för schemat.</span><span class="sxs-lookup"><span data-stu-id="6513b-158">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-159">-Namn</span><span class="sxs-lookup"><span data-stu-id="6513b-159">-Name</span></span>
<span data-ttu-id="6513b-160">Anger ett namn för schemat.</span><span class="sxs-lookup"><span data-stu-id="6513b-160">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-161">-OneTime</span><span class="sxs-lookup"><span data-stu-id="6513b-161">-OneTime</span></span>
<span data-ttu-id="6513b-162">Anger att cmdleten skapar ett engångs schema.</span><span class="sxs-lookup"><span data-stu-id="6513b-162">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6513b-163">-ResourceGroupName</span></span>
<span data-ttu-id="6513b-164">Anger namnet på en resurs grupp för vilken denna cmdlet skapar ett schema.</span><span class="sxs-lookup"><span data-stu-id="6513b-164">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-165">-StartTime</span><span class="sxs-lookup"><span data-stu-id="6513b-165">-StartTime</span></span>
<span data-ttu-id="6513b-166">Anger start tiden för ett schema som ett **DateTimeOffset** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6513b-166">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="6513b-167">Du kan ange en sträng som kan konverteras till en giltig **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="6513b-167">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="6513b-168">.</span><span class="sxs-lookup"><span data-stu-id="6513b-168">.</span></span> <span data-ttu-id="6513b-169">Om parametern *timezone* anges ignoreras förskjutningen och den angivna tids zonen används.</span><span class="sxs-lookup"><span data-stu-id="6513b-169">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-170">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="6513b-170">-TimeZone</span></span>
<span data-ttu-id="6513b-171">Anger tids zonen för schemat.</span><span class="sxs-lookup"><span data-stu-id="6513b-171">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="6513b-172">Strängen kan vara IANA-ID eller Windows tidszons-ID.</span><span class="sxs-lookup"><span data-stu-id="6513b-172">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-173">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="6513b-173">-WeekInterval</span></span>
<span data-ttu-id="6513b-174">Anger ett intervall, i veckor, för schemat.</span><span class="sxs-lookup"><span data-stu-id="6513b-174">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByWeekly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6513b-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6513b-175">CommonParameters</span></span>
<span data-ttu-id="6513b-176">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6513b-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6513b-177">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6513b-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6513b-178">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6513b-178">INPUTS</span></span>

### <span data-ttu-id="6513b-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="6513b-179">None</span></span>
<span data-ttu-id="6513b-180">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="6513b-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6513b-181">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6513b-181">OUTPUTS</span></span>

### <span data-ttu-id="6513b-182">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="6513b-182">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="6513b-183">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6513b-183">NOTES</span></span>

## <span data-ttu-id="6513b-184">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6513b-184">RELATED LINKS</span></span>

[<span data-ttu-id="6513b-185">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6513b-185">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="6513b-186">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6513b-186">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="6513b-187">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6513b-187">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


