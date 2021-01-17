---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98389178"
---
# <span data-ttu-id="be27a-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="be27a-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="be27a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be27a-102">SYNOPSIS</span></span>
<span data-ttu-id="be27a-103">Distribuerar DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="be27a-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="be27a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be27a-104">SYNTAX</span></span>

### <span data-ttu-id="be27a-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="be27a-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be27a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="be27a-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be27a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be27a-107">DESCRIPTION</span></span>
<span data-ttu-id="be27a-108">Cmdleten **Start-AzAutomationDscNodeConfigurationDeployment** distribuerar en önskad konfiguration för DSC-konfiguration i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="be27a-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="be27a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be27a-109">EXAMPLES</span></span>

### <span data-ttu-id="be27a-110">Exempel 1: Distribuera en Azure DSC-noduppsättning i Automation</span><span class="sxs-lookup"><span data-stu-id="be27a-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="be27a-111">Kommandot ovan distribuerar DSC-nodadressen med namnet "Config01. Node1" till den angivna tvådimensionella matrisen med nodnamn.</span><span class="sxs-lookup"><span data-stu-id="be27a-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="be27a-112">Distributionen sker på ett stadium sätt.</span><span class="sxs-lookup"><span data-stu-id="be27a-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="be27a-113">Exempel 2: schemalägga distribution av en Azure DSC-nodkonfigurationer i Automation</span><span class="sxs-lookup"><span data-stu-id="be27a-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

<span data-ttu-id="be27a-114">Med kommandot ovan schemaläggs en distribution av DSC-nodkonfigurationer med namnet "Config01. Node1" till den angivna tvådimensionella matrisen med nodnamn.</span><span class="sxs-lookup"><span data-stu-id="be27a-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="be27a-115">Distributionen sker på ett stadium sätt och utförs utifrån schemat.</span><span class="sxs-lookup"><span data-stu-id="be27a-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="be27a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be27a-116">PARAMETERS</span></span>

### <span data-ttu-id="be27a-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="be27a-117">-AutomationAccountName</span></span>
<span data-ttu-id="be27a-118">Anger namnet på det Automation-konto som innehåller DSC-konfigurationen som kompileras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be27a-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="be27a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be27a-119">-DefaultProfile</span></span>
<span data-ttu-id="be27a-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="be27a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be27a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="be27a-121">-Force</span></span>
<span data-ttu-id="be27a-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="be27a-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be27a-123">-InputObject</span></span>
<span data-ttu-id="be27a-124">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="be27a-124">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="be27a-125">-NodeConfigurationName</span></span>
<span data-ttu-id="be27a-126">Anger namnet på DSC-nodkonfigurationer som denna cmdlet distribuerar.</span><span class="sxs-lookup"><span data-stu-id="be27a-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-127">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="be27a-127">-NodeName</span></span>
<span data-ttu-id="be27a-128">Anger namnen på de noder som nodkonfigurationer ska distribueras till.</span><span class="sxs-lookup"><span data-stu-id="be27a-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be27a-129">-ResourceGroupName</span></span>
<span data-ttu-id="be27a-130">Anger namnet på en resurs grupp där denna cmdlet sammanställer en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="be27a-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="be27a-131">– Schema</span><span class="sxs-lookup"><span data-stu-id="be27a-131">-Schedule</span></span>
<span data-ttu-id="be27a-132">Automation schema-objekt för schemaläggning av distributions jobb.</span><span class="sxs-lookup"><span data-stu-id="be27a-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="be27a-133">-Confirm</span></span>
<span data-ttu-id="be27a-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="be27a-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be27a-135">-WhatIf</span></span>
<span data-ttu-id="be27a-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="be27a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be27a-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="be27a-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be27a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be27a-138">CommonParameters</span></span>
<span data-ttu-id="be27a-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be27a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be27a-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be27a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be27a-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be27a-141">INPUTS</span></span>

### <span data-ttu-id="be27a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="be27a-142">System.String</span></span>

### <span data-ttu-id="be27a-143">Microsoft. Azure. commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="be27a-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="be27a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be27a-144">OUTPUTS</span></span>

### <span data-ttu-id="be27a-145">Microsoft. Azure. commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="be27a-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="be27a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be27a-146">NOTES</span></span>

## <span data-ttu-id="be27a-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be27a-147">RELATED LINKS</span></span>

[<span data-ttu-id="be27a-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="be27a-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="be27a-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="be27a-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="be27a-150">Stopp-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="be27a-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="be27a-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="be27a-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="be27a-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="be27a-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="be27a-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="be27a-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
