---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: c866a1e4a703938e5ef860af3760b4bbb082fc3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745549"
---
# <span data-ttu-id="9e0d2-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="9e0d2-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="9e0d2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e0d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0d2-103">Hämtar en lista med program uppdateringar för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="9e0d2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e0d2-104">SYNTAX</span></span>

### <span data-ttu-id="9e0d2-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="9e0d2-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e0d2-106">ById</span><span class="sxs-lookup"><span data-stu-id="9e0d2-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e0d2-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="9e0d2-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e0d2-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="9e0d2-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e0d2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e0d2-109">DESCRIPTION</span></span>
<span data-ttu-id="9e0d2-110">Get-AzAutomationSoftwareUpdateRun cmdlet returnerar en lista med program uppdateringar körs.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="9e0d2-111">Eftersom en konfiguration för program uppdatering har ett associerat schema kan det utlösas flera gånger.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="9e0d2-112">Varje gång ett schema utlöses kommer en uppdaterings körning att skapas.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="9e0d2-113">Uppdaterings körning är en mängd av resultatet av att alla datorer körs.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="9e0d2-114">Du kan komma igång med viss konfiguration av program uppdateringar genom att skicka parametern SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="9e0d2-115">Om du vill ha ett specifikt kör-värde måste du skicka namnet parameter.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="9e0d2-116">Du kan också visa en lista med specifik status, köra det riktade specifika operativ systemet eller köra det efter en viss tid genom att skicka en lämplig parameter.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="9e0d2-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e0d2-117">EXAMPLES</span></span>

### <span data-ttu-id="9e0d2-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9e0d2-118">Example 1</span></span>
<span data-ttu-id="9e0d2-119">I det här exemplet visas alla uppdateringar som aktive ras av en viss konfiguration för program uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="9e0d2-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e0d2-120">PARAMETERS</span></span>

### <span data-ttu-id="9e0d2-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9e0d2-121">-AutomationAccountName</span></span>
<span data-ttu-id="9e0d2-122">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-122">The automation account name.</span></span>

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

### <span data-ttu-id="9e0d2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e0d2-123">-DefaultProfile</span></span>
<span data-ttu-id="9e0d2-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e0d2-125">-ID</span><span class="sxs-lookup"><span data-stu-id="9e0d2-125">-Id</span></span>
<span data-ttu-id="9e0d2-126">ID för körning av program uppdaterings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-126">Id of the software update configuration run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d2-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="9e0d2-127">-OperatingSystem</span></span>
<span data-ttu-id="9e0d2-128">Operativ systemet för kör.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e0d2-129">-ResourceGroupName</span></span>
<span data-ttu-id="9e0d2-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-130">The resource group name.</span></span>

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

### <span data-ttu-id="9e0d2-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e0d2-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="9e0d2-132">Konfiguration av program uppdatering utlöste körningen.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d2-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9e0d2-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="9e0d2-134">Namnet på program uppdaterings konfigurationen utlöste körningen.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d2-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9e0d2-135">-StartTime</span></span>
<span data-ttu-id="9e0d2-136">Minsta start tid för kör.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d2-137">-Status</span><span class="sxs-lookup"><span data-stu-id="9e0d2-137">-Status</span></span>
<span data-ttu-id="9e0d2-138">Status för kör.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0d2-139">CommonParameters</span></span>
<span data-ttu-id="9e0d2-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e0d2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0d2-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e0d2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0d2-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e0d2-142">INPUTS</span></span>

### <span data-ttu-id="9e0d2-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="9e0d2-143">System.Guid</span></span>

### <span data-ttu-id="9e0d2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9e0d2-144">System.String</span></span>

### <span data-ttu-id="9e0d2-145">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e0d2-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="9e0d2-146">System. Nullable ' 1 [[Microsoft. Azure. kommandon. Automation. Model. UpdateManagement. OperatingSystemType, Microsoft. Azure. PowerShell. cmdletar. Automation, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9e0d2-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9e0d2-147">System. Nullable ' 1 [[Microsoft. Azure. kommandon. Automation. Model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. PowerShell. cmdletar. Automation, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9e0d2-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9e0d2-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9e0d2-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="9e0d2-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e0d2-149">OUTPUTS</span></span>

### <span data-ttu-id="9e0d2-150">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="9e0d2-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="9e0d2-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e0d2-151">NOTES</span></span>

## <span data-ttu-id="9e0d2-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e0d2-152">RELATED LINKS</span></span>
