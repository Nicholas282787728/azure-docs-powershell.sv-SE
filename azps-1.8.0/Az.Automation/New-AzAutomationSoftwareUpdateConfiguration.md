---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 1e5c30f1e4ca1fef4aa78b2e4b6394068878b1c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754790"
---
# <span data-ttu-id="a9889-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9889-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="a9889-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9889-102">SYNOPSIS</span></span>
<span data-ttu-id="a9889-103">Skapar en schemalagd konfiguration för Azure Automation-programuppdatering.</span><span class="sxs-lookup"><span data-stu-id="a9889-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="a9889-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9889-104">SYNTAX</span></span>

### <span data-ttu-id="a9889-105">Windows (standard)</span><span class="sxs-lookup"><span data-stu-id="a9889-105">Windows (Default)</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedUpdateClassification <WindowsUpdateClasses[]>]
 [-ExcludedKbNumber <String[]>] [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9889-106">Linux</span><span class="sxs-lookup"><span data-stu-id="a9889-106">Linux</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9889-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9889-107">DESCRIPTION</span></span>
<span data-ttu-id="a9889-108">Skapar en konfiguration för program uppdatering som körs enligt ett schema för att uppdatera en lista med datorer.</span><span class="sxs-lookup"><span data-stu-id="a9889-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="a9889-109">Datorer inkluderar både virtuella Azure-datorer eller datorer som inte AZ.</span><span class="sxs-lookup"><span data-stu-id="a9889-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="a9889-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9889-110">EXAMPLES</span></span>

### <span data-ttu-id="a9889-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a9889-111">Example 1</span></span>
<span data-ttu-id="a9889-112">Skapar en konfiguration för program uppdatering för att installera viktiga uppdateringar på två Windows Azure-datorer en gång per lördag 9PM.</span><span class="sxs-lookup"><span data-stu-id="a9889-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="a9889-113">Uppdaterings längd är inställd på två timmar i det här exemplet.</span><span class="sxs-lookup"><span data-stu-id="a9889-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzVMResourceId $targetMachines `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :
```

## <span data-ttu-id="a9889-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9889-114">PARAMETERS</span></span>

### <span data-ttu-id="a9889-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9889-115">-AutomationAccountName</span></span>
<span data-ttu-id="a9889-116">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="a9889-116">The automation account name.</span></span>

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

### <span data-ttu-id="a9889-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="a9889-117">-AzureQuery</span></span>
<span data-ttu-id="a9889-118">Dynamisk grupp med Azure-frågor.</span><span class="sxs-lookup"><span data-stu-id="a9889-118">Dynamic group azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="a9889-119">-AzureVMResourceId</span></span>
<span data-ttu-id="a9889-120">Resurs-ID för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="a9889-120">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9889-121">-DefaultProfile</span></span>
<span data-ttu-id="a9889-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9889-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-123">-Varaktighet</span><span class="sxs-lookup"><span data-stu-id="a9889-123">-Duration</span></span>
<span data-ttu-id="a9889-124">Maximal längd för uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="a9889-124">Maximum duration for the update.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="a9889-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="a9889-126">KB-nummer för undantagna uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="a9889-126">KB numbers of excluded updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="a9889-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="a9889-128">Uteslutna Linux-paket.</span><span class="sxs-lookup"><span data-stu-id="a9889-128">Excluded Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="a9889-129">-IncludedKbNumber</span></span>
<span data-ttu-id="a9889-130">KB-nummer för inkluderade uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="a9889-130">KB numbers of included updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="a9889-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="a9889-132">Inkluderade Linux-paketets klassificeringar.</span><span class="sxs-lookup"><span data-stu-id="a9889-132">Included Linux package classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]
Parameter Sets: Linux
Aliases:
Accepted values: Unclassified, Critical, Security, Other

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="a9889-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="a9889-134">Inkluderade Linux-paket masker.</span><span class="sxs-lookup"><span data-stu-id="a9889-134">Included Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="a9889-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="a9889-136">Ingår i Windows Update.</span><span class="sxs-lookup"><span data-stu-id="a9889-136">Included Windows Update classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]
Parameter Sets: Windows
Aliases:
Accepted values: Unclassified, Critical, Security, UpdateRollup, FeaturePack, ServicePack, Definition, Tools, Updates

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="a9889-137">-Linux</span></span>
<span data-ttu-id="a9889-138">Anger att program uppdateringens konfiguration riktar sig till Linux-operativsystemens datorer.</span><span class="sxs-lookup"><span data-stu-id="a9889-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="a9889-139">-NonAzureComputer</span></span>
<span data-ttu-id="a9889-140">Dator namn som inte AZS.</span><span class="sxs-lookup"><span data-stu-id="a9889-140">Non-Az computer names.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="a9889-141">-NonAzureQuery</span></span>
<span data-ttu-id="a9889-142">Dynamisk grupp icke-Azure-fråga.</span><span class="sxs-lookup"><span data-stu-id="a9889-142">Dynamic group non Azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.NonAzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="a9889-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="a9889-144">Publicera uppgift.</span><span class="sxs-lookup"><span data-stu-id="a9889-144">Post task.</span></span>

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

