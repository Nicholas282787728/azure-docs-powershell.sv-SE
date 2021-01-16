---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 19c0321b1c915519b7c3617b52810da18e534521
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418616"
---
# <span data-ttu-id="95365-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="95365-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="95365-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95365-102">SYNOPSIS</span></span>
<span data-ttu-id="95365-103">Hämtar en lista med konfigurations dator för Azure Automation-programmet.</span><span class="sxs-lookup"><span data-stu-id="95365-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="95365-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95365-104">SYNTAX</span></span>

### <span data-ttu-id="95365-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="95365-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="95365-106">ById</span><span class="sxs-lookup"><span data-stu-id="95365-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95365-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="95365-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95365-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="95365-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95365-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95365-109">DESCRIPTION</span></span>
<span data-ttu-id="95365-110">Denna cmdlet returnerar en lista med datorer som körs.</span><span class="sxs-lookup"><span data-stu-id="95365-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="95365-111">Varje program uppdaterings körning kommer att utlösa en dator körning för var och en av datorerna för program uppdaterings konfiguration.</span><span class="sxs-lookup"><span data-stu-id="95365-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="95365-112">Om du vill hämta en speciell dator kör du parametern ID.</span><span class="sxs-lookup"><span data-stu-id="95365-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="95365-113">Du kan ange att all dator kör, alla körs för en viss dator, alla körs med specifik status genom att överföra motsvarande parametrar.</span><span class="sxs-lookup"><span data-stu-id="95365-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="95365-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95365-114">EXAMPLES</span></span>

### <span data-ttu-id="95365-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="95365-115">Example 1</span></span>
<span data-ttu-id="95365-116">I det här exemplet returneras alla misslyckade dator körningar för den angivna virtuella Azure-datorn.</span><span class="sxs-lookup"><span data-stu-id="95365-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
                                                      -AutomationAccountName "myaccount" `
                                                      -TargetComputer $targetComputer `
                                                      -Status Failed

MachineRunId          : 0033d6d6-828d-4712-adab-293cc4fc8809
TargetComputer        : /subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm
TargetComputerType    : AzureVirtualMachines
SoftwareUpdateRunId   : 46568d26-0182-49b2-8bfd-af3455780397
OperatingSystem       : Windows
Status                : Failed
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : 0033d6d6-828d-4712-adab-293cc4fc8809
CreationTime          : 5/17/2018 2:06:44 AM +00:00
LastModifiedTime      : 5/17/2018 2:08:49 AM +00:00
```

## <span data-ttu-id="95365-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95365-117">PARAMETERS</span></span>

### <span data-ttu-id="95365-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="95365-118">-AutomationAccountName</span></span>
<span data-ttu-id="95365-119">Namnet på Automation-kontot.</span><span class="sxs-lookup"><span data-stu-id="95365-119">The automation account name.</span></span>

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

### <span data-ttu-id="95365-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95365-120">-DefaultProfile</span></span>
<span data-ttu-id="95365-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95365-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95365-122">-ID</span><span class="sxs-lookup"><span data-stu-id="95365-122">-Id</span></span>
<span data-ttu-id="95365-123">ID för program uppdaterings datorn.</span><span class="sxs-lookup"><span data-stu-id="95365-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="95365-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95365-124">-ResourceGroupName</span></span>
<span data-ttu-id="95365-125">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="95365-125">The resource group name.</span></span>

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

### <span data-ttu-id="95365-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="95365-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="95365-127">Program uppdateringen körs.</span><span class="sxs-lookup"><span data-stu-id="95365-127">The software update run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun
Parameter Sets: BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95365-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="95365-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="95365-129">ID för program uppdaterings körningen.</span><span class="sxs-lookup"><span data-stu-id="95365-129">Id of the software update run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: BySucrId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95365-130">-Status</span><span class="sxs-lookup"><span data-stu-id="95365-130">-Status</span></span>
<span data-ttu-id="95365-131">Status för dator körningen.</span><span class="sxs-lookup"><span data-stu-id="95365-131">Status of the machine run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus]
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded, FailedToStart

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95365-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="95365-132">-TargetComputer</span></span>
<span data-ttu-id="95365-133">måldator för datorn.</span><span class="sxs-lookup"><span data-stu-id="95365-133">target computer for the machine run.</span></span>
<span data-ttu-id="95365-134">Kan antingen vara ett icke-AZ dator namn eller ett ID för en Azure VM-resurs.</span><span class="sxs-lookup"><span data-stu-id="95365-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95365-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95365-135">CommonParameters</span></span>
<span data-ttu-id="95365-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95365-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95365-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95365-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95365-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95365-138">INPUTS</span></span>

### <span data-ttu-id="95365-139">System. GUID</span><span class="sxs-lookup"><span data-stu-id="95365-139">System.Guid</span></span>

### <span data-ttu-id="95365-140">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="95365-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="95365-141">System. Nullable ' 1 [[Microsoft. Azure. kommandon. Automation. Model. UpdateManagement. SoftwareUpdateMachineRunStatus, Microsoft. Azure. PowerShell. cmdletar. Automation, version = 1.0.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="95365-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="95365-142">System. String</span><span class="sxs-lookup"><span data-stu-id="95365-142">System.String</span></span>

## <span data-ttu-id="95365-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95365-143">OUTPUTS</span></span>

### <span data-ttu-id="95365-144">Microsoft. Azure. commands. Automation. Model. UpdateManagement. SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="95365-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="95365-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95365-145">NOTES</span></span>

## <span data-ttu-id="95365-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95365-146">RELATED LINKS</span></span>
