---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9574CEB5-B699-4606-8C5E-CE2C0D01092D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupRetentionPolicyObject.md
ms.openlocfilehash: 3637709ca347a8e00433f247c80ec1c916e42017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575019"
---
# <span data-ttu-id="39f3c-101">New-AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="39f3c-101">New-AzureRmBackupRetentionPolicyObject</span></span>

## <span data-ttu-id="39f3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="39f3c-103">Skapar en bevarande princip för säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="39f3c-103">Creates a Backup retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39f3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39f3c-104">SYNTAX</span></span>

### <span data-ttu-id="39f3c-105">DailyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="39f3c-105">DailyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-DailyRetention] -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f3c-106">WeeklyRetentionParamSet</span><span class="sxs-lookup"><span data-stu-id="39f3c-106">WeeklyRetentionParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-WeeklyRetention] -DaysOfWeek <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f3c-107">MonthlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="39f3c-107">MonthlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f3c-108">MonthlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="39f3c-108">MonthlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-MonthlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f3c-109">YearlyRetentionInDailyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="39f3c-109">YearlyRetentionInDailyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInDailyFormat]
 -DaysOfMonth <System.Collections.Generic.List`1[System.String]> -MonthsOfYear <String[]> -Retention <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39f3c-110">YearlyRetentionInWeeklyFormatParamSet</span><span class="sxs-lookup"><span data-stu-id="39f3c-110">YearlyRetentionInWeeklyFormatParamSet</span></span>
```
New-AzureRmBackupRetentionPolicyObject [-YearlyRetentionInWeeklyFormat] -DaysOfWeek <String[]>
 -WeekNumber <String[]> -MonthsOfYear <String[]> -Retention <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39f3c-111">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39f3c-111">DESCRIPTION</span></span>
<span data-ttu-id="39f3c-112">Cmdleten **New-AzureRmBackupRetentionPolicyObject** skapar en lagrings princip för Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="39f3c-112">The **New-AzureRmBackupRetentionPolicyObject** cmdlet creates an Azure Backup retention policy.</span></span>
<span data-ttu-id="39f3c-113">En bevarande princip definierar hur länge säkerhets kopian behåller en återställnings punkt.</span><span class="sxs-lookup"><span data-stu-id="39f3c-113">A retention policy defines how long Backup keeps a recovery point.</span></span>
<span data-ttu-id="39f3c-114">Följande typer av bevarande är:</span><span class="sxs-lookup"><span data-stu-id="39f3c-114">The types of retention are the following:</span></span> 

- <span data-ttu-id="39f3c-115">Vardag</span><span class="sxs-lookup"><span data-stu-id="39f3c-115">Daily</span></span> 
- <span data-ttu-id="39f3c-116">Vecko</span><span class="sxs-lookup"><span data-stu-id="39f3c-116">Weekly</span></span> 
- <span data-ttu-id="39f3c-117">Månaders</span><span class="sxs-lookup"><span data-stu-id="39f3c-117">Monthly</span></span> 
- <span data-ttu-id="39f3c-118">Års</span><span class="sxs-lookup"><span data-stu-id="39f3c-118">Yearly</span></span> 

<span data-ttu-id="39f3c-119">Skapa en bevarande princip för varje typ av bevarande som du planerar att använda.</span><span class="sxs-lookup"><span data-stu-id="39f3c-119">Create one retention policy for each type of retention that you plan to use.</span></span>

<span data-ttu-id="39f3c-120">En säkerhets kopierings princip är kopplad till minst en bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="39f3c-120">A backup policy is associated with at least one retention policy.</span></span>
<span data-ttu-id="39f3c-121">Använd New-AzureRmBackupProtectionPolicy cmdlet för att skapa en säkerhets kopierings princip.</span><span class="sxs-lookup"><span data-stu-id="39f3c-121">To create a backup policy, use the New-AzureRmBackupProtectionPolicy cmdlet.</span></span>
<span data-ttu-id="39f3c-122">Du kan istället ange en bevarande princip för Enable-AzureRmBackupProtection cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f3c-122">You can instead provide a retention policy to the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="39f3c-123">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39f3c-123">EXAMPLES</span></span>

