---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 889318c911ae6f34b3655583ea2e9693da3bf80f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578592"
---
# <span data-ttu-id="5f64b-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5f64b-101">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="5f64b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f64b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f64b-103">Får distribution av DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="5f64b-103">Gets DSC Node configuration deployments in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f64b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f64b-104">SYNTAX</span></span>

### <span data-ttu-id="5f64b-105">ByAll (standard)</span><span class="sxs-lookup"><span data-stu-id="5f64b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment [[-Status] <String>] [[-StartTime] <DateTimeOffset>]
 [[-EndTime] <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f64b-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="5f64b-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f64b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f64b-107">DESCRIPTION</span></span>
<span data-ttu-id="5f64b-108">Cmdleten **Get-AzureRmAutomationDscNodeConfigurationDeployment** distribuerar en DSC-noduppsättning (Desired State Configuration) i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5f64b-108">The **Get-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="5f64b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f64b-109">EXAMPLES</span></span>

### <span data-ttu-id="5f64b-110">Exempel 1: Hämta en distribution av en datornod</span><span class="sxs-lookup"><span data-stu-id="5f64b-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="5f64b-111">Kommandot ovan distribuerar DSC-nodadressen med namnet "Config01. Node1" till den angivna tvådimensionella matrisen med nodnamn.</span><span class="sxs-lookup"><span data-stu-id="5f64b-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="5f64b-112">Distributionen sker på ett stadium sätt.</span><span class="sxs-lookup"><span data-stu-id="5f64b-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="5f64b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f64b-113">PARAMETERS</span></span>

### <span data-ttu-id="5f64b-114">-JobId</span><span class="sxs-lookup"><span data-stu-id="5f64b-114">-JobId</span></span>
<span data-ttu-id="5f64b-115">Anger jobb-ID för ett befintligt distributions jobb.</span><span class="sxs-lookup"><span data-stu-id="5f64b-115">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="5f64b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f64b-116">-ResourceGroupName</span></span>
<span data-ttu-id="5f64b-117">Anger namnet på en resurs grupp där denna cmdlet sammanställer en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5f64b-117">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="5f64b-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f64b-118">-AutomationAccountName</span></span>
<span data-ttu-id="5f64b-119">Anger namnet på det Automation-konto som innehåller DSC-konfigurationen som kompileras av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f64b-119">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="5f64b-120">-Status</span><span class="sxs-lookup"><span data-stu-id="5f64b-120">-Status</span></span>
<span data-ttu-id="5f64b-121">Status för jobb filtret.</span><span class="sxs-lookup"><span data-stu-id="5f64b-121">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f64b-122">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5f64b-122">-StartTime</span></span>
<span data-ttu-id="5f64b-123">Start tids filter.</span><span class="sxs-lookup"><span data-stu-id="5f64b-123">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f64b-124">-Slut tid</span><span class="sxs-lookup"><span data-stu-id="5f64b-124">-EndTime</span></span>
<span data-ttu-id="5f64b-125">Filter för slut tid.</span><span class="sxs-lookup"><span data-stu-id="5f64b-125">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f64b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f64b-126">-DefaultProfile</span></span>
<span data-ttu-id="5f64b-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f64b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f64b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f64b-128">CommonParameters</span></span>
<span data-ttu-id="5f64b-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f64b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f64b-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f64b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f64b-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f64b-131">INPUTS</span></span>

## <span data-ttu-id="5f64b-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f64b-132">OUTPUTS</span></span>

### <span data-ttu-id="5f64b-133">Microsoft. Azure. commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5f64b-133">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="5f64b-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f64b-134">NOTES</span></span>

## <span data-ttu-id="5f64b-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f64b-135">RELATED LINKS</span></span>

[<span data-ttu-id="5f64b-136">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5f64b-136">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="5f64b-137">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5f64b-137">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="5f64b-138">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5f64b-138">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5f64b-139">Stopp-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5f64b-139">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5f64b-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="5f64b-140">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
