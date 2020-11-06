---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f66d22e8ca07812ab76c482c29018f2a639d84f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579079"
---
# <span data-ttu-id="b3864-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3864-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="b3864-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b3864-102">SYNOPSIS</span></span>
<span data-ttu-id="b3864-103">Skapar en schemalagd konfiguration för Azure Automation-programuppdatering.</span><span class="sxs-lookup"><span data-stu-id="b3864-103">Creates a scheduled azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3864-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b3864-104">SYNTAX</span></span>

### <span data-ttu-id="b3864-105">Windows (standard)</span><span class="sxs-lookup"><span data-stu-id="b3864-105">Windows (Default)</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows]
 [-AzureVMResourceId <String[]>] [-NonAzureComputer <String[]>] [-Duration <TimeSpan>]
 [-IncludedUpdateClassification <WindowsUpdateClasses[]>] [-ExcludedKbNumber <String[]>]
 [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3864-106">Linux</span><span class="sxs-lookup"><span data-stu-id="b3864-106">Linux</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-AzureVMResourceId <String[]>]
 [-NonAzureComputer <String[]>] [-Duration <TimeSpan>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3864-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b3864-107">DESCRIPTION</span></span>
<span data-ttu-id="b3864-108">Skapar en konfiguration för program uppdatering som körs enligt ett schema för att uppdatera en lista med datorer.</span><span class="sxs-lookup"><span data-stu-id="b3864-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="b3864-109">Datorer inkluderar både virtuella Azure-datorer eller icke-Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="b3864-109">Computers include both azure virtual machines or non-azure computers.</span></span>

## <span data-ttu-id="b3864-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b3864-110">EXAMPLES</span></span>

### <span data-ttu-id="b3864-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b3864-111">Example 1</span></span>
<span data-ttu-id="b3864-112">Skapar en konfiguration för program uppdatering för att installera viktiga uppdateringar på två Windows Azure-datorer en gång per lördag 9PM.</span><span class="sxs-lookup"><span data-stu-id="b3864-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="b3864-113">Uppdaterings längd är inställd på två timmar i det här exemplet.</span><span class="sxs-lookup"><span data-stu-id="b3864-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzureRmAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceIds $targetMachines `
                                                 -IncludedUpdateClassifications Critical `
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

## <span data-ttu-id="b3864-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b3864-114">PARAMETERS</span></span>

### <span data-ttu-id="b3864-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b3864-115">-AutomationAccountName</span></span>
<span data-ttu-id="b3864-116">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="b3864-116">The automation account name.</span></span>

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

### <span data-ttu-id="b3864-117">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="b3864-117">-AzureVMResourceId</span></span>
<span data-ttu-id="b3864-118">Resurs-ID för virtuella Azure-datorer.</span><span class="sxs-lookup"><span data-stu-id="b3864-118">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="b3864-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3864-119">-DefaultProfile</span></span>
<span data-ttu-id="b3864-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b3864-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3864-121">-Varaktighet</span><span class="sxs-lookup"><span data-stu-id="b3864-121">-Duration</span></span>
<span data-ttu-id="b3864-122">Maximal längd för uppdateringen.</span><span class="sxs-lookup"><span data-stu-id="b3864-122">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="b3864-123">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="b3864-123">-ExcludedKbNumber</span></span>
<span data-ttu-id="b3864-124">KB-nummer för undantagna uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="b3864-124">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="b3864-125">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="b3864-125">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="b3864-126">Uteslutna Linux-paket.</span><span class="sxs-lookup"><span data-stu-id="b3864-126">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="b3864-127">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="b3864-127">-IncludedKbNumber</span></span>
<span data-ttu-id="b3864-128">KB-nummer för inkluderade uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="b3864-128">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="b3864-129">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="b3864-129">-IncludedPackageClassification</span></span>
<span data-ttu-id="b3864-130">Inkluderade Linux-paketets klassificeringar.</span><span class="sxs-lookup"><span data-stu-id="b3864-130">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="b3864-131">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="b3864-131">-IncludedPackageNameMask</span></span>
<span data-ttu-id="b3864-132">Inkluderade Linux-paket masker.</span><span class="sxs-lookup"><span data-stu-id="b3864-132">Included Linux package masks.</span></span>

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

### <span data-ttu-id="b3864-133">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="b3864-133">-IncludedUpdateClassification</span></span>
<span data-ttu-id="b3864-134">Ingår i Windows Update.</span><span class="sxs-lookup"><span data-stu-id="b3864-134">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="b3864-135">-Linux</span><span class="sxs-lookup"><span data-stu-id="b3864-135">-Linux</span></span>
<span data-ttu-id="b3864-136">Anger att program uppdateringens konfiguration riktar sig till Linux-operativsystemens datorer.</span><span class="sxs-lookup"><span data-stu-id="b3864-136">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="b3864-137">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="b3864-137">-NonAzureComputer</span></span>
<span data-ttu-id="b3864-138">Icke-Azure dator namn.</span><span class="sxs-lookup"><span data-stu-id="b3864-138">Non-Azure computer names.</span></span>

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

### <span data-ttu-id="b3864-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3864-139">-ResourceGroupName</span></span>
<span data-ttu-id="b3864-140">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b3864-140">The resource group name.</span></span>

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

### <span data-ttu-id="b3864-141">– Schema</span><span class="sxs-lookup"><span data-stu-id="b3864-141">-Schedule</span></span>
<span data-ttu-id="b3864-142">Schemalägg objekt som används för konfiguration av program uppdatering.</span><span class="sxs-lookup"><span data-stu-id="b3864-142">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="b3864-143">-Windows</span><span class="sxs-lookup"><span data-stu-id="b3864-143">-Windows</span></span>
<span data-ttu-id="b3864-144">Anger att konfiguration av Windows operativ system för program uppdatering är riktad.</span><span class="sxs-lookup"><span data-stu-id="b3864-144">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="b3864-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b3864-145">-Confirm</span></span>
<span data-ttu-id="b3864-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b3864-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3864-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3864-147">-WhatIf</span></span>
<span data-ttu-id="b3864-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b3864-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3864-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b3864-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3864-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3864-150">CommonParameters</span></span>
<span data-ttu-id="b3864-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3864-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3864-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3864-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3864-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b3864-153">INPUTS</span></span>

### <span data-ttu-id="b3864-154">Microsoft. Azure. commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="b3864-154">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="b3864-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3864-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b3864-156">System. string []</span><span class="sxs-lookup"><span data-stu-id="b3864-156">System.String[]</span></span>

### <span data-ttu-id="b3864-157">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="b3864-157">System.TimeSpan</span></span>

### <span data-ttu-id="b3864-158">Microsoft. Azure. commands. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="b3864-158">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="b3864-159">Microsoft. Azure. commands. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="b3864-159">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="b3864-160">System. String</span><span class="sxs-lookup"><span data-stu-id="b3864-160">System.String</span></span>

## <span data-ttu-id="b3864-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b3864-161">OUTPUTS</span></span>

### <span data-ttu-id="b3864-162">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3864-162">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="b3864-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b3864-163">NOTES</span></span>

## <span data-ttu-id="b3864-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b3864-164">RELATED LINKS</span></span>
