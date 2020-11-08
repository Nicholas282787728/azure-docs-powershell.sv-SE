---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088194"
---
# <span data-ttu-id="5bf8c-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5bf8c-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="5bf8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bf8c-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf8c-103">Stoppar en distribution av DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="5bf8c-104">Det här stoppar bara det aktuella distributions jobbet, men tar inte bort tilldelade nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="5bf8c-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bf8c-105">SYNTAX</span></span>

### <span data-ttu-id="5bf8c-106">ByJobId (standard)</span><span class="sxs-lookup"><span data-stu-id="5bf8c-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bf8c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5bf8c-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5bf8c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bf8c-108">DESCRIPTION</span></span>
<span data-ttu-id="5bf8c-109">Cmdleten **Stop-AzAutomationDscNodeConfigurationDeployment** stoppar en distribution av en Desired Configuration (DSC)-noduppsättning i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="5bf8c-110">Den avbryter tilldelningen av nodkonfigurationer till grupper med noder, om det finns en resterande nod som inte redan har tilldelats.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="5bf8c-111">För att avregistrera ett schemalagt jobb, Använd [unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) med JobScheduleId för att ta bort tilldelningen av ett befintligt schemalagt jobb.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="5bf8c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bf8c-112">EXAMPLES</span></span>

### <span data-ttu-id="5bf8c-113">Exempel 1: Distribuera en Azure DSC-noduppsättning i Automation</span><span class="sxs-lookup"><span data-stu-id="5bf8c-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="5bf8c-114">Kommandot ovan stoppar distributions jobbet för DSC-nodkonfigurationer med det skickade jobId.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="5bf8c-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bf8c-115">PARAMETERS</span></span>

### <span data-ttu-id="5bf8c-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5bf8c-116">-AutomationAccountName</span></span>
<span data-ttu-id="5bf8c-117">Anger namnet på det Automation-konto som innehåller DSC-konfigurationen som kompileras med den här cmdleten</span><span class="sxs-lookup"><span data-stu-id="5bf8c-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="5bf8c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bf8c-118">-DefaultProfile</span></span>
<span data-ttu-id="5bf8c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5bf8c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bf8c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5bf8c-120">-Force</span></span>
<span data-ttu-id="5bf8c-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="5bf8c-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf8c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bf8c-122">-InputObject</span></span>
<span data-ttu-id="5bf8c-123">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="5bf8c-123">Input object for Piping</span></span>

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

### <span data-ttu-id="5bf8c-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="5bf8c-124">-JobId</span></span>
<span data-ttu-id="5bf8c-125">Anger jobb-ID för ett befintligt distributions jobb.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="5bf8c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bf8c-126">-PassThru</span></span>
<span data-ttu-id="5bf8c-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5bf8c-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5bf8c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bf8c-129">-ResourceGroupName</span></span>
<span data-ttu-id="5bf8c-130">Anger namnet på en resurs grupp där denna cmdlet sammanställer en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="5bf8c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5bf8c-131">-Confirm</span></span>
<span data-ttu-id="5bf8c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bf8c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bf8c-133">-WhatIf</span></span>
<span data-ttu-id="5bf8c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bf8c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bf8c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf8c-136">CommonParameters</span></span>
<span data-ttu-id="5bf8c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf8c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf8c-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf8c-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf8c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bf8c-139">INPUTS</span></span>

### <span data-ttu-id="5bf8c-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="5bf8c-140">System.Guid</span></span>

### <span data-ttu-id="5bf8c-141">Microsoft. Azure. commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5bf8c-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="5bf8c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5bf8c-142">System.String</span></span>

## <span data-ttu-id="5bf8c-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bf8c-143">OUTPUTS</span></span>

### <span data-ttu-id="5bf8c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5bf8c-144">System.Boolean</span></span>

## <span data-ttu-id="5bf8c-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bf8c-145">NOTES</span></span>

## <span data-ttu-id="5bf8c-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bf8c-146">RELATED LINKS</span></span>

[<span data-ttu-id="5bf8c-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5bf8c-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="5bf8c-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5bf8c-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="5bf8c-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5bf8c-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5bf8c-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5bf8c-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5bf8c-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="5bf8c-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)