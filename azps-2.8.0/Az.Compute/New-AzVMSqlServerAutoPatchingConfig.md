---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 302197adbbf6e90397a5bb6f3e96be6d6836b1bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745078"
---
# <span data-ttu-id="8de5c-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="8de5c-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="8de5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8de5c-102">SYNOPSIS</span></span>
<span data-ttu-id="8de5c-103">Skapar ett konfigurations objekt för automatisk korrigering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8de5c-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="8de5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8de5c-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [<CommonParameters>]
```

## <span data-ttu-id="8de5c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8de5c-105">DESCRIPTION</span></span>
<span data-ttu-id="8de5c-106">Cmdleten **New-AzVMSqlServerAutoPatchingConfig** skapar ett konfigurations objekt för automatisk korrigering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="8de5c-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="8de5c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8de5c-107">EXAMPLES</span></span>

### <span data-ttu-id="8de5c-108">Exempel 1: skapa ett konfigurations objekt för att konfigurera automatisk korrigering</span><span class="sxs-lookup"><span data-stu-id="8de5c-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="8de5c-109">Det här kommandot skapar konfigurations objekt för korrigering.</span><span class="sxs-lookup"><span data-stu-id="8de5c-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="8de5c-110">Kommandot anger vecko dagen och fönstret underhåll.</span><span class="sxs-lookup"><span data-stu-id="8de5c-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="8de5c-111">Denna konfiguration möjliggör en korrigering som använder dessa värden.</span><span class="sxs-lookup"><span data-stu-id="8de5c-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="8de5c-112">Resultatet sparas i $AutoBackupConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="8de5c-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="8de5c-113">Du kan ange det här konfigurationsobjektet för andra cmdlets, till exempel Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8de5c-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="8de5c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8de5c-114">PARAMETERS</span></span>

### <span data-ttu-id="8de5c-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="8de5c-115">-DayOfWeek</span></span>
<span data-ttu-id="8de5c-116">Anger den dag i veckan då uppdateringar ska installeras.</span><span class="sxs-lookup"><span data-stu-id="8de5c-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="8de5c-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="8de5c-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8de5c-118">Lördag</span><span class="sxs-lookup"><span data-stu-id="8de5c-118">Sunday</span></span>
- <span data-ttu-id="8de5c-119">Dagarna</span><span class="sxs-lookup"><span data-stu-id="8de5c-119">Monday</span></span>
- <span data-ttu-id="8de5c-120">Torsdag</span><span class="sxs-lookup"><span data-stu-id="8de5c-120">Tuesday</span></span>
- <span data-ttu-id="8de5c-121">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="8de5c-121">Wednesday</span></span>
- <span data-ttu-id="8de5c-122">Torsdag</span><span class="sxs-lookup"><span data-stu-id="8de5c-122">Thursday</span></span>
- <span data-ttu-id="8de5c-123">Fredag</span><span class="sxs-lookup"><span data-stu-id="8de5c-123">Friday</span></span>
- <span data-ttu-id="8de5c-124">Afton</span><span class="sxs-lookup"><span data-stu-id="8de5c-124">Saturday</span></span>
- <span data-ttu-id="8de5c-125">Vardaglig</span><span class="sxs-lookup"><span data-stu-id="8de5c-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de5c-126">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="8de5c-126">-Enable</span></span>
<span data-ttu-id="8de5c-127">Anger att automatisk korrigering för den virtuella datorn är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="8de5c-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="8de5c-128">Om du aktiverar automatisk korrigering av cmdleten placeras Windows Update i interaktivt läge.</span><span class="sxs-lookup"><span data-stu-id="8de5c-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="8de5c-129">Om du inaktiverar automatisk uppdatering ändras inte Windows Update-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="8de5c-129">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de5c-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="8de5c-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="8de5c-131">Anger längden i minuter för underhålls fönstret.</span><span class="sxs-lookup"><span data-stu-id="8de5c-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="8de5c-132">Automatisk korrigering undvikr att utföra en åtgärd som kan påverka en virtuell dator tillgänglighet utanför det fönstret.</span><span class="sxs-lookup"><span data-stu-id="8de5c-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="8de5c-133">Ange en multipel av 30 minuter.</span><span class="sxs-lookup"><span data-stu-id="8de5c-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de5c-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="8de5c-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="8de5c-135">Anger den timme i dag då underhålls fönstret startar.</span><span class="sxs-lookup"><span data-stu-id="8de5c-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="8de5c-136">Den här tiden anger när uppdateringar börjar installera.</span><span class="sxs-lookup"><span data-stu-id="8de5c-136">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de5c-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="8de5c-137">-PatchCategory</span></span>
<span data-ttu-id="8de5c-138">Anger om viktiga uppdateringar ska ingå.</span><span class="sxs-lookup"><span data-stu-id="8de5c-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de5c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de5c-139">CommonParameters</span></span>
<span data-ttu-id="8de5c-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de5c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de5c-141">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8de5c-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de5c-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8de5c-142">INPUTS</span></span>

### <span data-ttu-id="8de5c-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="8de5c-143">None</span></span>

## <span data-ttu-id="8de5c-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8de5c-144">OUTPUTS</span></span>

### <span data-ttu-id="8de5c-145">Microsoft. Azure. commands. Compute. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="8de5c-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="8de5c-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8de5c-146">NOTES</span></span>

## <span data-ttu-id="8de5c-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8de5c-147">RELATED LINKS</span></span>

[<span data-ttu-id="8de5c-148">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="8de5c-148">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="8de5c-149">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8de5c-149">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)

