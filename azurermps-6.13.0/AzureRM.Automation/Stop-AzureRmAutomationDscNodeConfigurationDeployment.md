---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/stop-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 466cb31bd5e05235085fbc4f9045cf201a806e11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574040"
---
# <span data-ttu-id="4b480-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="4b480-101">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="4b480-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b480-102">SYNOPSIS</span></span>
<span data-ttu-id="4b480-103">Stoppar en distribution av DSC-nodkonfigurationer i Automation.</span><span class="sxs-lookup"><span data-stu-id="4b480-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="4b480-104">Det här stoppar bara det aktuella distributions jobbet, men tar inte bort tilldelade nodkonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="4b480-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b480-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b480-105">SYNTAX</span></span>

### <span data-ttu-id="4b480-106">ByJobId (standard)</span><span class="sxs-lookup"><span data-stu-id="4b480-106">ByJobId (Default)</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b480-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4b480-107">ByInputObject</span></span>
```
Stop-AzureRmAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b480-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b480-108">DESCRIPTION</span></span>
<span data-ttu-id="4b480-109">Cmdleten **Stop-AzureRmAutomationDscNodeConfigurationDeployment** stoppar en distribution av en Desired Configuration (DSC)-noduppsättning i Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4b480-109">The **Stop-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="4b480-110">Den avbryter tilldelningen av nodkonfigurationer till grupper med noder, om det finns en resterande nod som inte redan har tilldelats.</span><span class="sxs-lookup"><span data-stu-id="4b480-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="4b480-111">För att avregistrera ett schemalagt jobb, Använd [unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) med JobScheduleId för att ta bort tilldelningen av ett befintligt schemalagt jobb.</span><span class="sxs-lookup"><span data-stu-id="4b480-111">To unregister a scheduled job, please use the [Unregister-AzureRmAutomationScheduledRunbook](./Unregister-AzureRmAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="4b480-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b480-112">EXAMPLES</span></span>

### <span data-ttu-id="4b480-113">Exempel 1: Distribuera en Azure DSC-noduppsättning i Automation</span><span class="sxs-lookup"><span data-stu-id="4b480-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzureRmAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="4b480-114">Kommandot ovan stoppar distributions jobbet för DSC-nodkonfigurationer med det skickade jobId.</span><span class="sxs-lookup"><span data-stu-id="4b480-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="4b480-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b480-115">PARAMETERS</span></span>

### <span data-ttu-id="4b480-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4b480-116">-AutomationAccountName</span></span>
<span data-ttu-id="4b480-117">Anger namnet på det Automation-konto som innehåller DSC-konfigurationen som kompileras med den här cmdleten</span><span class="sxs-lookup"><span data-stu-id="4b480-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="4b480-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b480-118">-DefaultProfile</span></span>
<span data-ttu-id="4b480-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4b480-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b480-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4b480-120">-Force</span></span>
<span data-ttu-id="4b480-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="4b480-121">ps_force</span></span>

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

### <span data-ttu-id="4b480-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b480-122">-InputObject</span></span>
<span data-ttu-id="4b480-123">Indatavärdet för överföring</span><span class="sxs-lookup"><span data-stu-id="4b480-123">Input object for Piping</span></span>

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

### <span data-ttu-id="4b480-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="4b480-124">-JobId</span></span>
<span data-ttu-id="4b480-125">Anger jobb-ID för ett befintligt distributions jobb.</span><span class="sxs-lookup"><span data-stu-id="4b480-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="4b480-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b480-126">-PassThru</span></span>
<span data-ttu-id="4b480-127">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4b480-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4b480-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4b480-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4b480-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b480-129">-ResourceGroupName</span></span>
<span data-ttu-id="4b480-130">Anger namnet på en resurs grupp där denna cmdlet sammanställer en konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4b480-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="4b480-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b480-131">-Confirm</span></span>
<span data-ttu-id="4b480-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b480-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b480-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b480-133">-WhatIf</span></span>
<span data-ttu-id="4b480-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b480-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b480-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b480-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b480-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b480-136">CommonParameters</span></span>
<span data-ttu-id="4b480-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b480-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b480-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b480-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b480-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b480-139">INPUTS</span></span>

### <span data-ttu-id="4b480-140">System. GUID</span><span class="sxs-lookup"><span data-stu-id="4b480-140">System.Guid</span></span>

### <span data-ttu-id="4b480-141">Microsoft. Azure. commands. Automation. Model. NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="4b480-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>
<span data-ttu-id="4b480-142">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4b480-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4b480-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4b480-143">System.String</span></span>

## <span data-ttu-id="4b480-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b480-144">OUTPUTS</span></span>

### <span data-ttu-id="4b480-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b480-145">System.Boolean</span></span>

## <span data-ttu-id="4b480-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b480-146">NOTES</span></span>

## <span data-ttu-id="4b480-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b480-147">RELATED LINKS</span></span>

[<span data-ttu-id="4b480-148">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="4b480-148">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="4b480-149">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b480-149">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="4b480-150">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="4b480-150">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="4b480-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="4b480-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="4b480-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="4b480-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)
