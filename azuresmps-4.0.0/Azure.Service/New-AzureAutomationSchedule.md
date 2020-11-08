---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D28DD808-E8EF-4C71-A353-8BF1E458DF6F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9fcae4a0232331a020a716b3f7284b8f6dfc3212
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099449"
---
# <span data-ttu-id="e3882-101">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e3882-101">New-AzureAutomationSchedule</span></span>

## <span data-ttu-id="e3882-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e3882-102">SYNOPSIS</span></span>

<span data-ttu-id="e3882-103">Skapar ett automations schema.</span><span class="sxs-lookup"><span data-stu-id="e3882-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="e3882-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e3882-104">SYNTAX</span></span>

### <span data-ttu-id="e3882-105">ByDaily (standard)</span><span class="sxs-lookup"><span data-stu-id="e3882-105">ByDaily (Default)</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3882-106">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="e3882-106">ByOneTime</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>] [-OneTime]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e3882-107">ByHourly</span><span class="sxs-lookup"><span data-stu-id="e3882-107">ByHourly</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e3882-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e3882-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="e3882-109">**New-AzureAutomationSchedule-** cmdleten skapar ett schema i Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e3882-109">The **New-AzureAutomationSchedule** cmdlet creates a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="e3882-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e3882-110">EXAMPLES</span></span>

### <span data-ttu-id="e3882-111">Exempel 1: skapa ett engångs schema</span><span class="sxs-lookup"><span data-stu-id="e3882-111">Example 1: Create a one-time schedule</span></span>
```
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime
```

<span data-ttu-id="e3882-112">Med följande kommando skapas ett schema som körs en gång för det aktuella datumet kl 11:00 EM.</span><span class="sxs-lookup"><span data-stu-id="e3882-112">The following command creates a schedule that runs one time on the current date at 11:00 PM.</span></span>

### <span data-ttu-id="e3882-113">Exempel 2: skapa ett återkommande schema</span><span class="sxs-lookup"><span data-stu-id="e3882-113">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1
```

<span data-ttu-id="e3882-114">Med följande kommandon skapas ett nytt schema som löper på 1:00 PM varje dag för ett år från den aktuella dagen.</span><span class="sxs-lookup"><span data-stu-id="e3882-114">The following commands create a new schedule that runs at 1:00 PM every day for one year starting on the current day.</span></span>

## <span data-ttu-id="e3882-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e3882-115">PARAMETERS</span></span>

### <span data-ttu-id="e3882-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e3882-116">-AutomationAccountName</span></span>
<span data-ttu-id="e3882-117">Anger namnet på ett Automation-konto.</span><span class="sxs-lookup"><span data-stu-id="e3882-117">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="e3882-118">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="e3882-118">-DayInterval</span></span>
<span data-ttu-id="e3882-119">Anger ett intervall, i dagar, för schemat.</span><span class="sxs-lookup"><span data-stu-id="e3882-119">Specifies an interval, in days, for the schedule.</span></span>

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

### <span data-ttu-id="e3882-120">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="e3882-120">-Description</span></span>
<span data-ttu-id="e3882-121">Anger en beskrivning.</span><span class="sxs-lookup"><span data-stu-id="e3882-121">Specifies a description.</span></span>

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

### <span data-ttu-id="e3882-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e3882-122">-ExpiryTime</span></span>
<span data-ttu-id="e3882-123">Anger förfallo tiden för ett schema.</span><span class="sxs-lookup"><span data-stu-id="e3882-123">Specifies the expiry time of a schedule.</span></span>
<span data-ttu-id="e3882-124">En sträng kan anges om den kan konverteras till en giltig **datetime**.</span><span class="sxs-lookup"><span data-stu-id="e3882-124">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3882-125">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="e3882-125">-HourInterval</span></span>
<span data-ttu-id="e3882-126">Anger ett intervall, i timmar, för schemat.</span><span class="sxs-lookup"><span data-stu-id="e3882-126">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="e3882-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="e3882-127">-Name</span></span>
<span data-ttu-id="e3882-128">Anger ett namn för schemat.</span><span class="sxs-lookup"><span data-stu-id="e3882-128">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="e3882-129">-OneTime</span><span class="sxs-lookup"><span data-stu-id="e3882-129">-OneTime</span></span>
<span data-ttu-id="e3882-130">Visar att den här åtgärden skapar ett engångs schema.</span><span class="sxs-lookup"><span data-stu-id="e3882-130">Indicates that this operation creates a one-time schedule.</span></span>

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

### <span data-ttu-id="e3882-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="e3882-131">-Profile</span></span>
<span data-ttu-id="e3882-132">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="e3882-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e3882-133">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="e3882-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3882-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e3882-134">-StartTime</span></span>
<span data-ttu-id="e3882-135">Anger start tiden för ett schema.</span><span class="sxs-lookup"><span data-stu-id="e3882-135">Specifies the start time of a schedule.</span></span>
<span data-ttu-id="e3882-136">En sträng kan anges om den kan konverteras till en giltig **datetime**.</span><span class="sxs-lookup"><span data-stu-id="e3882-136">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3882-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3882-137">CommonParameters</span></span>
<span data-ttu-id="e3882-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3882-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3882-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3882-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3882-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e3882-140">INPUTS</span></span>

## <span data-ttu-id="e3882-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e3882-141">OUTPUTS</span></span>

### <span data-ttu-id="e3882-142">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="e3882-142">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="e3882-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e3882-143">NOTES</span></span>

## <span data-ttu-id="e3882-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e3882-144">RELATED LINKS</span></span>

[<span data-ttu-id="e3882-145">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e3882-145">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="e3882-146">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e3882-146">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="e3882-147">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="e3882-147">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


