---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 4810fe549f0edd109d83391e3df56916ec48b8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745584"
---
# <span data-ttu-id="94896-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="94896-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="94896-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="94896-102">SYNOPSIS</span></span>
<span data-ttu-id="94896-103">Får distribution av DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="94896-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="94896-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="94896-104">SYNTAX</span></span>

### <span data-ttu-id="94896-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="94896-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94896-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="94896-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94896-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="94896-107">DESCRIPTION</span></span>
<span data-ttu-id="94896-108">Cmdleten **Get-AzAutomationDscNodeConfigurationDeployment** distribuerar en DSC-noduppsättning (Desired State Configuration) i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="94896-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="94896-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="94896-109">EXAMPLES</span></span>

### <span data-ttu-id="94896-110">Exempel 1: Hämta en distribution av en datornod</span><span class="sxs-lookup"><span data-stu-id="94896-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="94896-111">Kommandot ovan distribuerar DSC-nodadressen med namnet "Config01. Node1" till den angivna tvådimensionella matrisen med nodnamn.</span><span class="sxs-lookup"><span data-stu-id="94896-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="94896-112">Distributionen sker på ett stadium sätt.</span><span class="sxs-lookup"><span data-stu-id="94896-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="94896-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="94896-113">PARAMETERS</span></span>

### <span data-ttu-id="94896-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94896-114">-AutomationAccountName</span></span>
<span data-ttu-id="94896-115">Anger namnet på det Automation-konto som innehåller DSC-konfigurationen som kompileras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94896-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="94896-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94896-116">-DefaultProfile</span></span>
<span data-ttu-id="94896-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="94896-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94896-118">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="94896-118">-EndTime</span></span>
<span data-ttu-id="94896-119">Filter för slut tid.</span><span class="sxs-lookup"><span data-stu-id="94896-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94896-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="94896-120">-JobId</span></span>
<span data-ttu-id="94896-121">Anger jobb-ID för ett befintligt distributions jobb.</span><span class="sxs-lookup"><span data-stu-id="94896-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94896-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94896-122">-ResourceGroupName</span></span>
<span data-ttu-id="94896-123">Anger namnet på en resurs grupp där denna cmdlet sammanställer en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="94896-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="94896-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="94896-124">-StartTime</span></span>
<span data-ttu-id="94896-125">Start tids filter.</span><span class="sxs-lookup"><span data-stu-id="94896-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94896-126">-Status</span><span class="sxs-lookup"><span data-stu-id="94896-126">-Status</span></span>
<span data-ttu-id="94896-127">Status för jobb filtret.</span><span class="sxs-lookup"><span data-stu-id="94896-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94896-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94896-128">CommonParameters</span></span>
<span data-ttu-id="94896-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94896-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94896-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94896-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94896-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="94896-131">INPUTS</span></span>

### <span data-ttu-id="94896-132">System. GUID</span><span class="sxs-lookup"><span data-stu-id="94896-132">System.Guid</span></span>

### <span data-ttu-id="94896-133">System. String</span><span class="sxs-lookup"><span data-stu-id="94896-133">System.String</span></span>

## <span data-ttu-id="94896-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="94896-134">OUTPUTS</span></span>

### <span data-ttu-id="94896-135">Microsoft. Azure. commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="94896-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="94896-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="94896-136">NOTES</span></span>

## <span data-ttu-id="94896-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="94896-137">RELATED LINKS</span></span>

[<span data-ttu-id="94896-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="94896-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="94896-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="94896-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="94896-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="94896-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="94896-141">Stopp-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="94896-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="94896-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="94896-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)