### <span data-ttu-id="a9889-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="a9889-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="a9889-146">Posta aktivitets parameter.</span><span class="sxs-lookup"><span data-stu-id="a9889-146">Post task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="a9889-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="a9889-148">För aktivitet.</span><span class="sxs-lookup"><span data-stu-id="a9889-148">Pre task.</span></span>

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

### <span data-ttu-id="a9889-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="a9889-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="a9889-150">För aktivitets parameter.</span><span class="sxs-lookup"><span data-stu-id="a9889-150">Pre task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="a9889-151">-RebootOnly</span></span>
<span data-ttu-id="a9889-152">Anger att program uppdaterings konfigurationen bara startar om datorerna.</span><span class="sxs-lookup"><span data-stu-id="a9889-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="a9889-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="a9889-153">-RebootSetting</span></span>
<span data-ttu-id="a9889-154">Starta om seeting.</span><span class="sxs-lookup"><span data-stu-id="a9889-154">Reboot Seeting.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.RebootSetting
Parameter Sets: (All)
Aliases:
Accepted values: IfRequired, Never, Always, RebootOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9889-155">-ResourceGroupName</span></span>
<span data-ttu-id="a9889-156">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a9889-156">The resource group name.</span></span>

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

### <span data-ttu-id="a9889-157">– Schema</span><span class="sxs-lookup"><span data-stu-id="a9889-157">-Schedule</span></span>
<span data-ttu-id="a9889-158">Schemalägg objekt som används för konfiguration av program uppdatering.</span><span class="sxs-lookup"><span data-stu-id="a9889-158">Schedule object used for software update configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="a9889-159">-Windows</span></span>
<span data-ttu-id="a9889-160">Anger att konfiguration av Windows operativ system för program uppdatering är riktad.</span><span class="sxs-lookup"><span data-stu-id="a9889-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-161">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9889-161">-Confirm</span></span>
<span data-ttu-id="a9889-162">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9889-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9889-163">-WhatIf</span></span>
<span data-ttu-id="a9889-164">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9889-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9889-165">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9889-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9889-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9889-166">CommonParameters</span></span>
<span data-ttu-id="a9889-167">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9889-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9889-168">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9889-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9889-169">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9889-169">INPUTS</span></span>

### <span data-ttu-id="a9889-170">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="a9889-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="a9889-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a9889-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a9889-172">System. string []</span><span class="sxs-lookup"><span data-stu-id="a9889-172">System.String[]</span></span>

### <span data-ttu-id="a9889-173">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="a9889-173">System.TimeSpan</span></span>

### <span data-ttu-id="a9889-174">Microsoft. Azure. commands. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="a9889-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="a9889-175">Microsoft. Azure. commands. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="a9889-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="a9889-176">System. String</span><span class="sxs-lookup"><span data-stu-id="a9889-176">System.String</span></span>

## <span data-ttu-id="a9889-177">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9889-177">OUTPUTS</span></span>

### <span data-ttu-id="a9889-178">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="a9889-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="a9889-179">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9889-179">NOTES</span></span>

## <span data-ttu-id="a9889-180">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9889-180">RELATED LINKS</span></span>