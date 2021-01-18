---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d93820d12a2f61714c58341f835bef8cba832b84
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524954"
---
# <span data-ttu-id="296e8-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="296e8-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="296e8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="296e8-102">SYNOPSIS</span></span>
<span data-ttu-id="296e8-103">Hämtar en lista med program uppdateringar för Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="296e8-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="296e8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="296e8-104">SYNTAX</span></span>

### <span data-ttu-id="296e8-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="296e8-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="296e8-106">ById</span><span class="sxs-lookup"><span data-stu-id="296e8-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="296e8-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="296e8-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="296e8-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="296e8-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="296e8-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="296e8-109">DESCRIPTION</span></span>
<span data-ttu-id="296e8-110">Get-AzAutomationSoftwareUpdateRun cmdlet returnerar en lista med program uppdateringar körs.</span><span class="sxs-lookup"><span data-stu-id="296e8-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="296e8-111">Eftersom en konfiguration för program uppdatering har ett associerat schema kan det utlösas flera gånger.</span><span class="sxs-lookup"><span data-stu-id="296e8-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="296e8-112">Varje gång ett schema utlöses kommer en uppdaterings körning att skapas.</span><span class="sxs-lookup"><span data-stu-id="296e8-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="296e8-113">Uppdaterings körning är en mängd av resultatet av att alla datorer körs.</span><span class="sxs-lookup"><span data-stu-id="296e8-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="296e8-114">Du kan komma igång med viss konfiguration av program uppdateringar genom att skicka parametern SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="296e8-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="296e8-115">Om du vill ha ett specifikt kör-värde måste du skicka namnet parameter.</span><span class="sxs-lookup"><span data-stu-id="296e8-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="296e8-116">Du kan också visa en lista med specifik status, köra det riktade specifika operativ systemet eller köra det efter en viss tid genom att skicka en lämplig parameter.</span><span class="sxs-lookup"><span data-stu-id="296e8-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="296e8-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="296e8-117">EXAMPLES</span></span>

### <span data-ttu-id="296e8-118">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="296e8-118">Example 1</span></span>
<span data-ttu-id="296e8-119">I det här exemplet visas alla uppdateringar som aktive ras av en viss konfiguration för program uppdateringar.</span><span class="sxs-lookup"><span data-stu-id="296e8-119">This example list all update runs triggered by a specific software update configuration.</span></span>

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

## <span data-ttu-id="296e8-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="296e8-120">PARAMETERS</span></span>

### <span data-ttu-id="296e8-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="296e8-121">-AutomationAccountName</span></span>
<span data-ttu-id="296e8-122">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="296e8-122">The automation account name.</span></span>

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

### <span data-ttu-id="296e8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="296e8-123">-DefaultProfile</span></span>
<span data-ttu-id="296e8-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="296e8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="296e8-125">-ID</span><span class="sxs-lookup"><span data-stu-id="296e8-125">-Id</span></span>
<span data-ttu-id="296e8-126">ID för körning av program uppdaterings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="296e8-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="296e8-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="296e8-127">-OperatingSystem</span></span>
<span data-ttu-id="296e8-128">Operativ systemet för kör.</span><span class="sxs-lookup"><span data-stu-id="296e8-128">The operating system of the run.</span></span>

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

### <span data-ttu-id="296e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="296e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="296e8-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="296e8-130">The resource group name.</span></span>

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

### <span data-ttu-id="296e8-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="296e8-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="296e8-132">Konfiguration av program uppdatering utlöste körningen.</span><span class="sxs-lookup"><span data-stu-id="296e8-132">The software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="296e8-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="296e8-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="296e8-134">Namnet på program uppdaterings konfigurationen utlöste körningen.</span><span class="sxs-lookup"><span data-stu-id="296e8-134">Name of the software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="296e8-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="296e8-135">-StartTime</span></span>
<span data-ttu-id="296e8-136">Minsta start tid för kör.</span><span class="sxs-lookup"><span data-stu-id="296e8-136">Minimum start time of the run.</span></span>

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

### <span data-ttu-id="296e8-137">-Status</span><span class="sxs-lookup"><span data-stu-id="296e8-137">-Status</span></span>
<span data-ttu-id="296e8-138">Status för kör.</span><span class="sxs-lookup"><span data-stu-id="296e8-138">Status of the run.</span></span>

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

### <span data-ttu-id="296e8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="296e8-139">CommonParameters</span></span>
<span data-ttu-id="296e8-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="296e8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="296e8-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="296e8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="296e8-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="296e8-142">INPUTS</span></span>

### <span data-ttu-id="296e8-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="296e8-143">System.Guid</span></span>

### <span data-ttu-id="296e8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="296e8-144">System.String</span></span>

### <span data-ttu-id="296e8-145">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="296e8-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="296e8-146">System. Nullable ' 1 [[Microsoft. Azure. kommandon. Automation. Model. UpdateManagement. OperatingSystemType, Microsoft. Azure. PowerShell. cmdletar. Automation, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="296e8-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="296e8-147">System. Nullable ' 1 [[Microsoft. Azure. kommandon. Automation. Model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. PowerShell. cmdletar. Automation, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="296e8-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="296e8-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="296e8-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="296e8-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="296e8-149">OUTPUTS</span></span>

### <span data-ttu-id="296e8-150">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="296e8-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="296e8-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="296e8-151">NOTES</span></span>

## <span data-ttu-id="296e8-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="296e8-152">RELATED LINKS</span></span>