### <span data-ttu-id="39f3c-124">Exempel 1: skapa en bevarande princip för daglig bevarande</span><span class="sxs-lookup"><span data-stu-id="39f3c-124">Example 1: Create a retention policy for daily retention</span></span>
```
PS C:\>$Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Daily
RetentionType      Retention          RetentionTimes
-------------      ---------          --------------
Daily              30
```

<span data-ttu-id="39f3c-125">Det första kommandot skapar en bevarande princip för 30 dagar efter varje dag och lagrar sedan den i $Daily variabel.</span><span class="sxs-lookup"><span data-stu-id="39f3c-125">The first command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="39f3c-126">Det andra kommandot visar innehållet i $Daily.</span><span class="sxs-lookup"><span data-stu-id="39f3c-126">The second command displays the contents of $Daily.</span></span>

### <span data-ttu-id="39f3c-127">Exempel 2: skapa en bevarande princip per månad</span><span class="sxs-lookup"><span data-stu-id="39f3c-127">Example 2: Create a monthly retention policy</span></span>
```
PS C:\>$Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $Monthly | select *
RetentionFormat : Daily
DaysOfMonth     : {10, 20}
WeekNumber      : 
DaysOfWeek      : 
RetentionType   : Monthly
Retention       : 12
RetentionTimes  :
```

<span data-ttu-id="39f3c-128">Det första kommandot skapar en bevarande princip som behåller den tionde och tjugonde varje månad under tolv månader.</span><span class="sxs-lookup"><span data-stu-id="39f3c-128">The first command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="39f3c-129">Kommandot lagrar bevarande principen i $Monthly variabel.</span><span class="sxs-lookup"><span data-stu-id="39f3c-129">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="39f3c-130">Det andra kommandot visar innehållet i $Monthly.</span><span class="sxs-lookup"><span data-stu-id="39f3c-130">The second command displays the contents of $Monthly.</span></span>

## <span data-ttu-id="39f3c-131">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39f3c-131">PARAMETERS</span></span>

### <span data-ttu-id="39f3c-132">-DailyRetention</span><span class="sxs-lookup"><span data-stu-id="39f3c-132">-DailyRetention</span></span>
<span data-ttu-id="39f3c-133">Anger att den här cmdleten skapar en daglig bevarande princip.</span><span class="sxs-lookup"><span data-stu-id="39f3c-133">Indicates that this cmdlet creates a Daily retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-134">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="39f3c-134">-DaysOfMonth</span></span>
<span data-ttu-id="39f3c-135">Anger vilka dagar i månaden som identifierar vilka återställnings punkter som säkerhets kopior finns kvar och hur länge.</span><span class="sxs-lookup"><span data-stu-id="39f3c-135">Specifies the days of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="39f3c-136">De acceptabla värdena för den här parametern är: heltal mellan 1 och 28 och sist.</span><span class="sxs-lookup"><span data-stu-id="39f3c-136">The acceptable values for this parameter are: integers from 1 through 28 and Last.</span></span>
<span data-ttu-id="39f3c-137">Ange den här parametern om du anger parametrarna *DailyRetention* , *MonthlyRetentionInDailyFormat* och *YearlyRetentionInDailyFormat* .</span><span class="sxs-lookup"><span data-stu-id="39f3c-137">Specify this parameter if you specify the *DailyRetention* , *MonthlyRetentionInDailyFormat* , and *YearlyRetentionInDailyFormat* parameters.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: MonthlyRetentionInDailyFormatParamSet, YearlyRetentionInDailyFormatParamSet
Aliases: 
Accepted values: 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-138">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="39f3c-138">-DaysOfWeek</span></span>
<span data-ttu-id="39f3c-139">Anger en matris med dagar i veckan.</span><span class="sxs-lookup"><span data-stu-id="39f3c-139">Specifies an array of days of the week.</span></span>
<span data-ttu-id="39f3c-140">De dagar som denna cmdlet anger för att identifiera vilka återställnings punkter som säkerhets kopian sparas och hur länge.</span><span class="sxs-lookup"><span data-stu-id="39f3c-140">The days that this cmdlet specifies identify which recovery points that Backup retains and for how long.</span></span>
<span data-ttu-id="39f3c-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="39f3c-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39f3c-142">Dagarna</span><span class="sxs-lookup"><span data-stu-id="39f3c-142">Monday</span></span> 
- <span data-ttu-id="39f3c-143">Torsdag</span><span class="sxs-lookup"><span data-stu-id="39f3c-143">Tuesday</span></span> 
- <span data-ttu-id="39f3c-144">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="39f3c-144">Wednesday</span></span> 
- <span data-ttu-id="39f3c-145">Torsdag</span><span class="sxs-lookup"><span data-stu-id="39f3c-145">Thursday</span></span> 
- <span data-ttu-id="39f3c-146">Fredag</span><span class="sxs-lookup"><span data-stu-id="39f3c-146">Friday</span></span> 
- <span data-ttu-id="39f3c-147">Afton</span><span class="sxs-lookup"><span data-stu-id="39f3c-147">Saturday</span></span> 
- <span data-ttu-id="39f3c-148">Lördag</span><span class="sxs-lookup"><span data-stu-id="39f3c-148">Sunday</span></span>

