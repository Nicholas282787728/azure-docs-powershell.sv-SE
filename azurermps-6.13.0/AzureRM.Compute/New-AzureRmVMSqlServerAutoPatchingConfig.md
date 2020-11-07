---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: d6814131ec4748f95f572762938d3c8bd5135c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756228"
---
# <span data-ttu-id="e0e5f-101">New-AzureRmVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="e0e5f-101">New-AzureRmVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="e0e5f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e0e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="e0e5f-103">Skapar ett konfigurations objekt för automatisk korrigering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0e5f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e0e5f-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0e5f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e0e5f-105">DESCRIPTION</span></span>
<span data-ttu-id="e0e5f-106">Cmdleten **New-AzureRmVMSqlServerAutoPatchingConfig** skapar ett konfigurations objekt för automatisk korrigering på en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-106">The **New-AzureRmVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="e0e5f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e0e5f-107">EXAMPLES</span></span>

### <span data-ttu-id="e0e5f-108">Exempel 1: skapa ett konfigurations objekt för att konfigurera automatisk korrigering</span><span class="sxs-lookup"><span data-stu-id="e0e5f-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureRmVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="e0e5f-109">Det här kommandot skapar konfigurations objekt för korrigering.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="e0e5f-110">Kommandot anger vecko dagen och fönstret underhåll.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="e0e5f-111">Denna konfiguration möjliggör en korrigering som använder dessa värden.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="e0e5f-112">Resultatet sparas i $AutoBackupConfig variabel.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="e0e5f-113">Du kan ange det här konfigurationsobjektet för andra cmdlets, till exempel Set-AzureRmVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="e0e5f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e0e5f-114">PARAMETERS</span></span>

### <span data-ttu-id="e0e5f-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="e0e5f-115">-DayOfWeek</span></span>
<span data-ttu-id="e0e5f-116">Anger den dag i veckan då uppdateringar ska installeras.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="e0e5f-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e0e5f-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e0e5f-118">Lördag</span><span class="sxs-lookup"><span data-stu-id="e0e5f-118">Sunday</span></span>
- <span data-ttu-id="e0e5f-119">Dagarna</span><span class="sxs-lookup"><span data-stu-id="e0e5f-119">Monday</span></span>
- <span data-ttu-id="e0e5f-120">Torsdag</span><span class="sxs-lookup"><span data-stu-id="e0e5f-120">Tuesday</span></span>
- <span data-ttu-id="e0e5f-121">Onsdagen</span><span class="sxs-lookup"><span data-stu-id="e0e5f-121">Wednesday</span></span>
- <span data-ttu-id="e0e5f-122">Torsdag</span><span class="sxs-lookup"><span data-stu-id="e0e5f-122">Thursday</span></span>
- <span data-ttu-id="e0e5f-123">Fredag</span><span class="sxs-lookup"><span data-stu-id="e0e5f-123">Friday</span></span>
- <span data-ttu-id="e0e5f-124">Afton</span><span class="sxs-lookup"><span data-stu-id="e0e5f-124">Saturday</span></span>
- <span data-ttu-id="e0e5f-125">Vardaglig</span><span class="sxs-lookup"><span data-stu-id="e0e5f-125">Everyday</span></span>

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

### <span data-ttu-id="e0e5f-126">-Aktivera</span><span class="sxs-lookup"><span data-stu-id="e0e5f-126">-Enable</span></span>
<span data-ttu-id="e0e5f-127">Anger att automatisk korrigering för den virtuella datorn är aktive rad.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="e0e5f-128">Om du aktiverar automatisk korrigering av cmdleten placeras Windows Update i interaktivt läge.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="e0e5f-129">Om du inaktiverar automatisk uppdatering ändras inte Windows Update-inställningarna.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="e0e5f-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="e0e5f-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="e0e5f-131">Anger längden i minuter för underhålls fönstret.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="e0e5f-132">Automatisk korrigering undvikr att utföra en åtgärd som kan påverka en virtuell dator tillgänglighet utanför det fönstret.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="e0e5f-133">Ange en multipel av 30 minuter.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="e0e5f-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="e0e5f-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="e0e5f-135">Anger den timme i dag då underhålls fönstret startar.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="e0e5f-136">Den här tiden anger när uppdateringar börjar installera.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="e0e5f-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="e0e5f-137">-PatchCategory</span></span>
<span data-ttu-id="e0e5f-138">Anger om viktiga uppdateringar ska ingå.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="e0e5f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0e5f-139">CommonParameters</span></span>
<span data-ttu-id="e0e5f-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0e5f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0e5f-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0e5f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0e5f-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e0e5f-142">INPUTS</span></span>

### <span data-ttu-id="e0e5f-143">Ingen</span><span class="sxs-lookup"><span data-stu-id="e0e5f-143">None</span></span>

## <span data-ttu-id="e0e5f-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e0e5f-144">OUTPUTS</span></span>

### <span data-ttu-id="e0e5f-145">Microsoft. Azure. commands. Compute. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="e0e5f-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="e0e5f-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e0e5f-146">NOTES</span></span>

## <span data-ttu-id="e0e5f-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e0e5f-147">RELATED LINKS</span></span>

[<span data-ttu-id="e0e5f-148">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="e0e5f-148">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="e0e5f-149">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e0e5f-149">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)

