---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521276"
---
# <span data-ttu-id="52c67-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="52c67-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="52c67-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="52c67-102">SYNOPSIS</span></span>
<span data-ttu-id="52c67-103">Avbryta en pågående distribution i en hanterings grupp</span><span class="sxs-lookup"><span data-stu-id="52c67-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="52c67-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="52c67-104">SYNTAX</span></span>

### <span data-ttu-id="52c67-105">StopByDeploymentName (standard)</span><span class="sxs-lookup"><span data-stu-id="52c67-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52c67-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="52c67-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52c67-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="52c67-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52c67-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="52c67-108">DESCRIPTION</span></span>
<span data-ttu-id="52c67-109">Cmdleten **Stop-AzManagementGroupDeployment** avbryter en distribution som har startat men inte slutförts i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="52c67-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="52c67-110">För att stoppa en distribution måste distributionen ha ett ofullständigt etablerings tillstånd, till exempel etablering och inte ett slutfört tillstånd, såsom etablerad eller misslyckad.</span><span class="sxs-lookup"><span data-stu-id="52c67-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="52c67-111">Använd New-AzManagementGroupDeployment cmdlet för att skapa en distribution i en hanterings grupp.</span><span class="sxs-lookup"><span data-stu-id="52c67-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="52c67-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="52c67-112">EXAMPLES</span></span>

### <span data-ttu-id="52c67-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="52c67-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="52c67-114">Det här kommandot avbryter en drift sättning "deployment01" i hanterings gruppen "myMG".</span><span class="sxs-lookup"><span data-stu-id="52c67-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="52c67-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="52c67-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="52c67-116">Det här kommandot får distributionen "deployment01" i hanterings gruppen "myMG" och säger upp det.</span><span class="sxs-lookup"><span data-stu-id="52c67-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="52c67-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="52c67-117">PARAMETERS</span></span>

### <span data-ttu-id="52c67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52c67-118">-DefaultProfile</span></span>
<span data-ttu-id="52c67-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="52c67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52c67-120">-ID</span><span class="sxs-lookup"><span data-stu-id="52c67-120">-Id</span></span>
<span data-ttu-id="52c67-121">Det fullt kvalificerade resurs-ID: t för distributionen.</span><span class="sxs-lookup"><span data-stu-id="52c67-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="52c67-122">exempel:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="52c67-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c67-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52c67-123">-InputObject</span></span>
<span data-ttu-id="52c67-124">Distributions objekt.</span><span class="sxs-lookup"><span data-stu-id="52c67-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52c67-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="52c67-125">-ManagementGroupId</span></span>
<span data-ttu-id="52c67-126">Hanterings gruppens ID.</span><span class="sxs-lookup"><span data-stu-id="52c67-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c67-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="52c67-127">-Name</span></span>
<span data-ttu-id="52c67-128">Namnet på distributionen.</span><span class="sxs-lookup"><span data-stu-id="52c67-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52c67-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52c67-129">-PassThru</span></span>
<span data-ttu-id="52c67-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="52c67-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="52c67-131">-För</span><span class="sxs-lookup"><span data-stu-id="52c67-131">-Pre</span></span>
<span data-ttu-id="52c67-132">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="52c67-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="52c67-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="52c67-133">-Confirm</span></span>
<span data-ttu-id="52c67-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="52c67-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52c67-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52c67-135">-WhatIf</span></span>
<span data-ttu-id="52c67-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="52c67-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52c67-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="52c67-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52c67-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52c67-138">CommonParameters</span></span>
<span data-ttu-id="52c67-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52c67-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52c67-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52c67-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52c67-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="52c67-141">INPUTS</span></span>

### <span data-ttu-id="52c67-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="52c67-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="52c67-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="52c67-143">OUTPUTS</span></span>

### <span data-ttu-id="52c67-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52c67-144">System.Boolean</span></span>

## <span data-ttu-id="52c67-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="52c67-145">NOTES</span></span>

## <span data-ttu-id="52c67-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="52c67-146">RELATED LINKS</span></span>