<span data-ttu-id="39f3c-149">Ange den här parametern om du anger parametrarna *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* och *YearlyRetentionInWeeklyFormat* .</span><span class="sxs-lookup"><span data-stu-id="39f3c-149">Specify this parameter if you specify the *WeeklyRetention* , *MonthlyRetentionInWeeklyFormat* , and *YearlyRetentionInWeeklyFormat* parameters.</span></span>

<span data-ttu-id="39f3c-150">Se till att de vecko dagar du väljer för säkerhets kopiering och kvarhållande är justerade.</span><span class="sxs-lookup"><span data-stu-id="39f3c-150">Be sure that the days of the week you select for backup and for retention are aligned.</span></span>
<span data-ttu-id="39f3c-151">Till exempel, om din säkerhets kopia är inställd för lördagar, måste bevarande principer också använda lördag.</span><span class="sxs-lookup"><span data-stu-id="39f3c-151">For example, if your backup is set for Saturdays, the retention policies must also use Saturday.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WeeklyRetentionParamSet, MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-152">-MonthlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="39f3c-152">-MonthlyRetentionInDailyFormat</span></span>
<span data-ttu-id="39f3c-153">Anger att den här cmdleten skapar en månatlig princip i önskat format.</span><span class="sxs-lookup"><span data-stu-id="39f3c-153">Indicates that this cmdlet creates a Monthly policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-154">-MonthlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="39f3c-154">-MonthlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="39f3c-155">Anger att denna cmdlet skapar en månatlig princip i vecko format.</span><span class="sxs-lookup"><span data-stu-id="39f3c-155">Indicates that this cmdlet creates a Monthly policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-156">-MonthsOfYear</span><span class="sxs-lookup"><span data-stu-id="39f3c-156">-MonthsOfYear</span></span>
<span data-ttu-id="39f3c-157">Anger vilka månader som har återställnings punkter som säkerhets kopian kvarhåller.</span><span class="sxs-lookup"><span data-stu-id="39f3c-157">Specifies which months of the year have the recovery points that Backup retains on a yearly basis.</span></span>
<span data-ttu-id="39f3c-158">De acceptabla värdena för den här parametern är: namn på månader, till exempel januari och februari.</span><span class="sxs-lookup"><span data-stu-id="39f3c-158">The acceptable values for this parameter are: names of months, such as January or February.</span></span>

