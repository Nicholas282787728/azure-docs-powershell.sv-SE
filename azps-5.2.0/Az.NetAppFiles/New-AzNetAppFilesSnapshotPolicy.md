---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshotpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshotPolicy.md
ms.openlocfilehash: cfa7fc38fa8c7b66347ae3632b6d1ea94ca07c86
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410723"
---
# <span data-ttu-id="a5a6d-101">New-AzNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="a5a6d-101">New-AzNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="a5a6d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a5a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a6d-103">Skapar en ny Azure NetApp-fil (ANF) för ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-103">Creates a new Azure NetApp Files (ANF) snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="a5a6d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a5a6d-104">SYNTAX</span></span>

### <span data-ttu-id="a5a6d-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a5a6d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshotPolicy -ResourceGroupName <String> -Location <String> -AccountName <String>
 -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a6d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5a6d-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshotPolicy -Name <String> [-Enabled] -HourlySchedule <PSNetAppFilesHourlySchedule>
 -DailySchedule <PSNetAppFilesDailySchedule> -WeeklySchedule <PSNetAppFilesWeeklySchedule>
 -MonthlySchedule <PSNetAppFilesMonthlySchedule> [-Tag <Hashtable>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a6d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a5a6d-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a6d-108">Cmdleten **New-AzNetAppFilesActiveDirectory** skapar en ny ögonblicks bild princip för ett ANF-konto.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-108">The **New-AzNetAppFilesActiveDirectory** cmdlet creates a new snapshot policy for an ANF account.</span></span>

## <span data-ttu-id="a5a6d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a5a6d-109">EXAMPLES</span></span>

### <span data-ttu-id="a5a6d-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a5a6d-110">Example 1</span></span>
```powershell
$hourlySchedule = @{        
        Minute = 2
        SnapshotsToKeep = 6
    }
    $dailySchedule = @{
        Hour = 1
        Minute = 2
        SnapshotsToKeep = 6
    }
    $weeklySchedule = @{
        Minute = 2    
        Hour = 1                
        Day = "Sunday,Monday"
        SnapshotsToKeep = 6
    }
    $monthlySchedule = @{
        Minute = 2    
        Hour = 1        
        DaysOfMonth = "2,11,21"
        SnapshotsToKeep = 6
    }
PS C:\> New-AzNetAppFilesSnapshotPolicy -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -Name "MySnapshotPolicy" -Enabled -HourlySchedule $hourlySchedule -DailySchedule $dailySchedule -WeeklySchedule $weeklySchedule -MonthlySchedule $monthlySchedule
```

<span data-ttu-id="a5a6d-111">Det här kommandot skapar den nya ANF Snapshot-principen för ANF-kontot "konto".</span><span class="sxs-lookup"><span data-stu-id="a5a6d-111">This command creates the new ANF snapshot policy for ANF account named account "MyAccount".</span></span>

## <span data-ttu-id="a5a6d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a5a6d-112">PARAMETERS</span></span>

### <span data-ttu-id="a5a6d-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a5a6d-113">-AccountName</span></span>
<span data-ttu-id="a5a6d-114">Namnet på ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="a5a6d-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="a5a6d-115">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="a5a6d-115">-AccountObject</span></span>
<span data-ttu-id="a5a6d-116">Kontot för det nya Snapshot policy-objektet</span><span class="sxs-lookup"><span data-stu-id="a5a6d-116">The Account for the new Snapshot Policy object</span></span>

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

### <span data-ttu-id="a5a6d-117">-DailySchedule</span><span class="sxs-lookup"><span data-stu-id="a5a6d-117">-DailySchedule</span></span>
<span data-ttu-id="a5a6d-118">En hash-matris som representerar det dagliga schemat</span><span class="sxs-lookup"><span data-stu-id="a5a6d-118">A hashtable array which represents the daily Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesDailySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a6d-119">-DefaultProfile</span></span>
<span data-ttu-id="a5a6d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5a6d-121">-Aktiverad</span><span class="sxs-lookup"><span data-stu-id="a5a6d-121">-Enabled</span></span>
<span data-ttu-id="a5a6d-122">Den egenskap som ska väljas är aktive rad eller inte</span><span class="sxs-lookup"><span data-stu-id="a5a6d-122">The property to decide policy is enabled or not</span></span>

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

### <span data-ttu-id="a5a6d-123">-HourlySchedule</span><span class="sxs-lookup"><span data-stu-id="a5a6d-123">-HourlySchedule</span></span>
<span data-ttu-id="a5a6d-124">En hash-tabell som representerar Tim schema</span><span class="sxs-lookup"><span data-stu-id="a5a6d-124">A hashtable array which represents the hourly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesHourlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6d-125">-Plats</span><span class="sxs-lookup"><span data-stu-id="a5a6d-125">-Location</span></span>
<span data-ttu-id="a5a6d-126">Resursens plats</span><span class="sxs-lookup"><span data-stu-id="a5a6d-126">The location of the resource</span></span>

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

### <span data-ttu-id="a5a6d-127">-MonthlySchedule</span><span class="sxs-lookup"><span data-stu-id="a5a6d-127">-MonthlySchedule</span></span>
<span data-ttu-id="a5a6d-128">En hash-matris som representerar det månads schemat</span><span class="sxs-lookup"><span data-stu-id="a5a6d-128">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesMonthlySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6d-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="a5a6d-129">-Name</span></span>
<span data-ttu-id="a5a6d-130">Namnet på ANF</span><span class="sxs-lookup"><span data-stu-id="a5a6d-130">The name of the ANF snapshot policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a6d-131">-ResourceGroupName</span></span>
<span data-ttu-id="a5a6d-132">Resurs gruppen för ANF-kontot</span><span class="sxs-lookup"><span data-stu-id="a5a6d-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a5a6d-133">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a5a6d-133">-Tag</span></span>
<span data-ttu-id="a5a6d-134">En hash-matris som representerar resursfiler</span><span class="sxs-lookup"><span data-stu-id="a5a6d-134">A hashtable array which represents resource tags</span></span>

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

### <span data-ttu-id="a5a6d-135">-WeeklySchedule</span><span class="sxs-lookup"><span data-stu-id="a5a6d-135">-WeeklySchedule</span></span>
<span data-ttu-id="a5a6d-136">En hash-matris som representerar det månads schemat</span><span class="sxs-lookup"><span data-stu-id="a5a6d-136">A hashtable array which represents the montly Schedule</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesWeeklySchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6d-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a5a6d-137">-Confirm</span></span>
<span data-ttu-id="a5a6d-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a6d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a6d-139">-WhatIf</span></span>
<span data-ttu-id="a5a6d-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a6d-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a6d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a6d-142">CommonParameters</span></span>
<span data-ttu-id="a5a6d-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a6d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a6d-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5a6d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a6d-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a5a6d-145">INPUTS</span></span>

### <span data-ttu-id="a5a6d-146">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a5a6d-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a5a6d-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a5a6d-147">OUTPUTS</span></span>

### <span data-ttu-id="a5a6d-148">Microsoft. Azure. commands. NetAppFiles. Models. PSNetAppFilesSnapshotPolicy</span><span class="sxs-lookup"><span data-stu-id="a5a6d-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshotPolicy</span></span>

## <span data-ttu-id="a5a6d-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a5a6d-149">NOTES</span></span>

## <span data-ttu-id="a5a6d-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a5a6d-150">RELATED LINKS</span></span>
