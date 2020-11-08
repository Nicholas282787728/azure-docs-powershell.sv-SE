---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7317DAC1-B535-4650-86BF-73E96F61EECD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23bb8e09fac8ec4fe0e8ff5b3c23ab995f03694c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099421"
---
# <span data-ttu-id="36581-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="36581-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="36581-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="36581-102">SYNOPSIS</span></span>
<span data-ttu-id="36581-103">Skapar ett konfigurations objekt för automatisk korrigering av virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="36581-103">Creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="36581-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="36581-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="36581-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="36581-105">DESCRIPTION</span></span>
<span data-ttu-id="36581-106">Cmdleten **New-AzureVMSqlServerAutoPatchingConfig** skapar ett konfigurations objekt för automatisk korrigering av virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="36581-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for virtual machine automatic patching.</span></span>

## <span data-ttu-id="36581-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="36581-107">EXAMPLES</span></span>

### <span data-ttu-id="36581-108">Exempel 1: skapa ett konfigurations objekt för att konfigurera automatisk korrigering</span><span class="sxs-lookup"><span data-stu-id="36581-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $APS = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
          Enable                        : True
          DayOfWeek                     : Thursday
          MaintenanceWindowStartingHour : 11
          MaintenanceWindowDuration     : 120
          PatchCategory                 : Important
```

<span data-ttu-id="36581-109">Det här kommandot skapar ett konfigurations objekt som kan användas för att konfigurera automatisk uppdatering med set-AzureVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="36581-109">This command creates configuration object that can be used to configure automatic patching using Set-AzureVMSqlServerExtension.</span></span>

## <span data-ttu-id="36581-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="36581-110">PARAMETERS</span></span>

### <span data-ttu-id="36581-111">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="36581-111">-DayOfWeek</span></span>
<span data-ttu-id="36581-112">Anger den dag i veckan då uppdateringar ska installeras.</span><span class="sxs-lookup"><span data-stu-id="36581-112">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="36581-113">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="36581-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36581-114">Lördag</span><span class="sxs-lookup"><span data-stu-id="36581-114">Sunday</span></span>
- <span data-ttu-id="36581-115">Dagarna</span><span class="sxs-lookup"><span data-stu-id="36581-115">Monday</span></span>
- <span data-ttu-id="36581-116">Torsdag</span><span class="sxs-lookup"><span data-stu-id="36581-116">Tuesday</span></span>
- <span data-ttu-id="36581-117">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="36581-117">Wednesday</span></span>
- <span data-ttu-id="36581-118">Torsdag</span><span class="sxs-lookup"><span data-stu-id="36581-118">Thursday</span></span>
- <span data-ttu-id="36581-119">Fredag</span><span class="sxs-lookup"><span data-stu-id="36581-119">Friday</span></span>
- <span data-ttu-id="36581-120">Afton</span><span class="sxs-lookup"><span data-stu-id="36581-120">Saturday</span></span>
- <span data-ttu-id="36581-121">Vardaglig</span><span class="sxs-lookup"><span data-stu-id="36581-121">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36581-122">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="36581-122">-Enable</span></span>
<span data-ttu-id="36581-123">Anger att automatisk korrigering för den virtuella datorn är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="36581-123">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="36581-124">Om du aktiverar automatisk korrigering av cmdleten kommer Windows Update till interaktivt läge.</span><span class="sxs-lookup"><span data-stu-id="36581-124">If you enable automated patching the cmdlet will put Windows Update into interactive mode.</span></span>
<span data-ttu-id="36581-125">Om du inaktiverar automatisk uppdatering ändras inte Windows Update-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="36581-125">If you disable automated patching, Windows Update settings will not change.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36581-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="36581-126">-InformationAction</span></span>
<span data-ttu-id="36581-127">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="36581-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="36581-128">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="36581-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="36581-129">Vidare</span><span class="sxs-lookup"><span data-stu-id="36581-129">Continue</span></span>
- <span data-ttu-id="36581-130">Över</span><span class="sxs-lookup"><span data-stu-id="36581-130">Ignore</span></span>
- <span data-ttu-id="36581-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="36581-131">Inquire</span></span>
- <span data-ttu-id="36581-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="36581-132">SilentlyContinue</span></span>
- <span data-ttu-id="36581-133">Stanna</span><span class="sxs-lookup"><span data-stu-id="36581-133">Stop</span></span>
- <span data-ttu-id="36581-134">Avbryt</span><span class="sxs-lookup"><span data-stu-id="36581-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36581-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="36581-135">-InformationVariable</span></span>
<span data-ttu-id="36581-136">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="36581-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36581-137">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="36581-137">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="36581-138">Anger underhålls fönstrets längd.</span><span class="sxs-lookup"><span data-stu-id="36581-138">Specifies the duration of the maintenance window.</span></span>
<span data-ttu-id="36581-139">Automatisk korrigering gör att det inte går att utföra en åtgärd som kan påverka en virtuell dators tillgänglighet utanför det fönstret.</span><span class="sxs-lookup"><span data-stu-id="36581-139">Automated patching will avoid performing an action that can impact a virtual machine availability outside of that window.</span></span>
<span data-ttu-id="36581-140">Endast 30 minuters ökningar är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="36581-140">Only 30 minutes increments are allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36581-141">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="36581-141">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="36581-142">Anger den timme i dag då underhålls fönstret startar.</span><span class="sxs-lookup"><span data-stu-id="36581-142">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="36581-143">Den här tiden anger när uppdateringar börjar installeras och avrundas till timmen.</span><span class="sxs-lookup"><span data-stu-id="36581-143">This time defines when updates start installing and is rounded to the hour.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36581-144">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="36581-144">-PatchCategory</span></span>
<span data-ttu-id="36581-145">Anger om viktiga uppdateringar ska ingå.</span><span class="sxs-lookup"><span data-stu-id="36581-145">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36581-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36581-146">CommonParameters</span></span>
<span data-ttu-id="36581-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36581-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36581-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36581-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36581-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="36581-149">INPUTS</span></span>

## <span data-ttu-id="36581-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="36581-150">OUTPUTS</span></span>

### <span data-ttu-id="36581-151">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="36581-151">AutoPatchingSettings</span></span>
<span data-ttu-id="36581-152">Den här cmdleten returnerar objekt som innehåller inställningar för automatisk korrigering.</span><span class="sxs-lookup"><span data-stu-id="36581-152">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="36581-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="36581-153">NOTES</span></span>

## <span data-ttu-id="36581-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="36581-154">RELATED LINKS</span></span>

[<span data-ttu-id="36581-155">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="36581-155">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)

[<span data-ttu-id="36581-156">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="36581-156">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="36581-157">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="36581-157">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)