```yaml
Type: System.String[]
Parameter Sets: YearlyRetentionInDailyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: January, February, March, April, May, June, July, August, September, October, November, December

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-159">-Bevarande</span><span class="sxs-lookup"><span data-stu-id="39f3c-159">-Retention</span></span>
<span data-ttu-id="39f3c-160">Anger den bevarande period, i dagar, månader eller år, för vilken säkerhets kopian lagrar en säkerhets kopie rad.</span><span class="sxs-lookup"><span data-stu-id="39f3c-160">Specifies the retention period, in days, months, or years, for which Backup stores a backup point.</span></span>
<span data-ttu-id="39f3c-161">Enheten beror på om den här cmdleten väljer ett alternativ för daglig, månatlig eller årlig bevarande.</span><span class="sxs-lookup"><span data-stu-id="39f3c-161">The unit depends on whether this cmdlet selects a daily, monthly, or yearly retention option.</span></span>
<span data-ttu-id="39f3c-162">Om du till exempel anger parametern *DailyRetention* , tolkar cmdleten den aktuella parametern som ett antal dagar.</span><span class="sxs-lookup"><span data-stu-id="39f3c-162">For example, if specify the *DailyRetention* parameter, the cmdlet interprets the current parameter as a number of days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-163">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="39f3c-163">-WeeklyRetention</span></span>
<span data-ttu-id="39f3c-164">Anger att denna cmdlet skapar en bevarande princip för varje vecka.</span><span class="sxs-lookup"><span data-stu-id="39f3c-164">Indicates that this cmdlet creates a Weekly retention policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyRetentionParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-165">-WeekNumber</span><span class="sxs-lookup"><span data-stu-id="39f3c-165">-WeekNumber</span></span>
<span data-ttu-id="39f3c-166">Anger veckorna för den månad som visar vilka återställnings punkter som säkerhets kopior kvarstår och hur länge.</span><span class="sxs-lookup"><span data-stu-id="39f3c-166">Specifies the weeks of the month that identify which recovery points Backup retains and for how long.</span></span>
<span data-ttu-id="39f3c-167">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="39f3c-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39f3c-168">Skapas</span><span class="sxs-lookup"><span data-stu-id="39f3c-168">First</span></span> 
- <span data-ttu-id="39f3c-169">Igen</span><span class="sxs-lookup"><span data-stu-id="39f3c-169">Second</span></span> 
- <span data-ttu-id="39f3c-170">Utanför</span><span class="sxs-lookup"><span data-stu-id="39f3c-170">Third</span></span> 
- <span data-ttu-id="39f3c-171">Sång</span><span class="sxs-lookup"><span data-stu-id="39f3c-171">Fourth</span></span> 
- <span data-ttu-id="39f3c-172">Senast</span><span class="sxs-lookup"><span data-stu-id="39f3c-172">Last</span></span>

```yaml
Type: System.String[]
Parameter Sets: MonthlyRetentionInWeeklyFormatParamSet, YearlyRetentionInWeeklyFormatParamSet
Aliases: 
Accepted values: First, Second, Third, Fourth, Last

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-173">-YearlyRetentionInDailyFormat</span><span class="sxs-lookup"><span data-stu-id="39f3c-173">-YearlyRetentionInDailyFormat</span></span>
<span data-ttu-id="39f3c-174">Anger att den här cmdleten skapar en årlig bevarande princip i varje dagligt format.</span><span class="sxs-lookup"><span data-stu-id="39f3c-174">Indicates that this cmdlet creates a Yearly retention policy in Daily format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInDailyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-175">-YearlyRetentionInWeeklyFormat</span><span class="sxs-lookup"><span data-stu-id="39f3c-175">-YearlyRetentionInWeeklyFormat</span></span>
<span data-ttu-id="39f3c-176">Anger att den här cmdleten skapar en årlig bevarande princip i varje vecka.</span><span class="sxs-lookup"><span data-stu-id="39f3c-176">Indicates that this cmdlet creates a Yearly retention policy in Weekly format.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: YearlyRetentionInWeeklyFormatParamSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f3c-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f3c-177">-DefaultProfile</span></span>
<span data-ttu-id="39f3c-178">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39f3c-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39f3c-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f3c-179">CommonParameters</span></span>
<span data-ttu-id="39f3c-180">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f3c-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f3c-181">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39f3c-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f3c-182">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39f3c-182">INPUTS</span></span>

### <span data-ttu-id="39f3c-183">Ingen</span><span class="sxs-lookup"><span data-stu-id="39f3c-183">None</span></span>

## <span data-ttu-id="39f3c-184">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39f3c-184">OUTPUTS</span></span>

### <span data-ttu-id="39f3c-185">AzureRmBackupRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39f3c-185">AzureRmBackupRetentionPolicy</span></span>

## <span data-ttu-id="39f3c-186">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39f3c-186">NOTES</span></span>
* <span data-ttu-id="39f3c-187">Ingen</span><span class="sxs-lookup"><span data-stu-id="39f3c-187">None</span></span>

## <span data-ttu-id="39f3c-188">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39f3c-188">RELATED LINKS</span></span>

[<span data-ttu-id="39f3c-189">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="39f3c-189">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="39f3c-190">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="39f3c-190">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


