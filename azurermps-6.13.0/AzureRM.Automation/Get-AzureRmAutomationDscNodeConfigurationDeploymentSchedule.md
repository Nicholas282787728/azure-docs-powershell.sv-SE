---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: f29c4f5587b79fdc2c6eb03907ed5c1327406e8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756725"
---
# <span data-ttu-id="648ff-101">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="648ff-101">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="648ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="648ff-102">SYNOPSIS</span></span>
<span data-ttu-id="648ff-103">Hämtar en distributions jobb schema för DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="648ff-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="648ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="648ff-104">SYNTAX</span></span>

### <span data-ttu-id="648ff-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="648ff-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="648ff-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="648ff-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="648ff-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="648ff-107">DESCRIPTION</span></span>
<span data-ttu-id="648ff-108">Cmdleten **Get-AzureRmAutomationDscNodeConfigurationDeployment** distribuerar en DSC-noduppsättning (Desired State Configuration) i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="648ff-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="648ff-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="648ff-109">EXAMPLES</span></span>

### <span data-ttu-id="648ff-110">Exempel 1: få alla distributions scheman</span><span class="sxs-lookup"><span data-stu-id="648ff-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="648ff-111">Exempel 2: skaffa ett distributions schema</span><span class="sxs-lookup"><span data-stu-id="648ff-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="648ff-112">Kommandot ovan distribuerar DSC-nodadressen med namnet "Config01. Node1" till den angivna tvådimensionella matrisen med nodnamn.</span><span class="sxs-lookup"><span data-stu-id="648ff-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="648ff-113">Distributionen sker på ett stadium sätt.</span><span class="sxs-lookup"><span data-stu-id="648ff-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="648ff-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="648ff-114">PARAMETERS</span></span>

### <span data-ttu-id="648ff-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="648ff-115">-AutomationAccountName</span></span>
<span data-ttu-id="648ff-116">Anger namnet på det Automation-konto som innehåller DSC-konfigurationen som kompileras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="648ff-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="648ff-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="648ff-117">-DefaultProfile</span></span>
<span data-ttu-id="648ff-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="648ff-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="648ff-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="648ff-119">-JobScheduleId</span></span>
<span data-ttu-id="648ff-120">Anger schema-ID för jobbet för ett befintligt schemalagt distributions jobb.</span><span class="sxs-lookup"><span data-stu-id="648ff-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="648ff-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="648ff-121">-ResourceGroupName</span></span>
<span data-ttu-id="648ff-122">Anger namnet på en resurs grupp där denna cmdlet sammanställer en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="648ff-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="648ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="648ff-123">CommonParameters</span></span>
<span data-ttu-id="648ff-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="648ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="648ff-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="648ff-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="648ff-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="648ff-126">INPUTS</span></span>

### <span data-ttu-id="648ff-127">System. GUID</span><span class="sxs-lookup"><span data-stu-id="648ff-127">System.Guid</span></span>

### <span data-ttu-id="648ff-128">System. String</span><span class="sxs-lookup"><span data-stu-id="648ff-128">System.String</span></span>

## <span data-ttu-id="648ff-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="648ff-129">OUTPUTS</span></span>

### <span data-ttu-id="648ff-130">Microsoft. Azure. commands. Automation. Model. NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="648ff-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="648ff-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="648ff-131">NOTES</span></span>

## <span data-ttu-id="648ff-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="648ff-132">RELATED LINKS</span></span>

[<span data-ttu-id="648ff-133">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="648ff-133">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="648ff-134">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="648ff-134">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="648ff-135">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="648ff-135">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="648ff-136">Stopp-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="648ff-136">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="648ff-137">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="648ff-137">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)
