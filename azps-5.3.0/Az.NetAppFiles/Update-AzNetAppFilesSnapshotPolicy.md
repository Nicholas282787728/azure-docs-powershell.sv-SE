---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: edb22cc9945ca665b2e24a4488bf3335faac4f50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422451"
---
# <span data-ttu-id="e77e8-101">Update-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e77e8-101">Update-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e77e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e77e8-102">SYNOPSIS</span></span>
<span data-ttu-id="e77e8-103">Uppdaterar en Azure NetApp (ANF) Snapshot-princip till valfri modifiering som tillhandahålls.</span><span class="sxs-lookup"><span data-stu-id="e77e8-103">Updates an Azure NetApp Files (ANF) snapshot policy to the optional modifiers provided.</span></span>

## <span data-ttu-id="e77e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e77e8-104">SYNTAX</span></span>

### <span data-ttu-id="e77e8-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e77e8-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77e8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e77e8-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled <Boolean>]
 [-HourlySchedule <PSNetAppFilesHourlySchedule>] [-DailySchedule <PSNetAppFilesDailySchedule>]
 [-WeeklySchedule <PSNetAppFilesWeeklySchedule>] [-MonthlySchedule <PSNetAppFilesMonthlySchedule>]
 [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77e8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e77e8-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e77e8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e77e8-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesSnapshotPolicy [-Enabled <Boolean>] [-HourlySchedule <PSNetAppFilesHourlySchedule>]
 [-DailySchedule <PSNetAppFilesDailySchedule>] [-WeeklySchedule <PSNetAppFilesWeeklySchedule>]
 [-MonthlySchedule <PSNetAppFilesMonthlySchedule>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesSnapshotPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e77e8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e77e8-109">DESCRIPTION</span></span>
<span data-ttu-id="e77e8-110">Cmdleten **Update-AzNetAppFilesSnapshotPolicy** ändrar en ANF-Snapshot-princip.</span><span class="sxs-lookup"><span data-stu-id="e77e8-110">The **Update-AzNetAppFilesSnapshotPolicy** cmdlet modifies an ANF snapshot policy.</span></span>

## <span data-ttu-id="e77e8-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e77e8-111">EXAMPLES</span></span>

### <span data-ttu-id="e77e8-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e77e8-112">Example 1</span></span>
```powershell
$hourlySchedule = @{
        Minute = 1
        SnapshotsToKeep = 3
    }
PS C:\> Update-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -AccountName "MyAccount" -Name "MySnapshotPolicy" -HourlySchedule $hourlySchedule
```

<span data-ttu-id="e77e8-113">Det här kommandot ändrar säkerhets kopierings princip för ANF "MySnapshotPolicy" så att angiven HourlySchedule visas.</span><span class="sxs-lookup"><span data-stu-id="e77e8-113">This command changes the ANF backup policy "MySnapshotPolicy" to have the given HourlySchedule.</span></span>

## <span data-ttu-id="e77e8-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e77e8-114">PARAMETERS</span></span>

### <span data-ttu-id="e77e8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e77e8-115">-AccountName</span></span>
<span data-ttu-id="e77e8-116">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="e77e8-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-117">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="e77e8-117">-AccountObject</span></span>
<span data-ttu-id="e77e8-118">Kontot för det nya Snapshot policy-objektet</span><span class="sxs-lookup"><span data-stu-id="e77e8-118">The Account for the new Snapshot Policy object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-119">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="e77e8-119">-DailySchedule</span></span>
<span data-ttu-id="e77e8-120">En hash-matris som representerar det dagliga schemat</span><span class="sxs-lookup"><span data-stu-id="e77e8-120">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e77e8-121">-DefaultProfile</span></span>
<span data-ttu-id="e77e8-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e77e8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e77e8-123">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="e77e8-123">-Enabled</span></span>
<span data-ttu-id="e77e8-124">Den egenskap som ska väljas är aktive rad eller inte</span><span class="sxs-lookup"><span data-stu-id="e77e8-124">The property to decide policy is enabled or not</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-125">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="e77e8-125">-HourlySchedule</span></span>
<span data-ttu-id="e77e8-126">En hash-tabell som representerar Tim schema</span><span class="sxs-lookup"><span data-stu-id="e77e8-126">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e77e8-127">-InputObject</span></span>
<span data-ttu-id="e77e8-128">Det SnapShot-objekt som ska tas bort</span><span class="sxs-lookup"><span data-stu-id="e77e8-128">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-129">-Plats</span><span class="sxs-lookup"><span data-stu-id="e77e8-129">-Location</span></span>
<span data-ttu-id="e77e8-130">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="e77e8-130">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-131">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="e77e8-131">-MonthlySchedule</span></span>
<span data-ttu-id="e77e8-132">En hash-matris som representerar det månads schemat</span><span class="sxs-lookup"><span data-stu-id="e77e8-132">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="e77e8-133">-Name</span></span>
<span data-ttu-id="e77e8-134">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="e77e8-134">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e77e8-135">-ResourceGroupName</span></span>
<span data-ttu-id="e77e8-136">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="e77e8-136">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e77e8-137">-ResourceId</span></span>
<span data-ttu-id="e77e8-138">Resurs-ID för ANF</span><span class="sxs-lookup"><span data-stu-id="e77e8-138">The resource id of the ANF Snapshot Policy</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="e77e8-139">-Tag</span></span>
<span data-ttu-id="e77e8-140">En hash-matris som representerar resursfiler</span><span class="sxs-lookup"><span data-stu-id="e77e8-140">A hashtable array which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-141">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="e77e8-141">-WeeklySchedule</span></span>
<span data-ttu-id="e77e8-142">En hash-matris som representerar det månads schemat</span><span class="sxs-lookup"><span data-stu-id="e77e8-142">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-143">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e77e8-143">-Confirm</span></span>
<span data-ttu-id="e77e8-144">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e77e8-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e77e8-145">-WhatIf</span></span>
<span data-ttu-id="e77e8-146">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e77e8-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e77e8-147">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e77e8-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e77e8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e77e8-148">CommonParameters</span></span>
<span data-ttu-id="e77e8-149">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e77e8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e77e8-150">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e77e8-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e77e8-151">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e77e8-151">INPUTS</span></span>

### <span data-ttu-id="e77e8-152">System. String</span><span class="sxs-lookup"><span data-stu-id="e77e8-152">System.String</span></span>

### <span data-ttu-id="e77e8-153">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e77e8-153">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="e77e8-154">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e77e8-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e77e8-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e77e8-155">OUTPUTS</span></span>

### <span data-ttu-id="e77e8-156">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="e77e8-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="e77e8-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e77e8-157">NOTES</span></span>

## <span data-ttu-id="e77e8-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e77e8-158">RELATED LINKS</span></span>
